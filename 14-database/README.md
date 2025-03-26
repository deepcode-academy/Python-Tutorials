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

- Ma’lumotlar bazasiga ulanish uchun sqlite3.connect() funksiyasidan foydalanamiz.

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
⏩ Agar "students.db" bazasi mavjud bo‘lmasa, yangi fayl hosil bo‘ladi.
