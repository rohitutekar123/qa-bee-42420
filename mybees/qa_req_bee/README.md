# OOM Fix Bee

When a container is OOM-killed or crash-looping, decides whether the limit is too low, the app
leaks, or something else is wrong, and raises the limit, opens a PR, or files a leak ticket.
Same folder layout as `bad_rollout/`; it uses no MCP integrations, so it has no `mcp.yaml`.
