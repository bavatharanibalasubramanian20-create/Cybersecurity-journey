# Bandit Level 5 → Level 6

**Date:** 2026-07-12

## Goal
Find a file with three specific properties: human-readable, 1033 bytes, not executable.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit5@bandit.labs.overthewire.org -p 2220` | Log into Level 5 |
| `cd inhere` | Change directory |
| `find . -type f -size 1033c ! -executable` | Search for file by properties |
| `cat ./maybehere07/.file2` | Read the found file |
| `exit` | Log out |

## What I Learned
- `find` can search by multiple properties at once
- `-type f` = only files, not directories
- `-size 1033c` = exactly 1033 bytes
- `! -executable` = not executable
- `find` returns full paths including subdirectories

## Password for Level 6
[REDACTED - saved locally]

## Next Level
[Bandit Level 6](https://overthewire.org/wargames/bandit/bandit6.html)
