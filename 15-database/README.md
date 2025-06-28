# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 15-DARS DATABASE

## ✅ MA'LUMOTLAR BAZASI VA PYTHON HAQIDA TUSHUNCHA

> [!NOTE]
> SQLite — bu kichik, mustaqil va yengil ma’lumotlar bazasi tizimi. U server talab qilmaydi, ya’ni barcha ma’lumotlar bitta faylda saqlanadi. Python `sqlite3` moduli orqali biz SQLite bilan to‘g‘ridan-to‘g‘ri ishlashimiz mumkin.

✅ SQLite AFZALLIKLARI: 

  - ✅ Kichik va tez ishlaydi
  - ✅ Server talab qilmaydi
  - ✅ Platformadan mustaqil
  - ✅ Python’da sqlite3 moduli bilan oson ishlaydi

## ✅ DATABASE BILAN ISHLASH BOSQICHLARI

📌 SQLite bilan ishlash uchun 5 asosiy bosqich mavjud:

- **Bazaga ulanish** – SQLite bazasiga ulanish yoki yangi fayl yaratish.
- **Jadval yaratish** – Ma’lumotlarni saqlash uchun jadval hosil qilish.
- **Ma’lumot qo‘shish** – Bazaga yangi malumotlar kiritish.
- **Ma’lumotlarni o‘qish** – Jadvaldagi ma’lumotlarni olish.
- **Ma’lumotlarni yangilash** va o‘chirish – Malumotlarni o‘zgartirish yoki o‘chirish.


## ✅ DATABASE BILAN ISHLASHNI BOSHLASH

### ✅ MA'LUMOTLAR BAZASIGA ULANISH

📌 Ma’lumotlar bazasiga ulanish uchun `sqlite3.connect()` funksiyasidan foydalanamiz.

```python
# sqlite3 modulini import qilamiz — SQLite ma'lumotlar bazasi bilan ishlash uchun kerak
import sqlite3

# students.db nomli SQLite ma'lumotlar bazasiga ulanamiz
# Agar bunday fayl bo‘lmasa, yangi ma'lumotlar bazasi yaratiladi
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz — bu orqali SQL buyruqlarini bajarish mumkin bo‘ladi
cur = conn.cursor()

# Bazaga muvaffaqiyatli ulanganimiz haqida xabar chiqaramiz
print("Ma’lumotlar bazasiga bog‘landik!")

# Ma'lumotlar bazasi bilan ish tugagach, ulanishni yopamiz
conn.close()
```

### ✅ JADVAL YARATISH

📌 Jadval yaratish uchun `CREATE TABLE` SQL buyrug‘idan foydalanamiz.

```python
# sqlite3 modulini import qilamiz — SQLite bilan ishlash uchun kerak
import sqlite3

# Bazaga ulanamiz ("students.db" fayl ko‘rinishida bo‘ladi)
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz — SQL buyruqlarini bajarish uchun kerak
cur = conn.cursor()

# Studentlar jadvalini yaratamiz agar mavjud bo‘lmasa
# Jadvalda quyidagi ustunlar bo‘ladi:
# id - unikal ID, avtomatik raqamlanadi
# name - talabaning ismi (string, bo‘sh bo‘lishi mumkin emas)
# age - talabaning yoshi (integer, bo‘sh bo‘lishi mumkin emas)
# grade - talabaning bahosi yoki kursi (string, bo‘sh bo‘lishi mumkin emas)
cur.execute("""
CREATE TABLE IF NOT EXISTS students (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    age INTEGER NOT NULL,
    grade TEXT NOT NULL
)
""")

# Jadval yaratildi degan xabarni chiqaramiz
print("Jadval yaratildi!")

# O‘zgartirishlarni saqlaymiz (commit qilamiz)
conn.commit()

# Bazaga ulanishni yopamiz
conn.close()
```


### ✅ MA'LUMOT QO'SHISH

📌 Ma’lumot qo‘shish uchun `INSERT INTO` buyrug‘idan foydalanamiz.

