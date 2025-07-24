## Day 3 – Ownership, Groups, and Playing God (with chown)

Today was all about who owns what. And how to steal it back.

### 🔍 Learned:
- `ls -l` ➤ Shows owner and group
- `chown user file` ➤ Changes file owner
- `chgrp group file` ➤ Changes group
- `sudo chown abdur:abdur test.txt` ➤ When `root` owns it, reclaim it
- `stat file` ➤ Detailed metadata

### 🔄 Experiment:
```bash
touch hack.txt
sudo chown root:root hack.txt
ls -l hack.txt
sudo chown $USER:$USER hack.txt
