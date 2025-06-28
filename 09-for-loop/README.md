# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 9-DARS FOR LOOP

📌 for – bu **tsikl operatori**, ya’ni **takrorlovchi kod**. Agar sizda bir nechta qiymatlar bo‘lsa (masalan, ro‘yxat, sonlar, harflar), for tsikli ularni **birma-bir** olib, har biriga bir xil amalni bajarish uchun ishlatiladi.

```python
# 'salom' degan matnli o'zgaruvchi yaratildi
soz = "salom"

# soz o'zgaruvchisidagi har bir harf bo'yicha yuramiz
for harf in soz:
    # Har bir harfni alohida qilib ekranga chiqaramiz
    print(harf)
```


## ✅ LISTLAR BILAN ISHLASH

📌 Ro'yxatlar eng keng tarqalgan takrorlanadigan obyektlardan biri hisoblanadi.


🎯 Buyurtmalar ro‘yxatini ekranga chiqarish

```python
# Buyurtma qilingan mahsulotlar ro'yxati
orders = ["bread", "milk", "eggs", "cheese"]

# Har bir mahsulot bo'yicha yurib chiqamiz
for item in orders:
    # Mahsulot nomini ekranga chiqaramiz
    print(f"Ordered item: {item}")
```

🎯 Narxlar ro'yxati bilan umumiy xarajatni hisoblash

```python
# Har bir mahsulot narxi (dollar)
prices = [2.5, 1.0, 3.2, 4.8]

# Umumiy summa uchun o'zgaruvchi
total_cost = 0

# Har bir narx ustida yuramiz
for price in prices:
    # Narxni umumiy summaga qo'shamiz
    total_cost += price

# Umumiy narxni ekranga chiqaramiz
print(f"Total cost: ${total_cost}")
```

🎯 Email ro'yxatidan foydalanuvchilarga xabar yuborish (simulyatsiya)

```python
# Email manzillar ro'yxati
emails = ["ali@example.com", "vali@example.com", "sara@example.com"]

# Har bir foydalanuvchiga xabar yuboramiz (simulyatsiya)
for email in emails:
    # Xabar yuborilganini bildiruvchi matn
    print(f"Sending email to: {email}")
```

🎯 Login bo‘lgan foydalanuvchilarni filtrlash

```python
# Foydalanuvchilar va ularning login statusi (True - tizimga kirgan)
users = [
    {"username": "admin", "logged_in": True},
    {"username": "john", "logged_in": False},
    {"username": "alice", "logged_in": True},
]

# Faqat login bo'lgan foydalanuvchilarni chiqaramiz
for user in users:
    if user["logged_in"]:
        print(f"{user['username']} is currently online.")
```

🎯 Mahsulot narxlarini chegirma bilan yangilash

```python
# Mahsulotlar va ularning narxlari ro'yxati
products = [
    {"name": "laptop", "price": 1000},
    {"name": "keyboard", "price": 100},
    {"name": "mouse", "price": 50},
]

# Har bir mahsulotga 10% chegirma beramiz
for product in products:
    # Chegirma miqdorini hisoblaymiz
    discount = product["price"] * 0.1
    # Narxni yangilaymiz
    product["price"] -= discount

# Natijani chiqaramiz
print("Discounted products:")
for product in products:
    print(f"{product['name']}: ${product['price']}")
```

🎯 Foydalanuvchi ismlarini bosh harf bilan yozib chiqish

```python
# Foydalanuvchilar ismlari ro'yxati (kichik harflarda)
usernames = ["ali", "sara", "bekzod", "nigora"]

# Har bir ismni bosh harf bilan yangilaymiz
for i in range(len(usernames)):
    # `.capitalize()` birinchi harfni katta qiladi
    usernames[i] = usernames[i].capitalize()

# Natijani chiqaramiz
print("Capitalized usernames:", usernames)
```

🎯 Sonlar ro'yxatidan faqat toq sonlarni ajratib olish

