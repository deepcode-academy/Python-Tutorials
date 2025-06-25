# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 6-DARS SETS

📌 Set — bu noyob (takrorlanmaydigan) elementlar dan tashkil topgan, tartibsiz va indekssiz ma’lumot turi.

## ✅ SET YARATISH

```python
# Bo'sh set yaratish
my_set = set()

# Elementlar bilan set yaratish
my_set = {1, 2, 3, 4, 5}
```

## ✅ SETGA E'LEMENT QO'SHISH


```python
# Set yaratamiz
my_set = {1, 2, 3}

# Yangi element qo'shamiz
my_set.add(4)  # 4 element sifatida qo'shiladi
print(my_set)  # Natija: {1, 2, 3, 4}

# Takroriy element qo'shilsa, set o'zgarmaydi
my_set.add(3)  # 3 allaqachon mavjud, shuning uchun set o'zgarmaydi
print(my_set)  # Natija: {1, 2, 3, 4}

# Bir nechta element qo'shamiz
my_set.update([5, 6, 7])  # 5, 6, 7 elementlari qo'shildi
print(my_set)  # Natija: {1, 2, 3, 4, 5, 6, 7}
```

## ✅ SETDAN E'LEMENT O'CHIRISH

```python
# Set yaratamiz
my_set = {1, 2, 3, 4, 5}

# Ma'lum bir elementni o'chiramiz
my_set.remove(3)  # 3 elementi o'chiriladi
print(my_set)  # Natija: {1, 2, 4, 5}

# remove() bilan mavjud bo'lmagan elementni o'chirsak xatolik bo'ladi
# my_set.remove(10)  # KeyError: 10

# discard() bilan element mavjud bo'lmasa ham xatolik bo'lmaydi
my_set.discard(10)  # Xatolik yo'q, set o'zgarishsiz qoladi
print(my_set)  # Natija: {1, 2, 4, 5}
```

## ✅ SET OPERATSIYALARI

### ❇️ .intersection()

📌 intersection — bu ikki yoki undan ortiq to‘plamdagi umumiy elementlarni topadi. Ya’ni, faqat har ikki setda mavjud bo‘lgan elementlargina natijaga olinadi. Agar biror element faqat bir setda bo‘lsa, u intersectionga kirmaydi. Bu amal orqali “ikkalasi orasida qanday o‘xshashlik bor?” degan savolga javob topiladi.

```python
# Ikki set yaratamiz
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# Umumiy elementlarni topamiz (& operatori bilan)
intersection_result = set1 & set2  # Faqat umumiy elementlar
print(intersection_result)  # Natija: {3, 4}

# intersection() metodi bilan
print(set1.intersection(set2))  # Natija: {3, 4}
```

📌 Agar intersection bo‘sh set bilan ishlatilsa, natija ham bo‘sh bo‘ladi.

- Intersection faqat ikkala setda bir vaqtda mavjud bo‘lgan elementlarni qaytaradi.
    - `set1` da: `{1, 2, 3, 4}`
    - `empty_set` da: hech narsa yo‘q → `{}`
    - Demak, ikkala setda mavjud bo‘lgan hech qanday element yo‘q.
    - Shuning uchun natija — bo‘sh set: `set()`

```python
set1 = {1, 2, 3, 4}
empty_set = set()

result = set1 & empty_set  # Bo'sh set bilan kesishish
print(result)  # Natija: set()
```

### ❇️ .difference()

📌 difference esa farqni topadi. Bu amal birinchi setdagi, lekin ikkinchi setda yo‘q bo‘lgan elementlarni ajratib beradi. Bunda faqat birinchi setga xos elementlar natijaga olinadi, umumiy yoki ikkinchisida mavjud bo‘lganlar olinmaydi. Bu orqali “menda bor, unda yo‘q” degan mantiqqa asoslangan natija olinadi.

```python
# Ikkita set yaratamiz
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# set1 dan set2 farqi (ya'ni, set1 dagi, ammo set2 da yo'q elementlar)
diff_result = set1 - set2
print(diff_result)  # Natija: {1, 2}

# difference() metodi bilan
print(set1.difference(set2))  # Natija: {1, 2}
```


### ❇️ .union()

📌 union esa barcha elementlarni birlashtiradi. Ya’ni, har ikki setdagi barcha elementlar bitta setga yig‘iladi va takrorlanmas holda saqlanadi. Union orqali “ikkovining jamlanmasi” olinadi. Bu amal barcha mavjud ma’lumotlarni umumlashtirish, birlashtirish uchun ishlatiladi.



```python
# Ikkita set yaratamiz
set1 = {1, 2, 3}
set2 = {3, 4, 5}

# Barcha elementlarni birlashtiramiz (takroriylar olib tashlanadi)
union_result = set1 | set2
print(union_result)  # Natija: {1, 2, 3, 4, 5}

# union() metodi bilan
print(set1.union(set2))  # Natija: {1, 2, 3, 4, 5}
```

## ✅ FROZENSET

- frozenset nima?
    - frozenset — bu **o‘zgarmas set** turidir. Ya’ni:
    - Oddiy **set** bilan bir xil ishlaydi, lekin uni yaratgandan so‘ng o‘zgartirib bo‘lmaydi.
    - Ichiga noyob elementlar saqlanadi.
    - **Tartibsiz** va **indekssiz**.
    - Undan **.add()**, **.remove()** kabi metodlar ishlamaydi, chunki u o‘zgartirilmaydi.

## ✅ FROZENSET YARATISH

```python
# Oddiy ro'yxat yaratamiz
my_list = [1, 2, 3, 4, 5]

# Ro'yxatdan frozenset yaratamiz
my_frozen_set = frozenset(my_list)

print(my_frozen_set)  # Natija: frozenset({1, 2, 3, 4, 5})
```

## ✅ FROZENSETDA .intersection() va .union() .difference()

```python
a = frozenset([1, 2, 3])
b = frozenset([2, 3, 4])

# intersection
print(a & b)  # Natija: frozenset({2, 3})

# union
print(a | b)  # Natija: frozenset({1, 2, 3, 4})

# difference
print(a - b)  # Natija: frozenset({1})
```



## AMALIYOT
- `my_list = [1, 2, 2, 3, 4, 4, 5]` <br>
Berilgan listdagi takroriy elementlarni olib tashlab, yangi to'plam yarating.
- `set1 = {1, 2, 3, 4}` <br>
`set2 = {3, 4, 5, 6}` <br>
Ikki to'plamdan umumiy elementlarni toping.
- `set1 = {1, 2, 3, 4}` <br>
`set2 = {3, 4, 5, 6}` <br>
Birinchi to'plamda mavjud, ikkinchi to'plamda mavjud bo'lmagan elementlarni aniqlang.
- `set1 = {1, 2, 3, 4}` <br>
`set2 = {3, 4, 5, 6}` <br>
`set3 = {5, 6, 7, 8}` <br>
Uchta to'plamdan umumiy bo'lmagan elementlarni aniqlang.
- `my_set = {5, 2, 9, 1, 7}` <br>
Berilgan to'plamning eng kichik va eng katta elementlarini toping.