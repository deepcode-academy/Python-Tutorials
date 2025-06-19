# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 3-DARS OPERATORS

- Python operatorlarini quyidagi guruhlarga bo'lish mumkin:
    - Arifmetik operatorlar
    - Taqqoslash operatorlari
    - Mantiqiy operatorlar
    - Bitwise (Bitli) operatorlar
    - Tayinlash (Assign) operatorlari
    - A'zolik (Membership) operatorlari
    - Identifikatsiya (Identity) operatorlari
    - Aralashtirilgan operatorlar (Mixed Operators)

## ✅ ARIFMETIK OPERATORLAR

📌 Python dasturlash tilida arifmetik operatorlar — sonlar ustida hisob-kitob qilish uchun ishlatiladigan maxsus belgilar yoki ifodalardir. Ular yordamida qo‘shish, ayirish, ko‘paytirish, bo‘lish kabi oddiy matematik amallarni bajarish mumkin.

```python
# a va b o'zgaruvchilariga qiymat beramiz
a = 10
b = 3

# Qo‘shish amali: a + b
yigindi = a + b
print(yigindi)  # Natija: 13

# Ayirish amali: a - b
ayirma = a - b
print(ayirma)  # Natija: 7

# Ko‘paytirish amali: a * b
kopaytma = a * b
print(kopaytma)  # Natija: 30

# Bo‘lish amali (natija float): a / b
bolish = a / b
print(bolish)  # Natija: 3.3333333333333335

# Butun qismga bo‘lish: a // b (natija butun son)
butun_qism = a // b
print(butun_qism)  # Natija: 3

# Qoldiqni topish: a % b
qoldiq = a % b
print(qoldiq)  # Natija: 1

# Darajaga ko‘tarish: a ** b (10 ning 3-darajasi)
daraja = a ** b
print(daraja)  # Natija: 1000
```

## ✅ TAQQOSLASH OPERATORLARI

