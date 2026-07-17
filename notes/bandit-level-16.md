# Bandit Level 16 → Level 17

**Date:** 2026-07-17

## Goal
Find the credential server among ports 31000-32000, submit password via SSL, and retrieve an SSH key.

## Commands Used

| Command | Purpose |
|---------|---------|
| `nmap -p 31000-32000 localhost` | Find open ports |
| `openssl s_client -connect localhost:PORT -quiet` | Test SSL ports |
| `echo "password" | openssl s_client -connect localhost:31790 -quiet 2&gt;/dev/null` | Submit password to SSL port |
| `sed '1d' /tmp/bandit17.key &gt; /tmp/bandit17_clean.key` | Remove "Correct!" line from response |
| `scp -P 2220 bandit16@...:/tmp/bandit17_clean.key bandit17.key` | Transfer key to local machine |
| `ssh -i bandit17.key bandit17@bandit.labs.overthewire.org -p 2220` | SSH with private key |

## What I Learned
- `nmap` scans port ranges efficiently
- SSL servers can be tested with `openssl s_client`
- Credential servers may prepend confirmation text ("Correct!")
- `sed '1d'` removes the first line from a file
- `2&gt;/dev/null` suppresses SSL handshake errors
- SCP transfers files securely between remote and local
- Always verify key file format with `head` and `tail`

## Key Challenges
- Multiple SSL ports, only one gives credentials
- Server response included "Correct!" before the key
- File transfer and permissions issues on Windows
- `openssl s_client` behavior differs between interactive and piped modes

## Password for Level 17
[REDACTED - saved locally]

## Next Level
[Bandit Level 17](https://overthewire.org/wargames/bandit/bandit17.html)
