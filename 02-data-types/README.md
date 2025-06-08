# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 DATA TYPES

## ✅ MA'LUMOT TURLARI

📌 Python dasturlash tilida har bir qiymat (value) — o‘zining ma'lumot turiga (data type) ega. Bu tur qiymatga qanday ishlov berishni aniqlaydi.


📌 Python dasturlash tilida `8` ta ma'lumot turi bor, ular quyidagilar:

| Definition      | Type                               |
|-----------------|------------------------------------|
| Text Type       | `str`                              |
| Numeric Types   | `int`, `float`, `complex`          |
| Sequence Types  | `list`, `tuple`, `range`           |
| Mapping Type    | `dict`                             |
| Set Types       | `set`, `frozenset`                 |
| Boolean Type    | `bool`                             |
| Binary Types    | `bytes`, `bytearray`, `memoryview` |
| None Type       | `NoneType`                         |

## ✅ STRING

📌 String — bu matnli ma’lumotlarni ifodalovchi ma’lumot turi. Ya’ni, harflar, raqamlar, bo‘sh joy, belgilardan tashkil topgan qator (yoki matn).

📌 Pythonda stringlar ikki yoki uchta qo‘shtirnoq (" ") yoki tirtirnoq (' ') bilan yoziladi.

```python
# Double quotes — ikki tirnoq (" ") bilan yozilgan oddiy string
text = "Hello world"
print(text)

# Single quotes — bitta tirnoq (' ') bilan yozilgan oddiy string
text = 'Hello world'
print(text)

# Triple double quotes — uchta ikki tirnoq (""" """) bilan yozilgan ko‘p qatorli matn (multiline string)
text = """This is a
multiline string."""
print(text)

# Triple single quotes — uchta bitta tirnoq (''' ''') bilan yozilgan ko‘p qatorli matn (multiline string)
text = '''This is also a
multiline string.'''
print(text)
```
### ❇️ STRING USTIDA AMALLAR

📌 Matnlarni qo'shish uchun `+` operatoridan foydalanamiz.


```python
# 📌 '+' operatori yordamida ikki yoki undan ortiq stringlarni birlashtirish mumkin

name = "Umid"
print("Mening ismim " + name)  # Natija: Mening ismim Umid

# 📌 Qo‘shishda so‘zlar orasiga bo‘sh joy (space) qo‘yish kerak, aks holda ular bir-biriga yopishib qoladi

first_name = "Umid"
last_name = "G'aybullayev"
print(first_name + last_name)  # Natija: UmidG'aybullayev (bo‘shliq yo‘q)

# 📌 To‘g‘ri natija uchun so‘zlar orasiga bo‘sh joy qo‘shamiz

print(first_name + " " + last_name)  # Natija: Umid G'aybullayev

```

### ❇️ STRING UZUNLIGINI ANIQLASH

📌 String uzunligi — bu stringdagi belgilar (characters) soni. Belgilarga harflar, raqamlar, bo‘sh joylar (spaces) va maxsus belgilar kiradi.

📌 String uzunligini topish uchun `len()` funksiyasidan foydalanamiz.


```python
# 📌 len() funksiyasi yordamida string uzunligini aniqlaymiz

text = "Hello, World!"

# 📌 text o'zgaruvchisidagi string uzunligini len() yordamida o'lchaymiz
length = len(text)  # Natija: 13

# 📌 Natijani ekranga chiqaramiz
print(length)
```

### ❇️ STRING E'LEMENTLARIGA MUROJAT QILISH
📌 String ichidan o'zimizga kerak bo'lgan e'lementlarni ajratib olish uchun quyidagi usuldan foydalanamiz:


```python
# 📌 String ichidan kerakli elementlarni olish uchun indekslash (indexing) va kesish (slicing) usullaridan foydalanamiz

text = "Hello world!"

# 📌 Birinchi e'lementni olish uchun indeks 0 dan boshlanadi
first_char = text[0]  # Natija: 'H'

# 📌 Oxirgi e'lementni olish uchun indeks sifatida -1 ishlatiladi
last_char = text[-1]  # Natija: '!'

# 📌 e'lementlarni kesib olish (substring) uchun start va stop indekslar beriladi (stop indeksi kiritilgan indeksdan oldingi belgigacha)
substring = text[0:5]  # Natija: 'Hello' (0-indeksdan 4-indeksgacha)

# 📌 Natijalarni ekranga chiqaramiz
print(first_char)
print(last_char)
print(substring)
```

### ❇️ STRINGLARNI KO'PAYTIRISH

📌 Python dasturida string ni ko‘paytirish orqali bir xil matnni takrorlash mumkin. Buning uchun `*` operatoridan foydalanamiz.

