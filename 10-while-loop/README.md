# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 10-DARS WHILE LOOP

📌 `while` — bu tsikl operatori, ya’ni biror shart True bo‘lganida kodni qayta-qayta bajaradi. Agar shart False bo‘lsa, while tsikli to‘xtaydi va keyingi kodga o‘tadi.

```python
# son degan o'zgaruvchiga 1 qiymatini beramiz
son = 1

# while tsikli: son 5 dan kichik yoki teng bo‘lguncha davom etadi
while son <= 5:
    # hozirgi son qiymatini ekranga chiqaramiz
    print(son)
    
    # son qiymatini 1 ga oshiramiz, shunda tsikl keyingi son bilan davom etadi
    son += 1
```

🎯 Foydalanuvchidan ma'lumot olish (stop deb yozmaguncha)

```python
# Foydalanuvchi kiritgan matnni saqlash uchun bo‘sh o‘zgaruvchi yaratamiz
user_input = ""

# while tsikli: foydalanuvchi 'stop' deb yozmaguncha davom etadi
while user_input.lower() != "stop":
    # Foydalanuvchidan matn kiritishni so‘raymiz
    user_input = input("So'z kiriting (to‘xtatish uchun 'stop'): ")
    
    # Foydalanuvchi kiritgan so‘zni ekranga chiqaramiz
    print(f"Siz '{user_input}' kiritdingiz")
```

🎯 Foydalanuvchi parolni to‘g‘ri kiritmaguncha bajariladi.

```python
# Foydalanuvchi kiritgan matnni saqlash uchun bo‘sh o‘zgaruvchi yaratamiz
user_input = ""

# while tsikli: foydalanuvchi 'stop' deb yozmaguncha davom etadi
while user_input.lower() != "stop":
    # Foydalanuvchidan matn kiritishni so‘raymiz
    user_input = input("So'z kiriting (to‘xtatish uchun 'stop'): ")
    
    # Foydalanuvchi kiritgan so‘zni ekranga chiqaramiz
    print(f"Siz '{user_input}' kiritdingiz")
```

🎯 Ro‘yxatda kerakli qiymatni topish (break bilan)

```python
# Mahsulotlar ro'yxatini yaratamiz
products = ["apple", "banana", "lemon", "melon", "grapes"]

# Indeksni 0 dan boshlaymiz
i = 0

# Tsikl: indeks ro'yxat uzunligidan kichik bo‘lsa davom etadi
while i < len(products):
    # Agar hozirgi element 'lemon' bo‘lsa
    if products[i] == "lemon":
        # 'lemon' topilganini ekranga chiqaramiz
        print("✅ 'lemon' mahsuloti topildi!")
        # Tsiklni to‘xtatamiz
        break
    # Indeksni 1 ga oshiramiz, keyingi elementga o‘tamiz
    i += 1
```

🎯 Manfiy va nol sonlarni tashlab ketish (continue bilan)

```python
# Sonlar ro'yxatini yaratamiz
numbers = [-3, -1, 0, 2, 4, 6]

# Indeksni 0 dan boshlaymiz
i = 0

# Tsikl: indeks ro'yxat uzunligidan kichik bo‘lsa davom etadi
while i < len(numbers):
    # Agar hozirgi son 0 yoki manfiy bo‘lsa
    if numbers[i] <= 0:
        # Indeksni 1 ga oshiramiz, keyingi songa o‘tamiz
        i += 1
        # Ushbu davrani tashlab, tsikl boshiga qaytamiz
        continue

    # Agar son musbat bo‘lsa, uni ekranga chiqaramiz
    print(numbers[i])

    # Indeksni 1 ga oshirib, keyingi elementga o‘tamiz
    i += 1
```

🎯 Foydalanuvchi login tizimi

```python
correct_username = "admin"  # To‘g‘ri login
correct_password = "12345"  # To‘g‘ri parol

login_attempts = 0  # Urinishlar soni

while login_attempts < 3:  # Faqat 3 marta urinib ko‘rish huquqi
    username = input("Login kiriting: ")  # Login so‘rashi
    password = input("Parol kiriting: ")  # Parol so‘rashi

    if username == correct_username and password == correct_password:
        print("✅ Xush kelibsiz, tizimga kirildi!")
        break  # To‘g‘ri kirilgan bo‘lsa, tsikl tugaydi
    else:
        print("❌ Login yoki parol noto‘g‘ri.")
        login_attempts += 1  # Urinishlar sonini oshirish

if login_attempts == 3:  # 3 marta noto‘g‘ri kirilgan bo‘lsa
    print("🚫 Urinishlar tugadi, kirish bloklandi.")
```