```python
# Sonlar ro'yxati
numbers = [4, 7, 12, 9, 15, 2, 8]

# Faqat toq sonlar uchun yangi ro'yxat
odd_numbers = []

# Har bir sonni tekshiramiz
for number in numbers:
    if number % 2 != 0:
        # Toq bo'lsa yangi ro'yxatga qo'shamiz
        odd_numbers.append(number)

# Natijani chiqaramiz
print("Odd numbers:", odd_numbers)
```

## ✅ RANGE

📌 Python dasturlash tilida `range()` funksiyasi ketma-ket sonlar qatorini yaratish uchun ishlatiladi. Bu funksiya odatda `for` loop bilan birga ishlatiladi va bizga ma’lum bir sonlar oralig‘ida takrorlash (aylanib chiqish) imkonini beradi.


🎯 Oddiy **range()** ishlatilishi

```python
# 0 dan 4 gacha (5 kirmaydi)
for i in range(5):
    print(i)
```

🎯 Belgilangan oraliqdagi qiymatlar

```python
# 3 dan 8 gacha bo'lgan sonlarni chiqaramiz
for i in range(3, 9):
    print(i)
```

🎯 Step bilan yurish

```python
# 0 dan 10 gacha bo'lgan juft sonlarni chiqaramiz (2 qadam bilan)
for index in range(0, 11, 2):
    print(index)
```

🎯 Orqaga qarab sanash

```python
# 10 dan 1 gacha orqaga qarab
for i in range(10, 0, -1):
    print(i)
```

🎯 Har bir foydalanuvchiga ID berish

```python
# 3 ta foydalanuvchi nomi
users = ["Ali", "Vali", "Sardor"]

# Foydalanuvchilarga ID raqam berish (1 dan boshlab)
for i in range(len(users)):
    print(f"User ID: {i+1} - Name: {users[i]}")
```

## ✅ DICTIONARY BILAN ISHLASH


🎯 Foydalanuvchi profillari ro‘yxati

```python
# Bir nechta foydalanuvchilarning profillari
users = [
    {"username": "ali", "email": "ali@example.com", "is_active": True},
    {"username": "sara", "email": "sara@example.com", "is_active": False},
    {"username": "diyor", "email": "diyor@example.com", "is_active": True},
]

# Faqat aktiv foydalanuvchilarni chiqaramiz
for user in users:
    if user["is_active"]:
        print(f"{user['username']} (email: {user['email']}) is active.")
```

🎯 Savatdagi mahsulotlar va umumiy narxni hisoblash

```python
# Xarid savatidagi mahsulotlar
cart = [
    {"name": "laptop", "price": 850.0, "quantity": 1},
    {"name": "mouse", "price": 25.0, "quantity": 2},
    {"name": "keyboard", "price": 45.0, "quantity": 1},
]

# Umumiy narxni hisoblaymiz
total = 0
for item in cart:
    total += item["price"] * item["quantity"]

print(f"Umumiy summa: ${total}")
```

🎯 Talabalar baholari bo‘yicha statistika

```python
# Talabalar va ularning baholari
grades = {
    "Ali": 87,
    "Sardor": 92,
    "Nigora": 78,
    "Lola": 85
}

# O‘rtacha bahoni hisoblaymiz
average = sum(grades.values()) / len(grades)
print(f"O‘rtacha baho: {average}")
```

🎯 Chegirma tizimi (promo code)

```python
# Promo kodlar va ularning chegirmalari (%)
promo_codes = {
    "SALE10": 10,
    "WELCOME15": 15,
    "VIP20": 20
}

code = input("Promo kodni kiriting: ").upper()

# Kodni tekshirib chegirma beramiz
if code in promo_codes:
    print(f"Sizga {promo_codes[code]}% chegirma berildi!")
else:
    print("Noto‘g‘ri promo kod!")
```

🎯 API javobini tahlil qilish (dictionary ko‘rinishida)

```python
# API dan kelgan javob
response = {
    "status": "success",
    "data": {
        "id": 102,
        "title": "New blog post",
        "author": "Umid",
        "views": 1234
    }
}

# Ma'lumotni tahlil qilish
if response["status"] == "success":
    blog = response["data"]
    print(f"Post: {blog['title']} (Author: {blog['author']}) — {blog['views']} views")
else:
    print("Xatolik yuz berdi.")
```

## ✅ SETS BILAN ISHLASH

