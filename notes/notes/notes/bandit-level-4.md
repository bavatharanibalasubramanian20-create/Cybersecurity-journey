# Bandit Level 4 → Level 5

**Date:** 2026-07-11

## Goal
Find the only human-readable file among 10 files in the `inhere` directory.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit4@bandit.labs.overthewire.org -p 2220` | Log into Level 4 |
| `cd inhere` | Change directory |
| `ls` | List files |
| `file ./*` | Check file types of all files at once |
| `cat ./-file07` | Read the ASCII text file |
| `exit` | Log out |

## What I Learned
- `file` command identifies file types without opening them
- `file ./*` checks all files in a directory efficiently
- `ASCII text` = human-readable
- `data`, `OpenPGP Secret Key` = binary/non-readable

## Password for Level 5
[REDACTED - saved locally]

## Next Level
[Bandit Level 5](https://overthewire.org/wargames/bandit/bandit5.html)
