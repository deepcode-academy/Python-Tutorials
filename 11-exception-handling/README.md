# PYTHON DASTURLASH ASOSLARI

## 11-Dars: ISTISNO HOLARLARNI BOSHQARISH (EXCEPTION HANDLING)

> [!NOTE]
> **Eslatma:** Pythonda istisno holatlarni boshqarish dasturda yuzaga keladigan xatoliklarni to'g'ri boshqarish va dasturimizni barqaror ishlashini ta'minlash uchun muhim hisoblanadi. Bu `try`, `except`, `else`, va `finally` bloklari orqali amalga oshiriladi.

### EXCEPTION HANDLING HAQIDA UMUMIY TUSHUNCHA
Dastur bajarilishi davomida foydalanuvchidan noto‘g‘ri ma'lumot kiritilishi, fayl topilmasligi, nolga bo‘lish holati yoki boshqa xatoliklar yuz berishi mumkin. Exception Handling orqali bu xatoliklar dastur to‘xtab qolmasdan, foydalanuvchiga tushunarli tarzda xabar berib, dasturni davom ettirish imkonini beradi.

### EXCEPTION HANDLING SINTAKSISI

```python
try:
    # Xato chiqishi mumkin bo'lgan kod
except XatoNomi:
    # Xato yuz bersa ishlaydigan kod
else:
    # Xato chiqmasa ishlaydigan kod
finally:
    # Har doim ishlaydigan kod
```

1. **try, except**
- `try` blokida xatolik chiqishi mumkin bo‘lgan kod yoziladi. `except` blokida aniq xatolik turi bilan uni ushlab qolamiz.
    
```python
try:
    # Foydalanuvchidan son so‘raymiz va butun songa o‘girib olamiz
    son = int(input("Biror son kiriting: "))
    # 10 ni kiritilgan songa bo‘lamiz
    natija = 10 / son
    # Hisoblangan natijani chiqaramiz
    print(f"Natija: {natija}")
except ZeroDivisionError:
    # Agar son 0 bo‘lsa, bo‘lish amali xatoga olib keladi va bu xabar chiqadi
    print("Xatolik: Nolga bo'lish mumkin emas!")
except ValueError:
    # Agar son emas, noto‘g‘ri qiymat kiritsa, bu xato yuz beradi va bu xabar chiqadi
    print("Xatolik: Iltimos, butun son kiriting!")
```



2. **else**
- Agar `try` blokida xatolik yuz bermasa, `else` bloki ishga tushadi. Bu blokda xatoliklar bo'lmasa bajarilishi kerak bo'lgan kodlar yoziladi.

```python
try:
    # Foydalanuvchidan son so‘raymiz va butun songa o‘girib olamiz
    son = int(input("Biror son kiriting: "))
    # 10 ni kiritilgan songa bo‘lamiz
    natija = 10 / son
except ZeroDivisionError:
    # Agar son 0 bo‘lsa, bu xatolik chiqadi
    print("Xatolik: Nolga bo'lish mumkin emas!")
except ValueError:
    # Agar son emas, noto‘g‘ri qiymat kiritsa, bu xatolik chiqadi
    print("Xatolik: Iltimos, butun son kiriting!")
else:
    # Agar xatolik bo‘lmasa, natijani chiqaramiz
    print(f"Natija: {natija}")
```



3. **finally**
- `finally` bloki har qanday holatda ham, xatolik yuz bergan yoki bermagan bo'lsa ham, bajariladi. Bu blok, masalan, resurslarni tozalash yoki fayllarni yopish uchun ishlatilishi mumkin.

```python
try:
    # Foydalanuvchidan son so‘raymiz va butun songa o‘girib olamiz
    son = int(input("Biror son kiriting: "))
    # 10 ni kiritilgan songa bo‘lamiz
    natija = 10 / son
except Exception as e:
    # Har qanday xatolik yuz bersa, xato haqida ma’lumot chiqaramiz
    print(f"Xatolik: {e}")
finally:
    # Bu blok har doim, xato bo‘lsa ham, bo‘lmasa ham ishlaydi
    print("Dastur yakunlandi.")
```

4. **XATONI NOMI BILAN CHIQARISH**
- Ba'zi hollarda, sodir bo'lgan xatoni dasturiy tilda yozib chiqish kerak bo'lishi mumkin. Bunda `as` kalit so'zi orqali xato ob'ektiga nom berish mumkin:

