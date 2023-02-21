---
title: Identification
weight: 2
---
### Unusual Accounts

Look for any suspicious entry in `/etc/passwd`, especially with UID 0. Also check `/etc/group` and `/etc/shadow`.

Look for orphaned files, which could have been left by a deleted account used in the attack:

```shell-session
# find / \( -nouser -o -nogroup \) -print
```

### Unusual Files

- Look for all SUID and GUID files:

  ```shell-session
  # find / -uid 0 \( -perm -4000 -o -perm 2000 \) -print
  ```

- Look for weird file names, starting with `.` or `..` or ` ` :

  ```shell-session
  # find / -name " *" -print
  # find / -name ".*" -print
  # find / -name "..*" -print
  ```

- Look for large files (here: larger than 10MB)

  ```shell-session
  # find / -size +10MB -print
  ```

- Look for processes running from or to files which have been unlinked :

  ```shell-session
  # lsof +L1
  ```

- Look for unusual files in /proc and /tmp. This last directory is a place of choice for hackers to store data or malicious binaries.

### Unusual Services

(Linux only) Run chkconfig (if installed) to check for all enabled
services:

```shell-session
# chkconfig --list
```

Look at the running processes (remember: a rootkit might change your results for everything in this paper, especially here!).

```shell-session
# ps -aux
```

Use `lsof -p [pid]` on unknown processes

You should know your usual running processes, and be able to figure out which processes could have been added by a hacker. Pay a special attention to the processes running under UID 0.

### Unusual Network Activity

Try to detect sniffers on the network using several ways:

Look at your kernel log files for interfaces entering promiscuous mode such as: `kernel: device eth0 entered promiscuous mode`

Use `# ip link` to detect the `PROMISC` flag. Prefer this method
to ifconfig, since ifconfig does not work on all kernels.

- Look for unusual port activity: `# netstat -nap` and `# lsof -i` to get more information about processes listening to ports.

- Look for unusual MAC entries in your LAN:

  ```shell-session
  # arp -a
  ```

- Look for any unexpected IP address on the network.

### Unusual Automated Tasks

- Look for unusual jobs scheduled by users mentioned in `/etc/cron.allow`. Pay a special attention to the cron jobs scheduled by UID 0 accounts (root):

  ```shell-session
  # crontab -u root -l
  ```

- Look for unusual system-wide cron jobs: `# cat /etc/crontab` and `# ls -la /etc/cron.*`

### Unusual Log Entries

Look through the log files on the system for suspicious events,
including the following:

- Huge number of authentication/login failures from local or remote access tools (sshd,ftpd,etc.)
- Remote Procedure Call (RPC) programs with a log entry that includes a large number of strange characters ...)
- A huge number of Apache logs mentioning `error`
- Reboots (Hardware reboot)
- Restart of applications (Software reboot)

Almost all log files are located under `/var/log` directory in most Linux distributions. Here are the main ones:

- `/var/log/message`: General message and system related stuff
- `/var/log/auth.log`: Authenication logs
- `/var/log/kern.log`: Kernel logs
- `/var/log/cron.log`: Crond logs (cron job)
- `/var/log/maillog`: Mail server logs
- `/var/log/httpd/`: Apache access and error logs directory
- `/var/log/boot.log`: System boot log
- `/var/log/mysqld.log`: MySQL database server log file
- `/var/log/secure`: Authentication log
- `/var/log/utmp` or `/var/log/wtmp`: Login records file

To look through the log files, tools like cat and grep may be useful:

```shell-session
cat /var/log/httpd/access.log | grep "GET /signup.jsp"
```

### Unusual Kernel log Entries

- Look through the kernel log files on the system for suspicious events.

  Use :

  ```shell-session
  # dmesg
  ```

  List all important kernel and system information :

  ```shell-session
  # lsmod
  # lspci
  ```

- Look for known rootkit (use rkhunter and such tools)

### File hashes

Verify all MD5 hashes of your binaries in `/bin`, `/sbin`, `/usr/bin`, `/usr/sbin` or any other related binary storing place. (use *AIDE* or such tool)

**WARNING**: this operation will probably change all file timestamps. This should only be done after all other investigations are done and you feel like you can alter these data.

- On systems with RPM installed, use: `# rpm -Va | sort`
- On some Linux, a script named `check-packages` can be used.
- On Solaris: `# pkg_chk -vn`
- On Debian: `debsums -ac`
- On Openbsd (not really this but a way): `pkg_delete -vn
