# Automated Metasploit Lab in VMware (Kali + Metasploitable2)

## Overview

This project demonstrates a small penetration testing lab running inside VMware, using:

- Kali Linux (attacker)
- Metasploitable2 (target)
- Metasploit Framework
- Nmap

The goal is to show a repeatable, automated attack chain using Metasploit resource scripts (.rc files) to:

1. Perform reconnaissance (Nmap + Metasploit database)
2. Identify vulnerable services
3. Automatically exploit known vulnerabilities
4. Interact with sessions
5. Record results and learning notes

This is designed as a learning project and for portfolio demonstration only. All testing is performed on intentionally vulnerable machines that you control.

## Lab environment

- Hypervisor: VMware
- Attacker VM: Kali Linux
- Target VM: Metasploitable2
- Network: Host-only or Internal (isolated)

Example IPs:

- Kali: 192.168.253.128
- Metasploitable2: 192.168.253.129

## Basic connectivity test

From Kali:

```bash
ping -c 4 192.168.253.129


