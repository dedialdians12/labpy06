Nama      : Dedi Aldiansyah
Nim       : 312210452
Kelas     : TI22B2

Tugas Praktikum 6

Membuat tampilan program sederhana dengan menyertakan beberapa fungsi yg menampilkan daftar nilai mahasiswa dengan fungsi sebagai berikut :

1. (T) untuk menambahkan data pada program
2. (L) menampilkan data pada program
3. (U) mengubah data berdasarkan nama pada program 
4. (H) menghapus data berdasarkan nama pada program
5. (C) mencari data berdasarkan nama pada program
6. (K) keluar program

1. Membuat dictionary

  Pertama membuat dictonary kosong dengan syntax a = {} . Fungsinya untuk menginput data dalam program tersebut dan memudahkan kita untuk memanggil data kembali.
2. Membuat Perulangan
Selanjutnya membuat kondisi perulangan menggunakan while True. Artinya ketika kita menginputkan data berdasarkan syntax maka jawabannya benar jika tidak maka akan break. Untuk menginisialkan penambahan menu pilihan Tambah, Lihat, Ubah, Hapus, Cari, dan Keluar menggunakan source code sebagai berikut :

```
while True:
    t = input("\n(T)ambah, (L)ihat, (U)bah, (H)apus, (C)ari, (K)eluar : ")
```

3. Menambahkan Data
Disini apabila kita menginputkan T maka kita akan diminta untuk menginputkan beberapa data. Data yang kita inputkan akan masuk ke dictionary a yang telah dibuat tadi dengan data nama sebagai keys dan sisanya sebagai values.
