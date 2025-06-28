# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 13-DARS MODULS

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
📌 Modul yaratganingizdan so'ng, uni boshqa Python dasturlarida `import` qilib ishlatishingiz mumkin.

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

### 📌 [math MODULI](https://docs.python.org/3/library/math.html)

### ✅ NIMA UCHUN FOYDALI?

- Matematik hisob-kitoblarni oson va aniq bajarish uchun kerak.
- Kvadrat ildiz, logarifm, trigonometrik funksiyalar, faktoriyal kabi ko‘plab matematik operatsiyalarni bajarish imkonini beradi.
- Dasturlashda murakkab matematik formulalarni ishlatishda yordam beradi.

### 1. `math.ceil(x)` 

📌 `x` sonini yuqoriga qarab yaxlitlaydi. Ya'ni, agar son butun emas bo‘lsa, keyingi eng yaqin butun songa oshiradi. Agar son butun bo‘lsa, o‘zi o‘zgarmaydi.

```python
# 'math' modulini import qilamiz
import math

# 5.1 sonini yuqoriga qarab butun songa yaxlitlaymiz (ceil funksiyasi)
print(math.ceil(5.1))   # Natija: 6

# 5.9 sonini yuqoriga qarab butun songa yaxlitlaymiz
print(math.ceil(5.9))   # Natija: 6

# Manfiy -3.4 sonini yuqoriga qarab yaxlitlaymiz (-3.4 dan katta eng kichik butun son -3)
print(math.ceil(-3.4))  # Natija: -3  

# 7 allaqachon butun son, shuning uchun o‘zgarmaydi
print(math.ceil(7))     # Natija: 7  
```

### 2. `math.floor(x)`

📌 `x` sonini pastga qarab yaxlitlaydi. Ya'ni, agar son butun emas bo‘lsa, oldingi eng yaqin butun songa tushiradi. Agar son butun bo‘lsa, o‘zi o‘zgarmaydi.

```python
# 'math' modulini import qilamiz
import math

# 5.9 sonini pastga qarab butun songa yaxlitlaymiz (floor funksiyasi)
print(math.floor(5.9))    # Natija: 5

# 5.1 sonini pastga qarab butun songa yaxlitlaymiz
print(math.floor(5.1))    # Natija: 5

# Manfiy -3.4 sonini pastga qarab yaxlitlaymiz (-3.4 dan kichik eng katta butun son -4)
print(math.floor(-3.4))   # Natija: -4  

# 7 allaqachon butun son, shuning uchun o‘zgarmaydi
print(math.floor(7))      # Natija: 7  
```

### [random MODULI](https://www.w3schools.com/python/module_random.asp)

📌 `random` moduli — bu Python kutubxonasi bo‘lib, u yordamida tasodifiy sonlar, tasodifiy elementlar tanlash va ro‘yxatlarni aralashtirish mumkin.

### ✅ NIMA UCHUN FOYDALI?

- O'yinlarda qahramonlar yoki voqealar uchun tasodifiylik yaratish uchun,
- Testlarda tasodifiy savollar tanlash uchun,
- Statistik tadqiqotlarda namuna olish uchun ishlatiladi.
- Shuningdek, har xil dasturlarda tasodifiy natijalar yaratishda qo‘llaniladi.

### 1. `random.randint(a, b)`

📌 `a` va `b` orasidagi tasodifiy butun sonni qaytaradi (a va b ham shu oraliqqa kiradi).

```python
# random modulini import qilamiz, bu modul tasodifiy sonlar bilan ishlash uchun kerak
import random

# 1 dan 10 gacha (ikkala chegarani ham qo'shib) tasodifiy butun son hosil qilamiz
son = random.randint(1, 10)

# Hosil qilingan tasodifiy sonni ekranga chiqaramiz
print(son)  # 1 dan 10 gacha bo'lgan butun son (masalan, 3, 7, 10 va hokazo)
```

### 2. `random.choice(sequence)`

📌 Berilgan ketma-ketlik (list, string yoki boshqa iterable) ichidan tasodifiy bitta elementni tanlaydi.

