# QuranQu — AI-Powered Quran Recitation Tutor

## Deskripsi
QuranQu adalah aplikasi mobile berbasis AI yang membantu umat Islam memperbaiki pelafalan (makhraj) huruf hijaiyah dan bacaan Al-Quran secara mandiri. Berbeda dari aplikasi mengaji lain yang hanya memberikan skor benar/salah, QuranQu mendiagnosis kesalahan pelafalan secara spesifik per huruf dan memberikan panduan visual serta tekstual untuk memperbaikinya.

> "QuranQu bukan sekadar aplikasi ngaji — dia tahu di mana kamu salah, dan mengajarimu cara memperbaikinya."

## Fitur Utama
- **AI Pronunciation Diagnostic** — analisis pelafalan real-time menggunakan pipeline CNN + NLP Transformer
- **Visual + Penjelasan Koreksi** — ilustrasi posisi mulut/lidah yang benar disertai penjelasan bahasa awam
- **Modul Berjenjang** — dari Pra-Tahsin (huruf hijaiyah dasar) hingga Tahsin (bacaan ayat dengan tajwid)
- **Gamifikasi** — streak harian, poin, dan leaderboard untuk menjaga konsistensi belajar

## Arsitektur Teknis (Cutting Edge)
QuranQu mengintegrasikan dua algoritma Machine Learning dalam satu pipeline:

1. **Convolutional Neural Network (CNN)** — mengubah suara pengguna menjadi spektrogram, lalu mengekstraksi pola fonetik untuk dibandingkan dengan dataset makhraj standar yang dikurasi pakar. Output: skor deviasi + lokasi kesalahan per huruf.

2. **NLP Transformer** — menerima output teknis dari CNN dan mengubahnya menjadi penjelasan bahasa awam yang mudah dipahami pengguna.

Alur: **Audio Input → CNN (deteksi fonetik) → Transformer NLP (generate penjelasan) → Output ke UI**

Lihat contoh skeleton code alur ini di [`/ml-pipeline/pseudocode_ml_pipeline.py`](./ml-pipeline/pseudocode_ml_pipeline.py).

## 🛠️ Tech Stack
- **Frontend:** React Native (Expo)
- **Backend:** Node.js + Express
- **ML Service:** Python (FastAPI) — serving CNN + NLP Transformer pipeline
- **Database:** PostgreSQL

## Struktur Folder
QuranQuMVP/
├── README.md
├── mockup/ # Screenshot desain UI (Figma/Stitch)
└── ml-pipeline/
└── pseudocode_ml_pipeline.py # Simulasi alur CNN + NLP Transformer

## Prototipe UI
Desain UI/UX prototipe dapat dilihat pada folder [`/mockup`](./mockup) atau melalui link Figma/Stitch: *(tempel link kamu di sini)*

## Model Bisnis
Freemium — akses gratis untuk latihan dasar, upgrade ke Premium untuk fitur AI diagnosis penuh (subscription bulanan/tahunan).

---
**Disusun oleh:** Raihan Okta Ramadhan (24523177)
**Program Studi Informatika, Universitas Islam Indonesia**
