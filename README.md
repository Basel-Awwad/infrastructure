# Infrastructure Projects Portfolio

This repository contains practical infrastructure and network engineering projects based on real-world scenarios.

All company names, public IP addresses, internal networks, customer information, and sensitive configurations have been anonymized.

## Projects

### 1. IPsec VPN Transit Architecture

A VPN transit solution designed to migrate production services behind a new firewall without requiring configuration changes from the external partner.

The existing IPsec VPN tunnel between the partner and the DR firewall was retained. A new IPsec tunnel was established between the Production firewall and the DR firewall.

The DR firewall operates as a transit gateway, routing traffic between the new Production environment and the existing Partner VPN.

#### Business Requirement

The external partner was unable to change the existing VPN peer configuration.

The objective was to:

- Move production services behind a new firewall.
- Preserve the existing Partner VPN configuration.
- Avoid downtime and Partner-side changes.
- Maintain bidirectional communication between PROD and the Partner network.

#### Solution

- Retained the existing Partner-to-DR IPsec VPN tunnel.
- Created a new IPsec VPN tunnel between PROD and DR.
- Used the DR firewall as a transit gateway.
- Configured firewall policies for bidirectional traffic.
- Applied NAT policies where required.
- Used anonymized Phase 2 selectors and IP addresses.

