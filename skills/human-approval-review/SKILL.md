---
name: human-approval-review
description: Use when reviewing customer-facing or externally visible marketing output before publishing, sending, scheduling, or handing off for activation.
version: 1.0.0
author: AI Marketing Army
license: MIT
metadata:
  hermes:
    tags: [marketing, review, safety, approval]
    related_skills: []
---

# Human Approval Review

## Overview

Use this skill to prepare marketing output for human review. The agent does not approve its own customer-facing work. It checks readiness, flags risks, and produces a concise review package so a human can make the final decision.

This is the practical version of the Human Approval Gate in the AI Marketing Army architecture.

## When to Use

Use when:
- Output may be published, sent, scheduled, uploaded, or shown externally.
- A draft includes product claims, performance claims, competitor references, pricing, compliance-sensitive language, or brand-sensitive messaging.
- A mock campaign run needs to demonstrate responsible human-in-the-loop governance.

Do not use when:
- The output is strictly internal and not used for decision-making.
- The task is to bypass human approval.
- The agent lacks the source material needed to check claims.

## Required Inputs

- Draft output
- Campaign brief
- Brand voice notes
- Audience / ICP brief
- Source material or proof points
- Channel requirements
- Known claims to avoid
- Privacy and safety rules

## Process

1. **Classify the output**
   - Internal-only
   - Customer-facing draft
   - Ready for human review
   - Not ready for review

2. **Check strategic fit**
   - Matches campaign objective
   - Addresses the intended audience
   - Uses the approved messaging angle
   - Has a clear CTA or purpose

3. **Check brand and tone**
   - Voice matches brand notes
   - Language is clear and human
   - No generic AI filler
   - No inappropriate hype

4. **Check claims and evidence**
   - Identify every factual, performance, comparative, or product claim.
   - Confirm whether a source is available.
   - Flag unsupported claims for removal or human confirmation.

5. **Check privacy and safety**
   - No private data
   - No credentials, tokens, or raw operational exports
   - No sensitive customer details
   - No accidental disclosure of private strategy

6. **Prepare decision recommendation**
   - Approve
   - Approve with edits
   - Needs revision
   - Block until evidence or human decision

The recommendation is advisory. The human makes the final approval decision.

## Output Format

```markdown
# Human Approval Review: [Asset / Campaign]

## Review Status
Recommendation: Approve / Approve with edits / Needs revision / Block

## Asset Summary
- Asset:
- Channel:
- Audience:
- Customer-facing: Yes/No

## Strategic Fit
- Objective fit:
- Audience fit:
- CTA clarity:

## Brand / Tone Check
- Fits brand voice: Yes/No/Partial
- Notes:

## Claims Check
| Claim | Source available? | Risk | Action |
|---|---|---|---|
| [Claim] | Yes/No | Low/Medium/High | Keep/Edit/Remove/Confirm |

## Privacy / Safety Check
- Private data present: Yes/No
- Credentials or tokens present: Yes/No
- Sensitive operational data present: Yes/No
- Notes:

## Required Edits Before Approval
1. [Edit]

## Human Decision Needed
- [Decision or judgement call]

## Final Handoff
- Suggested Kanban status:
- Next owner:
```

## Quality Bar

A good approval review:
- Makes the human's decision easier.
- Flags unsupported claims clearly.
- Separates objective issues from judgement calls.
- Does not silently rewrite risky claims without noting the issue.
- Never treats AI-generated output as self-approved.

## Common Pitfalls

1. **Approving without evidence.** Unsupported claims should be flagged, edited, or removed.
2. **Only checking grammar.** Approval includes strategy, brand, claims, and privacy.
3. **Ignoring channel context.** What works in a blog may fail in a community announcement.
4. **Letting the agent be the final approver.** Human decision remains required.
5. **Missing private data.** Always check for sensitive info before external use.

## Verification Checklist

- [ ] Output is classified correctly.
- [ ] Strategic fit and brand fit are checked.
- [ ] Claims are listed and source status is clear.
- [ ] Privacy and safety checks are complete.
- [ ] Final recommendation is clear but not self-approving.
