# Bandit Level 22 → Level 23

**Date:** 2026-07-29

## Goal
Understand a cron script that hashes the username to generate a filename, then find the password for bandit23.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit22@bandit.labs.overthewire.org -p 2220` | Log into Level 22 |
| `cat /usr/bin/cronjob_bandit23.sh` | Read the cron script |
| `bash /usr/bin/cronjob_bandit23.sh` | Execute to see debug output |
| `echo "I am user bandit23" | md5sum | cut -d ' ' -f 1` | Calculate hash for bandit23 |
| `cat /tmp/8ca319486bfbbc3663ea0fbe81326349` | Read password file |
| `exit` | Log out |

## What I Learned
- `whoami` returns current username
- `md5sum` generates MD5 hash of input
- `cut -d ' ' -f 1` extracts first field (the hash)
- Scripts can use dynamic filenames based on user identity
- Running a script as different user produces different output
- Cron jobs run as specific users, affecting file locations

## Password for Level 23
[REDACTED - saved locally]

## Next Level
[Bandit Level 23](https://overthewire.org/wargames/bandit/bandit23.html)
