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

### ❇️ DEL

📌 Lug'at ichidagi e'lementlarni o'chirish uchun `del` funksiyasidan foydalanamiz.

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

### ❇️ POP

📌 Lug'atdagi e'lementlarni o'chirish uchun `.pop()` metodidan ham foydalansak bo'ladi.

```python
# Telefon ma'lumotlari saqlanayotgan dictionary yaratilmoqda
phone_details = {
    "brand": "Samsung",
    "model": "Galaxy S21",
    "storage": "128GB",
    "price": 900
}

# "storage" kalitli element .pop() orqali o‘chirilmoqda va qiymati o'zgaruvchiga saqlanmoqda
removed_value = phone_details.pop("storage")

# O‘chirilgan qiymat ekranga chiqarilmoqda
print("Removed:", removed_value)

# Yangilangan dictionary ekranga chiqarilmoqda
print(phone_details)
```

## ✅ E'LEMENTLARGA MUROJAT QILISH

### ❇️ KEYS

📌 Kalitlarni olish.

```python
# Foydalanuvchi haqida ma'lumot saqlanmoqda
user_info = {
    "name": "Alice",
    "city": "New York"
}

# Barcha kalitlar (key) alohida olinmoqda
keys = user_info.keys()

# Kalitlar ekranga chiqarilmoqda
print(keys)
```

### ❇️ VALUES

📌 Qiymatlarni olish.

```python
# Foydalanuvchi haqida ma'lumot saqlanmoqda
user_info = {
    "name": "Alice",
    "city": "New York"
}

# Barcha qiymatlar (value) alohida olinmoqda
values = user_info.values()

# Qiymatlar ekranga chiqarilmoqda
print(values)
```
### ❇️ ITEMS

📌 Kalit-qiymat juftliklarini olish:
```python
# Foydalanuvchi haqida ma'lumot saqlanmoqda
user_info = {
    "name": "Alice",
    "city": "New York"
}

# Barcha kalit-qiymat juftliklari alohida olinmoqda
items = user_info.items()

# Juftliklar ekranga chiqarilmoqda
print(items)
```


## ✅ FOYDALI METODLAR

### ❇️ GET

📌 Kalit bo'yicha qiymatni oladi. Kalit mavjud bo'lmasa, `None` qaytaradi.

```python
# Avtomobil haqida ma'lumotlar saqlanmoqda
car_info = {
    "brand": "Chevrolet",
    "model": "Malibu",
    "year": 2022
}

# "model" kaliti orqali qiymat olinmoqda, agar mavjud bo‘lsa — shu qiymat qaytadi
car_model = car_info.get("model", "Not Found")
print("Model:", car_model)  # Natija: Malibu

# "color" degan kalit mavjud emas, shuning uchun "Not Found" qiymati qaytadi
car_color = car_info.get("color", "Not Found")
print("Color:", car_color)  # Natija: Not Found
```
### ❇️ UPDATE

📌 Dictionaryga yangi ma'lumot qo'shish yoki yangilash uchun ishlatiladi.

```python
# Talaba haqida dastlabki ma'lumotlar saqlanmoqda
student_info = {
    "name": "Diyor",
    "age": 18,
    "course": "Python"
}

# update() metodi yordamida yangi ma'lumotlar qo‘shilmoqda yoki mavjudlari yangilanmoqda
student_info.update({
    "age": 19,                # age mavjud edi — yangilanmoqda
    "course": "Django",       # course mavjud edi — yangilanmoqda
    "is_active": True         # yangi kalit — qo‘shilmoqda
})

# Natijani ekranga chiqarish
print(student_info)
```

### ❇️ POPINTEM

📌 Dictionarydan oxirgi qo‘shilgan kalit-qiymat juftligini olib tashlaydi va o‘sha juftlikni qaytaradi.

```python
# Mehmon haqida ma'lumotlar saqlanmoqda
guest_info = {
    "name": "Javlon",
    "room": 305,
    "nights": 3
}

# Oxirgi qo‘shilgan kalit-qiymat juftligi dictionary dan o‘chirilmoqda
removed_item = guest_info.popitem()

# O‘chirilgan juftlik (tuple shaklida) ekranga chiqarilmoqda
print("Removed:", removed_item)

# Yangilangan dictionary ekranga chiqarilmoqda
print("Updated:", guest_info)
```

### ❇️ SETDEFAULT

📌 Kalit mavjud bo'lmasa, qiymat qo'shadi va qaytaradi.

```python
# Foydalanuvchi haqida boshlang‘ich ma’lumotlar
user_info = {
    "username": "umiddev",
    "email": "umid@example.com"
}

# "email" kaliti mavjud bo‘lgani uchun mavjud qiymatni qaytaradi
email = user_info.setdefault("email", "default@example.com")
print("Email:", email)

# "phone" kaliti yo‘q edi, shuning uchun u yaratilib, berilgan qiymat qo‘shiladi
phone = user_info.setdefault("phone", "+998901234567")
print("Phone:", phone)

# Yangilangan dictionary ekranga chiqarilmoqda
print("Updated user_info:", user_info)
```

