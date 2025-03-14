# 📊 Catatan Keuanganku

Catatan Keuanganku adalah proyek pencatatan finansial berbasis spreadsheet yang dirancang untuk membantu mengelola pemasukan dan pengeluaran dengan lebih rapi dan terorganisir. Proyek ini bertujuan meningkatkan kesadaran finansial dengan memberikan tampilan ringkasan keuangan yang jelas dan mudah dipahami.

## Fitur Utama
- Dashboard Ringkasan: Menampilkan saldo awal, saldo akhir, total pemasukan, dan total pengeluaran.
- Pencatatan Pemasukan & Pengeluaran: Formulir sederhana untuk mencatat transaksi keuangan.
- Kategorisasi Transaksi: Memungkinkan pengelompokkan pemasukan dan pengeluaran berdasarkan kategori.
- Otomatisasi Perhitungan: Menggunakan rumus spreadsheet untuk menghitung total saldo secara otomatis.
- Visualisasi Data: Grafik sederhana untuk memahami pola pengeluaran dan pemasukan.

## 🛠 Cara Penggunaan

### 1️⃣ Manual (Spreadsheet)
1. Download file spreadsheet dari repositori ini.
2. Buka file di Microsoft Excel atau Google Sheets.
3. Isi data pada halaman pemasukan dan pengeluaran.
4. Dashboard akan otomatis memperbarui ringkasan saldo dan grafik berdasarkan data yang diinput.

### 2️⃣ Menggunakan Script (Opsional)
> Jika ingin mengotomatisasi pengisian data, bisa menggunakan script Python untuk membaca/memasukkan data ke dalam spreadsheet.

1. Install library Python yang dibutuhkan:
   ```bash
   pip install pandas openpyxl
   ```
2. Gunakan skrip berikut untuk menambahkan transaksi secara otomatis:
   ```python
   import pandas as pd

   file_path = "catatan_keuanganku.xlsx"
   sheet_name = "Pengeluaran"

   new_data = {
       "Tanggal": ["2025-03-14"],
       "Kategori": ["Makan"],
       "Deskripsi": ["Sarapan di kafe"],
       "Jumlah": [50000]
   }

   df = pd.read_excel(file_path, sheet_name=sheet_name)
   df = df.append(pd.DataFrame(new_data), ignore_index=True)
   df.to_excel(file_path, sheet_name=sheet_name, index=False)
   print("Data berhasil ditambahkan!")
   ```

 Teknologi yang Digunakan
- Microsoft Excel / Google Sheets (untuk pencatatan manual)
- Python (pandas, openpyxl) (opsional, untuk otomasi data)

---

🚀 Proyek ini masih bisa dikembangkan lebih lanjut! Jika ada ide atau ingin berkontribusi, silakan buat issue atau pull request di repositori ini. 😊
