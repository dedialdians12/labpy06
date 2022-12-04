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

```
    if t.lower() == 't':
        print("Tambah Data")
        nama = input("Nama\t\t: ")
        nim = int(input("NIM\t\t\t: "))
        uts = int(input("Nilai UTS\t: "))
        uas = int(input("Nilai UAS\t: "))
        tugas = int(input("Nilai Tugas\t: "))
        akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
        a [nama] = nim, uts, uas, tugas, akhir
```

4. Melihat Data

Apabila kita menginput L maka sistem akan menampilkan data yang sudah kita masukkan. Jika kita belum memasukkan data maka outputnya menjadi TIDAK ADA DATA.
Data dalam perulangan for di ambil dari variabel Dictionary a pada bagian value yang berbntuk list. variabel i = 0 digunakan untuk membuat nomer.

```
    elif t.lower() == 'l':
        if a.items():
            print("="*78)
            print("|                            Daftar Nilai Mahasiswa                          |")
            print("="*78)
            i = 0
            for z in a.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
                print("="*78)
        else:
            print("="*78)
            print("|                        Daftar Nilai Mahasiswa                           |")
            print("="*78)
            print("|                         TIDAK ADA DATA !!!                              |")
            print("="*78)
```

5. Mengubah Data

Apabila kita menginput U maka akan ada keterangan untuk mengubah data dan kita akan diminta untuk menginputkan nama yang mau diubah datanya, apabila nama tidak ada maka outputnya Nama {} tidak ditemukan. Dimana {} adalah nama/data yang mau kita ubah.

```
    elif t.lower() == 'u':
        print("Ubah Data")
        nama = input("\tMasukkan Nama\t\t: ")
        if nama in a.keys():
            nim = int(input("\tNIM\t\t\t: "))
            uts = int(input("\tNilai UTS\t\t\t: "))
            uas = int(input("\tNilai UAS\t\t\t: "))
            tugas = int(input("\tNilai Tugas\t\t\t: "))
            akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
            a[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))
```

6. Menghapus Data

Apabila kita menginput H maka kita akan diminta menginput nama yang akan dihapus. Jika nama ada di dalam dictionary, maka system akan menghapus keys/nama tersebut beserta valuesnya pada statement del a[nama].

```
    elif t.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama : ")
        if nama in a.keys():
            del a[nama]
        else:
             print("Nama {0} Tidak Ditemukan".format(nama))
```

7. Mencari Data

Apabila kita menginputkan C maka kita akan diminta untuk memasukkan nama yang akan dicari. Apabila nama yang dicari ada di dalam dictionary maka outputnya akan menampilkan data dari nama tersebut.

