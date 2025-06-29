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

## ✅ RETURN (QIYMAT QAYTARISH)

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

## ✅ VOID FUNCTION (HECH NIMA QAYTARMAYDIGAN FUNKSIYALAR)

📌 Void function – bu funksiya natija (qiymat) qaytarmaydi, faqat biror amalni bajaradi, masalan: ekranga chiqarish, faylga yozish, yoki ma’lumot bazasiga yozish.

```python
# Funksiya: foydalanuvchini kutib oladi
def print_welcome(name):
    print(f"Welcome, {name}!")  # Faqat chop etadi, hech nima qaytarmaydi

# Funksiyani chaqiramiz
print_welcome("Ali")
```

🎯 Sizda har bir foydalanuvchi tizimga kirganda logga yozib boradigan funksiya kerak. Bu funksiya hech narsa qaytarmaydi — faqat faylga yozadi.

```python
# Foydalanuvchini log fayliga yozish funksiyasi
def log_user_login(username):
    with open("log.txt", "a") as fayl:
        fayl.write(f"{username} tizimga kirdi.\n")

# Funksiyani chaqirish
log_user_login("Ali")
log_user_login("Laylo")
```

## ✅ VALUE-RETURNING FUNCTION (QIYMAT QAYTARADIGAN FUNKSIYALAR)

📌 Qiymat qaytaradigan funksiya — bu funksiya return operatori yordamida natijani (qiymatni) qaytaradi.

```python
# Funksiya: ikki sonning kattasini aniqlaydi
def get_maximum(a, b):
    if a > b:
        return a  # Agar a katta bo‘lsa, a ni qaytar
    else:
        return b  # Aks holda b ni qaytar

# Funksiyani chaqiramiz, 7 va 10 ni argument sifatida uzatamiz
max_number = get_maximum(7, 10)

# Natijani chiqaramiz
print(max_number)  # 10
```

🎯 Siz onlayn do‘kon qilayapsiz va sizga mahsulotlar ichidan eng qimmatini topuvchi funksiya kerak.

```python
# Funksiya: 2 ta mahsulot narxidan eng kattasini qaytaradi
def get_expensive(price1, price2):
    if price1 > price2:
        return price1
    else:
        return price2

# Misol uchun 2 ta mahsulot narxi
narx1 = 850_000
narx2 = 990_000

# Funksiyani chaqiramiz va natijani saqlaymiz
eng_qimmat = get_expensive(narx1, narx2)

print(f"Eng qimmat mahsulot narxi: {eng_qimmat} so'm")
```


## ✅ FUNKSIYAGA RO‘YXAT (LIST) UZATISH

📌 Pythonda funksiya yaratganda parametr sifatida ro‘yxat (list) berishimiz mumkin. Bu funksiyaga bir nechta qiymatni birdan uzatish imkonini beradi.

```python
# Funksiya: ro‘yxatdagi elementlarni ekranga chiqaradi
def print_list(items):
    # Har bir element ustida aylanish (for loop)
    for item in items:
        print(item)

# Ro‘yxat yaratamiz
fruits = ["apple", "banana", "cherry"]

# Funksiyaga ro‘yxatni argument sifatida uzatamiz
print_list(fruits)
```

🎯 Sizda Telegram bot bor va siz bir nechta foydalanuvchilarga avtomatik xabar yubormoqchisiz. Har bir foydalanuvchining ismi ro‘yxatda berilgan.

```python
# Funksiya: har bir foydalanuvchiga xush kelibsiz xabari yuboradi
def send_welcome(users):
    for user in users:
        print(f"Assalomu alaykum, {user}!")

# Foydalanuvchilar ro‘yxati
user_list = ["Ali", "Laylo", "Javohir"]

# Funksiyani chaqiramiz
send_welcome(user_list)
```

## ✅ *ARGS

📌 *args – bu funksiya istalgancha sonli argument qabul qilishi uchun ishlatiladi. U * belgisi bilan yoziladi, va Python uni tuple sifatida saqlaydi.

```python
# Funksiya: istalgancha son qabul qilib, ularning yig‘indisini qaytaradi
def total_sum(*args):
    # args bu tuple ko‘rinishidagi o‘zgaruvchi
    return sum(args)

# Funksiyaga 5 ta son uzatdik
print(total_sum(1, 2, 3, 4, 5))  # Natija: 15
```

