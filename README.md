# Pertemuan 04 Seleksi Multi-Kondisi dan Validasi Input

Nama: [Nama Kamu]
NIM: [NIM Kamu]
Kelas: [Kelas Kamu]

## Tujuan
Pada pertemuan ini, saya bertujuan memahami penggunaan seleksi multi-kondisi dengan if-elif-else serta mempelajari cara melakukan validasi input agar program dapat mengolah data sesuai dengan kondisi yang telah ditentukan.

## Cara Menjalankan

Buka terminal di VS Code, lalu jalankan perintah berikut:

```bash
# Menjalankan Latihan (Contoh: Latihan 1)
python3 latihan/01_predikat_nilai.py

# Menjalankan Praktik 1
python3 praktik/validasi_klasifikasi_nilai.py
```

## Tabel Keputusan

### 1. Latihan 1 (Predikat Nilai)
| Kondisi Nilai | Predikat |
| :--- | :---: |
| Nilai >= 85 | A |
| 70 <= Nilai < 85 | B |
| 60 <= Nilai < 70 | C |
| 50 <= Nilai < 60 | D |
| Nilai < 50 | E |

### 2. Latihan 2 (Klasifikasi Bilangan Bulat)
| Kondisi Angka (x) | Jenis Bilangan |
| :--- | :--- |
| x < 0 | Bilangan negatif |
| x == 0 | Nol |
| x > 0 dan x % 2 == 0 | Bilangan positif genap |
| x > 0 dan x % 2 != 0 | Bilangan positif ganjil |

### 3. Latihan 3 (Klasifikasi Sudut)
| Besarnya Sudut ($\theta$) | Klasifikasi / Output |
| :--- | :--- |
| $\theta \le 0$ atau $\theta \ge 180$ | Masukan ditolak |
| $0 < \theta < 90$ | Sudut lancip |
| $\theta == 90$ | Sudut siku-siku |
| $90 < \theta < 180$ | Sudut tumpul |

### 4. Latihan 4 (Ketuntasan Soal dari 20)
| Condition / Syarat | Status / Output |
| :--- | :--- |
| Input bukan integer | Masukan ditolak: jumlah harus berupa bilangan bulat |
| Soal Benar < 0 atau Soal Benar > 20 | Masukan ditolak: jumlah harus berada pada rentang 0 sampai 20 |
| Persentase Benar >= 75% | Tuntas |
| Persentase Benar < 75% | Belum tuntas |

### 5. Latihan 5 (Klasifikasi Segitiga Berdasarkan Sudut)
| Kondisi Sudut (A, B, C) | Output |
| :--- | :--- |
| A <= 0 atau B <= 0 atau C <= 0 | Masukan ditolak: setiap sudut harus lebih dari 0 derajat |
| A + B + C != 180 | Masukan ditolak: jumlah ketiga sudut harus 180 derajat |
| Sudut Terbesar > 90 | Segitiga tumpul |
| Sudut Terbesar == 90 | Segitiga siku-siku |
| Sudut Terbesar < 90 | Segitiga lancip |

### 6. Praktik 1 (Validasi dan Klasifikasi Nilai Akhir)
| Kategori / Kondisi | Syarat | Hasil / Output |
| :--- | :--- | :--- |
| Tipe Non-Angka | Input Ujian/Tugas/Hadir berupa teks | Masukan ditolak: seluruh data harus berupa angka. |
| Rentang Ujian | Ujian < 0 atau Ujian > 100 | Masukan ditolak: nilai ujian di luar rentang 0 sampai 100. |
| Rentang Tugas | Tugas < 0 atau Tugas > 100 | Masukan ditolak: nilai tugas di luar rentang 0 sampai 100. |
| Rentang Hadir | Hadir < 0 atau Hadir > 100 | Masukan ditolak: kehadiran di luar rentang 0 sampai 100. |
| Kehadiran Kurang | Kehadiran < 80% | Status = Tidak memenuhi syarat kehadiran |
| Predikat A | Hadir >= 80% dan Nilai Akhir >= 85 | Predikat A, Lulus |
| Predikat B | Hadir >= 80% dan 70 <= Nilai Akhir < 85 | Predikat B, Lulus |
| Predikat C | Hadir >= 80% dan 60 <= Nilai Akhir < 70 | Predikat C, Lulus |
| Predikat D | Hadir >= 80% dan 50 <= Nilai Akhir < 60 | Predikat D, Belum lulus |
| Predikat E | Hadir >= 80% dan Nilai Akhir < 50 | Predikat E, Belum lulus |

## Hasil Pengujian

### 1. Hasil Pengujian Latihan 1 (Predikat Nilai)
| Masukan (Nilai) | Keluaran yang Diharapkan | Keluaran Aktual | Status |
| :---: | :--- | :--- | :---: |
| 90 | Nilai 90.00 memperoleh predikat A. | Nilai 90.00 memperoleh predikat A. | Sesuai |
| 75 | Nilai 75.00 memperoleh predikat B. | Nilai 75.00 memperoleh predikat B. | Sesuai |
| 65 | Nilai 65.00 memperoleh predikat C. | Nilai 65.00 memperoleh predikat C. | Sesuai |
| 55 | Nilai 55.00 memperoleh predikat D. | Nilai 55.00 memperoleh predikat D. | Sesuai |
| 40 | Nilai 40.00 memperoleh predikat E. | Nilai 40.00 memperoleh predikat E. | Sesuai |

