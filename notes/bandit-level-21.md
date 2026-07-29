# Bandit Level 21 → Level 22

**Date:** 2026-07-29

## Goal
Find the cron job that runs automatically and extract the password it writes.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit21@bandit.labs.overthewire.org -p 2220` | Log into Level 21 |
| `ls /etc/cron.d/` | List cron jobs |
| `cat /etc/cron.d/cronjob_bandit22` | Read cron configuration |
| `cat /usr/bin/cronjob_bandit22.sh` | Read the script being executed |
| `cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv` | Read the password file |
| `exit` | Log out |

## What I Learned
- `cron` runs commands automatically on a schedule
- `/etc/cron.d/` contains cron job configurations
- Cron jobs can write sensitive data to predictable locations
- Reading scripts reveals what commands run and where output goes

## Password for Level 22
[REDACTED - saved locally]

## Next Level
[Bandit Level 22](https://overthewire.org/wargames/bandit/bandit22.html)
