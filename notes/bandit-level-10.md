# Bandit Level 10 → Level 11

**Date:** 2026-07-12

## Goal
Decode base64 encoded password from `data.txt`.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit10@bandit.labs.overthewire.org -p 2220` | Log into Level 10 |
| `base64 -d data.txt` | Decode base64 encoded data |
| `exit` | Log out |

## What I Learned
- `base64` encodes binary data as text
- `base64 -d` decodes base64 back to original text
- Common encoding method for transferring data

## Password for Level 11
[REDACTED - saved locally]

## Next Level
[Bandit Level 11](https://overthewire.org/wargames/bandit/bandit11.html)
