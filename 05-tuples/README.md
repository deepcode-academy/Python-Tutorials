# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 5-DARS TUPLES


📌 Tuple — bu Pythonda bir nechta ma’lumotni bitta o‘zgaruvchida saqlash uchun ishlatiladigan o‘zgarmas tuzilma. U dumaloq qavs ichida yoziladi va elementlar vergul bilan ajratiladi. Tuple yaratilgach, uning ichidagi qiymatlarni o‘zgartirib, o‘chirib yoki yangisini qo‘shib bo‘lmaydi. Undagi ma’lumotlar tartib bilan saqlanadi va indeks orqali chaqiriladi. Tuple listga o‘xshaydi, lekin o‘zgarmasligi bilan farq qiladi. U dasturda tezroq ishlaydi va kamroq xotira egallaydi. O‘zgarmas ma’lumotlarni xavfsiz saqlash uchun tuple juda qulay.


## ✅ TUPLE XUSUSIYATLARI

📌 **O‘zgarmaydi:** Tuple yaratilgandan keyin uning ichidagi ma’lumotlarni o‘zgartirib bo‘lmaydi. Masalan, yangi element qo‘shib yoki mavjudini o‘chirib bo‘lmaydi. Bu degani — tuple ichidagi ma’lumotlar doim bir xil bo‘lib qoladi.

📌 **Tartibli:** Tuple ichida ma’lumotlar tartib bilan saqlanadi. Har bir element o‘z o‘rniga ega. Siz bu o‘rinni raqam bilan chaqirishingiz mumkin (masalan: birinchi element, ikkinchi element va hokazo).

📌 **Har xil turdagi ma’lumot bo‘lishi mumkin:** Tuple ichida sonlar, matnlar, True/False qiymatlar yoki boshqa turdagi ma’lumotlar aralash bo‘lishi mumkin. Bularni bir joyda saqlash imkonini beradi.

📌 **Tez ishlaydi:** Tuple — kompyuter uchun engil va tez tuzilma. Dastur ishlaganda tuplelar ro‘yxatlarga qaraganda tezroq ishlaydi va kam xotira ishlatadi.

📌 **O‘zgarmaydigan ma’lumotlar uchun qulay:** Agar sizda haftaning kunlari, oylar nomi, davlatlar ro‘yxati kabi o‘zgarmas ma’lumotlar bo‘lsa, tuple juda foydali bo‘ladi.


## ✅ TUPLE VA LIST FARQI

|Feature|Tuple|List|
|-------|-----|----|
|O'zgarishi mumkinmi?|Yo'q(**immutable**)|Ha(**mutable**)|
|Tezligi|Tezroq|Sekinroq|
|Qavs turi|**()**|**[]**|
|Xotira sarfi|Kamroq|Ko'proq|
|Qo'llanilish holati|O'zgarmas ma'lumotlar uchun|O'zgaruvchi ma'lumotlar uchun|



## ✅ TUPLE YARATISH


### ❇️ ODDIY TUPLE YARATISH

```python
# Uchta meva nomini o‘z ichiga olgan tuple yaratamiz
fruits = ("apple", "banana", "cherry")

# fruits tuple ichidagi barcha elementlarni ekranga chiqaramiz
print(fruits)
```

### ❇️ BITTA E'LEMENTLI TUPLE YARATISH

```python
# Faqat bitta elementdan iborat tuple yaratamiz
# E’tibor bering, oxirida vergul qo‘yilishi shart
single_fruit = ("apple",)

# Bitta elementli tuple ni ekranga chiqaramiz
print(single_fruit)



# ❌ Bu tuple emas (string bo‘lib qoladi)

# Bu yerda vergul yo‘q, shuning uchun bu oddiy string bo‘ladi
not_a_tuple = ("apple")

# O‘zgaruvchi turi (type) ni tekshiramiz
print(type(not_a_tuple))  # <class 'str'>
```

## ✅ TUPLE E'LEMENTLARIGA MUROJAT QILISH

📌 Tuple ichidagi har bir element tartib bilan joylashgan va ularga **indekslar** orqali murojaat qilish mumkin. Hisoblash **0** dan boshlanadi, ya’ni birinchi elementning indeksi **0** bo‘ladi. Bu xuddi listdagi kabi ishlaydi.

```python
# Bu yerda 5 ta elementdan iborat tuple yaratilmoqda
my_tuple = (10, 20, 30, 40, 50)

# [0] — bu birinchi elementga murojaat, indeks 0 dan boshlanadi
print(my_tuple[0])  # 10

# [2] — bu uchinchi elementga murojaat (0 - 1 - 2), qiymati 30
print(my_tuple[2])  # 30

# [-1] — bu oxirgi elementga murojaat, -1 doimo oxirgi elementni bildiradi
print(my_tuple[-1])  # 50
```

