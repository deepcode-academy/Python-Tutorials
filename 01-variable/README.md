# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 O'ZGARUVCHILAR

>[!NOTE]
> Python dasturlash tilida `variables` — bu ma’lumotlarni `vaqtincha saqlash` uchun ishlatiladigan `nomlangan konteynerlardir`. O‘zgaruvchilar yordamida `ma’lumotlar bilan ishlash`, `ularni saqlash` va `qayta ishlatish` qulaylashadi.

## O'ZGARUVCHILAR

**O'zgaruvchi** - kompyuter xotirasida ma'lum bir qiymatni saqlash uchun ajratilgan joy.

📌 Tasavvur qiling, sizda bir savat bor va unga olma solyapsiz. Bu savat — bu o‘zgaruvchi, olma esa qiymat. Siz xohlagan paytingizda savatdagi olmani almashtirishingiz mumkin. Dasturlashda ham o‘zgaruvchi — bu ma’lumotni vaqtincha saqlash uchun ishlatiladigan idish.

![alt text](images/image.png)

**Example:**

Quyidagi misolda 4 ta o'zgaruvchi yaratdik (`x`, `y`, `name` va `is_student`) va ularga har xil ma'lumot yukladik.

```python
x = 5 # Butun son (int)
y = 3.14 # Haqiqiy son (float)
name = "Alice"  # Matn (str)
is_student = True  # Mantiqiy qiymat (bool)
print(x)
print(y)
print(name)
print(is_student)
```

**Result:**

`5` <br>
`3.14` <br>
`Alice` <br>
`True`

**Example:**

`variable` diyilishini sababi uning qiymati istalgan payt o'zgarishi mumkin:

```python
name = 'Alisher'
print(name)
name = "Muhammad"
print(name)
```

**Result:**

`Alisher` <br>
`Muhammad`

Yuqoridagi misolda `name` nomli o'zgaruvchiga avval `Alisher` keyin esa `Muhammad` deb qiymat berdik.

### O'ZGARUVCHILARNI NOMLASH
> [!CAUTION]
> O'zgaruvchilarga nom berishda quyidagi qoidalarga amal qiling:
> - O'zgaruvchi nomi harf yoki pastki chiziq (`_`) bilan boshlanishi kerak
> - O'zgaruvchi nomi raqam bilan boshlanishi mumkin emas
> - O'zgaruvchi nomida faqatgina lotin alifbosi harflari (`A-z`), raqamlar (`0-9`) va pastki chiziq (`_`) qatnashishi mumkin
> - O'zgaruvchi nomida bo'shliq (пробел) bo'lishi mumkin emas
> - O'zgaruvchi nomida katta-kichik harflar turlicha talqin qilinadi (`ism`, `ISM`, va `Ism` uchta turli o'zgaruvchi)

**Q'shimcha qoidalar:**
- O'zgaruvchi nomini kichik harflar bilan yozing.
- O'zgaruvchi nomida 2 va undan ortiq so'z qatnashsa ularning orasini pastki chiziq (`_`) bilan ajrating (`ism_sharif="Umid G'aybullayev"`) 
- O'zgaruvchiga tushunarli nom bering (`y=20` emas `yosh=20`, `d="Korea"` emas `davlat = "Korea"` va hokazo)
- Shuningdek o'zgaruvchilarga Pythonda ishlatiladigan funksiyalar va maxsus kalit so'zlarning(keywords) nomini bermang. Kalit so'zlar ro'yhatini ko'rish uchun python faylga  uyidagi kodni yozamiz:
```python
import keyword
print(keyword.kwlist)
```
Marhamat, ekraningizda Pythondagi maxsus kalit so'zlar ro'yhatini ko'ryapsiz:
![alt text](images/keyword.png)



## MA'LUMOT TURLARI
Python dasturlash tilida `7` ta ma'lumot turi bor, ular quyidagilar:

![alt text](images/data_types.png)

## STRING

- **String(str)** - Matnli ma'lumotlarni ifodalaydi. Masalan: `"hello"`, `'world'`, `"123"`.

**Example:**  

```python
# ikkitalik qo'shtirnoqlar bilan
text = "Hello world"
print(text)

# bittalik qo'shtirnoqlar bilan
text = 'Hello world'
print(text)

# Ko'p qatorli stringlar uchlik qo'shtirnoqlar bilan
text = """This is a
multiline string."""
print(text)

text = '''This is also a
multiline string.'''
print(text)
```
### STRING USTIDA AMALLAR
Matnlarni qo'shish uchun `+` operatoridan foydalanamiz.

