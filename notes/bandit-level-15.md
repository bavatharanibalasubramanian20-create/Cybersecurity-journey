# Bandit Level 15 → Level 16

**Date:** 2026-07-16

## Goal
Submit the current level's password to port 30001 using SSL/TLS encryption.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit15@bandit.labs.overthewire.org -p 2220` | Log into Level 15 |
| `echo "PASSWORD" | openssl s_client -connect localhost:30001 -quiet` | Send password over SSL/TLS |
| `exit` | Log out |

## What I Learned
- `openssl s_client` connects to SSL/TLS encrypted ports
- `nc` does not handle encryption—use `openssl` for secure connections
- `-connect host:port` specifies the SSL endpoint
- `-quiet` suppresses certificate/connection details, showing only server response
- SSL/TLS is standard for secure network communication

## Password for Level 16
[REDACTED - saved locally]

## Next Level
[Bandit Level 16](https://overthewire.org/wargames/bandit/bandit16.html)
