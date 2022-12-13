# TUGAS PRATIKUM PERTEMUAN 12

#### Soal
- Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah
  class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan:
-  Method tambah() untuk menambah data
-  Method tampilkan() untuk menampilkan data
-  Method hapus(nama) untuk menghapus data berdasarkan nama
-  Method ubah(nama) untuk mengubah data berdasarkan nama

#### progam

``` print("=" * 65)
print("|\tPROGRAM INPUT NILAI MAHASISWA MENGGUNAKAN FUNGSI\t|")
print("=" * 65)

dataMahasiswa = {}
class mahasiswa(object):
    def tambah():
        nama = str(input("Masukan Nama : "))
        nim = int(input("Masukan Nim   : "))
        tugas = int(input("Masukan Nilai Tugas : "))
        uts = int(input("Masukan Nilai UTS     : "))
        uas = int(input("Masukan Nilai UAS     : "))
        akhir = (tugas / 3) + (uts / 3.5) + (uas / 3.5)
        dataMahasiswa[nama] = nim, tugas, uts, uas, akhir,
        print("DATA BERHASIL DI TAMBAHKAN!")

    def tampilkan():
        print("=" * 61)
        print("|" + "\t" * 2 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
              "    |")
        print("=" * 61)
        print("|   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
        print("=" * 61)
        for tampil in dataMahasiswa.items():
            print("| {0:15}   | {1:9} | {2:5} | {3:3} | {4:3} | {5:5} |".format(tampil[0], tampil[1][0], tampil[1][1],
                                                                                tampil[1][2], tampil[1][3],
                                                                                "%.2f" % float(tampil[1][4])))
            print("=" * 61)

    def hapus(nama):
        del dataMahasiswa[nama]
        print("DATA BERHASIL DI HAPUS!")

    def ubah(nama):
        if nama in dataMahasiswa.keys():
            nim = int(input("Masukan Nim  : "))
            tugas = int(input("Masukan Nilai Tugas : "))
            uts = int(input("Masukan Nilai UTS     : "))
            uas = int(input("Masukan Nilai UAS     : "))
            akhir = (tugas / 3) + (uts / 3.5) + (uas / 3.5)
            dataMahasiswa[nama] = nim, tugas, uts, uas, akhir
            print("DATA BERHASIL DI UBAH!")
        else:
            print("DATA TIDAK DI TEMUKAN!")


while True:
    data = input(
        "\n 1 - Tambah Data\t 2 - Tampilkan Data\t 3 - Hapus Data\t 4 - Ubah Data\t 5 - Keluar \n :"
        )
    if (data.lower() == '1'):
        mahasiswa.tambah()

    elif (data.lower() == '4'):
        nama = str(input("Masukan Nama : "))
        mahasiswa.ubah(nama)
    elif (data.lower() == '3'):
        nama = str(input("Masukan Nama : "))
        if nama in dataMahasiswa:
            mahasiswa.hapus(nama)
        else:
            print("DATA TIDAK DI TEMUKAN ".format(nama))
    elif (data.lower() == '2'):
        if dataMahasiswa.items():
            mahasiswa.tampilkan()
        else:
            print('\033[1m', '\33[34m')
            print("=" * 69)
            print("|" + "\t" * 3 + "DAFTAR NILAI MAHASISWA" + "\t" * 3 +
                  "    |")
            print("=" * 69)
            print("| NO |   \tNAMA\t   |\tNIM \t| TUGAS | UTS | UAS | AKHIR |")
            print("=" * 69)
            print("|    " + "\t" * 3 + "\33[31mTIDAK ADA DATA" + "\t" * 4 + "    |")
            print("=" * 69)
    elif (data.lower() == '5'):
        print("\nThanks You\n")
        exit()
    else:
        print("PILIHAN TIDAK TERSEDIA")
        ```
        
![Screenshot (78)](https://user-images.githubusercontent.com/115714443/207395634-671ec759-14d8-4727-ba86-b2246f3f61b6.png)
![Screenshot (79)](https://user-images.githubusercontent.com/115714443/207395670-f8c662be-76d4-423e-b654-a1732fd6158d.png)
![Screenshot (80)](https://user-images.githubusercontent.com/115714443/207395676-05c398c2-e752-40cf-98fb-44b2546623f4.png)
![Screenshot (81)](https://user-images.githubusercontent.com/115714443/207395707-5b295c43-0c34-479b-9721-ccf084e12fd7.png)
        

#### penjelasan
1. dekralarasi dataMahasasiwa sebagai object untuk menerima inputan data.
2. deklarasi class di isi dengan method:
- def tambah() di isi dengan inputan nama, nim, tugas, uts, uas, akhir , di variable akhir di isi dengan penjumlahan dan bagi 3, untuk tugas 3.5 untuk uts, 3.5 untuk   uas. terakhir masukan semua kedalam object dataMahasiswa.
- def tampil() untuk mencetak object dataMahasiwa serta gunakan perulangan for untuk mecetak semua data jika di dalam object dataMahasiwa berisi banyak data.
- def hapus(nama) untuk menghapus data di dalam parameter nama dan gunakan syntax del.
- def ubah(nama) untuk mengubah data di dalam parameter nama dan gunakan statment if else nama di dalam dataMahasiswa lalu masukan kembali ke dalam object dataMahasiswa.
3. gunakan pengulangan while True di isikan dengan inputan menu, lalu di dalamnya di isikan dengan statment if elif else.
4. di dalam statment if elif else di isikan dengan memanggil masing-masing method yang ada di dalam class mahasiswa.

#### Flowchart

![flowchart08](https://user-images.githubusercontent.com/115714443/207394441-dc08d462-1bcf-429f-8249-cc3c3602708f.png)

### Hasil Run

![Screenshot (76)](https://user-images.githubusercontent.com/115714443/207394917-78ee0fce-5ff4-4da3-a43b-04f58927e1da.png)
![Screenshot (77)](https://user-images.githubusercontent.com/115714443/207394954-bbc9fcd7-ebff-497b-b034-d2093126b853.png)

### TERIMAKASI
