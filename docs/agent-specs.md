# Agent Specs

This document defines the operating spec for each agent in the AI Marketing Army proof of concept.

The goal is to make each agent concrete enough to implement, test, and explain without claiming the system is already a fully autonomous marketing department. Each agent has a narrow role, explicit boundaries, and a clear relationship to the shared Kanban board, knowledge base, connectors, and human approval gate.

## Shared operating model

All agents follow the same basic model:

1. Read the assigned Kanban card.
2. Pull relevant context from the shared knowledge base.
3. Use approved connectors where needed.
4. Produce a reviewable output.
5. Update the Kanban card with sources, assumptions, caveats, and next steps.
6. Route customer-facing output through the Human Approval Gate before anything is published, sent, posted, or pushed live.

## Shared input format

Every agent task should include:

- **Task ID:** Kanban card or issue reference
- **Objective:** What the task is trying to achieve
- **Context:** Brief, campaign, product, audience, or previous work
- **Source material:** Links, docs, exports, notes, or connector outputs
- **Required output:** Draft, brief, analysis, recommendations, etc.
- **Deadline / priority:** If applicable
- **Approval requirement:** Whether the output is internal-only or customer-facing

## Shared output format

Every agent handoff should include:

- **Task ID**
- **Output summary**
- **Work produced**
- **Sources used**
- **Assumptions / caveats**
- **Confidence level:** High / medium / low
- **Recommended next step**
- **Suggested reviewer or next agent**
- **Kanban status update**

## Shared connector principles

- Read-only access is preferred by default.
- Write access should be granted only when necessary.
- Customer-facing writes require human approval.
- Private data should stay in private systems and must not be copied into the public repo.
- Connector credentials, tokens, raw private exports, and API responses are never committed.

---

## 1. Orchestrator Agent

### Mission

Turn marketing requests into clear, trackable work and keep the six-agent system moving.

The Orchestrator is one of the six agents. It is not a separate control layer. Its special responsibility is creating and maintaining the shared work state.

### Typical tasks

- Turn a marketing brief into Kanban cards.
- Break broad requests into specialist subtasks.
- Decide which agent should handle each task.
- Set dependencies between cards.
- Identify blockers and missing context.
- Compile shift reports or project summaries.
- Decide when work is ready for human review.

### Skills needed

- Brief interpretation
- Task decomposition
- Prioritisation
- Project management
- Dependency mapping
- Handoff writing
- Quality control
- Status reporting
- Escalation judgement

### Connectors needed

- **Kanban board:** create cards, update statuses, comment on blockers
- **GitHub repo:** read project docs, prompts, skills, and public templates
- **Hermes skills:** load reusable procedures and workflows
- **Obsidian / GitHub knowledge base:** read brand and reference docs
- **Google Drive:** read briefs or operational source docs where needed
- **Slack / Discord / Telegram:** optional status notifications, not customer-facing posting

### Inputs

- Marketing brief
- Campaign objective
- Target audience
- Available source docs
- Existing Kanban state
- Agent capacity or priority rules

### Outputs

- Kanban cards
- Task assignments
- Dependency notes
- Handoff summaries
- Shift reports
- Review checklists
- Blocker escalations

### Approval boundaries

The Orchestrator can create and update internal tasks. It should not publish, send, schedule, or alter customer-facing output without human approval.

### Success criteria

- Work is visible and trackable.
- Every card has a clear owner, objective, and next step.
- Downstream agents receive enough context to act.
- Blockers are escalated early.
- No customer-facing action bypasses human approval.

---

## 2. Research Agent

### Mission

Find market, competitor, audience, and narrative signals, then turn them into source-backed insight notes for the rest of the team.

### Typical tasks

- Summarise a competitor launch.
- Track industry narratives and market shifts.
- Monitor public social/community sentiment.
- Extract audience pain points and objections.
- Create source-backed research briefs.
- Flag uncertainty, weak evidence, or contradictory sources.

### Skills needed

- Web research
- Source evaluation
- Competitor analysis
- Trend spotting
- Audience insight extraction
- Citation discipline
- Summarisation
- Marketing implication analysis
- Uncertainty handling

### Connectors needed

- **Web search:** find current public information
- **Browser:** inspect web pages and source material
- **X / Twitter:** read public narratives and sentiment
- **Discord:** read community exports or monitored channels where permitted
- **Telegram:** read community exports or monitored channels where permitted
- **Google Drive:** access stored research files or approved exports
- **Obsidian / GitHub knowledge base:** compare findings against existing positioning, ICPs, glossary, and notes
- **GitHub repo:** read public docs and write safe demo research notes where appropriate

### Inputs

- Research question
- Audience or market segment
- Competitor list
- Source constraints
- Brand/reference context
- Required confidence level

### Outputs

- Research briefs
- Competitor notes
- Trend summaries
- Audience pain-point notes
- Source lists
- Confidence ratings
- Implications for Content, Social, SEO, or Performance