```python
# Bazaga ulanamiz
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz
cur = conn.cursor()

# students jadvaliga yangi talaba ma'lumotini qo‘shamiz
# SQL so‘rovda parametrlar o‘rnida ? ishlatiladi, bu xavfsizroq va SQL injection xavfini kamaytiradi
# ("Ali", 20, "A") — bu parametrlar name, age va grade ustunlariga mos keladi
cur.execute("INSERT INTO students (name, age, grade) VALUES (?, ?, ?)", ("Ali", 20, "A"))

# Ma'lumot qo‘shilgani haqida xabar chiqaramiz
print("Ma’lumot qo‘shildi!")

# O‘zgarishlarni saqlaymiz
conn.commit()

# Bazaga ulanishni yopamiz
conn.close()
```

📌 Agar bir nechta ma’lumot qo‘shmoqchi bo‘lsak:

```python
# Bazaga ulanamiz
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz
cur = conn.cursor()

# Bir nechta talaba ma'lumotlarini ro'yxat shaklida tayyorlaymiz
students = [
    ("Vali", 19, "B"),
    ("Hasan", 21, "A"),
    ("Shahnoza", 20, "C")
]

# Ro'yxatdagi barcha ma'lumotlarni jadvalga bir vaqtning o'zida qo'shamiz
cur.executemany("INSERT INTO students (name, age, grade) VALUES (?, ?, ?)", students)

# Ma'lumotlar qo'shilganini bildiruvchi xabar chiqaramiz
print("Bir nechta yozuv qo‘shildi!")

# O'zgarishlarni saqlaymiz
conn.commit()

# Bazaga ulanishni yopamiz
conn.close()
```

### ✅ MA'LUMOTLARNI O'QISH

📌 Jadvaldagi barcha ma’lumotlarni olish uchun `SELECT` buyrug‘idan foydalanamiz.

```python
# Bazaga ulanamiz
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz
cur = conn.cursor()

# students jadvalidan barcha ustunlarni tanlab olamiz
cur.execute("SELECT * FROM students")  # "SELECT *" — jadvaldagi barcha ustunlar va qatorlar

# Barcha natijalarni list ko‘rinishida olamiz
students = cur.fetchall()

# Har bir talaba ma'lumotini alohida chiqaramiz
for student in students:
    print(student)

# Bazaga ulanishni yopamiz
conn.close()
```

📌 Agar faqat bitta ma’lumot olish kerak bo‘lsa:

```python
# students jadvalidan name ustuni "Ali" ga teng bo‘lgan birinchi qatorni tanlab olish
cur.execute("SELECT * FROM students WHERE name = ?", ("Ali",))

# Natijadan faqat bitta qatorni olish (birinchi topilgan)
student = cur.fetchone()

# Topilgan yozuvni konsolga chiqarish
print(student)
```

### ✅ MA'LUMOTLARNI YANGILASH

📌 Ma’lumotlarni o‘zgartirish uchun `UPDATE` buyrug‘idan foydalanamiz.

```python
# Bazaga ulanamiz
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz
cur = conn.cursor()

# students jadvalidagi name ustuni "Ali" bo‘lgan qatorni age ustunini 21 ga o‘zgartiramiz
cur.execute("UPDATE students SET age = ? WHERE name = ?", (21, "Ali"))

# Yangilanganini bildiruvchi xabar chiqaramiz
print("Ma’lumot yangilandi!")

# O‘zgarishlarni saqlaymiz
conn.commit()

# Bazaga ulanishni yopamiz
conn.close()
```

### ✅ MA'LUMOTLARNI O'CHIRISH

📌 Ma’lumotlarni o‘chirish uchun `DELETE FROM` buyrug‘idan foydalanamiz.

```python
# Bazaga ulanamiz
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz
cur = conn.cursor()

# students jadvalidan name ustuni "Ali" bo‘lgan qatorni o‘chiramiz
cur.execute("DELETE FROM students WHERE name = ?", ("Ali",))

# O‘chirildi degan xabarni chiqaramiz
print("Ma’lumot o‘chirildi!")

# O‘zgarishlarni saqlaymiz
conn.commit()

# Bazaga ulanishni yopamiz
conn.close()
```

## ✅ XATOLIKLARNI USHLASH

