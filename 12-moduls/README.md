# PYTHON DASTURLASH ASOSLARI

# 🧩 12-dars Modullar

## ✅ MODUL NIMA?
📌 Modul — bu Python fayli bo‘lib, u ichida `funksiyalar`, `classlar`, `o‘zgaruvchilar`, yoki boshqa Python kodlari saqlanadi.

📌 Modulning asosiy vazifasi — kodni bo‘laklarga ajratish, tartibli saqlash va boshqa joylarda qayta ishlatish imkonini berish.

## ✅ MODUL KERAKMI? NIMA FOYDA?

📌 **Quyidagi sabablarga ko‘ra modul foydali:**

- **Kod takrorlanmasligi** — bir marta yozilgan kodni istalgan joyda qayta ishlatish mumkin.
- **Kodlarni guruhlash** — o‘xshash funksiyalar bitta faylga to‘plansa, ularni boshqarish oson bo‘ladi.
- **Katta dasturlarni boshqarish osonlashadi** — har bir qism alohida modul bo‘lsa, tuzilma soddalashadi.
- **Test qilish oson** — modulni alohida sinab ko‘rish mumkin.


## ✅ MODULLARNI import QILISH
📌 Pythonda modullardan foydalanish uchun avvalo ularni `import` qilish kerak. Modullarni **import** qilish uchun `import` kalit so'zidan foydalaniladi.

```python
# Dasturga tashqi yoki ichki modulni ulash (import qilish) uchun ishlatiladi
# 'modul_nomi' o‘rniga kerakli modul nomi yoziladi (masalan: math, random, datetime va h.k.)
import modul_nomi
```

📌 `math` modulini `import` qilish
```python
# 'math' modulini import qilamiz, bu modulda matematik funksiyalar mavjud
import math

# Aylananing radiusi 5 ga teng deb belgilaymiz
radius = 5

# Aylana yuzini hisoblaymiz: π * r^2 formulasi asosida
yuza = math.pi * radius**2

# Hisoblangan aylana yuzini ekranga chiqaramiz
print(f"Aylana yuzi: {yuza}")
```

## ✅ MODULLARDAN MUAYYAN QISMLARNI IMPORT QILISH

📌`from modul_nomi import funksiya_yoki_object` sintaksisi yordamida siz ma'lum bir moduldan faqat kerakli `funksiya` yoki `o'zgaruvchini` import qilishingiz mumkin. Bu sizga modulni to'liq import qilmasdan, faqat zaruriy qismlarini olish imkonini beradi.

```python
# Belgilangan modul ichidan faqat kerakli funksiya yoki obyektni import qilish uchun ishlatiladi
# 'modul_nomi' – bu modul nomi (masalan: math, random, datetime)
# 'funksiya_yoki_object' – modul ichidagi aniq bir funksiya, klass yoki o‘zgaruvchi nomi
from modul_nomi import funksiya_yoki_object
```
📌 `math` modulidan `sqrt` funksiyasini import qilish

```python
# 'math' modulidan faqat 'sqrt' (kvadrat ildiz) funksiyasini import qilamiz
from math import sqrt

# Kvadrat ildizi olinadigan sonni belgilaymiz
son = 16

# Berilgan sonning kvadrat ildizini hisoblaymiz
ildiz = sqrt(son)

# Natijani ekranga chiqaramiz
print(f"{son} ning kvadrat ildizi: {ildiz}")
```

## ✅ MODULGA BOSHQA NOM BERISH
📌 Modulni import qilishda unga qisqa yoki qulayroq nom berish uchun `as` operatoridan foydalanishingiz mumkin.

```python
# 'math' modulini 'm' degan qisqa nom bilan import qilamiz
import math as m

# Aylananing radiusini belgilaymiz
radius = 7

# Aylananing diametrini hisoblaymiz: D = 2 * π * r formulasi bo‘yicha
diametr = 2 * m.pi * radius

# Hisoblangan diametrni ekranga chiqaramiz
print(f"Aylananing diametri: {diametr}")
```

## ✅ MODUL YARATISH
📌 Modul yaratish uchun asosiy dasturimizdagi funksiyalarni yangi faylga ko'chiramiz xolos. Modulga oson murojat qilishimiz uchun, faylimiz asosiy dasturimiz bilan bitta papkada bo'lishi kerak. Bunda adashib ketmaslik uchun, loyihangizning(dasturning) asosiy faylini `main.py` deb nomlash o'rinli. 

```python
# mymodule.py - Bu modulda funksiyalar va klasslar jamlangan

# Salomlashish uchun funksiya
def greet(name):
    """Salomlashish funktsiyasi."""
    return f"Salom, {name}!"

