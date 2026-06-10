# OverTheWire Bandit — Linux Security Wargame

## Objective
Complete the OverTheWire Bandit wargame challenges to develop Linux command-line security skills including file system navigation, privilege escalation concepts, SSH, encoding/decoding, and data extraction techniques.

---

## What is Bandit?
OverTheWire Bandit is a Linux-based wargame designed for beginners to learn security fundamentals through hands-on challenges. Each level requires finding a password hidden using increasingly complex Linux techniques to advance to the next level.

---

## Progress
Completed: **27+ levels**

| Level Range | Key Skills Practiced |
|---|---|
| 0-5 | SSH login, file reading, hidden files, spaces in filenames |
| 6-10 | find command, file permissions, grep, strings |
| 11-15 | Base64 decoding, ROT13, compression, SSH keys |
| 16-20 | Port scanning, SSL/TLS, setuid binaries, shell escapes |
| 21-27 | Cron jobs, bash scripts, git repositories, RSA private keys |

---

## Tools & Commands Used
| Tool / Command | Purpose |
|---|---|
| ssh | Remote login to each level |
| cat | Read file contents |
| ls -la | List hidden files and permissions |
| find | Locate files by size, owner, permissions |
| grep | Search file contents |
| strings | Extract readable text from binary files |
| base64 | Encode/decode data |
| tr | ROT13 character translation |
| file | Identify file types |
| gunzip / tar / bzip2 | Decompress files |
| nc (netcat) | Connect to ports |
| openssl | SSL/TLS connections |

---

## Notable Challenges

### Level 13-14 — SSH Private Key
- Retrieved an RSA private key instead of a password
- Used the key to authenticate to the next level:
  ssh -i sshkey.private bandit14@localhost -p 2220

### Level 17 — RSA Private Key (Multi-line)
- Password was a full RSA PRIVATE KEY block
- Required understanding of SSH key-based authentication

### Level 26 — SSH Key Only (No Password)
- Level 26 had no password — authentication via SSH key only
- Demonstrated real-world SSH key management concepts

---

## Key Takeaways
- Linux file permissions and the find command are essential for security work
- Many real-world vulnerabilities involve misconfigured file permissions and exposed credentials
- Encoding schemes (Base64, ROT13) are commonly used to obfuscate data
- SSH key authentication is more secure than password-based login
- Hands-on CTF-style challenges build the same skills used in SOC and penetration testing roles

---

## Skills Demonstrated
Linux CLI, SSH, File Permissions, grep, find, Base64, ROT13, Data Extraction, Netcat, OpenSSL, CTF Problem Solving, Security Fundamentals
