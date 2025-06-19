# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 01-DARS VARIABLES

## ✅ O'ZGARUVCHI NIMA?

📌 Python dasturlash tilida **o‘zgaruvchi (variable)** — bu kompyuterda **ma’lumotni vaqtincha saqlab turadigan nomlangan joy**. Bu joyga **biz har qanday ma’lumotni** (masalan, matn, son) joylashtirishimiz mumkin. Keyin bu nom orqali o‘sha ma’lumotdan **foydalanish, o‘zgartirish yoki hisoblash** osonlashadi. O‘zgaruvchilar bizga dastur ichida ma’lumot bilan ishlashni **tartibli** va **qulay** qiladi. Har safar ma’lumotni qayta yozmasdan, **nomini chaqirib ishlatishimiz mumkin**.


![alt text](images/image.png)


📌 Quyidagi misolda 4 ta o'zgaruvchi yaratdik (`x`, `y`, `name` va `is_student`) va ularga har xil ma'lumot yukladik.

```python
# Butun sonni (integer) o'zgaruvchiga saqlaymiz
x = 5

# Haqiqiy sonni (float) o'zgaruvchiga saqlaymiz
y = 3.14

# Matn (string) qiymatni o'zgaruvchiga saqlaymiz
name = "Alice"

# Mantiqiy (boolean) qiymatni o'zgaruvchiga saqlaymiz
is_student = True

# x o'zgaruvchisining qiymatini chiqaramiz
print(x)

# y o'zgaruvchisining qiymatini chiqaramiz
print(y)

# name o'zgaruvchisining qiymatini chiqaramiz
print(name)

# is_student o'zgaruvchisining qiymatini chiqaramiz
print(is_student)
```


📌 `variable` diyilishini sababi uning qiymati istalgan payt o'zgarishi mumkin:

```python
# 'name' o'zgaruvchisiga dastlab 'Alisher' matnini beramiz
name = 'Alisher'

# name o'zgaruvchisining hozirgi qiymatini chiqaramiz (Alisher)
print(name)

# name o'zgaruvchisining qiymatini o'zgartiramiz, endi u 'Muhammad' bo'ladi
name = "Muhammad"

# name o'zgaruvchisining yangi qiymatini chiqaramiz (Muhammad)
print(name)
```

## ✅ O'ZGARUVCHILARNI NOMLASH

## ❗ O'zgaruvchilarga nom berishda quyidagi qoidalarga amal qiling:

### ❌ O'zgaruvchi nomi harf yoki pastki chiziq (`_`) bilan boshlanishi kerak

✅ To‘g‘ri:

```python
# Harflardan tashkil topgan oddiy o'zgaruvchi nomi
ism = "Ali"

# Pastki chiziq (_) bilan boshlangan o'zgaruvchi nomi
_yosh = 25
```

❌ Noto‘g‘ri:

```python
# ❌ Son bilan boshlanmaydi
1ism = "Ali"
```

### ❌ O'zgaruvchi nomi raqam bilan boshlanishi mumkin emas

📌 Raqam faqat nomning oxirida yoki o‘rtasida ishlatilishi mumkin.

✅ To‘g‘ri:

```python
# O'zgaruvchi nomi harf bilan boshlangan va raqam bilan tugagan — to'g'ri
raqam1 = 10

# O'zgaruvchi nomi harf bilan boshlangan va oxirida raqam ishlatilgan — to'g'ri
sana2025 = 2025
```

❌ Noto‘g‘ri:

```python
# ❌ Raqam bilan boshlanmaydi
3dars = "Python"
```

### ❌ O'zgaruvchi nomida faqatgina ingliz tili alifbosi harflari (`A-z`), raqamlar (`0-9`) va pastki chiziq (`_`) qatnashishi mumkin

📌 Maxsus belgilar (`@`, `!`, `#`, `-` va boshqalar) o‘zgaruvchi nomida ishlatilmaydi.

✅ To‘g‘ri:

```python
# Lotin harflari va pastki chiziq ishlatilgan — to‘g‘ri
user_name = "Umid"

# Harf va raqam ishlatilgan — to‘g‘ri
user1 = "Ali"

# Pastki chiziq bilan boshlangan nom — bu ham to‘g‘ri
_max_score = 100
```

❌ Noto‘g‘ri:

```python
# O'zgaruvchi nomida '@' belgisi ishlatilgan — bu noto‘g‘ri
# ❌ Maxsus belgilar (masalan: @) Python'da o'zgaruvchi nomida bo'lmasligi kerak
ism@familiya = "Valijon"

# O'zgaruvchi nomida '!' belgisi ishlatilgan — bu ham noto‘g‘ri
# ❌ Maxsus belgilar (masalan: !) ruxsat etilmaydi
yosh! = 18
```

