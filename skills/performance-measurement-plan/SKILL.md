---
name: performance-measurement-plan
description: Use when defining KPIs, experiment hypotheses, tracking assumptions, and reporting structure for a campaign or mock campaign run.
version: 1.0.0
author: AI Marketing Army
license: MIT
metadata:
  hermes:
    tags: [marketing, analytics, measurement, experimentation]
    related_skills: []
---

# Performance Measurement Plan

## Overview

Use this skill to define how a campaign would be measured. The purpose is to connect marketing output to learning and business outcomes, even in a mock run where live analytics connectors are not configured.

For demos, use placeholder metrics and synthetic assumptions. Do not invent real performance data.

## When to Use

Use when:
- A campaign strategy needs success metrics.
- The Performance Analyst needs to define KPIs before launch.
- A mock campaign run needs a measurement section without live connectors.

Do not use when:
- The task is to report actual performance without access to approved data.
- The campaign objective is undefined.
- Metrics would imply real results from a synthetic demo.

## Required Inputs

- Campaign objective
- Funnel stage
- Target audience
- Channels
- Desired outputs
- CTA or conversion action
- Available analytics assumptions or approved historical context

## Process

1. **Identify the campaign objective**
   - Awareness
   - Engagement
   - Lead generation
   - Activation
   - Retention
   - Research/learning

2. **Choose primary and secondary KPIs**
   - Primary KPI should map to the objective.
   - Secondary KPIs should help interpret performance.
   - Avoid vanity metrics unless they support the stated objective.

3. **Define experiment hypothesis**
   - If we target [audience] with [message] on [channel], then [expected behaviour] because [reason].

4. **Map funnel and tracking assumptions**
   - Touchpoints
   - Events
   - UTM assumptions
   - Conversion definitions
   - Reporting cadence

5. **State limitations**
   - Missing connectors
   - Small sample size
   - Attribution uncertainty
   - Synthetic demo data

6. **Recommend next analysis tasks**
   - What to check after launch
   - What to compare
   - What would trigger iteration

## Output Format

```markdown
# Performance Measurement Plan: [Campaign Name]

## Objective
[Campaign objective]

## Funnel Stage
[Awareness / consideration / conversion / retention]

## Hypothesis
If [audience] sees [message] through [channel], then [behaviour] because [reason].

## Primary KPI
- KPI:
- Why it matters:
- Target or benchmark: Synthetic / TBD / sourced

## Secondary KPIs
- KPI:
- Purpose:

## Tracking Plan
- Channels:
- Events:
- UTMs:
- Conversion action:
- Reporting cadence:

## Dashboard / Report Outline
- Section 1:
- Section 2:
- Section 3:

## Risks and Limitations
- [Attribution, sample size, missing connector, synthetic data]

## Post-Campaign Questions
- [Question to answer after results]
```

## Quality Bar

A good measurement plan:
- Matches metrics to the campaign objective.
- Distinguishes leading indicators from outcomes.
- Avoids fake performance data.
- Makes limitations clear.
- Creates useful learning loops for the next campaign.

## Common Pitfalls

1. **Choosing metrics because they are easy.** Pick metrics that answer the campaign question.
2. **Reporting synthetic data as real.** Label all mock data clearly.
3. **Ignoring funnel stage.** Awareness campaigns should not be judged like direct-response campaigns.
4. **Overclaiming attribution.** Be honest about what can and cannot be known.
5. **Skipping the hypothesis.** Measurement should test a belief, not just count activity.

## Verification Checklist

- [ ] Primary KPI matches the campaign objective.
- [ ] Secondary KPIs explain performance, not just volume.
- [ ] Hypothesis is clear and testable.
- [ ] Tracking assumptions are explicit.
- [ ] Synthetic or missing data is labelled.