### Approval boundaries

The Research Agent can collect and summarise public or approved source material. It should not invent facts, store unnecessary personal data, or produce final customer-facing claims without review.

### Success criteria

- Findings are concise and source-backed.
- Claims include links or citations.
- Uncertainty is clearly labelled.
- Outputs explain why the finding matters for marketing.
- Sensitive or private data is handled conservatively.

---

## 3. Performance Analyst Agent

### Mission

Read marketing performance data, explain what is happening, and recommend experiments or optimisations.

### Typical tasks

- Analyse campaign performance.
- Identify top-performing content themes.
- Compare channel performance over time.
- Spot weak pages, posts, funnels, or campaigns.
- Recommend A/B tests or content experiments.
- Create measurement plans.
- Feed learnings back into the knowledge base.

### Skills needed

- Analytics literacy
- Data interpretation
- Funnel thinking
- KPI selection
- Experiment design
- Pattern recognition
- Spreadsheet analysis
- Caveat handling
- Business impact prioritisation

### Connectors needed

- **GA4:** traffic, conversions, user behaviour, landing page performance
- **Google Search Console:** search queries, impressions, clicks, SEO trends
- **Ad platforms:** spend, CTR, CPA, ROAS, audience and creative performance
- **Social scheduler:** post-level engagement and timing data
- **Email / CRM:** open rates, click rates, conversion data, lifecycle summaries
- **CMS:** content inventory and page metadata where needed
- **Google Drive:** analytics exports, campaign reports, dashboards
- **Obsidian / GitHub knowledge base:** prior learnings, experiment logs, positioning context

### Inputs

- Campaign or channel question
- Date range
- KPI definition
- Data export or connector access
- Relevant campaign notes
- Previous learning logs

### Outputs

- Performance summaries
- Experiment recommendations
- Measurement plans
- Channel analysis
- Learning-log updates
- Prioritised optimisation backlog cards

### Approval boundaries

The Performance Analyst can recommend changes and create internal analysis. It should not change budgets, targeting, live campaigns, tracking, or external dashboards without human approval.

### Success criteria

- Recommendations are grounded in data.
- Causality is not overstated.
- Caveats are explicit.
- Suggested experiments have clear hypotheses and success metrics.
- Outputs help decide what to do next.

---

## 4. Content Agent

### Mission

Produce long-form, strategic, and campaign content drafts from approved briefs and source material.

### Typical tasks

- Draft blog posts.
- Create thought-leadership outlines.
- Write landing-page sections.
- Turn research into a narrative draft.
- Rewrite copy to match brand voice.
- Convert rough notes into polished content.
- Flag claims that need source checking.

### Skills needed

- Copywriting
- Long-form writing
- Narrative structure
- Brand voice adaptation
- Editing
- Source-aware writing
- Claim checking
- Content repurposing
- Audience-aware messaging

### Connectors needed

- **Obsidian / GitHub knowledge base:** brand voice, positioning, ICPs, glossary, product specs
- **Google Drive:** briefs, outlines, drafts, research docs
- **GitHub repo:** prompts, templates, public examples
- **CMS:** create draft pages or posts, only if write access is approved
- **Web search / Browser:** source checking and current context
- **SEO agent outputs:** briefs, keyword clusters, search intent notes
- **Research agent outputs:** source-backed context and market insight

### Inputs

- Content brief
- Audience and funnel stage
- Brand voice guidance
- Research notes
- SEO brief, if relevant
- Required format and length
- Claims that need support

### Outputs

- Blog drafts
- Thought-leadership drafts
- Landing-page copy
- Article outlines
- Messaging options
- Claim-check notes
- Content handoff summaries

### Approval boundaries

The Content Agent can draft and revise. It should not publish, schedule, or update live website content without human approval. Unsupported claims should be flagged rather than smoothed over.

### Success criteria

- Drafts are clear, specific, and human-sounding.
- Content matches brand voice and audience context.
- Claims are supported or flagged.
- Output is ready for human review, not direct publication.
- The next reviewer can easily see sources and assumptions.

---

## 5. Social & Community Agent

### Mission

Turn strategy and approved content into channel-native social/community drafts, while monitoring audience signals.

### Typical tasks

- Draft X posts or threads.
- Repurpose blog posts into social content.
- Draft Discord or Telegram discussion prompts.
- Summarise community sentiment.
- Suggest replies to common questions.
- Monitor audience reactions.
- Create channel-specific content variants.

### Skills needed

- Social copywriting
- Channel adaptation
- Community tone judgement
- Sentiment summarisation
- Response drafting
- Short-form editing
- Narrative/meme awareness where relevant
- Escalation judgement
- Moderation awareness

### Connectors needed

