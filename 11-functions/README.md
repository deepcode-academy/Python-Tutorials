# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 11-DARS: FUNKSIYALAR (FUNCTIONS)

 📌 Python dasturlash tilida **funksiya** bu — kodni bir joyda yozib, ko‘p joylarda chaqirish, kodni tartibli va qisqa qilish uchun qulay vositadir. Funksiya yordamida kodni modullashtirish va takrorlanadigan qismni soddalashtirish mumkin.


## FUNKSIYA YARATISH (DEF)

```python
def greet():
    # Oddiy funksiya: salomlashish
    print("Hello, world!")
```

## FUNKSIYANI CHAQIRISH (CALLING A FUNCTION)

```python
greet()  # Funksiyani chaqirish natijasida "Hello, world!" chiqadi
```

## PARAMETRLAR (PARAMETERS) VA ARGUMENTLAR (ARGUMENTS)

```python
def add(a, b):
    # a va b parametrlar
    return a + b

result = add(2, 3)  # 2 va 3 argument sifatida uzatiladi
print(result)  # 5
```

## STANDART PARAMETRLAR (DEFAULT PARAMETERS)

```python
def power(base, exponent=2):
    # exponent uchun default qiymat 2
    return base ** exponent

print(power(3))      # 9 (3^2)
print(power(3, 3))   # 27 (3^3)
```

## QIYMAT QAYTARISH (RETURN)

```python
def multiply(x, y):
    return x * y  # Natija qaytariladi

product = multiply(4, 5)
print(product)  # 20
```

## HECH NIMA QAYTARMAYDIGAN FUNKSIYALAR (VOID FUNCTION)

```python
def print_welcome(name):
    print(f"Welcome, {name}!")  # Faqat ekranga chiqaradi, qiymat qaytarmaydi

print_welcome("Ali")
```

## QIYMAT QAYTARADIGAN FUNKSIYALAR (VALUE-RETURNING FUNCTION)

```python
def get_maximum(a, b):
    if a > b:
        return a
    else:
        return b

max_number = get_maximum(7, 10)
print(max_number)  # 10
```

## BIR NECHTA PARAMETRLAR BILAN ISHLASH

```python
def info(name, age, city):
    print(f"Name: {name}, Age: {age}, City: {city}")

info("Alice", 25, "Tashkent")
```

## FUNKSIYAGA RO‘YXAT (LIST) UZATISH

```python
def print_list(items):
    # Har bir elementni ekranga chiqaradi
    for item in items:
        print(item)

fruits = ["apple", "banana", "cherry"]
print_list(fruits)
```

## IXTIIYORIY ARGUMENTLAR: *ARGS

```python
def total_sum(*args):
    # args — tuple, istalgancha argument qabul qiladi
    return sum(args)

print(total_sum(1, 2, 3, 4, 5))  # 15
```

## KALITLI ARGUMENTLAR: **KWARGS

```python
def print_profile(**kwargs):
    # kwargs — dictionary, kalit so‘zli argumentlar qabul qiladi
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_profile(name="Bob", age=30, profession="Engineer")
```

## LAMBDA FUNKSIYALAR (QISQA FUNKSIYALAR)

```python
square = lambda x: x ** 2
print(square(6))  # 36

add = lambda x, y: x + y
print(add(3, 4))  # 7
```

## FUNKSIYALAR ICHIDA FUNKSIYALAR (NESTED FUNCTIONS)

```python
def outer(x):
    def inner(y):
        return y + 2
    return inner(x) * 2

result = outer(5)  # (5 + 2) * 2 = 14
print(result)  # 14
```

## REKURSIV FUNKSIYALAR (RECURSIVE FUNCTIONS)

```python
def factorial(n):
    # Bazaviy holat
    if n == 0:
        return 1
    # Rekursiv chaqirish
    return n * factorial(n - 1)

print(factorial(5))  # 120
```

## TYPE ANNOTATION – TURINI KO‘RSATISH

```python
def add_numbers(a: int, b: int) -> int:
    return a + b

result: int = add_numbers(10, 20)
print(result)  # 30
```

## DOCSTRING – FUNKSIYAGA HUJJAT YOZISH

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

## ICHKI (BUILT-IN) FUNKSIYALAR

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

## HIGHER-ORDER FUNKSIYALAR

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

## DEKORATORLAR (DECORATORS)

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