# Week 3 — Linux, Network Traffic Analysis, Nmap, and Metasploit

This was the week I practiced the most and enjoyed the most. I experienced the steps of a penetration test with real tools.

## 📖 Topics I Learned

### Linux Basics
- File system hierarchy (`/`, `/home`, `/etc`, `/root`), paths (absolute/relative).
- Core commands: `ls`, `cd`, `pwd`, `cat`, `grep`, `find`, `chmod`, `whoami`, `hostname`, `id`.
- File permissions (read/write/execute, `rwx`), hidden files (start with `.`, shown by `ls -la`).
- Kali Linux: a Debian-based distribution for pentesters that ships with tools ready to use.

### Network Traffic Analysis (Wireshark / tcpdump)
- Capturing and inspecting packets; **Follow TCP Stream**, **Export Objects**.
- Seeing how unencrypted protocols (FTP, Telnet, HTTP, SMTP) carry usernames/passwords in **cleartext**.
- Filtering: `http`, `tcp.port == 80`, `ip.addr == ...`, `contains`.
- Command-line analysis with `tshark` / `tcpdump`.

### Nmap — Network Scanning
- The logic of host discovery and port scanning.
- Important parameters:
  - `-sV` → service/version detection
  - `-p-` → scan all ports (1–65535)
  - `-T4` → timing/speed template
  - `--top-ports` → scan the most common ports
- Identifying running services and versions from open ports.

### Metasploit Framework
- Module types: **Exploit** (abuses a vulnerability), **Payload** (code that runs afterward), **Auxiliary** (scanning/support), **Meterpreter** (advanced, in-memory payload).
- **Bind shell** (the target opens a port) vs **Reverse shell** (the target connects back to the attacker).
- Basic flow: `search` → `use` → `set RHOSTS/LHOST` → `check` → `exploit`.
- Key settings: **RHOSTS** = target IP, **LHOST** = your own IP (for the reverse connection), **LPORT**.
- Meterpreter commands: `getuid`, `sysinfo`, `shell`, `download/upload`.
- Generating payloads with `msfvenom`.

## 🧪 Practice — Exercises
- **Wireshark labs:** traffic analysis across various protocols, the risks of unencrypted data.
- **Nmap scanning:** scanning a real target and enumerating its services/versions.
- **Metasploit:** exploiting a known web service vulnerability (RCE) to get a session.
- **Arrow (Telnet exploitation):** finding an open Telnet service → logging in with default/weak credentials → basic reconnaissance.

> *Note: Lab answers/flags are not shared here for confidentiality — only the steps and learned concepts are explained.*

## 💡 Key Takeaways
- The **reverse shell** idea: even if the target's firewall blocks incoming connections, it works because the target connects to *us* — that's why `LHOST` = **your own IP**.
- Default passwords (`root:root`, `admin:admin`) are still one of the biggest vulnerabilities.
- `nmap -sV` is lowercase — uppercase `-Sv` throws an error (details matter!).
- Since Telnet is unencrypted, modern systems should replace it with SSH.

## ✅ Status
Week 3 tasks completed. All tasks across the three weeks are done. 🎉