**Example:**

```python
name = "Umid"
print("Mening ismim " + name)
```
**Result:** `Mening ismim Umid`

**Example:**

```python
first_name = "Umid"
last_name = "G'aybullayev"
print(first_name + last_name)
```
**Result:** `UmidG'aybullayev` <br>

Yuqoridagi kodimizda ism va familiya qo'shilib qoldi, uni to'g'irlash uchun quyidagi ko'rinishda yozamiz:

**Example:**

```python
ism = "Umid"
familiya = "G'aybullayev"
print(ism + ' ' + familiya)
```
**Result:** `Umid G'aybullayev`

### STRING UZUNLIGINI ANIQLASH
Matnlarimizni uzunligini topish uchun `len()` funksiyasidan foydalanamiz.

**Example:**

```python
text = "Hello, World!"
length = len(text)  # 13
print(length)
```
**Result:** `13`

### STRING E'LEMENTLARIGA MUROJAT QILISH
Matnlarimiz ichidan o'zimizga kerak bo'lgan harflarni ajratib olish uchun quyidagi usuldan foydalanamiz:

**Example:**

```python
text = "Hello world!"
first_char = text[0] # H
last_char = text[-1]  # '!'
substring = text[0:5]  # 'Hello'
print(first_char)
print(last_char)
print(substring)
```
**Result:** <br>
`H` <br>
`!` <br>
`Hello`

### STRINGLARNI KO'PAYTIRISH

**Example:**

```python
text = "Hello"
text_repeated = text * 3
print(text_repeated)
```
**Result:** `HelloHelloHello`

### F-STRING(Python 3.6+)

**Example:**

```python
ism = "Umid"
yosh = 20
text = f"Mening ismim {ism}, yoshim {yosh}da" #Mening ismim Umid, yoshim 20da
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

# TASKS

1. O‘zgaruvchilar bilan arifmetik amallar
    - Quyidagi arifmetik amallarni bajarish uchun o‘zgaruvchilarni yarating:
        - `a` degan o'zgaruvchi yarating va unga `8` qiymat bering
        - `b` degan o'zgaruvchi yarating va unga `3` qiymat bering
        - Ularning `yig'indisi`, `ayirmasi`, `ko‘paytmasi` va `bo‘linmasi`ni hisoblang.

**Natija:** <br>
```python
Qo‘shish: 11
Ayirish: 5
Ko‘paytirish: 24
Bo‘lish: 2.6666666666666665
```

2. O‘zgaruvchi qiymatini almashtirish
    - `m` degan o'zgaruvchi yarating va unga `15` qiymat bering
    - `n` degan o'zgaruvchi yarating va unga `25` qiymat bering
    - Ularning qiymatlarini almashtiring, ya’ni `m` ning qiymatini `n` ga, `n` ning qiymatini esa `m` ga o‘tkazing.

**Natija:** <br>
```python
m = 25
n = 15
```
3. O‘zgaruvchi turlarini o‘zgartirish
    - Quyidagi ko‘rsatmalarga asosan o‘zgaruvchi turlarini o‘zgartiring:
        - `s` degan o'zgaruvchi yarating, unga `"123"` qiymat bering va butun songa o'zgartiring.
        - `r` degan o'zgaruvchi yarating, unga `"45.67"` qiymat bering va float turiga o'zgartiring
        - `q` degan o'zgaruvchi yarating, unga `"78.9"` qiymat bering va float turidan butun songa o'zgartiring.
        
**Natija:** <br>
```python
s = 123
r = 45.67
q = 78
```

4. O‘zgaruvchi uzunligini aniqlash
    - String o‘zgaruvchi yaratib, uning uzunligini aniqlang:
    - `matn` degan o'zgaruvchi yarating va unga `"Hello World!"` qiymatini bering.
    - Ushbu matnning `uzunligini` aniqlang va terminalga chiqaring.

**Natija:** <br>
```python
Matn uzunligi: 12
```

5. Ikki raqamni qo'shish
    - `raqam1` degan o'zgaruvchi yarating va unga `"5"` qiymat bering.
    - `raqam2` degan o'zgaruvchi yarating va unga `"5.5"` qiymat bering.
    - Berilgan ikkita raqamni (`int` yoki `float`) qo'shing va natijani terminalga chiqarib bering.

**Natija:** <br>
```python
Natija: 9.5
```