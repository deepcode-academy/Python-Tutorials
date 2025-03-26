# SQLite

## SQLite va Python haqida tushuncha

> [!NOTE]
> SQLite — bu kichik, mustaqil va yengil ma’lumotlar bazasi tizimi. U server talab qilmaydi, ya’ni barcha ma’lumotlar bitta faylda saqlanadi. Python sqlite3 moduli orqali biz SQLite bilan to‘g‘ridan-to‘g‘ri ishlashimiz mumkin.

- SQLite’ning afzalliklari: 
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

## Ma’lumotlarni o‘qish

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