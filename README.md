# Pertemuan 04 Seleksi Multi-Kondisi dan Validasi Input

Nama: Azizah Nur Kholishah

NIM: 2225250116

Kelas: 3E

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

### 1. Predikat Nilai
| Kondisi | Predikat |
|---|---|
| Nilai ≥ 85 | A |
| Nilai ≥ 70 dan Nilai < 85 | B |
| Nilai ≥ 60 dan Nilai < 70 | C |
| Nilai ≥ 50 dan Nilai < 60 | D |
| Nilai < 50 | E |

### 2. Klasifikasi Bilangan Bulat
| Kondisi | Keputusan |
|---|---|
| x < 0 | Bilangan negatif |
| x == 0 | Nol |
| x > 0 dan x % 2 == 0 | Bilangan positif genap |
| x > 0 dan x % 2 != 0 | Bilangan positif ganjil |

### 3. Validasi Rentang 
| Kondisi | Keputusan |
|---|---|
| sudut ≤ 0 atau sudut ≥ 180 | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180 |
| 0 < sudut < 90 | Sudut lancip |
| sudut == 90 | Sudut siku-siku |
| 90 < sudut < 180 | Sudut tumpul |

### 4. Validaasi Tipe
| Kondisi | Keputusan |
|---|---|
| Input bukan bilangan bulat | Masukan ditolak: jumlah harus berupa bilangan bulat |
| benar < 0 atau benar > 20 | Masukan ditolak: jumlah harus berada pada rentang 0 sampai 20 |
| 0 ≤ benar ≤ 20 dan persen ≥ 75 | Tuntas |
| 0 ≤ benar ≤ 20 dan persen < 75 | Belum tuntas |

### 5. Klasifikasi Segitiga Berdasarkan Sudut
| Kondisi | Keputusan |
|---|---|
| a ≤ 0 atau b ≤ 0 atau c ≤ 0 | Masukan ditolak: setiap sudut harus lebih dari 0 derajat |
| abs(a + b + c - 180) > 1e-9 | Masukan ditolak: jumlah ketiga sudut harus 180 derajat |
| Sudut terbesar > 90 | Segitiga tumpul |
| Sudut terbesar == 90 | Segitiga siku-siku |
| Sudut terbesar < 90 | Segitiga lancip |

### 6. Praktik 1 (Validasi dan Klasifikasi Nilai Akhir)
Nilai akhir dihitung menggunakan rumus:

Nilai Akhir = (0.6 × Nilai Ujian) + (0.4 × Nilai Tugas)

Mahasiswa harus memiliki kehadiran minimal 80% untuk dapat memperoleh predikat.

| Kondisi | Keputusan |
|---|---|
| Input bukan angka | Masukan ditolak: seluruh data harus berupa angka |
| Nilai ujian di luar rentang 0-100 | Penolakan nilai ujian |
| Nilai tugas di luar rentang 0-100 | Penolakan nilai tugas |
| Kehadiran di luar rentang 0-100 | Penolakan kehadiran |
| Kehadiran < 80 | Tidak memenuhi syarat kehadiran |
| Nilai akhir ≥ 85 | Predikat A, Lulus |
| 70 ≤ Nilai akhir < 85 | Predikat B, Lulus |
| 60 ≤ Nilai akhir < 70 | Predikat C, Lulus |
| 50 ≤ Nilai akhir < 60 | Predikat D, Belum lulus |
| Nilai akhir < 50 | Predikat E, Belum lulus |

## Hasil Pengujian

### 1. Latihan 1 - Predikat Nilai
| Input | Output |
|---|---|
| 92 | Nilai 92.00 memperoleh predikat A |
| 85 | Nilai 85.00 memperoleh predikat A |
| 84.9 | Nilai 84.90 memperoleh predikat B |
| 70 | Nilai 70.00 memperoleh predikat B |
| 60 | Nilai 60.00 memperoleh predikat C |
| 50 | Nilai 50.00 memperoleh predikat D |
| 49.9 | Nilai 49.90 memperoleh predikat E |

### 2. Latihan 2 - Klasifikasi Bilangan Bulat
| Input | Output |
|---|---|
| -7 | Bilangan negatif |
| 0 | Nol |
| 8 | Bilangan positif genap |
| 13 | Bilangan positif ganjil |

### 3. Latihan 3 - Validasi Rentang 
| Input | Output |
|---|---|
| 45 | Sudut lancip |
| 90 | Sudut siku-siku |
| 135 | Sudut tumpul |
| 0 | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180 |
| 180 | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180 |
| -30 | Masukan ditolak: sudut harus lebih dari 0 dan kurang dari 180 |

### 4. Latihan 4 - Validasi Tipe
| Input | Output |
|---|---|
| 15 | Persentase = 75.00 persen, Tuntas |
| 14 | Persentase = 70.00 persen, Belum tuntas |
| 20 | Persentase = 100.00 persen, Tuntas |
| 0 | Persentase = 0.00 persen, Belum tuntas |
| 21 | Masukan ditolak: jumlah harus berada pada rentang 0 sampai 20 |
| dua belas | Masukan ditolak: jumlah harus berupa bilangan bulat |

### 5. Latihan 5 - Klasifikasi Segitiga Berdasarkan Sudut
| Input | Output |
|---|---|
| 60, 60, 60 | Segitiga lancip |
| 90, 45, 45 | Segitiga siku-siku |
| 120, 30, 30 | Segitiga tumpul |
| 100, 50, 40 | Masukan ditolak: jumlah ketiga sudut harus 180 derajat |
| 0, 90, 90 | Masukan ditolak: setiap sudut harus lebih dari 0 derajat |

### Praktik 1 - Validasi dan Klasifikasi Nilai Akhir
| Nilai Ujian | Nilai Tugas | Kehadiran | Output |
|---|---|---|---|
| 90 | 80 | 95 | Nilai akhir = 86.00, Predikat A, Lulus |
| 75 | 70 | 85 | Nilai akhir = 73.00, Predikat B, Lulus |
| 60 | 60 | 80 | Nilai akhir = 60.00, Predikat C, Lulus |
| 55 | 50 | 90 | Nilai akhir = 53.00, Predikat D, Belum lulus |
| 40 | 30 | 100 | Nilai akhir = 36.00, Predikat E, Belum lulus |
| 90 | 90 | 75 | Nilai akhir = 90.00, Tidak memenuhi syarat kehadiran |
| 105 | 80 | 90 | Masukan ditolak: nilai ujian di luar rentang 0 sampai 100 |
| 80 | -5 | 90 | Masukan ditolak: nilai tugas di luar rentang 0 sampai 100 |
| 80 | 80 | abc | Masukan ditolak: seluruh data harus berupa angka |

## Refleksi 
Pada pertemuan ini, saya belajar menggunakan if-elif-else untuk membuat program dengan beberapa kondisi serta melakukan validasi input. Dari latihan yang dilakukan, saya menjadi lebih memahami cara mengklasifikasikan data dan menangani input yang tidak sesuai. 

Pada Praktik 1, saya juga belajar menggabungkan validasi nilai ujian, tugas, dan kehadiran untuk menentukan nilai akhir serta predikat mahasiswa. Hasil pengujian menunjukkan bahwa program dapat berjalan sesuai dengan kondisi yang telah ditentukan.
