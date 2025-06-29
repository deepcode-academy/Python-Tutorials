# Python Tutorials – Amaliy va Nazariy Savollar

Har bir mavzu uchun 10 tadan amaliy va nazariy aralash topshiriqlar. Topshiriqlar tutoriallardagi vazifalarga o‘xshamagan.

---

## 1. Python asoslari (Basic Syntax)

1. Python dasturida `input()` funksiyasidan foydalanib, foydalanuvchidan ism va yoshini so‘rashingiz va ularni bir qatorda chiqaruvchi dastur yozing.
2. Python’da o‘zgaruvchi nomlash qoidalarini sanab bering va har biriga misol yozing.
3. Quyidagi kod natijasini va sababini tushuntiring:
   ```python
   a = "5"
   b = 2
   print(a * b)
   ```
4. Ikkita sonning o‘rtacha arifmetigini hisoblovchi funksiya yozing.
5. Python interpretator va kompilyator o‘rtasidagi farqni izohlang.
6. Foydalanuvchidan ism, familiya va tug‘ilgan yilini so‘rab, uni "Salom, [Ism] [Familiya]. Siz [Yosh] yoshdasiz." ko‘rinishida chiqaradigan dastur yozing.
7. Python’da satrlarni birlashtirishning kamida ikki xil usulini ko‘rsating va misol yozing.
8. Quyidagi kodni tahlil qiling va natijasini yozing:
   ```python
   print("5" + str(7))
   ```
9. Python’da `type()` funksiyasining vazifasi nimadan iborat? Misol bilan tushuntiring.
10. Uchta o‘zgaruvchi yarating va ularning qiymatlarini bir-biriga almashtiring (swap) (masalan, a→b, b→c, c→a).

---

## 2. Ma’lumot turlari va o‘zgaruvchilar (Data Types, Variables)

1. Quyidagi kodda qanday xatolik bor? Tuzating va sababini izohlang:
   ```python
   age = int("yigirma")
   ```
2. `bool`, `float`, va `str` turlarini bir-biridan farqlash uchun amaliy misollar yozing.
3. Foydalanuvchi kiritgan satrni teskari qilib chiqaruvchi dastur yozing.
4. Python’da `None` qiymati nimani anglatadi? Misol keltiring.
5. List va Tuple’ni qiyoslab, ularning farqlarini jadval shaklida yozing.
6. Foydalanuvchi kiritgan 5 ta sonni ro‘yxatga joylab, ularning o‘rtacha qiymatini hisoblab chiqadigan dastur yozing.
7. Python’da `set` va `dict` turlari o‘rtasidagi farqlarni jadvalda ko‘rsating.
8. Quyidagi kod natijasini toping va izohlang:
   ```python
   x = [1, 2, 3]
   y = x
   y.append(4)
   print(x)
   ```
9. Berilgan satrda nechta unli harf borligini aniqlovchi funksiya yozing.
10. O‘zgaruvchining tipini dinamik tarzda o‘zgartirish mumkinmi? Misol bilan tushuntiring.

---

## 3. Operatorlar (Operators)

1. Uchta butun son berilgan. Ularning eng kattasini aniqlovchi dastur yozing.
2. Quyidagi kod natijasini toping va izohlang:
   ```python
   print(5 // 2, 5 / 2)
   ```
3. `and`, `or`, `not` operatorlarini ishlatib, hayotdan olingan shartli misol tuzing.
4. Python’da ustunlik tartibi (precedence) qanday ishlashini misol bilan tushuntiring.
5. Foydalanuvchi yoshini tekshirib, agar 18 dan kichik bo‘lsa “Yosh yetarli emas”, aks holda “Xush kelibsiz” degan xabar chiqadigan dastur yozing.
6. Foydalanuvchi kiritgan ikki son ustida barcha arifmetik amallarni bajarib, natijalarini ko‘rsatuvchi dastur yozing.
7. Quyidagi kodda qanday natija chiqishini va sababini izohlang:
   ```python
   x, y = 5, 3
   x += y * 2
   print(x)
   ```
8. `is` va `==` operatorlarining farqini misollar bilan tushuntiring.
9. Foydalanuvchi kiritgan son toqmi yoki juftligini aniqlovchi dastur yozing.
10. Bitli (bitwise) operatorlardan biriga misol keltiring va natijasini izohlang.

---

## 4. Shart operatorlari va sikllar (if, for, while)

1. 1 dan 100 gacha juft sonlarni ekranga chiqaruvchi kod yozing.
2. `break` va `continue` farqini misollar bilan tushuntiring.
3. Quyidagi kod natijasini aniqlang va izoh bering:
   ```python
   for i in range(3):
       for j in range(2):
           print(i, j)
   ```
4. Foydalanuvchi kiritgan son musbat, manfiy yoki nol ekanligini aniqlovchi dastur yozing.
5. `while` siklidan foydalanib, foydalanuvchidan “Ha” deb yozmaguncha so‘rashni davom ettiradigan dastur yozing.
6. Foydalanuvchi kiritgan N sonining faktorialini hisoblovchi dastur yozing.
7. `else` qismi sikllarda qanday ishlatiladi? Misol bilan tushuntiring.
8. Quyidagi kod natijasini aniqlang va sababi bilan yozing:
   ```python
   for i in range(1, 6):
       if i == 3:
           break
       print(i)
   ```
9. 1 dan 50 gacha bo‘lgan, 3 ga karrali sonlarni ekranga chiqaruvchi dastur yozing.
10. Foydalanuvchi 0 raqamini kiritmaguncha sonlarni qabul qilib, ularning yig‘indisini chiqaruvchi dastur yozing.

---

## 5. Funksiyalar (Functions)

1. To‘g‘ri to‘rtburchak yuzasini hisoblaydigan funksiya yozing.
2. Funksiya argumentlari va qaytariladigan qiymatlar haqida qisqacha nazariy tushuncha bering.
3. Quyidagi kodda qanday xatolik bor va uni tuzating:
   ```python
   def add(a, b):
       return a + b
   print(add(2))
   ```
4. Lambda funksiyalarning asosiy farqlari va afzalliklarini yozing.
5. Berilgan sonlar ro‘yxatidagi juft sonlar sonini hisoblovchi funksiya yozing.
6. Uch sonning eng kichigini topuvchi funksiya yozing.
7. Default argumentli va argumentlarsiz funksiya yaratish o‘rtasidagi farqni tushuntiring va misol yozing.
8. Quyidagi funksiya qanday natija qaytaradi? Sababini yozing:
   ```python
   def func(a, b=5):
       return a * b
   print(func(3))
   ```
9. Funksiya ichidan global o‘zgaruvchini o‘zgartirish uchun qanday kalit so‘z ishlatiladi? Misol bilan yozing.
10. Berilgan matn palindrom ekanligini tekshiruvchi funksiya yozing (palindrom – o‘qilishida teskari ham bir xil bo‘lgan so‘z yoki jumla).

---