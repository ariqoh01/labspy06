# labspy06
### Profil
__Nama  : Ariqoh Zulaika Zuhrah__

__Nim   : 312110138__

__Kelas : T1.21.A.1__
## latihan 
- Ubahlah kode dibawah ini menjadi fungsi menggunakan *lambda*

### Input
![Gambar1](Ss/input.PNG)

```py
import math
def a(x):
    return x**2

def b(x, y)
    return math.sqrt(x**2 + y**2)  

def c(*args):
    return sum(args)/len(args)

def d(s):
    return "".join(set(s))
```

### Penjelasan
- Untuk memperluas daftar fungsi matematika gunakan `import math`

- Fungsi lambda yang menggunakan variabel a-d
```py
def a(x):
    return x**2
    a = lambda x : x ** 2
print(a(2))

def b(x, y):
    return math.sqrt(x**2 + y**2)
    b = lambda x, y : x ** 2  + y ** 2
print(b(2, 2))

def c(*args):
    return sum(args)/len(args)
    c = lambda *args : sum(args)/len(args)
print(c(5, -6, 7, 8))

def d(s):
    return "".join(set(s))
    d = lambda s: "".join(set(s))
print(d("Ariqoh"))
```

### Output
![Gambar2](Ss/output.PNG)

## TUGAS PRAKTIKUM
Buat program sederhana dengan mengaplikasikan penggunaan fungsi
yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:<p>
• Fungsi tambah() untuk menambah data<p>
• Fungsi tapilkan() untuk menampilkan data<p>
• Fungsi hapus(nama) untuk menghapus data berdasarkan nama<p>
• Fungsi ubah(nama) untuk mengubah data berdasarkan nama<p>
• Buat flowchart dan penjelasan programnya pada README.md. • Commit dan push repository ke github<p>
Berikut adalah program nya:<P>

    x = {}
    
    while True:
        header="PROGRAM INPUT NILAI MAHASISWA"
        header2=("MENU UTAMA")
        print(header.center(97,"="))
        print()
        print(header2.center(97,"_"))
        c = input("\n(M)Menampilkan, (T)ambah, (U)bah), (H)apus, (C)ari, (K)eluar: ")
    
        if c.lower() == 't':
            print("Tambah Data")
            nama = input("Nama\t\t: ")
            nim = int(input("NIM\t\t\t: "))
            uts = int(input("Nilai UTS\t: "))
            uas = int(input("Nilai UAS\t: "))
            tugas = int(input("Nilai Tugas\t: "))
            akhir = tugas*30/100 + uts*35/100 + uas*35/100
            x[nama] = nim, uts, uas, tugas, akhir
    
        elif c.lower() == 'u':
            print("Ubah Data")
            nama = input("\tMasukkan Nama\t\t: ")
            if nama in x.keys():
                nim     = int(input("\tNIM      \t\t\t: "))
                uts     = int(input("\tNilai UTS\t\t\t: "))
                uas     = int(input("\tNilai UAS\t\t\t: "))
                tugas   = int(input("\tNilai Tugas\t\t\t: "))
                akhir   = tugas*30/100 + uts*35/100 + uas*35/100
                x[nama] = nim, uts, uas, tugas, akhir
            else:
                print("Nama {0} tidak ditemukan".format(nama))
    
        elif c.lower() == 'h':
            print("Hapus Data")
            nama = input("Masukkan Nama  : ")
            if nama in x.keys():
                del x[nama]
            else:
                print("Nama {0} Tidak Ditemukan".format(nama))
    
        elif c.lower() == 'c':
            print("Cari Data[case-sensitive]")
            nama = input("Masukkan Nama : ")
            if nama in x.keys():
                print("="*73)
                print("|                             Daftar Mahasiswa                          |")
                print("="*73)
                print("| Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
                print("="*73)
                print("| {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(nama, nim, uts, uas, tugas, akhir))
                print("="*73)
            else:
                print("Nama {0} Tidak Ditemukan".format(nama))
    
        elif c.lower() == 'm':
            if x.items():
                print("="*78)
                print("|                               Daftar Mahasiswa                             |")
                print("="*78)
                print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
                print("="*78)
                i = 0
                for z in x.items():
                    i += 1
                    print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                          .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
                print("=" * 78)
            else:
                print("="*78)
                print("|                               Daftar Mahasiswa                             |")
                print("="*78)
                print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
                print("="*78)
                print("|                                TIDAK ADA DATA                              |")
                print("="*78)
    
        elif c. lower() == 'k':
            break
    
        else:
            print("Pilih menu yang tersedia")

Berikut Untuk output Tambah Data:<P>
![Gambar3](Ss/1.PNG)
Syntax untuk menambahkan data sebagai berikut:<P>

        if c.lower() == 't':
        print("Tambah Data")
        nama = input("Nama\t\t: ")
        nim = int(input("NIM\t\t\t: "))
        uts = int(input("Nilai UTS\t: "))
        uas = int(input("Nilai UAS\t: "))
        tugas = int(input("Nilai Tugas\t: "))
        akhir = tugas*30/100 + uts*35/100 + uas*35/100
        x[nama] = nim, uts, uas, tugas, akhir
Berikut adalah Output untuk mengubah data dan menampilkan data yang sudah di ubah atau pun juga belum di ubah<P>
![Gambar4](Ss/2.PNG)
Dan berikut adalah syntax yang di masukan untuk ubah data dan tampilkan data<p>

        elif c.lower() == 'u':
        print("Ubah Data")
        nama = input("\tMasukkan Nama\t\t: ")
        if nama in x.keys():
            nim     = int(input("\tNIM      \t\t\t: "))
            uts     = int(input("\tNilai UTS\t\t\t: "))
            uas     = int(input("\tNilai UAS\t\t\t: "))
            tugas   = int(input("\tNilai Tugas\t\t\t: "))
            akhir   = tugas*30/100 + uts*35/100 + uas*35/100
            x[nama] = nim, uts, uas, tugas, akhir
        else:
            print("Nama {0} tidak ditemukan".format(nama))
dan syntax untuk menampilkan data<P>
    
        elif c.lower() == 'm':
        if x.items():
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            i = 0
            for z in x.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
            print("=" * 78)
Berikut juga saya cantumkan Flowchart nya dari program input data mahasiswa<P>
![Gambar5](Ss/3.png)
Untuk menu menu yang lain nya sperti hapus,cari atau keluar kalian bisa mencoba nya program sudah di sediakan<P>
Itu saja yang bisa saya jelaskan Terimakasih Wassalamualaikum wr wb.<P>