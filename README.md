# NETWORKWALKS CYBERSECURITY INTERNSHIP - WEEK 1

## Project Details
* **Student Name:** [Albert Kenney Sackitey]
* **Batch:** B084
* **Week:** Week 1 (Project Module 1)
* **Project Title:** Lab Setup for Cybersecurity & Ethical Hacking Practice

---

## Lab Objectives & Tasks Completed
1. **Virtualization Setup:** Downloaded and installed Oracle VM VirtualBox.
2. **Attack Machine Deployment:** Installed and configured Kali Linux inside VirtualBox.
3. **VM State Management:** Created and saved a initial clean snapshot of Kali Linux.
4. **Network Configuration:** Configured a NAT / NAT Network interface to enable internet access and inter-VM communication.
5. **Network Diagnostics:** Verified connectivity using ICMP ping requests to external domains.

---

## Step-by-Step Implementation

### Step 1: Virtual Machine Setup
* Installed VirtualBox and imported/installed the Kali Linux image.
* Configured system hardware resources (RAM, Processors, Storage).

### Step 2: System Snapshot Creation
* Took a VM snapshot right after initial setup to preserve a clean baseline restore point before starting penetration testing labs.

### Step 3: Network Adapter & Connectivity Fix
* Configured the VirtualBox network adapter to **NAT / NAT Network**.
* Restarted and reconfigured the network interface using NetworkManager CLI (`nmcli`):
  ```bash
  sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
  sudo nmcli connection down "Wired connection 1"
  sudo nmcli connection up "Wired connection 1"
