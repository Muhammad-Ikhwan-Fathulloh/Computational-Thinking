# Materi Computational Thinking

## Apa Itu Computational Thinking?

**Computational Thinking (CT)** adalah proses berpikir sistematis yang digunakan untuk memecahkan masalah secara logis, terstruktur, dan dapat diterapkan dalam bentuk algoritma yang dijalankan oleh komputer.

> Computational Thinking bukan sekadar keterampilan coding, melainkan cara berpikir yang membantu kita memecahkan masalah dalam kehidupan sehari-hari maupun dalam teknologi.

---

## Empat Pilar Computational Thinking

| Pilar               | Penjelasan                                                    | Tujuan                                                 |
| ------------------- | ------------------------------------------------------------- | ------------------------------------------------------ |
| Decomposition       | Memecah masalah kompleks menjadi bagian kecil                 | Mempermudah penyelesaian masalah                       |
| Pattern Recognition | Mencari pola atau kesamaan antar masalah                      | Menyusun solusi yang efisien                           |
| Abstraction         | Mengabaikan detail yang tidak relevan, fokus pada hal penting | Menyederhanakan masalah                                |
| Algorithm Design    | Membuat langkah-langkah sistematis untuk solusi               | Membentuk dasar program yang dapat dijalankan komputer |

---

## Penjelasan Masing-Masing Pilar dengan Contoh

### 1. Decomposition (Dekonstruksi)

**Definisi:** Memecah masalah besar menjadi tugas-tugas kecil yang lebih mudah dikelola.
**Contoh:** Saat membuat aplikasi toko online, kita memecah menjadi:

* Fitur input produk.
* Fitur keranjang belanja.
* Fitur pembayaran.
* Fitur laporan.

---

### 2. Pattern Recognition (Pengenalan Pola)

**Definisi:** Mengidentifikasi pola atau kemiripan antar masalah untuk menyusun solusi yang efisien.
**Contoh:** Semua produk memiliki harga dan jumlah yang akan dihitung. Pola penghitungan total belanja selalu berupa perkalian harga dan jumlah produk.

---

### 3. Abstraction (Abstraksi)

**Definisi:** Mengabaikan informasi yang tidak relevan dan fokus pada elemen penting dari masalah.
**Contoh:** Untuk menghitung belanja, kita hanya perlu fokus pada harga dan jumlah produk, tanpa memikirkan warna atau merek produk.

---

### 4. Algorithm Design (Perancangan Algoritma)

**Definisi:** Menyusun langkah-langkah logis dan sistematis yang dapat dijalankan oleh komputer.
**Contoh:**

* Input harga barang.
* Hitung total belanja.
* Jika belanja melebihi batas, berikan diskon.
* Cetak total yang harus dibayar.

---

## Mengapa Computational Thinking Penting?

* Mempermudah membuat algoritma dan kode yang rapi.
* Mengurangi potensi kesalahan saat memecahkan masalah.
* Dapat diterapkan di berbagai bidang seperti kesehatan, keuangan, logistik, pendidikan, dan lainnya.
* Mempermudah pembelajaran pemrograman dasar.
* Membangun pola pikir logis dan sistematis.

---

# Studi Kasus 1: Menghitung Total Belanjaan

## Deskripsi Masalah

Seorang kasir ingin membuat sistem sederhana untuk menghitung total belanjaan pelanggan. Jika total belanja melebihi Rp 200.000, pelanggan mendapatkan diskon 10%.

---

## Langkah-Langkah Computational Thinking

### Decomposition

* Input jumlah barang.
* Input harga setiap barang.
* Hitung total harga.
* Jika total harga > Rp 200.000, berikan diskon 10%.
* Tampilkan total pembayaran.

### Pattern Recognition

* Semua barang memiliki harga.
* Pola perhitungan total selalu penjumlahan harga.
* Diskon hanya berlaku jika total melebihi Rp 200.000.

### Abstraction

* Fokus pada harga barang dan total belanja.
* Abaikan jenis barang, pembayaran tunai atau non-tunai.

### Algorithm Design

1. Input jumlah barang.
2. Ulangi input harga setiap barang.
3. Hitung total harga.
4. Jika total harga > Rp 200.000, hitung diskon 10%.
5. Tampilkan total akhir yang harus dibayar.

---

## Flowchart

```plaintext
+------------------+
|      Mulai       |
+------------------+
         |
         v
+------------------+
| Input jumlah     |
| barang           |
+------------------+
         |
         v
+------------------+
| Loop input harga |
| tiap barang      |
+------------------+
         |
         v
+------------------+
| Hitung total     |
+------------------+
         |
         v
+-----------------------------+
| Total > 200.000?            |
+-------------+---------------+
              | Yes
              v
   +---------------------------+
   | Hitung diskon 10%         |
   +---------------------------+
              |
              v
   +---------------------------+
   | Kurangi total dengan      |
   | diskon                    |
   +---------------------------+
              |
              v
+------------------+
| Tampilkan total  |
+------------------+
         |
         v
+------------------+
|      Selesai     |
+------------------+
```

