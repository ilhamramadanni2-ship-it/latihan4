# Singly Linked List (Modul 4)[cite: 21]

Implementasi ADT Singly Linked List dalam C++ untuk praktikum Struktur Data, Modul 4 (Singly Linked List Bagian Pertama). Elemen list menyimpan data bertipe `int` dan dihubungkan dengan pointer `next`[cite: 21].

## Struktur File[cite: 21]

| File | Isi |
| :--- | :--- |
| `Singlylist.h`[cite: 21] | Deklarasi tipe (`infotype`, `address`, `ElmList`, `List`) dan prototype semua primitif[cite: 21] |
| `Singlylist.cpp`[cite: 21] | Implementasi semua primitif[cite: 21] |
| `main.cpp`[cite: 21] | Program uji untuk mencoba semua operasi[cite: 21] |

## Operasi yang Tersedia[cite: 21, 22]

| Operasi | Fungsi | Keterangan |
| :--- | :--- | :--- |
| Create[cite: 21, 22] | `CreateList(L)`[cite: 21, 22] | Membuat list kosong (`First = Nil`)[cite: 21, 22] |
| Alokasi[cite: 21, 22] | `alokasi(x)`[cite: 21, 22] | Membuat elemen baru dengan info `x`[cite: 21, 22] |
| Dealokasi[cite: 21, 22] | `dealokasi(P)`[cite: 21, 22] | Membebaskan memori elemen `P`[cite: 21, 22] |
| Insert[cite: 21, 22] | `insertFirst(L, P)`[cite: 21, 22] | Menyisipkan elemen `P` di awal list[cite: 21, 22] |
| View[cite: 21, 22] | `printInfo(L)`[cite: 21, 22] | Menampilkan semua info dalam list[cite: 21, 22] |
| Search[cite: 21, 22] | `findElm(L, x)`[cite: 21, 22] | Mengembalikan address elemen dengan info `x`, atau `Nil` jika tidak ada[cite: 21, 22] |
| Delete[cite: 22] | `delFirst(L, P)`[cite: 22] | Melepas elemen pertama, address-nya disimpan di `P`[cite: 22] |
| Delete[cite: 22] | `delLast(L, P)`[cite: 22] | Melepas elemen terakhir, address-nya disimpan di `P`[cite: 22] |
| Delete[cite: 22] | `delAfter(L, P, Prec)`[cite: 22] | Melepas elemen setelah `Prec`, address-nya disimpan di `P`[cite: 22] |
| Delete[cite: 22] | `delAll(L)`[cite: 22] | Menghapus dan mendealokasi seluruh elemen[cite: 22] |
| Update[cite: 22] | `updateElm(L, lama, baru)`[cite: 22] | Mengganti info `lama` menjadi `baru` (mencari dengan `findElm`)[cite: 22] |

`delFirst`, `delLast`, dan `delAfter` hanya melepas elemen dari list. Panggil `dealokasi(P)` sesudahnya untuk membebaskan memori[cite: 22].

## Cara Compile dan Run[cite: 23]

### Command line (g++)[cite: 23]
```bash
g++ main.cpp Singlylist.cpp -o singlylist
./singlylist
```[cite: 23]

Di Windows, jalankan dengan `singlylist.exe`[cite: 23].

### Code::Blocks[cite: 23, 24]
1. Buat project baru: File > New > Project > Console application > C++[cite: 24].
2. Tambahkan `Singlylist.h`, `Singlylist.cpp`, dan `main.cpp` ke project[cite: 24].
3. Pastikan opsi "all in build target" tercentang untuk setiap file[cite: 24].
4. Build and Run dengan `F9`[cite: 24].

## Contoh Output[cite: 24]

```text
List awal     : 9 12 8 0 2
Setelah delFirst : 12 8 0 2
Setelah delLast  : 12 8 0
Setelah delAfter (setelah 12): 12 0
Setelah update 0 -> 5 : 12 5
Setelah delAll   : (list kosong)
```[cite: 24]

List awal berurutan `9 12 8 0 2` karena `insertFirst` selalu menaruh elemen baru di depan, sehingga elemen yang dimasukkan terakhir menjadi elemen pertama[cite: 24].

## Catatan[cite: 24]
* `delLast` menangani kasus khusus saat list hanya berisi satu elemen[cite: 24].
* `delAfter` mengembalikan `Nil` pada `P` jika `Prec` bernilai `Nil` atau tidak ada elemen setelahnya[cite: 24].
* `updateElm` menampilkan pesan jika elemen yang dicari tidak ditemukan[cite: 24].