## ✅ TUPLE USTIDA AMALLAR

📌 Tuple — bu o‘zgarmas ma’lumot turi. Ya’ni, yaratilgach, uning ichidagi qiymatlarni o‘zgartirib, o‘chirib yoki yangisini qo‘shib bo‘lmaydi.

- Lekin, siz tuple bilan ikkita amalni bemalol bajara olasiz:
    - Tuplelarni birlashtirish
    - Tupleni takrorlash


### ✳️ + OPERATORI

📌 Bu usulda ikkita tuple birga qo‘shiladi va yangi tuple hosil bo‘ladi. Asl tuplelar o‘zgarmaydi.

```python
# Birinchi tuple
tuple1 = (1, 2)

# Ikkinchi tuple
tuple2 = (3, 4)

# Ikkalasini birlashtiramiz va yangi tuple hosil qilamiz
new_tuple = tuple1 + tuple2

# Natijani chiqaramiz
print(new_tuple)  # (1, 2, 3, 4)
```

❗ Yuqorida `tuple1` va `tuple2` o‘zgarmagan holda qoladi, faqat `+` orqali ularning qiymatlari birga qo‘shilib, `new_tuple` degan yangi tuple yaratiladi.

### ✳️ TAKRORLASH

📌 Agar bir tuple ni o‘zini o‘ziga birlashtirmoqchi bo‘lsangiz, uni yana o‘zi bilan `+` orqali birlashtirasiz.

```python
# Asl tuple
tuple1 = (1, 2, 3)

# O‘z-o‘ziga birlashtirish (ikki marta yozilgan bo‘ladi)
result = tuple1 + tuple1

# Natijani chiqaramiz
print(result)  # (1, 2, 3, 1, 2, 3)
```

### ❇️ TUPLENI KO'PAYTIRISH (TAKRORLASH)

📌 Tuple o‘zgarmas bo‘lsa ham, uni bir nechta marta takrorlab yangi tuple yaratish mumkin. Buning uchun `*` operatoridan foydalaniladi.

```python
# Bitta elementdan iborat tuple yaratilmoqda
tuple1 = ("hello",)

# Bu tuple 3 marta takrorlanmoqda
new_tuple = tuple1 * 3

# Natijada yangi tuple hosil bo‘ladi
print(new_tuple)  # ('hello', 'hello', 'hello')
```

### ❇️ TUPLE UZUNLIGINI ANIQLASH

📌 Tuple ichida nechta element borligini bilish uchun `len()` funksiyasidan foydalaniladi. Bu funksiya tuple uzunligini, ya’ni elementlar sonini qaytaradi.

```python
# 5 ta elementdan iborat tuple yaratilmoqda
my_tuple = (1, 2, 3, 4, 5)

# len() funksiyasi tuple ichidagi elementlar sonini hisoblaydi
print(len(my_tuple))  # 5
```

### ❇️ in OPERATORI

📌 in operatori yordamida biror qiymat tuple ichida bor yoki yo‘qligini tekshirish mumkin. Natija True yoki False ko‘rinishida chiqadi.

```python
# Mevalar saqlangan tuple yaratilmoqda
my_tuple = ("apple", "banana", "cherry")

# "banana" tuple ichida bormi? degan savolga javob tekshirilmoqda
print("banana" in my_tuple)  # True
```

### ❇️ TUPLENI QIYMATLARGA AJRATISH(`Unpacking`)

📌 Tuple ichidagi har bir qiymatni alohida o‘zgaruvchiga ajratib olish mumkin. Bunga Pythonda `unpacking` deyiladi.


```python
# 3 ta meva nomidan iborat tuple yaratilmoqda
my_tuple = ("apple", "banana", "cherry")

# Tuple ichidagi har bir qiymat alohida o‘zgaruvchiga ajratilmoqda
(fruit1, fruit2, fruit3) = my_tuple

# Har bir o‘zgaruvchidagi qiymat ekranga chiqariladi
print(fruit1)  # 'apple'
print(fruit2)  # 'banana'
print(fruit3)  # 'cherry'
```

### ❇️ NESTED TUPLE

📌 Tuple ichida yana boshqa tuple ham saqlanishi mumkin. Bunga **ichma-ich** tuple yoki **nested tuple** deyiladi.


