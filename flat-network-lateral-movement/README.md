# Flat Network Lateral Movement Lab

## Overview
This lab demonstrates how a flat enterprise network design enables unrestricted lateral movement following a single host compromise.

Rather than focusing on exploitation techniques, this lab analyzes how the absence of segmentation and monitoring allows an attacker to move freely across systems with minimal resistance or visibility.

---

## Lab Objectives

- Design a flat enterprise-style network
- Analyze attacker movement after initial access
- Identify missing security and detection controls
- Understand why lateral movement often goes unnoticed
- Establish a baseline for why segmentation matters

---

## Network Design

The network consists of:
- A single flat subnet
- Multiple hosts representing users and servers
- No internal segmentation or access controls
- Minimal monitoring or logging

This design reflects many real-world environments that prioritize simplicity over security.

---

## Attack Path Analysis

Once an attacker gains access to any host:
- All systems are reachable at Layer 3
- No trust boundaries restrict east-west movement
- Lateral movement requires little to no evasion

This lab focuses on understanding *why* movement is possible, not just that it is.

---

## Detection & Visibility Gaps

Key gaps demonstrated:
- No visibility into east-west traffic
- No internal controls to generate meaningful alerts
- Limited ability to distinguish normal vs malicious movement

This highlights why perimeter-focused monitoring fails in flat networks.

---

## Mitigation Preview

Future labs will demonstrate:
- Proper network segmentation
- Access control enforcement
- Improved monitoring placement

This lab serves as the insecure baseline for comparison.