```python
# 📌 Stringni ko‘paytirish orqali bir xil e'lementni takrorlash mumkin
# Buning uchun '*' operatoridan foydalanamiz

text = "Hello"

# 📌 hello so'zini 3 marta takrorlaymiz
text_repeated = text * 3  # Natija: 'HelloHelloHello'

# 📌 Natijani ekranga chiqaramiz
print(text_repeated)
```

### ❇️ F-STRING(Python 3.6+)

📌 Python 3.6 versiyasidan boshlab, string ichida o‘zgaruvchilarni (variables) va ifodalarni (expressions) to‘g‘ridan-to‘g‘ri joylashtirish uchun f-string (formatted string literal) usuli joriy etildi. Bu usul string formattingning eng qulay va tezkor usullaridan biri hisoblanadi.


```python
# 📌 O'zgaruvchilarni string ichida qulay tarzda qo'shish uchun f-string usulidan foydalanamiz
ism = "Umid"
yosh = 20

# 📌 f-string yordamida string ichiga o'zgaruvchilarni joylashtirish
text = f"Mening ismim {ism}, yoshim {yosh}da"  # Natija: Mening ismim Umid, yoshim 20da

# 📌 Natijani ekranga chiqaramiz
print(text)
```
**Result:** `Mening ismim Umid, yoshim 20da`

### STRING METODLARI
Python dasturlash tilida, stringlar ustida turli xil operatsiyalarni bajarish uchun bir qancha o'rnatilgan metodlar mavjud. Quyida eng ko'p qo'llaniladigan string metodlari va ularning misollari keltirilgan:

1. `.upper()` - Matndagi barcha harflarni katta harfga aylantiradi.

```python
text = "hello"
print(text.upper()) #HELLO
```
2. `.lower()` - Matndagi barcha harflarni kichik harfga aylantiradi.

```python
text = "HELLO"
print(text.lower()) #hello
```
3. `.capitalize()` - Matnning birinchi harfini katta harfga, qolganlarini kichik harfga aylantiradi.

```python
text = "hello world"
print(text.capitalize()) # Hello world
```
4. `.title()` - Matndagi har bir so'zning birinchi harfini katta harfga aylantiradi.

```python
text = "hello world"
print(text.title()) # Hello World
```

5. `.lstrip()` - Matnning faqat boshidagi bo'sh joylarni olib tashlaydi.

```python
text = "    hello world    "
print(text.lstrip()) # "hello world    "
```
6. `.rstrip()` - Matnning faqat oxiridagi bo'sh joylarni olib tashlaydi.

```python
text = "    hello world    "
print(text.rstrip()) # "    hello world"
```
7. `.strip()` - Matnning boshida va oxiridagi bo'sh joylarni olib tashlaydi.

```python
text = "    hello world    "
print(text.strip()) # "hello world"
```

## NUMBER

- **Number** - Raqamli ma'lumot turi `2` ga bo'linadi:
    - **Integer(int)** - Butun sonlarni ifodalaydi. Masalan: `10`, `-3`, `42`.

Integer ma'lumot turi butun sonlarni ifodalaydi. Bu sonlar `manfiy`, `musbat` yoki `0` bo'lishi mumkin. Integerlar cheklanmagan uzunlikka ega, ya'ni Python juda katta sonlarni ham integer sifatida saqlay oladi.

```python
x = 10
y = -5
z = 0
a = 12345678901234567890

print(type(x))  # <class 'int'>
print(type(y))  # <class 'int'>
print(type(z))  # <class 'int'>
print(type(a))  # <class 'int'>
```
### INTEGER USTIDA AMALLAR
Integerlar ustida asosiy matematik amallarni bajarish mumkin:
```python
a = 10
b = 3

print(a + b)  # Qo'shish: 13
print(a - b)  # Ayirish: 7
print(a * b)  # Ko'paytirish: 30
print(a / b)  # Bo'lish: 3.3333333333333335
print(a // b) # Butun qismini olish: 3
print(a % b)  # Qoldiqni olish: 1
print(a ** b) # Darajaga ko'tarish: 1000
```

### UZUN SONLARNI KIRITISH
Uzun sonlarni kiritishda, qulaylik uchun, raqamlarni pastki chiziq (`_`) yordamida guruhlash mumkin. Python - son tarkibidagi pastki chiziqlarni (`_`) inobatga olmasdan, uzun sonligicha qabul qiladi.

```python
aholi_soni = 7_594_000_000 # o'qishga qulay bo'lishi uchun shunaqa ko'rinishda yozdik
print("Yer sharida", aholi_soni, "ga yaqin odam yashaydi")
```