```python
# Bu yerda talaba haqida ma'lumotlar saqlanmoqda:
# ism, yosh, va baholar (baholar alohida tuple ichida)
student = ("Ali", 20, (85, 90, 95))

# Indeks 0 — ismni beradi
print(student[0])  # Ali

# Indeks 1 — yoshni beradi
print(student[1])  # 20

# Indeks 2 — baholar joylashgan ichki tuple
print(student[2])  # (85, 90, 95)

# Ichki tuple ichidagi ikkinchi bahoni olish
print(student[2][1])  # 90
```


### ❇️ TUPLE BILAN ISHLASHDA FOYDALI METODLAR

#### ✳️ .count()

📌 Bu funksiya siz bergan qiymatni tuple ichida qidiradi va nechta marta borligini sanaydi. Agar qiymat topilmasa, 0 qaytaradi.

```python
# Bir nechta takrorlanuvchi sonlardan iborat tuple
my_tuple = (1, 2, 2, 3, 2)

# 2 soni tuple ichida necha marta borligini hisoblaydi
print(my_tuple.count(2))  # 3
```

#### ✳️ .index()

📌 Bu metod tuple ichida berilgan qiymat qayerda turganini aniqlaydi, ya’ni indeks raqamini qaytaradi.

```python
# Elementlar ketma-ketligi
my_tuple = (1, 2, 3, 2, 4)

# 2 soni birinchi bo‘lib qayerda uchraganini topadi (indeks 1)
print(my_tuple.index(2))  # 1
```


# ✅ AMALIYOT

### ✅ 1-topshiriq:  
Quyidagi 3 ta hayvon nomidan iborat `animals` degan tuple yarating va ekranga chiqaring:  
- `"quyon"`, `"mushuk"`, `"it"`

---

### ✅ 2-topshiriq:  
Faqat `"apple"` qiymatidan iborat tuple yarating.  
- Vergul qo‘yilmasa, bu oddiy `string` bo‘lib qoladi. To‘g‘ri tuple yarating.

---

### ✅ 3-topshiriq:  
Quyidagi tupledagi ikkinchi elementni ekranga chiqaring:

```python
colors = ("red", "green", "blue")
```

---

### ✅ 4-topshiriq:  
Quyidagi tupledan oxirgi elementni `-1` indeks yordamida chiqaring:

```python
numbers = (5, 10, 15, 20)
```

---

### ✅ 5-topshiriq:  
Quyidagi ikki tupleni `+` operatori yordamida birlashtiring va yangi `result` nomli tuple yarating:

```python
a = (1, 2)
b = (3, 4)
```

---

### ✅ 6-topshiriq:  
Quyidagi tuple 3 marta takrorlab `new_tuple` degan yangi tuple yarating:

```python
word = ("Hi",)
```

---

### ✅ 7-topshiriq:  
Quyidagi tuple ichida nechta element borligini `len()` yordamida aniqlang:

```python
digits = (1, 2, 3, 4, 5, 6)
```

---

### ✅ 8-topshiriq:  
Quyidagi tupleda `"banana"` bor yoki yo‘qligini `in` operatori yordamida tekshirib chiqaring:

```python
fruits = ("apple", "banana", "cherry")
```

---

### ✅ 9-topshiriq:  
Quyidagi tupledagi qiymatlarni alohida 3 ta o‘zgaruvchiga ajrating (`unpacking` qiling):

```python
person = ("Ali", 25, "Toshkent")
```

---

### ✅ 10-topshiriq:  
Quyidagi nested tupledan 90 sonini alohida olib ekranga chiqaring:

```python
student = ("Ali", 20, (85, 90, 95))
```

---

### ✅ 11-topshiriq:  
Quyidagi tupleda `2` soni nechta marta qatnashganini `.count()` yordamida aniqlang:

```python
data = (1, 2, 3, 2, 4, 2)
```

---

### ✅ 12-topshiriq:  
Quyidagi tupleda `3` soni birinchi marta qaysi indeksda turganini `.index()` yordamida aniqlang:

```python
nums = (5, 3, 7, 3, 9)
```

---

### ✅ 13-topshiriq:  
Quyidagi kodda tuple emas, string yaratilgan. Uni tuzatib, haqiqiy tuple holatiga keltiring:

```python
item = ("book")
```

---

### ✅ 14-topshiriq:  
Quyidagi tupledan `"Python"` so‘zini indeks yordamida ajratib oling:

```python
langs = ("C++", "Python", "Java")
```

---

### ✅ 15-topshiriq:  
Quyidagi ikki tupleni `+` operatori yordamida birlashtiring va `new_tuple` nomli yangi tuplega saqlang:

```python
tuple1 = ("a", "b")
tuple2 = ("c", "d", "e")
```

---