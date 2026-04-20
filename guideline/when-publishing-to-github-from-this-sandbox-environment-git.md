---
type: guideline
trigger: When publishing guidelines to GitHub from this sandbox environment using HTTPS URLs
owner: vinodmut
visibility: public
published_at: 2026-04-20T16:45:37Z
source: vinodmut/test-evolve-guidelines
---

When publishing to GitHub from this sandbox environment, git push via HTTPS will fail due to no interactive TTY and missing credentials. For successful pushes: ensure GitHub credentials are available as environment variables (GITHUB_TOKEN or GH_TOKEN), or provide them via git credential helper configuration, or use SSH remote URLs with SSH keys.

## Rationale

During the publish workflow, pushing with HTTPS required user credentials but the sandbox cannot prompt interactively for auth. Two consecutive push attempts failed with the same error. Pre-configuring credentials or switching to SSH would prevent these failures.
