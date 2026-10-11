# Singly Linked List (Modul 4)

Praktikum Struktur Data Modul 4 mengenai implementasi Abstract Data Type (ADT) Singly Linked List menggunakan bahasa C++. Elemen di dalam list menyimpan data bertipe `int` yang saling terhubung menggunakan pointer `next`.

## Struktur File

| File | Penjelasan |
| :--- | :--- |
| `Singlylist.h` | Berisi deklarasi tipe (`infotype`, `address`, `ElmList`, `List`) dan prototype semua fungsi/prosedur. |
| `Singlylist.cpp` | Tempat implementasi atau isi dari semua fungsi dan prosedur yang sudah dideklarasikan. |
| `main.cpp` | Program utama untuk menjalankan dan menguji seluruh operasi linked list. |

## Daftar Operasi

| Operasi | Fungsi | Keterangan |
| :--- | :--- | :--- |
| Create | `CreateList(L)` | Membuat list baru yang masih kosong (`First = Nil`). |
| Alokasi | `alokasi(x)` | Membuat elemen baru dengan nilai `x`. |
| Dealokasi | `dealokasi(P)` | Menghapus dan membersihkan memori elemen `P`. |
| Insert | `insertFirst(L, P)` | Menambahkan elemen `P` di posisi paling depan list. |
| View | `printInfo(L)` | Menampilkan semua isi data yang ada di dalam list. |
| Search | `findElm(L, x)` | Mencari elemen berdasarkan nilai `x`, mengembalikan alamatnya atau `Nil` jika tidak ketemu. |
| Delete | `delFirst(L, P)` | Melepas elemen pertama dari list, alamatnya disimpan di `P`. |
| Delete | `delLast(L, P)` | Melepas elemen terakhir dari list, alamatnya disimpan di `P`. |
| Delete | `delAfter(L, P, Prec)` | Melepas elemen setelah `Prec`, alamatnya disimpan di `P`. |
| Delete | `delAll(L)` | Menghapus seluruh elemen yang ada di list sekaligus. |
| Update | `updateElm(L, lama, baru)` | Mengubah nilai elemen dari `lama` menjadi `baru` (dicari pakai `findElm`). |

*Catatan:* Fungsi `delFirst`, `delLast`, dan `delAfter` sifatnya hanya melepas kaitan elemen dari list. Jangan lupa panggil `dealokasi(P)` setelahnya agar memori komputer bersih.

## Cara Compile & Run

### Lewat Terminal (g++)
```bash
g++ main.cpp Singlylist.cpp -o singlylist
./singlylist