📌 Ma’lumotlar bazasi bilan ishlaganda xatoliklarni ushlash muhim.

```python
# try-except-finally blokida kod yozamiz — xatolik yuz berganda uni ushlab, boshqarish uchun
try:
    # Bazaga ulanamiz
    conn = sqlite3.connect("students.db")
    # Cursor obyekti yaratamiz
    cur = conn.cursor()

    # students jadvalidan barcha ustunlar va qatorlarni olamiz
    cur.execute("SELECT * FROM students")
    # Natijalarni list sifatida saqlaymiz
    students = cur.fetchall()

    # Har bir ma'lumotni ekranga chiqaramiz
    for student in students:
        print(student)

# Agar sqlite3 bilan bog‘liq xatolik yuz bersa, uni ushlaymiz va xabar chiqaramiz
except sqlite3.Error as e:
    print("Xatolik yuz berdi:", e)

# Nihoyat, kod tugagach (xato bo‘lsa ham yoki bo‘lmasa ham) bazaga ulanishni yopamiz
finally:
    conn.close()
```

# ✅ AMALIYOT

## ✅ 1-topshiriq:
`"library.db"` nomli SQLite bazasini yarating. `"books"` nomli jadval yarating (`id`, `title`, `author`, `year`).  
- `id INTEGER PRIMARY KEY AUTOINCREMENT`
- `title`, `author`, `year` NOT NULL

---

## ✅ 2-topshiriq:
`"books"` jadvaliga quyidagi ma’lumotlarni kiriting (`executemany()` funksiyasidan foydalaning):
| id  | title              | author        | year  |
|-----|--------------------|---------------|-------|
| 1   | Python Basics      | John Smith    | 2020  |
| 2   | SQL for Beginners  | Alice Brown   | 2018  |
| 3   | Data Science Guide | Michael Clark | 2021  |

---

## ✅ 3-topshiriq:
`"books"` jadvalidagi barcha kitoblarni ekranga chiqaring. Natija `id`, `title`, `author`, `year` formatida bo‘lsin.

---

## ✅ 4-topshiriq:
Foydalanuvchidan **muallif nomini** so‘rang. Shu muallif tomonidan yozilgan barcha kitoblarni chiqaring.
Agar kitob topilmasa, `"Bu muallifning kitoblari yo'q"` deb chiqaring.

---

## ✅ 5-topshiriq:
`"SQL for Beginners"` kitobining chiqish yilini `2019` ga o‘zgartiring. Yangilangan ma’lumotni ekranga chiqaring.

---

## ✅ 6-topshiriq:
`"books"` jadvalidan chiqish yili eng kichik bo‘lgan kitobni toping (eng eski kitob).

---

## ✅ 7-topshiriq:
`"books"` jadvalidan `2020` yildan keyin chiqqan kitoblarni chiqarish kodini yozing.

---

## ✅ 8-topshiriq:
`"Data Science Guide"` kitobini `"books"` jadvalidan o‘chiring. O‘chirilganidan keyin jadvaldagi barcha kitoblarni ekranga chiqaring.

---

## ✅ 9-topshiriq:
`"university.db"` bazasini yarating va `"students"` jadvalini yarating:
- `id INTEGER PRIMARY KEY AUTOINCREMENT`
- `name TEXT NOT NULL`
- `age INTEGER NOT NULL`
- `faculty TEXT NOT NULL`

---

## ✅ 10-topshiriq:
`"students"` jadvaliga kamida 5 ta talaba haqida ma’lumot kiriting.

---

## ✅ 11-topshiriq:
Foydalanuvchidan fakultet nomini so‘rang va shu fakultetdagi talabalarni chiqaring.

---

## ✅ 12-topshiriq:
`"students"` jadvalidan eng yosh talabani toping.

---

## ✅ 13-topshiriq:
`"name"` ismli talabaning yoshini `21` ga o‘zgartiring.

---

## ✅ 14-topshiriq:
`"students"` jadvalidagi har bir fakultet bo‘yicha nechta talaba borligini hisoblang.

---

## ✅ 15-topshiriq:
`"students"` jadvalidan eng ko‘p talabaga ega bo‘lgan fakultetni aniqlang.
