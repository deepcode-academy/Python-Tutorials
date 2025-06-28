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
Yuqorida misolda, **loop** sonlar ro'yxatidagi **manfiy** va **0** qiymatlarini o'tkazib yuboradi. Musbat sonlar chop etiladi.

### `while loop` KAMCHILIKLARI
- **Cheksiz loop:** Agar shart hech qachon `False` bo'lmasa, loop cheksiz davom etishi mumkin, bu esa dasturiy ta'minotning ishdan chiqishiga olib kelishi mumkin.
- **Shartni tekshirish:** Har safar shartni diqqat bilan tekshirish kerak, chunki noto'g'ri shart **loop**ning noto'g'ri ishlashiga olib kelishi mumkin.

## AMALIYOT
1. 1 dan 10 gacha bo'lgan sonlarni terminalga chiqarish:
    - `1` dan `10` gacha bo'lgan sonlarni `while loop` yordamida terminalga chiqaradigan dastur yozing.
2. Foydalanuvchi kiritgan sonning raqamlarini yig'indisini hisoblash:
    - Foydalanuvchidan bir son kiritishini so'rang va ushbu sonning raqamlarini yig'indisini hisoblaydigan dastur yozing. Masalan, foydalanuvchi `123` sonini kiritgan bo'lsa, natija `6` bo'lishi kerak (`1 + 2 + 3`).
3. Foydalanuvchi kiritgan ma'lumot bilan ishlash:
    - Foydalanuvchi `exit` so'zini kiritmaguncha, uning kiritgan ma'lumotlarini qabul qilib terminalga chiqaring.
4. Juft sonlarni hisoblash:
    - Foydalanuvchidan son kiriitishini so'rang va `1` dan ushbu songacha bo'lgan barcha juft sonlarni ekranga chiqaring.
5. Minimal sonni topish:
    - Foydalanuvchidan bir nechta sonlar kiritishni so'rang va foydalanuvchi `0` ni kiritganda kiritilgan sonlar ichidan eng kichik sonni ekranga chiqaring.