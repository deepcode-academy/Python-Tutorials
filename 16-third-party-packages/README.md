# 🐍 PYTHON DASTURLASH ASOSLARI  

# 🧩 16-DARS THIRD PARTY PACKAGES

📌 Python kutubxonalari 3 guruhga bo‘linadi:

1. **Standart kutubxonalar** – Python bilan birga keladi.
2. **Ikkinchi tomon kutubxonalari** – rasmiy Python jamoasi tashqarisida ishlab chiqilgan, ammo mashhur.
3. **Uchinchi tomon kutubxonalari (Third-party)** – mustaqil ishlab chiquvchilar yoki jamoalar tomonidan yaratilgan va keng turdagi loyihalar uchun ishlatiladi.

---

## 🔍 Third-Party Packages nima?

**Third-party packages** — bu Pythonning o‘zida yo‘q, lekin boshqa ishlab chiquvchilar tomonidan ishlab chiqilgan kutubxonalardir. Ular dasturchilarga turli murakkab ishlarni oson bajarishga yordam beradi (masalan: web dasturlash, ma’lumotlar tahlili, sun’iy intellekt, grafikalar chizish va h.k.).

---

## 🚀 Third-party paketlarni o‘rnatish

Python’ning `pip` (Python Package Installer) vositasi yordamida:

```bash
pip install package_nomi
```

### Masalan:

```bash
pip install requests
pip install numpy
pip install flask
```

---

## ✅ Eng ko‘p ishlatiladigan third-party kutubxonalar

| Kutubxona       | Maqsadi                                                                 |
|----------------|-------------------------------------------------------------------------|
| `requests`      | HTTP so‘rovlar yuborish va javob olish uchun                            |
| `beautifulsoup4`| Web sahifalarni tahlil qilish (scraping)                                |
| `pandas`        | Jadval (DataFrame) ko‘rinishidagi ma’lumotlar bilan ishlash             |
| `numpy`         | Katta hajmdagi massivlar va matematik hisoblar                          |
| `matplotlib`    | Grafikalar chizish                                                      |
| `seaborn`       | Statistik grafiklar chizish (matplotlib ustida ishlaydi)                |
| `scikit-learn`  | Mashinaviy o‘rganish (machine learning) algoritmlari                    |
| `flask`         | Yengil web ilovalar yaratish uchun freymvork                            |
| `django`        | To‘liq web freymvork (backend development)                              |
| `pytest`        | Avtomatik test yozish va bajarish uchun                                 |
| `opencv-python` | Rasm va video tahlili, kompyuter ko‘rish (Computer Vision)              |
| `sqlalchemy`    | Ma’lumotlar bazalari bilan ishlash (ORM)                                |
| `celery`        | Asinxron ishlov berish (masalan: xabar yuborish fon rejimida)           |
| `fastapi`       | Tezkor REST API yaratish uchun zamonaviy web-freymvork                  |
| `transformers`  | Natural Language Processing (NLP) uchun (Hugging Face tomonidan yaratilgan) |

---

## 🔧 Misollar bilan tushuntirish

### 1. `requests` bilan API’dan ma’lumot olish:

```python
import requests

url = "https://jsonplaceholder.typicode.com/posts"
response = requests.get(url)

if response.status_code == 200:
    data = response.json()
    print(data[0])  # Birinchi post
else:
    print("Xatolik yuz berdi.")
```

### 2. `numpy` bilan matematik amallar:

```python
import numpy as np

arr = np.array([1, 2, 3, 4])
print(arr * 2)  # Har bir elementni 2 ga ko‘paytiradi
```

### 3. `pandas` bilan jadval (DataFrame) ishlatish:

```python
import pandas as pd

data = {
    "Ism": ["Umid", "Ali"],
    "Yosh": [25, 30]
}
df = pd.DataFrame(data)
print(df)
```

### 4. `matplotlib` bilan grafik chizish:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3]
y = [2, 4, 6]
plt.plot(x, y)
plt.title("Oddiy Grafik")
plt.show()
```

---

## 📄 `requirements.txt` bilan kutubxonalarni boshqarish

Loyihada foydalanilgan barcha kutubxonalarni ro‘yxatga olish:

```bash
pip freeze > requirements.txt
```

Keyin boshqa kompyuterda bu fayl orqali hammasini o‘rnatish:

```bash
pip install -r requirements.txt
```

---

## 🌐 PyPI (Python Package Index)

Python kutubxonalarining asosiy ombori: [https://pypi.org](https://pypi.org)

Bu yerda har qanday third-party paketni topish, hujjatlari bilan tanishish va o‘rnatish mumkin.

---

## 📌 Third-party kutubxonalarni yangilash va o‘chirish

### Yangilash:

```bash
pip install --upgrade package_nomi
```

### O‘chirish:

```bash
pip uninstall package_nomi
```

---

## 🛠️ Virtual Environment (tavsiya qilinadi)

Har bir loyiha uchun alohida muhit yaratish muhim. Misol:

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

Bu orqali har bir loyiha o‘z kutubxonalariga ega bo‘ladi.

---

# PRACTICS

1. requests bilan soʻrov yuborish
    - https://jsonplaceholder.typicode.com/posts sahifasiga GET soʻrovi yuboring va javobdan 5 ta postning sarlavhasini (title) chiqaring.

2. beautifulsoup4 bilan HTML tahlil qilish
   - https://www.example.com sahifasidan barcha <a> teglarini ajrating va havola (href) manzillarini chop eting.

3. numpy yordamida massiv bilan ishlash
   - 1 dan 100 gacha boʻlgan sonlar bilan massiv yarating va barcha juft sonlarni chiqaring.

4. matplotlib bilan grafik chizish
   - 1 dan 10 gacha sonlarning kvadratlarini chizadigan grafik tuzing.

5. pandas yordamida maʼlumotlar tahlili
   - Talabalar haqida maʼlumotlardan iborat DataFrame yarating (Ism, Yoshi, Ball). Yoshi 20 dan katta boʻlganlarni ajrating.

6. flask bilan oddiy web ilova
   - Flask yordamida sahifada "Assalomu alaykum!" yozuvi chiqadigan web ilova yarating.

7. pytest bilan test yozish
   - Ikki sonni qoʻshuvchi funksiya yozing va pytest orqali uni test qiling.

8. pandas bilan CSV fayl o'qish
   - data.csv faylini pandas yordamida o'qing va maʼlumotlarni ekranga chiqaring.

9. requests bilan JSON API dan maʼlumot olish
   - https://api.coindesk.com/v1/bpi/currentprice.json API dan Bitcoin narxini olib, konsolga chiqaring.

10. matplotlib bilan histogram chizish
    - Tasodifiy 100 ta son yarating (numpy yordamida) va histogram ko'rinishida chizing.

11. numpy bilan matritsalar ustida amallar
    - 2 ta 3x3 o'lchamdagi matritsa yarating va ularni qo'shing.

12. flask bilan parametrli sahifa
    - URL orqali foydalanuvchi ismini qabul qilib, "Salom, Ism!" degan javob qaytaradigan Flask ilova yarating.

13. beautifulsoup4 bilan sahifa sarlavhasini olish
    - Web sahifadan <title> tegidagi matnni chiqaradigan dastur tuzing.

14. pandas bilan ustun qoʻshish
    - Mavjud jadvalga yangi ustun qoʻshing: talaba baholari asosida "Oʻtdi" yoki "Oʻtmadi" degan ustun hosil qiling.

15. venv yordamida virtual muhit yaratish
    - Terminal orqali yangi virtual muhit yarating va unga requests, numpy, pandas paketlarini o‘rnating.