```python
# random modulini import qilamiz, tasodifiy element tanlash uchun kerak bo‘ladi
import random

# Mevalar ro‘yxatini yaratamiz
mevalar = ['olma', 'banan', 'anor', 'shaftoli']

# Ro‘yxatdan tasodifiy bitta meva tanlaymiz
tasodifiy_meva = random.choice(mevalar)

# Tanlangan mevaning nomini ekranga chiqaramiz
print(tasodifiy_meva)  # masalan, 'anor' yoki 'banan' chiqishi mumkin
```

### 3. `random.shuffle(list)`

📌 List elementlarini joyini tasodifiy tarzda almashtiradi (listni o‘zgartiradi).

```python
# random modulini import qilamiz, ro'yxat elementlarini aralashtirish uchun kerak
import random

# Raqamlar ro'yxatini yaratamiz
raqamlar = [1, 2, 3, 4, 5]

# Ro'yxatdagi elementlarni tasodifiy tartibda aralashtiramiz
random.shuffle(raqamlar)

# Aralashtirilgan ro'yxatni ekranga chiqaramiz
print(raqamlar)  # ro'yxat elementlari aralashadi, masalan, [3, 1, 5, 2, 4]
```

### [datetime MODULI](https://www.w3schools.com/python/python_datetime.asp)

📌 `datetime` moduli - Python kutubxonasi bo‘lib, sana va vaqt bilan ishlash uchun ishlatiladi. 

### ✅ NIMA UCHUN FOYDALI?

- Vaqtni hisoblash (masalan, ikki sana orasidagi farqni topish)
- Hozirgi vaqtni olish
- Sanalarni formatlash va ko‘rsatish
- Muddatlarni qo‘shish yoki ayirish.

### 1. `datetime.date.today()`

📌 Hozirgi kundagi sanani qaytaradi (faqat sana, vaqt emas).

```python
# datetime modulini import qilamiz, vaqt va sana bilan ishlash uchun kerak
import datetime

# Hozirgi sanani olish uchun today() funksiyasidan foydalanamiz
bugun = datetime.date.today()

# Olingan sanani ekranga chiqaramiz, masalan: 2025-06-06
print(bugun)  # masalan, 2025-06-06
```

### 2. `datetime.datetime.now()`

📌 Hozirgi sanani va vaqtni to‘liq qaytaradi (soat, daqiqa, soniya bilan).

```python
# datetime modulini import qilamiz, sana va vaqt bilan ishlash uchun kerak
import datetime

# Hozirgi sana va vaqtni olish uchun now() funksiyasidan foydalanamiz
hozir = datetime.datetime.now()

# Olingan sana va vaqtni ekranga chiqaramiz, masalan: 2025-06-06 15:30:25.123456
print(hozir)  # masalan, 2025-06-06 15:30:25.123456
```

### 3. `datetime.timedelta(days=5)`

📌 Vaqt oralig‘ini ifodalaydi. Masalan, 5 kun yoki 2 soat kabilarni yaratadi.

```python
# datetime modulini import qilamiz, sana va vaqt bilan ishlash uchun kerak
import datetime

# timedelta obyektini yaratamiz, bu 5 kunlik vaqt farqini ifodalaydi
besh_kun = datetime.timedelta(days=5)

# Hozirgi sanani olamiz
bugun = datetime.date.today()

# Bugungi sanaga 5 kun qo'shamiz, natijada kelasi sana hosil bo'ladi
kelasi_sana = bugun + besh_kun

# Kelasi sanani ekranga chiqaramiz
print(kelasi_sana)  # bugun sanadan 5 kun keyingi sana chiqadi
```

### 📌 [os MODULI](https://www.w3schools.com/python/module_os.asp)

`os moduli` — bu Python kutubxonasi bo‘lib, u orqali operatsion tizim bilan bog‘liq amallarni bajarish mumkin.

### ✅ NIMA UCHUN FOYDALI?

- Fayllar va papkalar ustida amallar bajarish (yaratish, o‘chirish, ko‘rish)
- Biz ishlab turgan papkani yo'lini aniqlash
- Papka va fayllar bilan dastur orqali interaktiv ishlash

### 1. `os.getcwd()`

📌 Biz ishlab turgan papkani (working directory) yo‘lini qaytaradi.

