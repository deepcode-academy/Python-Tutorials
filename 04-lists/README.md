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

### RO'YHATNI SARALASH

Ro'yhatni saralash uchun `.sort()` metodidan foydalanamiz. `.sort()` metodi ro'yhatimiz raqamlardan iborat bo'lsa o'sib borish tartibida saralaydi, agar ro'yhatimiz stringdan(harflardan) tashkil topgan bo'lsa alifbo tartibida saralaydi.

Pythonda ro'yxatlar bilan ishlashda `sort()` va `sorted() `metodlari mavjud bo'lib, ularning farqlari quyidagicha:

#### `.sort()` metodi
- `sort()` metodi ro'yxatni o'zida o'zgartiradi (`in-place`). Bu metod chaqirilganda asl ro'yxat o'zgartiriladi va yangi ro'yxat yaratilmaydi.

- sort() metodi faqat ro'yxatlar (lists) uchun mavjud.

```python
my_list = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]
my_list.sort()
print(my_list)
```

#### `.sorted()` funksiyasi

- `sorted()` funksiyasi asl ro'yxatni o'zgartirmaydi, balki saralangan elementlardan yangi ro'yxat yaratadi va qaytaradi.

- `sorted()` funksiyasi ro'yxat (`lists`) dan tashqari boshqa iteralanadigan (`iterable`) obyektlar bilan ham ishlashi mumkin, masalan, qatorlar (`tuples`), lug'atlar (`dictionaries`), va hokazo.

- `sorted()` funksiyasi saralangan yangi ro'yxatni qaytaradi.

```python
my_list = [3, 1, 4, 1, 5, 9]
sorted_list = sorted(my_list)
print(sorted_list)  # [1, 1, 3, 4, 5, 9]
print(my_list)      # [3, 1, 4, 1, 5, 9]
```

#### Qo'shimcha parametrlar

- `key` parametri: Elementlarni solishtirish uchun qo'shimcha funksiyani belgilash imkonini beradi.

- `reverse` parametri: Saralash tartibini belgilaydi (True bo'lsa, teskari tartibda saralanadi).

`.sort()` metodi bilan

```python
my_list = [3, 1, 4, 1, 5, 9]
my_list.sort(reverse=True)
print(my_list)  # [9, 5, 4, 3, 1, 1]
```

`.sorted()` funksiyasi bilan

```python
my_list = [3, 1, 4, 1, 5, 9]
sorted_list = sorted(my_list, reverse=True)
print(sorted_list)  # [9, 5, 4, 3, 1, 1]
print(my_list)      # [3, 1, 4, 1, 5, 9]
```


### RO'YHATNI TESKARIGA O'ZGARTIRISH

Ba'zida ro'yxatni aylantirish (boshini oxiriga, oxirini boshiga) talab qilinishi mumkin. Buning uchun 
`.reverse()` metodidan foydalanamiz.

```python
my_list.reverse()
print(my_list)
```

### RO'YHATNI BIRLASHTIRISH

Pythonda ro'yhatlarni birlashtirishni bir nechta usullari bor. Quyida ularga misollar ko'ramiz:

Birinchi usuli `+` operatori bilan birlashtirish:

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]
merged_list = list1 + list2
print(merged_list)
```

**Natija:** `[1, 2, 3, 4, 5, 6]`

`.extend()` metodi bilan birlashtirish:

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]
list1.extend(list2)
print(list1)
```

**Natija:** `[1, 2, 3, 4, 5, 6]`

`itertools.chain()` yordamida:

```python
import itertools

list1 = [1, 2, 3]
list2 = [4, 5, 6]
combined_list = list(itertools.chain(list1, list2))
print(combined_list)
```

**Natija:** `[1, 2, 3, 4, 5, 6]`

### RO'YHAT ICHIDAGI RO'YHAT

Pythonda ro'yxatlar ichidagi ro'yxatlar, ya'ni `ko'p o'lchovli ro'yxatlar` yaratish va ulardan foydalanish juda oddiy. Quyida bunday ro'yxatlar bilan qanday ishlashni ko'rsatib beraman.

```python
multi_dimensional_list = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

