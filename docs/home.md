# 📘 Design Guideline - Biro Pengadaan Barang dan Jasa

Panduan ini digunakan untuk menjaga konsistensi desain web **Biro Pengadaan Barang dan Jasa**.  

---

## 🎨 Palet Warna
- **Hijau Utama (Primary)**: `#0A6D36`  
  Digunakan pada header, background hero, dan elemen penting.
- **Kuning Emas (Accent/Highlight)**: `#F1C40F`  
  Digunakan pada tombol utama (CTA), ikon penting, highlight informasi.
- **Putih (Background Utama)**: `#FFFFFF`  
  Digunakan sebagai latar belakang konten agar tetap bersih dan jelas.
- **Abu Muda (Secondary Background)**: `#F4F6F7`  
  Digunakan untuk blok konten tambahan.
- **Abu Medium (Text Secondary)**: `#BDC3C7`  
  Digunakan pada teks deskriptif.
- **Hitam Tua (Text Utama)**: `#2C3E50`  
  Digunakan untuk teks utama agar terbaca jelas.

---

## ✍️ Tipografi
- **Font Utama**: *Sans-serif modern* (misalnya: `Inter`, `Roboto`, atau `Open Sans`)
- **Ukuran & Hierarki**:
  - Heading 1 (H1): 36px Bold → Hero title / Judul halaman
  - Heading 2 (H2): 28px Semi-bold → Sub-judul
  - Heading 3 (H3): 22px Semi-bold → Section heading
  - Body Text: 16px Regular → Konten utama
  - Caption / Label: 14px Regular → Informasi tambahan

---

## 📐 Layout & Grid
- **Grid System**: 12 Kolom (Bootstrap style)  
- **Container**: Maksimal 1200px, margin otomatis untuk rata tengah.  
- **Padding & Spacing**:
  - Section spacing: 60px atas & bawah
  - Card spacing: 20px internal padding
  - Antar-komponen: minimal 24px

---

## 🔘 Komponen Desain

### 1. Header
- Logo di kiri
- Navigasi utama (Profil, Program Kerja, Regulasi, Pelayanan, Laporan, Galeri, Kontak)
- Tombol Login → gaya *primary button* kuning

### 2. Hero Section
- Background hijau dengan overlay transparan
- Judul besar (H1) putih
- Sub-judul → putih dengan ukuran lebih kecil
- Tombol CTA:
  - **Primary (Kuning)** → "Lihat Tender Aktif"
  - **Secondary (Putih dengan border hijau)** → "Unduh Dokumen Pedoman"

### 3. Info Cards (Highlight)
- 3 kolom utama (Tender Aktif, Pemenang Terbaru, Agenda Kegiatan)
- Ikon lingkaran dengan background kuning
- Teks bold untuk angka/nama penting

### 4. Tentang Biro
- Layout 2 kolom (teks di kiri, layanan di kanan)
- Teks ringkas + tautan "Baca Selengkapnya"

### 5. Layanan Utama
- Grid 2x2
- Ikon dalam lingkaran kuning
- Judul layanan bold
- Sub-judul opsional di bawah

### 6. Footer
- Informasi kontak
- Link cepat ke halaman utama
- Warna background hijau tua, teks putih

---

## 🖼️ Ikonografi
- Gaya **flat modern**
- Dominan warna **kuning (#F1C40F)** di background ikon
- Bentuk lingkaran dengan ikon di tengah
- Ikon konsisten (misalnya `Feather Icons` atau `Lucide`)

---

## 📱 Responsivitas
- **Mobile (≤768px)**:
  - Menu navigasi berubah menjadi hamburger menu
  - Hero text rata tengah
  - Info cards → stack vertikal
  - Grid layanan → 1 kolom
- **Tablet (768–1024px)**:
  - Navigasi horizontal
  - Info cards → 2 kolom
- **Desktop (≥1200px)**:
  - Layout penuh dengan 3 kolom & 2 kolom untuk layanan

---

## ✅ Contoh Penggunaan

### Tombol Primary
```html
<button class="btn-primary">Lihat Tender Aktif</button>