🎯 Foydalanuvchi kirgan sahifalarni yagona ro‘yxatga olish

```python
# Sahifalar bo'yicha foydalanuvchi harakati (ba'zilari takrorlangan)
visited_pages = ["home", "about", "contact", "home", "products", "contact"]

# Takrorlangan sahifalarni set orqali avtomatik chiqarib tashlaymiz
unique_pages = set(visited_pages)

print("Foydalanuvchi kirgan noyob sahifalar:")
for page in unique_pages:
    print(page)
```

🎯 Email ro'yxatlaridagi dublikatlarni olib tashlash

```python
# Ro'yxatda takrorlanuvchi email manzillar bor
emails = [
    "ali@example.com",
    "sara@example.com",
    "ali@example.com",
    "jamshid@example.com",
    "sara@example.com"
]

# set yordamida faqat noyob email manzillarni olamiz
unique_emails = set(emails)

print("Yagona email manzillar:")
for email in unique_emails:
    print(email)
```

🎯 Ikkita foydalanuvchi orasidagi umumiy do‘stlarni topish

```python
# Foydalanuvchilarning do'stlari
friends_1 = {"Ali", "Sara", "Lola", "Bekzod"}
friends_2 = {"Lola", "Sardor", "Ali", "Diyor"}

# Umumiy do'stlar: kesishma (intersection)
common_friends = friends_1 & friends_2

print("Umumiy do'stlar:")
print(common_friends)
```

🎯 Ro‘yxatdan o‘tgan foydalanuvchilar va online foydalanuvchilar orasidagi farq

```python
# Ro'yxatdan o‘tgan foydalanuvchilar
registered_users = {"ali", "sara", "diyor", "nigora"}

# Hozir online bo'lgan foydalanuvchilar
online_users = {"ali", "sardor"}

# Faqat ro'yxatdan o‘tgan, lekin online bo'lmaganlar
offline_users = registered_users - online_users

print("Hozir offline foydalanuvchilar:")
print(offline_users)
```

## ✅ TUPLE BILAN ISHLASH

🎯 Oddiy tuple ustidan for tsik

```python
# Koordinatalar (o'zgarmas qiymatlar)
coordinates = (10, 20, 30)

# Har bir koordinatani chiqarish
for coordinate in coordinates:
    print(coordinate)
```

🎯 Mahsulotlar ro‘yxati tupleda (ID, nomi, narxi)

```python
# Har bir mahsulot: (id, nomi, narxi)
products = (
    (1, "Laptop", 1200),
    (2, "Mouse", 30),
    (3, "Keyboard", 50),
)

# Mahsulotlar haqida to‘liq ma’lumot chiqaramiz
for product_id, name, price in products:
    print(f"ID: {product_id}, Nomi: {name}, Narxi: ${price}")
```

## ✅ NESTED LOOPS


🎯 2D ro'yxat (matritsa) elementlarini ko‘rsatish

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in matrix:
    for element in row:
        print(element, end=" ")
    print()  # Qator oxirida yangi qatorga o'tish
```

📌 Python dasturlash tilida `print()` funksiyasi biror narsani ekranga chiqargandan so‘ng avtomatik tarzda yangi qatorga o‘tadi. Bu yangi qator belgisi `\n` deb ataladi. Ammo ba’zida har bir chiqishdan keyin yangi qatorga o‘tmasdan, boshqa belgi (masalan, bo‘sh joy yoki vergul) qo‘yishni xohlaysiz. Shu holatda `print()` funksiyasida `end` parametri ishlatiladi.

🎯 Foydalanuvchilar va ularning telefon raqamlari

```python
# Har bir foydalanuvchining bir nechta telefon raqami bor
users = {
    "Ali": ["+998901112233", "+998912223344"],
    "Sara": ["+998933445566"],
    "Diyor": ["+998935551234", "+998998887766"]
}

# Har bir foydalanuvchi va raqamlarini chiqaramiz
for name, phones in users.items():
    print(f"{name}ning raqamlari:")
    for phone in phones:
        print(f" - {phone}")
