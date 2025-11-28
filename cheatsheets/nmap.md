# 🛰️ Nmap Cheat Sheet

**Maintained by Ox1deSec**

---

## 🔍 Basic Scans
```bash
nmap <target-ip>              # Default scan
nmap -sC -sV <target-ip>      # Default scripts + version detection
nmap -A <target-ip>           # Aggressive scan (OS, version, scripts, traceroute)
```
---

## ⚡ Port Scanning
```bash
nmap -p 80 <target-ip>        # Scan specific port
nmap -p 1-65535 <target-ip>   # Scan all ports
nmap -p- <target-ip>          # Shortcut for all ports
```
---

## 🧩 Service & Version Detection
```bash
nmap -sV <target-ip>          # Detect service versions
nmap -sV --version-all <target-ip> # Try harder for version detection
```
---

## 🔐 OS Detection
```bash
nmap -O <target-ip>           # Detect operating system
nmap -A <target-ip>           # Aggressive scan includes OS detection

```
---

## 🛠️ Common Flags
```bash
-Pn → Treat all hosts as online (skip ping)

-sS → TCP SYN scan (stealthy)

-sU → UDP scan

-T4 → Faster execution (less stealthy)

--top-ports 20 → Scan top 20 most common ports
```
---

## 🧩 Example Workflow
```bash
nmap -sC -sV -oN initial.txt <target-ip>
nmap -p- -T4 -oN full.txt <target-ip>
nmap -A -oN aggressive.txt <target-ip>
```

---

## ⚡ Identity
Maintained by **Ox1deSec** 

“Enumerate, exploit, remediate — repeat.”

