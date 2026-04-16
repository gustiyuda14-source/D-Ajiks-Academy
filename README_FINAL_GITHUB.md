# 🎓 D'Ajiks Academy - TIU CAT System

Sistem CAT (Computer Assisted Test) interaktif untuk Tes Intelegensia Umum (TIU) SKD CPNS 2021, dibuat khusus untuk **Inspektorat Pemerintah Provinsi Sulawesi Tenggara**.

---

## ✨ Fitur Utama

✅ **25 Soal TIU** - Materi Pekerjaan  
✅ **Timer Real-time** - 90 menit countdown  
✅ **Scoring Otomatis** - Nilai 0-100  
✅ **Print Results** - Export PDF hasil ujian  
✅ **Detail Jawaban** - Lihat benar/salah per soal  
✅ **Database Ready** - Simpan hasil ke Supabase  
✅ **Responsive Design** - Desktop & Tablet  

---

## 🚀 Quick Start

### Online Demo
```
https://dajiks-academy-xxxxx.netlify.app
```

### Local Development
```bash
# 1. Clone repo
git clone https://github.com/[username]/dajiks-academy.git

# 2. Open index.html di browser
# Atau gunakan live server:
python -m http.server 8000
# Buka: http://localhost:8000
```

---

## 📊 Soal & Materi

- **Tipe 1:** Kecepatan Kerja Individual & Bersama-sama (10 soal)
- **Tipe 2:** Variasi Jumlah Pekerja & Target (6 soal)
- **Tipe 3:** Penambahan/Pengurangan Pekerja & Timeline (9 soal)

---

## 🛠️ Setup dengan Netlify + Supabase

### Prasyarat
- GitHub account
- Netlify account (gratis)
- Supabase account (gratis)

### Step by Step
1. Fork/Clone repo ini
2. Update `.env` dengan Supabase API keys
3. Push ke GitHub
4. Connect ke Netlify
5. Deploy! 🎉

Lihat `SETUP_SERVER_DAJIKS_ACADEMY.md` untuk panduan lengkap.

---

## 📁 Struktur File

```
dajiks-academy/
├── index.html           (Aplikasi utama)
├── .env.example         (Template environment variables)
├── .gitignore           (Git ignore patterns)
├── README.md            (File ini)
└── supabase-config.js   (Database config - optional)
```

---

## 🔐 Environment Variables

Buat `.env` file berdasarkan `.env.example`:

```
REACT_APP_SUPABASE_URL=https://[your-project].supabase.co
REACT_APP_SUPABASE_ANON_KEY=eyJhbGc...
```

**Jangan upload `.env` ke GitHub!** Sudah di `.gitignore`.

---

## 📱 Browser Support

| Browser | Status |
|---------|--------|
| Chrome | ✅ |
| Firefox | ✅ |
| Safari | ✅ |
| Edge | ✅ |

---

## 📝 Update Soal

Edit array `questions` di `index.html`:

```javascript
const questions = [
  {
    id: 1,
    category: "PEKERJAAN TIPE 1",
    question: "Pertanyaan soal...",
    options: ['A', 'B', 'C', 'D', 'E'],
    correct: 0, // Index jawaban benar
    optionLabels: ['A', 'B', 'C', 'D', 'E']
  },
  // ... soal lainnya
];
```

---

## 🗄️ Database Schema (Supabase)

### Tabel: peserta
```sql
id | nama | email | created_at
```

### Tabel: hasil_ujian
```sql
id | peserta_id | benar | salah | nilai | jawaban_detail | created_at
```

### Tabel: soal
```sql
id | nomor_soal | kategori | pertanyaan | opsi | jawaban_benar
```

---

## 🚀 Deploy ke Netlify

1. Hubungkan repo GitHub ke Netlify
2. Set environment variables di Netlify dashboard
3. Deploy otomatis saat push ke `main` branch

---

## 📊 Monitoring Hasil

1. Login Supabase
2. Table Editor → `hasil_ujian`
3. Lihat semua hasil peserta
4. Export ke CSV jika diperlukan

---

## 🤝 Contributing

Kontribusi welcome! Ikuti langkah:

1. Fork repo
2. Create feature branch: `git checkout -b feature/nama-fitur`
3. Commit: `git commit -m "Add fitur baru"`
4. Push: `git push origin feature/nama-fitur`
5. Create Pull Request

---

## 📞 Support

- **Issues:** GitHub Issues
- **Email:** [email Anda]
- **WhatsApp:** [nomor Anda]

---

## 📄 License

MIT License - Bebas digunakan

---

## 🙏 Credits

Dikembangkan untuk:
- **Inspektorat Pemerintah Provinsi Sulawesi Tenggara**
- **Semua peserta tes kedinasan**

---

Made with ❤️ by D'Ajiks Development Team

**Version:** 2.0.0  
**Status:** ✅ Production Ready  
**Last Updated:** April 17, 2026