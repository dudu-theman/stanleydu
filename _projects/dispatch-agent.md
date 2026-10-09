---
layout: project
title: Dispatch Agent
tagline: AI intake and provider matching for home repairs. 
blurb: >-
  Tell it what's broken, get the top 3 local pros (Chicagoland only)
year: 2026
status: Live
order: 2
repo: https://github.com/dudu-theman/dispatch_agent
demo: https://dispatchagent-ui.vercel.app/
stack: [Python, FastAPI, SQLite]
mermaid: true
---

## Architecture

```mermaid
flowchart LR
    user["Homeowner"]
    agent["Claude: update lead"]
    check{"Lead complete?"}
    match["Match & rank local providers"]

    user -->|"message"| agent
    agent --> check
    check -->|"no: ask one question"| user
    check -->|"yes"| match
    match -->|"top 3 providers"| user
```