```

🎯 Kategoriya va mahsulotlar

```python
# Mahsulotlar toifalar bo'yicha guruhlangan
categories = {
    "Elektronika": ["Telefon", "Noutbuk", "Smart soat"],
    "Kiyim": ["Ko‘ylak", "Shim", "Poyabzal"],
    "Oziq-ovqat": ["Non", "Sut", "Yog‘"]
}

# Har bir kategoriya va mahsulotlarini chiqaramiz
for category, items in categories.items():
    print(f"{category}:")
    for item in items:
        print(f" - {item}")
```

🎯 Sayt menyusini chiqarish (asosiy bo‘lim + ichki bo‘limlar)

```python
# Sayt menyusi
menu = {
    "Bosh sahifa": [],
    "Kurslar": ["Python", "Django", "Flask"],
    "Aloqa": ["Biz haqimizda", "Bog‘lanish"]
}

# Menyuni chiqaramiz
for main_menu, submenus in menu.items():
    print(main_menu)
    for submenu in submenus:
        print(f"  - {submenu}")
```

## ✅ FOR ELSE

📌 Python dasturlash tilida `for...else` bu — `for` tsikli bilan birga ishlatiladigan maxsus konstruktsiya bo‘lib, u orqali loop muvaffaqiyatli tugaganidan keyin `else` qismi bajariladi.

🎯 Foydalanuvchi ro‘yxatida admin borligini tekshirish

```python
users = ["ali", "sara", "lola", "jamshid"]

for user in users:
    if user == "admin":
        print("Admin foydalanuvchi topildi.")
        break
else:
    print("Admin foydalanuvchi ro'yxatda yo'q.")
```

🎯 Parol to‘g‘riligini tekshirish

```python
# Parollar bazasi
correct_passwords = ["pass123", "admin456", "qwerty789"]

user_input = "admin456"

for password in correct_passwords:
    if user_input == password:
        print("Parol to'g'ri.")
        break
else:
    print("Parol noto'g'ri.")
```


## ✅ BREAK

📌 `break` operatori loopni to'xtatadi. Bu operator `for` yoki `while` loopda ishlatilishi mumkin. `break` loopning bajarilishini to'xtatadi va loopdan chiqadi, hatto loop to'liq tugamagan bo'lsa ham.

🎯 Ma’lumotlar bazasidan kerakli foydalanuvchini topish

```python
# Foydalanuvchilar ro'yxatini lug'atlar ko'rinishida yaratdik
users = [
    {"id": 1, "name": "Ali"},
    {"id": 2, "name": "Sara"},
    {"id": 3, "name": "Diyor"}
]

# Qidirilayotgan foydalanuvchining ID raqamini belgiladik
searched_id = 2

# users ro'yxatidagi har bir element (ya'ni foydalanuvchi) bo'yicha yuramiz
for user in users:
    # Agar foydalanuvchining 'id' qiymati qidirilayotgan id ga teng bo'lsa
    if user["id"] == searched_id:
        # Foydalanuvchi topilganini ekranga chiqaramiz
        print(f"Foydalanuvchi topildi: {user['name']}")
        # Qolgan elementlarni tekshirishning hojati yo'q, loop ni to'xtatamiz
        break
```

🎯 API javobidan kerakli postni topish


```python
# Postlar listini yaratdik, har bir post dictionary ko'rinishida berilgan
posts = [
    {"id": 1, "title": "Salom"},
    {"id": 2, "title": "Python haqida"},
    {"id": 3, "title": "Xayr"}
]

# Qidirilayotgan postning sarlavhasini belgiladik
search_title = "Python haqida"

# posts listdagi har bir post bo'yicha yuramiz
for post in posts:
    # Agar postning 'title' qiymati qidirilayotgan sarlavhaga teng bo'lsa
    if post["title"] == search_title:
        # Post topilganini ekranga chiqaramiz
        print("Post topildi:", post)
        # Endi qolgan postlarni tekshirishning hojati yo'q, loop ni to'xtatamiz
        break
```

🎯 for + else bilan birga break ishlatish

```python
# Shaharlar nomlari yozilgan ro'yxat yaratildi
cities = ["Toshkent", "Samarqand", "Buxoro", "Xiva"]