```python
# os modulini import qilamiz, operatsion tizim bilan bog‘liq funksiyalar uchun kerak
import os

# Hozirgi ishchi papkaning (current working directory) yo‘lini olamiz
papka = os.getcwd()

# Olingan papka yo‘lini ekranga chiqaramiz, masalan: /home/username/projects
print(papka)  # Masalan: /home/username/projects
```

### 2. `os.listdir(path)`

📌 Berilgan papka ichidagi barcha fayl va papkalar ro‘yxatini beradi.

```python
# os modulini import qilamiz, operatsion tizim bilan ishlash uchun kerak
import os

# Hozirgi papkadagi barcha fayl va papkalar ro'yxatini olamiz
fayllar = os.listdir('.')  # '.' bu hozirgi ishlab turgan papkani bildiradi

# Olingan fayl va papkalar ro'yxatini ekranga chiqaramiz
print(fayllar)  # Masalan: ['file1.txt', 'image.png', 'folder1']
```

### 3. `os.mkdir(name)`

📌 Yangi papka yaratadi.

```python
# os modulini import qilamiz, operatsion tizim bilan ishlash uchun kerak
import os

# 'yangi_papka' nomli yangi papka yaratamiz (agar mavjud bo'lmasa)
os.mkdir('yangi_papka')

# Papka yaratilib bo‘lgani haqida xabar beramiz
print("Yangi papka yaratildi")
```

### 3. `os.remove(filename)`

📌 Faylni o‘chiradi.

```python
# os modulini import qilamiz, fayllar va papkalar bilan ishlash uchun kerak
import os

# 'eskifayl.txt' nomli faylni o'chiramiz (agar mavjud bo'lsa)
os.remove('old_file.txt')

# Fayl muvaffaqiyatli o'chirilgani haqida xabar beramiz
print("Fayl o'chirildi")
```

### 📌 [json MODULI](https://www.w3schools.com/python/python_json.asp)

📌 `json moduli` — bu Python kutubxonasi bo‘lib, `JSON` formatidagi ma’lumotlar bilan ishlash uchun ishlatiladi. `JSON` — bu ma’lumotlarni yozish va uzatishda keng qo‘llaniladigan standart format.
Web dasturlashda, `API` (Application Programming Interface) lar bilan ishlashda juda muhim.

### ✅ NIMA UCHUN FOYDALI?

- JSON formatidagi ma’lumotlarni Python obyektlariga o‘qish,
- Python obyektlarini JSON formatiga yozish,
- API dan kelgan JSON javoblarini qayta ishlash,
- Ma’lumotlarni faylga JSON formatida saqlash va o‘qish.

### `json.loads(s)`

📌 JSON ko‘rinishidagi satrni Python obyektiga (list, dictionary va boshqalar) aylantiradi.

```python
# json modulini import qilamiz, JSON formatidagi ma'lumotlarni o'qish va yozish uchun kerak
import json

# JSON formatidagi satrni yaratamiz (string ko'rinishida)
json_satr = '{"ism": "Umid", "yosh": 25}'

# json.loads() funksiyasi yordamida JSON stringlarni Python dictionaryga aylantiramiz
python_obj = json.loads(json_satr)

# Python lug'atini ekranga chiqaramiz
print(python_obj)  # {'ism': 'Umid', 'yosh': 25}

# Dictionarydan 'ism' kalitiga mos keluvchi qiymatni chiqaramiz
print(python_obj['ism'])  # Umid
```

### 2. `json.dumps(obj)`

📌 Python obyektini JSON formatidagi stringga aylantiradi.

```python
# json modulini import qilamiz, JSON formatiga o‘tkazish va o‘qish uchun kerak
import json

# Python dictionary yaratamiz
python_obj = {'ism': 'Umid', 'yosh': 25}

# json.dumps() yordamida Python dictionaryni JSON formatidagi stringga aylantiramiz
json_satr = json.dumps(python_obj)

# JSON formatidagi stringni ekranga chiqaramiz
print(json_satr)  # '{"ism": "Umid", "yosh": 25}'
```

### 3. `json.load(file)`

📌 JSON faylini o‘qiydi va Python obyektiga aylantiradi.

