# Bandit Level 11 → Level 12

**Date:** 2026-07-15

## Goal
Decode a ROT13-encrypted password from `data.txt`.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit11@bandit.labs.overthewire.org -p 2220` | Log into Level 11 |
| `cat data.txt` | Read encoded file |
| `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'` | Decode ROT13 cipher |
| `exit` | Log out |

## What I Learned
- ROT13 is a substitution cipher that shifts letters by 13 positions
- `tr` command translates characters based on mapping
- ROT13 is its own inverse: applying it twice returns original text
- `A-Za-z` = all letters, `N-ZA-Mn-za-m` = ROT13 mapping
- Common in CTFs and basic obfuscation

## Password for Level 12
[REDACTED - saved locally]

## Next Level
[Bandit Level 12](https://overthewire.org/wargames/bandit/bandit12.html)
