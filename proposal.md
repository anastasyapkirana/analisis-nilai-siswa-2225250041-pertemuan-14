# PROPOSAL PROYEK
# PROGRAM ANALISIS NILAI SISWA BERBASIS PYTHON

## 1. Judul Proyek

**Program Analisis Nilai Siswa Berbasis Python**

## 2. Latar Belakang

Pengolahan nilai siswa merupakan salah satu kegiatan yang dilakukan oleh guru dalam proses evaluasi pembelajaran. Pengolahan nilai meliputi pencatatan nilai tugas, Ujian Tengah Semester (UTS), dan Ujian Akhir Semester (UAS), perhitungan nilai akhir, serta penentuan status kelulusan siswa.

Jika pengolahan dilakukan secara manual, terdapat kemungkinan kesalahan perhitungan, kesulitan dalam mencari data, dan membutuhkan waktu lebih lama untuk membuat rekapitulasi nilai.

Oleh karena itu, dirancang sebuah program sederhana menggunakan bahasa Python yang dapat membantu guru mengelola data siswa, menghitung nilai akhir berdasarkan bobot tertentu, menentukan kelulusan, dan menghasilkan statistik nilai kelas.

## 3. Pengguna dan Tujuan

### Pengguna

Pengguna utama program adalah guru yang bertanggung jawab mengelola dan mengevaluasi nilai siswa dalam suatu kelas.

### Tujuan

1. Mempermudah pencatatan data siswa.
2. Menghindari penggunaan nomor absen yang sama.
3. Menghitung nilai akhir secara otomatis.
4. Menentukan status kelulusan berdasarkan batas nilai.
5. Menyediakan informasi statistik nilai kelas.
6. Menyimpan data agar dapat digunakan kembali.

## 4. Ruang Lingkup Proyek

### Fitur wajib

1. Menambahkan data siswa berupa nomor absen, nama, nilai tugas, UTS, dan UAS.
2. Memvalidasi agar nomor absen tidak digunakan oleh lebih dari satu siswa.
3. Memvalidasi nilai agar berada dalam rentang 0–100.
4. Menampilkan seluruh data siswa.
5. Mencari siswa berdasarkan nomor absen.
6. Menghitung nilai akhir berdasarkan bobot.
7. Menentukan status kelulusan dengan batas nilai 75.
8. Menghitung rata-rata, nilai tertinggi, dan nilai terendah kelas.
9. Menghitung jumlah siswa lulus dan tidak lulus.
10. Menyimpan dan membaca data melalui file.

### Aturan perhitungan nilai

| Komponen | Bobot |
|---|---:|
| Nilai tugas | 40% |
| Nilai UTS | 30% |
| Nilai UAS | 30% |
| **Total** | **100%** |

Rumus nilai akhir:

Nilai Akhir = (Tugas × 0,40) + (UTS × 0,30) + (UAS × 0,30)

Ketentuan kelulusan:
- Nilai akhir ≥ 75: Lulus.
- Nilai akhir < 75: Tidak lulus.

### Batasan proyek

- Program dibuat menggunakan Python.
- Program dijalankan melalui terminal atau console.
- Program digunakan untuk mengelola data dalam satu kelas.
- Setiap siswa memiliki satu nomor absen yang unik.
- Nilai tugas, UTS, dan UAS berada dalam rentang 0–100.
- Program tidak menggunakan database atau layanan eksternal.
- Antarmuka grafis dan web tidak termasuk dalam ruang lingkup proyek.

## 5. Kebutuhan Program

### Kebutuhan fungsional

| ID | Kebutuhan | Prioritas |
|---|---|---|
| F01 | Menambahkan data siswa | Wajib |
| F02 | Memvalidasi nomor absen unik | Wajib |
| F03 | Memvalidasi nilai 0–100 | Wajib |
| F04 | Menampilkan dan mencari data siswa | Wajib |
| F05 | Menghitung nilai akhir | Wajib |
| F06 | Menentukan status kelulusan | Wajib |
| F07 | Menghitung statistik nilai kelas | Wajib |
| F08 | Menyimpan dan membaca data | Wajib |

### Kebutuhan nonfungsional

1. Program mudah dijalankan melalui terminal VS Code.
2. Program memiliki nama fungsi dan variabel yang jelas.
3. Pesan kesalahan mudah dipahami.
4. Program menangani input tidak valid.
5. Data dapat dibaca kembali setelah program dijalankan ulang.

## 6. Spesifikasi Input, Proses, dan Output (IPO)

### Input

- Nomor absen siswa.
- Nama siswa.
- Nilai tugas.
- Nilai UTS.
- Nilai UAS.
- Pilihan menu pengguna.

### Proses

1. Menerima data siswa.
2. Memeriksa nomor absen agar tidak duplikat.
3. Memvalidasi nilai dalam rentang 0–100.
4. Menghitung nilai akhir menggunakan bobot yang ditentukan.
5. Menentukan status kelulusan berdasarkan nilai 75.
6. Menghitung statistik seluruh nilai siswa.
7. Menyimpan atau membaca data dari file.

### Output

- Daftar data siswa.
- Hasil pencarian siswa.
- Nilai akhir setiap siswa.
- Status kelulusan.
- Rata-rata nilai kelas.
- Nilai tertinggi dan terendah.
- Jumlah siswa lulus dan tidak lulus.
- File penyimpanan data siswa.

