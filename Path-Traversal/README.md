# Path Traversal

## Definition

Path traversal allows attackers to access files outside the intended directory.

---

# Common Payloads

```bash
../../../etc/passwd
..\\..\\..\\windows\\win.ini
```

---

# Impact

- Read sensitive files
- Read credentials
- Access application source code
