# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 7-DARS DICTIONARY

## ✅ DICTIONARY NIMA?

📌 Python dasturlash tilida dictionary — bu kalit-qiymat (key-value) juftliklarini saqlovchi ma’lumotlar turidir. Har bir kalit yagona bo‘ladi va unga mos qiymat bo‘ladi. Dictionary ma’lumotlar `{}` qavslar ichida yoziladi va har bir kalit bilan qiymat `:` bilan ajratiladi. Bu ma'lumot turi ma’lumotlarni tartibli saqlash, oson topish va boshqarish uchun ishlatiladi.

## ✅ DICTIONARY YARATISH

### ❇️ BO'SH DICTIONARY YARATISH

```python
# Bo'sh dictionary yaratish
user_info = {}
```

### ❇️ E'LEMENTLAR BILAN DICTIONARY YARATISH

```python
# Kalit-qiymatlar bilan dictionary yaratish
user_info = {
    'name': 'Alice',         # Foydalanuvchining ismi
    'age': 30,               # Foydalanuvchining yoshi
    'city': 'New York'       # Foydalanuvchining shahri
}
```

## ✅ DICTIONARYGA E'LEMENT QO'SHISH

📌 Dictionaryga e'lement qo'shish uchun o'zgaruvchi nomidan kn `[]` qavs ochib ichiga keyni beramiz, undan keyin qo'shmoqchi bo'lgan value yani qiymatni beramiz.

```python
# Bo'sh dictionary yaratilyapti
student_info = {}

# Dictionary ga yangi kalit-qiymat juftligi qo‘shilmoqda: ism
student_info["name"] = "Umid"

# Dictionary ga yangi kalit-qiymat juftligi qo‘shilmoqda: yosh
student_info["age"] = 20

# Dictionary ga yangi kalit-qiymat juftligi qo‘shilmoqda: kurs
student_info["course"] = "Python Programming"

# Dictionary ga yangi kalit-qiymat juftligi qo‘shilmoqda: talabalik holati
student_info["is_student"] = True

# Natijani ekranga chiqarish
print(student_info)
```

## ✅ E'LEMENTLARNI YANGILASH

```python
# Talaba haqida ma'lumotlarni saqlovchi dictionary yaratilmoqda
student_profile = {
    "full_name": "Azizbek Tursunov",
    "age": 19,
    "faculty": "Computer Science",
    "is_active": True
}

# "age" kalitiga yangi yosh qiymati berilmoqda (19 dan 20 ga yangilanmoqda)
student_profile["age"] = 20

# "faculty" kalitidagi qiymat o‘zgartirilmoqda (Computer Science dan Data Science ga)
student_profile["faculty"] = "Data Science"

# "is_active" kalitidagi qiymat yangilanmoqda (True dan False ga)
student_profile["is_active"] = False

# Natija ekranga chiqarilmoqda
print(student_profile)
```

## ✅ E'LEMENT O'CHIRISH

- Lug'at ichidagi e'lementlarni o'chirish uchun `del` funksiyasidan foydalanamiz:
```python
# Kitob haqida ma'lumotlar saqlanayotgan dictionary yaratilmoqda
book_info = {
    "title": "Python Basics",
    "author": "John Smith",
    "year": 2021,
    "price": 150000
}

# "price" kalitidagi element dictionary dan o‘chirilmoqda
del book_info["price"]

# Natija ekranga chiqarilmoqda
print(book_info)
```
- Lug'atdagi e'lementlarni o'chirish uchun `.pop()` metodidan ham foydalansak bo'ladi:
```python
age = my_dict.pop('age')
print(age)  # 26
print(my_dict)  # {'name': 'Alice', 'city': 'New York'}
```

### E'LEMENTLARNI KO'RISH
- Kalitlarni olish:
```python
keys = my_dict.keys()
print(keys)  # dict_keys(['name', 'city'])
```
- Qiymatlarni olish:
```python
values = my_dict.values()
print(values)  # dict_values(['Alice', 'New York'])
```
- Kalit-qiymat juftliklarini olish:
```python
items = my_dict.items()
print(items)  # dict_items([('name', 'Alice'), ('city', 'New York')])
```

### LUG'ATLARNI BOSHQARISH

- Lug'atni tozalash uchun `.clear()` metodidan foydalanamiz:
```python
my_dict.clear()
print(my_dict)  # {}
```
- Lug'atni nusxalash uchun `.copy()` metodidan foydalanamiz:
```python
new_dict = my_dict.copy()
print(new_dict)
```

### LUG'ATLARDA FOYDALI METODLAR
- **`.get()` metodi:** Kalit bo'yicha qiymatni olish (kalit mavjud bo'lmasa, `None` qaytaradi).
```python
name = my_dict.get('name', 'Not Found')
print(name)  # 'Alice'
```
- **`.setdefault()` metodi:** Kalit mavjud bo'lmasa, qiymat qo'shadi va qaytaradi.
```python
country = my_dict.setdefault('country', 'USA')
print(country)  # 'USA'
print(my_dict)  # {'name': 'Alice', 'city': 'New York', 'country': 'USA'}
```

## AMALIYOT

- otam (onam, akam, ukam, va hokazo) degan lug'at yarating va lug'atga shu inson haqida kamida 3 ta m'alumot kiriting (ismi, tu'gilgan yili, shahri, manzili va hokazo). Lug'atdagi ma'lumotni matn shaklida konsolga chiqaring: `Otamning ismi Mavlutdin, 1954-yilda, Samarqand viloyatida tug'ilgan`

- Oila a'zolaringizning sevimli taomlari lug'atini tuzing. Lug'atda kamida 5 ta ism-taom jufltigi bo'lsin. Kamida uch kishining sevimli taomini konsolga chiqaring: `Alining sevimli taomi osh`

- Berilgan `student` lug'atidagi age kalitining qiymatini `1` ga oshiring va yangi `grade` kalit-qiymat juftligini qo'shing.
```python
student = {
    'name': 'Alice',
    'age': 21,
    'major': 'Mathematics'

    # student = {'name': 'Alice', 'age': 22, 'major': 'Mathematics', 'grade': 'A'}
}
```

- Berilgan `employee` lug'atidan `department` kalitini o'chiring va yangi lug'atni chop eting.
```python
employee = {
    'name': 'John',
    'age': 30,
    'position': 'Manager',
    'department': 'Sales'

    # employee = {'name': 'John', 'age': 30, 'position': 'Manager'}
}
```

- `grades` lug'atidagi barcha qiymatlarning yig'indisini hisoblang va natijani chop eting.
```python
grades = {
    'Math': 90,
    'Science': 85,
    'English': 92,
    'History': 88

    # Yig'indi: 355
}
```

- `scores` lug'atidagi `eng kichik` va `eng katta` qiymatlarni toping va ularni chop eting.
```python
scores = {
    'player1': 35,
    'player2': 42,
    'player3': 28,
    'player4': 50

    # Eng kichik qiymat: 28
    # Eng katta qiymat: 50
}
```