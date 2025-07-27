# 🔱 Red Team Arsenal

**Full-blown Red Team battleground in Docker — from Nmap to Ghidra, shell to Shodan, a total of 60+ tools and custom scripts all under one containerized roof.**

---

# Work in Progress Repository

---

## 🧠 About the Arsenal

Red Team Arsenal is a Docker-based offensive security lab tailored for ethical hackers, red teamers, and cybersecurity professionals. It combines CLI tools, GUI applications, and API-integrated scripts — all categorized and accessible via an interactive launcher.

---

## 📦 Tool Arsenal – Full List & Categorization

Each tool is tagged by type:

- 🧱 **CLI**: Terminal-based, supports automation  
- 🖥️ **UI**: GUI-based, requires X11/VNC/web port  
- 🔐 **API**: Script-based tools that require API keys

---

### 🔍 Reconnaissance & Scanning

| Tool           | Type  | Use |
|----------------|-------|-----|
| `nmap`         | CLI   | Network and port scanner with NSE scripting support |
| `amass`        | CLI   | Subdomain and DNS enumeration |
| `subfinder`    | CLI   | Passive subdomain enumeration |
| `assetfinder`  | CLI   | Quickly find domain assets |
| `rustscan`     | CLI   | Blazing fast port scanner |
| `gobuster`     | CLI   | Directory, DNS, and VHost brute-forcing |
| `wfuzz`        | CLI   | Web fuzzing for parameters, headers |
| `dirb`         | CLI   | Basic directory brute-forcing |
| `dirbuster`    | UI    | Java-based directory brute-forcing tool |
| `nikto`        | CLI   | Scan web servers for vulnerabilities |
| `theHarvester` | CLI   | Collect emails/domains from public sources |
| `recon-ng`     | CLI   | Recon framework with modular plugin system |
| `censys`       | API   | Internet-wide scan engine via API |
| `shodan`       | API   | Search connected devices across the internet |

---

### 📡 Enumeration

| Tool           | Type | Use |
|----------------|------|-----|
| `enum4linux`   | CLI  | SMB and NetBIOS enumeration |
| `smbclient`    | CLI  | SMB share interaction |
| `rpcclient`    | CLI  | Enumerate Windows info via RPC |
| `netcat`       | CLI  | Swiss army knife for networking |
| `telnet`       | CLI  | Protocol testing and banner grabbing |
| `crackmapexec` | CLI  | AD enumeration and credential spraying |

---

### 💥 Exploitation Frameworks & Payloads

| Tool          | Type | Use |
|---------------|------|-----|
| `metasploit`  | CLI  | Powerful exploit and post-exploit framework |
| `msfvenom`    | CLI  | Generate payloads for multiple platforms |
| `veil`        | CLI  | AV-evading payload and shellcode generator |
| `unicorn`     | CLI  | Inject shellcode using PowerShell |
| `thefatrat`   | CLI  | AV-bypassing reverse shell payload generator |
| `shellter`    | CLI  | Inject backdoors into Windows executables |
| `reverse shell generator` | CLI | Auto-generate reverse shells (PentestMonkey) |

---

### 🌐 Web Application Hacking

| Tool         | Type | Use |
|--------------|------|-----|
| `burp suite` | UI   | Intercepting proxy for web application testing |
| `owasp zap`  | UI   | Automated web vulnerability scanner |
| `sqlmap`     | CLI  | Automated SQL injection and DB exploitation |
| `xsstrike`   | CLI  | Automated XSS detection |
| `wapiti`     | CLI  | Web application scanner for XSS, SSRF, etc. |
| `nikto`      | CLI  | Server-side web vulnerability scanning |

---

### 🔐 Password Cracking & Auth Bypass

| Tool           | Type | Use |
|----------------|------|-----|
| `john`         | CLI  | Crack password hashes using wordlists |
| `hashcat`      | CLI  | GPU-accelerated password cracker |
| `hydra`        | CLI  | Fast login brute-forcer for many protocols |
| `medusa`       | CLI  | Parallel login brute-forcer |
| `crackmapexec` | CLI  | Credential validation on AD environments |

---

### 🧨 Privilege Escalation & Post Exploitation

| Tool        | Type | Use |
|-------------|------|-----|
| `mimikatz`  | CLI  | Extract credentials from Windows memory |
| `powersploit` | CLI | PowerShell-based post-exploitation framework |
| `nishang`   | CLI  | PowerShell scripts for exploitation |
| `linpeas`   | CLI  | Linux privilege escalation auditing |
| `winpeas`   | CLI  | Windows privilege escalation tool |
| `pspy`      | CLI  | Process snooping for cronjobs, hidden scripts |
| `lse.sh`    | CLI  | Linux Smart Enumeration tool |
| `les.sh`    | CLI  | Linux Exploit Suggester |
| `gtfobins`  | CLI  | Privilege escalation via Unix binaries |

---

### 🔒 Cryptography & Encoding Tools

| Tool       | Type | Use |
|------------|------|-----|
| `openssl`  | CLI  | Create/manage certs, encrypt/decrypt data |
| `gpg`      | CLI  | Secure file encryption using key pairs |
| `cyberchef`| UI   | Web-based decoder, encoder, hasher, etc. |

---

### ☁️ Cloud Hacking & Audit Tools

| Tool         | Type | Use |
|--------------|------|-----|
| `pacu`       | CLI  | AWS exploitation framework |
| `scoutsuite` | CLI  | Security audit for AWS, Azure, GCP |
| `prowler`    | CLI  | AWS CIS benchmark scanner |
| `cloudsploit`| CLI  | Cloud configuration scanner |
| `cloudgoat`  | CLI  | Create vulnerable AWS environments |

---

### 🧬 Reverse Engineering Tools

| Tool     | Type | Use |
|----------|------|-----|
| `ghidra` | UI   | Advanced disassembler and decompiler |
| `cutter` | UI   | GUI for radare2 with visualization |
| `radare2`| CLI  | Powerful binary analysis framework |
| `gdb`    | CLI  | Debug and reverse-engineer binaries |
| `strings`| CLI  | Extract printable characters from files |
| `ltrace` / `strace` | CLI | Monitor library and system calls |

---

### 🧰 Supporting Tools

| Tool              | Type | Use |
|-------------------|------|-----|
| `tmux` / `byobu`  | CLI  | Terminal multiplexer |
| `python3`, `pip`, `pwntools` | CLI | For automation, scripting, CTFs |
| `git`             | CLI  | Pull exploits, tools, configs |
| `proxychains`     | CLI  | Route traffic through proxies |
| `ngrok`, `localtunnel` | CLI | Tunnel external access |
| `neofetch`        | CLI  | Display system info for fun |

---

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/AdityaBhatt3010/Red-Team-Arsenal
cd Red-Team-Arsenal

# Build the Docker image
docker build -t redteam-arsenal .

# Run the container
docker run -it --rm \
  -v $(pwd)/loot:/opt/loot \
  -p 8080:8080 -p 1337:1337 \
  redteam-arsenal

# Launch the CLI tool selector
./arsenal.sh
```

---

## ⚠️ Legal Disclaimer

> This project is intended for **educational and authorized security testing** only. Do not use these tools on any systems or networks without proper permission.

---

## 👨‍💻 Author

**Aditya Bhatt** <br/>
Cybersecurity | Red Teaming | VAPT Specialist <br/>
* 📍 [GitHub](https://github.com/AdityaBhatt3010)  <br/>
* ✍️ [Medium](https://medium.com/@adityabhatt3010) <br/>

---
