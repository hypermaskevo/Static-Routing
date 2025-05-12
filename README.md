# Static-Routing
This lab demonstrates how to configure **static routes** between multiple routers to enable end-to-end communication between hosts on different subnets using **Cisco Packet Tracer**.
## 🧪 Lab Overview

- **Goal:** Configure static routes so that **PC1** can successfully ping **PC2**.
- **Topology:** 3 routers (R1, R2, R3), 2 PCs (PC1, PC2), and switches in between.
- **Subnets:**
  - `192.168.1.0/24` — PC1's network
  - `192.168.12.0/24` — Between R1 and R2
  - `192.168.13.0/24` — Between R2 and R3
  - `192.168.3.0/24` — PC2's network

## 🔧 Configuration Steps

1. **Assign IP addresses** to all router interfaces and PCs as shown in the topology.
2. **Set default gateways** on:
   - PC1: `192.168.1.254`
   - PC2: `192.168.3.254`
3. **Configure static routes**:
   - On **R1**, add a route to `192.168.3.0/24` via `192.168.12.2`
   - On **R2**, add routes:
     - To `192.168.1.0/24` via `192.168.12.1`
     - To `192.168.3.0/24` via `192.168.13.2`
   - On **R3**, add a route to `192.168.1.0/24` via `192.168.13.1`

## 📁 File Info

- **File Name:** `Day 11 - Configuring Static Routes.pkt`
- **Software Required:** Cisco Packet Tracer
- **Difficulty:** 🟡 Intermediate

## ✅ Learning Objectives

- Practice assigning IP addresses to interfaces
- Understand the concept of routing tables and static routing
- Learn to test connectivity using `ping` and `tracert`

## 📷 Preview

![image](https://github.com/user-attachments/assets/40ca2f95-271c-417a-ac4e-3c9d3c4d27a7)


---

> 🧠 *Tip:* Use the `show ip route` command to verify that routes are correctly added on each router.

## 📚 Author
Yurii Vysotskyi —  surl.li/fsjjyv
