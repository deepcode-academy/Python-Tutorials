# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 LISTS


## ✅ PYTHONDA LISTSLAR BILAN ISHLASH

📌 LIST — bu bir nechta ma'lumotlarni bitta o‘zgaruvchida **navbatma-navbat** saqlash uchun ishlatiladigan ma'lumot turi.

## ✅ LISTNING ASOSIY XUSUSIYATLARI

✳️ Bir nechta qiymatni bitta joyda saqlaydi

✳️ Har bir qiymatning tartib raqami (index) bo‘ladi (0 dan boshlanadi)

✳️ Istalgan turdagi ma’lumotlar (son, matn, True/False) saqlanishi mumkin

✳️ O‘zgartirish mumkin (ya'ni listdagi ma’lumotlarni qo‘shish, o‘chirish, almashtirish mumkin)

## ✅ QACHON ISHLATILADI?

✳️ Ko‘p sonli ma’lumotlarni tartib bilan saqlash kerak bo‘lsa

✳️ Ma’lumotlar ustida takrorlash, filtrlash, yoki saralash kerak bo‘lsa

✳️ Bir nechta qiymatni bitta o‘zgaruvchida saqlash orqali kodni soddalashtirish kerak bo‘lsa



## ✅ LIST YARATISH

```python
# Bir nechta elementli list
my_list = [10, "DeepCode", True, 3.14]

# Bo‘sh list
empty_list = []
```

## ✅ LIST ELEMENTLARIGA MUROJAT QILISH

### ✳️ INDEX ORQALI MUROJAT QILISH

📌 Listdagi har bir element o‘zining indeks raqami bilan tartiblanadi. Pythonda indekslash `0` dan boshlanadi.

```python
# Mevalar ro'yxatini yaratamiz
fruits = ['olma', 'banan', 'gilos', 'shaftoli']

# Ro'yxatdagi birinchi elementni (0-indeks) ekranga chiqaramiz
print(fruits[0])  # 'olma'

# Ro'yxatdagi uchinchi elementni (2-indeks) ekranga chiqaramiz
print(fruits[2])  # 'gilos'
```

### ✳️ NEGATIVE INDEXING

📌 Pythonda oxirgi elementga manfiy indekslar yordamida murojaat qilinadi.

```python
# Mevalar ro'yxatini yaratamiz
fruits = ['olma', 'banan', 'gilos', 'shaftoli']

# Ro'yxatdagi oxirgi elementni (manfiy indeks -1) ekranga chiqaramiz
print(fruits[-1])  # 'shaftoli'

# Ro'yxatdagi oxiridan ikkinchi elementni (manfiy indeks -2) ekranga chiqaramiz
print(fruits[-2])  # 'gilos'
```

### ✳️ SLICING

📌 Listning ma’lum qismini olish uchun slicing ishlatiladi: `list[start:stop]`

```python
# Mevalar ro'yxatini yaratamiz
fruits = ['olma', 'banan', 'gilos', 'shaftoli']

# Indeks 1 dan boshlab 3 gacha bo'lgan elementlarni olish (3-indeks kirmaydi)
print(fruits[1:3])  # ['banan', 'gilos']

# Boshlanishi avtomatik 0 deb olinadi, 0 dan 2 gacha bo'lgan elementlar (2-indeks kirmaydi)
print(fruits[:2])   # ['olma', 'banan']

# Indeks 2 dan boshlab oxirigacha bo'lgan elementlarni olish
print(fruits[2:])   # ['gilos', 'shaftoli']
```

### ✳️ SLICING WITH STEP

```python
# Mevalar ro'yxatini yaratamiz
fruits = ['olma', 'banan', 'gilos', 'shaftoli']

# Har 2-elementdan birini olamiz: 0, 2-indeksdagilar (ya'ni 1-element, 3-element)
print(fruits[::2])   # ['olma', 'gilos']

# Ro'yxatni teskari tartibda chiqaramiz
print(fruits[::-1])  # ['shaftoli', 'gilos', 'banan', 'olma']
```

## ✅ LISTDAGI E'LEMENTLAR SONINI TOPISH

📌List uzunligi degani — list ichida nechta element (ya'ni qiymat) borligini bildiradi. Pythonda bu uzunlikni `len()` funksiyasi yordamida topamiz.

```python
# Bu yerda bizda 5 ta kompaniya bor
companies = ['Google', 'Microsoft', 'Amazon', 'Tesla', 'Apple']

# len(companies) — bu companies listida nechta element borligini hisoblaydi
print(len(companies))
``` 

## ✅ LISTGA E'LEMENT QO'SHISH

### ✳️ .append(x)

📌 list oxiriga bitta element qo‘shadi.


```python
# Dastlab avtomobillar ro'yxatini yaratamiz
cars = ['Nexia', 'Cobalt']

# Ro'yxat oxiriga yangi element 'Malibu' ni qo‘shamiz
cars.append('Malibu')

# Yangilangan ro'yxatni ekranga chiqaramiz
print(cars)  # ['Nexia', 'Cobalt', 'Malibu']
```

📌 `.append()` faqat bitta element qo‘shadi. Agar bir nechta element qo‘shmoqchi bo‘lsangiz, ularni list ko‘rinishida beriladi va list ichiga yana bir list qo‘shiladi:

```python
# Dastlab 3 ta sondan iborat ro'yxat yaratamiz
my_list = [1, 2, 3]

# Ro'yxat oxiriga [4, 5] ro'yxatini bitta element sifatida qo‘shamiz (ichki ro'yxat bo'ladi)
my_list.append([4, 5])

# Natijaviy ro'yxatni ekranga chiqaramiz
print(my_list)  # [1, 2, 3, [4, 5]]
```

### ✳️ .extend()

📌 bir nechta elementni alohida-alohida qo‘shadi.

```python
# Boshlang'ich ro'yxat: 1, 2, 3 sonlari mavjud
my_list = [1, 2, 3]

# extend() metodi orqali [4, 5] ro'yxatining elementlarini alohida-alohida qo‘shamiz
my_list.extend([4, 5])

# Natijaviy ro'yxatni chiqaramiz
print("extend() natijasi:", my_list)  # Bu ro'yxatning elementlarini alohida qo'shadi
```

### ✳️ .insert(i, x)

📌 list ichidagi istalgan joyga bitta element qo‘shadi

```python
# Dastlab 1, 2, 3 sonlaridan iborat ro'yxat yaratamiz
my_list = [1, 2, 3]

# 2-pozitsiyaga (ya'ni 3-element o'rniga) 99 sonini qo‘shamiz
my_list.insert(2, 99)

# Natijaviy ro'yxatni ekranga chiqaramiz
print(my_list)  # [1, 2, 99, 3]
```

### ✳️ += 

📌 listga boshqa listni qo‘shadi


```python
# Boshlang'ich ro'yxat: 1, 2, 3
my_list = [1, 2, 3]

# += operatori yordamida [4, 5] ro'yxatini my_list ga kengaytiramiz (xuddi extend() kabi ishlaydi)
my_list += [4, 5]

# Natijaviy ro'yxatni chiqaramiz
print(my_list)  # [1, 2, 3, 4, 5]
```

## ✅ E'LEMENTLARNI O'CHIRISH

### ✳️ .remove(x)

📌 list ichida siz ko‘rsatgan qiymatga teng bo‘lgan birinchi elementni o‘chiradi.


```python
# Dastlabki list: bir nechta sonlar mavjud, jumladan ikki marta 3 soni
my_list = [1, 2, 3, 4, 3, 5]

# remove() metodi listdan **birinchi uchragan** 3 ni o'chiradi
my_list.remove(3)

# Yangilangan listni ekranga chiqaramiz
print(my_list)  # [1, 2, 4, 3, 5]
```

### ✳️ .pop()

📌 Agar `.pop()` funksiyasiga hech narsa bermasangiz, oxirgi elementni o‘chiradi.

```python
# Dastlabki ro'yxatni yaratamiz
my_list = [10, 20, 30, 40, 50]

# pop() metodi ro'yxatning oxirgi elementini (50) o'chirib tashlaydi
my_list.pop()

# Yangilangan ro'yxatni ekranga chiqaramiz
print(my_list)  # [10, 20, 30, 40]
```

### ✳️ .pop(i)

📌  Aniq indexdagi elementni o‘chiradi

```python
# Boshlang'ich ro'yxat: 10, 20, 30, 40
my_list = [10, 20, 30, 40]

# pop(1) metodi ro'yxatdagi 1-indeksdagi elementni (ya'ni 20 ni) o'chiradi
my_list.pop(1)

# Yangilangan ro'yxatni ekranga chiqaramiz
print(my_list)  # [10, 30, 40]
```

### ✳️ del

📌 Istalgan element yoki butun listni o‘chiradi

```python
# Boshlang'ich ro'yxat: 4 ta harf mavjud
my_list = ['a', 'b', 'c', 'd']

# del operatori yordamida ro'yxatdagi 2-indeksdagi element ('c') ni o‘chiramiz
del my_list[2]

# Ro'yxat yangilanadi: endi ['a', 'b', 'd'] bo'ladi
print("1-element o‘chirilgan ro‘yhat:", my_list)  # ['a', 'b', 'd']

# Ro'yxatni qaytadan yaratamiz
my_list = ['a', 'b', 'c', 'd']

# del operatori yordamida butun ro'yxatni (ya'ni my_list o'zgaruvchisini) o‘chiramiz
del my_list

# Bu yerda my_list endi mavjud emas, agar pastda print(my_list) desangiz — xatolik (NameError) chiqadi
# print(my_list)  # ❌ NameError: name 'my_list' is not defined
```

## ✅ LISTNI TOZALASH

📌 Agar list ichidagi hamma elementlarni o‘chirib, uni bo‘sh holatga keltirmoqchi bo‘lsangiz, `.clear()` metodidan foydalaniladi.

```python
# Boshlang'ich ro'yxat: 1 dan 5 gacha sonlar mavjud
my_list = [1, 2, 3, 4, 5]

# clear() metodi ro'yxatdagi barcha elementlarni o‘chiradi (lekin ro'yxatning o‘zi qoladi, bo‘sh holatda)
my_list.clear()

# Bo‘sh ro'yxatni ekranga chiqaramiz
print(my_list)  # []
```

## ✅ LISTNI SARALASH

📌 Python dasturlash tilida listdagi elementlarni tartiblash uchun ikkita asosiy vosita mavjud: `.sort()` metodi va `sorted()` funksiyasi. Ularning ikkalasi ham listni tartiblash uchun ishlatiladi, lekin ular orasida muhim farqlar bor. Tartiblashda raqamlar o'sib borish tartibida, matnlar esa alifbo tartibida tartiblanadi.



### ✳️ .sort()

📌 `.sort()` — bu listning o‘ziga tegishli metod bo‘lib, u faqat listlar bilan ishlaydi. Agar siz `.sort()` metodini ishlatsangiz, u listning o‘zini tartiblaydi, ya’ni listdagi e'lementlar joyida o‘zgaradi. Boshqacha aytganda, bu metod listni o‘zgartiradi va tartiblangan yangi list yaratmaydi. Misol uchun, sizda bir list bo‘lsa va `.sort()` desangiz, o‘sha list tartiblanadi va avvalgi tartibi yo‘qoladi. Shuning uchun, agar sizga asl list kerak bo‘lsa, `.sort()`ni ishlatishdan oldin ehtiyot bo‘lish kerak, chunki u listni butunlay o‘zgartirib yuboradi. Bu metod hech qanday natija qaytarmaydi, ya’ni `None` degan qiymatni qaytaradi.

```python
# Boshlang'ich ro'yxat: aralash tartibda sonlar mavjud
my_list = [3, 1, 4, 1, 5, 9, 2]

# sort() metodi ro'yxatni o'sish tartibida (kichikdan kattaga) saralaydi
my_list.sort()

# Tartiblangan ro'yxatni ekranga chiqaramiz
print(my_list)  # [1, 1, 2, 3, 4, 5, 9]
```

### ✳️ .sorted()

📌 `sorted()` esa funksiyadir. Bu funksiya faqat `list` emas, balki boshqa turdagi ma’lumotlar bilan ham ishlay oladi — masalan, `string`, `tuple` va boshqa tartiblangan ma’lumot turlari bilan. `sorted()` funksiyasining eng katta afzalligi — u mavjud listni o‘zgartirmaydi. U asl listga tegmaydi, balki yangi tartiblangan listni qaytaradi. Bu esa sizga asl ma’lumotni saqlab qolgan holda, tartiblangan nusxasi bilan ishlash imkonini beradi. Agar sizga vaqtincha tartiblangan natija kerak bo‘lsa yoki original listni o‘zgartirmasdan ishlashni xohlasangiz, `sorted()` funksiyasi aynan sizga mos keladi.

```python
# Boshlang'ich ro'yxat: aralash tartibdagi sonlar
my_list = [3, 1, 4, 1, 5, 9]

# sorted() funksiyasi yangi tartiblangan ro'yxat yaratadi, asl ro'yxat o'zgarmaydi
sorted_list = sorted(my_list)

# Yangi (saralangan) ro'yxatni chiqaramiz
print("Yangi ro‘yxat:", sorted_list)  # [1, 1, 3, 4, 5, 9]

# Asl ro'yxat o'zgarishsiz qolganini ko'rsatamiz
print("Asl ro‘yxat:", my_list)        # [3, 1, 4, 1, 5, 9]
```

## ✅ TESKARI TARTIBDA SARALASH

### ✳️ .sort(reverse=True)

```python
# Boshlang'ich list: aralash sonlar mavjud
my_list = [3, 1, 4, 1, 5, 9]

# sort() metodi orqali listni kamayish tartibida tartiblaymiz
my_list.sort(reverse=True)

# Tartiblangan listni ekranga chiqaramiz
print(my_list)  # [9, 5, 4, 3, 1, 1]
```


### ✳️ sorted(..., reverse=True)

```python
# Boshlang'ich list: aralash sonlar mavjud
my_list = [3, 1, 4, 1, 5, 9]

# sorted() funksiyasi listni kamayish tartibida tartiblaydi va yangi list qaytaradi
sorted_list = sorted(my_list, reverse=True)

# Teskari tartiblangan yangi listni chiqaramiz
print("Teskari list:", sorted_list)  # [9, 5, 4, 3, 1, 1]
```

## ✅ QO'SHIMCHA PARAMETR

### ✳️ KEY

```python
# Ismlar listi: har xil uzunlikdagi so'zlardan iborat
names = ['Ali', 'Muhammad', 'Zafar', 'Islom']

# sort() metodi va key=len parametri yordamida listni so'z uzunligi bo'yicha o'sish tartibida saralaymiz
names.sort(key=len)

# Saralangan listni chiqaramiz
print(names)  # ['Ali', 'Zafar', 'Islom', 'Muhammad']
```



## ✅ LISTNI TESKARIGA O'ZGARTIRISH

### ✳️ .reverse()

📌 Ba'zida ro‘yxatdagi elementlarni teskari tartibda ko‘rsatish kerak bo‘ladi — ya'ni oxirgi element birinchi, birinchi element esa oxirgi bo‘ladi.

```python
# Boshlang'ich list: 1 dan 5 gacha bo'lgan sonlar
my_list = [1, 2, 3, 4, 5]

# reverse() metodi list elementlarini teskari tartibda joylashtiradi
my_list.reverse()

# Teskari tartibga keltirilgan listni ekranga chiqaramiz
print(my_list)  # [5, 4, 3, 2, 1]
```

## ✅ LISTNI BIRLASHTIRISH

### ✳️ +

📌 Bu usulda ikkita listni qo‘shib, yangi bitta list hosil qilamiz.

```python
# 1-chi list
list1 = [1, 2, 3]

# 2-chi list
list2 = [4, 5, 6]

# + operatori yordamida ikkala listni birlashtiramiz
merged_list = list1 + list2

# Yangi birlashtirilgan listni chiqaramiz
print(merged_list)  # [1, 2, 3, 4, 5, 6]
```

### ✳️ +=

📌 Bu usulda ikkinchi list elementlari birinchi listga qo‘shiladi va birinchi ro‘yxat o‘zgartiriladi.

```python
# 1-chi list
list1 = [1, 2, 3]

# 2-chi list
list2 = [4, 5, 6]

# += operatori list2 dagi elementlarni list1 ga alohida-alohida qo‘shadi
list1 += list2

# Natijaviy list1 ni ekranga chiqaramiz
print(list1)  # [1, 2, 3, 4, 5, 6]
```

### ✳️ .extend()

```python
# 1-chi list
list1 = [1, 2, 3]

# 2-chi list
list2 = [4, 5, 6]

# extend() metodi list2 dagi barcha elementlarni list1 ga alohida-alohida qo‘shadi
list1.extend(list2)

# Natijaviy list1 ni ekranga chiqaramiz
print(list1)  # [1, 2, 3, 4, 5, 6]
```


## ✅ MULTI DEMENSIONAL LIST

📌 Pythonda list ichiga yana boshqa list joylash mumkin. Bu holat **multi dimensional list** deb ataladi (inglizchasiga o‘xshab "2D list" ham deyiladi).

```python
# Bu multi-dimensional list (ya'ni list of lists) — har bir element o'z ichida yana bir list saqlaydi
multi_dimensional_list = [
    [1, 2, 3],   # 0-index: birinchi inner list
    [4, 5, 6],   # 1-index: ikkinchi inner list
    [7, 8, 9]    # 2-index: uchinchi inner list
]
```

### ✳️ E'LEMENTLARGA MUROJAT QILISH

Ro'yxat ichidagi ro'yxatdagi elementlarga indekslar yordamida murojaat qilish mumkin.

```python
# List of lists (ya'ni list ichidagi list)
multi_dimensional_list = [
    [1, 2, 3],   # 0-index: birinchi inner list
    [4, 5, 6],   # 1-index: ikkinchi inner list
    [7, 8, 9]    # 2-index: uchinchi inner list
]

# Faqat bitta row'ni (masalan: 1-chi row) chiqaramiz
print("1-chi row:", matrix[1])  # [4, 5, 6]

# Endi shu row ichidan bitta elementni chiqaramiz (masalan: 2-chi element)
print("1-chi rowdagi 2-chi element:", matrix[1][1])  # 5
```

### ✳️ E'LEMENT QO'SHISH

```python
# List of lists (multi-dimensional list)
multi_dimensional_list = [
    [1, 2, 3],   # 0-index: birinchi ichki list (row)
    [4, 5, 6],   # 1-index: ikkinchi ichki list (row)
    [7, 8, 9]    # 2-index: uchinchi ichki list (row)
]

# append() metodi yordamida butun bir yangi ichki list (row) qo‘shiladi
multi_dimensional_list.append([10, 11, 12])

# Yangi list'ni ekranga chiqaramiz
print(multi_dimensional_list)
```

### ✳️ E'LEMENT O'ZGARTIRISH

```python
# Boshlang'ich list of lists (multi-dimensional list)
multi_dimensional_list = [
    [1, 2, 3],   # 0-index
    [4, 5, 6],   # 1-index
    [7, 8, 9]    # 2-index
]

# 0-indexdagi ichki listni yangisi bilan almashtiramiz
multi_dimensional_list[0] = [13, 14, 15]

# Natijani chiqaramiz
print(multi_dimensional_list)
```

### ✳️ ICHKI E'LEMENTNI O'ZGARTIRISH

```python
# Multi-dimensional list (list ichida listlar)
multi_dimensional_list = [
    [1, 2, 3],   # 0-index row
    [4, 5, 6],   # 1-index row
    [7, 8, 9]    # 2-index row
]

# 1-index row (ya'ni [4, 5, 6]) dagi 1-index elementni (ya'ni 5) 99 bilan almashtiramiz
multi_dimensional_list[1][1] = 99

# Natijani chiqaramiz
print(multi_dimensional_list)
```


## ✅ RO'YHATDA E'LEMENT BORLIGINI TEKSHIRISH

📌 Pythonda list ichida ma’lum bir e'lement bor yoki yo‘qligini tekshirish uchun `in` operatoridan foydalaniladi.

```python
# Oddiy list
my_list = [1, 2, 3, 4, 5]

# 3 elementi my_list ichida mavjudmi? → Ha, shuning uchun natija: True
print(3 in my_list)  # True

# 6 elementi my_list ichida mavjudmi? → Yo‘q, shuning uchun natija: False
print(6 in my_list)  # False
```

## ✅ QO'SHIMCHA FUNKSIYALAR

Python dasturlash tilida ro'yxatlar bilan ishlashda quyidagi funksiyalar yordamida ro'yxatdagi elementlarni `qo'shish`, `maksimal` va `minimal` qiymatlarni topish mumkin:

### ✳️ sum()

📌 listdagi sonlar yig‘indisini hisoblaydi

```python
# Oddiy sonlardan iborat list
my_list = [10, 20, 30, 40, 50]

# sum() funksiyasi listdagi barcha elementlarning yig'indisini hisoblaydi
sum_of_list = sum(my_list)

# Natijani chiqaramiz
print(f"Ro'yxatdagi elementlar yig'indisi: {sum_of_list}")
```

### ✳️ max()

📌 Listdagi eng katta qiymatni qaytaradi.

```python
# Sonlardan iborat list
my_list = [10, 20, 30, 40, 50]

# max() funksiyasi listdagi eng katta qiymatni qaytaradi
max_value = max(my_list)

# Natijani ekranga chiqaramiz
print(f"Ro'yxatdagi eng katta qiymat: {max_value}")
```

### ✳️ min()

📌 Listdagi eng kichik qiymatni qaytaradi.

```python
# Sonlardan iborat list
my_list = [10, 20, 30, 40, 50]

# min() funksiyasi listdagi eng kichik qiymatni qaytaradi
min_value = min(my_list)

# Natijani ekranga chiqaramiz
print(f"Ro'yxatdagi eng kichik qiymat: {min_value}")
```

## ✅ range()

Bu funktsiya yordamida biz ma'lum oraliqdagi sonlar ketma-ketligini yaratishimiz mumkin. 
`list()` funktsiyasi yordamida esa bu oraliqni ro'yxat shaklida saqlab olamiz:

```python
# 0 dan 9 gacha bo‘lgan sonlar ro‘yhatini yaratamiz
sonlar = list(range(0, 10))

# Natijani ekranga chiqaramiz
print(sonlar)
```

> [!CAUTION]
> range(a, b) funksiyasi doim `a` dan boshlanadi, `b` dan bitta oldin to‘xtaydi.

### ✳️ STEP

```python
# 0 dan 20 gacha (20 kirmaydi), har 2 qadam bilan — juft sonlar
juft_sonlar = list(range(0, 20, 2))

# 1 dan 20 gacha (20 kirmaydi), har 2 qadam bilan — toq sonlar
toq_sonlar = list(range(1, 20, 2))

# Juft sonlarni ekranga chiqaramiz
print("Juft sonlar: ", juft_sonlar)

# Toq sonlarni ekranga chiqaramiz
print("Toq sonlar: ", toq_sonlar)
```


> [!NOTE]
> Agar siz `0` dan boshlamoqchi bo‘lsangiz, `range(10)` deb yozish yetarli:

### NEGATIVE STEP

📌 Agar siz kamayib boruvchi sonlar ketma-ketligini istasangiz, `step` qiymatini manfiy qiling:

```python
# 10 dan 1 gacha kamayuvchi sonlar ro'yxatini yaratamiz
kamayuvchi = list(range(10, 0, -1))

# Natijani ekranga chiqaramiz
print(kamayuvchi)
```


## AMALIYOT

# 🐍 Python Lists — Amaliy Topshiriqlar

Quyidagi 15 ta topshiriq orqali `list` mavzusini mustahkamlaysiz. Har bir mashqni alohida bajaring va natijani `print()` yordamida terminalda ko‘ring.

---

## 1. Ro'yxat yaratish va elementga murojaat qilish

- Quyidagi elementlarga ega bo‘lgan ro'yxatni yarating: `'olma'`, `'banan'`, `'gilos'`, `'xurmo'`, `'anjir'`.
- Ro'yxatning **ikkinchi** va **to‘rtinchi** elementlarini terminalga chiqaring.

---

## 2. Ro'yxatni o‘zgartirish

- `1` dan `5` gacha bo‘lgan sonlar ro'yxatini yarating.
- Ro'yxatdagi **uchinchi** elementni `10` ga almashtiring va natijani chiqaring.

---

## 3. Element qo‘shish va o‘chirish

- Bo‘sh ro'yxat yarating.
- Ro'yxatga `'dog'`, `'cat'`, `'chicken'` elementlarini qo‘shing.
- `'cat'` elementini o‘chirib, ro'yxatni chiqaring.

---

## 4. Ro'yxat uzunligini topish

- Ro'yxat: `'red'`, `'green'`, `'blue'`, `'yellow'`, `'purple'`.
- Ro'yxatning uzunligini hisoblab, terminalga chiqaring.

---

## 5. Ro'yxatlarni birlashtirish

- Ikkita ro'yxat yarating:
  - `['a', 'b', 'c']`
  - `['d', 'e', 'f']`
- Ularni birlashtirib, yangi ro'yxatni terminalga chiqaring.

---

## 6. Element mavjudligini tekshirish

- Ro'yxat: `['mashina', 'avtobus', 'velosiped', 'poyezd']`
- `'avtobus'` ro'yxatda bormi? Tekshirib natijani (`True` yoki `False`) chiqaring.

---

## 7. Ro'yxatni saralash

- Ro'yxat: `[3, 1, 4, 2, 5]`
- O'sish tartibida saralang va natijani chiqaring.

---

## 8. Teskari tartibda chiqarish

- Ro'yxat: `[10, 20, 30, 40, 50]`
- `.reverse()` metodi yordamida ro'yxatni teskari chiqarish.

---

## 9. Ro'yxatni tozalash

- Ro'yxat: `['kitob', 'qalam', 'daftar', 'sumka']`
- `.clear()` yordamida barcha elementlarni o‘chirib, natijani chiqaring.

---

## 10. Ro'yxatni ko‘paytirish

- Ro'yxat: `[1, 2, 3]`
- Ro'yxatni `4` marta ko‘paytirib, yangi ro'yxatni terminalga chiqaring.

---

## 11. Minimal va maksimal qiymatni topish

- Ro'yxat: `[25, 17, 9, 50, 33]`
- `min()` va `max()` funksiyalari yordamida eng kichik va eng katta qiymatlarni toping.

---

## 12. Ro'yxatni nusxalash

- Ro'yxat: `[100, 200, 300, 400, 500]`
- Nusxa ko‘chiring (`copy()`) va yangi ro'yxatni chiqarib ko‘rsating.

---

## 13. Ro'yxatdagi elementlar yig‘indisi

- Ro'yxat: `[2, 4, 6, 8, 10]`
- `sum()` funksiyasi orqali yig‘indini hisoblang va natijani chiqaring.

---

## 14. Slicing va step ishlatish

- Ro'yxat: `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`
- Har ikkinchi elementni ajratib olib, yangi ro'yxat hosil qiling.

---

## 15. Multi-dimensional listdan element olish

- Ro'yxat: `[[1, 2], [3, 4], [5, 6]]`
- Ikkinchi ichki ro'yxatdagi ikkinchi elementni (`4`) terminalga chiqaring.

---