```py
try:
    # "malumot.txt" faylini ochamiz
    file = open("malumot.txt")
    # Fayldagi barcha ma'lumotlarni o‘qiymiz
    data = file.read()
    # O‘qilgan ma'lumotlarni ekranga chiqaramiz
    print(data)
except FileNotFoundError as xato:
    # Agar fayl mavjud bo‘lmasa, xato xabari chiqariladi
    print(f"Xatolik: {xato}")
```


5. **BIR NECHTA XATOLARNI BITTA except DA USHLASH**

- Bir nechta xatolarni bitta `except` blokida ushlash mumkin.

```python
try:
# Foydalanuvchidan son so‘raymiz va uni butun songa o‘giramiz
x = int(input("Son kiriting: "))

# 10 ni kiritilgan songa bo‘lamiz
y = 10 / x

# Agar foydalanuvchi son o‘rniga matn kiritsa (ValueError),
# yoki 0 kiritsa (ZeroDivisionError), bu except bloki ishga tushadi
except (ValueError, ZeroDivisionError) as x:
    # Xatolik haqida foydalanuvchiga xabar beramiz
    print(f"Xatolik: {x}")
```

6. **MAXSUS XATOLIK YARATISH (raise)**

> [!NOTE]
> Pythonda `raise` — bu sun'iy (ya'ni o‘zimiz xohlagan paytda) xatolik chaqirish uchun ishlatiladi. Ayniqsa, foydalanuvchi noto‘g‘ri ma'lumot kiritsa, unga aniq xatolik berish uchun foydalidir.

```python
# Manfiy son kiritilsa xatolik (ValueError) chiqaradigan funksiya
def tekshir(son):
    # Agar son manfiy bo‘lsa, xatolik chiqaramiz
    if son < 0:
        raise ValueError("Manfiy son kiritish mumkin emas!")
    # Aks holda, sonni qaytaramiz
    return son

try:
    # Funksiyani manfiy son bilan chaqiramiz (bu xatoga olib keladi)
    tekshir(-5)

except ValueError as x:
    # Agar ValueError yuz bersa, xatolik haqida xabar chiqaramiz
    print(f"Xatolik: {x}")
```

## AMALIYOT

1. Nolga bo‘lish
    - Foydalanuvchidan ikkita son oling va birinchisini ikkinchisiga bo‘ling. Nolga bo‘lishdan himoyalaning.

2. Raqamga aylantirish
    - Foydalanuvchidan matn ko‘rinishida qiymat oling va uni `int` yoki `float` ga aylantiring. Agar foydalanuvchi harf kiritsa, xatolik chiqsin.

3. Notog‘ri operator
    - Foydalanuvchi ikkita son va bitta operator kiritsin (`+`, `-`, `*`, `/`). Operator noto‘g‘ri bo‘lsa, xatolik chiqsin.

4. Manfiy sonni taqiqlash
    - Foydalanuvchi son kiritadi. Agar son manfiy bo‘lsa, `raise` orqali `ValueError` chiqarilsin: `"Manfiy son kiritish mumkin emas!"`

5. Listdagi elementga murojaat
    - Berilgan ro‘yxatdan (`list`) indeks orqali element oling. Agar noto‘g‘ri indeks kiritilsa, `IndexError` chiqsin.

6. Lug‘atdan qiymat o‘qish
    - Foydalanuvchi lug‘atdan `key` bo‘yicha ma’lumot olishga harakat qiladi. Agar `key` mavjud bo‘lmasa, `KeyError` chiqsin.

7. Foydalanuvchidan parol olish
    - Foydalanuvchi parol kiritadi. Agar parol bo‘sh bo‘lsa, `raise ValueError` bilan xatolik chiqarilsin.

8. Har doim ishlaydigan kod
    - Foydalanuvchi son kiritadi va uni `int` ga aylantirib chiqarasiz. `finally` blokida `"Dastur tugadi"` degan matn chiqsin.

9. Bir nechta xatolarni ushlash
    - Foydalanuvchidan son kiriting va 10 ni ushbu songa bo‘ling. `ValueError` yoki `ZeroDivisionError` yuz bersa, bitta `except` bilan ushlang.

10. Funksiya orqali xatolik
    - Funksiya yarating: son kiritsa va u 100 dan katta bo‘lsa, `raise ValueError("100 dan katta son kiritish mumkin emas")` chiqsin.

11. Float sonni tekshirish
    - Foydalanuvchi haqiqiy son kiritsin. Agar son butun bo‘lsa, `raise ValueError("Faqat haqiqiy son kiriting")` chiqsin.