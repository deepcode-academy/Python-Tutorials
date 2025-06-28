# 🐍 PYTHON DASTURLASH ASOSLARI

# 🧩 12-DARS EXCEPTION HANDLING

> [!NOTE]
> **Eslatma:** Pythonda istisno holatlarni boshqarish dasturda yuzaga keladigan xatoliklarni to'g'ri boshqarish va dasturimizni barqaror ishlashini ta'minlash uchun muhim hisoblanadi. Bu `try`, `except`, `else`, va `finally` bloklari orqali amalga oshiriladi.

## ✅ EXCEPTION HANDLING HAQIDA UMUMIY TUSHUNCHA
📌 Dastur bajarilishi davomida foydalanuvchidan noto‘g‘ri ma'lumot kiritilishi, fayl topilmasligi, nolga bo‘lish holati yoki boshqa xatoliklar yuz berishi mumkin. Exception Handling orqali bu xatoliklar dastur to‘xtab qolmasdan, foydalanuvchiga tushunarli tarzda xabar berib, dasturni davom ettirish imkonini beradi.

## ✅ EXCEPTION HANDLING SINTAKSISI

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

## ✅ try, except
📌 `try` blokida xatolik chiqishi mumkin bo‘lgan kod yoziladi. `except` blokida aniq xatolik turi bilan uni ushlab qolamiz.
    
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



## ✅ else
📌 Agar `try` blokida xatolik yuz bermasa, `else` bloki ishga tushadi. Bu blokda xatoliklar bo'lmasa bajarilishi kerak bo'lgan kodlar yoziladi.

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



## ✅ finally
📌 `finally` bloki har qanday holatda ham, xatolik yuz bergan yoki bermagan bo'lsa ham, bajariladi. Bu blok, masalan, resurslarni tozalash yoki fayllarni yopish uchun ishlatilishi mumkin.

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

## ✅ XATONI NOMI BILAN CHIQARISH
📌 Ba'zi hollarda, sodir bo'lgan xatoni dasturiy tilda yozib chiqish kerak bo'lishi mumkin. Bunda `as` kalit so'zi orqali xato ob'ektiga nom berish mumkin:

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


## ✅ BIR NECHTA XATOLARNI BITTA except DA USHLASH

📌 Bir nechta xatolarni bitta `except` blokida ushlash mumkin.

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

## ✅ MAXSUS XATOLIK YARATISH (raise)

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

# ✅ AMALIYOT


## ✅ 1-topshiriq:
Foydalanuvchidan ikkita son oling va birinchisini ikkinchisiga bo‘ling. Nolga bo‘lishdan himoyalangan holda exception handling bilan dastur tuzing.

---

## ✅ 2-topshiriq:
Foydalanuvchidan matn ko‘rinishida qiymat oling va uni `int` yoki `float` ga aylantiring. Agar foydalanuvchi harf kiritsa, xatolik chiqsin.

---

## ✅ 3-topshiriq:
Foydalanuvchi ikkita son va bitta operator kiritsin (`+`, `-`, `*`, `/`). Operator noto‘g‘ri bo‘lsa, xatolik chiqsin.

---

## ✅ 4-topshiriq:
Foydalanuvchi son kiritadi. Agar son manfiy bo‘lsa, `raise` orqali `ValueError` chiqarilsin: `"Manfiy son kiritish mumkin emas!"`

---

## ✅ 5-topshiriq:
Berilgan ro‘yxatdan (`list`) indeks orqali element oling. Agar noto‘g‘ri indeks kiritilsa, `IndexError` chiqsin.

---

## ✅ 6-topshiriq:
Foydalanuvchi lug‘atdan `key` bo‘yicha ma’lumot olishga harakat qiladi. Agar `key` mavjud bo‘lmasa, `KeyError` chiqsin.

---

## ✅ 7-topshiriq:
Foydalanuvchi parol kiritadi. Agar parol bo‘sh bo‘lsa, `raise ValueError` bilan xatolik chiqarilsin.

---

## ✅ 8-topshiriq:
Foydalanuvchi son kiritadi va uni `int` ga aylantirib chiqarasiz. `finally` blokida `"Dastur tugadi"` degan matn chiqsin.

---

## ✅ 9-topshiriq:
Foydalanuvchidan son kiriting va 10 ni ushbu songa bo‘ling. `ValueError` yoki `ZeroDivisionError` yuz bersa, bitta `except` bilan ushlang.

---

## ✅ 10-topshiriq:
Funksiya yarating: son kiritsa va u 100 dan katta bo‘lsa, `raise ValueError("100 dan katta son kiritish mumkin emas")` chiqsin.

---

## ✅ 11-topshiriq:
Foydalanuvchi haqiqiy son kiritsin. Agar son butun bo‘lsa, `raise ValueError("Faqat haqiqiy son kiriting")` chiqsin.

---

## ✅ 12-topshiriq:
Fayl ochishga harakat qiling. Fayl mavjud bo‘lmasa, xatolik xabarini chiqaring (FileNotFoundError).

---

## ✅ 13-topshiriq:
Biror list yarating va foydalanuvchidan indeks so‘rang. Indeks noto‘g‘ri bo‘lsa, foydalanuvchiga tushunarli xabar chiqaring.

---

## ✅ 14-topshiriq:
Foydalanuvchidan yoshini so‘raydigan funksiya yozing. Agar foydalanuvchi manfiy yoki 120 dan katta yosh kiritsa, `raise ValueError` chiqsin.

---

## ✅ 15-topshiriq:
Foydalanuvchidan ikkita raqamli string so‘rang va ularni son sifatida qo‘shing. Agar harflar kiritsa, xatolikdan foydalanuvchiga ogohlantirish chiqaring.
