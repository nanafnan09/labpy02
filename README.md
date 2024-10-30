# Pratikum 2

Nama:Afnan Dika Ramadhan

NIM 312410518

Mata Kuliah :Bahasa Pemrograman

# Kegunaan `if`,`else`,`elif` dalam python

Penggunaan `if`, `else`, dan `elif` dalam Python adalah bagian penting dari kontrol aliran program, yang memungkinkan pengembang untuk membuat keputusan berdasarkan kondisi tertentu. Berikut adalah penjelasan mendetail mengenai masing-masing pernyataan tersebut.

# If
`If` digunakan untuk mengeksekusi blok kode tertentu jika kondisi yang diberikan bernilai True. Jika kondisi tersebut bernilai False, maka blok kode di bawahnya akan diabaikan.

# Else
`Else` digunakan bersama dengan `if` untuk menangani semua kemungkinan lain ketika kondisi dalam `if` tidak terpenuhi. Blok kode di bawah `else` hanya akan dieksekusi jika kondisi dalam `if` bernilai False.

# Elif
`Elif,` singkatan dari `"else if"`, digunakan untuk mengevaluasi beberapa kondisi secara berurutan. Jika kondisi dalam `if` tidak terpenuhi, Python akan memeriksa kondisi dalam setiap `elif` hingga menemukan yang benar atau sampai semua kondisi diperiksa.

# Hasil kode pemrograman Ticket Bioskop 
```
python
# Fungsi untuk menghitung harga tiket
def hitung_harga_tiket(tipe_tiket, status_member):
    # Harga tiket reguler dan VIP
    harga_reguler = 50000
    harga_vip = 100000

    # Menentukan harga berdasarkan tipe tiket
    if tipe_tiket.lower() == 'reguler':
        harga_tiket = harga_reguler
    elif tipe_tiket.lower() == 'vip':
        harga_tiket = harga_vip
    else:
        print("Tipe tiket tidak valid. Silakan masukkan 'reguler' atau 'vip'.")
        return None

    # Menghitung diskon jika pengguna adalah member
    if status_member.lower() == 'ya':
        diskon = 0.2 * harga_tiket
        total_harga = harga_tiket - diskon
    elif status_member.lower() == 'tidak':
        total_harga = harga_tiket
    else:
        print("Status member tidak valid. Silakan masukkan 'ya' atau 'tidak'.")
        return None

    return total_harga

# Meminta input dari pengguna
tipe_tiket = input("Masukkan tipe tiket (reguler/vip): ")
status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ")

# Menghitung total harga
total_harga = hitung_harga_tiket(tipe_tiket, status_member)

# Menampilkan hasil jika valid
if total_harga is not None:
    print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")

```

#Penjelasan Terkait Kode Pemrograman Ticket Bioskop

# 1.Definisi Fungsi
```
python
def hitung_harga_tiket(tipe_tiket, status_member):
```
Fungsi `hitung_harga_ticket`didefinisikan menghitung total harga tiket
Menentukan tipe tiket `VIP/REGULER`
Menentukan status member (`apakah member atau tidak`)

# 2.Harga tiket
```
python
harga_reguler = 50000
harga_vip = 100000
```
Dua variabel ini ditentukan untuk menyimpan harga tiket reguler atau VIP

# 3.Menentukan harga berdasarkan tipe tiket
```
python
if tipe_tiket.lower() == 'reguler':
    harga_tiket = harga_reguler
elif tipe_tiket.lower() == 'vip':
    harga_tiket = harga_vip
else:
    print("Tipe tiket tidak valid. Silakan masukkan 'reguler' atau 'vip'.")
    return None
```
Kondisi: Menggunakan pernyataan `if` untuk memeriksa tipe tiket yang dimasukkan.
Jika pengguna memasukkan `reguler`, maka `harga_tiket` diatur ke `harga_reguler`.
Jika pengguna memasukkan `vip`, maka `harga_tiket` diatur ke `harga_vip`.
Jika tidak valid, program akan mencetak pesan kesalahan dan mengembalikan `None`

# 4.Menghitung Diskon Untuk Member
```
python
if status_member.lower() == 'ya':
    diskon = 0.2 * harga_tiket
    total_harga = harga_tiket - diskon
elif status_member.lower() == 'tidak':
    total_harga = harga_tiket
else:
    print("Status member tidak valid. Silakan masukkan 'ya' atau 'tidak'.")
    return None
```
Kondisi:Memeriksa status keanggotaan.
Jika pengguna adalah member (`ya`), diskon sebesar 20% dari `harga_tiket` dihitung dan dikurangi dari harga tiket untuk mendapatkan `total_harga`.
Jika bukan member (`tidak`), maka `total_harga` sama dengan `harga_tiket`.
Jika status member tidak valid, program akan mencetak pesan kesalahan dan mengembalikan `None`.

# 5.return total_harga
```
python
return total_harga
```
Fungsi mengembalikan nilai `total_harga`, yang merupakan jumlah yang harus dibayar oleh pengguna.

# 6.Meminta input dari pengguna
```
python
tipe_tiket = input("Masukkan tipe tiket (reguler/vip): ")
status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ")
```
Program meminta pengguna untuk memasukkan tipe tiket dan status keanggotaan.

# 7.Menghitung Total Harga
```
python
total_harga = hitung_harga_tiket(tipe_tiket, status_member)
```
Memanggil fungsi `hitung_harga_tiket` dengan `parameter` yang diberikan oleh pengguna dan menyimpan hasilnya dalam `variabel total_harga`

#8.Menampilkan Hasil
```
python
if total_harga is not None:
    print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")
```
Jika `total_harga` tidak bernilai `None`, program mencetak total harga yang harus dibayar dengan format dua desimal.

