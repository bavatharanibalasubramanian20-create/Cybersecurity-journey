# Bandit Level 13 → Level 14

**Date:** 2026-07-15

## Goal
Use a private SSH key to log in as bandit14 and read the password file.

## The Problem
The server blocks SSH connections from localhost (one level to another). The key must be used from your local machine.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit13@bandit.labs.overthewire.org -p 2220` | Log into Level 13 |
| `cat sshkey.private` | View the private key |
| `exit` | Log out from server |
| `notepad bandit14_key` (local) | Save key to local file |
| `ssh -i bandit14_key bandit14@bandit.labs.overthewire.org -p 2220` | SSH from local machine using key |
| `cat /etc/bandit_pass/bandit14` | Read password file |
| `exit` | Log out |

## What I Learned
- Private SSH keys authenticate without passwords
- `ssh -i keyfile user@host` uses a specific key
- OverTheWire blocks localhost connections between levels
- Keys must be saved locally with correct permissions (`chmod 600` or `icacls`)
- `cat HINT` provides crucial guidance when stuck
- Error messages are informative—read them carefully

## Password for Level 14
[REDACTED - saved locally]

## Next Level
[Bandit Level 14](https://overthewire.org/wargames/bandit/bandit14.html)
