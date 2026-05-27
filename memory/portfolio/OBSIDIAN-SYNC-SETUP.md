# Obsidian Sync Setup for Agency Portfolio

This document covers how to set up Obsidian Sync for multi-client agency vaults.

## Prerequisites

- Obsidian installed on each team member's machine
- [Obsidian Sync](https://obsidian.md/sync) subscription ($10/user/month)
- Each client vault created and populated via the `intake` skill

## Vault structure

```
~/your-agency/
  client-a/          <- one vault per client
    walter-code/
    DASHBOARD.md
  client-b/
    walter-code/
  portfolio/         <- portfolio manager vault
    DASHBOARD.md
    scans/
    alerts/
    reports/
```

## Per-client vault setup

1. Create a new Obsidian vault for each client from the `memory/` templates
2. Enable Obsidian Sync in each vault's Settings → Sync
3. Create one remote vault per client (named after the client)
4. Share each vault only with team members who work on that client
5. **Never share a client's vault with other clients**

## Portfolio vault setup

1. Create a separate Obsidian vault for the portfolio manager
2. Enable Obsidian Sync on it
3. Share with principals and team leads only

## Access matrix

| Vault | Shared with |
|---|---|
| client-a-vault | Account lead for Client A |
| client-b-vault | Account lead for Client B |
| portfolio-vault | Principals, team leads |

## Security rules

- Client vaults are never shared with other clients — even if the same agency owns both accounts
- The portfolio vault is read-only across client contexts
- Store no client-specific data in the portfolio vault — only cross-client intelligence
- Revoke access immediately when a team member leaves or changes accounts

## Related Skills

- `portfolio-manager` — reads across all client vaults
- `client-context` — foundation for each individual vault
