# Bandit Level 9 → Level 10

**Date:** 2026-07-12

## Goal
Find the password in `data.txt` among human-readable strings, preceded by `=` characters.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit9@bandit.labs.overthewire.org -p 2220` | Log into Level 9 |
| `strings data.txt \| grep "="` | Extract readable strings, filter for `=` |
| `exit` | Log out |

## What I Learned
- `strings` extracts human-readable text from binary/mixed files
- `strings` + `grep` filters output to find specific patterns
- Useful when data is hidden in binary files

## Password for Level 10
[REDACTED - saved locally]

## Next Level
[Bandit Level 10](https://overthewire.org/wargames/bandit/bandit10.html)