## 7. Algoritma dan Pseudocode

```text
MULAI

    Tampilkan menu utama

    SELAMA pengguna belum memilih keluar:

        Terima pilihan menu

        JIKA pilihan tambah siswa:
            Terima nomor absen
            Periksa apakah nomor absen sudah digunakan

            JIKA nomor absen sudah digunakan:
                Tampilkan pesan nomor absen duplikat
            JIKA BELUM:
                Terima nama dan nilai tugas, UTS, UAS
                Validasi seluruh nilai

                JIKA nilai valid:
                    Simpan data siswa
                    Hitung nilai akhir
                    Tentukan status kelulusan
                JIKA TIDAK:
                    Tampilkan pesan kesalahan

        JIKA pilihan tampilkan data:
            Tampilkan seluruh data siswa

        JIKA pilihan cari siswa:
            Cari berdasarkan nomor absen
            Tampilkan hasil pencarian

        JIKA pilihan analisis:
            Hitung rata-rata, minimum, dan maksimum
            Hitung jumlah siswa lulus dan tidak lulus
            Tampilkan hasil analisis

        JIKA pilihan simpan:
            Simpan data ke file

        JIKA pilihan baca:
            Baca data dari file

        JIKA pilihan keluar:
            Akhiri program

SELESAI
```

## 8. Struktur Program dan Modularisasi

Program dirancang menggunakan beberapa modul agar setiap fungsi memiliki tanggung jawab yang jelas.

| Modul | Fungsi | Tanggung jawab |
|---|---|---|
| `main.py` | `main()` | Mengatur menu dan alur program |
| `siswa.py` | `tambah_siswa()` | Menambah dan memvalidasi data siswa |
| `siswa.py` | `cari_siswa()` | Mencari siswa berdasarkan nomor absen |
| `analisis.py` | `hitung_nilai_akhir()` | Menghitung nilai akhir |
| `analisis.py` | `tentukan_status()` | Menentukan kelulusan |
| `analisis.py` | `hitung_statistik()` | Menghitung statistik kelas |
| `file_handler.py` | `baca_data()` | Membaca data dari file |
| `file_handler.py` | `simpan_data()` | Menyimpan data ke file |

### Struktur folder

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

## 9. Struktur Data

Program menggunakan dictionary untuk menyimpan data siswa dengan nomor absen sebagai key.

Contoh:

```python
data_siswa = {
    1: {
        "nama": "Andi",
        "tugas": 80,
        "uts": 70,
        "uas": 90
    },
    2: {
        "nama": "Budi",
        "tugas": 70,
        "uts": 65,
        "uas": 60
    }
}
```

Alasan penggunaan dictionary:
- Nomor absen dapat digunakan sebagai key.
- Pencarian siswa berdasarkan nomor absen lebih mudah.
- Setiap siswa dapat memiliki beberapa atribut.
- Nomor absen yang sama tidak dapat menjadi dua key terpisah.

List dapat digunakan untuk mengolah kumpulan nilai ketika menghitung statistik kelas.

## 10. Test Case Awal

| ID | Kategori | Input/Kondisi | Expected Result |
|---|---|---|---|
| TC01 | Normal | Tugas 80, UTS 70, UAS 90 | Nilai akhir 80 |
| TC02 | Batas | Nilai akhir tepat 75 | Status Lulus |
| TC03 | Invalid | Nilai tugas 105 | Ditolak karena di luar rentang |
| TC04 | Invalid | Nomor absen sudah digunakan | Ditolak karena duplikat |
| TC05 | Invalid | File data tidak ditemukan | Pesan kesalahan ditampilkan |
| TC06 | Normal | Semua siswa memiliki nilai akhir ≥ 75 | Jumlah siswa lulus sama dengan jumlah data |

## 11. Pembagian Tugas

Proyek dikerjakan secara individu.

| Tugas | Penanggung jawab |
|---|---|
| Perancangan kebutuhan dan ruang lingkup | Anastasya Putri Kirana |
| Perancangan algoritma dan pseudocode | Anastasya Putri Kirana |
| Perancangan struktur program | Anastasya Putri Kirana |
| Implementasi program | Anastasya Putri Kirana |
| Pengujian dan debugging | Anastasya Putri Kirana |
| Dokumentasi dan pengelolaan GitHub | Anastasya Putri Kirana |

## 12. Jadwal dan Milestone

| Tahap | Target Pengerjaan |
|---|---|
| Pertemuan 14 | Menyelesaikan proposal, struktur folder, pseudocode, dan test case |
| Antara Pertemuan 14–15 | Mempersiapkan struktur program dan implementasi awal |
| Pertemuan 15 | Implementasi fitur, integrasi, testing, debugging, dan dokumentasi |
| Pertemuan 16 | Presentasi, demonstrasi, dan evaluasi proyek |

## 13. Repository

Nama repository:

`analisis-nilai-siswa-2225250041`

Platform: GitHub

URL repository: Akan diisi setelah repository dibuat.

## Penutup

Program Analisis Nilai Siswa dirancang untuk membantu guru mengelola dan menganalisis nilai siswa secara lebih terstruktur. Dengan menggunakan Python, program diharapkan mampu mengurangi kesalahan perhitungan, mempermudah pencarian data, dan menghasilkan informasi kelulusan serta statistik kelas secara otomatis.

Rancangan ini akan menjadi dasar implementasi program pada Pertemuan 15.