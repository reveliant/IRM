---
title: Identification
weight: 2
---
Please note that the **Sysinternals** Troubleshooting Utilities can be used to perform most of these tasks.

### Unusual Accounts

Look for unusual accounts created, especially in the Administrators group:

`C:\> lusrmgr.msc`

or

`C:\> net localgroup administrators` or `net localgroup administrateurs`

### Unusual Files

- Look for unusually big files on the storage support, bigger than 5MB. (can be an indication of a system compromised for illegal content storage)
- Look for unusual files added recently in system folders,
especially C:\WINDOWS\system32.
- Look for files using the “hidden” attribute: `C:\> dir /S /A:H`
- Use `windirstat` if possible.

### Unusual Registry Entries

Look for unusual programs launched at boot time in the Windows registry, especially:

```regitry
HKLM\Software\Microsoft\Windows\CurrentVersion\Run
HKLM\Software\Microsoft\Windows\CurrentVersion\Runonce
HKLM\Software\Microsoft\Windows\CurrentVersion\RunonceEx
```

Use `HiJackThis` if possible. (Also have a look in your Startup folder)

### Unusual Processes and Services

Check all running processes for unusual/unknown entries, especially processes with username “SYSTEM” and “ADMINISTRATOR”:

```console
C:\> taskmgr.exe
```

(or `tlisk`, `tasklist` depending on Windows release)

Use `psexplorer` if possible.

### Check user’s autostart folders

- `C:\Documents and Settings\user\Start Menu\Programs\Startup`
- `C:\WinNT\Profiles\user\Start Menu\Programs\Startup`

- Look for unusual/unexpected network services installed and started

  ```console
  C:\> services.msc
  C:\> net start
  ```

### Unusual Network Activity

- Check for file shares and verify each one is linked to a normal activity:

  ```console
  C:\> net view \\127.0.0.1
  ```

  Use `tcpview` if possible.

- Look at the opened sessions on the machine:

  ```console
  C:\> net session
  ```

- Have a look at the sessions the machine has opened with other systems:

  ```console
  C:\> net use
  ```

- Check for any suspicious Netbios connexion:

  ```console
  C:\> nbtstat –S
  ```

- Look for any suspicious activity on the system’s ports :

  ```console
  C:\> netstat –na 5
  ```

  (5 makes it being refreshed each 5 seconds)

  Use `–o` flag for Windows XP/2003 to see the owner of each process:

  ```console
  C:\> netstat –nao 5
  ```

  Use `fport` if possible.

### Unusual Automated Tasks

Look at the list of scheduled tasks for any unusual entry:

```console
C:\> at
```

On Windows 2003/XP:

```console
C:\> schtasks
```

### Unusual Log Entries

Watch your log files for unusual entries:

```console
C:\> eventvwr.msc
```

If possible, use *Event Log Viewer* or such tool

Search for events affecting the firewall, the antivirus, the file protection, or any suspicious new service.

Look for a huge amount of failed login attempts or locked out accounts.

Watch your firewall (if any) log files for suspect activity.

### Rootkit check

Run *Rootkit Revealer*, *Rootkit Hooker*, *Ice Sword*, *Rk Detector*, *SysInspector*, *Rootkit Buster*.

It’s always better to run several of these tools than only one.

### Malware check

Run at least one anti-virus product on the whole disk. If possible use several anti-virus. The anti-virus must absolutely be up-to-date.