### ❌ O'zgaruvchi nomida bo'shliq (пробел) bo'lishi mumkin emas

✅ To‘g‘ri:

```python
# O'zgaruvchi nomida pastki chiziq ishlatilgan — bu to‘g‘ri usul
ism_familiya = "Ali Karimov"
```

❌ Noto‘g‘ri:

```python
# O'zgaruvchi nomida bo‘shliq (space) ishlatilgan — bu noto‘g‘ri
# ❌ Python'da o'zgaruvchi nomi bo‘shliq bilan yozilmaydi
ism familiya = "Ali Karimov"
```

### ❌ O'zgaruvchi nomida katta-kichik harflar turlicha talqin qilinadi (`ism`, `ISM`, va `Ism` uchta turli o'zgaruvchi)

📌 Pythonda `ism`, `ISM` va `Ism` bu uchta alohida o‘zgaruvchi hisoblanadi.

```python
# kichik harflardan tashkil topgan o'zgaruvchi
ism = "Ali"

# hamma harflari katta bo'lgan o'zgaruvchi — bu boshqa o'zgaruvchi
ISM = "Vali"

# bosh harfi katta, qolgan kichik bo'lgan o'zgaruvchi — yana boshqa o'zgaruvchi
Ism = "Sami"

# 'ism' o'zgaruvchisining qiymatini chiqaramiz
print(ism)  # Ali

# 'ISM' o'zgaruvchisining qiymatini chiqaramiz
print(ISM)  # Vali

# 'Ism' o'zgaruvchisining qiymatini chiqaramiz
print(Ism)  # Sami
```

## ✅ QO'SHIMCHA QOIDALAR

### ❇️ O'zgaruvchi nomini kichik harflar bilan yozing.

📌 Python kodini o‘qishda va tushunishda qulaylik uchun o‘zgaruvchilarni kichik harflar bilan yozish odatiy hisoblanadi.

```python
# To'g'ri va tavsiya qilinadigan usul — o'zgaruvchi nomi kichik harflardan iborat
ism = "Umid"

# Tavsiya qilinmaydi — bosh harf bilan boshlash kodda chalkashlik keltirib chiqarishi mumkin
Ism = "Umid"

# Tavsiya qilinmaydi — hamma harflar katta bo‘lishi ko‘pincha konstantalar uchun ishlatiladi
ISM = "Umid"
```

### ❇️ O'zgaruvchi nomida 2 va undan ortiq so'z qatnashsa ularning orasini pastki chiziq (`_`) bilan ajrating (`ism_sharif="Umid G'aybullayev"`) 

📌 Bu usul o‘zgaruvchi nomini o‘qishni osonlashtiradi va kodni yanada tushunarli qiladi.

```python
# Ikkita so‘zdan tashkil topgan o'zgaruvchi nomi, so‘zlar pastki chiziq bilan ajratilgan
ism_sharif = "Umid G'aybullayev"

# Ikkita so‘zdan tashkil topgan o'zgaruvchi nomi, so‘zlar pastki chiziq yordamida bog‘langan
tugilgan_yil = 2004
```

### ❇️ O'zgaruvchiga tushunarli nom bering (`y=20` emas `yosh=20`, `d="Korea"` emas `davlat = "Korea"` va hokazo)

📌 O‘zgaruvchi nomi uning ma’nosini ifodalashi kerak, shunda kodni o‘qish va tushunish osonlashadi.

```python
# Yomon misollar — nomlar qisqa va ma’nosiz, kodni tushunishni qiyinlashtiradi
y = 20
d = "Korea"

# Yaxshi misollar — nomlar ma’noli va tushunarli
yosh = 20
davlat = "Korea"
```

### ❇️ Shuningdek o'zgaruvchilarga Pythonda ishlatiladigan funksiyalar va maxsus kalit so'zlarning(keywords) nomini bermang. Kalit so'zlar ro'yhatini ko'rish uchun python faylga  uyidagi kodni yozamiz:

📌 Chunki bu nomlar Python tili tomonidan maxsus ma’noga ega va ular bilan nomlash kodni buzadi yoki xato beradi.

```python
# Python kalit so'zlarini ko'rish uchun quyidagilarni yozamiz
import keyword

# Python kalit so'zlar ro'yxatini chiqaramiz
print(keyword.kwlist)
```

✅ To‘g‘ri:

