# OS Command Injection

## Definition

Allows attackers to execute operating system commands.

Also known as:
- Shell Injection

---

# Example

Application executes:

```bash
stockreport.pl 381 29
```

Attack:

```bash
& echo test &
```

Result:

```bash
stockreport.pl & echo test & 29
```

---

# Command Separators

```bash
&
;
|
```

---

# Useful Commands

## Linux

```bash
whoami
uname -a
ifconfig
netstat -an
ps -ef
```

## Windows

```bash
whoami
ver
ipconfig /all
tasklist
```

---

# Impact

- Execute commands
- Read files
- Full server compromise
- Internal pivoting
