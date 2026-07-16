# Bandit Level 14 → Level 15

**Date:** 2026-07-16

## Goal
Submit the current level's password to port 30000 on localhost to retrieve the next password.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit14@bandit.labs.overthewire.org -p 2220` | Log into Level 14 |
| `cat /etc/bandit_pass/bandit14` | Verify correct password |
| `echo "PASSWORD" | nc localhost 30000` | Send password to port 30000 |
| `exit` | Log out |

## What I Learned
- `nc` (netcat) sends data over network connections
- `echo "text" | nc host port` pipes text to a network port
- Services can listen on ports and respond with data
- Always verify the exact password before submitting

## Password for Level 15
[REDACTED - saved locally]

## Next Level
[Bandit Level 15](https://overthewire.org/wargames/bandit/bandit15.html)
