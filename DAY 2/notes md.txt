# 🔐 Day 2 – Users & Permissions Mastery (Linux)

## 👥 User Management

- List users: `cut -d: -f1 /etc/passwd`
- Add user: `sudo adduser pcxuser`
- Add sudo: `sudo usermod -aG sudo pcxuser`
- Switch user: `su - pcxuser`
- Show current user: `whoami`
- Show UID/GID: `id`
- See all logged-in users: `w`, `who`

## 👥 Group Management

- List groups: `cut -d: -f1 /etc/group`
- Add group: `sudo groupadd devs`
- Add user to group: `sudo usermod -aG devs pcxuser`
- Show user groups: `groups pcxuser`
- Change default group: `sudo usermod -g devs pcxuser`

## 🛡️ File Permissions

- View: `ls -l`
- Change permission: `chmod 755 file`
- Lock file: `chmod 000 file`
- Make file executable: `chmod +x file`
- Change ownership: `sudo chown pcxuser:pcxuser file`
- Reset ownership: `sudo chown $USER:$USER file`
- Delete protected file: `sudo rm file`

## 🔍 Special Cases

- `---x------`: execute-only by owner
- `chmod u+rwx`: full access to owner
- `chmod go-rwx`: restrict group & others

---

## 🧪 Practice

```bash
# Create user
sudo adduser pcxuser

# Give sudo
sudo usermod -aG sudo pcxuser

# Switch user
su - pcxuser

# Create file and test permissions
touch test.sh
chmod 000 test.sh
chmod u+x test.sh
sudo chown root:root test.sh
sudo chown $USER:$USER test.sh
chmod 755 test.sh
