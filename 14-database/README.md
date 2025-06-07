# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 14-DARS MA'LUMOTLAR BAZASI (SQLite)

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
# id - unikal identifikator, avtomatik raqamlanadi
# name - talabaning ismi (matn, bo‘sh bo‘lishi mumkin emas)
# age - talabaning yoshi (butun son, bo‘sh bo‘lishi mumkin emas)
# grade - talabaning bahosi yoki kursi (matn, bo‘sh bo‘lishi mumkin emas)
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

# Bir nechta talaba yozuvlarini ro'yxat shaklida tayyorlaymiz
students = [
    ("Vali", 19, "B"),
    ("Hasan", 21, "A"),
    ("Shahnoza", 20, "C")
]

# Ro'yxatdagi barcha yozuvlarni jadvalga bir vaqtning o'zida qo'shamiz
cur.executemany("INSERT INTO students (name, age, grade) VALUES (?, ?, ?)", students)

# Yozuvlar qo'shilganini bildiruvchi xabar chiqaramiz
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

# students jadvalidan barcha yozuvlarni tanlab olamiz
cur.execute("SELECT * FROM students")  # "SELECT *" — jadvaldagi barcha ustunlar va yozuvlar

# Barcha natijalarni list ko‘rinishida olamiz
students = cur.fetchall()

# Har bir talaba yozuvini alohida chiqaramiz
for student in students:
    print(student)

# Bazaga ulanishni yopamiz
conn.close()
```

- Agar faqat bitta ma’lumot olish kerak bo‘lsa:

```python
cur.execute("SELECT * FROM students WHERE name = ?", ("Ali",))
student = cur.fetchone()
print(student)
```

**Natija:**

```shell
(1, 'Ali', 20, 'A')
```

### Ma’lumotlarni yangilash

- Ma’lumotlarni o‘zgartirish uchun `UPDATE` buyrug‘idan foydalanamiz.

```python
conn = sqlite3.connect("students.db")
cur = conn.cursor()

# Ali’ning yoshini 21 ga o‘zgartiramiz
cur.execute("UPDATE students SET age = ? WHERE name = ?", (21, "Ali"))

print("Ma’lumot yangilandi!")

conn.commit()
conn.close()
```

### Ma’lumotlarni o‘chirish

- Ma’lumotlarni o‘chirish uchun `DELETE FROM` buyrug‘idan foydalanamiz.

```python
conn = sqlite3.connect("students.db")
cur = conn.cursor()

# "Ali" ismli talabani o‘chiramiz
cur.execute("DELETE FROM students WHERE name = ?", ("Ali",))

print("Ma’lumot o‘chirildi!")

conn.commit()
conn.close()
```

## Xatoliklarni ushlash

- Ma’lumotlar bazasi bilan ishlaganda xatoliklarni ushlash muhim.

```python
try:
    conn = sqlite3.connect("students.db")
    cur = conn.cursor()

    cur.execute("SELECT * FROM students")
    students = cur.fetchall()

    for student in students:
        print(student)

except sqlite3.Error as e:
    print("Xatolik yuz berdi:", e)

finally:
    conn.close()
```

# PRACTICS

1. Yangi jadval yaratish
   - `"library.db"` nomli SQLite bazasini yarating.
   - `"books"` nomli jadval yarating (`id`, `title`, `author`, `year`).
   - PK: `id INTEGER PRIMARY KEY AUTOINCREMENT.`
   - NOT NULL: `title`, `author`, `year`.

2. Kitoblar ma’lumotlarini kiritish
   - `"books"` jadvaliga quyidagi ma’lumotlarni kiriting:
   - `executemany()` funksiyasidan foydalaning.

| id  | title              | author        | year  |
|-----|--------------------|---------------|-------|
| 1   | Python Basics      | John Smith    | 2020  |
| 2   | SQL for Beginners  | Alice Brown   | 2018  |
| 3   | Data Science Guide | Michael Clark | 2021  |

3. Barcha kitoblarni chiqarish
    - `"books"` jadvalidagi barcha kitoblarni ekranga chiqaring.
    - Natija `id`, `title`, `author`, `year` formatida bo‘lsin.

4. Muallif bo‘yicha qidirish
    - Foydalanuvchidan **muallif nomini** so‘rang.
    - Shu muallif tomonidan yozilgan barcha kitoblarni chiqaring.
    - Agar kitob topilmasa, `"Bu muallifning kitoblari yo'q"` deb chiqaring.

5. Kitob yilini yangilash
   - `"SQL for Beginners"` kitobining chiqish yilini `2019` ga o‘zgartiring.
   - Yangilangan ma’lumotni ekranga chiqaring.

6. Eng eski kitobni topish
    - `"books"` jadvalidan chiqish yili eng kichik bo‘lgan kitobni toping.

7. 2020-yildan keyin chiqqan kitoblarni chiqarish
   - `"books"` jadvalidan `2020` yildan keyin chiqqan kitoblarni chiqarish kodini yozing.

8. Kitobni o‘chirish
   - `"Data Science Guide"` kitobini `"books"` jadvalidan o‘chiring.
   - O‘chirilganidan keyin jadvaldagi barcha kitoblarni ekranga chiqaring.

9. Talabalar jadvallarini yaratish
   - `"university.db"` bazasini yarating.
   - `"students"` jadvalini yarating:
   - `id INTEGER PRIMARY KEY AUTOINCREMENT`,
   - `name TEXT NOT NULL`,
   - `age INTEGER NOT NULL`,
   - `faculty TEXT NOT NULL`.

10. Talabalar jadvaliga ma’lumot qo‘shish
    - `"students"` jadvaliga kamida 5 ta talaba haqida ma’lumot kiriting.

11. Fakultet bo‘yicha qidirish
    - Foydalanuvchidan fakultet nomini so‘rang.
    - Shu fakultetdagi talabalarni chiqaring.

12. Eng yosh talabani topish
    - `"students"` jadvalidan eng yosh talabani toping.

13. Talabaning yoshini yangilash
    - `"name"` ismli talabaning yoshini `21` ga o‘zgartiring.

14. Fakultet bo‘yicha talabalarni sanash
    - `"students"` jadvalidagi har bir fakultet bo‘yicha nechta talaba borligini hisoblang.

15. Eng ko‘p talabaga ega fakultetni topish
    - `"students"` jadvalidan eng ko‘p talabaga ega bo‘lgan fakultetni aniqlang.