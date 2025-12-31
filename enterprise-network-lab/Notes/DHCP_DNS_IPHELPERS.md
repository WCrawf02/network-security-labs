# DHCP, DNS, and IP Helper Configuration

This document outlines how DHCP relay (ip helper-address) was configured
to support multiple VLANs with centralized services.

Key points:
- DHCP server located in Server VLAN
- IP helpers configured on SVIs
- APIPA troubleshooting and resolution

## Overview
This lab uses a centralized DHCP and DNS server to support multiple VLANs
across an enterprise network.

## DHCP Design
- Single DHCP server located in the Server VLAN
- Separate DHCP scopes per VLAN
- Clients receive IPs dynamically

## IP Helper Configuration
- `ip helper-address` configured on all VLAN SVIs
- Allows DHCP broadcast traffic to reach the server

## DNS Configuration
- Central DNS server
- Sales and VPN VLANs explicitly permitted via ACLs

## Why This Matters
This design reflects real enterprise environments where services are centralized
and access is controlled via routing and ACL policies.