# Qidirilayotgan shahar nomi belgilanmoqda
search = "Andijon"

# cities ro'yxatidagi har bir shahar ustida yurib chiqamiz
for city in cities:
    # Agar ro'yxatdagi shahar nomi qidirilayotgan nomga teng bo‘lsa
    if city == search:
        # Ekranga topilganligi haqida xabar chiqaramiz
        print("Shahar topildi!")
        # Endi boshqa shaharlarni tekshirish shart emas, loop to‘xtatiladi
        break
# Agar loop oxirigacha borib chiqqan bo‘lsa va break ishlamagan bo‘lsa
else:
    # Demak shahar ro'yxatda yo‘q, degan xabar chiqariladi
    print("Shahar ro'yxatda yo'q.")
```


## ✅ CONTINUE

📌 Python dasturlash tilida continue operatori tsikl ichida ishlatiladigan boshqaruvchi buyruq bo‘lib, u ishga tushganda tsikldagi shu takrorlanishning qolgan qismini o‘tkazib yuboradi va keyingi takrorlanishga (iteration) o‘tadi.

```python
# Sonlardan iborat ro'yxat yaratildi
sonlar = [1, 2, 3, 4, 5]

# sonlar ro'yxatidagi har bir son bo'yicha yuramiz
for son in sonlar:
    # Agar hozirgi son 2 ga bo‘linganda qoldiq 0 bo‘lsa, ya’ni juft bo‘lsa
    if son % 2 == 0:
        # Bu sonni tashlab o‘tamiz va loop keyingi son bilan davom etadi
        continue
    # Agar son toq bo‘lsa (ya’ni yuqoridagi shart bajarilmagan bo‘lsa), uni chiqaramiz
    print(son)
```

🎯 Faqat musbat sonlarni chiqarish

```python
# Musbat va manfiy sonlardan iborat ro'yxat yaratildi
sonlar = [-1, 2, -3, 4, -5]

# sonlar ro'yxatidagi har bir son bo'yicha yuramiz
for son in sonlar:
    # Agar hozirgi son 0 dan kichik bo‘lsa, ya’ni manfiy bo‘lsa
    if son < 0:
        # Manfiy sonni chiqarib o‘tib ketamiz, ya’ni pastdagi qator bajarilmaydi
        continue
    # Faqat musbat sonlar (0 va undan katta) shu yerda ekranga chiqariladi
    print(son)
```

🎯 Faqat juft indeksli mevalarni chiqarish

```python
# Mevalardan iborat ro'yxat yaratildi
mevalar = ['olma', 'banan', 'apelsin', 'anjir']

# range() funksiyasi orqali indekslar bo'yicha 0 dan len(mevalar) gacha yuramiz
for i in range(len(mevalar)):
    # Agar hozirgi indeks toq bo‘lsa (ya'ni 1, 3, ...)
    if i % 2 != 0:
        # Bu indeksdagi elementni o‘tkazib yuboramiz va loop davom etadi
        continue
    # Faqat juft indeks (0, 2, ...) dagi mevalar ekranga chiqariladi
    print(mevalar[i])
```



## ✅ PASS

📌 Python dasturlash tilida pass operatori — bu hech qanday amal bajarmaydigan buyruq. Ya’ni, u bo‘sh kod blokini vaqtincha to‘ldirish uchun ishlatiladi.

```python
# 0 dan 4 gacha bo‘lgan sonlar ustida aylanuvchi for tsikli
for son in range(5):
    # Agar son 3 ga teng bo‘lsa
    if son == 3:
        pass  # Hech qanday amal bajarmaymiz, faqat kod sintaksisini saqlab qolamiz
    else:
        print(son)  # Aks holda, sonni ekranga chiqaramiz
```

🎯 Kod hali yozilmagan, lekin struktura tayyor bo‘lishi kerak

```python
def validate_user_input():
    # Bu funksiya foydalanuvchi kiritgan ma'lumotni tekshiradi
    pass  # Keyinroq bu yerga tekshirish kodi yoziladi
```

🎯 Bo‘sh class yaratish

```python
class PaymentSystem:
    pass  # Bu class keyin to‘ldiriladi
