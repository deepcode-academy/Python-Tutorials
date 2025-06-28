# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 9-DARS FOR LOOP

📌 for – bu **tsikl operatori**, ya’ni **takrorlovchi kod**. Agar sizda bir nechta qiymatlar bo‘lsa (masalan, ro‘yxat, sonlar, harflar), for tsikli ularni **birma-bir** olib, har biriga bir xil amalni bajarish uchun ishlatiladi.


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


### `continue` OPERATORI
> [!NOTE] 
> `continue` operatori **for loop** ichida ishlatiladi va u **for loop**ning takrorlanishini to'xtatib, keyingi takrorlashga o'tadi. Ya'ni, `continue` operatori **for loop** ichidagi qolgan kodni bajarishdan voz kechib, **for loop**ning keyingi takrorlanishga o'tishni ta'minlaydi.
- `continue` operatoridan foydalanish:
    - Agar **for loop** ichida muayyan shart bajarilganda qolgan kodlarni bajarish kerak bo'lmasa, `continue` operatoridan foydalaniladi.
```python
sonlar = [1, 2, 3, 4, 5]

for son in sonlar:
    if son % 2 == 0:
        continue
    print(son)
```
- `continue` operatorining foydalari
    - **Shart Bajarilganda Kodni O'tkazib Yuborish:** Agar siz **for loop**ning qolgan qismidagi kodni o'tkazib yuborishni xohlasangiz, `continue` operatori juda foydali bo'lishi mumkin.
    - **Tajriba Va Shartlarga Ko'ra Kodni Soddalashtirish:** `continue` operatori yordamida siz ko'proq shartni tekshirishni oldini olishingiz mumkin, bu esa kodingizni soddalashtiradi va o'qilishini yaxshilaydi.
    - **For loopni Boshqarish:** `continue` operatori **for loop**ni boshqarishga yordam beradi, masalan, ba'zi holatlarda faqat muayyan shart bajarilganida kod bajarilishi kerak bo'lganda.

- Faqat musbat sonlarni chiqarish:
```python
sonlar = [-1, 2, -3, 4, -5]

for son in sonlar:
    if son < 0:
        continue
    print(son)
```
Yuqoridagi misolda, manfiy sonlar o'tkazib yuboriladi va faqat musbat sonlar ekranga chiqariladi.

- Faqat juft indexdagi elementlar bilan ishalash:
```python
mevalar = ['olma', 'banan', 'apelsin', 'anjir']

for i in range(len(mevalar)):
    if i % 2 != 0:
        continue
    print(mevalar[i])
```
Yuqoridagi misolda, faqat juft indekslardagi elementlar ekranga chiqariladi.

- `continue` operatorining kamchiliklari
    - **Kodni o'qish murakkablashishi mumkin:** Ba'zi hollarda, `continue` operatoridan haddan tashqari foydalanish kodingizni murakkablashtirishi mumkin, chunki har bir iteratsiyadagi kodning bajarilishini tushunish qiyinlashadi.
    - **Tuzilishi noqulay bo'lishi mumkin:** Agar **for loop**da juda ko'p shartlar bo'lsa va ular har xil `continue` operatorlariga bog'liq bo'lsa, bu kodni murakkab va noqulay tuzishga olib kelishi mumkin.

### pass OPERATORI
> [!NOTE]
> `pass` operatori Pythonda `hech narsa qilmaslik` uchun ishlatiladi. U bo'sh joyni saqlash uchun mo'ljallangan bo'lib, u qachonlardir qo'shilishi mumkin bo'lgan kod uchun o'rinbosar bo'lib xizmat qiladi. `pass` operatori kodning sintaksisi to'g'ri bo'lishi uchun ishlatiladi, lekin u hech qanday amaliyot bajarmaydi.

- `pass` operatoridan foydalanish
    - Agar siz kod yozayotganda hali bajarilishi kerak bo'lgan blokni to'liq qilmagan bo'lsangiz yoki shunchaki vaqtincha bo'sh qoldirmoqchi bo'lsangiz, `pass` operatoridan foydalanishingiz mumkin. Bu kodning ishlashiga to'sqinlik qilmaydi va boshqa qismdagi kodlarni sinab ko'rishga imkon beradi.
