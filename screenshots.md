# Screenshot Checklist

Suggested filenames assume a `screenshots/` folder in the repo root. Check each off as you capture it. Redact your Subscription ID if it's visible in any shot.

## Networking

- [ ] Resource group overview, showing all resources — `screenshots/rg-overview.png`
- [ ] VNet overview showing all 5 subnets and their address ranges — `screenshots/vnet-subnets.png`

## Security — NSGs

- [ ] `nsg-web` inbound/outbound rules (full list, priorities visible) — `screenshots/nsg-web-rules.png`
- [ ] `nsg-app` inbound/outbound rules — `screenshots/nsg-app-rules.png`
- [ ] `nsg-data` inbound/outbound rules — `screenshots/nsg-data-rules.png`

## Route Tables

- [ ] `rt-web` routes showing 0.0.0.0/0 → Firewall — `screenshots/rt-web-routes.png`
- [ ] `rt-app` routes — `screenshots/rt-app-routes.png`
- [ ] `rt-data` routes — `screenshots/rt-data-routes.png`

## Azure Firewall

- [ ] Firewall overview (public IP + private IP visible) — `screenshots/firewall-overview.png`
- [ ] Firewall Policy — DNAT rule collection (80 & 443) — `screenshots/firewall-dnat-rules.png`
- [ ] Firewall Policy — Network rule collection (DNS) — `screenshots/firewall-network-rules.png`
- [ ] Firewall Policy — Application rule collection (ubuntu + pypi FQDNs) — `screenshots/firewall-app-rules.png`

## Bastion

- [ ] Bastion resource overview — `screenshots/bastion-overview.png`
- [ ] A successful Bastion session connected to `vm-web` — `screenshots/bastion-connected.png`

## Compute

- [ ] `vm-web` Overview page — confirm no public IP field — `screenshots/vm-web-overview.png`
- [ ] `vm-app` Overview page — confirm no public IP field — `screenshots/vm-app-overview.png`
- [ ] `vm-app` → Identity blade — System assigned: **On** — `screenshots/vm-app-identity.png`

## Storage

- [ ] Storage account overview — `screenshots/storage-overview.png`
- [ ] Blob container `app-data` with entries listed — `screenshots/storage-container-entries.png`
- [ ] Private Endpoint configuration (subnet = data-subnet, IP 10.0.3.4) — `screenshots/storage-private-endpoint.png`
- [ ] Networking blade — Public network access: **Disabled** — `screenshots/storage-public-access-disabled.png`
- [ ] IAM — Storage Blob Data Contributor assigned to `vm-app` identity — `screenshots/storage-rbac.png`

## Monitoring

- [ ] Log Analytics Workspace overview — `screenshots/law-overview.png`
- [ ] VM Insights "Monitored (2)" tab showing both VMs enabled — `screenshots/vm-insights-monitored.png`
- [ ] Alert rules list (all 14, showing Enabled status) — `screenshots/alert-rules-list.png`

## Connectivity & Isolation Tests (terminal output)

- [ ] `nslookup` + `apt update` succeeding on `vm-web` — `screenshots/test-web-outbound.png`
- [ ] `nslookup` + `apt update` succeeding on `vm-app` — `screenshots/test-app-outbound.png`
- [ ] `curl` from `vm-web` to `vm-app:8080` succeeding — `screenshots/test-web-to-app.png`
- [ ] `curl` from `vm-app` to storage account succeeding — `screenshots/test-app-to-storage.png`
- [ ] `curl` from `vm-web` to storage account **timing out** (isolation proof) — `screenshots/test-isolation-blocked.png`
- [ ] `systemctl status app` showing `active (running)` — `screenshots/systemd-app-status.png`

## Application Demo

- [ ] Browser showing the demo page loaded via the Firewall's public IP — `screenshots/demo-page-loaded.png`
- [ ] Browser after submitting a message, showing it listed with timestamp — `screenshots/demo-page-entry-added.png`

