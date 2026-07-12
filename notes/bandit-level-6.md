# Bandit Level 6 → Level 7

**Date:** 2026-07-12

## Goal
Find a file somewhere on the entire server with specific ownership and size.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit6@bandit.labs.overthewire.org -p 2220` | Log into Level 6 |
| `find / -type f -user bandit7 -group bandit6 -size 33c 2&gt;/dev/null` | Search entire filesystem |
| `cat /var/lib/dpkg/info/bandit7.password` | Read the found file |
| `exit` | Log out |

## What I Learned
- `find /` searches the entire server from root
- `-user` and `-group` filter by ownership
- `2&gt;/dev/null` hides "Permission denied" errors
- Brackets `[]` in instructions are placeholders, not part of actual commands

## Password for Level 7
[REDACTED - saved locally]

## Next Level
[Bandit Level 7](https://overthewire.org/wargames/bandit/bandit7.html)
