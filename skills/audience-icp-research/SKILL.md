---
name: audience-icp-research
description: Use when creating a structured ICP and audience insight brief from campaign context, synthetic research inputs, approved notes, or connector outputs.
version: 1.0.0
author: AI Marketing Army
license: MIT
metadata:
  hermes:
    tags: [marketing, research, icp, audience]
    related_skills: []
---

# Audience / ICP Research

## Overview

Use this skill to turn product and campaign context into a practical audience profile. The output should help other agents make better messaging, channel, SEO, and measurement decisions.

For public portfolio demos, use synthetic or sanitised information. If live research is unavailable, clearly label assumptions and confidence levels.

## When to Use

Use when:
- A campaign needs a defined primary ICP before content or messaging work.
- The Research Agent needs to summarise audience needs, pains, triggers, objections, and channels.
- A mock campaign requires realistic audience logic without using private customer data.

Do not use when:
- The task is only to polish already-approved persona copy.
- The required audience data is private and has not been approved for the task.
- The agent is expected to make statistical claims without source material.

## Required Inputs

- Campaign brief
- Product/company profile
- Category or market context
- Existing audience notes, if available
- Approved research snippets, if available
- Any known exclusions or sensitive claims

## Process

1. **Identify the buying context**
   - Who feels the pain?
   - What job are they trying to get done?
   - What triggers urgency?
   - What alternatives do they currently use?

2. **Define the primary ICP**
   - Role or profile
   - Company type or life stage
   - Maturity level
   - Budget or resource assumptions
   - Current workflow

3. **Map pains and motivations**
   - Functional pains
   - Emotional pains
   - Career or status motivations
   - Team/business pressures

4. **Map objections and friction**
   - Trust concerns
   - Cost or time concerns
   - Switching costs
   - Technical barriers
   - Compliance or reputational risks

5. **Map messaging implications**
   - What the audience wants to hear
   - What to avoid saying
   - Which proof points matter
   - Which channels likely fit

6. **State confidence**
   - High: supported by provided sources.
   - Medium: reasonable inference from context.
   - Low: placeholder assumption for mock run.

## Output Format

```markdown
# Audience / ICP Brief: [Campaign Name]

## Primary ICP
- Name / shorthand:
- Description:
- Role or profile:
- Context:
- Maturity level:

## Jobs To Be Done
- Functional job:
- Emotional job:
- Business outcome:

## Pain Points
- [Pain] — confidence: High/Medium/Low

## Buying Triggers
- [Trigger]

## Objections
- [Objection]
- Suggested response:
- Proof needed:

## Messaging Implications
- Lead with:
- Avoid:
- Useful proof points:
- Tone notes:

## Channel Assumptions
- Best-fit channels:
- Lower-fit channels:
- Rationale:

## Assumptions and Caveats
- [Clearly labelled assumption]

## Recommended Next Tasks
- [Task for Content / SEO / Performance / Social]
```

## Quality Bar

A good ICP brief:
- Is specific enough to guide messaging.
- Avoids generic persona fluff.
- Separates evidence from assumptions.
- Connects audience insight to practical campaign decisions.
- Does not expose private customer data.

## Common Pitfalls

1. **Creating a generic persona.** Avoid vague labels like "busy professionals" without decision context.
2. **Pretending assumptions are research.** Label synthetic or inferred points.
3. **Ignoring objections.** Good campaign strategy anticipates why people might not believe or act.
4. **Over-segmenting too early.** For a first mock run, one primary ICP is enough.
5. **Making unsupported demographic claims.** Only include demographics when relevant and sourced.

## Verification Checklist

- [ ] Primary ICP is clear and usable.
- [ ] Jobs, pains, triggers, and objections are included.
- [ ] Messaging implications are explicit.
- [ ] Confidence levels or assumptions are labelled.
- [ ] No private data or unsupported statistical claims are included.