### BIR NECHTA O'ZGARUVCHIGA QIYMAT BERISH
Birdaniga bir nechta o'zgaruvchiga qiymat berish uchun o'zgaruvchilar va ularga mos qiymatlar vergul (`,`) bilan ajratiladi:
```python
x, y, z = 10, -7.25, -30
```

### O'ZGARUVCHI TURINI ALMASHTIRISH

Python dasturlash tilida o'zgaruvchilar turini bir ma'lumot turidan boshqa ma'lumot turiga o'zgartirish jarayoni `type casting` deb ataladi.

#### integerdan floatga o'zgartirish

```python
x = 10
y = float(x)  # 10.0

print(type(y))  # <class 'float'>
print(y)        # 10.0
```

#### floatdan integerga o'zgartirish
> [!NOTE]
> Floatni Integerga o'zgartirishda kasr qismini olib tashlaydi.

```python
x = 3.14
y = int(x)  # 3

print(type(y))  # <class 'int'>
print(y)        # 3
```

#### stringdan integerga o'zgartirish

> [!CAUTION]
> stringni integerga o'zgartirish uchun string faqat `raqamlarni` o'z ichiga olishi kerak.

```python
s = "123"
x = int(s)  # 123

print(type(x))  # <class 'int'>
print(x)        # 123
```

#### integerdan stringga o'zgartirish

```python
x = 123
s = str(x)  # "123"

print(type(s))  # <class 'str'>
print(s)        # "123"
```

#### floatdan stringga o'zgartirish

```python
x = 3.14
s = str(x)  # "3.14"

print(type(s))  # <class 'str'>
print(s)        # "3.14"
```

### input()
Foydalanuvchidan ma'lumot olish uchun `input()` funksiyasidan foydalanamiz:

```python
ism = input("Ismingizni kiriting: ")
print(ism)
```

Yuqoridagi kodda foydalanuvchidan ism kiritishini so'radik va kiritilgan ismni terminalga chiqardik.

Input funksiyasidan foydalanishni o'rgandik, endi shu funksiya yordamida foydalanuvchidan son olishni o'rganamiz:

```python
#1 foydalanuvchining tug'ilgan yilini so'raymiz
t_yil = input("Tug'ilgan yilingizni kiriting: ")
#2 foydalanuvchi yoshini xisoblaymiz
yosh = 2020 - t_yil # 
#3 foydalanuvchi yoshini konsolga chiqaramiz
print("Siz " + yosh + " yoshda ekansiz")
```

- **Floating Point(float)** - O'nlik sonlarni ifodalaydi. Masalan: `3.14`, `-2.7`,` 0.99`.

> [!NOTE]
> Pythonda o'nlik sonlar `floating point numbers` yoki qisqa qilib `floats` deyiladi. Ingliz tilida o'nlik sonlarni yozishda vergul (`,`) emas nuqta (`.`) belgisi ishlatiladi, va bu nuqta sonning katta kichikligiga qarab joyi o'zgargani uchun `"floating"` deyiladi.

```python
pi = 3.14159 # o'nlik son (float)
radius = 10  # butun son (integer)
diametr = 2*radius
print("Aylana uzunligi ", pi*diametr, " ga teng.")
```


# Constants

### KONSTANTA

Python dasturlash tilida "constant" deb ataladigan o'zgaruvchilar mavjud emas, lekin dasturchilar odatda o'zgaruvchilarni konstantalar sifatida ishlatishadi. Bu odatda o'zgaruvchining qiymati dastur davomida o'zgarmasligini anglatadi.

1. **Konstantalarni nomlash:** Konstantalarni nomlashda katta harflar ishlatiladi. Bu, dasturchiga o'zgaruvchining qiymati o'zgarmasligini anglatadi.

```python
PI = 3.14159
MAX_USERS = 100
```

2. **Konstantalarni modullarda saqlash:** Konstantalarni alohida Python faylida (modulda) saqlash tavsiya etiladi. Bu, konstantalarni boshqa fayllarda ishlatishni osonlashtiradi. Misol uchun, `constants.py` nomli fayl yaratib, unda konstantalarni saqlash mumkin:

```python
# constants.py
PI = 3.14159
MAX_USERS = 100
```

- Keyin boshqa faylda bu konstantalarni ishlatish mumkin:

```python
import constants

print(constants.PI)  # 3.14159
print(constants.MAX_USERS)  # 100
```

3. Konstantalarni o'zgartirishga urinish: Python tilida konstantalarni o'zgartirish mumkin, lekin bu tavsiya etilmaydi. Agar siz konstantani o'zgartirmoqchi bo'lsangiz, bu dastur xatolarga olib kelishi mumkin.

```python
PI = 3.14159
PI = 3.14  # Bu tavsiya etilmaydi, lekin xato emas
```