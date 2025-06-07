# PYTHON DASTURLASH ASOSLARI

# 🧩 13-DARS FAYLLAR

📌 Fayl — bu kompyuterda ma'lumotlar saqlanadigan obyekt. U matn, rasm, ovoz yoki dasturiy kod bo‘lishi mumkin. Biz dasturda aynan matnli fayllar bilan ko‘p ishlaymiz, masalan: .txt, .csv, .json fayllar.

## ❓ FAYL NIMA UCHUN KERAK?

📝 Ma'lumotlarni saqlash — Dastur tugagandan keyin ham ma'lumot yo‘qolmasligi uchun.

🔁 Qayta ishlash — Avval yozilgan ma'lumotlarni o‘qib, tahlil qilish yoki o‘zgartirish.

📤 Boshqa dasturlar bilan almashish — Fayllar orqali boshqa dasturlar bilan axborot almashiladi.

📚 Katta hajmdagi ma'lumotlar — Ma'lumot bazasidan oldin oddiy fayllarda saqlanadi (masalan, .csv fayllar).

## ✅ FAYLNI OCHISH

📌 Faylni ochish uchun `open()` funksiyasidan foydalaniladi. Bu funksiya fayl nomini va rejimini qabul qiladi. `open()` funksiyasida ikkinchi parametr sifatida fayl rejimini ko'rsatishingiz mumkin:

## ✅ FAYL REJIMLARI

- `r` – Faylni o'qish uchun ochish. Fayl mavjud bo'lishi kerak.
- `w` – Faylga yozish uchun ochish. Agar fayl mavjud bo'lmasa, yangi fayl yaratadi. Mavjud fayl bo'lsa, ma'lumotlarni o'chirib yuboradi.
- `a` – Faylga qo'shish uchun ochish. Mavjud faylga yangi ma'lumot qo'shadi, agar fayl mavjud bo'lmasa, yangi fayl yaratadi.
- `x` – Faylni faqat yangi fayl yaratish uchun ochadi. Agar fayl allaqachon mavjud bo'lsa, xato chiqaradi.

```python
# Faylni o'qish uchun ochish
f = open("file.txt", "r")

# Faylga yozish uchun ochish
f = open("file.txt", "w")

# Faylga qo'shish uchun ochish
f = open("file.txt", "a")

# Fayl mavjud emasligini tekshirib, yaratish
f = open("file.txt", "x")
```

## ✅ FAYLNI O'QISH

Fayl ichidagi ma'lumotlarni o'qish uchun bir necha usullar mavjud:
- `read()` – Faylni to'liq o'qiydi.
- `readline()` – Fayldan bir qatorni o'qiydi.
- `readlines()` – Fayldagi barcha qatorlarni ro'yxat sifatida o'qiydi.

```python
f = open("file.txt", "r")

# Barcha ma'lumotni o'qish
content = f.read()
print(content)

# Bir qatorni o'qish
line = f.readline()
print(line)

# Barcha qatorlarni ro'yxatga o'qish
lines = f.readlines()
print(lines)

f.close()
```

## ✅ FAYLGA YOZISH

Faylga yozish uchun `write()` yoki `writelines()` metodlaridan foydalaniladi:
- `write()` – Faylga matn yozadi.
- `writelines()` – Ro'yxatdagi barcha qatorlarni faylga yozadi.

```python
# Faylga ma'lumot yozish

# "file.txt" nomli faylni yozish ("w") rejimida ochyapti
f = open("file.txt", "w")

# Faylga "Hello, Python!" matnini yozadi va yangi qatordan boshlaydi
f.write("Hello, Python!\n")

# Faylga ikkinchi qatorda matn yozadi
f.write("This is a second line.\n")

# Faylni yopadi, bu majburiy — ma'lumotlar saqlanadi va fayl yopiladi
f.close()


# Ro'yxatni faylga yozish

# Yoziladigan har bir element yangi qatordan iborat bo‘lgan ro'yxat
lines = ["First line\n", "Second line\n", "Third line\n"]

# "file.txt" nomli faylni yana yozish rejimida ochyapti (eski ma'lumot o‘chiriladi)
f = open("file.txt", "w")

# Ro'yxatdagi barcha elementlarni faylga ketma-ket yozadi
f.writelines(lines)

# Faylni yopadi
f.close()
```

## ✅ FAYLNI YOPISH

Fayl bilan ish tugagandan so'ng, uni yopish kerak. Faylni yopish uchun `close()` metodidan foydalaniladi.
```python
f = open("file.txt", "r")
# Fayldan o'qish jarayoni
f.close()  # Faylni yopish
```

> [!NOTE]
> Yana bir usul – faylni `with` bloki yordamida ochish, bunda fayl avtomatik ravishda yopiladi:
```python
with open("file.txt", "r") as f:
    content = f.read()
    print(content)
# Bu usulda faylni yopish shart emas, fayl avtomatik ravishda yopiladi.
```

## ✅ FAYL REJIMLARI

- `t` – Matn rejimi. Fayllarni matn sifatida ochadi. Bu rejim `r` va `w` bilan birga ishlatiladi. Masalan, `rt` yoki `wt`.
- `b` – Ikkilik (`binary`) rejimi. Fayllarni ikkilik rejimda ochadi. Masalan, `rb` yoki `wb`.

```python
# Ikkilik faylni o'qish
with open("image.png", "rb") as img:
    data = img.read()
    print(data)

# Ikkilik faylga yozish
with open("output.bin", "wb") as bin_file:
    bin_file.write(b"Binary data")
```

## ✅ FAYLLAR BILAN BOG'LIQ BAZI FUNKSIYALAR

- `os.remove()` – **Faylni o'chirish.**
- `os.rename()` – **Fayl nomini o'zgartirish.**
- `os.path.exists()` – **Fayl mavjudligini tekshirish.**

```python
# OS (Operating System) moduli — fayllar bilan ishlash, o‘chirish, nomini o‘zgartirish uchun kerak
import os

# "file.txt" nomli faylni o‘chiradi
# Agar bu fayl mavjud bo‘lmasa, xatolik (FileNotFoundError) yuz beradi
os.remove("file.txt")

# "old_name.txt" nomli faylni "new_name.txt" deb o‘zgartiradi
# Agar "old_name.txt" mavjud bo‘lmasa, yoki allaqachon "new_name.txt" mavjud bo‘lsa, xatolik beradi
os.rename("old_name.txt", "new_name.txt")

# Fayl mavjudligini tekshiradi
# Agar "file.txt" mavjud bo‘lsa, "File exists" chiqadi, bo‘lmasa "File not found"
if os.path.exists("file.txt"):
    print("File exists")
else:
    print("File not found")
```

# AMALIYOT

1. Yangi fayl yaratish va unga ma'lumot yozish:
- `example.txt` deb nomlangan yangi fayl yarating va unga `"Python is fun!"` yozuvini kiriting.
2. Fayldan ma'lumot o'qish
- Yaratilgan fayldan yozilgan ma'lumotni o'qing va ekranga chiqarib bering.