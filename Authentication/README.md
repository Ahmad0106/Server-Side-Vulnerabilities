# Authentication Vulnerabilities

## Authentication vs Authorization

Authentication:
Verify user identity.

Authorization:
Verify what the user can do.

---

# Common Vulnerabilities

- Username Enumeration
- Brute-force
- 2FA Bypass

---

# Username Enumeration

Different responses reveal valid usernames.

Examples:
- Invalid username
- Incorrect password

---

# Brute-force

Attackers try many credentials automatically.

Common tools:
- Hydra
- Burp Intruder

---

# Common Password Patterns

```text
Mypassword1!
Mypassword2!
Mypassword1?
```

Users often make predictable changes.

---

# Brute-force Usernames

Common usernames:
- admin
- administrator

Emails are also predictable:
- firstname.lastname@company.com

---

# 2FA Bypass

Sometimes users become logged in before entering the verification code.

Try accessing:

```bash
/my-account
/dashboard
```

After step 1 login.

---

# Notes

Weak authentication often leads to account takeover.
