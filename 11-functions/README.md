# 🐍 PYTHON DASTURLASH ASOSLARI

## 🧩 11-DARS: FUNKSIYALAR (FUNCTIONS)

> **Eslatma:**  
> Python dasturlash tilida **funksiya** bu — kodni bir joyda yozib, ko‘p joylarda chaqirish, kodni tartibli va qisqa qilish uchun qulay vositadir. Funksiya yordamida kodni modullashtirish va takrorlanadigan qismni soddalashtirish mumkin.

---

## FUNKSIYA YARATISH VA CHAQIRISH

Pythonda funksiya yaratish uchun `def` kalit so‘zi ishlatiladi:

```python
def function_name(parameters):
    # Funksiya tanasi (bu yerda kodlar bo'ladi)
    # ...
    return value  # Natija qaytarish (ixtiyoriy)
```

**Oddiy misol:**

```python
def add_numbers(a, b):
    # a va b ni qo'shamiz
    result = a + b
    return result  # Natijani qaytaramiz

sum_result = add_numbers(3, 5)  # Funksiyani 3 va 5 argumentlari bilan chaqiramiz
print(sum_result)  # 8 chiqaradi
```

---

## PARAMETR VA ARGUMENTLAR

- **Parametr** — funksiya yaratilganda e'lon qilinadigan o‘zgaruvchilar.
- **Argument** — funksiya chaqirilganda parametrga uzatiladigan haqiqiy qiymat.

```python
def square_number(number):
    # number parametrining kvadratini hisoblaymiz va natijani qaytaramiz
    return number ** 2

result = square_number(5)  # 5 argument sifatida uzatiladi
print(result)  # 25 chiqaradi
```

---

## POSITIONAL VA KEYWORD ARGUMENTLAR

- **Positional (pozitsion) argumentlar:** tartib bo‘yicha uzatiladi
- **Keyword (kalit so‘zli) argumentlar:** parametr nomi bilan uzatiladi

```python
def multiply(a, b):
    # a va b ni ko'paytirib natijani qaytaramiz
    return a * b

result1 = multiply(2, 4)        # Pozitsion argumentlar: a=2, b=4
result2 = multiply(b=5, a=3)    # Kalit so'zli argumentlar: a=3, b=5
print(result1)  # 8
print(result2)  # 15
```

---

## QAYTISH QIYMATI (`return`)

Funksiya natijani `return` operatori yordamida qaytaradi. `return`dan keyingi kod bajarilmaydi.

```python
def power(base, exponent):
    # base ni exponent darajaga ko'taramiz va natijani qaytaramiz
    return base ** exponent

result = power(2, 3)  # 2^3 = 8
print(result)  # 8
```

---

## DEFAULT (STANDART) QIYMATLI PARAMETRLAR

Agar funksiya chaqirilganda ba’zi parametrlar uzatilmasa, u holda oldindan ko‘rsatilgan qiymat ishlatiladi.

```python
def greet(name="Friend"):
    # Agar name uzatilmasa, "Friend" ishlatiladi
    print(f"Hello, {name}!")

greet()          # Hello, Friend!
greet("Alice")   # Hello, Alice!
```

---

## *ARGS VA **KWARGS

Agar funksiya argumentlar soni oldindan noma’lum bo‘lsa, `*args` va `**kwargs` ishlatiladi.

- `*args` — turli sonli **pozitsion** argumentlarni tuple ko‘rinishida qabul qiladi.
- `**kwargs` — turli sonli **kalit so‘zli** argumentlarni dictionary ko‘rinishida qabul qiladi.

```python
def total_sum(*args):
    # args — tuple ko'rinishida barcha argumentlarni oladi
    return sum(args)

print(total_sum(1, 2, 3, 4))  # 10

def show_info(**kwargs):
    # kwargs — dictionary ko'rinishida barcha kalit-qiymatlarni oladi
    for key, value in kwargs.items():
        print(f"{key}: {value}")

show_info(name="Alice", age=22, city="Tashkent")
# name: Alice
# age: 22
# city: Tashkent
```

---

## LAMBDA FUNKSIYALARI

> **Lambda** — qisqa (bir qatorli) anonim funksiya. Ko‘pincha qisqa operatsiyalar uchun ishlatiladi.

```python
# Lambda funksiyasi: ikki sonni qo'shadi
sum_func = lambda x, y: x + y
result = sum_func(5, 3)
print(result)  # 8
```

**Def orqali xuddi shu funksiya:**

```python
def add(x, y):
    return x + y

result = add(5, 3)
print(result)  # 8
```

**Lambda funksiyalarni map, filter, sorted bilan ishlatish:**