# ✅ AMALIYOT

## ✅ 1-topshiriq:  
Bo‘sh dictionary yarating va unga quyidagi kalit-qiymatlarni qo‘shing:  
- `"name"`: `"John"`  
- `"age"`: `25`  
- `"city"`: `"Tashkent"`  
So‘ng dictionaryni ekranga chiqaring.

---

## ✅ 2-topshiriq:  
Quyidagi dictionary berilgan:  
```python
person = {"name": "Ali", "age": 30, "job": "Engineer"}
```  
Undagi `"age"` qiymatini `31` ga yangilang va dictionaryni chop eting.

---

## ✅ 3-topshiriq:  
Yuqoridagi `person` dictionarydan `"job"` elementini `del` yordamida o‘chiring.  
Keyin dictionaryni ekranga chiqarib ko‘ring.

---

## ✅ 4-topshiriq:  
Quyidagi dictionarydan `.pop()` metodi yordamida `"model"` kalitli elementni olib tashlang:  
```python
car = {"brand": "BMW", "model": "X5", "year": 2020}
```  
O‘chirilgan qiymatni va yangilangan dictionaryni ekranga chiqaring.

---

## ✅ 5-topshiriq:  
Bo‘sh dictionary yarating va `setdefault()` yordamida quyidagi elementlarni qo‘shing:  
- `"username"`: `"coder123"`  
- `"email"`: `"coder@example.com"`  
Agar `"email"` mavjud bo‘lsa, uni yangilamasin.

---

## ✅ 6-topshiriq:  
Quyidagi dictionarydan `.popitem()` yordamida oxirgi elementni o‘chirib tashlang:  
```python
movie = {"title": "Inception", "director": "Nolan", "year": 2010}
```  
O‘chirilgan element va yangilangan dictionaryni chop eting.

---

## ✅ 7-topshiriq:  
Quyidagi dictionary berilgan:  
```python
student = {"name": "Ziyoda", "course": "Python", "age": 21}
```  
`update()` yordamida quyidagicha o‘zgartiring:  
- `"course"`: `"Django"`  
- `"is_active"`: `True`  
So‘ng natijani chop eting.

---

## ✅ 8-topshiriq:  
Quyidagi dictionarydan `get()` yordamida `"email"` va `"phone"` qiymatlarini ajrating:  
```python
user = {"username": "umiddev", "email": "umid@example.com"}
```  
Agar `"phone"` mavjud bo‘lmasa, `"No number"` qiymatini qaytaring.

---

## ✅ 9-topshiriq:  
Quyidagi dictionaryda `keys()`, `values()`, `items()` metodlaridan foydalanib ularni alohida chop eting:  
```python
laptop = {"brand": "Lenovo", "ram": "16GB", "ssd": "512GB"}
```

---

## ✅ 10-topshiriq:  
Quyidagi dictionary berilgan:  
```python
book = {"title": "Python 101", "author": "Alex", "pages": 300}
```  
Agar `"pages"` kaliti mavjud bo‘lsa — yangilang, mavjud bo‘lmasa — `250` qiymatini qo‘shing.

---

## ✅ 11-topshiriq:  
Quyidagi dictionaryda `"price"` mavjudligini tekshirib ko‘ring va mavjud bo‘lsa — `del` yordamida o‘chirib tashlang:  
```python
product = {"name": "Mouse", "brand": "Logitech", "price": 150000}
```

---

## ✅ 12-topshiriq:  
Quyidagi ikkita dictionaryni `update()` yordamida birlashtiring:  
```python
a = {"a": 1, "b": 2}
b = {"b": 3, "c": 4}
```  
Natijada `a` dictionaryni yangilang va chop eting.

---

## ✅ 13-topshiriq:  
Quyidagi dictionaryga `"skills"` degan yangi kalit qo‘shing va qiymat sifatida `["Python", "SQL"]` ro‘yxatini bering.

---

## ✅ 14-topshiriq:  
Quyidagi dictionaryda `"status"` kaliti mavjud emas.  
`setdefault()` yordamida `"active"` qiymatini qo‘shing:  
```python
account = {"username": "admin"}
```

---

## ✅ 15-topshiriq:  
Quyidagi dictionarydagi barcha kalit va qiymatlarni alohida ro‘yxatlarga ajrating:  
```python
info = {"x": 10, "y": 20, "z": 30}
```  
Kalitlar `keys_list` nomli ro‘yxatga, qiymatlar esa `values_list` nomli ro‘yxatga saqlansin.
