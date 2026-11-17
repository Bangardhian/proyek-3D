# 🚗 Mobil 3D – Kumpulkan Koin

Game balap 3D interaktif berbasis browser yang dibuat dengan **Three.js**. Kendarai mobil, kumpulkan koin sebelum waktu habis, hindari bahaya, dan naikkan level. Model mobil 3D dibuat lewat [Vi3W](https://app.vi3w.in) (*3D in 3 Clicks!*).

🎮 **Demo langsung:** [vi3w-car3d.netlify.app](https://vi3w-car3d.netlify.app)

---

## ✨ Fitur

- **Model 3D dari Vi3W** – mobil `mobil_car.glb` dimuat langsung ke scene Three.js.
- **Mekanik game** – kumpulkan koin (target per level), skor, level, rekor tertinggi, dan batas waktu per ronde.
- **Rintangan & bahaya** – hindari hazard yang muncul di arena.
- **Power-up Magnet** – menarik koin di sekitar mobil selama beberapa detik.
- **Nitro (NOS)** dan **rem tangan** untuk manuver lebih dinamis.
- **Shop / Garage** – sistem toko dan garasi dalam game.
- **Kamera dinamis** – beberapa sudut pandang, termasuk *driver's POV*; drag mouse untuk memutar kamera dan scroll untuk zoom.
- **HUD lengkap** – speedometer (km/j), timer, skor, jumlah koin, level, rekor, dan minimap.
- **Siklus waktu** – ganti suasana pagi / siang / sore / malam.
- **Multi-bahasa (10 bahasa)** – ganti bahasa kapan saja.
- **Responsif** – kontrol sentuh untuk HP/tablet (mode **D-Pad** atau **setir rotasi**), plus kontrol keyboard di desktop. Ada pesan otomatis untuk memutar perangkat ke mode lanskap.

---

## 🎛️ Kontrol

### Keyboard (Desktop)

| Tombol | Fungsi |
|---|---|
| `W` `A` `S` `D` / `↑` `←` `↓` `→` | Kemudi (gas, rem/mundur, belok) |
| `Shift` | Turbo / Nitro |
| `Space` | Rem tangan |
| `P` / `Esc` | Jeda |
| `R` | Ulang game |
| `L` | Ganti bahasa |
| `F` | Balik arah depan |
| `T` | Ganti pagi / siang / sore / malam |
| **Drag mouse** | Putar kamera |
| **Scroll** | Zoom |

### Layar Sentuh (HP / Tablet)

- **Gas** & **Rem** – pedal di sisi kanan layar
- **NOS** – tombol nitro
- **Rem tangan** – tombol `(P)`
- **Lampu depan** – tombol headlight
- **Belok** – pilih di menu *Pengaturan*:
  - **Mode Tombol Panah (D-Pad)**, atau
  - **Mode Setir Mobil Rotasi (Steering Wheel)**

---

## 🛠️ Teknologi

- [Three.js](https://threejs.org/) `v0.165.0` (dimuat via CDN dengan *import map*)
- HTML5, CSS3, JavaScript (ES Modules)
- Format model: **glTF Binary (`.glb`)**
- Hosting: Netlify

---

## 📁 Struktur Proyek

```
proyek-3D/
├── index.html       # Struktur halaman, HUD, kontrol sentuh, menu pengaturan
├── style.css        # Tampilan & layout responsif
├── script.js        # Logika game, kamera, kontrol, dan loader model
└── mobil_car.glb    # Model mobil 3D (dibuat dengan Vi3W)
```

---

## 🚀 Menjalankan Secara Lokal

Karena memakai ES Modules dan memuat file `.glb`, proyek ini **harus dijalankan lewat server lokal** (tidak bisa dibuka langsung dengan `file://`).

1. Clone repositori:
   ```bash
   git clone https://github.com/Bangardhian/proyek-3D.git
   cd proyek-3D
   ```
2. Jalankan server lokal, pilih salah satu:
   ```bash
   # Python
   python -m http.server 8000

   # atau Node.js
   npx serve .
   ```
   Atau gunakan ekstensi **Live Server** di VS Code.
3. Buka `http://localhost:8000` di browser.

> 💡 Dibutuhkan koneksi internet karena Three.js dimuat dari CDN (jsDelivr).

---

## 🌐 Deploy

Proyek ini adalah situs statis, jadi bisa langsung di-deploy ke **Netlify**, GitHub Pages, atau hosting statis lainnya tanpa proses build.

---

## 👤 Pembuat

**Bagus Ardian Prabowo**
GitHub: [@Bangardhian](https://github.com/Bangardhian)

Dibuat sebagai prototipe cepat (*fast prototyping*) menggunakan Three.js dan alat bantu AI coding, dengan model 3D dari Vi3W.
