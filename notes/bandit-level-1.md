# Bandit Level 1 → Level 2

**Date:** 2026-07-10

## Goal
Read a file named `-` (dash) in the home directory.

## The Problem
A filename that is just `-` is interpreted as a command option, not a file.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit1@bandit.labs.overthewire.org -p 2220` | Log into Level 1 |
| `ls` | List files |
| `cat ./-` | Read file using relative path |
| `exit` | Log out |

## What I Learned
- Filenames starting with `-` are special characters in Linux
- `./` prefix tells the shell "this is a file in current directory"
- Absolute path `/home/bandit1/-` would also work

## Password for Level 2
[REDACTED - saved locally]

## Next Level
[Bandit Level 2](https://overthewire.org/wargames/bandit/bandit2.html)
