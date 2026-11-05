---
title: "About"
hideMeta: true
ShowToc: false
ShowPostNavLinks: false
---

I use agent products heavily and build on them. My work, study, and daily life run on a personal agent workbench I built on Claude Code and Codex, and I use it every day. I keep a running log of cases where an agent got the task right but didn't do it well, and I trace each failure back to context, tools, or the model.

Before business school, I spent 6+ years as co-founder and Head of Products at United AI, an industrial AI start-up, leading core products from 0 to 1 with a small team. At TikTok, where I've been a Product Manager Intern since May 2026, I work on creator-side products and used agents to build an education video pipeline and a product acceptance workflow. I'm a second-year MBA student at UC Berkeley Haas.

## Education

### University of California, Berkeley, Haas School of Business

**Master of Business Administration** · Expected May 2027

### The Hong Kong University of Science and Technology

**Master of Science in Data-Driven Modeling** · Nov 2023

### Tsinghua University

**Bachelor of Engineering, Electrical Engineering** · May 2017

- Chinese Physics Olympiad (CPhO), Silver Medal (2012); admitted to Tsinghua without the national college entrance exam
- National College Students Physics Competition, First Prize (2015)
- Tsinghua "Challenge Cup", Special Prize (top 5 of 100+ projects); Tsinghua President's Innovation Challenge, Gold Prize (Top 1%)

## AI and Agent Practice

**Personal agent workbench** (Claude Code + Codex, Feb 2026 – present)

- Built a personal agent workbench synced across devices, with rules for multi-agent collaboration; I use it every day, for meeting notes, drafting shared cloud docs and revising them from comments, diagrams, course management, information collection, and everyday tasks outside work.
- Self-improving loop: designed sleep-review, which scans Claude Code and Codex session logs every day, flags user corrections, repeated tasks, and skill friction, and turns them into three tiers of improvement proposals (memory, skill additions, structural changes) that ship after human review.
- Search: treat search as the agent's context supply. Built routing by query type, added paid Chinese and English search APIs including DeepSeek and Exa, and packaged it as my own search skill.
- Multi-model collaboration: model-council has 5 models answer blind and review each other anonymously, then a chair synthesizes consensus and disagreement; cross-review has Claude and Codex take turns reviewing and testing the actual artifacts.
- Agent behavior log: an ongoing record of real cases where an agent got the task right but didn't do it well, each broken down into what happened, why, and the PM takeaway.

## Experience

### TikTok

**Product Manager Intern, LIVE Ecosystem Governance** · San Jose, CA  
*May 2026 – Nov 2026 · Post-enforcement creator perception and education*

- Built an end-to-end GenAI video pipeline (script → storyboard → AI-avatar clips → assembly) for creator policy education, cutting per-video production from about a month to days; designed per-stage production targets, guardrails, and 5 human-in-the-loop gates pairing automated QA with reviewable artifacts that operations edit to steer the next stage.
- Built AI into both ends of the PM workflow: interactive C-side and B-side prototypes built with Claude Code became the main artifact for aligning with regional operations, design, legal, and engineering; set up an agent-based product acceptance step that checks features against the PRD and also role-plays users and PMs to catch experience issues the PRD doesn't cover.
- Identified that education materials were hard-coded into the app, so even a copy-only change took weeks to ship; drove a 0-to-1 education asset management platform to centralize assets and release status, targeting release within a day in phase 2 and laying the foundation for segmented materials, multi-touchpoint delivery, and impact measurement.

### United AI

**Co-founder; Head of Products, Marketing and Strategic Planning** · Tianjin, China  
*2019 – Feb 2025 · Series A start-up in Industrial IoT, $20M valuation*

United AI is a SaaS platform for predictive maintenance (PDM) and Advanced Planning & Scheduling (APS).

- Owned end-to-end product lifecycle for the PDM platform, from product strategy to GTM, defining roadmap, PRD, and system architecture (cloud/edge/on-prem), averaging $1.5M in annual revenue.
- Led 0-to-1 PDM prototype development in Agile sprints, iterating with pilot customers to define and prioritize the MVP feature set, delivering the MVP in 3 months and signing 5 pilot customers for $80K in revenue by year-end.
- Defined an API-first architecture roadmap based on customer pain point analysis, trading a 3-month timeline delay and 25% cost increase for integration flexibility, expanding SAM by 3x and boosting win rate from 30% to 72%.
- Launched an on-prem product to bypass IT approval bottlenecks; architected air-gapped deployment, trading 25% higher ops cost for 67% faster adoption (under 1 month vs. 3 months), unlocking clients with high security requirements.
- Upgraded the on-prem offering from a rule-based to a self-learning engine using a bidirectional workflow API with client work-order systems, creating an automated data feedback loop that raised unknown-fault detection accuracy from 34% to 76%.
- Captured the untapped maritime market by architecting an on-board edge computing solution that addressed vibration noise and satellite bandwidth constraints, establishing our largest vertical (36% of revenue, $2.5M cumulative).
- Increased ARPU 20% by analyzing 10,000+ user sessions via SQL and identifying high-frequency touchpoints; partnered with engineering to ship a mobile app, increasing user engagement by ~3x.
- Drove product segmentation (Basic/Advanced/Enterprise tiers), deliberately sacrificing short-term ARPU to accelerate the data flywheel; expanded from 2 to 8 industry verticals, growing the customer base 180%.

### Speech Recognition Lab, Tsinghua University

**Software Engineer, Machine Learning Platform** · Beijing, China  
*2018*

- Enabled modern deep learning capabilities within a C++ speaker recognition library by compiling TensorFlow into a dynamic link library (.dll), then architecting a unified C++ API that abstracted the full training lifecycle.
- Cut speaker recognition latency from 15–20s to under the 8s contract requirement via layered optimization (input filtering, FP16 quantization, batch tuning), trading 4% accuracy for a 66% latency reduction and enabling production launch.

## Honors and Skills

- Honors: Contributing drafter, China shipbuilding industry group standard T/CSNAME 100—2025 on machinery condition monitoring (2025); Hurun China Under 30s To Watch (Entrepreneur list, 2021).
- Tools: Claude Code, Cowork, Codex, MCP, multi-agent orchestration, prototyping with vibe coding; SQL, Python; A/B testing.
- Certifications: Project Management Professional (PMP); Vibration Analysis: Category II.
- Interests: StarCraft II (top 100 on the national ladder; top 8 at a national collegiate tournament).
