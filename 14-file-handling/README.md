# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 14-DARS FILE HANDLING

📌 Fayl — bu kompyuterda ma'lumotlar saqlanadigan obyekt. U matn, rasm, ovoz yoki dasturiy kod bo‘lishi mumkin. Biz dasturda aynan matnli fayllar bilan ko‘p ishlaymiz, masalan: .txt, .csv, .json fayllar.

## ❓ FAYL NIMA UCHUN KERAK?

📝 Ma'lumotlarni saqlash — Dastur tugagandan keyin ham ma'lumot yo‘qolmasligi uchun.

🔁 Qayta ishlash — Avval yozilgan ma'lumotlarni o‘qib, tahlil qilish yoki o‘zgartirish.

📤 Boshqa dasturlar bilan almashish — Fayllar orqali boshqa dasturlar bilan axborot almashiladi.

📚 Katta hajmdagi ma'lumotlar — Ma'lumot bazasidan oldin oddiy fayllarda saqlanadi (masalan, .csv fayllar).

## ✅ FAYLNI OCHISH

📌 Faylni ochish uchun `open()` funksiyasidan foydalaniladi. Bu funksiya fayl nomini va rejimini qabul qiladi. `open()` funksiyasida ikkinchi parametr sifatida fayl rejimini ko'rsatishingiz mumkin:

## ✅ FAYL REJIMLARI

📌 `r` – Faylni o'qish uchun ochish. Fayl mavjud bo'lishi kerak.

📌 `w` – Faylga yozish uchun ochish. Agar fayl mavjud bo'lmasa, yangi fayl yaratadi. Mavjud fayl bo'lsa, ma'lumotlarni o'chirib yuboradi.

📌 `a` – Faylga qo'shish uchun ochish. Mavjud faylga yangi ma'lumot qo'shadi, agar fayl mavjud bo'lmasa, yangi fayl yaratadi.

📌 `x` – Faylni faqat yangi fayl yaratish uchun ochadi. Agar fayl allaqachon mavjud bo'lsa, xato chiqaradi.

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

📌 Fayl ichidagi ma'lumotlarni o'qish uchun bir necha usullar mavjud:
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

📌 Faylga yozish uchun `write()` yoki `writelines()` metodlaridan foydalaniladi:
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

📌 Fayl bilan ish tugagandan so'ng, uni yopish kerak. Faylni yopish uchun `close()` metodidan foydalaniladi.
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

## ✅ FAYLNI YOPMASA NIMA BO'LADI?

### ✅ 1. MA'LUMOTLAR FAYLGA YOZILMASLIGI MUMKIN (YOKI KECHIKIB YOZILISHI)

📌 Python faylga yozayotgan paytda ma'lumotlarni dastlab xotira buferida saqlaydi. Faylni yopsangizgina bu ma'lumotlar diskka to‘liq yoziladi.

```python
# "data.txt" nomli faylni yozish ("w") rejimida ochadi (agar fayl bo'lmasa, yangi yaratadi)
f = open("data.txt", "w")

# Faylga "Bu matn faylga yoziladi." matnini yozadi
f.write("Bu matn faylga yoziladi.")

# Faylni yopish yo‘q, shuning uchun yozilgan ma'lumot faylga saqlanmasligi yoki fayl ochiq qolishi mumkin
# f.close() qatori bo‘lmasa, ma'lumotlar operatsion tizimning fayl keshida qolishi ehtimoli bor
```

### ✅ 2. FAYL BOSHQALAR UCHUN BAND BO‘LIB QOLADI

📌 Agar siz faylni yopmasangiz, u operatsion tizim tomonidan "ochiq" deb hisoblanadi va boshqa dasturlar (yoki boshqa kod qismlari) uni o‘qiy olmaydi yoki tahrirlay olmaydi.

### ✅ 3. XOTIRA RESURSLARI ORTIQCHA BAND BO‘LADI

📌 Har bir ochilgan fayl tizimda resurs (file descriptor) sifatida band qilinadi. Fayllar yopiqlmasa, bu resurslar ortadi va dastur sekinlashishi yoki xatoliklar chiqishi mumkin.

### ✅ 4. MA'LUMOTLAR BUZILISHI YOKI YO‘QOLISHI MUMKIN

📌 Agar yozish davomida fayl yopilmasa va dastur to‘satdan to‘xtasa, yozilgan ma'lumotlar saqlanmasligi yoki fayl buzilishi mumkin.

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

# ✅ AMALIYOT


## ✅ 1-topshiriq:
`example.txt` faylini ochib, uning ichidagi matnni to‘liq o‘qing va ekranga chiqaring.

---

## ✅ 2-topshiriq:
`info.txt` nomli yangi fayl yarating va foydalanuvchidan `ism`, `familiya` va `yosh` so‘rab, faylga yozing.

---

## ✅ 3-topshiriq:
`numbers.txt` nomli faylga `1` dan `10` gacha bo‘lgan sonlarni har birini yangi qatordan yozing.

---

## ✅ 4-topshiriq:
`numbers.txt` faylini o‘qing va har bir qatordagi sonni ikkiga ko‘paytirib ekranga chiqaring.

---

## ✅ 5-topshiriq:
`append_example.txt` fayliga har safar dasturni ishga tushirganingizda `"New line"` yozuvi qo‘shilsin.

---

## ✅ 6-topshiriq:
Foydalanuvchidan `3` ta gap yozdirib oling va ularni `sentences.txt` fayliga yozing.

---

## ✅ 7-topshiriq:
`sentences.txt` faylidan faqat birinchi qatorni o‘qib chiqaring va chop eting.

---

## ✅ 8-topshiriq:
`lines.txt` faylida `5` ta qatordan iborat matn bor deb tasavvur qiling. Har bir qatordagi belgilar sonini chiqaring.

---

## ✅ 9-topshiriq:
`data.txt` fayli mavjud bo‘lsa, uni o‘chiring. Mavjud emasligini tekshirib, foydalanuvchiga bildiring.

---

## ✅ 10-topshiriq:
`old.txt` faylini `new.txt` deb o‘zgartiring. Fayl mavjud emas bo‘lsa, `“Fayl topilmadi”` deb chiqaring.

---

## ✅ 11-topshiriq:
`users.txt` faylida foydalanuvchilarning ismlari bo‘lsin. Fayldan ro‘yxatni o‘qib, har bir ismni `Hello, <ism>!` shaklida ekranga chiqaring.

---

## ✅ 12-topshiriq:
`text.txt` fayliga inglizcha `3` gap yozing. So‘ng ushbu faylni o‘qib, har bir gapdagi so‘zlar sonini hisoblang.

---

## ✅ 13-topshiriq:
Rasmlar uchun `photo.jpg` faylini `rb` (binary read) rejimida oching va fayl hajmini (baytlarda) aniqlang.

---

## ✅ 14-topshiriq:
`items.txt` faylidan barcha qatorlarni ro‘yxatga o‘qing, ushbu ro‘yxatni `output.txt` fayliga nusxa ko‘chiring.
