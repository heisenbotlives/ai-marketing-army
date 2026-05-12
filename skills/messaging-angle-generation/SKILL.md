---
name: messaging-angle-generation
description: Use when developing campaign messaging angles from a brief, ICP, positioning notes, brand voice, and approval constraints.
version: 1.0.0
author: AI Marketing Army
license: MIT
metadata:
  hermes:
    tags: [marketing, messaging, positioning, campaign]
    related_skills: []
---

# Messaging Angle Generation

## Overview

Use this skill to turn strategy inputs into a set of campaign messaging angles. A messaging angle is not finished copy; it is a strategic route that can be tested across content, social, email, SEO, or ads.

Angles should be distinct, grounded in the audience brief, and honest about the proof needed to support them.

## When to Use

Use when:
- A campaign needs several possible creative or strategic routes.
- The Content Agent needs direction before drafting assets.
- The Orchestrator wants options to review before committing to a campaign package.

Do not use when:
- The brief has no defined audience or product context.
- The task is final copy approval.
- A claim requires evidence that is not available.

## Required Inputs

- Campaign brief
- Audience / ICP brief
- Product profile
- Brand voice notes
- Known proof points
- Approval constraints
- Channel assumptions

## Process

1. **Extract the strategic ingredients**
   - Audience pain
   - Desired outcome
   - Product promise
   - Differentiator
   - Available proof
   - Tone constraints

2. **Generate multiple angle types**
   Consider angles such as:
   - Pain-led
   - Outcome-led
   - Contrarian
   - Educational
   - Use-case-led
   - Risk-reduction
   - Workflow/productivity
   - Social proof-led, only if proof exists

3. **Pressure-test each angle**
   - Is it relevant to the ICP?
   - Is it specific?
   - Does it require unsupported evidence?
   - Could it sound overhyped?
   - Which channel suits it best?

4. **Rank the angles**
   Recommend the strongest 2-3 based on relevance, proof availability, distinctiveness, and risk.

## Output Format

```markdown
# Messaging Angles: [Campaign Name]

## Strategy Inputs Used
- Audience:
- Product promise:
- Key pain:
- Available proof:
- Brand voice:

## Angle Options

### Angle 1: [Name]
- Core idea:
- Target audience:
- Pain or trigger:
- Main promise:
- Example headline:
- Best-fit channels:
- Proof needed:
- Risk / watchout:
- Confidence: High/Medium/Low

## Recommended Angles
1. [Angle] — reason
2. [Angle] — reason
3. [Angle] — reason

## Angles Rejected
- [Rejected angle] — why not

## Handoff Notes
- For Content Agent:
- For Social & Community Agent:
- For SEO Agent:
- For Performance Analyst:
```

## Quality Bar

Good messaging angles are:
- Distinct from one another.
- Rooted in the ICP's actual pains and triggers.
- Specific enough to inspire copy.
- Honest about proof and claim risk.
- Suitable for the campaign stage and channel.

## Common Pitfalls

1. **Writing final copy too early.** Keep angles strategic; copy comes later.
2. **Making every angle the same.** Each option should have a different strategic route.
3. **Using fake social proof.** Do not invent customers, metrics, testimonials, or awards.
4. **Ignoring brand voice.** An angle can be strategically good but tonally wrong.
5. **Overpromising.** Flag claims that need evidence before publication.

## Verification Checklist

- [ ] At least 5 distinct angles are provided.
- [ ] Each angle includes audience, promise, proof needed, and risk.
- [ ] Top recommendations are ranked with reasons.
- [ ] Unsupported claims are flagged.
- [ ] Handoff notes are useful for downstream agents.
