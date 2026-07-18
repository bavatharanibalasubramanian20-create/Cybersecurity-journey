# Bandit Level 19 → Level 20

**Date:** 2026-07-19

## Goal
Use a setuid binary to run a command as bandit20 and read the password file.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit19@bandit.labs.overthewire.org -p 2220` | Log into Level 19 |
| `ls -la` | Find the setuid binary |
| `./bandit20-do` | Check usage instructions |
| `./bandit20-do cat /etc/bandit_pass/bandit20` | Run cat as bandit20 |
| `exit` | Log out |

## What I Learned
- `setuid` binaries run with the owner's permissions, not the user's
- `s` in permissions (`-rwsr-x---`) indicates setuid
- `./binary command` executes `command` with the binary owner's privileges
- Useful for privilege escalation scenarios

## Password for Level 20
[REDACTED - saved locally]

## Next Level
[Bandit Level 20](https://overthewire.org/wargames/bandit/bandit20.html)
