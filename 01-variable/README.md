# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 VARIABLES

>[!NOTE]
> Python dasturlash tilida `variables` — bu ma’lumotlarni `vaqtincha saqlash` uchun ishlatiladigan `nomlangan konteynerlardir`. O‘zgaruvchilar yordamida `ma’lumotlar bilan ishlash`, `ularni saqlash` va `qayta ishlatish` qulaylashadi.

## ✅ O'ZGARUVCHI NIMA?

**O'zgaruvchi** - kompyuter xotirasida ma'lum bir qiymatni saqlash uchun ajratilgan joy.

📌 Tasavvur qiling, sizda bir savat bor va unga olma solyapsiz. Bu savat — bu o‘zgaruvchi, olma esa qiymat. Siz xohlagan paytingizda savatdagi olmani almashtirishingiz mumkin. Dasturlashda ham o‘zgaruvchi — bu ma’lumotni vaqtincha saqlash uchun ishlatiladigan idish.

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

## ✅ 1-topshiriq: O‘zgaruvchilar yaratish

Quyidagi qiymatlarni mos o‘zgaruvchilarga saqlang va ularni `print()` yordamida ekranga chiqaring:

- Butun son: `25`
- Haqiqiy son: `4.5`
- Matn: `"Python"`
- Mantiqiy qiymat: `False`

**Kutilgan natija:**
```
25
4.5
Python
False
```

---

## ✅ 2-topshiriq: Qiymatni o‘zgartirish

Quyidagi amallarni bajaring:

- `ism` nomli o‘zgaruvchiga `"Ali"` qiymatini bering
- So‘ng bu o‘zgaruvchiga `"Vali"` qiymatini bering
- `print()` orqali oxirgi qiymatini chiqaring

**Kutilgan natija:**
```
Vali
```

---

## ✅ 3-topshiriq: Birdaniga bir nechta o‘zgaruvchi

Quyidagi qiymatlarni bitta qatorda yozing:

- `yosh = 20`
- `ism = "Aziza"`
- `status = True`

Ularni alohida `print()` bilan chiqaring.

**Kutilgan natija:**
```
20
Aziza
True
```

---

## ✅ 4-topshiriq: `type()` funksiyasi

Quyidagi kod orqali o‘zgaruvchilarning turini aniqlang:

```python
a = 10
b = "salom"
c = 3.14
d = False
```

Har birining `type()` qiymatini ekranga chiqaring.

**Kutilgan natija:**
```
<class 'int'>
<class 'str'>
<class 'float'>
<class 'bool'>
```

---

## ✅ 5-topshiriq: Foydalanuvchidan ma’lumot olish

Foydalanuvchidan `ism` va `yosh` ni `input()` yordamida oling va ularni quyidagicha chiqaruvchi dastur yozing:

```python
# Misol:
# Kirish:
# Ismingizni kiriting: Aziza
# Yoshingizni kiriting: 18

# Chiqish:
# Salom Aziza, siz 18 yoshdasiz.
```

---

## ✅ 6-topshiriq: O‘zgaruvchi turlarini tekshirish

Foydalanuvchidan quyidagi ma’lumotlarni oling:

- ism (matn)
- yosh (butun son)

Keyin ularning turini `type()` yordamida chiqaring.

**Kutilgan natija:**
```
<class 'str'>
<class 'str'>  # Sababi input() har doim str turida bo‘ladi
```

Bonus: `int()` orqali yoshni butun songa aylantirib ko‘ring.

---

## ✅ 7-topshiriq: O‘zgaruvchi nomlash xatolari

Quyidagi o‘zgaruvchilar to‘g‘rimi yoki noto‘g‘riligini aniqlang. Agar noto‘g‘ri bo‘lsa, to‘g‘ri shaklini yozing:

```python
1son = 5        # noto‘g‘ri
my-name = "Ali" # noto‘g‘ri
def = 10        # noto‘g‘ri (Python kalit so‘z)
ism_1 = "Aziza" # to‘g‘ri
```

---

## ✅ 8-topshiriq: `int()`, `float()`, `str()` funksiyalaridan foydalanish

Foydalanuvchidan son oling va uni:

- `int` turiga o‘tkazing
- `float` turiga o‘tkazing
- `str` turiga o‘tkazing

Har birining `type()` ni chiqaruvchi dastur yozing.

---

## ✅ 9-topshiriq: Foydalanuvchining to‘liq ma’lumotini chiqarish

Quyidagi ma’lumotlarni input orqali oling:

- ism
- familiya
- yosh
- kasb

Va quyidagicha formatda chiqarilsin:

```
Ismingiz: Ali
Familiyangiz: Karimov
Yoshingiz: 20
Kasbingiz: Dasturchi
```

---

## ✅ 10-topshiriq: O‘zgaruvchilarni almashtirish

Quyidagi o‘zgaruvchilar qiymatini bir-biri bilan almashtiring:

```python
a = 5
b = 10
```

So‘ng yangi qiymatlarni `print()` bilan chiqaring.

**Kutilgan natija:**
```
a = 10
b = 5
```
