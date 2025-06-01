# 🔹 Python Realtime Chat App with Firebase 🔹

Aplikasi chat real-time berbasis **Python + Firebase** yang mendukung login/signup, chat pribadi, dan grup publik. Dirancang dengan antarmuka sederhana menggunakan `Tkinter` dan dapat digunakan sebagai dasar pembuatan aplikasi desktop chat sendiri.

## 📦 Fitur Utama

- 🔐 **Sign Up / Login** dengan penyimpanan akun di Firebase
- 💬 **Chat Pribadi (1-on-1)** berdasarkan username
- 👥 **Chat Grup** (komunitas/grup bebas)
- ➕ **Buat Grup Sendiri** langsung dari aplikasi
- 🧭 **Navigasi Tab** untuk tiap ruang obrolan (pribadi/grup)
- 🔔 **Notifikasi Suara** jika ada pesan baru
- 🕓 **Tampilkan Status Online Terakhir**
- ✅ Validasi username dan grup di Firebase
- 🛡️ Password disimpan sebagai hash

---

## 📁 Struktur Firebase

Gunakan Firebase Realtime Database dengan struktur:

/users/{username}:
password: "hashed-password"
email: "optional-email"
lastOnline: timestamp

/chats/pribadi/{user1}_{user2}/:
[{ sender: user1, text: "pesan", timestamp: ... }]

/chats/komunitas/{groupName}/:
[{ sender: user2, text: "halo semua", timestamp: ... }]

yaml
Copy
Edit

---

## 🔧 Cara Install & Menjalankan

### 1. Pastikan Python Terinstall
- Download Python dari [python.org](https://www.python.org/downloads/)
- Saat instalasi, centang opsi **"Add Python to PATH"**

### 2. Clone Repository

```bash
git clone https://github.com/username/realtime-chat-app.git
cd realtime-chat-app
3. Install Library yang Dibutuhkan
bash
Copy
Edit
pip install firebase-admin python-dotenv
Jika ingin menggunakan notifikasi suara:

bash
Copy
Edit
pip install playsound
Atau gunakan winsound jika hanya di Windows.

4. Setup Firebase
Buat project di Firebase Console

Aktifkan Realtime Database

Pilih mode Test

Buat file firebase_config.json dari Firebase Admin SDK dan simpan di folder project

Buat .env dengan isi:

ini
Copy
Edit
FIREBASE_JSON=firebase_config.json
5. Jalankan Aplikasi
bash
Copy
Edit
python app.py
🖥️ Tentang Script Ini
Script utama berbasis Tkinter GUI, dan menghubungkan ke Firebase Realtime Database untuk menyimpan akun pengguna serta chat. Fitur seperti tab navigasi, suara notifikasi, dan validasi akun ditambahkan agar lebih mirip aplikasi modern.

✅ To-Do Selanjutnya
 Tambah emoji dan dukungan media

 Fitur edit & hapus pesan

 Dark mode

 Web versi menggunakan Flask atau React

🤝 Kontribusi
Pull Request, laporan bug, dan saran sangat diterima. Cukup fork repo ini dan buat perubahan yang bermanfaat!

📜 Lisensi
MIT License © 2025

yaml
Copy
Edit

---

Kalau Anda ingin saya bantu sekaligus **buat repositori GitHub-nya langsung**, tinggal
