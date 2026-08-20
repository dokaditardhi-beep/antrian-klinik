# Aplikasi Antrean Klinik (UMUM & BPJS)

Aplikasi antrean klinik berbasis web dengan desain bersih, modern, dan didominasi warna biru muda menggunakan **Tailwind CSS**. Aplikasi ini berjalan sepenuhnya di sisi klien (client-side) tanpa memerlukan database server, sehingga sangat mudah untuk dijalankan dan di-host.

## 🌟 Fitur Utama

1. **Dashboard Utama**: Memberikan gambaran statistik antrean secara real-time (jumlah pasien menunggu, terlayani, dan sisa antrean).
2. **Kiosk Tiket Mandiri**: Antarmuka ramah pengguna bagi pasien untuk mengambil nomor antrean (UMUM - Kode `A` atau BPJS - Kode `B`) beserta tombol cetak instan.
3. **Layar Panggil Operator**: Kontrol panel bagi petugas loket pelayanan (Loket 1, 2, 3, dst.) untuk memanggil antrean berikutnya, memanggil ulang (recall), atau menandai pelayanan selesai.
4. **Layar Monitor Publik**: Layar display untuk ruang tunggu pasien yang menampilkan panggilan aktif berukuran besar, status setiap loket, riwayat panggilan terakhir, dan teks berjalan (running text).
5. **Panggilan Suara Otomatis (TTS & Audio Chime)**: Bunyi bel antrean elektronik ("ding-dong") disintesis secara real-time menggunakan Web Audio API, dilanjutkan dengan suara panggilan dalam Bahasa Indonesia menggunakan Web Speech API secara offline.
6. **Sinkronisasi Multi-Tab Real-time**: Menggunakan sistem event `localStorage` untuk sinkronisasi instan antar tab. Anda dapat membuka Kiosk Tiket di tablet, Layar Monitor di TV ruang tunggu, dan Layar Operator di PC loket—semuanya akan terhubung secara real-time tanpa server!
7. **Cetak Tiket POS Thermal (80mm)**: Dilengkapi dengan CSS khusus cetak `@media print` untuk menghasilkan cetakan tiket berukuran 80mm layaknya mesin cetak tiket antrean fisik profesional.

## 🚀 Cara Menjalankan Aplikasi

Aplikasi ini bersifat portabel dan tidak memiliki dependensi server. Anda cukup:

1. **Buka File HTML**: Double-click (klik dua kali) file `index.html` di browser Anda (disarankan Google Chrome atau Microsoft Edge).
2. **Menjalankan Server Lokal (Opsional)**: Jika ingin menggunakan server lokal, Anda bisa menggunakan Python atau Node.js:
   ```bash
   # Menggunakan Python 3
   python3 -m http.server 8000
   ```
   Lalu buka `http://localhost:8000` pada browser Anda.

## 🖨️ Panduan Cetak Tiket Antrean (Print)

Saat tombol **"Cetak Tiket"** ditekan di Kiosk, browser akan memunculkan dialog pencetakan secara otomatis. Agar hasilnya maksimal seperti printer thermal POS:

1. **Pilih Printer**: Arahkan ke printer thermal Anda (contoh: Epson TM, thermal printer 80mm).
2. **Pengaturan Halaman**:
   - **Ukuran Kertas (Paper Size)**: Pilih `Roll Paper 80mm` atau ukuran serupa.
   - **Margin**: Pilih `None` (Tanpa margin).
   - **Header & Footer**: Matikan/uncheck pilihan "Headers and footers" agar alamat URL browser tidak ikut tercetak di atas dan bawah tiket.
   - **Background Graphics**: Hidupkan/check pilihan ini agar elemen visual tercetak dengan sempurna.

## 📂 Struktur Data & Reset

* Semua data antrean disimpan di dalam memori browser (`localStorage`).
* Anda dapat masuk ke menu **Pengaturan** di navigasi atas untuk:
  - Mengubah nama, alamat, dan pesan tiket klinik.
  - Menambah atau menghapus loket pelayanan.
  - Membuat data simulasi (Mock data) untuk melakukan demonstrasi.
  - Melakukan **Reset Semua Antrean** untuk mengembalikan nomor antrean dari awal (`A-001` dan `B-001`).

---
Dibuat dengan ❤️ untuk kemudahan pelayanan kesehatan masyarakat.
# antrian-klinik
# antrian-klinik
