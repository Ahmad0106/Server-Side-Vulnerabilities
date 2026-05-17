# Access Control

## Definition

Access control determines whether a user is allowed to perform actions or access resources.

Depends on:
- Authentication
- Session management

---

# Types

## Vertical Privilege Escalation

Normal user accesses admin functionality.

Example:

```bash
/admin
```

---

## Horizontal Privilege Escalation

Access another user's data.

Example:

```bash
/myaccount?id=123
```

Change to:

```bash
/myaccount?id=456
```

---

## Horizontal to Vertical

Compromise an admin account using IDOR.

---

# Common Vulnerabilities

- Unprotected functionality
- Security by obscurity
- Parameter-based access control
- IDOR

---

# Security By Obscurity

Example:

```bash
/administrator-panel-yb556
```

Hidden URLs are not secure.

---

# Parameter-Based Access Control

Examples:

```bash
admin=true
role=1
```

If controllable by users → vulnerable.

---

# Notes

Always test:
- Hidden endpoints
- JavaScript files
- Cookies
- Parameters
