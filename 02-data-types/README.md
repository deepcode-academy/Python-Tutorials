# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 2-DARS DATA TYPES

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
# '+' operatori yordamida ikki yoki undan ortiq stringlarni birlashtirish mumkin

name = "Umid"
print("Mening ismim " + name)  # Natija: Mening ismim Umid

# Qo‘shishda so‘zlar orasiga bo‘sh joy (space) qo‘yish kerak, aks holda ular bir-biriga yopishib qoladi

first_name = "Umid"
last_name = "G'aybullayev"
print(first_name + last_name)  # Natija: UmidG'aybullayev (bo‘shliq yo‘q)

# To‘g‘ri natija uchun so‘zlar orasiga bo‘sh joy qo‘shamiz

print(first_name + " " + last_name)  # Natija: Umid G'aybullayev

```

### ❇️ STRING UZUNLIGINI ANIQLASH

📌 String uzunligi — bu stringdagi belgilar (characters) soni. Belgilarga harflar, raqamlar, bo‘sh joylar (spaces) va maxsus belgilar kiradi.

📌 String uzunligini topish uchun `len()` funksiyasidan foydalanamiz.


```python
# len() funksiyasi yordamida string uzunligini aniqlaymiz

text = "Hello, World!"

# text o'zgaruvchisidagi string uzunligini len() yordamida o'lchaymiz
length = len(text)  # Natija: 13

# Natijani ekranga chiqaramiz
print(length)
```

### ❇️ STRING E'LEMENTLARIGA MUROJAT QILISH
📌 String ichidan o'zimizga kerak bo'lgan e'lementlarni ajratib olish uchun quyidagi usuldan foydalanamiz:


```python
# String ichidan kerakli elementlarni olish uchun indekslash (indexing) va kesish (slicing) usullaridan foydalanamiz

text = "Hello world!"

# Birinchi e'lementni olish uchun indeks 0 dan boshlanadi
first_char = text[0]  # Natija: 'H'

# Oxirgi e'lementni olish uchun indeks sifatida -1 ishlatiladi
last_char = text[-1]  # Natija: '!'

# e'lementlarni kesib olish (substring) uchun start va stop indekslar beriladi (stop indeksi kiritilgan indeksdan oldingi belgigacha)
substring = text[0:5]  # Natija: 'Hello' (0-indeksdan 4-indeksgacha)

# Natijalarni ekranga chiqaramiz
print(first_char)
print(last_char)
print(substring)
```

### ❇️ STRINGLARNI KO'PAYTIRISH

📌 Python dasturida string ni ko‘paytirish orqali bir xil matnni takrorlash mumkin. Buning uchun `*` operatoridan foydalanamiz.

```python
# Stringni ko‘paytirish orqali bir xil e'lementni takrorlash mumkin
# Buning uchun '*' operatoridan foydalanamiz

text = "Hello"

# hello so'zini 3 marta takrorlaymiz
text_repeated = text * 3  # Natija: 'HelloHelloHello'

# Natijani ekranga chiqaramiz
print(text_repeated)
```

### ❇️ F-STRING(Python 3.6+)

📌 Python 3.6 versiyasidan boshlab, string ichida o‘zgaruvchilarni (variables) va ifodalarni (expressions) to‘g‘ridan-to‘g‘ri joylashtirish uchun f-string (formatted string literal) usuli joriy etildi. Bu usul string formattingning eng qulay va tezkor usullaridan biri hisoblanadi.


```python
# O'zgaruvchilarni string ichida qulay tarzda qo'shish uchun f-string usulidan foydalanamiz
ism = "Umid"
yosh = 20

# f-string yordamida string ichiga o'zgaruvchilarni joylashtirish
text = f"Mening ismim {ism}, yoshim {yosh}da"  # Natija: Mening ismim Umid, yoshim 20da

# Natijani ekranga chiqaramiz
print(text)
```

### ❇️ STRING METODLARI

📌 Python dasturlash tilida, stringlar ustida turli xil operatsiyalarni bajarish uchun bir qancha o'rnatilgan metodlar mavjud. Quyida eng ko'p qo'llaniladigan string metodlari va ularning misollari keltirilgan:

1. `.upper()`

```python
# .upper() - Matndagi barcha harflarni katta harfga aylantiradi
text = "hello"
print(text.upper())  # Natija: HELLO


