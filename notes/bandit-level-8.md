# Bandit Level 8 → Level 9

**Date:** 2026-07-12

## Goal
Find the only line in `data.txt` that occurs exactly once.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit8@bandit.labs.overthewire.org -p 2220` | Log into Level 8 |
| `sort data.txt \| uniq -u` | Sort and find unique lines |
| `exit` | Log out |

## What I Learned
- `sort` arranges lines alphabetically
- `uniq -u` shows only lines that appear exactly once
- `|` (pipe) connects commands: output of first becomes input of second
- `sort` must come before `uniq` because `uniq` only detects adjacent duplicates

## Password for Level 9
[REDACTED - saved locally]

## Next Level
[Bandit Level 9](https://overthewire.org/wargames/bandit/bandit9.html)
