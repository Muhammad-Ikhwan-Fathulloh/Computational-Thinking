# Pembahasan dan Jawaban Latihan Soal Computational Thinking

---

## Latihan Soal Level 1 (Mudah)

### Kasus: Menghitung Luas Lingkaran

### Langkah Computational Thinking

**Decomposition**

* Input jari-jari lingkaran.
* Hitung luas lingkaran dengan rumus L = π \* r².
* Tampilkan hasil.

**Pattern Recognition**

* Semua lingkaran dihitung dengan rumus yang sama.

**Abstraction**

* Fokus pada input jari-jari dan hasil luas.
* Abaikan warna, tebal garis, atau posisi lingkaran.

**Algorithm Design**

1. Input jari-jari.
2. Hitung luas dengan rumus L = π \* r².
3. Tampilkan hasil.

---

### Pseudocode

```plaintext
START
Input jari_jari
luas = 3.14 * jari_jari * jari_jari
Output luas
END
```

---

### Implementasi Python

```python
# Program Menghitung Luas Lingkaran

# Input jari-jari
jari_jari = float(input("Masukkan jari-jari lingkaran: "))

# Hitung luas
luas = 3.14 * jari_jari * jari_jari

# Cetak hasil
print(f"Luas lingkaran: {luas:.2f}")
```

---

## Latihan Soal Level 2 (Menengah)

### Kasus: Menentukan Kelulusan Berdasarkan 5 Mata Pelajaran

### Langkah Computational Thinking

**Decomposition**

* Input nilai 5 mata pelajaran.
* Hitung rata-rata nilai.
* Jika rata-rata ≥ 75, cetak "Lulus".
* Jika rata-rata < 75, cetak "Tidak Lulus".

**Pattern Recognition**

* Semua siswa memiliki 5 nilai.
* Pola kelulusan menggunakan rata-rata nilai.

**Abstraction**

* Fokus pada perhitungan rata-rata dan status kelulusan.

**Algorithm Design**

1. Input nilai 5 mata pelajaran.
2. Hitung rata-rata.
3. Tentukan kelulusan.
4. Tampilkan hasil.

---

### Pseudocode

```plaintext
START
Input nilai1, nilai2, nilai3, nilai4, nilai5
rata_rata = (nilai1 + nilai2 + nilai3 + nilai4 + nilai5) / 5

IF rata_rata >= 75 THEN
    status = "Lulus"
ELSE
    status = "Tidak Lulus"
END IF

Output rata_rata, status
END
```

---

### Implementasi Python

```python
# Program Menentukan Kelulusan

# Input nilai
nilai = []
for i in range(5):
    nilai_input = float(input(f"Masukkan nilai mata pelajaran ke-{i+1}: "))
    nilai.append(nilai_input)

# Hitung rata-rata
rata_rata = sum(nilai) / len(nilai)

# Menentukan kelulusan
if rata_rata >= 75:
    status = "Lulus"
else:
    status = "Tidak Lulus"

# Cetak hasil
print(f"Rata-rata nilai: {rata_rata:.2f}")
print(f"Status: {status}")
```

---

## Latihan Soal Level 3 (Sulit)

### Kasus: Sistem Parkir dengan Diskon

### Langkah Computational Thinking

**Decomposition**

* Input lama parkir.
* Hitung biaya 2 jam pertama: Rp 5.000.
* Hitung biaya sisa jam: Rp 3.000 per jam.
* Jika total biaya > Rp 20.000, diskon 15%.
* Cetak total biaya.

**Pattern Recognition**

* Semua kendaraan membayar biaya awal yang sama.
* Biaya tambahan per jam berikutnya.
* Diskon berlaku jika total biaya melebihi Rp 20.000.

**Abstraction**

* Fokus pada lama parkir dan total biaya.
* Abaikan jenis kendaraan atau metode pembayaran.

**Algorithm Design**

1. Input lama parkir.
2. Hitung biaya 2 jam pertama.
3. Hitung biaya tambahan jika lebih dari 2 jam.
4. Jika total biaya > 20.000, hitung diskon 15%.
5. Tampilkan biaya total.

---

### Pseudocode

```plaintext
START
Input lama_parkir

IF lama_parkir <= 2 THEN
    biaya = 5000
ELSE
    biaya = 5000 + (lama_parkir - 2) * 3000
END IF

IF biaya > 20000 THEN
    diskon = biaya * 0.15
    biaya = biaya - diskon
END IF

Output biaya
END
```

---

### Implementasi Python

```python
# Program Sistem Parkir dengan Diskon

# Input lama parkir
lama_parkir = float(input("Masukkan lama parkir (jam): "))

# Hitung biaya parkir
if lama_parkir <= 2:
    biaya = 5000
else:
    biaya = 5000 + (lama_parkir - 2) * 3000

# Hitung diskon jika biaya > Rp 20.000
if biaya > 20000:
    diskon = biaya * 0.15
    biaya -= diskon
    print(f"Diskon 15% sebesar: Rp {diskon:,.2f}")
else:
    print("Tidak mendapatkan diskon.")

# Cetak total biaya
print(f"Total biaya parkir: Rp {biaya:,.2f}")
```

---

## Kesimpulan

| Aspek          | Penjelasan                                    |
| -------------- | --------------------------------------------- |
| Level Mudah    | Hitung luas lingkaran                         |
| Level Menengah | Hitung rata-rata nilai dan kelulusan siswa    |
| Level Sulit    | Sistem perhitungan biaya parkir dengan diskon |