```python
# To‘g‘ri misollar — kalit so'zlarni o'zgaruvchi nomining bir qismi sifatida ishlatish mumkin
def_funksiya = 10
for_son = 20
```

❌ Noto‘g‘ri:

```python
# Noto‘g‘ri misollar — kalit so‘zlarni o‘zgaruvchi nomi sifatida ishlatish mumkin emas
def = 10    # ❌ 'def' kalit so'z, o'zgaruvchi sifatida ishlatilmaydi
for = 20    # ❌ 'for' kalit so'z, o'zgaruvchi sifatida ishlatilmaydi
```

# ✅ AMALIYOT

### ✅ 1-topshiriq:
Quyidagi qiymatlarni o‘zgaruvchilarga yuklang va print() orqali ekranga chiqaring:
- ismingiz
- yoshingiz
- sevimli soningiz
- talaba ekanligingiz (True yoki False)

---

### ✅ 2-topshiriq:
- Quyidagi ma’lumotlar uchun mos o‘zgaruvchilar yarating:
    - kitob_nomi → “Sariq devni minib”
    - muallif → “Xudoyberdi To‘xtaboyev”
    - sahifalar_soni → 185
    - Ularni print() yordamida chiqarib bering.

---

### ✅ 3-topshiriq:
- Quyidagi noto‘g‘ri o‘zgaruvchi nomlarini to‘g‘rilang:

```python
1kitob = "Python"
ism familiya = "Ali Karimov"
davlat@ = "Uzbekistan"
```

---

### ✅ 4-topshiriq:
- Quyidagi qiymatlarni saqlovchi o‘zgaruvchilarni yarating va print() bilan ularning turini (type()) chiqaring:
    - yosh = 25
    - baho = 4.5
    - ism = "Dilshod"
    - is_student = False

---

### ✅ 5-topshiriq:
- Quyidagi kodni yozing:
    - name o‘zgaruvchisi yarating va unga ism kiriting.
    - Keyin, uning qiymatini boshqa ism bilan almashtiring.
    - Har ikkala holatda qiymatni ekranga chiqaring.

---

### ✅ 6-topshiriq:
- Quyidagi noto‘g‘ri o‘zgaruvchilarni aniqlang va nega xato ekanligini yozing:

```python
for = "dars"
def = "funksiya"
yosh! = 20
```

---

### ✅ 7-topshiriq:
- Quyidagi ikkita o‘zgaruvchini yarating:
    - ism = "Jamshid"
    - ISM = "Anvar"
    - Ularning ikkalasini print() bilan chiqaring va nima sababdan ikkala qiymat chiqayotganini tushuntiring.

---

### ✅ 8-topshiriq:
- O‘zgaruvchi nomlarida pastki chiziq (_) ishlatish kerak bo‘lgan 3 ta misol yozing. Masalan: foydalanuvchi_ismi, kitob_soni, manzil_nomi

---

### ✅ 9-topshiriq:
- Tushunarli va tushunarsiz o‘zgaruvchi nomlariga 3 tadan misol yozing:
    - Yaxshi: yosh, davlat, kitob_nomi
    - Yomon: x, d, n1

---

### ✅ 10-topshiriq:
- Quyidagi kodni to‘g‘ri ko‘rinishga keltiring:
```python
3son = 25
user name = "Ali"
yosh@ = 20
```

---

### ✅ 11-topshiriq:
- Quyidagi o‘zgaruvchilarni yarating va print() yordamida ularni chiqarib bering:
    - kitob_nomi = "Yulduzli tunlar"
    - muallif = "Pirimqul Qodirov"
    - narx = 37000
    - mavjud = True

---

### ✅ 12-topshiriq:
- Kalit so‘zlar ro‘yxatini ko‘rsatadigan kod yozing va uni bajaring. Kod natijasida ekranda Python kalit so‘zlari chiqishi kerak.

---

### ✅ 13-topshiriq:
- Quyidagi kodni tahlil qiling. Nima sababdan xatolik borligini tushuntiring:
```python
import = "data"
True = 1
```

---

### ✅ 14-topshiriq:
- O‘zgaruvchilarni quyidagi ma’nolarga qarab yarating:
    - Foydalanuvchining ismi
    - Parol
    - Email manzili
    - Tug‘ilgan yili

---

### ✅ 15-topshiriq:
- Quyidagi qiymatlar uchun mos o‘zgaruvchilar yarating va ularni print() yordamida chiqarib, bir satrda type() funksiyasi bilan ularning turlarini ham ko‘rsating:
```python
ism = "Sardor"
yosh = 22
talaba = True
ball = 4.9
```