- **X / Twitter:** read public conversations and draft posts
- **Discord:** read community channels or exports where permitted
- **Telegram:** read community channels or exports where permitted
- **Social scheduler:** create drafts and inspect scheduled content
- **Slack:** internal coordination or community support handoffs where relevant
- **Obsidian / GitHub knowledge base:** brand voice, approved messages, community guidelines
- **Google Drive:** campaign plans and approved content assets
- **CMS / content library:** source long-form pieces for repurposing

### Inputs

- Campaign brief
- Approved content or source asset
- Target channel
- Audience segment
- Brand/community guidelines
- Current sentiment or conversation context
- Approval requirement

### Outputs

- Draft posts
- Draft threads
- Community response suggestions
- Sentiment summaries
- Social content calendars
- Channel-specific variants
- Escalation notes

### Approval boundaries

The Social & Community Agent should not auto-post, impersonate humans deceptively, or engage in sensitive conversations without review. Customer-facing posts and replies require human approval.

### Success criteria

- Drafts feel native to the channel.
- Posts are useful rather than generic.
- Community risk is flagged early.
- Sensitive topics are escalated.
- Outputs are ready for approval, not automatic posting.

---

## 6. SEO Agent

### Mission

Improve discoverability through search strategy, on-page recommendations, and content opportunity analysis.

### Typical tasks

- Create keyword and search-intent briefs.
- Identify content gaps.
- Review competitor pages.
- Suggest internal links.
- Draft title tags and meta descriptions.
- Prioritise SEO opportunities.
- Recommend updates to existing content.

### Skills needed

- Keyword research
- Search intent analysis
- SERP analysis
- Content gap analysis
- On-page SEO
- Internal linking strategy
- Metadata writing
- Content inventory review
- Effort/impact prioritisation

### Connectors needed

- **Google Search Console:** queries, impressions, clicks, page performance
- **GA4:** landing page behaviour and conversion context
- **CMS:** content inventory, metadata, live page structure
- **Web search / Browser:** SERP and competitor analysis
- **Google Drive:** content inventories, keyword exports, planning docs
- **Obsidian / GitHub knowledge base:** product context, positioning, glossary, ICPs
- **Research agent outputs:** market language and competitor notes

### Inputs

- Topic or product area
- Target audience
- Content inventory
- Search data or export
- Competitor pages
- Business priority
- Constraints from brand or product positioning

### Outputs

- SEO briefs
- Keyword clusters
- Search-intent maps
- Internal-link recommendations
- Metadata suggestions
- Content refresh recommendations
- Prioritised SEO backlog cards

### Approval boundaries

The SEO Agent can recommend and draft changes. It should not publish CMS edits, change metadata live, or chase irrelevant keywords without human approval.

### Success criteria

- Recommendations align with business strategy.
- Search intent is clear.
- Data limitations are stated.
- Priorities are practical and effort-aware.
- No search volume or competitor facts are invented.

---

## Connector-to-agent matrix

| Connector | Orchestrator | Research | Performance Analyst | Content | Social & Community | SEO |
|---|---:|---:|---:|---:|---:|---:|
| Kanban board | Write | Read | Read | Read | Read | Read |
| Obsidian / GitHub KB | Read | Read/write notes | Read/write learnings | Read | Read | Read |
| GitHub repo / skills | Read | Read | Read | Read | Read | Read |
| Google Drive | Read | Read | Read | Read | Read | Read |
| GA4 | - | - | Read | - | - | Read |
| Google Search Console | - | - | Read | - | - | Read |
| Ad platforms | - | - | Read | - | - | - |
| X / Twitter | - | Read | Read analytics if available | - | Read / draft | - |
| Discord | - | Read | - | - | Read / draft | - |
| Telegram | - | Read | - | - | Read / draft | - |
| Social scheduler | - | - | Read | - | Draft | - |
| CMS | - | Read | Read | Draft | Read | Draft recommendations |
| Email / CRM | - | - | Read | Draft | Draft | - |
| Slack | Notify | - | - | - | Notify/escalate | - |
| Web search | - | Read | - | Read | Read | Read |
| Browser | - | Read | - | Read | Read | Read |

**Note:** “Draft” means preparing an artefact for review, not publishing it. Customer-facing write actions still require human approval.

## Implementation priority

For a practical proof of concept, implement in this order:

1. **Kanban + Knowledge Base:** Orchestrator creates cards; agents read/write safe markdown notes.
2. **Research + Content loop:** Research creates a brief; Content turns it into a draft.
3. **SEO support:** SEO adds search-intent and metadata recommendations.
4. **Performance loop:** Performance Analyst reads synthetic exports and suggests experiments.
5. **Social repurposing:** Social & Community turns approved drafts into channel-specific posts.
6. **Human Approval Gate:** Add an explicit approval state before any simulated publishing step.
7. **Real connectors later:** Swap synthetic demo data for real connector outputs only when privacy and credentials are handled safely.