🎯 Sizda savatdagi mahsulotlar narxini avtomatik hisoblaydigan funksiya bor.

```python
# Funksiya: mahsulot narxlarini qabul qilib, umumiy summani hisoblaydi
def hisobla_savat(*narxlar):
    umumiy = sum(narxlar)
    return umumiy

# Mahsulotlar: non 8000, sut 12000, guruch 25000, choy 15000
print(hisobla_savat(8000, 12000, 25000, 15000))  # Natija: 60000
```

## ✅ **KWARGS

📌 **kwargs — bu funksiyaga kalit-qiymat juftliklari ko‘rinishida istalgancha argument yuborish imkonini beradi. U lug‘at (dictionary) sifatida qabul qilinadi: *key: value*

```python
# Funksiya: foydalanuvchi profilidagi har bir kalit-qiymatni chiqaradi
def print_profile(**kwargs):
    # kwargs — dictionary, .items() bilan kalit-qiymatlarni ajratamiz
    for key, value in kwargs.items():
        print(f"{key}: {value}")

# Funksiyani chaqiramiz, kalit-qiymat juftliklari bilan
print_profile(name="Bob", age=30, profession="Engineer")
```

🎯 Sizda foydalanuvchini ma’lumotlar bazasiga yozish funksiyasi bor. Har bir foydalanuvchi har xil ma’lumot yuborishi mumkin: faqat **ism**, yoki **ism + yoshi**, yoki hammasi.


```python
def save_user(**info):
    print("Yangi foydalanuvchi ma'lumotlari:")
    for key, value in info.items():
        print(f"{key}: {value}")
    print("✅ Saqlandi\n")

# Turli foydalanuvchilar turlicha ma'lumot yuboradi
save_user(name="Ali", age=25)
save_user(name="Laylo", phone="998901234567", email="laylo@mail.com")
```

## ✅ LAMBDA FUNKSIYALAR

📌 **lambda** — bu bir qatorli va tez yoziladigan funksiyalardir. Odatdagi def funksiyalarga o‘xshaydi, lekin juda sodda va qisqa ko‘rinishda yoziladi. Lambda funksiyalar odatda bir martalik, oddiy amallar uchun ishlatiladi (masalan: hisoblash, filtrlash, saralash).

```python
# 1. Sonni kvadratga ko‘tarish (x ** 2)
square = lambda x: x ** 2
print(square(6))  # 36

# 2. Ikkita sonni qo‘shish (x + y)
add = lambda x, y: x + y
print(add(3, 4))  # 7
```

🎯 Sizda bir nechta foydalanuvchi bor, ularni yosh bo‘yicha tartiblash kerak. Bunda lambda funksiyadan foydalanish mumkin.

```python
# Foydalanuvchilar (lug‘atlar ro‘yxati)
users = [
    {"name": "Ali", "age": 25},
    {"name": "Laylo", "age": 20},
    {"name": "Javohir", "age": 30},
]

# Yosh bo‘yicha tartiblash (lambda yordamida)
sorted_users = sorted(users, key=lambda user: user["age"])

# Natijani chiqaramiz
for user in sorted_users:
    print(f"{user['name']} - {user['age']} yosh")
```

## ✅ NESTED FUNCTIONS

📌 **Nested function** — bu bir funksiyaning ichida boshqa funksiya yaratish demakdir. Ichki funksiya (inner) faqat tashqi funksiya (outer) ichida mavjud bo‘ladi va tashqaridan chaqirib bo‘lmaydi. Bu usul kodni modullashtirish, xavfsizroq saqlash va faqat kerakli joyda ishlatish uchun qulay.

```python
def outer(x):  # Tashqi funksiya
    def inner(y):  # Ichki funksiya
        return y + 2  # Ichki funksiya 2 ni qo‘shadi
    return inner(x) * 2  # Inner natijasi 2 ga ko‘paytiriladi

result = outer(5)  # (5 + 2) * 2 = 14
print(result)  # 14
```

🎯 Siz foydalanuvchiga xush kelibsiz xabarini turli tillarda chiqarishni xohlaysiz.