# Foydalanuvchi ismini doim katta harflarda saqlash uchun,
# bazada bir xil ism turli holatda yozilgan bo‘lsa ham xatolik bo‘lmasin
user_input = "umid"
username = user_input.upper()
print(username)  # UMID
```
2. `.lower()`

```python
# .lower() - Matndagi barcha harflarni kichik harfga aylantiradi
text = "HELLO"
print(text.lower())  # Natija: hello


# Email yoki username tekshiruvda har doim kichik harflarga o‘zgartirish kerak,
# chunki email kichik harflarda yoziladi
email = "User@Example.COM"
email_normalized = email.lower()
print(email_normalized)  # user@example.com
```
3. `.capitalize()`

```python
# .capitalize() - Matnning birinchi harfini katta harfga, qolganlarini kichik harfga aylantiradi
text = "hello world"
print(text.capitalize())  # Natija: Hello world


# Foydalanuvchi ismini chiroyli ko‘rsatish uchun,
# faqat birinchi harf katta bo‘lsin
name = "umid"
print(name.capitalize())  # Umid
```
4. `.title()`

```python
# .title() - Matndagi har bir so'zning birinchi harfini katta harfga aylantiradi
text = "hello world"
print(text.title())  # Natija: Hello World



# Blog post yoki maqola sarlavhasini
# har bir so‘zni bosh harfi katta bo‘lsin uchun formatlash
title = "python dasturlash asoslari"
print(title.title())  # Python Dasturlash Asoslari
```

5. `.lstrip()`

```python
# .lstrip() - Matnning boshidagi bo'sh joylarni olib tashlaydi
text = "    hello world    "
print(text.lstrip())  # Natija: "hello world    "
```

6. `.rstrip()`

```python
# .rstrip() - Matnning oxiridagi bo'sh joylarni olib tashlaydi
text = "    hello world    "
print(text.rstrip())  # Natija: "    hello world"
```
7. `.strip()`

```python
# .strip() - Matnning boshidagi va oxiridagi bo'sh joylarni olib tashlaydi
text = "    hello world    "
print(text.strip())  # Natija: "hello world"



# toza ma’lumot olish maqsadida
user_input = "   umid   "
clean_input = user_input.strip()
print(clean_input)  # "umid"
```

8. `.replace(old, new)`

```python
# 1-qator: "matn" nomli o'zgaruvchiga biror matn qiymatini beramiz
matn = "Salom dunyo"

# 2-qator: "matn"dagi "dunyo" so'zini "Umid" so'ziga almashtiramiz.
# replace() metodi eski so'zni yangi so'z bilan almashtirib, natijani "yangi_matn" ga saqlaydi
yangi_matn = matn.replace("dunyo", "Umid")

# 3-qator: Yangi hosil bo'lgan matnni ekranga chiqaramiz
print(yangi_matn)


# 1-qator: "raqam" o'zgaruvchisiga telefon raqamini matn ko'rinishida beramiz
raqam = "+998 90 123 45 67"

# 2-qator: 
# .replace(" ", "") - bu yerda barcha bo'sh joylar (" ") olib tashlanadi
# .replace("+", "") - bu yerda "+" belgisi olib tashlanadi
raqam = raqam.replace(" ", "").replace("+", "")

# 3-qator: Tozalangan raqamni ekranga chiqaramiz
print(raqam)
```

9. `.split(separator)`

```python
# 1-qator: "text" o'zgaruvchisiga matn berilgan
text = "Hello world Python"

# 2-qator: .split() metodi bo'sh joy (" ") bo'yicha matnni bo'lib, ro'yxatga aylantiradi
print(text.split())  
# Natija: ['Hello', 'world', 'Python']

# 3-qator: .split('o') metodi "o" harfi bo'yicha bo'lib ro'yxatga aylantiradi
print(text.split('o'))  
# Natija: ['Hell', ' w', 'rld Pyth', 'n']





# 1-qator: "qidiruv" nomli o'zgaruvchiga foydalanuvchi yozgan matn saqlanadi
qidiruv = "telefon kompyuter printer"

# 2-qator: .split() metodi yordamida matn bo'sh joy bo'yicha bo'linadi
# Natijada ['telefon', 'kompyuter', 'printer'] degan ro'yxat (list) hosil bo'ladi
sozlar = qidiruv.split()

