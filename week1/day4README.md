# 📊 SQL NULL HANDLING

---

## ⚡ CONCEPT

```sql
IFNULL(col, value) → replace NULL

COALESCE(a, b, c) → first non-null

NULLIF(a, b) → NULL if equal

IS NULL / IS NOT NULL → filtering
```

---

## 🧪 PRACTICE

### 🟢 LEVEL 1

```sql
salary IS NULL

discount IS NOT NULL

category IS NULL

COUNT(manager_id)
```

---

### 🟡 LEVEL 2 (IFNULL)

```sql
IFNULL(salary, 0)

IFNULL(bonus, 1000)

IFNULL(amount, 500)

IFNULL(stock, 0)
```

---

### 🔵 LEVEL 3 (COALESCE)

```sql
COALESCE(salary, bonus)

COALESCE(salary, bonus, 0)

COALESCE(price, 1000)

COALESCE(amount, discount, 0)
```

---

### 🟣 LEVEL 4 (NULLIF)

```sql
NULLIF(salary, 0)

NULLIF(discount, 0)

amount / NULLIF(discount, 0)

NULLIF(coupon_code, 'DISC10')
```

---

### 🔴 LEVEL 5

```sql
salary + bonus

salary IS NULL AND bonus IS NULL

price IS NULL AND category IS NOT NULL

amount IS NULL AND discount IS NULL
```

---

### ⚫ LEVEL 6

```sql
COALESCE(salary, bonus, 1000)

NULLIF(discount, 0)

amount - discount

salary IS NULL AND manager_id IS NOT NULL
```

---

## 🚀 NOTES

* Use **COALESCE** (best practice)
* IFNULL → simple replace
* NULLIF → cleaning (0 → NULL)
* NULL ≠ 0

---
