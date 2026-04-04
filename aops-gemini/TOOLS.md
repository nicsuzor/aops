---
name: tools
title: Tools Index
type: index
category: framework
description: |
    Reference for MCP servers and standard tools available to the agent.
    Used by hydrator for routing decisions - what capabilities exist.
permalink: tools
tags: [framework, routing, tools, index]
---

# Tools Index

Reference for agent capabilities. Use this to understand what operations are possible.

## Core Server

| Server | Purpose                 | Key Operations                                           |
| ------ | ----------------------- | -------------------------------------------------------- |
| `pkb`  | Personal knowledge base | Tasks, semantic search, knowledge graph, memories, notes |

PKB is always available. See CONNECTORS.md for optional tool categories.

## Connector Categories

These are optional tools resolved at runtime. Skills reference them as `~~category`.

| Category         | Placeholder          | Purpose                                                        |
| ---------------- | -------------------- | -------------------------------------------------------------- |
| Email & calendar | `~~email`            | Search/read/draft messages, list events, create meetings       |
| Research library | `~~research-library` | Search papers, get citations, find similar works               |
| Case database    | `~~case-database`    | Search decisions, get case summaries, legal reasoning analysis |
| Documentation    | `~~documentation`    | Look up API docs for any programming library                   |
| AI assistant     | `~~ai-assistant`     | Delegate analysis to another AI model                          |

<!-- NS: exclude Standard Tools from this file. -->

## Standard Tools

| Tool        | Purpose                |
| ----------- | ---------------------- |
| `read_file`      | Read file contents     |
| `write_file`     | Create new files       |
| `replace`      | Modify existing files  |
| `Bash`      | Run shell commands     |
| `glob`      | Find files by pattern  |
| `grep_search`      | Search file contents   |
| `Task`      | Spawn subagents        |
| `WebFetch`  | Fetch web page content |
| `WebSearch` | Search the web         |

## Routing Hints

- **Email work** → use `~~email` connector (e.g., Outlook, Gmail)
- **Research/citations** → use `~~research-library` (e.g., Zotero) or `~~case-database`
- **Remember context** → `pkb` server: `create_memory`, `search`, `append`
- **Task management** → `pkb` server: `create_task`, `update_task`, `list_tasks`, `complete_task`
- **Documentation lookup** → use `~~documentation` connector (e.g., Context7)