```python
for son in range(5):
    if son == 3:
        pass
    else:
        print(son)
```
Tushuntirish:
- Ushbu misolda, son `3` ga teng bo'lganda hech narsa qilinmaydi, lekin **for loop**ni davom ettiriladi. `3` raqamiga yetilganda `pass` operatori ishlatiladi va bu hech qanday natija bermaydi. Shuning uchun faqat `3` dan boshqa sonlar chop etiladi.

- `pass` operatorining foydalari:
    - **Kod Tuzilishini Saqlash:** `pass` operatori kod tuzilishini saqlab qoladi va keyinchalik ushbu qismga kod qo'shilishini kutib turadi.
    - **Vaqtinchalik Yechim:** `pass` dasturda vaqtincha yechim sifatida ishlatiladi, ya'ni siz hali bajarilishi kerak bo'lgan qismni aniqlab olmaganingizda.
    - **Sintaksis Xatolarni Oldini Olish:** Agar siz `if`, `for`, `while`, yoki funksiyalar kabi bloklarni yaratgan bo'lsangiz, lekin ularni hali to'ldirmagan bo'lsangiz, `pass` operatori yordamida sintaksis xatolarini oldini olishingiz mumkin.
Misollar:
- Bo'sh funksiyani yaratish:
```python
def empty_func():
    pass
```
Yuqoridagi misolda, `empty_func` nomli funksiyani yaratdik, lekin u hech narsa qilmaydi. Keyinchalik ushbu funktsiya ichiga kod yozishingiz mumkin.

- Bo'sh class yaratish:
```python
class EmptyClass:
    pass
```
Yuqoridagi misolda, `EmptyClass` nomli **class** yaratildi, lekin uning ichida hech qanday metod yoki atribut yo'q. `pass` operatori **class**ni to'ldirish uchun bo'sh joy saqlashga imkon beradi.
- Shartli bo'sh blok:
```python
for son in range(10):
    if son % 2 == 0:
        pass  # Juft sonlar uchun hech narsa qilmaymiz
    else:
        print(son)
```
Yuqoridagi misolda, juft sonlar uchun hech narsa qilinmaydi, faqat toq sonlar chop etiladi.

- `pass` operatorining kamchiliklari
    - **Boshqaruv tuzilmasi mumkin:** Agar siz `pass` operatoridan foydalanishni unutib qo'ysangiz, kodda muhim qismi bo'sh qolishi mumkin, bu esa keyinchalik dasturda muammolar keltirib chiqarishi mumkin.
    - **Kamdan-kam foydalaniladi:** `pass` operatori kodni tayyorlash va sinovdan o'tkazish jarayonida foydali, lekin final versiyasida odatda kamdan-kam ishlatiladi.

## AMALIYOT
- Elementlarni chiqarish:
    - `for` loop yordamida ro‘yxatdagi barcha elementlarni ekranga chiqaruvchi kod yozing.
    ```python
    mevalar = ["olma", "banan", "shaftoli"]
    ```
- Sonlar yig‘indisi:
    - `for` loop yordamida `1` dan `10` gacha bo‘lgan sonlarning yig‘indisini toping.
- Harflarni hisoblash:
    - Bir matn berilgan. for loop yordamida matndagi nechta unli harf borligini hisoblang. Unli harflar: `a, e, i, o, u`.
- Sonlarni ko‘paytirish:
    - Ro‘yxatdagi sonlarni `2` ga ko‘paytiring va yangi ro‘yxat hosil qiling.
    ```python
    sonlar = [2, 4, 6, 8]


    # [4, 8, 12, 16]
    ```