🎯 Infinite Loop (Cheksiz tsikl) va undan himoyalanish

📌 Har doim shart o‘zgaruvchisini yangilashni unutmang

```python
# num o'zgaruvchiga 1 qiymati beriladi
num = 1

# Tsikl: num 5 dan kichik bo‘lsa davom etadi
while num < 5:
    # num qiymatini chiqaradi
    print(num)
    
    # ❌ Indeks oshirilmayapti, shuning uchun num har doim 1 bo‘lib qoladi
    # num += 1 YO‘Q! => bu yerda indeksni oshirish yo‘q, shuning uchun bu tsikl hech qachon tugamaydi
```

# ✅ AMALIYOT

## ✅ 1-topshiriq:
Foydalanuvchi kiritgan natural son uchun 1 dan shu songacha bo‘lgan sonlar yig‘indisini while loop orqali hisoblang.

---

## ✅ 2-topshiriq:
Quyidagi ro‘yxatda nechta elementda eng kamida 2 ta unli harf borligini aniqlang (while loopdan foydalaning):
```python
words = ["apple", "sky", "queue", "book", "cry"]
```

---

## ✅ 3-topshiriq:
Ro‘yxatda eng katta va eng kichik sonning farqini while loop yordamida toping:
```python
numbers = [7, 12, -3, 8, 0, 15]
```

---

## ✅ 4-topshiriq:
Foydalanuvchi 10 ta son kiritadi. While loop orqali faqat musbat va toq sonlarni yangi ro‘yxatga yozing.

---

## ✅ 5-topshiriq:
Quyidagi ro‘yxatdagi har bir so‘zning birinchi va oxirgi harfini birlashtirib yangi ro‘yxat hosil qiling (while loop bilan):
```python
words = ["python", "apple", "code", "loop"]
# natija: ["pn", "ae", "ce", "lp"]
```

---

## ✅ 6-topshiriq:
Ro‘yxatdan faqat 3 ga va 5 ga bo‘linadigan sonlarni ajratib, ularning o‘rtacha qiymatini while loopda hisoblang:
```python
nums = [5, 9, 15, 20, 22, 30, 35]
```

---

## ✅ 7-topshiriq:
Foydalanuvchi matn kiritadi. While loop yordamida matndagi raqamlarni topib, ularni son sifatida yig‘indisini hisoblang.
> Masalan: "salom12dunyo3" => natija: 15

---

## ✅ 8-topshiriq:
Berilgan ro‘yxatdan elementlarning indekslari juft bo‘lganlarini while loop bilan alohida ro‘yxatga chiqarib bering:
```python
fruits = ["olma", "banan", "gilos", "anor", "nok", "shaftoli"]
```

---

## ✅ 9-topshiriq:
Ro‘yxatda ketma-ket 2 marta uchraydigan elementlarni while loop yordamida aniqlang:
```python
items = [1, 2, 2, 3, 4, 4, 4, 5]
# natija: 2, 4
```

---

## ✅ 10-topshiriq:
Foydalanuvchi kiritgan matndan while loop yordamida faqat bosh harflarni ajratib, bitta string qilib chiqaring.
> Masalan: "Salom DunYo" => "SDY"

---

## ✅ 11-topshiriq:
Quyidagi ro‘yxatdan palindrom (teskari o‘qilganda ham bir xil) so‘zlarni while loop bilan ajratib chiqaring:
```python
words = ["anna", "python", "level", "loop", "radar"]
```

---

## ✅ 12-topshiriq:
While loop yordamida 100 dan kichik Fibonacci sonlarini ro‘yxatga yig‘ing.

---

## ✅ 13-topshiriq:
Ro‘yxatda nechta elementda harflar soni raqamlar sonidan ko‘p ekanini while loop yordamida hisoblang:
```python
elements = ["abc123", "hello", "42", "py2025", "test"]
```

---

## ✅ 14-topshiriq:
Ro‘yxatdagi sonlardan har birining raqamlari yig‘indisini while loop bilan hisoblab, yangi ro‘yxatga joylang:
```python
nums = [12, 305, 47, 88]
# natija: [3, 8, 11, 16]
```

---

## ✅ 15-topshiriq:
Ro‘yxatdagi elementlardan faqat birinchi harfi har doim katta, qolganlari kichik bo‘lgan yangi ro‘yxatni while loop orqali yarating:
```python
names = ["aNVAR", "mUROD", "dILSHOD"]
# natija: ["Anvar", "Murod", "Dilshod"]
```