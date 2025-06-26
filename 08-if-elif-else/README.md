# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 8-DARS IF...ELIF...ELSE..

## TARMOQLANISH

📌 Shu vaqtgacha yozgan dasturlarimizga e'tibor bersangiz, dasturimiz yuqoridan pastga qarab qatorma-qator bajarilib keldi. Bu chiziqli dastur deyiladi. Ammo ba'zida shartga qarab kodning bir qismidan boshqa qismiga o'tish zarur bo'ladi. Bunday holat `"tarmoqlanish"` deb ataladi. 

![alt text](images/flowchart.png)

📌 Python dasturlash tilida shart operatorlari (`conditional statements`) dasturda turli vaziyatlarga qarab turli amallarni bajarishga imkon beradi.

## ✅ IF

📌 Python dasturlash tilida `if` operatori **shartni tekshirish** uchun ishlatiladi. Ya'ni, agar biror shart **True** bo‘lsa, unga tegishli kodlar bajariladi. Agar shart **False** bo‘lsa, kod bajarilmaydi.


```python
# Bankdagi hisobdagi pul miqdori
account_balance = 1500  

# Agar balans 1000 dan katta bo‘lsa, foydalanuvchi pul yechishi mumkin
if account_balance > 1000:
    print("You can withdraw money")  # Foydalanuvchiga ruxsat beriladi
```

```python
# Foydalanuvchining savatidagi umumiy mahsulot narxi
total_price = 250  

# Agar narx 200 dan katta bo‘lsa, bepul yetkazib berish taklif qilinadi
if total_price > 200:
    print("You qualify for free shipping")  # Bepul yetkazib berish haqida xabar
```

```python
# Foydalanuvchi kiritgan parol
password = "mysecurepass"  

# Agar parol uzunligi 8 belgidan ko‘p bo‘lsa, kuchli parol deb baholanadi
if len(password) > 8:
    print("Your password is strong")  # Kuchli parol haqida xabar
```

## ✅ ELSE

![alt text](images/if-else.png)

📌 Python dasturlash tilida `else` operatori `if` dan keyin yoziladi. Agar `if` dagi **False** bo;lsa, else ichidagi kodlar bajariladi.


```python
# Foydalanuvchi shakarmi tanladi (ha yoki yo'q)
wants_sugar = True  

# Agar foydalanuvchi shakar istasa
if wants_sugar:
    print("Adding sugar to your coffee")  # Qahvaga shakar qo‘shiladi
else:
    print("Preparing your coffee without sugar")  # Shakarsiz qahva tayyorlanadi
```

```python
# Telefon quvvati foizda
battery_percentage = 15  

# Agar quvvat 20 dan kam bo‘lsa, ogohlantirish chiqariladi
if battery_percentage < 20:
    print("Battery is low. Please charge your phone.")  # Quvvat kamligi haqida ogohlantirish
else:
    print("Battery level is sufficient.")  # Quvvat yetarli
```

```python
# Talabaning olgan bahosi
exam_score = 72  

# Agar baho 60 yoki undan yuqori bo‘lsa, imtihondan o‘tgan hisoblanadi
if exam_score >= 60:
    print("You passed the exam!")  # O‘tdi degan xabar
else:
    print("You failed the exam.")  # Yiqildi degan xabar
```

## ✅ LIST BILAN ISHLASH

📌 Onlayn do‘konda foydalanuvchi savatida kamida 1 mahsulot borligini va maxsus mahsulot bor-yo‘qligini tekshirish:

```python
# Xaridor savatidagi mahsulotlar ro'yxati
shopping_cart = ["bread", "sugar", "apple"]

# Agar savatda kamida bitta mahsulot bo‘lsa
if shopping_cart:
    print("The cart has items")  # Savatda mahsulot borligi haqida xabar
else:
    print("The cart is empty")  # Savat bo‘shligi haqida xabar



# Agar savatda 'sugar' bo‘lsa
if "sugar" in shopping_cart:
    print("Sugar is in the cart")  # Shakar mavjudligi haqida xabar
else:
    print("Sugar is not in the cart")  # Shakar yo‘qligi haqida xabar



# Agar savatda 5 ta yoki undan ko‘p mahsulot bo‘lsa, bepul yetkazib berish
if len(shopping_cart) >= 5:
    print("Free delivery available")  # Bepul yetkazib berish
else:
    print("Delivery charges apply")  # Pullik yetkazib berish
```

## ✅ TUPLE BILAN ISHLASH

📌 Foydalanuvchining geolokatsiyasi asosida joylashuvni aniqlash

```python
# Foydalanuvchining geografik joylashuvi (kenglik, uzunlik)
user_location = (41.2995, 69.2401)  # Toshkent koordinatalari

# Agar joylashuv ma'lum bo‘lsa (ya'ni tuple bo‘sh bo‘lmasa)
if user_location:
    print("Location detected")  # Joylashuv aniqlandi
else:
    print("Location not available")  # Joylashuv topilmadi



# Foydalanuvchi O'zbekiston hududida joylashganmi – kenglik bo‘yicha tekshiramiz
if 41.0 <= user_location[0] <= 42.0:
    print("User is located in Uzbekistan")  # Foydalanuvchi O‘zbekistonda
else:
    print("User is outside of Uzbekistan")  # Foydalanuvchi boshqa mamlakatda
```


