---
name: campaign-asset-drafting
description: Use when drafting campaign assets from an approved brief, audience profile, messaging angle, brand voice, and channel requirements.
version: 1.0.0
author: AI Marketing Army
license: MIT
metadata:
  hermes:
    tags: [marketing, copywriting, content, campaign-assets]
    related_skills: []
---

# Campaign Asset Drafting

## Overview

Use this skill to create reviewable campaign assets from approved strategy inputs. The output should be useful but not treated as publish-ready until it passes human approval.

This skill prioritises clarity, brand fit, channel suitability, and claim discipline over volume.

## When to Use

Use when:
- A campaign brief and messaging angle are ready.
- The Content Agent needs to draft posts, emails, landing page sections, ad copy, or campaign copy.
- A mock run needs tangible marketing outputs for review.

Do not use when:
- Strategy inputs are missing.
- The requested asset would require unsupported legal, financial, medical, or performance claims.
- The task is to publish or schedule content directly.

## Required Inputs

- Campaign brief
- ICP / audience brief
- Selected messaging angle
- Brand voice notes
- Channel or format requirements
- Proof points available
- Claims to avoid
- CTA

## Process

1. **Confirm the asset list**
   - Identify which assets are required.
   - Confirm format and channel constraints.
   - Keep first-run output small enough to review.

2. **Translate strategy into copy**
   - Lead with the audience pain or desired outcome.
   - Use the selected messaging angle consistently.
   - Match brand voice.
   - Keep claims evidence-based.

3. **Create variants where useful**
   - Vary hook, framing, or CTA.
   - Do not create repetitive filler.

4. **Annotate review needs**
   - Mark claims that need source verification.
   - Mark areas where tone or compliance may need human judgement.
   - Note which assets are customer-facing.

5. **Prepare approval handoff**
   - Include a short rationale and checklist for the human reviewer.

## Output Format

```markdown
# Campaign Asset Drafts: [Campaign Name]

## Inputs Used
- Brief:
- Audience:
- Messaging angle:
- Brand voice:
- CTA:

## Asset 1: [Channel / Format]
- Purpose:
- Audience:
- Status: Draft for human review

### Draft
[Copy]

### Rationale
[Why this draft fits the strategy]

### Claims / Proof Check
- Claim:
- Source available: Yes/No
- Review needed:

### Revision Notes
- [Suggested improvement or option]

## Approval Notes
- Customer-facing: Yes
- Human approval required before use: Yes
- Risks or watchouts:
```

## Quality Bar

Good campaign assets:
- Map clearly to the brief, ICP, and messaging angle.
- Use plain, specific language.
- Avoid generic AI-sounding phrases.
- Do not invent proof.
- Include a clear CTA where appropriate.
- Are labelled as drafts until approved.

## Common Pitfalls

1. **Writing from thin air.** Always anchor copy in the brief and audience profile.
2. **Overusing hype.** Avoid empty superlatives and vague transformation claims.
3. **Forgetting the channel.** A LinkedIn post, email, ad, and community message need different structures.
4. **Inventing metrics.** Never create fake percentages, customer counts, revenue figures, or performance results.
5. **Skipping review notes.** Human approval needs context, not just copy.

## Verification Checklist

- [ ] Every asset is tied to an input brief and angle.
- [ ] Customer-facing drafts are marked for approval.
- [ ] Unsupported claims are flagged or removed.
- [ ] CTA is clear where needed.
- [ ] Tone matches brand notes.
- [ ] No private data or fake proof is included.
