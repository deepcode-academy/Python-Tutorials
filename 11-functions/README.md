# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 11-DARS FUNCTIONS

 📌 Python dasturlash tilida **funksiya** bu — kodni bir joyda yozib, ko‘p joylarda chaqirish, kodni tartibli va qisqa qilish uchun qulay vositadir. Funksiya yordamida kodni modullashtirish va takrorlanadigan qismni soddalashtirish mumkin.


## ✅ FUNKSIYA YARATISH (DEF)

```python
def greet():
    # Oddiy funksiya: salomlashish
    print("Hello, world!")
```

## ✅ CALLING A FUNCTION (FUNKSIYANI CHAQIRISH)

📌 Pythonda yozilgan funksiyani ishlatish uchun uni chaqirish kerak bo‘ladi. Buning uchun faqat funksiyaning nomi va qavslar () yoziladi.

```python
# Bu yerda biz greet() degan nomli funksiya yaratdik
def greet():
    # Funksiya ichida "Hello, world!" degan matnni chiqaradigan buyruq bor
    print("Hello, world!")

# Bu yerda esa yuqorida yaratilgan greet() funksiyasini chaqiryapmiz
greet()
```

## ✅ PARAMETERS AND ARGUMENTS (PARAMETRLAR VA ARGUMENTLAR)

📌 **Parametr** – bu funksiya yaratilyotganda yoziladigan o‘zgaruvchilar bo‘lib, ular funksiyaga ma’lumot qabul qilish uchun ishlatiladi.

```python
# Funksiya yaratilyapti, u 2 ta parametr oladi: a va b
def add(a, b):
    # a va b sonlar qo‘shilib, natija qaytariladi
    return a + b

# Funksiyani chaqiryapmiz, 2 va 3 argument sifatida uzatilyapti
result = add(2, 3)

# Natijani chiqaramiz
print(result)  # Natija: 5
```

🎯 Tasavvur qilaylik, siz foydalanuvchi ma’lumotlarini qabul qilib, uni ro‘yxatga qo‘shishingiz kerak.

```python
# Bo‘sh foydalanuvchilar ro‘yxati
users = []

# Funksiya foydalanuvchi ma’lumotlarini qabul qiladi
def add_user(name, age):
    # name va age – bu parametrlar
    user = {
        "name": name,
        "age": age
    }
    users.append(user)  # user ma’lumoti ro‘yxatga qo‘shiladi

# Funksiyani chaqiramiz, foydalanuvchi ma’lumotlarini argument sifatida beramiz
add_user("Ali", 25)
add_user("Laylo", 22)

# Natijada users ro‘yxatida 2 ta foydalanuvchi bo‘ladi
print(users)
```

📌 **Argument** – bu funksiyani chaqirayotganingizda beriladigan **real qiymat**. Parametrga haqiqiy qiymat uzatish uchun ishlatiladi.

```python
# Funksiya yaratildi. Parametr: ism
def salom_ber(ism):
    print(f"Salom, {ism}!")

# Funksiyani chaqirdik, argument sifatida "Umid" uzatildi
salom_ber("Umid")
```

🎯 Sizda email jo‘natuvchi tizim bor va siz **to**, **subject**, **body** argumentlarini berib, email jo‘natasiz.

```python
# Email jo‘natish funksiyasi
def send_email(to, subject, body):
    print(f"To: {to}")
    print(f"Subject: {subject}")
    print(f"Body: {body}")
    print("Email muvaffaqiyatli yuborildi!")

# Real loyiha – argumentlar bilan chaqirilmoqda
send_email(
    to="user@example.com",            # Argument: kimga yuboriladi
    subject="Xush kelibsiz!",         # Argument: sarlavha
    body="Siz muvaffaqiyatli ro‘yxatdan o‘tdingiz."  # Argument: matn
)
```

## ✅ DEFAULT PARAMETERS (STANDART PARAMETRLAR)

📌 **Standart parametr** — bu funksiyada oldindan belgilangan qiymatga ega bo‘lgan parametr. Agar funksiyani chaqirishda bu parametr uchun argument berilmasa, u default qiymatni ishlatadi.

```python
# Funksiya yaratildi, exponent parametri uchun default qiymat 2
def power(base, exponent=2):
    # base son exponent darajaga ko‘tariladi
    return base ** exponent

# Faqat bitta argument berdik – base = 3, exponent 2 deb olinadi (default)
print(power(3))      # Natija: 9 (3^2)

# Ikkala argumentni ham berdik – base = 3, exponent = 3
print(power(3, 3))   # Natija: 27 (3^3)
```

🎯 Sizda parol yaratish funksiyasi bor. Unga uzunlik (length) parametri beriladi, lekin foydalanuvchi kiritmasa, standart qiymat sifatida 8 belgilanadi.

```python
import random
import string

# Parol yaratish funksiyasi: uzunlik uchun standart qiymat 8
def generate_password(length=8):
    belgilar = string.ascii_letters + string.digits
    parol = ''.join(random.choice(belgilar) for _ in range(length))
    return parol

# Default uzunlik bilan chaqirish
print(generate_password())      # Masalan: a7B3kL2q

# Uzunlikni o‘zimiz beramiz
print(generate_password(12))    # Masalan: jD93kLm8Tz2Q
```

## ✅ QIYMAT QAYTARISH (RETURN)

