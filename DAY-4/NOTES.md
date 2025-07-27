# 🚀 Day 4: Linux File Permissions & Git Basics

## 🔐 Linux Permissions - Octal Magic

In Linux, every file/directory has **three types of users**:
- User (Owner)
- Group
- Others

And three types of permissions:
- Read (r) = 4
- Write (w) = 2
- Execute (x) = 1

### Common Permission Modes:
| Octal | Meaning           | Symbolic   |
|-------|-------------------|------------|
| 777   | Full for all      | rwxrwxrwx  |
| 755   | Only user writes  | rwxr-xr-x  |
| 700   | Private            | rwx------  |
| 644   | Read-only to others | rw-r--r-- |
| 600   | Private read/write | rw------- |
| 000   | No access         | ---------- |

### Set Permissions:
```bash
chmod 755 script.sh
chmod 644 notes.txt
chmod 700 secrets.txt
