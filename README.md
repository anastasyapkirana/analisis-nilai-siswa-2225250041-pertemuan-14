# Program Analisis Nilai Siswa

## Deskripsi
Program Analisis Nilai Siswa merupakan proyek Python berbasis terminal yang dirancang untuk membantu pengguna mengelola dan menganalisis nilai siswa.

Program ini menggunakan tiga komponen nilai, yaitu nilai tugas, UTS, dan UAS, untuk menghitung nilai akhir berdasarkan bobot yang telah ditentukan.

## Tujuan
- Mengelola data nilai siswa.
- Menghitung nilai akhir berdasarkan bobot.
- Menentukan status kelulusan siswa.
- Menampilkan statistik nilai siswa.

## Ketentuan Penilaian

| Komponen | Bobot |
|---|---:|
| Tugas | 40% |
| UTS | 30% |
| UAS | 30% |
| **Total** | **100%** |

Rumus nilai akhir:

`Nilai Akhir = (Tugas × 0,40) + (UTS × 0,30) + (UAS × 0,30)`

Ketentuan kelulusan:
- Nilai akhir ≥ 75: Lulus.
- Nilai akhir < 75: Tidak lulus.

## Data Siswa
Setiap siswa memiliki data:
- Nomor absen
- Nama
- Nilai tugas
- Nilai UTS
- Nilai UAS

Nomor absen harus unik dan setiap nilai harus berada pada rentang 0–100.

## Teknologi
- Bahasa pemrograman Python
- Visual Studio Code
- Git dan GitHub

## Struktur Proyek
Struktur folder dan file proyek dapat dilihat pada bagian proposal.

## Dokumentasi
Dokumen perancangan proyek tersedia pada file [`proposal.md`](proposal.md).

## Status Proyek
Tahap perancangan (Pertemuan 14). Implementasi program akan dilakukan pada tahap berikutnya.

---- Pertemuan 15 ----
## Fitur Program

1. Menambahkan data siswa.
2. Memvalidasi nomor absen agar tidak duplikat.
3. Memvalidasi nilai dalam rentang 0–100.
4. Menampilkan seluruh data siswa.
5. Mencari siswa berdasarkan nomor absen.
6. Menghitung nilai akhir berdasarkan bobot.
7. Menentukan status kelulusan.
8. Menampilkan statistik nilai kelas.
9. Menyimpan dan membaca data siswa.

## Ketentuan Penilaian

- Nilai tugas: 40%
- Nilai UTS: 30%
- Nilai UAS: 30%
- Batas kelulusan: 75

## Persyaratan

- Python 3.x
- Visual Studio Code (disarankan)

## Cara Menjalankan

Buka terminal pada folder utama proyek, kemudian jalankan:

```bash
py src/main.py
```

## Struktur Folder

```text
analisis-nilai-siswa-2225250041/
├── README.md
├── proposal.md
├── .gitignore
├── data/
│   └── data_siswa.txt
├── src/
│   ├── main.py
│   ├── siswa.py
│   ├── analisis.py
│   └── file_handler.py
└── tests/
    └── test_cases.md
```

## Pengujian

Pengujian program mencakup:
- Perhitungan nilai akhir.
- Batas kelulusan.
- Validasi nilai.
- Nomor absen duplikat.
- Penyimpanan data.
- Statistik kelas.

Hasil pengujian dicatat dalam file `tests/test_cases.md`.

## Status Proyek

Implementasi dan pengujian program dilakukan pada Pertemuan 15.


## Cara Menjalankan

Pastikan Python sudah terpasang.

Jalankan perintah berikut dari folder utama proyek:

```bash
py src/main.py