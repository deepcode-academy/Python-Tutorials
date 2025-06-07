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

## SQLite bilan ishlash bosqichlari

- SQLite bilan ishlash uchun 5 asosiy bosqich mavjud:
  - **Bazaga ulanish** – SQLite bazasiga ulanish yoki yangi fayl yaratish.
  - **Jadval yaratish** – Ma’lumotlarni saqlash uchun jadval hosil qilish.
  - **Ma’lumot qo‘shish** – Bazaga yangi malumotlar kiritish.
  - **Ma’lumotlarni o‘qish** – Jadvaldagi ma’lumotlarni olish.
  - **Ma’lumotlarni yangilash** va o‘chirish – Malumotlarni o‘zgartirish yoki o‘chirish.


## SQLite bilan ishlashni boshlash

### Ma’lumotlar bazasiga ulanish

- Ma’lumotlar bazasiga ulanish uchun `sqlite3.connect()` funksiyasidan foydalanamiz.

```python
import sqlite3

# students.db nomli ma’lumotlar bazasiga ulanamiz
conn = sqlite3.connect("students.db")

# Cursor obyekti yaratamiz
cur = conn.cursor()

print("Ma’lumotlar bazasiga bog‘landik!")

# Ulashni yopamiz
conn.close()
```

**Result:**

```markdown
Ma’lumotlar bazasiga bog‘landik!
```
⏩ Agar `"students.db"` bazasi mavjud bo‘lmasa, yangi fayl hosil bo‘ladi.

### Jadval yaratish

- Jadval yaratish uchun `CREATE TABLE` SQL buyrug‘idan foydalanamiz.

```python
import sqlite3

# Bazaga ulanish
conn = sqlite3.connect("students.db")
cur = conn.cursor()

# Studentlar jadvalini yaratamiz
cur.execute("""
CREATE TABLE IF NOT EXISTS students (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    age INTEGER NOT NULL,
    grade TEXT NOT NULL
)
""")

print("Jadval yaratildi!")

# O‘zgarishlarni saqlaymiz va ulanishni yopamiz
conn.commit()
conn.close()
```

- `id INTEGER PRIMARY KEY AUTOINCREMENT` – har bir yozuv uchun unikal ID yaratiladi.
- `name TEXT NOT NULL` – talabalar ismi matn ko‘rinishida bo‘ladi.
- `age INTEGER NOT NULL` – yosh raqam ko‘rinishida bo‘ladi.
- `grade TEXT NOT NULL` – baho matn sifatida saqlanadi.

### Ma’lumot qo‘shish

- Ma’lumot qo‘shish uchun `INSERT INTO` buyrug‘idan foydalanamiz.

```python
conn = sqlite3.connect("students.db")
cur = conn.cursor()

# Bitta talaba qo‘shamiz
cur.execute("INSERT INTO students (name, age, grade) VALUES (?, ?, ?)", ("Ali", 20, "A"))

print("Ma’lumot qo‘shildi!")

conn.commit()
conn.close()
```

- Agar bir nechta ma’lumot qo‘shmoqchi bo‘lsak:

```python
conn = sqlite3.connect("students.db")
cur = conn.cursor()

# Bir nechta yozuv qo‘shish
students = [
    ("Vali", 19, "B"),
    ("Hasan", 21, "A"),
    ("Shahnoza", 20, "C")
]

cur.executemany("INSERT INTO students (name, age, grade) VALUES (?, ?, ?)", students)

print("Bir nechta yozuv qo‘shildi!")

conn.commit()
conn.close()
```

### Ma’lumotlarni o‘qish

- Jadvaldagi barcha ma’lumotlarni olish uchun `SELECT` buyrug‘idan foydalanamiz.

```python
conn = sqlite3.connect("students.db")
cur = conn.cursor()

cur.execute("SELECT * FROM students")  # Barcha yozuvlarni olish
students = cur.fetchall()  # Ma’lumotlarni list ko‘rinishida olish

for student in students:
    print(student)

conn.close()
```

**⏩ Natija:**

```shell
(1, 'Ali', 20, 'A')
(2, 'Vali', 19, 'B')
(3, 'Hasan', 21, 'A')
(4, 'Shahnoza', 20, 'C')
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