# homelab-scripts

Scripts I use to run and keep an eye on the home lab — health checks, connectivity sweeps, and small automations for the things I got tired of doing by hand.

## One rule I stick to

No hardcoded IPs in anything that sweeps or checks the cluster. Early on, two separate problems got hidden because a script had the wrong IP baked into it and quietly reported bad results. Now node addresses get pulled dynamically (for example, from `pvecm`) instead of being hardcoded.

## Layout

- `health/` — node and service checks
- `network/` — connectivity, DNS, and VLAN checks
- `collection/` — pulling current state and inventory
- `maintenance/` — routine cleanup and admin tasks

(Adjust to match your repo.)

## Before running anything

Read the script first. These are written for my environment, so paths and hostnames will differ from yours. Everything here is checked with `shellcheck` in CI.
