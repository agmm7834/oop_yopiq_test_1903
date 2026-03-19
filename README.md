# 1. Python OOP nima va nima uchun ishlatiladi

## Masala 1

Siz foydalanuvchilarni boshqaruvchi tizim yaratyapsiz.

`User` nomli class yarating.

**Talablar:**

* Atributlar:

  * `name` (string)
  * `email` (string, unique bo‘lishi kerak)
* Class attribute:

  * `users` — barcha yaratilgan obyektlar ro‘yxati

**Metodlar:**

* `__init__()`:

  * yangi user yaratilganda uni `users` ro‘yxatiga qo‘shsin
  * agar email takror bo‘lsa, obyekt yaratilmasin
* `get_info()` → `"Name: Ali, Email: ali@mail.com"`
* `@classmethod find_user(email)` → userni qaytarsin
* `delete_user(email)` → users ro‘yxatidan o‘chirsin

---

## Masala 2

`Product` class orqali kichik ombor tizimi yarating.

**Atributlar:**

* `name`
* `price` (>0 bo‘lishi kerak)
* `quantity` (>=0)

**Metodlar:**

* `total_price()` → umumiy qiymat
* `apply_discount(percent)` → narxni kamaytiradi
* `sell(amount)` → quantity kamayadi (yetarli bo‘lmasa xato)

**Vazifa:**

* 5 ta product yarating
* umumiy qiymati eng katta mahsulotni toping

---

## Masala 3

Bank tizimi yozing.

`BankAccount` class:

**Atributlar:**

* `owner`
* `__balance` (private)

**Metodlar:**

* `deposit(amount)` (amount > 0)
* `withdraw(amount)` (balance yetarli bo‘lsa)
* `transfer(other_account, amount)`
* `get_balance()`

**Qo‘shimcha:**

* noto‘g‘ri operatsiyada xatolik chiqsin

---

## Masala 4

`Employee` class orqali kompaniya tizimi yarating.

**Atributlar:**

* `name`
* `salary`
* `department`

**Metodlar:**

* `increase_salary(percent)`
* `compare_salary(other)`

**Vazifa:**

* 6 ta employee yarating
* har bir department bo‘yicha eng katta salaryni toping

---

## Masala 5

Kutubxona tizimi yozing.

`Library` class:

**Atribut:**

* `books = {nom: soni}`

**Metodlar:**

* `add_book(name, count)`
* `borrow_book(name)` (agar mavjud bo‘lsa kamaytiradi)
* `return_book(name)` (oshiradi)

**Vazifa:**

* eng ko‘p olingan kitobni aniqlang

---

# 2. Class tushunchasi

## Masala 1

`Rectangle` class yozing.

**Atributlar:**

* `width`
* `height`

**Metodlar:**

* `area()`
* `perimeter()`
* `is_square()`

**Qo‘shimcha:**

* width yoki height manfiy bo‘lsa xatolik chiqsin

---

## Masala 2

`Circle` class yozing.

**Atribut:**

* `radius`

**Metodlar:**

* `area()`
* `circumference()`
* `compare(other_circle)` → katta radiusni aniqlaydi

---

## Masala 3

`Student` class yozing.

**Atributlar:**

* `name`
* `grades` (list)

**Metodlar:**

* `average()`
* `max_grade()`
* `is_passed()` (avg >= 60)

---

## Masala 4

`Car` class yozing.

**Atributlar:**

* `brand`
* `speed` (>=0)

**Metodlar:**

* `accelerate(value)`
* `brake(value)`
* `is_speeding(limit)`

---

## Masala 5

`Book` class yozing.

**Atributlar:**

* `title`
* `pages`
* `read_pages`

**Metodlar:**

* `read(n)` → o‘qilgan sahifani oshiradi
* `progress()` → foizda qaytaradi

---

# 3. Object (obyekt) bilan ishlash

## Masala 1

`User` obyektlari ro‘yxatini yarating (kamida 5 ta).

**Vazifa:**

* eng uzun ismli userni toping
* email bo‘yicha sort qiling

---

## Masala 2

`Car` obyektlari bilan ishlang.

**Vazifa:**

* eng tez mashinani toping
* o‘rtacha tezlikni hisoblang

---

## Masala 3

`Product` obyektlari bilan ishlang.

**Vazifa:**

* total_price eng katta productni toping
* narx bo‘yicha sort qiling

---

## Masala 4

`Student` obyektlari bilan ishlang.

**Vazifa:**

* eng yuqori average toping
* faqat passed talabalarni ajrating

---

## Masala 5

`BankAccount` obyektlari bilan ishlang.

**Vazifa:**

* eng katta balans
* eng ko‘p pul o‘tkazgan user

---

# 4. Attribute (murakkab ishlash)

## Masala 1

`Car` classda `speed` uchun setter yozing:

* speed manfiy bo‘lmasin
* juda katta bo‘lsa (300 dan yuqori) xatolik

---

## Masala 2

`Student` classda `grades`:

* faqat 0–100 oralig‘ida qo‘shilsin
* noto‘g‘ri qiymat bo‘lsa xato

---

## Masala 3

`Product`:

* `price` manfiy bo‘lmasin
* setter orqali nazorat

---

## Masala 4

`User`:

* email formatini tekshiring (`@` bo‘lishi shart)

---

## Masala 5

`BankAccount`:

* balansni tashqaridan o‘zgartirib bo‘lmasin

---

# 5. Method (logik masalalar)

## Masala 1

`Calculator`:

* add, subtract, multiply, divide
* divide da 0 bo‘lsa exception

---

## Masala 2

`Math`:

* factorial(n)
* fibonacci(n)

---

## Masala 3

`TextProcessor`:

* word_count()
* unique_words()
* most_common_word()

---

## Masala 4

`Shop`:

* cart (list)
* add_product(product)
* remove_product(product)
* total_price()

---

## Masala 5

`Game`:

* score
* add_score(points)
* level_up() (har 100 ballda level oshsin)

---