# 3-qator: ro'yxatdagi har bir so'z ustida aylanish (for loop) boshlanadi
for text in sozlar:
    # 4-qator: har bir so'z ekranga chiqariladi
    print("Qidirilmoqda:", text)
```

10. `.join(iterable)`

```python
# 1-qator: 3 ta so'zdan iborat ro'yxat yaratiladi
words = ['Hello', 'world', 'Python']

# 2-qator: ' '.join(words) ro'yxatdagi so'zlarni bo'sh joy bilan birlashtiradi
print(' '.join(words))  # Natija: Hello world Python

# 3-qator: '-'.join(words) so'zlarni "-" bilan birlashtiradi
print('-'.join(words))  # Natija: Hello-world-Python





# 1-qator: 'kodlar' nomli ro'yxat yaratilmoqda,
# ichida 3 ta element - matn ko'rinishidagi kodlar bor
kodlar = ['AB12', 'CD34', 'EF56']

# 2-qator: '-'.join(kodlar) yordamida ro'yxat elementlari orasiga 
# chiziqcha ("-") qo'yib, ularni bitta matnga birlashtiramiz
parol = '-'.join(kodlar)

# 3-qator: natijani ekranga chiqaramiz
print("Yangi parol:", parol)
```

11. `.find(substring)`

```python
# 1-qator: text o'zgaruvchisiga "Hello world" matni saqlanmoqda
text = "Hello world"

# 2-qator: .find() metodi yordamida "world" so'zining text ichidagi 
# boshlanish indeksini topamiz. Agar topilsa, indeks qaytariladi
print(text.find("world"))  # Natija: 6

# 3-qator: .find() metodi yordamida "Python" so'zining indeksini izlaymiz,
# lekin matnda yo'q, shuning uchun -1 qaytariladi
print(text.find("Python")) # Natija: -1




# 1-qator: url o'zgaruvchisiga URL matni saqlanmoqda
url = "https://example.com/page?id=123"

# 2-qator: url ichidan "id=" matnining indeksini topamiz
pos = url.find("id=")

# 3-qator: agar "id=" topilgan bo'lsa (indeks -1 emas)
if pos != -1:
    # 4-qator: identifikatorni "id=" dan keyingi qismdan ajratib olamiz
    # pos+3 degani "id=" so'zidan keyingi belgidan boshlab olish
    identifikator = url[pos+3:]
    # 5-qator: ekranga chiqaramiz
    print("ID:", identifikator)
```

12. `.startswith(prefix)`

```python
# 1-qator: text o'zgaruvchisiga "Hello world" matni saqlanmoqda
text = "Hello world"

# 2-qator: .startswith() metodi yordamida matn "Hello" bilan boshlanishini tekshiramiz
print(text.startswith("Hello"))  # Natija: True

# 3-qator: .startswith() metodi yordamida matn "world" bilan boshlanishini tekshiramiz
print(text.startswith("world"))  # Natija: False




# 1-qator: url o'zgaruvchisiga URL manzili saqlanmoqda
url = "https://example.com/api/user"

# 2-qator: url matni "https://example.com/api/" bilan boshlanishini tekshiramiz
if url.startswith("https://example.com/api/"):
    # 3-qator: agar to'g'ri bo'lsa, "API so'rovi" deb chiqaramiz
    print("API so'rovi")
```

13. `.endswith(suffix)`

```python
# 1-qator: text o'zgaruvchisiga "Hello world" matni saqlanmoqda
text = "Hello world"

# 2-qator: .endswith() metodi yordamida matn "world" bilan tugashini tekshiramiz
print(text.endswith("world"))  # Natija: True

# 3-qator: .endswith() metodi yordamida matn "Hello" bilan tugashini tekshiramiz
print(text.endswith("Hello"))  # Natija: False




# 1-qator: filename o'zgaruvchisiga fayl nomi saqlanmoqda
filename = "photo.jpg"

# 2-qator: agar filename ".jpg" bilan tugasa, shart bajariladi
if filename.endswith(".jpg"):
    # 3-qator: ekranga "Rasm fayli" deb chiqaramiz
    print("Rasm fayli")
```

14. `.count(substring)`

```python
# 1-qator: text o'zgaruvchisiga "hello hello world" matni saqlanmoqda
text = "hello hello world"

