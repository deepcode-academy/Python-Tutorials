
# 14-DARS: OOP – OBJECT ORIENTED PROGRAMMING

Ushbu darsimizda OOP (Object-Oriented Programming) ya’ni obyektga yo‘naltirilgan dasturlash haqida gaplashamiz. OOP dasturlash tamoyillaridan foydalangan holda kodni ancha tartibli va qulay holatda yozish mumkin.

## OOP nima?

OOP – bu dasturda real hayotdagi obyektlar (mashina, inson, kompyuter) kabi obyektlarni yaratish va ular bilan ishlash usulidir. Har bir obyekt o‘ziga xos xususiyatlar (attributes) va xatti-harakatlarga (methods) ega bo‘ladi.

---

## OOP ning asosiy tushunchalari:

### 1. Class
Class bu - shablon. U orqali ko‘plab obyektlar (instance) yaratiladi.

```python
class Car:
    def __init__(self, model, rang):
        self.model = model
        self.rang = rang
```

### 2. Object
Class asosida yaratilgan nusxa (instance).

```python
car1 = Car("Malibu", "oq")
car2 = Car("Cobalt", "qora")
```

### 3. __init__ metodi
Bu metod classdan obyekt yaratilganda avtomatik chaqiriladi.

```python
def __init__(self, model, rang):
    self.model = model
    self.rang = rang
```

### 4. self
Bu parametr obyektning o‘ziga ishora qiladi.

---

## Misol: Obyekt yaratish va atributlarga murojaat qilish

```python
class Talaba:
    def __init__(self, ism, yosh):
        self.ism = ism
        self.yosh = yosh

talaba1 = Talaba("Umid", 20)
print(talaba1.ism)
print(talaba1.yosh)
```

---

## Method
Bu class ichida yozilgan funksiyadir.

```python
class Talaba:
    def __init__(self, ism, yosh):
        self.ism = ism
        self.yosh = yosh

    def salom_ber(self):
        print(f"Salom, mening ismim {self.ism}")

talaba1 = Talaba("Umid", 20)
talaba1.salom_ber()
```

## Encapsulation 

- Obyekt ichidagi ma’lumotlarni (atributlar) tashqi muhitdan yashirish, faqat kerakli metodlar orqali foydalanishga ruxsat berish.

- Afzalligi:
  - Ma’lumotlar himoyalanadi
  - Keraksiz aralashuvlarning oldi olinadi

```python
class BankHisobi:
    def __init__(self, balans):
        self.__balans = balans  # ikki pastki chiziq bilan yashirilgan

    def balans_korish(self):
        return self.__balans

    def pul_yechish(self, summa):
        if summa <= self.__balans:
            self.__balans -= summa
            return f"{summa} so‘m yechildi"
        else:
            return "Yetarli mablag‘ yo‘q"

hisob = BankHisobi(100000)
print(hisob.balans_korish())  # Natija: 100000
print(hisob.pul_yechish(30000))  # Natija: 30000 so‘m yechildi
```

- `__balans` tashqaridan to‘g‘ridan-to‘g‘ri o‘zgartirilmaydi — bu **encapsulation**.


## Inheritance

- Bitta classdan boshqa class xususiyatlarini meros olish (ya’ni, boshqa class unga o‘xshash bo‘ladi).

- Afzalligi:
  - Kodni takrorlamaslik
  - Kengaytma qilish oson

```python
class Hayvon:
    def ovoz(self):
        print("Bu hayvon tovush chiqaryapti")

class It(Hayvon):  # Hayvon classidan meros oldi
    def ovoz(self):
        print("Vov-vov")

class Mushuk(Hayvon):
    def ovoz(self):
        print("Miyav")

it = It()
it.ovoz()  # Natija: Vov-vov

mushuk = Mushuk()
mushuk.ovoz()  # Natija: Miyav
```

- `It` va `Mushuk` — `Hayvon` classining merosxo‘rlari.

## Polymorphism

- Bir xil nomdagi metodlar, lekin turli classlarda har xil ishlashi mumkin.

- Afzalligi:
  - Kodni soddalashtiradi
  - Har xil obyektlar bir xil metodga ega bo‘lishi mumkin

```python
class Talaba:
    def ishlash(self):
        print("Talaba dars qilmoqda")

class Uqituvchi:
    def ishlash(self):
        print("Uqituvchi dars bermoqda")

def ish_boshla(shaxs):
    shaxs.ishlash()

t = Talaba()
u = Uqituvchi()

ish_boshla(t)  # Natija: Talaba dars qilmoqda
ish_boshla(u)  # Natija: Uqituvchi dars bermoqda
```

- `ish_boshla()` funksiyasi kimga berilsa, shunga qarab o‘zini tutadi — bu `polymorphism`.


## OOP afzalliklari:
- Katta loyihalarda kodni tartibli saqlaydi
- Qayta ishlatiladigan kodlar yozish mumkin
- Kengaytirishga qulay


# PRACTICS

### 1-masala:
Quyidagi classni yozing: `Kitob`. U quyidagi atributlarga ega bo‘lsin: `nomi`, `muallif`, `sahifa_soni`.
Method: `malumot_ber()` – kitob haqida ma’lumot chiqaradi.

```python
class Kitob:
    def __init__(self, nomi, muallif, sahifa_soni):
        self.nomi = nomi
        self.muallif = muallif
        self.sahifa_soni = sahifa_soni

    def malumot_ber(self):
        print(f"{self.nomi} muallifi: {self.muallif}, sahifalar soni: {self.sahifa_soni}")

kitob1 = Kitob("Ufq", "Said Ahmad", 300)
kitob1.malumot_ber()
```

### 2-masala:
`Telefon` nomli class yarating. Atributlari: `brend`, `model`, `narx`. Method: `narx_oshir(foiz)` – narxni berilgan foizga oshirsin.

```python
class Telefon:
    def __init__(self, brend, model, narx):
        self.brend = brend
        self.model = model
        self.narx = narx

    def narx_oshir(self, foiz):
        self.narx += self.narx * foiz / 100

telefon1 = Telefon("Samsung", "Galaxy A52", 300)
telefon1.narx_oshir(10)
print(telefon1.narx)
```
