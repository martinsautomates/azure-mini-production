# Screenshot Gallery

All screenshots below were captured from the live environment before the resource group was deleted to stop billing. Images live in `screenshots/`.

## Networking

**Resource group — all 43 resources**
![Resource Group Overview](./screenshots/rg-overview.png)

**VNet — all 5 subnets with NSG and route table associations**
![VNet Subnets](./screenshots/vnet-subnets.png)

**rt-web — default route to Firewall**
![Route Table](./screenshots/rt-web-routes.png)

## Security — Network Security Groups

**nsg-web — HTTP/HTTPS in, Bastion SSH, deny rest of VNet**
![nsg-web](./screenshots/nsg-web-rules.png)

**nsg-app — Web-only on 8080, Bastion SSH, deny rest of VNet**
![nsg-app](./screenshots/nsg-app-rules.png)

**nsg-data — App-only, deny rest of VNet**
![nsg-data](./screenshots/nsg-data-rules.png)

## Azure Firewall

**Overview — public/private IP, Standard SKU**
![Firewall Overview](./screenshots/firewall-overview.png)

**DNAT rules — 80 & 443 → Web VM**
![DNAT Rules](./screenshots/firewall-dnat-rules.png)

**Network rules — DNS**
![Network Rules](./screenshots/firewall-network-rules.png)

**Application rules — Ubuntu repos & PyPI**
![Application Rules](./screenshots/firewall-app-rules.png)

## Compute

**vm-web — no public IP**
![vm-web Overview](./screenshots/vm-web-overview.png)

**vm-app — no public IP**
![vm-app Overview](./screenshots/vm-app-overview.png)

## Storage

**Blob container with entries written by the app**
![Storage Container](./screenshots/storage-container-entries.png)

**Private Endpoint — private IP in the Data subnet**
![Private Endpoint](./screenshots/storage-private-endpoint.png)

## Monitoring

**14 alert rules across both VMs**
![Alert Rules](./screenshots/alert-rules-list.png)

**VM Insights — both VMs monitored**
![VM Insights](./screenshots/vm-insights-monitored.png)

## Application & Connectivity Tests

**Outbound DNS + apt working through the Firewall (App VM)**
![Outbound Test](./screenshots/test-app-outbound.png)

**App VM → Storage Account succeeding**
![App to Storage](./screenshots/test-app-to-storage.png)

**Web VM → App VM succeeding (port 8080, via Bastion session)**
![Web to App](./screenshots/test-web-to-app.png)

**systemd — app.service active and running under Gunicorn**
![systemd Status](./screenshots/systemd-app-status.png)

**nginx active and running**
![nginx Status](./screenshots/nginx-status.png)

**Live demo — browser round-trip through Web → App → Storage**
![Live Demo](./screenshots/demo-page-entry-added.png)