# 2-qator: .count() metodi yordamida matnda "hello" so'zi necha marta takrorlanganini hisoblaymiz
print(text.count("hello"))  # Natija: 2
```


## ✅ NUMBERS

📌 Numbers — bu sonlarni ifodalash uchun ishlatiladigan ma'lumot turi. 

📌 Pythonda asosiy 3ta number type mavjud:

- **int** — butun sonlar (masalan, 5, -10, 100)
- **float** — o'nlik sonlar (masalan, 3.14, -0.001, 2.0)
- **complex** — kompleks sonlar (masalan, 2 + 3j, -1j)

### ❇️ INTEGER

📌 Integer ma'lumot turi butun sonlarni ifodalaydi. Bu sonlar `manfiy`, `musbat` yoki `0` bo'lishi mumkin. Integerlar cheklanmagan uzunlikka ega, ya'ni Python juda katta sonlarni ham integer sifatida saqlay oladi.

```python
x = 10                       # musbat butun son
y = -5                       # manfiy butun son
z = 0                        # nol
a = 12345678901234567890     # juda katta butun son

# Quyidagi print() funksiyalari har bir o'zgaruvchining turini ko'rsatadi
print(type(x))  # <class 'int'>
print(type(y))  # <class 'int'>
print(type(z))  # <class 'int'>
print(type(a))  # <class 'int'>
```
### ✅ INTEGER USTIDA AMALLAR
📌 Integerlar ustida asosiy matematik amallarni bajarish mumkin:

```python
# Integerlar (butun sonlar) ustida bajariladigan asosiy matematik amallar

a = 10  # Birinchi butun son
b = 3   # Ikkinchi butun son

# Qo'shish: ikkita sonni qo'shadi, natija 13 bo'ladi
print(a + b)  # 10 + 3 = 13

# Ayirish: birinchi sondan ikkinchi sonni ayiradi, natija 7 bo'ladi
print(a - b)  # 10 - 3 = 7

# Ko'paytirish: ikkita sonni ko'paytiradi, natija 30 bo'ladi
print(a * b)  # 10 * 3 = 30

# Bo'lish: birinchi sonni ikkinchi songa bo'ladi, natija float (kasr) turida chiqadi
print(a / b)  # 10 / 3 ≈ 3.3333333333333335