## ✅ SET BILAN ISHLASH

📌  Saytga kirgan foydalanuvchilar `ID` raqamlari setda saqlanadi, va admin ularni tekshiradi.

```python
# Bugun saytga kirgan foydalanuvchilarning ID raqamlari (takrorlanmaydi)
active_user_ids = {101, 202, 303, 404}

# Agar kamida bitta foydalanuvchi saytga kirgan bo‘lsa
if active_user_ids:
    print("Bugun saytga foydalanuvchilar kirgan")  # Foydalanuvchilar bor

# Aks holda, hech kim kirmagan bo‘ladi
else:
    print("Hali hech kim saytga kirmagan")  # Set bo‘sh



# Agar 202-ID foydalanuvchi kirgan bo‘lsa
if 202 in active_user_ids:
    print("202-ID foydalanuvchi tizimga kirgan")  # Shu ID topildi
else:
    print("202-ID foydalanuvchi hali kirmagan")  # Shu ID yo‘q

# Bugun kirgan foydalanuvchilar soni 100 dan oshgan bo‘lsa
if len(active_user_ids) > 100:
    print("Yuqori aktivlik")  # Juda ko‘p foydalanuvchi
else:
    print("Oddiy kun")  # Odatdagi foydalanuvchi soni
```


### DICTIONARY BILAN ISHLASH:
- Dictionary bo'sh yoki to'la ekanligini tekshirish:
```python
my_dict = {"name": "Alice", "age": 25}

if my_dict:  # Dictionary bo'sh bo'lmasa
    print("Dictionary to'la")
else:
    print("Dictionary bo'sh")
```
- E'lement mavjud ekanligini tekshirish:
```python
my_dict = {'a': 1, 'b': 2, 'c': 3}

# Kalit mavjudligini tekshirish
if 'b' in my_dict:
    print("'b' kaliti lug'atda mavjud")
else:
    print("'b' kaliti lug'atda mavjud emas")

# Qiymat mavjudligini tekshirish
if 2 in my_dict.values():
    print("2 qiymati lug'atda mavjud")
else:
    print("2 qiymati lug'atda mavjud emas")
```
- Bir nechta shartni tekshirish:
```python
my_dict = {"name": "Alice", "age": 25, "city": "New York"}

if "age" in my_dict and my_dict["age"] > 20:  # "age" kaliti mavjud va qiymati 20 dan katta bo'lsa
    print("Yoshi 20 dan katta")
else:
    print("Shart bajarilmadi")
```
- Dictionary uzunligini tekshirish:
```python
my_dict = {"name": "Alice", "age": 25, "city": "New York"}

if len(my_dict) > 2:  # Dictionaryda 2 dan ortiq kalit mavjud bo'lsa
    print("Dictionaryda 2 dan ortiq kalit mavjud")
else:
    print("Dictionaryda 2 yoki undan kam kalit mavjud")
```


## `elif` OPERATORI

![alt text](images/elif.png)

`elif` (**else if**) operatori ko'p shartlarni ketma-ket tekshirish uchun ishlatiladi. Agar birinchi shart `if` bajarilmasa, `elif` sharti tekshiriladi. Agar hech qaysi shart bajarilmasa, `else` bloki bajariladi.

**Sintaksis:**
```python
if shart1:
    # Bu yerda shart1 bajarilganda bajariladigan kodlar
elif shart2:
    # Bu yerda shart2 bajarilganda bajariladigan kodlar
else:
    # Bu yerda hech qaysi shart bajarilmaganda bajariladigan kodlar
```
Quyidagi misolda `x` o'zgaruvchisiga berilgan qiymat `10` dan katta ekanligini tekshirdik. Agar shart `True` bo'lsa, terminalga `x` `10` dan katta degan so'z chiqadi. Aksxolda agar `x` `5` dan katta bo'lsa `5` dan katta lekin `10` dan kichik yoki teng degna so'z chiqadi, aks xolda x `5` dan kichik yoki teng degan so'z chiqadi:
```python
x = 7

if x > 10:
    print("x 10 dan katta")
elif x > 5:
    print("x 5 dan katta lekin 10 dan kichik yoki teng")
else:
    print("x 5 dan kichik yoki teng")
```

```python
my_list = [1, 2, 3, 4, 5]

if len(my_list) == 0:
    print("Ro'yxat bo'sh")
elif len(my_list) > 0 and len(my_list) <= 3:
    print("Ro'yxatda 3 yoki undan kam element bor")
else:
    print("Ro'yxatda 3 dan ortiq element bor")
```

