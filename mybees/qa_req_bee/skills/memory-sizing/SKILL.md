---
name: memory-sizing
description: How to pick a new memory request and limit for a container. Use before proposing any limit change.
---
# Memory sizing guide (example; the customer replaces this)

- New limit = p99 of 7-day working set x 1.3, rounded up to the next 64Mi.
- Request = p50 of 7-day working set, never above the limit.
- Never more than the `max_limit_increase_pct` setting in one change; propose the capped value
  and say the cap applied.
- JVM workloads: also check -Xmx; raising the container limit without -Xmx changes nothing.
