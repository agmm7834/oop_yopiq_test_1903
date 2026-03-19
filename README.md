# 1. Python OOP nima va nima uchun ishlatiladi

## Masala 1

Foydalanuvchilarni boshqaruvchi tizim yozing.

`User` class yarating.

**Talablar:**

* `name` (string)
* `email` (string, unique bo‘lishi shart)
* class attribute: `users = []`

**Metodlar:**

* `__init__(name, email)`

  * agar email oldin mavjud bo‘lsa → `ValueError`
  * aks holda obyekt `users` ga qo‘shilsin
* `get_info()` → `"Name: Ali, Email: ali@mail.com"`
* `@classmethod find_user(email)` → user obyektini qaytarsin yoki `None`
* `delete_user(email)` → users dan o‘chirsin (topilmasa xato)

**Vazifa:**

* kamida 5 ta user yarating
* bitta userni toping
* bitta userni o‘chiring

---

## Masala 2

Ombor (inventory) tizimi yozing.

`Product` class:

**Atributlar:**

* `name`
* `price` (>0)
* `quantity` (>=0)

**Metodlar:**

* `total_price()` → price * quantity
* `sell(amount)`

  * agar amount > quantity → `ValueError`
  * aks holda quantity kamayadi
* `restock(amount)` → quantity oshadi

**Vazifa:**

* 4 ta mahsulot yarating
* eng katta total_price ga ega mahsulotni toping

---

## Masala 3

Bank tizimi yozing.

`BankAccount` class:

**Atributlar:**

* `owner`
* `__balance` (private)

**Metodlar:**

* `deposit(amount)` → amount > 0 bo‘lsin
* `withdraw(amount)` → balans yetarli bo‘lmasa `ValueError`
* `transfer(other_account, amount)`
* `get_balance()`

**Vazifa:**

* 2 ta account yarating
* pul o‘tkazing
* noto‘g‘ri holatda xatolik chiqishini tekshiring

---

# 2. Class tushunchasi

## Masala 1

`Rectangle` class yozing.

**Atributlar:**

* `width`
* `height`

**Shartlar:**

* width va height > 0 bo‘lsin (aks holda `ValueError`)

**Metodlar:**

* `area()`
* `perimeter()`
* `is_square()` → True/False

---

## Masala 2

`Circle` class yozing.

**Atribut:**

* `radius` (>0)

**Metodlar:**

* `area()`
* `circumference()`
* `compare(other_circle)` → katta radiusli obyektni qaytarsin

---

## Masala 3

`Student` class yozing.

**Atributlar:**

* `name`
* `grades` (list)

**Metodlar:**

* `add_grade(x)` (0–100 bo‘lsin, aks holda xato)
* `average()`
* `is_passed()` → average >= 60

---

# 3. Object bilan ishlash

## Masala 1

`Car` class yozing (`brand`, `speed`).

**Shart:**

* speed >= 0

**Vazifa:**

* 5 ta obyekt yarating
* eng tez mashinani toping (`max`)
* o‘rtacha tezlikni hisoblang

---

## Masala 2

`Student` obyektlari bilan ishlang.

**Vazifa:**

* 5 ta student yarating
* har biriga turli grades bering
* eng yuqori average toping
* faqat passed studentlarni alohida listga ajrating

---

## Masala 3

`Product` obyektlari bilan ishlang.

**Vazifa:**

* 5 ta product yarating
* `total_price()` bo‘yicha sort qiling
* eng katta qiymatli productni toping

---

# 4. Attribute (nazorat bilan)

## Masala 1

`Car` class yozing.

**Atribut:**

* `_speed` (protected)

**Metodlar:**

* `set_speed(value)`

  * 0 ≤ value ≤ 300
  * aks holda `ValueError`
* `get_speed()`

---

## Masala 2

`Product` class yozing.

**Atribut:**

* `_price`

**Metodlar:**

* `set_price(value)` → value > 0
* `get_price()`

---

## Masala 3

`User` class yozing.

**Atribut:**

* `email`

**Shart:**

* email ichida `"@"` bo‘lishi shart
* aks holda `ValueError`

---

# 5. Method (murakkab logika)

## Masala 1

`Calculator` class yozing.

**Metodlar:**

* `add(a, b)`
* `subtract(a, b)`
* `multiply(a, b)`
* `divide(a, b)` → b = 0 bo‘lsa `ZeroDivisionError`

---

## Masala 2

`TextProcessor` class yozing.

**Atribut:**

* `text`

**Metodlar:**

* `word_count()`
* `unique_words()` → set
* `most_common_word()` → eng ko‘p uchragan so‘z

---

## Masala 3

`Game` class yozing.

**Atributlar:**

* `score`
* `level`

**Metodlar:**

* `add_score(points)`
* har 100 ball oshganda level +1 bo‘lsin

---

# 6. **init** (default va tekshiruv)

## Masala 1

`Student` class:

**Atributlar:**

* `name`
* `grades=None`

**Shart:**

* agar None bo‘lsa → bo‘sh list yaratilsin

---

## Masala 2

`Car` class:

* `brand`
* `speed=0` default

---

## Masala 3

`Account` class:

* `balance` (>0 bo‘lsin)
* aks holda `ValueError`

---

# 7. Instance attribute

## Masala 1

`User` class:

* har obyekt uchun avtomatik `id` (1,2,3…)

---

## Masala 2

`Student`:

* har bir obyekt o‘z `grades` listiga ega bo‘lsin
* boshqa obyektga ta’sir qilmasin

---

## Masala 3

`Account`:

* har biri mustaqil balans bilan ishlasin

---

# 8. Class attribute

## Masala 1

`User`:

* `users_count`
* har yangi obyekt yaratilganda oshsin

---

## Masala 2

`Product`:

* `global_discount`
* `apply_discount()` da ishlatilsin

---

## Masala 3

`Game`:

* `max_level` (class attribute)
* level oshishi shu limitdan oshmasin

---

# 9. Instance vs Class attribute

## Masala 1

Classda:

* `x = 10`

Instance orqali:

* `x = 20`

Natijalarni solishtiring va tushuntiring

---

## Masala 2

Class atributni o‘zgartiring:

* barcha obyektga ta’sirini tekshiring

---

## Masala 3

Classda list saqlang:

* bir obyekt orqali o‘zgartirib, boshqalarga ta’sirini ko‘rsating

---

# 10. Encapsulation

## Masala 1

`BankAccount`:

* `__balance`
* tashqaridan o‘qib bo‘lmasin

---

## Masala 2

`User`:

* `__password`
* `check_password(p)` metod yozing

---

## Masala 3

Protected `_data` bilan class yozing va subclassda ishlating

---

# 11. Getter / Setter

## Masala 1

`Product`:

* property orqali `price` boshqaring
* price > 0

---

## Masala 2

`Student`:

* `grade` setter (0–100)

---

## Masala 3

Read-only property (`id`) yarating

---

# 12. Inheritance

## Masala 1

`Animal` → `Dog`

* `make_sound()` override

---

## Masala 2

`Vehicle` → `Car`

* `fuel_type` atribut qo‘shing
* `info()` metod yozing

---

## Masala 3

`User` → `Admin`

* `delete_user()` qo‘shing

---

# 13. super()

## Masala 1

Parent `__init__` ni `super()` bilan chaqiring

---

## Masala 2

Parent metodni override qilib ichida `super()` ishlating

---

## Masala 3

3 darajali inheritance qilib:

* har bosqichda `super()` ishlating

---

