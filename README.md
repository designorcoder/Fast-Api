﻿Loyihaning batafsil tavsifi

Har bir faylning roli

Endpointlar tafsiloti

Ishga tushirish bo‘yicha to‘liq qo‘llanma

Swagger haqida

Hissa qo‘shish bo‘limi

Lisensiya bo‘limi (Mualliflik xuquqi bor)


![Screenshot 2025-04-11 101202](https://github.com/user-attachments/assets/ce1d9982-3e93-4ac0-900a-8948b8298389)



##✅ To‘liq README.md:

```bash
# 🏫 School & Student Management API

Bu loyiha FastAPI yordamida yozilgan backend API bo‘lib, maktablar va talabalar haqidagi ma’lumotlarni boshqarish uchun mo‘ljallangan. Loyiha asosan o‘quv       
maqsadida yaratilgan va unda oddiy CRUD funksiyalarining boshlang‘ich namunasi mavjud.

---
```
## 📌 Asosiy imkoniyatlar
```
- Maktablar ro‘yxatini olish
- Talabalar ro‘yxatini olish
- Maktab yoki talaba nomi bo‘yicha qidiruv
- Swagger UI orqali API ni test qilish imkoniyati
- JSON formatda javoblar

---
```
## 🛠 Texnologiyalar
```
- **Python 3.10+**
- **FastAPI** – engil, tez va zamonaviy API framework
- **Uvicorn** – ASGI server
- **Pydantic** – ma’lumotlar validatsiyasi uchun

---
```
## 📁 Loyihadagi fayllar
```
| Fayl nomi   | Tavsifi |
|-------------|---------|
| `main.py`   | Asosiy API logikasi va routerlar joylashgan |
| `data.py`   | Statik `school_db` va `student_db` ma’lumotlar |
| `model.py`  | Pydantic modellari – `School` va `Student` |

---
```
## 🚀 Loyihani ishga tushurish

1. **Repoda ishlash**:
```
git clone https://github.com/username/your-repo.git
cd your-repo

```
1 Virtual muhit yaratish:
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```
2 Kerakli kutubxonalarni o‘rnatish:
```bash
pip install fastapi uvicorn
```
3 Serverni ishga tushurish:
```bash
uvicorn main:app --reload
```
4 Swagger UI ochish (brauzer orqali):
```bash
http://127.0.0.1:8000/docs
```

###📡 API endpointlari
##🔍 GET so‘rovlari
Endpoint	Tavsifi
/api/school	Barcha maktablar ro‘yxatini qaytaradi
/api/student	Barcha talabalar ro‘yxatini qaytaradi
/api/school/{school_name}	Nom bo‘yicha maktabni topadi
/api/student/{student_name}	Nom bo‘yicha talabani topadi
✍️ POST so‘rovlari
Endpoint	Tavsifi
/api/school-create	Yangi maktab qo‘shish (hozircha school_dbga yozmaydi)
/api/student-create	Yangi talaba qo‘shish (hozircha student_dbga yozmaydi)

##🧾 Ma’lumotlar namunasi
Maktab (School) formati:
```bash
{
  "title": "IT School",
  "room": [1, 2, 3],
  "teacher": ["Ali", "Bekzod"]
}
```
Talaba (Student) formati:
```bash
{
  "name": "Javohir",
  "email": "javohir@gmail.com",
  "room_id": 2,
  "since": ["Python", "English"]
}
```
##🧪 Swagger UI
Loyiha ishga tushirilgach, avtomatik tarzda Swagger UI sahifasi yaratiladi. Bu sahifa orqali barcha endpointlarni test qilishingiz mumkin.

🧭 http://127.0.0.1:8000/docs

##⚠️ Eslatma
school-create va student-create endpointlari vaqtincha faqat ma’lumotni qabul qiladi, lekin uni data.pydagi school_db va student_dbga yozmaydi.

model.py faylidagi teacher: List[int] qismi aslida List[str] bo‘lishi kerak — aks holda validatsiya xatosi chiqishi mumkin.

📄 Lisensiya
Ushbu loyiha ochiq manba bo‘lib, istalgan maqsadda foydalanish mumkin. (Lekin mualliflik xuquqi bor)