```python
my_tuple = (1, 2, 3, 4, 5)

if len(my_tuple) == 0:
    print("Tuple bo'sh")
elif len(my_tuple) > 0 and len(my_tuple) <= 3:
    print("Tuple-da 3 yoki undan kam element bor")
else:
    print("Tuple-da 3 dan ortiq element bor")
```

```python
my_set = {1, 2, 3, 4, 5}

if len(my_set) == 0:
    print("Set bo'sh")
elif len(my_set) > 0 and len(my_set) <= 3:
    print("Setda 3 yoki undan kam element bor")
else:
    print("Setda 3 dan ortiq element bor")
```
- Ikkita to'plamni solishtirish:
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}

if set1 == set2:  # Ikkala set bir xil bo'lsa
    print("Setlar teng")
elif set1 & set2:  # Ikkala setda umumiy elementlar bo'lsa
    print("Setlarda umumiy elementlar mavjud")
else:
    print("Setlarda umumiy elementlar yo'q")
```

```python
my_dict = {"name": "Alice", "age": 25}

if "name" not in my_dict:
    print("Ism kiritilmagan")
elif my_dict["age"] < 18:
    print("Yosh kichikroq")
else:
    print("Ism va yosh mos")
```



## SHARTLARNI ZANJIR ORQALI ULASH (`and`, `or`, `not`)

Siz shartlarni birgalikda ishlatishingiz mumkin, bu orqali bir nechta shartlarni birga tekshirish mumkin.
- `and`: Ikkala shart ham to'g'ri bo'lsa, shart bajariladi.
- `or`: Har qanday bir shart to'g'ri bo'lsa, shart bajariladi.
- `not`: Shartning qiymatini teskariga o'zgartiradi.

```python
x = 7
y = 10

if x > 5 and y > 5:
    print("x va y har ikkalasi ham 5 dan katta")
    
if x > 5 or y < 5:
    print("yoki x 5 dan katta yoki y 5 dan kichik")

if not (x > 10):
    print("x 10 dan katta emas")
```

## SHART OPERATORLARINI ICHMA-ICH JOYLASH (Nested Conditions)
Shart operatorlarini bir-birining ichiga joylashtirish orqali murakkabroq mantiqiy holatlar yaratish mumkin.

```python
x = 8

if x > 5:
    if x < 10:
        print("x 5 dan katta va 10 dan kichik")
    else:
        print("x 10 dan katta yoki teng")
else:
    print("x 5 dan kichik yoki teng")
```

- Ko'p darajali ichma-ich shart operatorlari:
```python
x = 10
y = 20
z = 30

if x > 5:  # Birinchi darajadagi shart
    if y > 15:  # Ikkinchi darajadagi shart
        if z > 25:  # Uchinchi darajadagi shart
            print("x 5 dan katta, y 15 dan katta, va z 25 dan katta")
        else:
            print("x 5 dan katta, y 15 dan katta, lekin z 25 dan kichik yoki teng")
    else:
        print("x 5 dan katta, lekin y 15 dan kichik yoki teng")
else:
    print("x 5 dan kichik yoki teng")
```

- Ichma-ich shart operatorlari bilan foydalanuvchi `login`, `parol`ini tekshirish:
```python
username = "admin"
password = "1234"

if username == "admin":  # Birinchi darajadagi shart
    if password == "1234":  # Ikkinchi darajadagi shart
        print("Tizimga kirdingiz!")
    else:
        print("Noto'g'ri parol!")
else:
    print("Noto'g'ri foydalanuvchi nomi!")
```

## AMALIYOT

- Sonning musbat, manfiy yoki nol ekanligini aniqlash.
    - Foydalanuvchi kiritgan sonning musbat, manfiy yoki nol ekanligini aniqlaydigan dastur yozing.
- Talabaning bahosini aniqlash:
    - Talabaning o'rtacha bahosi asosida uning bahosini aniqlaydigan dastur yozing. Shartlar quyidagicha bo'lsin:
        - 90 va undan yuqori: "A"
        - 80 va undan yuqori: "B"
        - 70 va undan yuqori: "C"
        - 60 va undan yuqori: "D"
        - 60 dan past: "F"
- Yilning faslini aniqlash:
    - Foydalanuvchi kiritgan oy raqami asosida qaysi fasl ekanligini aniqlaydigan dastur yozing:
        - 12, 1, 2 - Qish
        - 3, 4, 5 - Bahor
        - 6, 7, 8 - Yoz
        - 9, 10, 11 - Kuz
- Foydalanuvchi login tizimi:
    - Foydalanuvchi login va parol kiritadi, va tizim ularning to'g'ri yoki noto'g'ri ekanligini tekshiradi. Agar login "admin" va parol "1234" bo'lsa, tizimga kirish muvaffaqiyatli bo'ladi, aks holda xato xabarini chiqaradi.
- Sonning juft yoki toq ekanligini aniqlash.
    - Foydalanuvchi kiritgan sonning juft yoki toq ekanligini aniqlaydigan dastur yozing.