# Ikki sonni qo‘shish funksiyasi
def add(a, b):
    """Ikki sonni qo'shish funktsiyasi."""
    return a + b

# Ikki sonni ko‘paytirish funksiyasi
def multiply(a, b):
    """Ikki sonni ko'paytirish funktsiyasi."""
    return a * b

# Shaxslarni ifodalovchi klass
class Person:
    """Shaxs klassi."""
    
    # Klassni ishga tushiruvchi konstruktor
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    # Shaxs haqida tanishtiruvchi metod
    def introduce(self):
        """Shaxsni tanishtiruvchi metod."""
        return f"Men {self.name} va {self.age} yoshdaman."
```

## ✅MODULDAN FOYDALANISH
📌 `Modul` yaratganingizdan so'ng, uni boshqa Python dasturlarida `import` qilib ishlatishingiz mumkin.

```python
# mymodule modulini import qilamiz, undagi funksiyalar va klasslardan foydalanish uchun
import mymodule

# greet funksiyasini chaqirib, "Ali" ga salom beramiz
print(mymodule.greet("Ali"))

# add funksiyasi yordamida 5 va 3 sonlarini qo‘shamiz va natijani chiqaramiz
print(mymodule.add(5, 3))

# multiply funksiyasi yordamida 4 va 7 sonlarini ko‘paytiramiz va natijani chiqaramiz
print(mymodule.multiply(4, 7))

# Person klassidan yangi obyekt yaratamiz, ism va yoshni beramiz
person = mymodule.Person("Omar", 25)

# obyektning introduce metodini chaqirib, tanishtirish matnini chiqaramiz
print(person.introduce())
```
## ✅ MODULNI KENGAYTIRISH
📌 Modulga qo'shimcha funksiyalar yoki klasslar qo'shishingiz mumkin.


```python
# Ikki sondan birini ayirish funksiyasi
def subtract(a, b):
    """Ikki sondan birini ayirish funktsiyasi."""
    return a - b

# Ikki sonni bo'lish funksiyasi
def divide(a, b):
    """Ikki sonni bo'lish funktsiyasi."""
    if b == 0:
        # Agar bo‘luvchi 0 bo‘lsa, xatolik chiqaramiz
        raise ValueError("Bo'lish uchun 0 bilan bo'lish mumkin emas!")
    return a / b
```

## ✅ FOYDALI MODULLAR
### SANA VA VAQT BILAN ISHLASH UCHUN

- `datetime` moduli sana va vaqt bilan ishlash uchun juda foydali. Ushbu modul quyidagi asosiy komponentlarni o'z ichiga oladi:
- **datetime:** Sana va vaqtni ifodalovchi obyektlar yaratish uchun.
- **date:** Faqat sana ma'lumotini ifodalash uchun.
- **time:** Faqat vaqt ma'lumotini ifodalash uchun.
- **timedelta:** Sana yoki vaqt o'rtasidagi farqni ifodalash uchun.
- **timezone:** Soat zonalarini boshqarish uchun.

1. `datetime` - sana va vaqtni ifodalash uchun ishlatiladi:
```python
from datetime import datetime

# Hozirgi sana va vaqtni olish
now = datetime.now()
print(now)  # 2024-08-19 14:30:00.123456

# Sana va vaqtni formatlash
formatted = now.strftime("%Y-%m-%d %H:%M:%S")
print(formatted)  # 2024-08-19 14:30:00
```
2. `date` - faqat sana ma'lumotini saqlaydi:
```python
from datetime import date

# Hozirgi sanani olish
today = date.today()
print(today)  # 2024-08-19

# Sana obyektini yaratish
specific_date = date(2024, 8, 19)
print(specific_date)  # 2024-08-19
```
3. `time` - faqat vaqt ma'lumotlarini saqlaydi:
```python
from datetime import time

# Vaqt obyektini yaratish
specific_time = time(14, 30, 45)
print(specific_time)  # 14:30:45
```
4. `timedelta` - ikki sana yoki vaqtni o'rtasidagi farqni ifodalash uchun ishlatiladi:
```python
from datetime import datetime, timedelta

# Hozirgi sana va vaqt
now = datetime.now()

# 5 kun qo'shish
future_date = now + timedelta(days=5)
print(future_date)

# 5 kun oldingi sana
past_date = now - timedelta(days=5)
print(past_date)
```
5. `timezone` - soat zonalarini boshqarish uchun ishlatiladi:
```python
from datetime import datetime, timedelta

# Hozirgi sana va vaqt
now = datetime.now()

# 5 kun qo'shish
future_date = now + timedelta(days=5)
print(future_date)

# 5 kun oldingi sana
past_date = now - timedelta(days=5)
print(past_date)
```