# Butun qismini olish: bo'linmaning faqat butun qismini oladi, o'nlik qismi tashlanadi
print(a // b)  # 10 // 3 = 3

# Qoldiqni olish: bo'linmaning qoldig'ini hisoblaydi (modulus)
print(a % b)  # 10 % 3 = 1

# Darajaga ko'tarish: birinchi sonni ikkinchi son darajasiga ko'taradi
print(a ** b)  # 10 ** 3 = 1000
```

### ✅ UZUN SONLARNI KIRITISH

📌 Uzun sonlarni kiritishda, qulaylik uchun, raqamlarni pastki chiziq (`_`) yordamida guruhlash mumkin. Python - son tarkibidagi pastki chiziqlarni (`_`) inobatga olmasdan, uzun sonligicha qabul qiladi.

```python
# Bank hisobidagi pul miqdori (katta son)
bank_hisobi = 1_250_000_000  # 1 milliard 250 million so'm

print("Sizning hisobingizdagi mablag'", bank_hisobi, "so'm")
# Chiqarish: Sizning hisobingizdagi mablag' 1250000000 so'm
```


### ✅ BIR NECHTA O'ZGARUVCHIGA QIYMAT BERISH
📌 Birdaniga bir nechta o'zgaruvchiga qiymat berish uchun o'zgaruvchilar va ularga mos qiymatlar vergul (`,`) bilan ajratiladi:

```python
# Bir nechta o'zgaruvchilarga bir qatorda qiymat berish mumkin

# x ga 10 (integer), y ga -7.25 (float), z ga -30 (integer) qiymatlari bir vaqtning o'zida berildi
x, y, z = 10, -7.25, -30

# Natijalarni chiqaramiz
print("x ning qiymati:", x)  # 10
print("y ning qiymati:", y)  # -7.25
print("z ning qiymati:", z)  # -30
```

### ✅ O'ZGARUVCHI TURINI ALMASHTIRISH

📌 Python dasturlash tilida o'zgaruvchilar turini bir ma'lumot turidan boshqa ma'lumot turiga o'zgartirish jarayoni `type casting` deb ataladi.


```python
# Type casting misollari — qiymatlarni o'zgaruvchilarga saqlash va ularni turini tekshirish

# 1. int() — float va stringdan int ga o'tish
float_son = 3.7
int_from_float = int(float_son)          # 3.7 dan 3 ga (kasr qismi tashlanadi)

string_son = "25"
int_from_string = int(string_son)        # "25" matnidan 25 (int) hosil bo'ladi

# 2. float() — int va stringdan float ga o'tish
int_son = 10
float_from_int = float(int_son)          # 10 dan 10.0 ga

string_float = "3.14"
float_from_string = float(string_float)  # "3.14" matnidan 3.14 hosil bo'ladi

# 3. str() — har qanday qiymatni stringga aylantirish
int_num = 123
str_from_int = str(int_num)               # int 123 -> string "123"

float_num = 3.14
str_from_float = str(float_num)           # float 3.14 -> string "3.14"

bool_val = True
str_from_bool = str(bool_val)             # True -> "True"

# 4. bool() — qiymatni True yoki False ga aylantirish
bool_from_one = bool(1)                   # 1 -> True
bool_from_zero = bool(0)                  # 0 -> False

bool_from_empty_str = bool("")            # bo'sh string -> False
bool_from_nonempty_str = bool("Hello")   # bo'sh bo'lmagan string -> True

bool_from_empty_list = bool([])           # bo'sh ro'yxat -> False
bool_from_list = bool([1, 2, 3])          # bo'sh bo'lmagan ro'yxat -> True

# Natijalarni chiqaramiz

print(int_from_float, type(int_from_float))         # 3 <class 'int'>
print(int_from_string, type(int_from_string))       # 25 <class 'int'>

print(float_from_int, type(float_from_int))         # 10.0 <class 'float'>
print(float_from_string, type(float_from_string))   # 3.14 <class 'float'>

print(str_from_int, type(str_from_int))             # '123' <class 'str'>
print(str_from_float, type(str_from_float))         # '3.14' <class 'str'>
print(str_from_bool, type(str_from_bool))           # 'True' <class 'str'>

print(bool_from_one, type(bool_from_one))           # True <class 'bool'>
print(bool_from_zero, type(bool_from_zero))         # False <class 'bool'>
print(bool_from_empty_str, type(bool_from_empty_str))       # False <class 'bool'>
print(bool_from_nonempty_str, type(bool_from_nonempty_str)) # True <class 'bool'>
print(bool_from_empty_list, type(bool_from_empty_list))     # False <class 'bool'>
print(bool_from_list, type(bool_from_list))                   # True <class 'bool'>
```


### ✅ INPUT

📌 `input()` — bu Python dasturlash tilidagi maxsus funksiya bo‘lib, u foydalanuvchidan klaviatura orqali ma'lumot olish uchun ishlatiladi.

```python
# input() funksiyasi foydalanuvchidan ma'lumot olish uchun ishlatiladi.
# Funksiya ichidagi matn — bu foydalanuvchiga ko'rsatiladigan savol yoki so'rov.

ism = input("Ismingizni kiriting: ")  # Foydalanuvchidan ismni so'raymiz

print("Salom,", ism)  # Kiritilgan ismni ekranga chiqaramiz
```

📌 input() har doim matn (string) ko‘rinishida qiymat oladi. Agar son kiritilishini istasak, stringni son turiga o‘zgartirish kerak.

```python
# foydalanuvchi kiritgan matnni butun songa aylantiramiz
yosh = int(input("Yoshingizni kiriting: "))  
print("Sizning yoshingiz:", yosh)
```


```python
# 1. Foydalanuvchidan tug'ilgan yilini so'raymiz
t_yil = input("Tug'ilgan yilingizni kiriting: ")

# 2. input() funksiyasi har doim matn (string) ko'rinishida ma'lumot beradi,
# shuning uchun uni butun son (integer) ga o'tkazamiz
t_yil = int(t_yil)

# 3. Yilni hozirgi yil bilan solishtirib, yoshni hisoblaymiz
hozirgi_yil = 2025
yosh = hozirgi_yil - t_yil

# 4. Natijani ekranga chiqaramiz
print("Siz " + str(yosh) + " yoshda ekansiz.")
```

### ❇️ FLOAT

📌 Pythonda o'nlik sonlar `floating point numbers` yoki qisqa qilib `floats` deyiladi. Ingliz tilida o'nlik sonlarni yozishda vergul (`,`) emas nuqta (`.`) belgisi ishlatiladi, va bu nuqta sonning katta kichikligiga qarab joyi o'zgargani uchun `"floating"` deyiladi.


```python
pi = 3.14159       # o'nlik son, ya'ni float turidagi o'zgaruvchi
radius = 10        # butun son, ya'ni int turidagi o'zgaruvchi
diametr = 2 * radius  # diametrni hisoblaymiz (radiusning 2 barobariga teng)

# aylana uzunligini hisoblab, natijani chiqaramiz
print("Aylana uzunligi ", pi * diametr, " ga teng.")
```

### ❇️ FLOAT USTIDA AMALLAR

```python
a = 5.5    # a o'zgaruvchisiga 5.5 (float) qiymat berildi
b = 2.0    # b o'zgaruvchisiga 2.0 (float) qiymat berildi

print("Qo‘shish:", a + b)       # a va b ni qo‘shish => 7.5
print("Ayirish:", a - b)        # a dan b ni ayirish => 3.5
print("Ko‘paytirish:", a * b)   # a va b ni ko‘paytirish => 11.0
print("Bo‘lish:", a / b)        # a ni b ga bo‘lish (haqiqiy bo‘lish) => 2.75
print("Butun qismga bo‘lish:", a // b)  # a ni b ga bo‘lish va butun qismni olish => 2.0
print("Qoldiq:", a % b)         # a ni b ga bo‘lishda qolgan qoldiq => 1.5
print("Daraja:", a ** b)        # a ni b-darajaga ko‘tarish => 30.25
```

## ✅ COMPLEX

📌 Complex sonlar — bu ikkita qismdan iborat sonlar: haqiqiy qism (real part) va mavhum qism (imaginary part).

📌 Pythonda murakkab sonlar `complex` tipida saqlanadi. Pythonda imaginary part `j` yoki `J` harfi bilan ifodalanadi (elektronika va fizikada `j` ishlatiladi, matematikada esa `i`).

### ❇️ COMPLEX SON YARATISH

```python
# Kompleks son yaratamiz: real part 3, imaginary part 4j
z1 = 3 + 4j

# Kompleks sonni konsolga chiqaramiz
print(z1)  # Natija: (3+4j)
```

## ✅ KONSTANTA

📌 Python dasturlash tilida `"constant"` deb ataladigan o'zgaruvchilar mavjud emas, lekin dasturchilar odatda o'zgaruvchilarni konstantalar sifatida ishlatishadi. Bu odatda o'zgaruvchining qiymati dastur davomida o'zgarmasligini anglatadi.

1. **Konstantalarni nomlash:** Konstantalarni nomlashda katta harflar ishlatiladi. Bu, dasturchiga o'zgaruvchining qiymati o'zgarmasligini anglatadi.

```python
# Bu yerda PI nomli konstanta e'lon qilinmoqda
# Odatda konstanta nomlari katta harflarda yoziladi
# PI ning qiymati o‘zgarmaydi va doim 3.14159 bo‘lib qoladi
PI = 3.14159

# Bu yerda MAX_USERS nomli konstanta e'lon qilinmoqda
# Bu maksimum foydalanuvchilar sonini bildiradi
MAX_USERS = 100
```

2. **Konstantalarni modullarda saqlash:** Konstantalarni alohida Python faylida (modulda) saqlash tavsiya etiladi. Bu, konstantalarni boshqa fayllarda ishlatishni osonlashtiradi. Misol uchun, `constants.py` nomli fayl yaratib, unda konstantalarni saqlash mumkin:

```python
# constants.py

# constants.py faylida o'zgarmas (konstanta) qiymatlar saqlanadi
# Bu konstantalar boshqa fayllardan import qilib ishlatiladi

# Aylana uchun PI qiymati
PI = 3.14159

# Maksimal foydalanuvchilar soni
MAX_USERS = 100
```

- Keyin boshqa faylda bu konstantalarni ishlatish mumkin:

```python
# main.py

# constants.py modulidagi konstantalarni import qilamiz
import constants

# PI konstantasini terminalga chiqaramiz
print(constants.PI)  # Natija: 3.14159

# MAX_USERS konstantasini terminalga chiqaramiz
print(constants.MAX_USERS)  # Natija: 100
```

3. Konstantalarni o'zgartirishga urinish: Python tilida konstantalarni o'zgartirish mumkin, lekin bu tavsiya etilmaydi. Agar siz konstantani o'zgartirmoqchi bo'lsangiz, bu dastur xatolarga olib kelishi mumkin.

```python
# PI konstanta deb qaralmoqda, ya'ni doimiy qiymat sifatida ishlatiladi
PI = 3.14159

# Ammo bu yerda PI qiymatini o'zgartirib yubordik
# Bu sintaktik jihatdan xato emas, lekin yomon amaliyot hisoblanadi
# Chunki dasturchilar PI o'zgarmaydi deb o'ylaydi
PI = 3.14  # ❌ Bu tavsiya etilmaydi

# Dastur davomida bu o'zgarish kutilmagan xatolarga olib kelishi mumkin
print("PI qiymati:", PI)  # Natija: 3.14
```

# ✅ AMALIYOT

## ✅ 1-topshiriq: String birlashtirish
Foydalanuvchidan ism va familiya input() orqali oling. Ularni birlashtirib, "F.I.O: <ism> <familiya>" tarzida ekranga chiqaring.

---

## ✅ 2-topshiriq: String uzunligini topish
Foydalanuvchidan matn input() orqali oling va uning uzunligini `len()` yordamida aniqlang.

---

## ✅ 3-topshiriq: String indekslash va kesish
"Python dasturlash" matnini o‘zgaruvchiga saqlang. Birinchi harfini, oxirgi harfini va "dastur" so‘zini alohida ekranga chiqaring.

---

## ✅ 4-topshiriq: String ko‘paytirish
Foydalanuvchidan so‘z oling va uni 4 marta ketma-ket chiqaruvchi dastur yozing.

---

## ✅ 5-topshiriq: F-stringdan foydalanish
Foydalanuvchidan ism va yosh input() orqali olib, quyidagicha f-string yordamida chiqaring.  
Misol: `Ismingiz: Aziza, Yoshingiz: 19`

---

## ✅ 6-topshiriq: String metodlari bilan ishlash
Foydalanuvchidan matn input() orqali oling. Uni:
- katta harflarga,
- kichik harflarga,
- birinchi harfini katta qilishga
o‘zgartirib, har birini alohida ekranga chiqaring.

---

## ✅ 7-topshiriq: .replace() va .split() metodi
Foydalanuvchidan telefon raqami oling (masalan: "+998 90 123 45 67") va uni bo‘sh joylar va "+" belgisidan tozalang, so‘ng split() yordamida 2 xonali bloklarga ajrating.

---

## ✅ 8-topshiriq: .join() va .count()
Foydalanuvchidan so‘zlar ro‘yxatini input() orqali so‘rab, ularni vergul bilan birlashtiring va "a" harfi necha marta qatnashganini hisoblang.

---

## ✅ 9-topshiriq: .find(), .startswith(), .endswith()
Foydalanuvchidan matn va so‘z oling. Matnda so‘z qayerdan boshlanishini, matn aynan shu so‘z bilan boshlanish yoki tugashini aniqlang.

---

## ✅ 10-topshiriq: Integer va float ustida amallar
Foydalanuvchidan ikkita butun son va bir float son oling. Ularning yig‘indisi, ko‘paytmasi va o‘zaro bo‘linmasini hisoblang.

---

## ✅ 11-topshiriq: Uzoq sonni guruhlash
Bank hisobingizdagi pul miqdorini pastki chiziq yordamida o‘qish oson bo‘ladigan formatda yozing va ekranga chiqaring.

---

## ✅ 12-topshiriq: Type casting (turini o‘zgartirish)
Foydalanuvchidan raqamli matn oling va uni int, float, str va bool turiga o‘tkazib, har birini va turini chiqaring.

---

## ✅ 13-topshiriq: Kompleks son
Real va imag qismlarni input orqali olib, kompleks son yarating va uni ekranga chiqaring.

---

## ✅ 14-topshiriq: Konstantadan foydalanish
PI va MAX_USERS konstantasini yarating (katta harflar bilan). Ularni ekranga chiqaruvchi dastur yozing.

---

## ✅ 15-topshiriq: Foydalanuvchi yoshi va input
Foydalanuvchidan tug‘ilgan yilini input orqali olib, yoshini hisoblab chiqaring (hozirgi yilni o‘zingiz yozing).  
Misol: `Siz 20 yoshdasiz.`

---