# HASIL DARI KODE PEMROGRAMAN TIKET BIOSKOP
![Foto](https://github.com/nanafnan09/flowchart-kalkulator-tiket/blob/cb4b9ab4afa91b5f5e5652395e2285a302984cca/Coding%20Ticket.png)

# Flowchart Tiket Bioskop
![Foto](https://github.com/nanafnan09/flowchart-kalkulator-tiket/blob/b929e9a616af93d79512daa4cda628641e21a634/flowchart%20tiket.png)

Penjelasan Terkait Flowchart Diatas:
1.Start:Proses Dimulai
2.Input tipe tiket: Pengguna memasukkan tipe tiket yang ingin dibeli, yang bisa berupa `Reguler` atau `VIP`.
3.Input status member: Pengguna juga diminta untuk memasukkan status keanggotaan, apakah `YA` (member) atau `TIDAK` (bukan member).
Apakah Tiket Reguler?
Jika YA:Harga tiket ditetapkan sebesar `50,000`
Jika TIDAK:Harga tiket ditetapkan sebesar `100,000`

Apakah status member = YA?
Jika YA: Diskon sebesar 20% diberikan (diskon = 0.2).
Jika TIDAK: Tidak ada diskon (diskon = 0).
Perhitungan Total Harga: Total harga dihitung dengan rumus:
`Total Harga=Harga Tiket×(1−Diskon)`
Output total harga: Menampilkan hasil akhir total harga tiket yang harus dibayar oleh pengguna.
Selesai:Proses Selesai

# Kode Pemrograman Kalkulator Sederhana
```
Python
# Fungsi untuk melakukan operasi aritmatika
def kalkulator(angka1, angka2, operator):
    if operator == '+':
        return angka1 + angka2
    elif operator == '-':
        return angka1 - angka2
    elif operator == '*':
        return angka1 * angka2
    elif operator == '/':
        if angka2 != 0:
            return angka1 / angka2
        else:
            return "Error: Pembagian dengan nol tidak diperbolehkan."
    else:
        return "Error: Operator tidak valid. Gunakan +, -, *, atau /."

# Meminta input dari pengguna
try:
    angka1 = float(input("Masukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    operator = input("Masukkan operator (+, -, *, /): ")

    # Menghitung hasil
    hasil = kalkulator(angka1, angka2, operator)

    # Menampilkan hasil
    print(f"Hasil: {hasil}")

except ValueError:
    print("Error: Masukkan angka yang valid.")
```
# Penjelasan Terkait Kode Pemrograman Diatas
# 1. Fungsi Kalkulator
```
python
def kalkulator(angka1, angka2, operator):
```
Fungsi `kalkulator` didefinisikan dengan tiga parameter: `angka1`, `angka2`, dan `operator`. Fungsi ini akan mengembalikan hasil dari operasi aritmatika berdasarkan operator yang
diberikan.

# Operasi Aritmatika
# Penjumlahan (`+`):
```
python
if operator == '+':
    return angka1 + angka2
```
Jika operator adalah `+`, maka fungsi akan mengembalikan hasil penjumlahan `angka1` dan `angka2`.

# Pengurangan(`-`):
```
python
elif operator == '-':
    return angka1 - angka2
```
Jika operator adalah `-`, maka fungsi akan mengembalikan hasil pengurangan.

# Perkalian (`*`):
```
python
elif operator == '*':
    return angka1 * angka2
```
Jika operator adalah `*`, maka fungsi akan mengembalikan hasil perkalian.

# Pembagian (`/`):
```
python
elif operator == '/':
    if angka2 != 0:
        return angka1 / angka2
    else:
        return "Error: Pembagian dengan nol tidak diperbolehkan."
```
Jika operator adalah `/`, fungsi akan memeriksa apakah angka2 tidak sama dengan nol. Jika tidak, maka akan mengembalikan hasil pembagian; jika ya, akan mengembalikan pesan kesalahan.

# Operator Tidak Valid:
```
python
else:
    return "Error: Operator tidak valid. Gunakan +, -, *, atau /."
```
Jika operator yang dimasukkan tidak valid, fungsi akan mengembalikan pesan kesalahan.

# Input dari Pengguna
```
python
try:
    angka1 = float(input("Masukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    operator = input("Masukkan operator (+, -, *, /): ")
```
Bagian ini meminta pengguna untuk memasukkan dua angka dan satu operator. Fungsi `input()` digunakan untuk mengambil input dari pengguna, dan `float()` digunakan untuk mengonversi input menjadi tipe data float.

# Menghitung dan Menampilkan Hasil
```
python
hasil = kalkulator(angka1, angka2, operator)
print(f"Hasil: {hasil}")
```
Setelah mendapatkan input dari pengguna, program memanggil fungsi `kalkulator` dengan argumen yang telah dimasukkan oleh pengguna. Hasilnya kemudian ditampilkan di layar.

# Penanganan Kesalahan
```
python
except ValueError:
    print("Error: Masukkan angka yang valid.")
```
Bagian ini menangani kesalahan jika pengguna memasukkan nilai yang tidak dapat dikonversi menjadi float (misalnya huruf atau karakter non-numerik). Jika terjadi kesalahan, program akan menampilkan pesan kesalahan yang sesuai.

# Hasil Dari Kode Pemrograman (`+`)
![Foto](https://github.com/nanafnan09/flowchart-kalkulator-tiket/blob/b929e9a616af93d79512daa4cda628641e21a634/Codingan%20(%2B).png)

# Hasil Dari Kode Pemrograman (`-`)
![Foto](https://github.com/nanafnan09/flowchart-kalkulator-tiket/blob/b929e9a616af93d79512daa4cda628641e21a634/Codingan%20(-).png)
