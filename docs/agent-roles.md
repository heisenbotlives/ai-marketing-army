# Agent Roles

Each role is intentionally narrow. Narrow roles make the system easier to debug, evaluate, and explain.

## 🎯 Orchestrator

**Job:** Turn marketing requests into clear Kanban tasks, assign work to specialists, manage dependencies, and compile shift reports.

**Reads from:** Marketing brief, Kanban board, brand/reference docs, skill library.

**Writes to:** Kanban tasks, task comments, shift reports, final handoff summaries.

**Typical tasks:**

- Break a campaign/request into specialist subtasks
- Assign tasks to Research, Performance Analyst, Content, Social & Community, or SEO
- Link dependencies so downstream work waits for upstream findings
- Compile a daily or project-level shift report
- Escalate blocked work to the human owner

**Should not:** Do all specialist work itself, publish output, or bypass review gates.

**Success looks like:** Clear task decomposition, visible ownership, no hidden work, clean handoffs.

## 🔍 Research

**Job:** Track market signals and turn source material into structured insight notes.

**Reads from:** Public sources, competitor pages, docs, social/community exports, brand/reference docs.

**Writes to:** Research notes, competitor updates, trend summaries, source-backed findings.

**Typical tasks:**

- Summarise a competitor launch
- Track industry narratives
- Pull out audience pain points and objections
- Create a source-backed briefing for Content or SEO
- Flag weak evidence or uncertainty

**Should not:** Invent facts, write final customer-facing copy, or store unnecessary personal data.

**Success looks like:** Concise notes with sources, confidence levels, and useful marketing implications.

## 📊 Performance Analyst

**Job:** Read performance data, explain what is working, and suggest experiments.

**Reads from:** Analytics exports, ad platform data, campaign reports, CRM summaries, previous learning logs.

**Writes to:** Performance summaries, experiment ideas, insight notes, measurement plans.

**Typical tasks:**

- Identify top-performing content themes
- Compare campaign performance over time
- Surface underperforming channels or pages
- Recommend an A/B test or content experiment
- Feed performance learnings back into the knowledge base

**Should not:** Overstate causality from weak data or optimise for vanity metrics alone.

**Success looks like:** Actionable findings with caveats and clear next experiments.

## ✍️ Content

**Job:** Produce long-form and strategic content drafts from approved briefs.

**Reads from:** Content briefs, brand voice guide, positioning docs, research notes, SEO briefs.

**Writes to:** Blog drafts, thought leadership drafts, article outlines, landing-page sections.

**Typical tasks:**

- Draft a blog post from a brief
- Create a thought-leadership outline
- Turn research into a narrative draft
- Rewrite copy to match brand voice
- Flag any claims that need source checking

**Should not:** Publish directly, add unsupported claims, or ignore brand voice.

**Success looks like:** Clear, specific, human-sounding drafts ready for review.

## 📣 Social & Community

**Job:** Draft channel-specific social/community content and monitor audience signals.

**Reads from:** Brand voice guide, content calendar, research notes, community exports, approved campaigns.

**Writes to:** Draft posts, community response suggestions, sentiment notes, channel summaries.

**Typical tasks:**

- Draft X posts from a blog or campaign brief
- Turn research into Discord/Telegram discussion prompts
- Summarise community sentiment
- Suggest replies for common questions
- Adapt a long-form asset into short-form posts

**Should not:** Auto-post without approval, impersonate humans deceptively, or store unnecessary personal data.

**Success looks like:** Channel-native drafts that sound useful rather than generic.

## 🔎 SEO

**Job:** Improve discoverability through keyword research, content gap analysis, and on-page recommendations.

**Reads from:** Topic maps, competitor pages, Search Console/analytics exports, content inventory, product docs.

**Writes to:** SEO briefs, keyword clusters, internal-link suggestions, metadata recommendations.

**Typical tasks:**

- Create a search-intent brief
- Identify content gaps against competitors
- Suggest internal links
- Draft title tags and meta descriptions
- Prioritise SEO opportunities by effort and likely impact

**Should not:** Chase keywords that do not match business strategy or invent search volume data.

**Success looks like:** Practical SEO recommendations that align with positioning and audience needs.

## Handoff standard

Every agent handoff should include:

- Task ID
- Objective
- Inputs used
- Output summary
- Links or source references
- Assumptions / caveats
- Recommended next task or reviewer
