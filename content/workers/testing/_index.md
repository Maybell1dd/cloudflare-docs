---
pcx_content_type: navigation
title: Testing
weight: 9
---

# Testing

There are many ways of testing Workers and Pages projects. This section gives an overview of the different types of tools we provide for testing and debugging.

{{<directory-listing showDescriptions="true">}}

## Testing comparison matrix

| Feature                                   | Vitest&nbsp;Pool | `unstable_dev()` | Miniflare's&nbsp;API |
| ----------------------------------------- | ---------------- | ---------------- | -------------------- |
| Unit testing                              | ✅               | ❌               | ❌                   |
| Integration testing                       | ✅               | ✅               | ✅                   |
| Loading Wrangler configuration files      | ✅               | ✅               | ❌                   |
| Bindings directly in tests                | ✅               | ❌               | ✅                   |
| Isolated per-test storage                 | ✅               | ❌               | ❌                   |
| Outbound request mocking                  | ✅               | ❌               | ✅                   |
| Multiple Workers support                  | ✅               | 🚧[^1]           | ✅                   |
| Direct access to Durable Object instances | ✅               | ❌               | ❌                   |
| Run Durable Object alarms immediately     | ✅               | ❌               | ❌                   |
| List Durable Objects                      | ✅               | ❌               | ❌                   |
| Testing Service Workers                   | ❌               | ✅               | ✅                   |

[^1]: Support for multiple workers in `unstable_dev()` relies on `wrangler dev`'s service registry which can be unreliable when running multiple tests in parallel.