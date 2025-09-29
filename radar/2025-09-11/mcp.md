---
title: "MCP (Model Context Protocol)"
ring: adopt
quadrant: frameworks
tags: []
---

The Model Context Protocol (MCP) is an open protocol for safely exposing tools,
data sources, and system capabilities to AI assistants and IDE / CLI agent runtimes
in a standardized way. It defines how a client (assistant runtime / IDE) discovers,
lists, and invokes server-provided resources (tools, prompts, data references)
over a bidirectional transport (e.g., stdio, WebSocket). MCP promotes
interoperability, composability, and security auditing versus bespoke plugin SDKs.