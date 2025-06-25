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




- To'plamlarda `.difference()` metodi bir setdagi elementlarni boshqa setdagi elementlardan chiqarib tashlash uchun ishlatiladi. Natijada birinchi setda bor, lekin ikkinchi (yoki ko'proq) setda yo'q bo'lgan elementlar qaytariladi.

Python dasturlash tilida setlar farqini topish oshirish uchun bir nechta usullar mavjud:

- **`-` operatori:** .difference() metodi uchun maxsus operator.

```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

difference_set = set1 - set2
print(difference_set)  # Natija: {1, 2}
```

- **`difference()` metodi:** Bir yoki bir nechta to'plamlar(set) farqlarini tekshiradi.

```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

difference_set = set1.difference(set2)
print(difference_set)  # Natija: {1, 2}
```

- To'plamlarda `.union()` (**birlashtirish**) metodi ikki yoki undan ortiq to'plamlarning barcha elementlarini yagona to'plamda birlashtirish uchun ishlatiladi. Natijada barcha to'plamlardan elementlar qaytariladi, takroriy elementlar faqat bitta marta saqlanadi.

Python dasturlash tilida to'plamlarni birlashtirilishini amalga oshirish uchun bir nechta usullar mavjud:

- **`|` operatori:** Birlashtirish amali uchun maxsus operator.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

union_set = set1 | set2
print(union_set)  # Natija: {1, 2, 3, 4, 5}
```

- **`.union()` metodi:** Bir yoki bir nechta to'plamlarni birlashtiradi.

```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

union_set = set1.union(set2)
print(union_set)  # Natija: {1, 2, 3, 4, 5}
```

> [!NOTE]
> Birlashtirilgan to'plamda har bir element faqat bir marta bo‘ladi, ya'ni takroriy elementlar olib tashlanadi.

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