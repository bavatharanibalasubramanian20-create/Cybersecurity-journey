# Bandit Level 18 → Level 19

**Date:** 2026-07-17

## Goal
Read `readme` file despite `.bashrc` logging out immediately on SSH login.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme"` | Run command directly, bypass interactive shell |
| `exit` | — |

## What I Learned
- `.bashrc` runs automatically when starting an interactive shell
- SSH can execute a remote command directly without starting a shell
- `ssh user@host "command"` runs the command and exits
- Useful when the target system has restrictive login configurations

## Password for Level 19
[REDACTED - saved locally]

## Next Level
[Bandit Level 19](https://overthewire.org/wargames/bandit/bandit19.html)
