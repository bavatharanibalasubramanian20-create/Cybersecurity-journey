# Bandit Level 12 → Level 13

**Date:** 2026-07-15

## Goal
Reverse a hexdump and decompress multiple layers to find the password.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit12@bandit.labs.overthewire.org -p 2220` | Log into Level 12 |
| `mktemp -d` | Create secure temp directory |
| `cp ~/data.txt .` | Copy file to working directory |
| `mv data.txt data.hex` | Rename for clarity |
| `xxd -r data.hex &gt; data.bin` | Reverse hexdump to binary |
| `file data.bin` | Check file type |
| `mv data.bin data.gz && gunzip data.gz` | Decompress gzip layer 1 |
| `mv data data.bz2 && bunzip2 data.bz2` | Decompress bzip2 layer |
| `mv data data.gz && gunzip data.gz` | Decompress gzip layer 2 |
| `mv data data.tar && tar xf data.tar` | Extract tar layer 1 |
| `file data5.bin && mv data5.bin data5.tar && tar xf data5.tar` | Extract tar layer 2 |
| `file data6.bin && mv data6.bin data6.bz2 && bunzip2 data6.bz2` | Decompress bzip2 layer 2 |
| `file data6 && mv data6 data6.tar && tar xf data6.tar` | Extract tar layer 3 |
| `file data8.bin && mv data8.bin data8.gz && gunzip data8.gz` | Decompress gzip layer 3 |
| `file data8 && cat data8` | Read final ASCII text |
| `exit` | Log out |

## Compression Layers Found

| Layer | Type | Tool Used |
|-------|------|-----------|
| 1 | Hexdump | `xxd -r` |
| 2 | gzip | `gunzip` |
| 3 | bzip2 | `bunzip2` |
| 4 | gzip | `gunzip` |
| 5 | tar | `tar xf` |
| 6 | tar | `tar xf` |
| 7 | bzip2 | `bunzip2` |
| 8 | tar | `tar xf` |
| 9 | gzip | `gunzip` |
| 10 | ASCII text | `cat` |

## What I Learned
- `xxd -r` reverses a hexdump back to binary
- `file` command identifies compression types without guessing
- Files can be nested with multiple compression layers
- `mktemp -d` creates secure temporary directories
- Always work in `/tmp` for file manipulation challenges
- Never guess compression type—always use `file` first

## Password for Level 13
[REDACTED - saved locally]

## Next Level
[Bandit Level 13](https://overthewire.org/wargames/bandit/bandit13.html)
