---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

![bg left:40% 80%](https://marp.app/assets/marp.svg)

# **Marp**

Markdown Presentation Ecosystem

https://marp.app/

---

# How to write slides

Split pages by horizontal ruler (`---`). It's very simple! :satisfied:

```markdown
# Slide 1

foobar

---

# Slide 2

foobar



# **What is Linux?**

- A free and open-source operating system
- Built around the Linux kernel
- Used in servers, desktops, mobile devices, and embedded systems
- Popular distributions: Ubuntu, Fedora, Debian, Arch Linux

---

# **Why Use Linux?**

- Free and open-source
- Highly customizable
- More secure than many other OSes
- Efficient resource usage
- Preferred for servers and development environments

---

# **Linux Distributions**

- **Debian-based** → Ubuntu, Linux Mint
- **RPM-based** → Fedora, CentOS, RHEL
- **Arch-based** → Manjaro, EndeavourOS
- **Others** → Gentoo, Slackware

---

# **Basic Linux Commands**

- `ls` → List files and directories
- `cd <directory>` → Change directory
- `pwd` → Print current directory
- `mkdir <name>` → Create a new directory
- `rm <file>` → Remove a file
- `rmdir <directory>` → Remove an empty directory

---

# **File Operations**

- `cp <source> <destination>` → Copy files
- `mv <source> <destination>` → Move/rename files
- `cat <file>` → View file contents
- `nano <file>` → Edit a file
- `touch <file>` → Create a new file

---

# **User Management**

- `whoami` → Display current user
- `id` → Show user ID and group ID
- `adduser <username>` → Create a new user
- `passwd <username>` → Change password
- `su <user>` → Switch user
- `sudo <command>` → Run command as root

---

# **File Permissions**

- View permissions:
```sh
ls -l
```
- Change permissions:
```sh
chmod 755 file
```
- Change file owner:
```sh
chown user:group file
```

---

# **Process Management**

- `ps aux` → View running processes
- `top` / `htop` → Monitor system usage
- `kill <PID>` → Terminate a process
- `killall <name>` → Kill processes by name

---

# **Networking Commands**

- `ifconfig` / `ip addr` → Show network info
- `ping <host>` → Check connectivity
- `netstat -tulnp` → Show open ports
- `curl <url>` → Fetch data from a URL
- `scp <file> user@host:/path` → Secure copy files over SSH

---

# **Package Management**

- **Debian-based (Ubuntu, Debian):**
```sh
sudo apt update
sudo apt install <package>
```
- **Red Hat-based (Fedora, CentOS):**
```sh
sudo dnf install <package>
```
- **Arch Linux:**
```sh
sudo pacman -S <package>
```

---

# **System Monitoring**

- `df -h` → Check disk usage
- `du -sh <directory>` → Show size of a directory
- `free -m` → View memory usage
- `uptime` → Show system uptime
- `journalctl -xe` → View system logs

---

# **Linux Best Practices**

- Keep the system updated
- Use strong passwords and SSH keys
- Regularly check logs
- Limit sudo access
- Backup important data

---

# **Resources**

- [Linux Documentation](https://linux.die.net/)
- [The Linux Command Line](https://linuxcommand.org/)
- [Ubuntu Wiki](https://help.ubuntu.com/)
- [Arch Wiki](https://wiki.archlinux.org/)

---

# **Thank You!**

Happy Linux Exploration! 🐧
