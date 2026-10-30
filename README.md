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