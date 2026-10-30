---
title: "Your Agent Needs Search"
date: 2026-10-29
description: "Two days after DeepSeek released its search API, a problem I had been stuck on for two weeks got solved."
---

## The short version

On October 17, DeepSeek released its own search API (two endpoints, Search and Fetch). I connected it to my agent that same day, for a simple reason: Claude Code is what I mainly use, and its built-in search is good enough for English but can't find a lot of the content in Chinese communities. Two days later, it solved a problem I had been stuck on for two weeks.

I want to use this to lay out one view: an agent needs search, and what that search is connected to largely decides how much the agent can get done.

## Agent capability = context × model × harness

This is how I think about agents now: capability is the product of context, model and harness (the tools, workflow and rules around the model). Multiplication means that if any one of them is missing a key piece, the result is wrong, and even a very strong model can't make up for it.

Of the three, the user has little control over the model, the harness can be built up over time, and context is the easiest to overlook and the one you can do the most about.

Where does context come from? One way is that the person volunteers it. The other is that the agent goes and finds it. People can give only so much: they can't give what they don't know, and what they think is right may be wrong (the story below is an example). The more the agent can find by itself, the less the person has to explain, and using it is a completely different experience. And what an agent mainly relies on to find things on its own is search.

Strictly speaking, search is itself part of the harness: it is the channel in the harness whose job is to add things to the context. So the three factors aren't independent: which search channels the harness is connected to decides what can get into the context. Once the model is set, what search is connected to basically sets the ceiling on the context.

## A problem I was stuck on for two weeks

I use a China-market Android phone whose Google services were preinstalled through the manufacturer's channel, and it normally works fine for me in the US. Starting October 7, the Chase Android app asked me to verify my age as soon as I opened it, then said my Google Play Store was out of date, and I couldn't transfer money.

Several US states have passed laws requiring app stores to verify age, and for this step Chase goes through Google Play's services. But the Play Store's settings page said "up to date," and I sent Claude a screenshot of that page.

**First try** (October 7): 3 searches and 1 page fetch, all in English. The suggestion was to update Play and go through Google's age verification. I updated both the Play Store and Play services. It didn't help.

**Second try** (October 18): 7 searches and 3 fetches, again all in English. It found a tally of bad reviews: of the 13 people who reported "Play is too old," 11 said their Play was already up to date. So it decided this was a false alarm from Chase and told me to reinstall the app and clear its data. That didn't help either.

**Third try** (October 19): I switched to a background research agent whose only job was to look into this, and it used the DeepSeek search I had set up for it. One Chinese query turned up two posts. In the phone maker's official community forum, someone with a China-market phone of the same brand as mine was stuck on Play 49.3.28 in the same way, with the same "up to date" message. In a Chinese-language forum about US credit cards, two users of Chinese-brand phones got things working again after installing a newer Play over the old one.

It turns out the "up to date" the Play Store shows on these China-market phones isn't really the latest. I went back and looked, and the screenshot I had sent Claude said 49.x right there, while the current mainline version of Play was already 53.x. Claude then helped me find a site where I could download the Play Store APK, and told me which version to install. I installed 53.5.48, restarted, cleared Chase's storage, and the verification passed on the spot. I finally paid back the money I had owed a friend for two weeks.

## Tracing it back: was it really search?

More than one thing changed between the third try and the first two: I switched to a background agent, it searched many more times, and the main session that sent it out also named Chinese communities in the task description as places to check. So I had an agent go back and scan the research agent's tool-call logs, working backward from each source to the first call whose results contained it.

The third try ran 22 English searches, 23 page fetches and 1 Chinese search. The two posts that decided it both came from that one Chinese query. It was only after getting those two posts that the research agent went to check Play's mainline version, and only then did it put "check the version number first" as step one of its report. None of the 22 English searches went in this direction.

One more detail: the two posts were published on October 1 and October 4. I first asked on October 7, so the answer was already online by then. The problem stayed unsolved for two weeks, and the reason wasn't that the information didn't exist yet. The agent couldn't find it.

All three tries used Claude Opus 5.5, so the model factor didn't change. What turned the result around was one new piece in the context: "people with the same kind of phone have run into exactly the same thing."

## Similar cases show what to doubt

What kept the first two tries stuck, besides missing information, was a piece of wrong information, and I was the one who gave it: the "up to date" in the screenshot. The screenshot was real, but it was only the Play Store's own account of itself. The agent took it as a premise and went looking elsewhere, so that tally of bad reviews got read as "a Chase false alarm" instead of "those 11 people's Play wasn't actually the latest either."

The agent can't find out on its own what the user got wrong. Only after it finds other people who also see "up to date" and are stuck on the same version does it know which claim to go back and doubt. So search does more than fill in missing information; it is also one of the few ways an agent can check the user's premises. I'd like to write a separate post about the problem on the user's side (people can only give what they think is right).

## Search coverage should follow the users

Why couldn't so many English searches find it? Because where the evidence lives depends on where the people who hit the same problem are.

People on a China-market phone with Google services installed, using US apps in the US, discuss their problems on Chinese-language forums. It makes no difference that the conversation is in English or that the app is American. People in the English-speaking world who run into Chase's age verification have phones where Play updates itself, so they never hit this pitfall at all.

So if you build agents, the defaults for search (which channels it connects to, which languages it searches in, which communities it goes to) should follow the information world the user lives in, rather than the language of the conversation or the developer's own defaults.

## Limitations

This is a single case, not a study. The Chinese channels themselves are unreliable too: that day the Reddit, Zhihu and Xiaohongshu channels didn't connect, only DeepSeek's API did, and on another day the result might be different. DeepSeek's search ranks English official pages poorly; for English I still rely on the built-in search. So I am not saying "Chinese search is better." What I am saying is that search coverage should be built as a capability and also watched as a metric.

## Last thoughts

In the past, when we ran into something we didn't know how to do, our first reaction was to Google it or Baidu it, and what we thought about was how to use the search box well: how to write the keywords, which results to trust.

Now I can't even remember the last time I opened a search box. When I run into a problem, my first reaction is to open an agent and ask.

The entry point has changed, so the thing to think about now is how to use agents well. I think a good place to start is giving yours the best search you can. I'll write about my own current search setup in the next post.

## Appendix: if you also use a China-market Android phone

If an app like Chase gets stuck on age verification in the US and says Play is too old, while the Play Store says it's up to date, check the version number in the Play Store settings. If it's still on an old version like 49.x, download the current mainline Play Store from a trusted APK site and install it over the old one (I installed 53.5.48), restart, clear the storage of the app that's giving you trouble, and try again.
