# SSRF

## Definition

Server-Side Request Forgery allows attackers to force the server to make requests.

---

# SSRF Against Localhost

Payloads:

```bash
http://127.0.0.1/admin
http://localhost/admin
```

Applications may trust localhost requests.

---

# SSRF Against Internal Systems

Payload:

```bash
http://192.168.0.68/admin
```

Internal systems often:
- Have weaker security
- Trust internal traffic
- Expose admin functionality

---

# Why SSRF Is Dangerous

- Access internal services
- Bypass access control
- Read sensitive data
- Reach private systems

---

# Common Features To Test

- Stock checkers
- PDF generators
- Webhooks
- URL import
- Image fetchers

---

# Notes

SSRF can sometimes lead to:
- RCE
- Internal network pivoting
- Cloud compromise