#### Elementlarga murojaat qilish

Ro'yxat ichidagi ro'yxatdagi elementlarga indekslar yordamida murojaat qilish mumkin.

```python
print(multi_dimensional_list[0][2])  # 3
```
Yuqoridagi kodda `0` indexda turgan ro'yhatni tanlab oldim va tanlangan ro'yhatning ichidagi `2` indexda turgan elementga murojat qildim.

Ro'yxatlar ichidagi ro'yxatlarga yangi ro'yxat qo'shish mumkin:

```python
multi_dimensional_list.append([10, 11, 12])
print(multi_dimensional_list)
```

Ro'yhat ichidagi ro'yhatlarni o'zgartirish mumkin:

```python
multi_dimensional_list[0] = [13, 14, 15]
print(multi_dimensional_list)
```

Ma'lum bir ichki ro'yxat elementini o'zgartirish mumkin:

```python
multi_dimensional_list[1][1] = 99
print(multi_dimensional_list)
```

### RO'YHATNI KO'PAYTIRISH

```python
my_list = [1, 2, 3]
multiplied_list = my_list * 3
print(multiplied_list)
```

### RO'YHATDA E'LEMENT BORLIGINI TEKSHIRISH

Python'da ro'yxat ichida element borligini tekshirish uchun `in` operatoridan foydalanish mumkin. Bu operator juda sodda va qulay bo'lib, ro'yxat ichida ma'lum bir elementning mavjudligini aniqlash imkonini beradi.

```python
my_list = [1, 2, 3, 4, 5]
print(3 in my_list)  # True
print(6 in my_list)  # False
```
### QO'SHIMCHA FUNKSIYALAR

Python dasturlash tilida ro'yxatlar bilan ishlashda quyidagi funksiyalar yordamida ro'yxatdagi elementlarni `qo'shish`, `maksimal` va `minimal` qiymatlarni topish mumkin:

`sum()` **funksiyasi:** Ro'yxatdagi barcha sonlarning yig'indisini qaytaradi.

```python
my_list = [10, 20, 30, 40, 50]
# Ro'yxatdagi elementlar yig'indisini hisoblash
sum_of_list = sum(my_list)
print(f"Ro'yxatdagi elementlar yig'indisi: {sum_of_list}")
```

`max()` **funksiyasi:** Ro'yxatdagi eng katta qiymatni qaytaradi.

```python
# Ro'yxatdagi eng katta qiymatni topish
max_value = max(my_list)
print(f"Ro'yxatdagi eng katta qiymat: {max_value}")
```

`min()` **funksiyasi:** Ro'yxatdagi eng kichik qiymatni qaytaradi.

```python
# Ro'yxatdagi eng kichik qiymatni topish
min_value = min(my_list)
print(f"Ro'yxatdagi eng kichik qiymat: {min_value}")
```

### `.range()` FUNKSIYASI

Bu funktsiya yordamida biz ma'lum oraliqdagi sonlar ketma-ketligini yaratishimiz mumkin. 
`list()` funktsiyasi yordamida esa bu oraliqni ro'yxat shaklida saqlab olamiz:

```python
sonlar = list(range(0,10)) # 
print(sonlar)
```
**Natija:** `[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`

Yuqoridagi misolda `range(0,10)` funktsiyasi 0 dan 9 gacha sonlar ketma-ketligini shakllantirdi, `list(range(0,9))` esa bu ketma-ketlikni ro'yxatga aylantirdi.

> [!CAUTION]
> Diqqat! E'tibor qiling 
`range()` funktsiyasi ikkinchi indeksdan bitta avval to'xtaydi.

`range()` yordamida qadamni ham berishimiz mumkin:

```python
juft_sonlar = list(range(0,20,2)) # 0 dan 20 gacha 2 qadam bilan
toq_sonlar = list(range(1,20,2))  # 1 dan 20 gacha 2 qadam bilan
print("Juft sonlar: ", juft_sonlar)
print("Toq sonlar: ", toq_sonlar)
```
**Natija:**
**Juft sonlar:** `[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]`
**Toq sonlar:** `[1, 3, 5, 7, 9, 11, 13, 15, 17, 19] `

