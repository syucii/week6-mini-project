# week6-mini-project
# – Event Management API

## 📘 Deskripsi
REST API CRUD sederhana untuk mengelola data event (judul, lokasi, tanggal, harga tiket, dan jumlah kursi).  
Dibangun menggunakan **Express.js** dengan pola **MVC** dan database **MySQL**.

---

## ⚙️ Tech Stack
- Node.js + Express.js  
- MySQL (mysql2 + dotenv)  
- Morgan & custom logger middleware  

---

## 📁 Struktur Folder
```
src/
 ├─ app.js
 ├─ config/db.js
 ├─ controllers/eventController.js
 ├─ models/eventModel.js
 ├─ routes/eventRoutes.js
 ├─ middleware/
 │   ├─ logger.js
 │   ├─ validate.js
 │   └─ errorHandler.js
 └─ utils/httpResponse.js
.env
README.md
screenshot/
```

---

## 🔐 Environment (.env)
```
PORT=3000
DB_HOST=127.0.0.1
DB_USER=root
DB_PASSWORD=
DB_NAME=mini_project_uts
DB_PORT=3306
```

---

## 🚀 Cara Menjalankan
```bash
npm i
npm run dev
```
Server akan berjalan di:  
👉 http://localhost:3000

---

## 🧠 Endpoint CRUD

| Method | Endpoint | Deskripsi |
|:--:|:--|:--|
| GET | /events | Menampilkan semua event |
| GET | /events/:id | Menampilkan 1 event |
| POST | /events | Menambah event baru |
| PUT | /events/:id | Mengubah data event |
| DELETE | /events/:id | Menghapus event |

### Contoh Body (POST / PUT)
```json
{
  "title": "Workshop AR & Unity",
  "location": "Lab Riset XR",
  "event_date": "2025-11-15 09:00:00",
  "ticket_price": 15000,
  "seats": 60
}
```

---

## 🧰 Middleware
- **logger** → mencatat `method + url` ke console  
- **validate** → memastikan field tidak kosong, angka & tanggal valid  
- **errorHandler** → menangani error global (400, 404, 500)

---

## 🧪 Pengujian (Postman)
Semua endpoint diuji menggunakan Postman.  
Lihat folder `/screenshot` untuk hasil:
1. POST (create)
2. GET (list & by id)
3. PUT (update)
4. DELETE (delete)

---

## 🗒️ Kesimpulan
Project ini memperlihatkan cara membangun REST API berbasis **Express.js** dengan struktur **MVC**, menggunakan **middleware**, dan terhubung ke **MySQL** secara aman dengan `.env`.  
API dapat dikembangkan lebih lanjut dengan fitur **filter event**, **pagination**, atau **user authentication**.

---

## 📸 Dokumentasi
Semua screenshot uji API tersedia di folder `screenshot/`.
