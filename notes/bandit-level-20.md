# Bandit Level 20 → Level 21

**Date:** 2026-07-19

## Goal
Use a setuid binary that connects to a port and verifies a password to get the next level's credentials.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit20@bandit.labs.overthewire.org -p 2220` | Log into Level 20 |
| `nc -lk 8080 &` | Start persistent listener on port 8080 |
| `echo "PASSWORD" | nc -lk 8080 &` | Listener that sends password to connecting clients |
| `./suconnect 8080` | Binary connects to port, receives password, verifies, returns next password |
| `exit` | Log out |

## What I Learned
- `nc -lk` keeps listening after each connection (`-k` = keep listening)
- `echo "text" | nc -lk PORT` creates a listener that sends text to anyone who connects
- `suconnect` connects first, then reads the password from the listener
- Timing matters: the listener must be ready before the binary connects
- The binary takes only a port number, not a hostname

## Key Mistakes
- Tried `localhost 8080` as two arguments — binary only takes port
- Sent password before binary connected — listener was empty when binary read it
- Used `nc -l` without `-k` — listener closed after first connection

## Password for Level 21
[REDACTED - saved locally]

## Next Level
[Bandit Level 21](https://overthewire.org/wargames/bandit/bandit21.html)