```python
# json modulini import qilamiz, JSON fayllarni o'qish va yozish uchun kerak
import json

# 'data.json' faylini o'qish uchun ochamiz ('r' - read rejimi)
with open('data.json', 'r') as fayl:
    # fayldagi JSON ma'lumotlarni Python obyektiga (masalan, dictionary) o‘qiymiz
    malumot = json.load(fayl)

# Olingan ma'lumotni ekranga chiqaramiz
print(malumot)
```

### 4. `json.dump(obj, file)`

📌 Python obyektini JSON faylga yozadi.

```python
# json modulini import qilamiz, JSON formatida yozish va o'qish uchun kerak
import json

# Python dictionary yaratamiz, uni JSON formatida faylga yozamiz
data = {'ism': 'Umid', 'yosh': 25}

# 'data.json' faylini yozish uchun ochamiz ('w' - write rejimi)
with open('data.json', 'w') as fayl:
    # Python dictionaryni JSON formatida faylga yozamiz
    json.dump(data, fayl)
```

# ✅ AMALIYOT

## ✅ 1-topshiriq:
`math` modulidan foydalanib, 10 ta sonning kvadrat ildizini hisoblovchi dastur yozing va natijalarni chiqaring.

---

## ✅ 2-topshiriq:
`random` modulidan foydalanib, 1 dan 100 gacha bo‘lgan 5 ta tasodifiy butun sonlarni ro‘yxatga joylashtiring va ularni ekranga chiqaring.

---

## ✅ 3-topshiriq:
`datetime` modulidan foydalanib, bugungi sanani va vaqtni formatlangan holda `YYYY-MM-DD HH:MM:SS` ko‘rinishida ekranga chiqaring.

---

## ✅ 4-topshiriq:
O‘zingizning kichik modul faylingizni yarating (`mycalc.py`) va unga `add(a, b)`, `subtract(a, b)`, `multiply(a, b)`, `divide(a, b)` funksiyalarini yozing. Keyin ularni boshqa dasturga import qilib, natijalarni ko‘rsating.

---

## ✅ 5-topshiriq:
`math` modulidan `pi` va `sin` funksiyalarini import qilib, 0 dan π gacha bo‘lgan 5 ta qiymat uchun sinuslarini hisoblab chiqaring.

---

## ✅ 6-topshiriq:
`random.choice()` funksiyasi yordamida ro‘yxatdan tasodifiy 3 ta ism tanlab, ularni ekranga chiqaring.

---

## ✅ 7-topshiriq:
`random.shuffle()` yordamida berilgan ro‘yxat elementlarini aralashtiring va natijani chop eting.

---

## ✅ 8-topshiriq:
`datetime` modulidan foydalanib, foydalanuvchidan yil, oy, kun kiritishini so‘rang va shu sanani `datetime.date` obyekti sifatida saqlang.

---

## ✅ 9-topshiriq:
Yangi modul yarating, unga `greet(name)` funksiyasini yozing, u berilgan ismga salom beradi. Modulni import qilib, turli ismlar bilan chaqiring.

---

## ✅ 10-topshiriq:
`math` modulining `ceil` va `floor` funksiyalarini import qilib, foydalanuvchi kiritgan haqiqiy son uchun ikkala qiymatni ham chiqaring.

---

## ✅ 11-topshiriq:
O‘z modulingizda yangi funksiya yarating — `is_even(number)` — son juft yoki toqligini tekshiradi va `True` yoki `False` qaytaradi. Modulni import qilib, ro‘yxatdagi sonlarni tekshiring.

---

## ✅ 12-topshiriq:
`random` modulidan foydalanib, 52 ta kartadan iborat ro‘yxat yarating (masalan: "Queen of Hearts", "10 of Diamonds", va hokazo), keyin tasodifiy 5 ta kartani tanlab chiqaring. (Diamonds, Hearts, Clubs, Spades)

---

## ✅ 13-topshiriq:
`datetime` modulidan hozirgi vaqtni olib, uni soat, daqiqa va sekundga ajratib chiqaradigan dastur yozing.

---

## ✅ 14-topshiriq:
Modulga yangi funksiyalar qo‘shing: `factorial(n)` va `is_prime(n)`, ularni o‘zingiz yozing (modulda) va keyin asosiy dasturda chaqiring.

---

## ✅ 15-topshiriq:
`math` modulidan `pow` funksiyasini import qilib, foydalanuvchidan asosi va darajani qabul qilib, natijani hisoblang.
