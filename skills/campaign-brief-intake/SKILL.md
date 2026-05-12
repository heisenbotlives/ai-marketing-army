---
name: campaign-brief-intake
description: Use when turning a rough marketing request into a structured campaign brief, assumptions list, open questions, and initial Kanban-ready task breakdown.
version: 1.0.0
author: AI Marketing Army
license: MIT
metadata:
  hermes:
    tags: [marketing, campaign-planning, orchestration, brief]
    related_skills: []
---

# Campaign Brief Intake

## Overview

Use this skill to convert an informal campaign request into a clear, reusable campaign brief. The goal is not to invent a perfect strategy immediately; it is to create enough structure for specialist agents to work from the same assumptions.

This skill is designed for mock campaign runs and public portfolio examples. Use synthetic or sanitised information only unless a private connector is explicitly configured and approved.

## When to Use

Use when:
- A human gives a vague campaign idea or marketing request.
- The Orchestrator needs to create Kanban cards from a brief.
- A mock campaign needs a single source of truth before research, messaging, content, SEO, or measurement work begins.

Do not use when:
- The request is already a complete strategy document.
- The task is only copy editing an existing asset.
- The output would require private customer, analytics, or account data that has not been approved for use.

## Required Inputs

Collect or infer the following. If something is missing, state it as an assumption rather than pretending it is known.

- Product or company name
- Product category
- Campaign objective
- Target audience
- Offer or core promise
- Timeframe
- Priority channels
- Geographic or market assumptions
- Brand voice constraints
- Compliance or claim constraints
- Known source material
- Success criteria

## Process

1. **Restate the request**
   - Summarise the human's request in plain language.
   - Preserve the business goal and constraints.
   - Do not add unsupported claims.

2. **Separate facts from assumptions**
   - Facts: explicitly provided by the brief or approved source material.
   - Assumptions: reasonable placeholders for a mock run.
   - Open questions: important gaps that would need a human or connector later.

3. **Define the campaign frame**
   - Objective
   - Audience
   - Funnel stage
   - Primary message
   - Channels
   - Timeline
   - Expected output pack

4. **Create initial Kanban-ready work items**
   - Break the campaign into specialist tasks.
   - Assign suggested owner agent.
   - Add dependencies and acceptance criteria.
   - Flag any customer-facing output for human approval.

5. **Prepare handoff package**
   - Create a brief that Research, Performance Analyst, Content, Social & Community, and SEO agents can all reuse.

## Output Format

```markdown
# Campaign Brief: [Campaign Name]

## Request Summary
[Plain-language summary]

## Objective
[Primary objective]

## Audience
- Primary ICP:
- Secondary audience:
- Key pain points:

## Product / Offer
- Product:
- Category:
- Core promise:
- Proof points available:
- Proof points needed:

## Campaign Frame
- Funnel stage:
- Campaign angle:
- Priority channels:
- Timeframe:
- Desired outputs:

## Facts
- [Provided fact]

## Assumptions for Mock Run
- [Clearly labelled assumption]

## Open Questions
- [Question]

## Initial Kanban Cards
### Card 1: [Title]
- Owner agent:
- Objective:
- Inputs:
- Output:
- Dependencies:
- Acceptance criteria:
- Approval required: Yes/No

## Risks / Watchouts
- [Unsupported claims, missing sources, tone risks, sensitive data risks]
```

## Quality Bar

A good brief is:
- Specific enough for agents to work independently.
- Honest about unknowns.
- Clearly synthetic where it uses mock data.
- Free of private data, credentials, customer lists, or raw operational exports.
- Clear about which outputs need human approval.

## Common Pitfalls

1. **Inventing evidence.** Do not create fake metrics, testimonials, awards, or customer logos.
2. **Skipping assumptions.** If a detail is not provided, label it as an assumption.
3. **Over-scoping the run.** Keep the first mock campaign small enough to review.
4. **Forgetting approval.** Any external-facing copy must be marked for human review.
5. **Mixing private and public data.** Public demo briefs must use synthetic or sanitised information.

## Verification Checklist

- [ ] Objective, audience, offer, channels, and timeframe are defined.
- [ ] Facts, assumptions, and open questions are separated.
- [ ] Initial Kanban cards are actionable.
- [ ] Customer-facing outputs are marked for approval.
- [ ] No private data, API keys, credentials, or raw operational data are included.
