# Bandit Level 2 → Level 3

**Date:** 2026-07-11

## Goal
Read a file with spaces in the name that also starts with `--`.

## The Problem
The filename is `--spaces in this filename--`. Two issues:
1. Spaces in the filename
2. Starts with `--` which `cat` interprets as "end of options"

## Failed Attempts

| Command | Result |
|---------|--------|
| `cat "spaces in this filename"` | No such file (missing `--`) |
| `cat "-spaces in this filename-"` | Wrong number of dashes |
| `cat ./--spaces in this filename--` | Shell still split on spaces |

## What Worked

```bash
cat -- "./--spaces in this filename--"
