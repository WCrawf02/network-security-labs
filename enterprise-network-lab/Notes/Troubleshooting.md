# Troubleshooting and Lessons Learned

## Issue: Clients Receiving APIPA (169.254.x.x)

### Root Cause
- Missing `ip helper-address` on VLAN interfaces
- Server interface not properly connected to core switch

### Resolution
- Verified SVI status using `show ip interface brief`
- Added `ip helper-address` to all VLAN SVIs
- Confirmed server VLAN routing

---

## Issue: Simulation Mode Red X Packets

### Root Cause
- Packet Tracer simulation mode shows control-plane traffic
- Red X does not always indicate failure

### Resolution
- Verified connectivity in real-time mode
- Confirmed successful pings and DHCP leases

---

## Issue: VLAN Traffic Blocked Unexpectedly

### Root Cause
- ACL direction or ordering issue
- Incorrect wildcard mask

### Resolution
- Verified ACL placement inbound on SVIs
- Tested permit statements before deny rules
- Used `show access-lists` to validate hit counts

---

## Verification Commands Used
- `show ip route`
- `show access-lists`
- `show ip interface`
- End-to-end ping testing per VLAN

## Key Takeaway
All issues were resolved through systematic isolation and verification rather
than guesswork.