📌 Python dasturlash tilida taqqoslash operatorlari (comparison operators) — ikki qiymatni taqqoslash uchun ishlatiladi. Ular natijada `True` yoki `False` (ya'ni mantiqiy qiymat) qaytaradi.

### 1. ❇️ TENGMI ==

Ikkita qiymat teng bo‘lsa, `True`, aks holda `False` qaytaradi.

```python
# 'a' o'zgaruvchisiga 5 soni berilyapti
a = 5

# 'b' o'zgaruvchisiga 3 soni berilyapti
b = 3

# 'result' o'zgaruvchisiga 'a' va 'b' tengmi degan shart natijasi berilyapti
# Bu yerda 5 == 3 bo'lmagani uchun natija False bo'ladi
result = (a == b)  # False, chunki 5 ≠ 3

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: False
```

### 2. ❇️ TENG EMAS !=

📌 Qiymatlar bir-biriga teng bo‘lmasa, `True` qaytaradi.

```python
# 'a' o'zgaruvchisiga 5 soni berilyapti
a = 5

# 'b' o'zgaruvchisiga 3 soni berilyapti
b = 3

# 'result' o'zgaruvchisiga 'a' va 'b' teng emasmi degan shart natijasi berilyapti
# Bu yerda 5 != 3 bo'lgani uchun natija True bo'ladi
result = (a != b)  # True, chunki 5 ≠ 3

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: True
```

### 3. ❇️ KATTA >

📌 Chap tomondagi qiymat o‘ng tomondagidan katta bo‘lsa, `True`.

```python
# 'a' o'zgaruvchisiga 5 soni berilyapti
a = 5

# 'b' o'zgaruvchisiga 3 soni berilyapti
b = 3

# 'result' o'zgaruvchisiga 'a' > 'b' sharti natijasi berilyapti
# Bu yerda 5 > 3 bo'lgani uchun natija True bo'ladi
result = (a > b)  # True, chunki 5 > 3

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: True
```

### 4. ❇️ KICHIK <

📌 Chap tomondagi qiymat o‘ng tomondagidan kichik bo‘lsa, `True`.

```python
# 'a' o'zgaruvchisiga 5 soni berilyapti
a = 5

# 'b' o'zgaruvchisiga 3 soni berilyapti
b = 3

# 'result' o'zgaruvchisiga 'a' < 'b' (ya'ni 5 < 3) sharti tekshirilmoqda
# Bu shart noto‘g‘ri, chunki 5 kichik emas 3 dan — natija: False
result = (a < b)  # False, chunki 5 < 3 emas

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: False
```

### 5. ❇️ KATTA YOKI TENG >=

📌 Agar chap tomondagi qiymat katta yoki teng bo‘lsa, `True`.

```python
# 'a' o'zgaruvchisiga 5 soni berilyapti
a = 5

# 'b' o'zgaruvchisiga 3 soni berilyapti
b = 3

# 'result' o'zgaruvchisiga 'a' >= 'b' (ya'ni 5 katta yoki teng 3) sharti tekshirilmoqda
# Bu shart to‘g‘ri, chunki 5 katta 3 dan — natija: True
result = (a >= b)  # True, chunki 5 >= 3

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: True
```

### 6. ❇️ KICHIK YOKI TENG (<=)

📌 Agar chap tomondagi qiymat kichik yoki teng bo‘lsa, `True`.

```python
# 'a' o'zgaruvchisiga 5 soni berilyapti
a = 5

# 'b' o'zgaruvchisiga 3 soni berilyapti
b = 3

# 'result' o'zgaruvchisiga 'a' <= 'b' (ya'ni 5 kichik yoki teng 3) sharti tekshirilmoqda
# Bu shart noto‘g‘ri, chunki 5 kichik emas va 5 teng ham emas 3 ga — natija: False
result = (a <= b)  # False, chunki 5 <= 3 emas

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: False
```

## ✅ MANTIQIY OPERATORLAR

📌 Python dasturlash tilida mantiqiy operatorlar (logical operators) shartlarni solishtirishda ishlatiladi va ular **True** yoki **False** qiymatlar bilan ishlaydi. Ular bir nechta shartlarni birlashtirish yoki tahlil qilish uchun qoʻllaniladi.

### 1. ❇️ AND

📌 Bu operator ikkala shart True boʻlsa, `True` qaytaradi.

```python
# 'a' o'zgaruvchisiga True (rost) qiymati berilmoqda
a = True

# 'b' o'zgaruvchisiga False (yolg'on) qiymati berilmoqda
b = False

# 'result' o'zgaruvchisiga 'a and b' mantiqiy ifodasi natijasi berilmoqda
# AND operatori ikkala qiymat ham True bo'lsa, True qaytaradi. Aks holda False.
# Bu yerda: True and False → natija: False
result = a and b  # result False ga teng bo'ladi

# 'result' ni ekranga chiqaramiz
print(result)  # Natija: False
```

### 2. ❇️ OR

📌 Hech bo'lmaganda bitta shart `True` bo'lsa, natija `True` bo'ladi, aks holda `False`.

```python
# 'a' o'zgaruvchisiga True (rost) qiymati berilyapti
a = True

# 'b' o'zgaruvchisiga False (yolg'on) qiymati berilyapti
b = False

# 'result' o'zgaruvchisiga 'a or b' mantiqiy ifodasi natijasi berilyapti
# OR operatori ikkala qiymatdan hech bo'lmaganda bittasi True bo'lsa, True qaytaradi
# Bu yerda: True or False → natija: True
result = a or b  # result True ga teng bo'ladi

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: True
```

### 3. ❇️ NOT

📌 Shartning mantiqiy qiymatini teskariga o'zgartiradi (`True` bo'lsa `False`ga, `False` bo'lsa `True`ga).

```python
# 'a' o'zgaruvchisiga True (rost) qiymati berilyapti
a = True

# 'result' o'zgaruvchisiga 'not a' ifodasi natijasi berilmoqda
# NOT operatori qiymatni teskarisiga o'zgartiradi: True → False, False → True
# Bu yerda: not True → False
result = not a  # result False ga teng bo'ladi

# 'result' o'zgaruvchisini ekranga chiqaramiz
print(result)  # Natija: False
```

📌 Quyidagi misolda mantiqiy operatorlar qanday ishlashini ko'rishimiz mumkin:

```python
# 'a' o'zgaruvchisiga 8 soni berilmoqda
a = 8

# 'b' o'zgaruvchisiga 12 soni berilmoqda
b = 12

# 'c' o'zgaruvchisiga 8 soni berilmoqda
c = 8

# 'd' o'zgaruvchisiga 15 soni berilmoqda
d = 15

# AND operatorlari bilan uchta shart tekshirilmoqda:
# (a == c) → 8 == 8 → True
# (b > a) → 12 > 8 → True
# (d % 5 == 0) → 15 % 5 == 0 → 0 == 0 → True
# AND operatori bilan bog‘langan barcha shartlar True bo‘lsa, umumiy natija ham True bo'ladi
result = (a == c) and (b > a) and (d % 5 == 0)
# True: chunki a va c teng, b a dan katta, d esa 5 ga bo'linadi

# Natijani ekranga chiqaramiz
print(result)  # True
```

```python
# 'x' o'zgaruvchisiga 3 soni berilmoqda
x = 3

# 'y' o'zgaruvchisiga 7 soni berilmoqda
y = 7

# 'z' o'zgaruvchisiga 10 soni berilmoqda
z = 10

# OR operatorlari bilan uchta shart tekshirilmoqda:
# (x > y) → 3 > 7 → False
# (z == 10) → 10 == 10 → True
# (y < 5) → 7 < 5 → False
# OR operatorida hech bo‘lmaganda bitta shart True bo‘lsa, umumiy natija True bo‘ladi
result = (x > y) or (z == 10) or (y < 5)
# True: chunki faqat (z == 10) sharti True

# Natijani ekranga chiqaramiz
print(result)  # True
```

```python
# 'a' o'zgaruvchisiga 4 soni berilmoqda
a = 4

# 'b' o'zgaruvchisiga 9 soni berilmoqda
b = 9

# Quyidagi ifodada birinchi navbatda AND operatori ishlaydi:
# (a < b) → 4 < 9 → True
# (b < 10) → 9 < 10 → True
# Demak: (a < b) and (b < 10) → True and True → True

# NOT operatori esa ifodani inkor qiladi: not True → False
result = not ((a < b) and (b < 10))
# (a < b) and (b < 10) → True, lekin not uni False qiladi

# Natijani ekranga chiqaramiz
print(result)  # False
```

```python
# 'x' o'zgaruvchisiga 6 soni berilmoqda
x = 6

# 'y' o'zgaruvchisiga 12 soni berilmoqda
y = 12

# 'z' o'zgaruvchisiga 6 soni berilmoqda
z = 6

# Butun ifoda ikki qismdan iborat:
# 1-qism: (x == z or y < 10)
#    (x == z) → 6 == 6 → True
#    (y < 10) → 12 < 10 → False
#    OR operatori bor, shuning uchun hech bo‘lmaganda bitta shart True bo‘lsa, natija: True

# 2-qism: not (y % 2 != 0)
#    (y % 2 != 0) → 12 % 2 → 0 → 0 != 0 → False
#    not False → True

# Yakuniy ifoda:
# True and True → natija: True
result = (x == z or y < 10) and not (y % 2 != 0)

# Natijani ekranga chiqaramiz
print(result)  # True
```

```python
# 'is_logged_in' — foydalanuvchi tizimga kirganmi? → True (ha, kirgan)
is_logged_in = True

# 'is_admin' — foydalanuvchi adminmi? → False (yo‘q, admin emas)
is_admin = False

# 'has_permission' — foydalanuvchining kerakli ruxsatlari bormi? → True (ha, bor)
has_permission = True

# Yakuniy mantiqiy ifoda:
# Foydalanuvchi tizimga kirgan bo‘lishi kerak (is_logged_in → True)
# Ruxsati bo‘lishi kerak (has_permission → True)
# Va admin bo‘lmasligi kerak (not is_admin → not False → True)

# Shartlar: True and True and True → natija: True
result = is_logged_in and has_permission and not is_admin

# Natijani ekranga chiqaramiz
print(result)  # True
```

## ✅ BITWISE(BITLI) OPERATORLAR

📌 Python tilida **bitwise** (`bitli`) operatorlar sonlarning bitlari ustida to'g'ridan-to'g'ri amallarni bajaradi. Bu operatorlar ikkita sonning **binary** (`ikkilik`) shakldagi bitlari bilan ishlaydi.


### ❇️  AND (`&`)

📌 Bu operator ikkala sonning mos bitlarini `AND` amali bilan solishtiradi. Ikkala bit ham `1` bo'lsa, natija `1`, aks holda `0`.
```python
# a o'zgaruvchiga 5 soni berilmoqda
# 5 ning ikkilik (binary) ko'rinishi: 0101
a = 5

# b o'zgaruvchiga 3 soni berilmoqda
# 3 ning ikkilik (binary) ko'rinishi: 0011
b = 3

# a va b o'zgaruvchilari ustida bitwise AND (&) amali bajarilmoqda
# a: 0101
# b: 0011
#    ----
# &  0001   --> faqat ikkala bit ham 1 bo'lgan joyda natija 1 bo'ladi
natija = a & b

# natijani ekranga chiqaramiz
# 0001 bu 10lik sanoq sistemasida 1 ga teng
print(natija)
```
### ❇️ OR (`|`)

📌 Bu operator ikkala sonning mos bitlarini `OR` amali bilan solishtiradi. Kamida bitta bit `1` bo'lsa, natija `1`, aks holda `0`.

```python
# a o'zgaruvchiga 5 soni berilmoqda
# 5 ning ikkilik (binary) ko'rinishi: 0101
a = 5

# b o'zgaruvchiga 3 soni berilmoqda
# 3 ning ikkilik (binary) ko'rinishi: 0011
b = 3

# a va b ustida bitwise OR (|) operatori bajarilmoqda
# a: 0101
# b: 0011
#    ----
# |  0111   --> har ikkala bitdan hech bo'lmaganda biri 1 bo'lsa, natijada 1 bo'ladi
natija = a | b

# natijani ekranga chiqaramiz
# 0111 bu 10lik sanoq sistemasida 7 ga teng
print(natija)
```
### ❇️ XOR (`^`)

📌 Bu operator ikkala sonning mos bitlarini `XOR` amali bilan solishtiradi. Agar bitta bit `1`, ikkinchisi `0` bo'lsa, natija `1`, aks holda `0`.

```python
# a o'zgaruvchiga 5 soni berilmoqda
# 5 ning ikkilik (binary) ko'rinishi: 0101
a = 5

# b o'zgaruvchiga 3 soni berilmoqda
# 3 ning ikkilik (binary) ko'rinishi: 0011
b = 3

# a va b ustida bitwise XOR (^) operatori bajarilmoqda
# a: 0101
# b: 0011
#    ----
# ^  0110   --> faqat bitta bit 1 bo'lsa (ya'ni faqat 1 yoki faqat 0 bo'lsa), natija 1 bo'ladi
#             agar ikkala bit bir xil bo‘lsa (0-0 yoki 1-1) natija 0 bo‘ladi
natija = a ^ b

# natijani ekranga chiqaramiz
# 0110 bu 10lik sanoq sistemasida 6 ga teng
print(natija)
```

### ❇️ NOT (`~`)

📌  Bu operator bitlarning qarama-qarshi qiymatini qaytaradi. `0` ni `1` ga, `1` ni `0` ga o'zgartiradi. Python tilida `~x = -x-1` deb qabul qilinadi.

```python
# a o'zgaruvchiga 5 soni berilmoqda
# 5 ning ikkilik (binary) ko'rinishi: 0101
a = 5

# bitwise NOT (~) operatori a ustida qo'llanilmoqda
# ~a bu bitlarning inkori (teskari qiymati) degani
# Python tilida bu quyidagicha ishlaydi: ~x = -x - 1
# ~5 = -5 - 1 = -6

# Yoki binary orqali tushuntirsak:
# 5  ->  0000 0101
# ~5 ->  1111 1010  (ya'ni 2 ning komplementi orqali -6 bo'ladi)
natija = ~a

# natijani ekranga chiqaramiz
# natija: -6
print(natija)
```
### ❇️ LEFT SHIFT (`<<`)

📌 Bu operator bitlarni chapga siljitadi va o'ng tomonga `0` qo'shadi. Har bir siljitish operatsiyasi bitlarning qiymatini `2` ga ko'paytiradi.

```python
# a o'zgaruvchiga 5 soni berilmoqda
# 5 ning ikkilik (binary) ko'rinishi: 0101
a = 5

# a << 1 bu bitlarni 1 pozitsiyaga chapga siljitish degani
# 0101 (5) chapga 1 ta siljisa: 1010 bo'ladi
# bu 10 lik sanoq sistemasida 10 ga teng
# Har bir chapga siljitish qiymatni 2 ga ko'paytiradi:
# 5 << 1 = 5 * 2 = 10
natija = a << 1

# natijani ekranga chiqaramiz
# natija: 10
print(natija)
```

### ❇️ RIGHT SHIFT (`>>`)

📌 Bu operator bitlarni o'ngga siljitadi va chap tomonga `0` yoki sonning ishorasi (`positive`/`negative sign`) qo'yiladi. Har bir siljitish operatsiyasi bitlarning qiymatini `2` ga kamaytiradi.

```python
# a o'zgaruvchiga 5 soni berilmoqda
# 5 ning ikkilik (binary) ko'rinishi: 0101
a = 5

# a >> 1 bu bitlarni 1 pozitsiyaga o'ngga siljitish degani
# 0101 (5) o'ngga 1 ta siljisa: 0010 bo'ladi
# bu 10 lik sanoq sistemasida 2 ga teng
# Har bir o'ngga siljitish qiymatni 2 ga kamaytiradi:
# 5 >> 1 = 5 // 2 = 2
natija = a >> 1

# natijani ekranga chiqaramiz
# natija: 2
print(natija)
```
7. EXTRA EXAMPLES 
- `AND`, `OR`, `XOR` **operatorlari bilan:**
```python
a = 12  # 1100
b = 6   # 0110

natija_and = a & b  # 0100 (4)
natija_or = a | b   # 1110 (14)
natija_xor = a ^ b  # 1010 (10)

print(natija_and)
print(natija_or)
print(natija_xor)
```
8. `NOT`, **chapga va o'ngga siljitish bilan:**
```python
x = 7  # 0111

natija_not = ~x     # -1000 (-8)
chapga = x << 2     # 11100 (28)
ongga = x >> 2     # 0001 (1)

print(natija_not)
print(chapga)
print(ongga)
```

## TAYINLASH(ASSIGN) OPERATORALRI
Pythonda **tayinlash**(`assign`) operatorlari yordamida o'zgaruvchilarga qiymatlar tayinlanadi. Bu operatorlar nafaqat qiymatlarni o'zgaruvchilarga tayinlash, balki matematik amallarni bajarib, natijani ham o'zgaruvchiga saqlash imkonini beradi. Quyida tayinlash operatorlarining to'liq ro'yxati va ulardan foydalanish misollari keltirilgan:

1. `=` - **Oddiy tayinlash operatori**
    - Bu operator oddiy qiymat tayinlash uchun ishlatiladi.
```python
x = 10
y = 5
```
Yuqoridagi misolda `x` o'zgaruvchisiga `10`, `y` o'zgaruvchisiga esa `5` qiymati tayinlanadi.

2. `+=` - **Qo'shish va tayinlash**
    - Bu operator yordamida o'zgaruvchi qiymatini berilgan qiymatga qo'shib, natijani o'zgaruvchiga qayta tayinlash mumkin.
```python
x = 10
x += 5  # x endi 15 ga teng bo'ladi
```

3. `-=` - **Ayirish va tayinlash**
- Bu operator yordamida o'zgaruvchi qiymatini berilgan qiymatdan ayirib, natijani o'zgaruvchiga qayta tayinlash mumkin.
```python
x = 10
x -= 3  # x endi 7 ga teng bo'ladi
```

4. `*=` - **Ko'paytirish va tayinlash**
- Bu operator yordamida o'zgaruvchi qiymatini berilgan qiymatga ko'paytirib, natijani o'zgaruvchiga qayta tayinlash mumkin.
```python
x = 4
x *= 2  # x endi 8 ga teng bo'ladi
```
5. `/=` - **Bo'lish va tayinlash**
- Bu operator yordamida o'zgaruvchi qiymatini berilgan qiymatga bo'lib, natijani o'zgaruvchiga qayta tayinlash mumkin.
```python
x = 20
x /= 4  # x endi 5.0 ga teng bo'ladi (natija float turida bo'ladi)
```
6. `%=` - **Qoldiqni tayinlash**
- Bu operator yordamida o'zgaruvchi qiymatini berilgan qiymatga bo'lgandan keyin qoldiqni o'zgaruvchiga qayta tayinlash mumkin.
```python
x = 10
x %= 3  # x endi 1 ga teng bo'ladi (qoldiq)
```
7. `**=` - **Daraja va tayinlash**
- Bu operator yordamida o'zgaruvchi qiymatini berilgan darajaga oshirib, natijani o'zgaruvchiga qayta tayinlash mumkin.
```python
x = 3
x **= 2  # x endi 9 ga teng bo'ladi (3^2 = 9)
```
8. `//=` - **Butun bo'lish va tayinlash**
- Bu operator yordamida o'zgaruvchi qiymatini berilgan qiymatga butun bo'lib, natijani o'zgaruvchiga qayta tayinlash mumkin.
```python
x = 10
x //= 3  # x endi 3 ga teng bo'ladi (butun qismini oladi)
```
## A'ZOLIK(MEMBERSHIP) OPERATORLARI
- Pythonda a'zolik (membership) operatorlari ma'lum bir elementning **ketma-ketlik**(`sequence`), masalan, **ro'yxat**(`list`), **qator**(`string`) yoki **to'plam**(`set`) ichida mavjudligini tekshirish uchun ishlatiladi. 
1. `in` **operatori**
- Bu operator yordamida elementning ma'lum bir ketma-ketlikda mavjudligini tekshirish mumkin.
```python
mevalar = ['olma', 'banan', 'nok']
if 'olma' in mevalar:
    print("Olma ro'yxatda mavjud.")
```
**Natija:** `Olma ro'yxatda mavjud.` <br>
Bu yerda `olma in mevalar ifodasi` True qiymatini qaytaradi, chunki `olma` mevalar ro'yxatida mavjud.

2. `not in` **operatori**
- Bu operator yordamida elementning ma'lum bir ketma-ketlikda mavjud emasligini tekshirish mumkin.
```python
mevalar = ['olma', 'banan', 'nok']
if 'uzum' not in mevalar:
    print("Uzum ro'yxatda mavjud emas.")
```
`Natija:` **Uzum ro'yxatda mavjud emas.**
Yuqorida `uzum not in mevalar` ifodasi True qiymatini qaytaradi, chunki 'uzum' mevalar ro'yxatida mavjud emas.

3. Stringlarda misollar
- A'zolik operatorlari **qatorlar**(`string`) bilan ham ishlaydi. Kichik qatorning kattaroq qator ichida mavjud yoki mavjud emasligini tekshirish mumkin.
```python
matn = "Salom dunyo"
if 'dunyo' in matn:
    print("'dunyo' matn ichida mavjud.")
```

## IDENTIFIKATSIYA(IDENTYFY) OPERATORLARI
- Pythonda identifikatsiya (identity) operatorlari ikki ob'ektning bir xil xotira joylashuvida saqlanayotganini aniqlash uchun ishlatiladi. Bu operatorlar ob'ektlarning identifikatorlarini solishtiradi, ya'ni ikki o'zgaruvchining aslida bitta ob'ektga ishora qilayotganini tekshiradi.

1. `is` **operatori**
- `is` operatori yordamida ikkita o'zgaruvchining bir xil ob'ektga ishora qilayotganligini tekshirish mumkin.
```python
a = [1, 2, 3]
b = a
if a is b:
    print("a va b bir xil ob'ekt.")
```
**Natija:** `a va b bir xil ob'ekt.` <br>
Yuqorida `a` va `b` bir xil ro'yxatga ishora qilmoqda, shuning uchun `a is b` ifodasi `True` qiymatini qaytaradi.

2. `is not` **operatori**
`is not` operatori yordamida ikkita o'zgaruvchining bir xil obyektga ishora qilmayotganini tekshirish mumkin.
```python
a = [1, 2, 3]
b = [1, 2, 3]
if a is not b:
    print("a va b bir xil ob'ekt emas.")
```
**Natija:** `a va b bir xil ob'ekt emas.`
Yuqorida `a` va `b` bir xil qiymatlarni o'z ichiga olgan bo'lsa ham, ular alohida ob'ektlar. Shuning uchun `a is not b` ifodasi True qiymatini qaytaradi.

- Identifikatsiya operatorlarining ishlash prinsipi
    - Identifikatsiya operatorlari ob'ektlarning xotira joylashuvini tekshiradi, ya'ni ob'ektlarning `ID` raqamlarini solishtiradi.
```python
a = [1, 2, 3]
b = [1, 2, 3]
print(id(a))  # a ob'ektining ID raqami
print(id(b))  # b ob'ektining ID raqami
```
Agar `a` va `b` ID raqamlari turli bo'lsa, demak ular alohida obyektlar.

## ARALASHTIRILGAN OPERATORLAR(MIXED OPERATORS)
- Python dasturlash tilida aralashtirilgan **operatorlar**(`mixed operators`) deganda bir nechta turli operatorlarni bitta ifodada ishlatish tushuniladi. Bu ifodalar matematik va mantiqiy amallarni birlashtirib, ancha murakkab hisob-kitoblar yoki shartlarni aniqlashga yordam beradi. Quyida aralashtirilgan operatorlardan foydalanish misollari keltirilgan:

1. `Arifmetik` va `mantiqiy` operatorlar aralashmasi
```python
x = 10
y = 5
z = 20

natija = (x + y) * z > 100 and z % y == 0
print(natija)
```
**Natija:** `True`
Yuqoridagi `(x + y) * z > 100` and `z % y == 0` ifodasi arifmetik (`+, *, %`) va mantiqiy (`and`) operatorlar aralashmasidan iborat. Ifoda birinchi bo'lib `(x + y) * z > 100` qismini hisoblaydi, so'ngra `z % y == 0` qismini tekshiradi va oxirida and operatori yordamida natijalarni birlashtiradi.

2. `Arifmetik` va `solishtirish` operatorlari aralashmasi
```python
a = 7
b = 3

natija = a * 2 > b + 5
print(natija)
```
**Natija:** `True`
Yuqorida `a * 2 > b + 5` ifodasi avval `a * 2 va b + 5` qismlarini hisoblaydi, keyin esa ularni `>` solishtirish operatori bilan solishtiradi.

3. **Shartli**(`ternary`) ifoda va arifmetik operatorlar
```python
a = 10
b = 5

max_qiymat = a if a > b else b
print(max_qiymat)
```
**Natija:** `10`
Yuqoridagi misolda `a if a > b else b` shartli ifoda yordamida aralashtirilgan operatorlar orqali `a` va `b` ning maksimal qiymatini aniqlaymiz.

## AMALIYOT
1. Ikkita o'zgaruvchi yarating va ularning qiymatlarini qo'shib natijani ekranga chiqaruvchi dastur yozing.
2. Foydalanuvchi tomonidan kiritilgan ikkita sonning ayirmasini hisoblab ekranga chiqaruvchi dastur yozing.
3. Ikkita o'zgaruvchi yarating va ularni bo'lgandan keyin butun qismini ekranga chiqaruvchi dastur yozing.
4. Foydalanuvchi tomonidan kiritilgan ikkita sonni bo'lgandan keyin qoldig'ini ekranga chiqaruvchi dastur yozing.