---

## Pseudocode

```plaintext
START
Input jumlah_barang
Set total = 0
FOR i = 1 TO jumlah_barang DO
    Input harga_barang
    total = total + harga_barang
END FOR

IF total > 200000 THEN
    diskon = total * 10 / 100
    total = total - diskon
END IF

Output total pembayaran
END
```

---

## Implementasi Python

```python
# Program Menghitung Total Belanjaan dengan Diskon

# Input jumlah barang
jumlah_barang = int(input("Masukkan jumlah barang: "))

# Inisialisasi total
total = 0

# Input harga barang dan hitung total
for i in range(jumlah_barang):
    harga = float(input(f"Masukkan harga barang ke-{i+1}: "))
    total += harga

# Cek apakah dapat diskon
if total > 200000:
    diskon = total * 0.10
    total -= diskon
    print(f"Diskon 10% sebesar: Rp {diskon:,.2f}")
else:
    print("Tidak mendapatkan diskon.")

# Tampilkan total pembayaran
print(f"Total yang harus dibayar: Rp {total:,.2f}")
```

---

# Studi Kasus 2: Sistem Penilaian Mahasiswa

## Deskripsi Masalah

Hitung nilai akhir mahasiswa dengan bobot:

* Tugas: 30%
* UTS: 30%
* UAS: 40%

Tentukan kelulusan:

* Lulus jika nilai akhir ≥ 70
* Tidak lulus jika nilai akhir < 70

---

## Langkah-Langkah Computational Thinking

### Decomposition

* Input nama mahasiswa.
* Input nilai Tugas, UTS, UAS.
* Hitung nilai akhir.
* Tentukan kelulusan.
* Cetak hasil.

### Pattern Recognition

* Semua mahasiswa memiliki 3 jenis nilai.
* Kelulusan ditentukan oleh batas nilai yang sama (≥ 70).

### Abstraction

* Fokus pada input nama dan 3 nilai.
* Abaikan jurusan, dosen, dan mata kuliah.

### Algorithm Design

1. Input nama mahasiswa.
2. Input nilai Tugas, UTS, UAS.
3. Hitung nilai akhir.
4. Tentukan kelulusan.
5. Cetak hasil.

---

## Pseudocode

```plaintext
START
Input nama
Input nilai_tugas
Input nilai_uts
Input nilai_uas

nilai_akhir = (nilai_tugas * 0.3) + (nilai_uts * 0.3) + (nilai_uas * 0.4)

IF nilai_akhir >= 70 THEN
    status = "Lulus"
ELSE
    status = "Tidak Lulus"
END IF

Output nama, nilai_akhir, status
END
```

---

## Implementasi Python

```python
# Program Menghitung Nilai Akhir Mahasiswa

# Input data mahasiswa
nama = input("Masukkan nama mahasiswa: ")
nilai_tugas = float(input("Masukkan nilai Tugas: "))
nilai_uts = float(input("Masukkan nilai UTS: "))
nilai_uas = float(input("Masukkan nilai UAS: "))

# Hitung nilai akhir
nilai_akhir = (nilai_tugas * 0.3) + (nilai_uts * 0.3) + (nilai_uas * 0.4)

# Menentukan kelulusan
if nilai_akhir >= 70:
    status = "Lulus"
else:
    status = "Tidak Lulus"

# Cetak hasil
print("\n===== Hasil Akhir =====")
print(f"Nama Mahasiswa : {nama}")
print(f"Nilai Akhir    : {nilai_akhir:.2f}")
print(f"Status         : {status}")
```

---

# Latihan Soal Computational Thinking

## Level 1 (Mudah)

**Kasus:** Buat program untuk menghitung luas lingkaran.

* Input jari-jari lingkaran.
* Hitung luas dengan rumus L = π \* r².
* Cetak hasil.

---

## Level 2 (Menengah)

**Kasus:** Buat sistem penilaian 5 mata pelajaran, tentukan apakah siswa lulus (rata-rata nilai minimal 75).

* Input nilai 5 mata pelajaran.
* Hitung rata-rata.
* Jika rata-rata ≥ 75, cetak "Lulus".
* Jika rata-rata < 75, cetak "Tidak Lulus".

---

## Level 3 (Sulit)

**Kasus:** Sistem parkir:

* 2 jam pertama: Rp 5.000.
* Jam berikutnya: Rp 3.000 per jam.
* Jika total biaya parkir melebihi Rp 20.000, diskon 15%.

Tentukan:

* Biaya parkir total.
* Cetak struk pembayaran.

---

# Kesimpulan

| Aspek            | Penjelasan                                         |
| ---------------- | -------------------------------------------------- |
| Tujuan           | Memecah masalah, mengenali pola, membuat algoritma |
| Pentingnya       | Menyusun langkah sebelum coding                    |
| Hasil            | Membantu membuat program lebih rapi dan logis      |
| Manfaat Tambahan | Meningkatkan pola pikir sistematis dan efisien     |
