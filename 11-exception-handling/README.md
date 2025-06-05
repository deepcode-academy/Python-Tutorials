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

1. **try** va **except**
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



3. `finally`
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


4. Xatoni nom bilan chiqarish:
- Ba'zi hollarda, sodir bo'lgan xatoni dasturiy tilda yozib chiqish kerak bo'lishi mumkin. Bunda `as` kalit so'zi orqali xato ob'ektiga nom berish mumkin:

    ```py
    try:
        file = open('myfile.txt')
    except FileNotFoundError as e:
        print(f"Xato: {e}")
    ```
    **Tushuntirish:**
    - Agar `myfile.txt` nomli fayl mavjud bo'lmasa, `FileNotFoundError` xatosi paydo bo'ladi.
    - `as e` orqali bu xatoni `e` nomli o'zgaruvchida saqlab, uni ekranga chiqarish mumkin.

5. 

## AMALIYOT
1. Nolga bo'lishni tekshirish
    - Foydalanuvchi `2` ta son kiritadi. Siz bu sonlarni `bir-biriga` bo'lishingiz kerak, lekin `0` ga bo'lishdan ehtiyot bo'lish kerak.

**Natija:** Agar foydalanuvchi `0` kiritsa, `Xatolik: Nolga bo'lish mumkin emas` degan xabar chiqadi. Agar foydalanuvchi son o'rniga boshqa belgilar kiritsa, `Xatolik: Iltimos, faqat son kiriting` degan xabar chiqadi.

2. Faylni ochish va o'qish
    - Berilgan fayl nomini ochishga harakat qiling. Agar fayl mavjud bo'lmasa, tegishli xatolik xabari chiqsin.

**Natija:** Agar foydalanuvchi mavjud bo'lmagan fayl nomini kiritsa, `Xatolik: Fayl topilmadi` degan xabar chiqadi.

3. Raqamli qiymatni aylantirish
    - Foydalanuvchi kiritgan satrni butun son yoki haqiqiy songa aylantirishga harakat qiling.

**Natija:** Agar foydalanuvchi son emas, balki boshqa harflar yoki belgilar kiritsa, `Xatolik: Satrni son ko'rinishiga o'tkazib bo'lmadi` degan xabar chiqadi.

4. Hisoblash operatsiyasi
    - Foydalanuvchi ikkita son va bir operator (`+, -, *, /`) kiritsin. Hisoblashni amalga oshiring va natijani ko'rsating.

**Natija:** Agar foydalanuvchi noto'g'ri operator kiritsa yoki nolga bo'lishga harakat qilsa, tegishli xatolik xabarlari chiqadi.