```python
def greeting(language):
    def get_message(name):
        if language == "uz":
            return f"Salom, {name}!"
        elif language == "en":
            return f"Hello, {name}!"
        elif language == "ru":
            return f"Привет, {name}!"
        else:
            return f"Hi, {name}!"
    
    return get_message  # Ichki funksiyani qaytaramiz

# O‘zbekcha salomlashuv funksiyasi
salomlash_uz = greeting("uz")
print(salomlash_uz("Umid"))  # Salom, Umid!

# Inglizcha salomlashuv funksiyasi
salomlash_en = greeting("en")
print(salomlash_en("Umid"))  # Hello, Umid!
```

## ✅ RECURSIVE FUNCTIONS

📌 **Rekursiv funksiya** — bu o‘zini o‘zi ichida chaqiradigan funksiya. Bu usul, odatda takroriy (recursive) muammolarni hal qilish uchun ishlatiladi — masalan: faktorial, Fibonachchi, fayl strukturalari, daraxt ko‘rinishidagi ma’lumotlar va hokazo.

```python
def factorial(n):
    # Bazaviy holat: n 0 bo‘lsa, 1 ni qaytar
    if n == 0:
        return 1
    # Rekursiv chaqirish: n * factorial(n - 1)
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

🎯 Kompyuterdagi papkalar ichida yana papkalar bo‘lishi mumkin. Har bir darajadagi fayllarni hisoblash uchun rekursiya ishlatiladi (o‘rnatilgan os moduli orqali).

```python
import os

def count_files(folder_path):
    total = 0
    for item in os.listdir(folder_path):
        full_path = os.path.join(folder_path, item)
        if os.path.isdir(full_path):
            total += count_files(full_path)  # Ichki papkani tekshirish
        else:
            total += 1  # Fayl topildi
    return total

# Misol uchun: "/home/umid/hujjatlar"
print(count_files("/home/umid/hujjatlar"))
```

## ✅ TYPE ANNOTATION – TURINI KO‘RSATISH

📌 **Type annotation** — bu o‘zgaruvchilar, parametrlar va return (natija) uchun ma’lumot turini ko‘rsatish usulidir. Bu yordamida kod ancha tushunarli bo‘ladi, xatolarni aniqlash osonlashadi, IDE (VS Code, PyCharm) avtomatik tekshirish qiladi.


```python
def add_numbers(a: int, b: int) -> int:
    # a va b butun sonlar sifatida olinadi, natija ham int bo‘ladi
    return a + b

result: int = add_numbers(10, 20)
print(result)  # 30
```

🎯 Siz API orqali yangi foydalanuvchi yaratadigan funksiya yozmoqchisiz. Ushbu foydalanuvchining ismi, yoshi va faollik holati (True yoki False) bo‘lishi kerak.

```python
def create_user(name: str, age: int, active: bool) -> dict:
    return {
        "name": name,
        "age": age,
        "active": active
    }

user_info: dict = create_user("Umid", 25, True)
print(user_info)
```

## ✅ DOCSTRING

📌 Docstring (documentation string) — bu funksiya, klass yoki modul nima qilishini tavsiflab beruvchi matn. U funksiyaning birinchi qatorida uchta qo‘shtirnoq (""") bilan yoziladi. Maqsad: Funksiya qanday ishlaydi, qanday parametrlar oladi, va nima qaytaradi — bularni tushuntirish.

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

## ✅ HIGHER-ORDER FUNKSIYALAR

📌 **Higher-order function** — bu boshqa funksiyani argument sifatida qabul qiladigan yoki funksiya sifatida natijada qaytaradigan funksiyadir. Pythonda funksiyalar ham "obyekt" bo‘lgani uchun, ularni o‘zgaruvchiga berish, funksiyaga uzatish, yoki qaytarish mumkin.

```python
# apply_twice funksiyasi boshqa funksiya (func) va qiymat (value) oladi
def apply_twice(func, value):
    # func(value) chaqiriladi → natijasi yana func ga beriladi
    return func(func(value))

# increment funksiyasi bitta sonni 1 ga oshiradi
def increment(x):
    return x + 1

