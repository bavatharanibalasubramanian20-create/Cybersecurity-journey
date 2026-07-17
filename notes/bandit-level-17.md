# Bandit Level 17 → Level 18

**Date:** 2026-07-17

## Goal
Find the only changed line between two files.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit17@bandit.labs.overthewire.org -p 2220` | Log into Level 17 |
| `diff passwords.old passwords.new` | Compare two files |
| `exit` | Log out |

## What I Learned
- `diff` compares files line by line
- `&lt;` means line exists in first file only
- `&gt;` means line exists in second file only
- `---` separates the two sections

## Password for Level 18
[REDACTED - saved locally]

## Next Level
[Bandit Level 18](https://overthewire.org/wargames/bandit/bandit18.html)