📌 **return** — bu funksiya natijasini (qiymatini) tashqariga qaytarish uchun ishlatiladi. Bu qiymatni keyin saqlash, chiqarish yoki boshqa hisob-kitoblarda ishlatish mumkin.

```python
# Funksiya: x va y ni ko‘paytiradi
def multiply(x, y):
    return x * y  # Natija return orqali qaytariladi

# multiply(4, 5) = 20, bu qiymat product o‘zgaruvchisiga saqlanadi
product = multiply(4, 5)

# Natijani ekranga chiqaramiz
print(product)  # 20
```

🎯 Siz onlayn do‘konda mahsulotga 15% QQS solig‘i qo‘shilgan yakuniy narxni hisoblashni xohlaysiz.

```python
# Funksiya: mahsulot narxiga 15% soliq qo‘shadi
def hisobla_qqs(narx):
    qqs = narx * 0.15
    umumiy = narx + qqs
    return umumiy  # Yakuniy narx qaytariladi

# 100 000 so‘mlik mahsulot uchun yakuniy narx
yakuniy_narx = hisobla_qqs(100000)

print(f"Yakuniy narx (QQS bilan): {yakuniy_narx} so'm")
```

## ✅ HECH NIMA QAYTARMAYDIGAN FUNKSIYALAR (VOID FUNCTION)

```python
def print_welcome(name):
    print(f"Welcome, {name}!")  # Faqat ekranga chiqaradi, qiymat qaytarmaydi

print_welcome("Ali")
```

## ✅ QIYMAT QAYTARADIGAN FUNKSIYALAR (VALUE-RETURNING FUNCTION)

```python
def get_maximum(a, b):
    if a > b:
        return a
    else:
        return b

max_number = get_maximum(7, 10)
print(max_number)  # 10
```

## ✅ BIR NECHTA PARAMETRLAR BILAN ISHLASH

```python
def info(name, age, city):
    print(f"Name: {name}, Age: {age}, City: {city}")

info("Alice", 25, "Tashkent")
```

## ✅ FUNKSIYAGA RO‘YXAT (LIST) UZATISH

```python
def print_list(items):
    # Har bir elementni ekranga chiqaradi
    for item in items:
        print(item)

fruits = ["apple", "banana", "cherry"]
print_list(fruits)
```

## ✅ IXTIIYORIY ARGUMENTLAR: *ARGS

```python
def total_sum(*args):
    # args — tuple, istalgancha argument qabul qiladi
    return sum(args)

print(total_sum(1, 2, 3, 4, 5))  # 15
```

## ✅ KALITLI ARGUMENTLAR: **KWARGS

```python
def print_profile(**kwargs):
    # kwargs — dictionary, kalit so‘zli argumentlar qabul qiladi
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_profile(name="Bob", age=30, profession="Engineer")
```

## ✅ LAMBDA FUNKSIYALAR (QISQA FUNKSIYALAR)

```python
square = lambda x: x ** 2
print(square(6))  # 36

add = lambda x, y: x + y
print(add(3, 4))  # 7
```

## ✅ FUNKSIYALAR ICHIDA FUNKSIYALAR (NESTED FUNCTIONS)

```python
def outer(x):
    def inner(y):
        return y + 2
    return inner(x) * 2

result = outer(5)  # (5 + 2) * 2 = 14
print(result)  # 14
```

## ✅ REKURSIV FUNKSIYALAR (RECURSIVE FUNCTIONS)

```python
def factorial(n):
    # Bazaviy holat
    if n == 0:
        return 1
    # Rekursiv chaqirish
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

## ✅ TYPE ANNOTATION – TURINI KO‘RSATISH

```python
def add_numbers(a: int, b: int) -> int:
    return a + b

result: int = add_numbers(10, 20)
print(result)  # 30
```

## ✅ DOCSTRING – FUNKSIYAGA HUJJAT YOZISH

```python
def multiply(a: int, b: int) -> int:
    """
    Ikki sonni ko'paytiradi va natijani qaytaradi.
    :param a: birinchi son
    :param b: ikkinchi son
    :return: natija (int)
    """
    return a * b

print(multiply.__doc__)
```

## ✅ ICHKI (BUILT-IN) FUNKSIYALAR

```python
# len()
numbers = [1, 2, 3]
print(len(numbers))  # 3

# type()
print(type(numbers))  # <class 'list'>

# print()
print("Hello, Python!")

# input()
# name = input("Ismingizni kiriting: ")
# print(name)

# sum()
values = [4, 5, 6]
print(sum(values))  # 15

# max()
print(max(values))  # 6

# min()
print(min(values))  # 4

# range()
for i in range(3):
    print(i)  # 0, 1, 2
```

## ✅ HIGHER-ORDER FUNKSIYALAR

- **Higher-order function** — boshqa funksiyani argument sifatida qabul qiladigan yoki funksiya qaytaradigan funksiya.

```python
def apply_twice(func, value):
    # func — boshqa funksiya
    return func(func(value))

def increment(x):
    return x + 1

result = apply_twice(increment, 5)
print(result)  # 7
```

## ✅ DEKORATORLAR (DECORATORS)

```python
def uppercase_decorator(func):
    def wrapper():
        result = func()
        return result.upper()
    return wrapper

@uppercase_decorator
def greet():
    return "hello"

print(greet())  # "HELLO"
```