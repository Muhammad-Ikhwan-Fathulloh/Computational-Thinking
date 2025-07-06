# Materi Computational Thinking

## Apa Itu Computational Thinking?

**Computational Thinking (CT)** adalah pendekatan sistematis untuk memecahkan masalah yang dapat diselesaikan secara efektif, efisien, dan seringkali bisa diotomatisasi oleh komputer.

> Computational Thinking bukan tentang menjadi programmer, tetapi tentang berpikir seperti seorang programmer.

---

## Empat Pilar Computational Thinking

| Pilar               | Penjelasan                                                    | Tujuan                                                 |
| ------------------- | ------------------------------------------------------------- | ------------------------------------------------------ |
| Decomposition       | Memecah masalah kompleks menjadi bagian kecil                 | Mempermudah penyelesaian masalah                       |
| Pattern Recognition | Mencari pola atau kesamaan antar masalah                      | Menyusun solusi yang efisien                           |
| Abstraction         | Mengabaikan detail yang tidak relevan, fokus pada hal penting | Menyederhanakan masalah                                |
| Algorithm Design    | Membuat langkah-langkah sistematis untuk solusi               | Membentuk dasar program yang dapat dijalankan komputer |

---

## Kenapa Computational Thinking Penting?

* Memahami alur sebelum ngoding.
* Mempermudah membuat algoritma yang rapi.
* Meminimalisir kesalahan.
* Membantu berpikir logis dan terstruktur.
* Dapat diaplikasikan dalam semua bidang (bukan hanya IT).

---

## Studi Kasus: Menghitung Total Belanjaan

### Deskripsi Masalah:

Seorang kasir ingin membuat sistem sederhana untuk menghitung total belanjaan pelanggan. Jika total belanja melebihi Rp 200.000, pelanggan mendapatkan diskon 10%.

---

## Step 1: Decomposition

### Memecah Masalah

* Input jumlah barang.
* Input harga setiap barang.
* Hitung total harga.
* Jika total harga > Rp 200.000, diskon 10%.
* Cetak total pembayaran.

---

## Step 2: Pattern Recognition

### Pola yang Terlihat

* Setiap barang memiliki harga.
* Perhitungan total adalah proses penjumlahan.
* Diskon hanya terjadi jika total harga melebihi batas.

---

## Step 3: Abstraction

### Fokus Utama

* Hanya menghitung harga dan diskon.
* Mengabaikan: jenis barang, metode pembayaran, pajak, dsb.

---

## Step 4: Algorithm Design

### Menyusun Langkah Solusi

1. Minta input jumlah barang.
2. Input harga setiap barang (diulang).
3. Hitung total harga.
4. Jika total > 200.000, hitung diskon 10%.
5. Tampilkan total akhir.

---

## Flowchart Proses

```plaintext
+------------------+
|     Mulai        |
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

## Implementasi Koding Python

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

## Kesimpulan

| Aspek      | Penjelasan                                      |
| ---------- | ----------------------------------------------- |
| Tujuan CT  | Memecah masalah, mengenali pola, membuat solusi |
| Pentingnya | Menyusun langkah sebelum coding                 |
| Hasil      | Membantu membuat program lebih rapi dan logis   |

---

## Tambahan: Tips Computational Thinking

* Selalu mulai dari **dekomposisi** masalah.
* Gunakan **flowchart** atau **pseudocode** sebelum coding.
* Berlatih dengan masalah sederhana, lalu tingkatkan kompleksitas.
* Jangan langsung menulis kode tanpa pemahaman alur.
