---
project: /home/vantt/projects/obsidian-hybrid-search
sources: [README.md, AGENTS.md, CLAUDE.md]
source_hash: e68da047d940a839
model: haiku
generated: "2026-11-10T03:23:47.988Z"
body_hash: 3328b3c0016b3dd2
---
Obsidian Hybrid Search is an npm package that searches a local Obsidian vault by meaning, exact words, titles, aliases, tags, and links, and returns results through a CLI, JSON-lines IPC, or an MCP server. It is for Obsidian users who want to find and reuse their own notes, and for AI agents that should start from those notes and cite their sources. It runs locally by default with SQLite, FTS5, and sqlite-vec, and can optionally call OpenAI-compatible embedding APIs. It also includes a native Obsidian plugin for search while writing.