```python
# map — har bir elementga amal bajaradi
numbers = [1, 2, 3, 4]
squares = list(map(lambda x: x ** 2, numbers))
print(squares)  # [1, 4, 9, 16]

# filter — shart bo'yicha elementlarni tanlaydi
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # [2, 4]

# sorted — tartiblashda lambda ishlatish
fruits = ["apple", "banana", "peach", "orange"]
sorted_fruits = sorted(fruits, key=lambda x: len(x))
print(sorted_fruits)  # ['peach', 'apple', 'banana', 'orange']
```

---

## ICHKI FUNKSIYA (FUNCTION INSIDE FUNCTION)

Funksiya ichida boshqa funksiya e'lon qilish mumkin — **ichki funksiya**.

```python
def outer_function(x):
    # Ichki funksiya
    def inner_function(y):
        # y ning kvadratini hisoblaydi
        return y ** 2
    # inner_function natijasiga 5 qo'shib qaytaradi
    return inner_function(x) + 5

result = outer_function(3)
print(result)  # 14
```

**Ichki funksiya afzalliklari:**
- Kapsulatsiya — kodni izolyatsiya qilish
- Kod takrorlanishini kamaytirish
- Murakkab funksiyalar uchun yordamchi funksiya sifatida

---

## FUNKSIYA ICHIDA LAMBDA QAYTARISH

Lambda funksiyani boshqa funksiya ichida qaytarish mumkin.

```python
def multiplier(factor):
    # Lambda funksiya factor ga ko'paytiradi
    return lambda x: x * factor

double = multiplier(2)  # double endi x2 ko'paytiradi
triple = multiplier(3)  # triple endi x3 ko'paytiradi

print(double(5))  # 10
print(triple(5))  # 15
```

---

## QISQA XULOSA

- Funksiya — kodni modular va qayta ishlatish uchun vosita.
- Parametrlar va argumentlar, pozitsion va kalit so‘zli argumentlar farqini biling.
- *args va **kwargs yordamida o‘zgaruvchan argumentlar bilan ishlang.
- Lambda qisqa va bir qatordan iborat funksiya uchun qulay.
- Ichki funksiyalar va lambda yordamida murakkab tuzilmalarni yaratish mumkin.

> **Amaliy mashq:**  
> Har bir misoldagi kodni o'zingiz yozib, qanday ishlashini tekshirib ko’ring va qatorlardagi izoh (comment)larni diqqat bilan o’qing.

## AMALIYOT
- Oddiy matematik funksiya:
    - Funksiya yarating, u ikkita sonni qabul qilib, ularni ko'paytirib qaytarsin. Agar foydalanuvchi son bermasa, ikkala son uchun standart qiymat 1 bo'lsin. <br>
    **Natija:**
    ```python
    print(kopaytirish(5, 3))  # Natija: 15
    print(kopaytirish())      # Natija: 1
    ```
- Salomlash funksiyasi:
    - Funksiya yarating, u ismni qabul qilsin va foydalanuvchiga `Salom, [ism]!` deb salomlashsin. Agar ism berilmasa, `Salom, Do'stim!` deb salomlashsin. <br>
    **Natija:**
    ```python
    print(salomlash("Ali"))  # Natija: Salom, Ali!
    print(salomlash())       # Natija: Salom, Do'stim!
    ```
- Sonlarning kvadratlari:
    - Funksiya yarating, u bir ro'yxat qabul qilib, har bir elementning kvadratini qaytarsin. Ro'yxatni `map()` va lambda funksiyasi yordamida qayta ishlang. <br>
    **Natija:**
    ```python
    print(kvadratlar([1, 2, 3, 4]))  # Natija: [1, 4, 9, 16]
    ```
- Juft sonlarni filtrlang:
    - Funksiya yarating, u ro'yxatdan faqat juft sonlarni ajratib qaytarsin. `filter()` va lambda funksiyasidan foydalaning. <br>
    **Natija:**
    ```python
    print(juft_sonlar([1, 2, 3, 4, 5, 6]))  # Natija: [2, 4, 6]
    ```
- Student ma'lumotlarini qaytaruvchi funksiya:
    - Funksiya yarating, u talabaning `ismi`, `yoshi`, va `kursini` qabul qilib, bu ma'lumotlarni tartiblangan ko'rinishda qaytarsin. `**kwargs` dan foydalaning. <br>
    **Natija:**
    ```python
    talaba_ma'lumotlari(ism="Ali", yosh=21, kurs="Python")
    # Natija:
    # ism: Ali
    # yosh: 21
    # kurs: Python
    ```