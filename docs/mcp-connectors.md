# MCP Connectors

MCP connectors are the bridge between agents and external systems. They let agents use tools without giving every agent unlimited access to everything.

## Connector design principle

Each connector should expose only the access needed for the task. Read-only is preferred unless the agent genuinely needs to write. Customer-facing write actions should require human approval.

## Planned connector categories

### Knowledge connectors

- Obsidian or local markdown vault
- GitHub repo for public docs and skills
- Google Drive for operational files

### Data connectors

- Google Analytics / exports
- Search Console / exports
- Ad platform exports
- CRM or sales summaries

### Channel connectors

- X/Twitter drafting or posting
- Discord community monitoring
- Telegram community monitoring
- CMS draft creation
- Email/newsletter draft creation

## Access model

| Agent | Default access | Write access | Approval needed |
|---|---|---|---|
| Orchestrator | Kanban, skills, brief docs | Kanban tasks, shift reports | For changing external/public systems |
| Research | Public sources, reference KB | Research notes | For storing sensitive/community data |
| Performance Analyst | Operational exports | Analysis notes, experiment proposals | For changing campaigns/budgets |
| Content | Brand KB, briefs, research notes | Draft docs | Before publication |
| Social & Community | Brand KB, approved content, community exports | Draft posts/responses | Before posting |
| SEO | Brand KB, content inventory, search exports | SEO briefs/recommendations | Before CMS changes |

## Public repo boundary

This repo documents connector assumptions. It does not include credentials, tokens, private API responses, or raw operational data.

## Future implementation notes

When connectors are actually wired up, each should document:

- What the connector can read
- What the connector can write
- Which agents can use it
- What needs human approval
- Where credentials live
- How logs/audits are retained