### 2. Hasil Pengujian Latihan 2 (Klasifikasi Bilangan Bulat)
| Masukan (x) | Keluaran yang Diharapkan | Keluaran Aktual | Status |
| :---: | :--- | :--- | :---: |
| -5 | Bilangan negatif | Bilangan negatif | Sesuai |
| 0 | Nol | Nol | Sesuai |
| 4 | Bilangan positif genap | Bilangan positif genap | Sesuai |
| 7 | Bilangan positif ganjil | Bilangan positif ganjil | Sesuai |

### 3. Hasil Pengujian Latihan 3 (Klasifikasi Sudut)
| Masukan (Sudut) | Keluaran yang Diharapkan | Keluaran Aktual | Status |
| :---: | :--- | :--- | :---: |
| 0 | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180. | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180. | Sesuai |
| 45 | Sudut lancip | Sudut lancip | Sesuai |
| 90 | Sudut siku-siku | Sudut siku-siku | Sesuai |
| 120 | Sudut tumpul | Sudut tumpul | Sesuai |
| 180 | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180. | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180. | Sesuai |

### 4. Hasil Pengujian Latihan 4 (Ketuntasan Soal dari 20)
| Masukan (Soal Benar) | Keluaran yang Diharapkan | Keluaran Aktual | Status |
| :---: | :--- | :--- | :---: |
| abc | Masukan ditolak: jumlah harus berupa bilangan bulat. | Masukan ditolak: jumlah harus berupa bilangan bulat. | Sesuai |
| -2 | Masukan ditolak: jumlah harus berada pada rentang 0 sampai 20. | Masukan ditolak: jumlah harus berada pada rentang 0 sampai 20. | Sesuai |
| 25 | Masukan ditolak: jumlah harus berada pada rentang 0 sampai 20. | Masukan ditolak: jumlah harus berada pada rentang 0 sampai 20. | Sesuai |
| 16 | Persentase = 80.00 persen<br>Tuntas | Persentase = 80.00 persen<br>Tuntas | Sesuai |
| 10 | Persentase = 50.00 persen<br>Belum tuntas | Persentase = 50.00 persen<br>Belum tuntas | Sesuai |

### 5. Hasil Pengujian Latihan 5 (Klasifikasi Segitiga Berdasarkan Sudut)
| Sudut A | Sudut B | Sudut C | Keluaran yang Diharapkan | Keluaran Aktual | Status |
| :---: | :---: | :---: | :--- | :--- | :---: |
| 0 | 90 | 90 | Masukan ditolak: setiap sudut harus lebih dari 0 derajat. | Masukan ditolak: setiap sudut harus lebih dari 0 derajat. | Sesuai |
| 60 | 60 | 70 | Masukan ditolak: jumlah ketiga sudut harus 180 derajat. | Masukan ditolak: jumlah ketiga sudut harus 180 derajat. | Sesuai |
| 100 | 40 | 40 | Segitiga tumpul | Segitiga tumpul | Sesuai |
| 90 | 45 | 45 | Segitiga siku-siku | Segitiga siku-siku | Sesuai |
| 60 | 60 | 60 | Segitiga lancip | Segitiga lancip | Sesuai |

### Hasil Pengujian Praktik 1 (Validasi dan Klasifikasi Nilai Akhir)
| Ujian | Tugas | Kehadiran | Nilai Akhir | Keluaran yang Diharapkan | Keluaran Aktual | Status |
| :---: | :---: | :---: | :---: | :--- | :--- | :---: |
| 90 | 80 | 95 | 86.00 | Predikat A, Lulus | Nilai akhir = 86.00<br>Predikat A, Lulus | Sesuai |
| 75 | 70 | 85 | 73.00 | Predikat B, Lulus | Nilai akhir = 73.00<br>Predikat B, Lulus | Sesuai |
| 60 | 60 | 80 | 60.00 | Predikat C, Lulus | Nilai akhir = 60.00<br>Predikat C, Lulus | Sesuai |
| 55 | 50 | 90 | 53.00 | Predikat D, Belum lulus | Nilai akhir = 53.00<br>Predikat D, Belum lulus | Sesuai |
| 40 | 30 | 100 | 36.00 | Predikat E, Belum lulus | Nilai akhir = 36.00<br>Predikat E, Belum lulus | Sesuai |
| 90 | 90 | 75 | 90.00 | Nilai akhir tetap tampil, status Tidak memenuhi syarat kehadiran | Nilai akhir = 90.00<br>Status = Tidak memenuhi syarat kehadiran | Sesuai |
| 105 | 80 | 90 | - | Pesan penolakan rentang nilai ujian | Masukan ditolak: nilai ujian di luar rentang 0 sampai 100. | Sesuai |
| 80 | -5 | 90 | - | Pesan penolakan rentang nilai tugas | Masukan ditolak: nilai tugas di luar rentang 0 sampai 100. | Sesuai |
| 80 | 80 | abc | - | Pesan penolakan tipe | Masukan ditolak: seluruh data harus berupa angka. | Sesuai |

## Refleksi 
Pada pertemuan ini, saya belajar menggunakan if-elif-else untuk membuat program dengan beberapa kondisi serta melakukan validasi input. Dari latihan yang dilakukan, saya menjadi lebih memahami cara mengklasifikasikan data dan menangani input yang tidak sesuai. 

Pada Praktik 1, saya juga belajar menggabungkan validasi nilai ujian, tugas, dan kehadiran untuk menentukan nilai akhir serta predikat mahasiswa. Hasil pengujian menunjukkan bahwa program dapat berjalan sesuai dengan kondisi yang telah ditentukan.