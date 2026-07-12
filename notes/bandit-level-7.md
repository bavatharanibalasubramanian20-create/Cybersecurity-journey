# Bandit Level 7 → Level 8

**Date:** 2026-07-12

## Goal
Find the password in `data.txt` next to the word "millionth".

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit7@bandit.labs.overthewire.org -p 2220` | Log into Level 7 |
| `grep "millionth" data.txt` | Search for pattern in file |
| `exit` | Log out |

## What I Learned
- `grep` searches for text patterns in files
- `grep "pattern" filename` returns matching lines
- Useful for finding specific data in large files

## Password for Level 8
[REDACTED - saved locally]

## Next Level
[Bandit Level 8](https://overthewire.org/wargames/bandit/bandit8.html)