```

🎯 Exception (xatolik)ni vaqtincha e'tiborga olmaslik

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    pass  # Hozircha xatoni ko‘rsatmaymiz, faqat chetlab o‘tamiz
```

🎯 Bo‘sh if yoki for bloklarida sintaksis xatosidan saqlanish

```python
users = ["admin", "user", "guest"]

for user in users:
    if user == "admin":
        pass  # Hozircha admin uchun alohida ish yo‘q
    else:
        print(f"{user} uchun oddiy xush kelibsiz")
```


# ✅ AMALIYOT

## ✅ 1-topshiriq:
Foydalanuvchi kiritgan natural son uchun 1 dan shu songacha bo‘lgan sonlar yig‘indisini for loop orqali hisoblang.

---

## ✅ 2-topshiriq:
Quyidagi ro‘yxatda nechta elementda eng kamida 2 ta unli harf borligini aniqlang:
```python
words = ["apple", "sky", "queue", "book", "cry"]
```

---

## ✅ 3-topshiriq:
Ro‘yxatda eng katta va eng kichik sonning farqini toping:
```python
numbers = [7, 12, -3, 8, 0, 15]
```

---

## ✅ 4-topshiriq:
Foydalanuvchi 10 ta son kiritadi. For loop orqali faqat musbat va toq sonlarni yangi ro‘yxatga yozing.

---

## ✅ 5-topshiriq:
Quyidagi ro‘yxatdagi har bir so‘zning birinchi va oxirgi harfini birlashtirib yangi ro‘yxat hosil qiling:
```python
words = ["python", "apple", "code", "loop"]
# natija: ["pn", "ae", "ce", "lp"]
```

---

## ✅ 6-topshiriq:
Ro‘yxatdan faqat 3 ga va 5 ga bo‘linadigan sonlarni ajratib, ularning o‘rtacha qiymatini hisoblang:
```python
nums = [5, 9, 15, 20, 22, 30, 35]
```

---

## ✅ 7-topshiriq:
Foydalanuvchi matn kiritadi. Matndagi raqamlarni topib, ularni son sifatida yig‘indisini hisoblang.
> Masalan: "salom12dunyo3" => natija: 15

---

## ✅ 8-topshiriq:
Berilgan ro‘yxatdan elementlarning indekslari juft bo‘lganlarini alohida ro‘yxatga chiqarib bering:
```python
fruits = ["olma", "banan", "gilos", "anor", "nok", "shaftoli"]
```

---

## ✅ 9-topshiriq:
Ro‘yxatda ketma-ket 2 marta uchraydigan elementlarni aniqlang:
```python
items = [1, 2, 2, 3, 4, 4, 4, 5]
# natija: 2, 4
```

---

## ✅ 10-topshiriq:
Foydalanuvchi kiritgan matndan faqat bosh harflarni ajratib, bitta string qilib chiqaring.
> Masalan: "Salom DunYo" => "SDY"

---

## ✅ 11-topshiriq:
Quyidagi ro‘yxatdan palindrom (teskari o‘qilganda ham bir xil) so‘zlarni ajratib chiqaring:
```python
words = ["anna", "python", "level", "loop", "radar"]
```

---

## ✅ 12-topshiriq:
for loop yordamida 100 dan kichik Fibonacci sonlarini ro‘yxatga yig‘ing.

---

## ✅ 13-topshiriq:
Ro‘yxatda nechta elementda harflar soni raqamlar sonidan ko‘p ekanini hisoblang:
```python
elements = ["abc123", "hello", "42", "py2025", "test"]
```

---

## ✅ 14-topshiriq:
Ro‘yxatdagi sonlardan har birining raqamlari yig‘indisini hisoblab, yangi ro‘yxatga joylang:
```python
nums = [12, 305, 47, 88]
# natija: [3, 8, 11, 16]
```

---

## ✅ 15-topshiriq:
Ro‘yxatdagi elementlardan faqat birinchi harfi har doim katta, qolganlari kichik bo‘lgan yangi ro‘yxat yarating:
```python
names = ["aNVAR", "mUROD", "dILSHOD"]
# natija: ["Anvar", "Murod", "Dilshod"]
```