- Kamida 5 elementdan iborat ismlar degan ro'yxat tuzing, va ro'yxatdagi har bir ismga takrorlanuvchi xabar yozing.
- Yuqoridagi tsikl tugaganidan so'ng, ekranga "Kod n marta takrorlandi" degan xabarni chiqaring (n o'rniga kod necha marta takrorlanganini yozing).
- 10 dan 100 gacha bo'lgan juft sonlar ro'yxatini tuzing. Ro'yxatning xar bir elementining kvadratini yangi qatordan konsolga chiqaring.
- Ma'lum bir elementni qidirish:
    - Quyidagi misolda, ro'yxatdagi kerakli elementni topib, uni topgan zahoti **for loop**ni to'xtatamiz.
```python
mevalar = ['olma', 'banan', 'apelsin', 'anjir']
```
Bu misolda, **for loop**i `mevalar` ro'yxatidagi elementlarni ketma-ket tekshiradi. `apelsin` topilganidan so'ng, `break` operatori siklni to'xtatadi.
- Juft sonni qidirish
    - Quyidagi misolda, ro'yxatdagi birinchi juft sonni topganimizda **for loop**ni to'xtatamiz.
```python
sonlar = [1, 3, 5, 6, 7, 9]
```
Bu misolda, **for loop**i `sonlar` ro'yxatidagi elementlarni tekshiradi. `6` raqami birinchi juft son bo'lganligi uchun, `break` operatori siklni to'xtatadi.
- O'quvchilar ro'yxatidan ma'lum bir ismni qidirish
    - Quyidagi misolda, o'quvchilar ro'yxatidan ma'lum bir ismni topganimizda **for loop**ni to'xtatamiz.
```python
oquvchilar = ['Ali', 'Vali', 'Olim', 'Jasur']
```
Bu misolda, **for loop**i `oquvchilar` ro'yxatidagi ismlar ustida aylanadi. `Olim` ismi topilganida, `break` operatori **for loop**ini to'xtatadi.
- 10 dan katta bo'lgan birinchi sonni topish
    - Quyidagi misolda, ro'yxatdagi `10` dan katta bo'lgan birinchi sonni topganimizda **for loop**ni to'xtatamiz.
```python
sonlar = [2, 4, 10, 15, 8]
```
Bu misolda, **for loop**i `sonlar` ro'yxatidagi sonlarni ketma-ket tekshiradi. `15` raqami `10` dan katta bo'lgan birinchi son bo'lib, `break` operatori **for loop**ni to'xtatadi.
- Toq sonlarni chiqarish:
    - Quyidagi misolda, ro'yxatdagi faqat **toq** sonlarni ekranga chiqaramiz. **Juft** sonlarga kelganda, `continue` operatori ishlaydi va ularni o'tkazib yuboradi.
```python
sonlar = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
Bu misolda, **for loop**i sonlar ro'yxatidagi barcha sonlarni tekshiradi. Agar son juft bo'lsa, `continue` operatori ishlaydi va **for loop**ning qolgan qismi o'tkazilib, keyingi takrorlashga o'tiladi. Natijada faqat toq sonlar chop etiladi.
- Ma'lum bir harfni o'tkazib yuborish:
    - Quyidagi misolda, string ichidagi ma'lum bir harfni (masalan, `a` harfini) ekranga chiqarmasdan o'tkazib yuboramiz.
```python
matn = "salom dunyo"
```
Yuqoridagi misolda, **for loop**i matndagi barcha harflarni tekshiradi. Agar harf `a` ga teng bo'lsa, `continue` operatori ishlaydi va u harfni chiqarishdan o'tkazib yuboradi. Natijada `a` harfi chiqmaydi.

- Manfiy sonlarni o'tkazib yuborish
    - Quyidagi misolda, ro'yxatdagi manfiy sonlarni ekranga chiqarishni o'tkazib yuboramiz va faqat musbat sonlarni chop etamiz.
```python
sonlar = [-5, 3, -1, 7, -8, 10]
```
Yuqoridagi misolda, **for loop**i sonlar ro'yxatidagi barcha sonlarni tekshiradi. Agar son **manfiy** bo'lsa, `continue` operatori ishlaydi va u sonni ekranga chiqarmasdan o'tkazib yuboradi. Natijada faqat **musbat** sonlar chiqariladi.
