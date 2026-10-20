# Hab Rujukan Mesyuarat Farmasi JKN Pahang

Sistem **Hab Rujukan Mesyuarat Farmasi** adalah aplikasi web satu muka surat (*Single Page Application - SPA*) yang direka khas untuk Jabatan Kesihatan Negeri (JKN) Pahang. Ia bertindak sebagai pusat sehenti (hub) digital tanpa kertas (*paperless*) bagi memudahkan urusan mesyuarat pengurusan dan teknikal farmasi.

Aplikasi ini dibina 100% menggunakan HTML, CSS, dan JavaScript tanpa memerlukan sebarang pelayan belakang (*serverless/no-backend*). Ini menjadikannya sangat ringan, pantas, dan mudah diselenggara oleh sesiapa sahaja.

## 🚀 Ciri-Ciri Utama
* **Akses Dokumen Berpusat:** Pautan terus ke folder Google Drive bagi mesyuarat terkini dan arkib rujukan mesyuarat lepas.
* **Jadual Interaktif:** Atur cara mesyuarat yang dibahagikan mengikut tab hari/kategori (Pengurusan, Teknikal, Pembangunan, Inovasi).
* **Maklumat Logistik:** Memaparkan maklumat lokasi dan kemudahan Wi-Fi dengan fungsi "Salin ke Papan Keratan" (*copy-to-clipboard*).
* **Direktori Urus Setia:** Pautan terus ke WhatsApp Urus Setia bagi setiap bahagian mesyuarat dengan templat mesej sapaan automatik.
* **Reka Bentuk Premium:** Antaramuka *Glassmorphism* dengan latar belakang beranimasi untuk imej korporat yang profesional.
* **Responsif:** Sesuai dipaparkan pada semua peranti (Telefon pintar, Tablet/iPad, dan Komputer).

---

## 💻 Cara Penggunaan (Urus Setia)

Untuk membuka dan melihat sistem ini, anda hanya perlu **dwiklik (double-click)** pada fail `index.html` (atau nama fail HTML anda) dan ia akan dibuka secara automatik di pelayar web anda (Google Chrome, Microsoft Edge, atau Safari).

---

## 🛠️ Panduan Kemas Kini / Penyelenggaraan Sistem (SOP)

Untuk menukar maklumat di dalam sistem ini, **JANGAN** gunakan perisian seperti Microsoft Word. Sila buka fail HTML tersebut menggunakan penyunting teks ringkas seperti:
* **Windows:** Notepad atau Visual Studio Code
* **Mac:** TextEdit (pastikan dalam mod *Plain Text*) atau Visual Studio Code

### 1. Mengemas Kini Pautan Google Drive & Maklumat Urus Setia
Tatal (*scroll*) ke bahagian paling bawah fail kod. Cari blok yang dilabelkan sebagai `KONFIGURASI DATA UTAMA`.

* **Pautan Terkini:** Gantikan pautan URL di bahagian `terkini: "..."`.
* **Pautan Arkib:** Tambah, ubah, atau buang baris `{ nama: "Bil. X/202X", link: "..." }` di bahagian `arkib: [ ]`. Jika tiada arkib, biarkan ia kosong sebagai `arkib: []`.
* **Urus Setia:** Tukar nama dan nombor telefon di dalam tatasusunan `URUSETIA = [ ... ]`. Pastikan nombor telefon diletakkan kod negara (cth: `6012...` tanpa simbol `+` atau sengkang `-`).

### 2. Mengubah Tajuk, Tarikh & Lokasi Mesyuarat
Cari (Ctrl+F atau Cmd+F) frasa ini di dalam kod:
`<!-- UBAH TAJUK, BILANGAN, TARIKH & TEMPAT MESYUARAT DI SINI -->`
Ubah teks yang berada di bawah tag tersebut mengikut keperluan mesyuarat akan datang.

### 3. Mengubah Jadual / Atur Cara (Tentatif)
Cari frasa ini di dalam kod:
`<!-- UBAH JADUAL/TENTATIF UNTUK SETIAP HARI DI BAWAH -->`
* Setiap sesi dikawal oleh kelas `<li class="key">` (untuk aktiviti utama/mesyuarat) atau `<li>` biasa (untuk rehat/makan).
* Gantikan teks di dalam `<div class="time">...</div>`, `<div class="what">...</div>`, dan senarai sub-aktiviti di dalam `<ul>...</ul>`.

---

## 🌐 Cara Mengehoskan Laman Web (Hosting)
Untuk membolehkan ahli mesyuarat mengakses sistem ini melalui internet (menggunakan URL seperti `mesyuarat-farmasi-pahang.netlify.app`), anda boleh menggunakan perkhidmatan *hosting* percuma:

1. **Gunakan Netlify (Paling Mudah - Tiada Akaun Diperlukan untuk Drop):**
   * Pergi ke [Netlify Drop](https://app.netlify.com/drop).
   * Seret dan lepas (*drag & drop*) folder yang mengandungi fail HTML anda ke dalam bulatan yang disediakan.
   * Laman web anda akan terus aktif (*live*) dan URL akan diberikan.

2. **Gunakan GitHub Pages:**
   * Cipta akaun di [GitHub](https://github.com/).
   * Cipta *Repository* baharu dan muat naik fail HTML ini (pastikan nama fail dinamakan semula kepada `index.html`).
   * Pergi ke tetapan (*Settings*) > *Pages* dan aktifkan *GitHub Pages*.

---
**Pembangun:** Muhammad Hafizul Aniq bin Khairul Hafidz, RPh. 25588  
**Hak Cipta:** &copy; 2026 Bahagian Perkhidmatan Farmasi, JKN Pahang.
