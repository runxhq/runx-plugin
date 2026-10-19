---
name: runx-discovery
description: Find and inspect published Runx skills, then explain the local execution prerequisites without claiming the hosted MCP executed them.
---

# Runx skill discovery

Use this skill when a user asks whether a Runx skill exists, what it does, what authority it needs, or how to try it locally.

1. Search the hosted catalog with `search_skills` using the user's task, then inspect a relevant match with `get_skill`.
2. Ground the answer in the returned skill name, version, source, requirements and license. If a field is missing, say it is unknown.
3. Give the installation or execution path from the inspected skill and the [Runx docs](https://runx.ai/docs). Local execution uses the Runx runtime, explicit authority and a receipt; this hosted connection provides discovery only.
4. Do not infer that a skill is installed, runnable in the current workspace, approved to use a provider, or successfully executed from a search result. Ask the user for the local runtime state or a receipt if they need those claims verified.
