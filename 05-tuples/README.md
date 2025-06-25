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

### TUPLE USTIDA AMALLAR

📌 Tuple — bu o‘zgarmas ma’lumot turi. Ya’ni, yaratilgach, uning ichidagi qiymatlarni o‘zgartirib, o‘chirib yoki yangisini qo‘shib bo‘lmaydi.

- 📌 Lekin, siz tuple bilan ikkita amalni bemalol bajara olasiz:
    - Tuplelarni birlashtirish
    - Tupleni takrorlash


1. Tuplelarni birlashtirish:
    - Tuple'lar o'zgarmas (`immutable`) ma'lumot turi bo'lganligi uchun birlashtirish jarayonida asl `tuple`lar o'zgarmaydi. Yangi tuple yaratiladi.

    ```python
    tuple1 = (1, 2)
    tuple2 = (3, 4)
    new_tuple = tuple1 + tuple2
    print(new_tuple)  # (1, 2, 3, 4)
    ```
    - Agar siz bir tupleni o'z-o'ziga birlashtirishni xohlasangiz, yana bir tuple qo'shib berishingiz kerak bo'ladi.
    ```python
    tuple1 = (1, 2, 3)

    # tuple1 ni o'z-o'zidan ikki marta birlashtirish
    result = tuple1 + tuple1
    print(result)
    ```

#### TUPLENI BOSHQA MALUMOT TURLARI BILAN BIRLASHTIRISH

2. Tupleni ko‘paytirish:
```python
tuple1 = ("hello",)
new_tuple = tuple1 * 3
print(new_tuple)  # ('hello', 'hello', 'hello')
```

### TUPLE UZUNLIGINI ANIQLASH

`Tuple`dagi elementlar sonini aniqlash uchun `len()` funksiyasidan foydalaniladi:

```python
my_tuple = (1, 2, 3, 4, 5)
print(len(my_tuple))  # 5
```

### TUPLEDA `in` OPERATORI
- Biror qiymat tupleda bor yoki yo‘qligini `in` operatori yordamida tekshirish mumkin:
```python
my_tuple = ("apple", "banana", "cherry")
print("banana" in my_tuple)  # True
```

### TUPLENI QIYMATLARGA AJRATISH(`Unpacking`)
- Tuplening barcha qiymatlarini o‘zgaruvchilarga ajratib olish mumkin:
```python
my_tuple = ("apple", "banana", "cherry")
(fruit1, fruit2, fruit3) = my_tuple
print(fruit1)  # 'apple'
print(fruit2)  # 'banana'
print(fruit3)  # 'cherry'
```

### TUPLE ICHIDA TUPLE
- Tuple ichida yana boshqa tuplelar saqlanishi mumkin:
```python
nested_tuple = (1, 2, (3, 4), 5)
print(nested_tuple[2])  # (3, 4)
```
### TUPLE BILAN ISHLASHDA FOYDALI FUNKSIYALAR
1. `.count():` Tuple ichida biror qiymat necha marta takrorlanganini aniqlaydi.
```python
my_tuple = (1, 2, 2, 3)
print(my_tuple.count(2))  # 2
```

2. `.index():` Tuple ichida berilgan qiymatning indeksini topadi.
```python
my_tuple = (1, 2, 3)
print(my_tuple.index(2))  # 1
```

> [!NOTE]
> Agar Tuple ga o'zgartirish talab qilinsa, yagona yo'li o'zgarmas ro'yxatni `list()` funksiyasi yordamida `List` (oddiy ro'yxat) ko'rinishiga keltirib olish, o'zgarishlarni bajarsih va qaytarib `tuple()` funktsiyasi yordamida o'zgarmas ro'yxatga o'tkazish mumkin:

```python
toys = ('bus','car','bear','dino','snake','lizard') # o'zgarmas ro'yxat
toys = list(toys) # o'zgarmas ro'yxatni oddiy ro'yxatga (List) aylantiramiz
# Ro'yxatga o'zgartirishlar kiritamiz
toys.append('dragon')
toys.remove('bus')
toys[1] = 'mcqueen'
toys = tuple(toys) # Ro'yxatni qaytadan o'zgarmas ro'yxatga (Tuple) aylantiramiz
print(toys)
```

# AMALIYOT

1. **Tuple yaratish va qiymatlarni chiqarish.**
    ```python
    # 1. Quyidagi tuple'ni yarating va har bir elementini ekranga chiqaring.
    my_tuple = (10, 20, 30, 40, 50)
    ```
    **Natija:**
    ```shell
    (10, 20, 30, 40, 50)
    ```
2. **Tuple elementlariga indeks orqali murojaat qilish.**
    ```python
    # 2. Quyidagi tuple'dan birinchi va oxirgi elementni ekranga chiqaring.
    my_tuple = ('apple', 'banana', 'cherry', 'date', 'elderberry')
    ```
    **Natija:**
    ```shell
    Birinchi element: apple
    Oxirgi element: elderberry
    ```
3. **Tuple’larni birlashtirish.**
    ```python
    # 3. Ikkita tuple'ni birlashtirib, yangi tuple yarating.
    tuple1 = (1, 2, 3)
    tuple2 = (4, 5, 6)
    ```
    **Natija:**
    ```shell
    (1, 2, 3, 4, 5, 6)
    ```

4. **Tuple uzunligini aniqlash.**
    ```python
    # 4. Quyidagi tuple'ning uzunligini aniqlang.
    my_tuple = ('cat', 'dog', 'rabbit', 'parrot')
    ```
    **Natija:**
    ```shell
    4
    ```

5. **Tuple ichidagi elementlarning qiymatini sanash.**
    ```python
    # 5. Tuple ichida necha marta 'apple' so‘zi mavjudligini aniqlang.
    fruits = ('apple', 'banana', 'cherry', 'apple', 'apple', 'banana')
    ```
    **Natija:**
    ```shell
    3
    ```
6. **Tuple ichida qiymat mavjudligini tekshirish.**
    ```python
    # 6. Tuple ichida 'banana' bor-yo‘qligini tekshiring.
    fruits = ('apple', 'banana', 'cherry')
    ```
    **Natija:**
    ```shell
    True
    ```