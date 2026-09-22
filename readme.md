# JOHN TRAVOLTA ASSIGNMENT

## 1. Deskripsi Permasalahan

John Travolta adalah seorang karyawan yang mendapatkan gaji mingguan berdasarkan jumlah jam kerja.

* Jam kerja normal: **40 jam/minggu**
* Rate normal: **Rp15.000/jam**
* Jam kerja di atas 40 jam dihitung sebagai lembur
* Rate lembur: **1,5 × rate normal**

Selain menghitung gaji, program menentukan kondisi keuangan berdasarkan perbandingan antara pemasukan dan pengeluaran.

---

## 2. Analisis Masalah

### Input

* Jumlah jam kerja
* Jumlah pengeluaran mingguan

### Proses

1. Menghitung gaji normal.
2. Menghitung gaji lembur jika jam kerja lebih dari 40 jam.
3. Menghitung total gaji.
4. Membandingkan pemasukan dengan pengeluaran.
5. Menentukan status tabungan.

### Output

* Total gaji mingguan.
* Status keuangan.
* Jumlah tabungan atau kekurangan.

---

## 3. Perhitungan Manual

### Diketahui

* Jam kerja = **52 jam**
* Jam normal = **40 jam**
* Rate normal = **Rp15.000/jam**
* Pengeluaran = **Rp600.000**

### Gaji Normal

```text
40 × Rp15.000 = Rp600.000
```

### Jam Lembur

```text
52 − 40 = 12 jam
```

### Rate Lembur

```text
1,5 × Rp15.000 = Rp22.500/jam
```

### Gaji Lembur

```text
12 × Rp22.500 = Rp270.000
```

### Total Gaji

```text
Rp600.000 + Rp270.000 = Rp870.000
```

**Total gaji John Travolta = Rp870.000.**

### Perhitungan Tabungan

```text
Pendapatan  = Rp870.000
Pengeluaran = Rp600.000

Rp870.000 > Rp600.000
```

Maka John **bisa menabung**.

```text
Tabungan = Rp870.000 − Rp600.000
         = Rp270.000
```

**Tabungan John = Rp270.000.**

---

## 4. Algoritma Menghitung Gaji

```text
START

Input jumlah jam kerja

Jika jam kerja <= 40:
    gaji = jam kerja × 15000

Jika jam kerja > 40:
    jam lembur = jam kerja - 40
    gaji normal = 40 × 15000
    rate lembur = 1,5 × 15000
    gaji lembur = jam lembur × rate lembur
    total gaji = gaji normal + gaji lembur

Tampilkan total gaji

END
```

---

## 5. Program Python Menghitung Gaji

```python
rate = 15000

jam = int(input("Masukkan jumlah jam kerja: "))

if jam <= 40:
    gaji = jam * rate
else:
    lembur = jam - 40
    gaji = (40 * rate) + (lembur * rate * 1.5)

print("Total gaji: Rp", int(gaji))
```

### Contoh Output

```text
Masukkan jumlah jam kerja: 52
Total gaji: Rp 870000
```

---

## 6. Algoritma Menghitung Tabungan

```text
START

Input pemasukan
Input pengeluaran

Jika pemasukan > pengeluaran:
    tabungan = pemasukan - pengeluaran
    tampilkan "Bisa menabung"
    tampilkan tabungan

Jika pemasukan = pengeluaran:
    tampilkan "Tidak bisa menabung"

Jika pemasukan < pengeluaran:
    kekurangan = pengeluaran - pemasukan
    tampilkan "Cari tambahan"
    tampilkan kekurangan

END
```

---

## 7. Program Python Menghitung Tabungan

```python
pemasukan = int(input("Masukkan pemasukan: "))
pengeluaran = int(input("Masukkan pengeluaran: "))

if pemasukan > pengeluaran:
    tabungan = pemasukan - pengeluaran
    print("Bisa menabung")
    print("Jumlah tabungan:", tabungan)

elif pemasukan == pengeluaran:
    print("Tidak bisa menabung")

else:
    kekurangan = pengeluaran - pemasukan
    print("Cari tambahan")
    print("Kekurangan:", kekurangan)
```

### Contoh Output

```text
Masukkan pemasukan: 870000
Masukkan pengeluaran: 600000

Bisa menabung
Jumlah tabungan: 270000
```

---

## 8. Testing Scenario / Test Case

|  No. | Input                 | Skenario                 | Expected Output         |
| ---: | --------------------- | ------------------------ | ----------------------- |
| TC01 | 40 jam                | Jam kerja normal         | Rp600.000               |
| TC02 | 52 jam                | Jam kerja dengan lembur  | Rp870.000               |
| TC03 | 60 jam                | Jam lembur lebih tinggi  | Rp1.050.000             |
| TC04 | Rp870.000 / Rp600.000 | Pendapatan > pengeluaran | Bisa menabung Rp270.000 |
| TC05 | Rp500.000 / Rp500.000 | Pendapatan = pengeluaran | Tidak bisa menabung     |
| TC06 | Rp400.000 / Rp700.000 | Pendapatan < pengeluaran | Cari tambahan           |

---

## 9. Perkembangan Pengerjaan

1. Memahami kebutuhan dan aturan perhitungan.
2. Menentukan input, proses, dan output.
3. Membuat algoritma menggunakan percabangan.
4. Mengimplementasikan algoritma menggunakan Python.
5. Menguji program dengan beberapa skenario.
6. Memastikan program dapat digunakan dengan nilai input yang berbeda.

---

## 10. Kesimpulan

John Travolta bekerja selama **52 jam** dengan rate **Rp15.000/jam**. Setelah menghitung 40 jam kerja normal dan 12 jam lembur, diperoleh total gaji sebesar **Rp870.000**.

Dengan pengeluaran sebesar **Rp600.000**, John memiliki sisa sebesar **Rp270.000**, sehingga John **bisa menabung Rp270.000** dalam satu minggu.

Program juga dapat digunakan untuk menghitung gaji dan kondisi tabungan dengan berbagai nilai input.
