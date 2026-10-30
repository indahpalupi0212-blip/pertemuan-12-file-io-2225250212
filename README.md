# Pertemuan 12 — File I/O dan Error Handling

## Identitas

- Nama: Indah Palupi Kusumaningrum

- NIM: 2225250212

- Kelas: 3F

## Tujuan

Mempelajari cara membaca, menulis, dan menambahkan data ke file teks menggunakan Python, serta menangani error dasar ketika file tidak ditemukan atau data tidak sesuai format.

## Struktur Proyek

```text
pertemuan-12-file-io-2225250212/
├── data/
│   ├── catatan.txt
│   ├── nilai.txt
│   └── hasil_rekap.txt
├── latihan/
│   ├── 01_tulis_file.py
│   ├── 02_baca_file.py
│   ├── 03_append_file.py
│   ├── 04_proses_baris.py
│   ├── 05_file_not_found.py
│   └── 06_value_error.py
├── tugas/
│   └── rekap_nilai_file.py
├── README.md
└── .gitignore
```

## Materi yang Dipelajari

1. Menulis file dengan mode `w`.
2. Membaca file dengan mode `r`.
3. Menambahkan data dengan mode `a`.
4. Memproses baris menggunakan `strip()` dan `split()`.
5. Menangani `FileNotFoundError`.
6. Menangani `ValueError`.
7. Menghitung statistik nilai dari file.
8. Menyimpan hasil rekap ke file teks.

## Format File Input

File `data/nilai.txt` menggunakan format NIM,nilai, satu record per baris.

Contoh:

```text
A001,85
A002,78
A003,92
A004,abc
A005,74
A006,88
```

## Cara Menjalankan

Jalankan perintah berikut dari terminal pada folder utama proyek.

```bash
python latihan/01_tulis_file.py
python latihan/02_baca_file.py
python latihan/03_append_file.py
python latihan/04_proses_baris.py
python latihan/05_file_not_found.py
python latihan/06_value_error.py
python tugas/rekap_nilai_file.py
```

## Error yang Ditangani

- `FileNotFoundError`: terjadi ketika file input tidak ditemukan.
- `ValueError`: terjadi ketika nilai tidak dapat dikonversi menjadi angka atau format baris tidak sesuai.

Program tugas melewati baris yang tidak valid agar record lainnya tetap dapat diproses.

## Pengujian

| Kasus | Hasil yang diharapkan |
|---|---|
| Semua data valid | Semua record diproses dan rekap benar |
| File tidak ditemukan | Pesan error ditampilkan tanpa menghentikan program secara tidak tertangani |
| Nilai berisi teks | Baris tidak valid dilewati |
| Baris kosong | Baris kosong dilewati |
| Nilai 60 | Dihitung sebagai lulus |

## Refleksi

Melalui praktik ini, saya mempelajari bahwa data dapat disimpan dalam file agar tetap tersedia setelah program selesai. Saya juga mempelajari penggunaan mode file, pemrosesan teks, konversi tipe data, serta penanganan error menggunakan `try-except`.