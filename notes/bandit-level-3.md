# Bandit Level 3 → Level 4

**Date:** 2026-07-11

## Goal
Find and read a hidden file in the `inhere` directory.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit3@bandit.labs.overthewire.org -p 2220` | Log into Level 3 |
| `ls` | List files |
| `cd inhere` | Change directory |
| `ls -la` | List all files including hidden |
| `cat ...Hiding-From-You` | Read hidden file |
| `exit` | Log out |

## What I Learned
- Hidden files start with `.` (dot)
- `ls` alone does not show hidden files
- `ls -la` shows all files including hidden ones
- Filenames can have multiple dots `...`

## Password for Level 4
[REDACTED - saved locally]

## Next Level
[Bandit Level 4](https://overthewire.org/wargames/bandit/bandit4.html)
