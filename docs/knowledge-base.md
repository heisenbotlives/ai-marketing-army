# Knowledge Base

The knowledge base is split into three layers because not all context has the same privacy, update frequency, or ownership model.

## Layer 1: Brand and reference

**Storage:** Obsidian, synced via GitHub when appropriate.

**Purpose:** Durable context that agents need repeatedly.

**Examples:**

- Brand voice guide
- Positioning and messaging
- ICPs and personas
- Product specs
- Glossary
- Approved claims and proof points
- Content guidelines
- Competitor profiles

**Lifecycle:** Updated deliberately. Should be reviewed before being treated as authoritative.

**Why Obsidian:** It is easy for a human marketer to maintain, link, and browse. It also works well as markdown context for agents.

## Layer 2: Operational data

**Storage:** Google Drive or equivalent private workspace.

**Purpose:** Data that changes frequently or may contain sensitive information.

**Examples:**

- Analytics exports
- Campaign performance reports
- Ad platform exports
- Customer research summaries
- Sales notes
- Community exports
- Experiment results

**Lifecycle:** Updated frequently. Agents should cite the file/date they used and avoid treating old exports as current.

**Why separate:** Operational data may contain sensitive or private information and should not be committed to a public repo.

## Layer 3: Skills

**Storage:** GitHub markdown files or Hermes skill files.

**Current repo examples:** The [`skills/`](../skills/) directory contains starter Hermes-style marketing skills for mock campaign runs, including brief intake, audience/ICP research, messaging angle generation, asset drafting, measurement planning, and human approval review.

**Purpose:** Reusable procedures that tell agents how to do recurring work.

**Examples:**

- How to write a competitor brief
- How to convert a blog post into social posts
- How to create an SEO brief
- How to review a draft for brand voice
- How to run a performance readout

**Lifecycle:** Versioned and improved over time. Skills should be patched when a better workflow is discovered.

## Why three layers

This split keeps prompts narrower, reduces accidental data exposure, and makes it clearer which sources should be treated as stable context versus changing evidence.

## Citation standard

Agent outputs should state:

- Which knowledge layer was used
- Which specific note/file/export was used
- Date or version where relevant
- Confidence level
- Any missing context
