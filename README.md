# Praktikum 6 - Sistem Manajemen Data Mahasiswa
Nama: Ica Rizqiah

Nim: 312410554

Mata Kuliah : Bahasa Pemrograman

## Penjelasan code program Sistem Manajemen Data Mahasiswa

Program ini adalah sistem sederhana untuk mengelola data mahasiswa yang mencakup nama dan nilai.

Data mahasiswa disimpan dalam bentuk list yang berisi dictionary.

Program ini menyediakan beberapa fungsi untuk menambah, menampilkan, menghapus, dan mengubah data mahasiswa.

### 1. Variabel Global mahasiswa


```python
mahasiswa = []
```

Penjelasan: Variabel ini adalah list kosong yang digunakan untuk menyimpan data mahasiswa. Setiap data mahasiswa disimpan dalam bentuk dictionary dengan format:

```python
    {'nama': 'Nama Mahasiswa', 'nilai': Nilai Mahasiswa}
```

### 2. Fungsi `tambah(nama, nilai)`

```python
def tambah(nama, nilai):
    mahasiswa.append({'nama': nama, 'nilai': nilai})
    print(f"Data mahasiswa '{nama}' berhasil ditambahkan.")
```

Penjelasan: Fungsi ini digunakan untuk menambahkan data mahasiswa ke dalam list `mahasiswa.`

Parameter:

`nama`: Nama mahasiswa yang akan ditambahkan (string).

`nilai`: Nilai mahasiswa yang akan ditambahkan (integer atau float).

Proses:

Membuat dictionary baru berisi `nama dan nilai`.

Menambahkan dictionary tersebut ke dalam list `mahasiswa`.

Menampilkan pesan bahwa data berhasil ditambahkan.

### 3. Fungsi `tampilkan()`

```python
def tampilkan():
    if not mahasiswa:
        print("Tidak ada data mahasiswa.")
        return
    print("\nDaftar Nilai Mahasiswa:")
    for index, mhs in enumerate(mahasiswa, start=1):
        print(f"{index}. Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")
```

Penjelasan: Fungsi ini digunakan untuk menampilkan semua data mahasiswa yang ada di list `mahasiswa.`

Proses:

Mengecek apakah list `mahasiswa` kosong. Jika kosong, menampilkan pesan "Tidak ada data mahasiswa."

Jika tidak kosong, menampilkan data mahasiswa dengan format:

-Nomor urut.

-Nama mahasiswa.

-Nilai mahasiswa.

### 4. Fungsi `hapus(nama)`

```python
def hapus(nama):
    global mahasiswa
    for mhs in mahasiswa:
        if mhs['nama'] == nama:
            mahasiswa.remove(mhs)
            print(f"Data mahasiswa '{nama}' berhasil dihapus.")
            return
    print(f"Data mahasiswa dengan nama '{nama}' tidak ditemukan.")
```

Penjelasan: Fungsi ini digunakan untuk menghapus data mahasiswa berdasarkan nama.

Parameter:

`nama`: Nama mahasiswa yang ingin dihapus (string).

Proses:

Mencari mahasiswa dengan nama yang sesuai di dalam list `mahasiswa.`

Jika ditemukan, menghapus data tersebut menggunakan metode `.remove().`

Menampilkan pesan bahwa data berhasil dihapus.

Jika tidak ditemukan, menampilkan pesan bahwa nama tidak ditemukan.

### 5. Fungsi `ubah(nama, nilai_baru)`

```python
def ubah(nama, nilai_baru):
    for mhs in mahasiswa:
        if mhs['nama'] == nama:
            mhs['nilai'] = nilai_baru
            print(f"Data mahasiswa '{nama}' berhasil diubah menjadi nilai {nilai_baru}.")
            return
    print(f"Data mahasiswa dengan nama '{nama}' tidak ditemukan.")
```

Penjelasan: Fungsi ini digunakan untuk mengubah nilai mahasiswa berdasarkan nama.

Parameter:

`nama`: Nama mahasiswa yang nilainya ingin diubah (string).

`nilai_baru`: Nilai baru untuk mahasiswa tersebut (integer atau float).

Proses:

Mencari mahasiswa dengan nama yang sesuai di dalam list `mahasiswa.`

Jika ditemukan, mengganti nilai mahasiswa dengan `nilai_baru.`

Menampilkan pesan bahwa data berhasil diubah.

Jika tidak ditemukan, menampilkan pesan bahwa nama tidak ditemukan.

### 6. Program Utama

```python
while True:
    print("\nMenu:")
    print("1. Tambah Data Mahasiswa")
    print("2. Tampilkan Data Mahasiswa")
    print("3. Hapus Data Mahasiswa")
    print("4. Ubah Data Mahasiswa")
    print("5. Keluar")
    
    pilihan = input("Pilih menu (1-5): ")
    
    if pilihan == '1':
        nama = input("Masukkan nama mahasiswa: ")
        nilai = float(input("Masukkan nilai mahasiswa: "))
        tambah(nama, nilai)
    elif pilihan == '2':
        tampilkan()
    elif pilihan == '3':
        nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
        hapus(nama)
    elif pilihan == '4':
        nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
        nilai_baru = float(input("Masukkan nilai baru: "))
        ubah(nama, nilai_baru)
    elif pilihan == '5':
        print("Keluar dari program.")
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
```

Penjelasan: Program utama menyediakan antarmuka menu sederhana untuk pengguna.

Proses:

1. Menampilkan daftar menu:
   
-Tambah data mahasiswa.

-Tampilkan data mahasiswa.

-Hapus data mahasiswa.

-Ubah data mahasiswa.

-Keluar dari program.

2. Meminta input dari pengguna untuk memilih salah satu menu (1-5).
   
3. Berdasarkan pilihan:
 
-Memanggil fungsi `tambah()` jika memilih 1.

-Memanggil fungsi `tampilkan()` jika memilih 2.

-Memanggil fungsi `hapus()` jika memilih 3.

-Memanggil fungsi `ubah()` jika memilih 4.

-Mengakhiri program jika memilih 5.

-Menampilkan pesan kesalahan jika pilihan tidak valid.

## Flowchart penggunaan program

![foto](https://github.com/keeyyaaa/labpy06/blob/4b766e93c50374444586727aa5aa4b4048ac7dd1/labpy%2006%20fc.png)

## Hasil code program

![foto](https://github.com/keeyyaaa/labpy06/blob/d8a0b96f086203096745da5832a5aaf214b2679c/code%20labpy06.png)

![foto]()