> [!NOTE]
> Agar sonlar ketma-ketligi `0` dan boshlansa, `range()` funktsiyasida yakuniy indeksni ko'rsatish kifoya. Misol uchun `range(0,10)` emas `range(10)` deb yozsak ham bo'laveradi.


## AMALIYOT
1. **Ro'yhat yaratish va elementga murojat qilish.**
    - Quyidagi elementlarga ega bo'lgan ro'yxatni yarating: `'olma'`, `'banan'`, `'gilos'`, `'xurmo'`, `'anjir'`.
    - Ro'yxatning `ikkinchi` va `to'rtinchi` elementlarini oling va ularni terminalga chiqaring.

2. **Ro'yxatni o'zgartirish.**
    - `1` dan `5` gacha bo'lgan sonlar ro'yxatini yarating.
    - Ro'yxatdagi `uchinchi` elementni `10` ga almashtiring va yangilangan ro'yxatni terminalga chiqaring.

3. **Element qo'shish va o'chirish.**
    - Bo'sh ro'yxat yarating.
    - Ro'yxatga `'dog'`, `'cat'` va `'chicken'` elementlarini qo'shing.
    - Ro'yxatdan `'cat'` ni `o'chiring` va natijani terminalga chiqaring.

4. **Ro'yxat uzunligini topish.**
    - Quyidagi elementlarga ega ro'yxat yarating: `'red'`, `'green'`, `'blue'`, `'yellow'`, `'purple'`.
    - Ro'yxatning `uzunligini` toping va terminalga chiqaring.

5. **Ro'yxatlarni birlashtirish.**
    - Quyidagi ikkita ro'yxatni yarating:
        - Ro'yxat1: `['a', 'b', 'c']`
        - Ro'yxat2: `['d', 'e', 'f']`
    - Ikkala ro'yxatni birlashtiring va natijani terminalga chiqaring.

6. **Elementning mavjudligini tekshirish.**
    - Quyidagi ro'yxatni yarating: `['mashina', 'avtobus', 'velosiped', 'poyezd']`
    - Ro'yxatda `'avtobus'` bor-yo'qligini tekshiring va natijani terminalga chiqaring `(True/False)`.

7. **Ro'yxatni saralash.**
    - Quyidagi sonlardan iborat ro'yxat yarating: `[3, 1, 4, 2, 5]`.
    - Ro'yxatni `o'sish` tartibida saralang va natijani terminalga chiqaring.

8. **Ro'yxatdagi elementlarni teskari tartibda Terminalga chiqarish.**
    - Quyidagi ro'yxatni yarating: `[10, 20, 30, 40, 50]`.
    - Ro'yxatni `teskari` tartibda terminalga chiqaring (`reverse`).

9. **Ro'yxatni tozalash.**
    - Quyidagi ro'yxatni yarating: `['kitob', 'qalam', 'daftar', 'sumka']`.
    - Ro'yxatni tozalang (`hamma elementlarni o'chiring`) va bo'sh ro'yxatni terminalga chiqaring.

10. **Ro'yxat elementlarini ko'paytirish.**
    - Ro'yxat yarating: `[1, 2, 3]`.
    - Ro'yxat elementlarini `4` marta ko'paytiring va natijani terminalga chiqaring.

11. **Minimal va Maksimal qiymatni topish.**
    - Quyidagi ro'yxatni yarating: `[25, 17, 9, 50, 33]`.
    - Ro'yxatdagi `eng kichik` va `eng katta` qiymatni toping va terminalga chiqaring.

12. **Ro'yxatni Nusxalash.**
    - Quyidagi ro'yxatni yarating: `[100, 200, 300, 400, 500]`.
    - Ushbu ro'yxatdan `nusxa` ko'chiring va `yangi` ro'yxatni qaytaring.