# apply_twice funksiyasiga increment funksiyasi va 5 soni uzatilmoqda
result = apply_twice(increment, 5)
print(result)  # 7 chiqadi, chunki: increment(increment(5)) → increment(6) → 7
```

## ✅ DECORATORS

📌 Dekorator — bu boshqa funksiyani o‘rab, unga qo‘shimcha imkoniyatlar qo‘shadigan higher-order funksiyadir. Asosiy funksiyani o‘zgartirmasdan unga funksional qo‘shish uchun ishlatiladi.

```python
def uppercase_decorator(func):
    # Ichki funksiyani yaratamiz
    def wrapper():
        result = func()          # Asosiy funksiyani chaqiramiz
        return result.upper()    # Natijani katta harflarga o‘zgartiramiz
    return wrapper               # wrapper funksiyasini qaytaramiz

@uppercase_decorator
def greet():
    return "hello"

print(greet())  # "HELLO"
```

🎯 APIda foydalanuvchini tekshirish (auth) uchun dekorator

```python
# login_required — bu dekorator funksiyasi bo‘lib, boshqa funksiyani argument sifatida qabul qiladi
def login_required(func):
    
    # Ichki wrapper funksiyasi — bu o‘ralgan yangi funksiya
    def wrapper():
        # Qo‘shimcha amal: foydalanuvchining login holatini tekshirish imitatsiyasi
        print("🔐 Foydalanuvchi login bo‘lganligini tekshiryapmiz...")
        
        # Asl funksiyani chaqiramiz (masalan: view_dashboard)
        return func()
    
    # wrapper funksiyasini qaytaramiz — ya’ni dekoratsiya qilingan yangi funksiya
    return wrapper


# Bu yerda view_dashboard funksiyasi login_required dekoratori bilan "bezanmoqda"
# Ya'ni, view_dashboard = login_required(view_dashboard)
@login_required
def view_dashboard():
    # Asl funksiyadagi ish: dashboard ochilishini bildiradi
    print("📊 Dashboard ochildi.")


# Endi bu chaqirilganda avval dekorator ishlaydi, keyin as
```

# ✅ AMALIYOT

## ✅ 1-topshiriq:
`hello()` nomli funksiya yozing, u chaqirilganda "Assalomu alaykum!" matnini chiqarsin.

---

## ✅ 2-topshiriq:
`to_square(x)` funksiyasini yozing, u argument sifatida berilgan sonning kvadratini qaytarsin.

---

## ✅ 3-topshiriq:
`multiply(a, b)` funksiyasini tuzing, u berilgan ikki sonning ko‘paytmasini qaytarsin.

---

## ✅ 4-topshiriq:
`say_hello(name)` funksiyasiga ism argumenti berilganda, "Salom, {ism}!" ko‘rinishida xabar chiqaring.

---

## ✅ 5-topshiriq:
`power(base, exponent=2)` funksiyasi uchun, exponent argumenti berilmasa, sonni kvadratga ko‘tarsin.

---

## ✅ 6-topshiriq:
`show_list(items)` funksiyasiga ro‘yxat berilganda, har bir elementni yangi qatordan chiqarsin.

---

## ✅ 7-topshiriq:
`print_line()` funksiyasi har chaqirilganda 40 ta "-" belgisi chiqarib bersin.

---

## ✅ 8-topshiriq:
`get_max(a, b)` funksiyasi ikki sonning kattasini qaytarsin.

---

## ✅ 9-topshiriq:
`sum_all(*numbers)` funksiyasi har qancha son qabul qilib, ularning yig‘indisini qaytarsin.

---

## ✅ 10-topshiriq:
`user_info(**kwargs)` funksiyasi kalit-qiymat juftliklarini qabul qilib, har birini alohida qatordan ko‘rsatsin.

---

## ✅ 11-topshiriq:
`ages = [19, 21, 17, 25]` ro‘yxatini lambda funksiyasi yordamida o‘sish tartibida sort qiling.

---

## ✅ 12-topshiriq:
`outer()` nomli funksiya yarating, uning ichida `inner()` funksiyasi bo‘lsin va `outer()` chaqirilganda natija qaytarsin.

---

## ✅ 13-topshiriq:
`factorial(n)` funksiyasini yozing, u n faktorialni hisoblab qaytarsin.

---

## ✅ 14-topshiriq:
`add_numbers(a: int, b: int) -> int` funksiyasi yarating, natijasini chop eting.

---

## ✅ 15-topshiriq:
`subtract(a, b)` funksiyasini yozing va unga tushuntiruvchi docstring yozing. Docstringni funksiyaning `__doc__` atributi orqali chop eting.

---