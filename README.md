# Fungsi dan Fungsi Rekursif

## Daftar Isi

- Fungsi
    + Pengenalan Fungsi
    + Tujuan Fungsi
    + Pendefinisan Fungsi
    + Prototipe Fungsi
    + Parameter Fungsi
    + Pemanggilan Fungsi
    + Nilai _return_ Fungsi
- Fungsi Rekursif
    + Pengenalan Fungsi Rekursif
    + Base Case
    + Recursive Case

# Fungsi

## Pengenalan Fungsi

**Fungsi** adalah sebuah kumpulan statement untuk melakukan tugas spesifik (tugas tertentu), yang bisa membutuhkan input ataupun tidak, untuk menghasilkan output yang sesuai.

Secara umum, fungsi dibedakan menjadi dua, yakni Fungsi Standar Library dan Fungsi yang dibuat pengguna. Fungsi Standar Library adalah fungsi bawaan yang telah disertakan dalam library standar, missal fungsi `printf()`, `scanf()` yang ada di dalam library `<stdio.h>`. Sedangkan Fungsi yang dibuat oleh pengguna adalah fungsi yang sengaja dibuat oleh pengguna.

## Tujuan Fungsi

Tujuan dibuatnya fungsi secara umum adalah untuk membuat program menjadi lebih modular. Fungsi digunakan ketika ingin menjalankan serangkaian perintah secara berulang kali, terkadang dengan input yang berbeda, dengan tujuan tidak mengulang penulisan kode berkali-kali, serta apabila nantinya program mengalami bug, akan mempermudah proses perbaikan.

## Pendefinisian Fungsi

Sebelum fungsi dapat digunakan dan bisa dipanggil, perlu dilakukan pendefinisan terlebih dahulu. Pendefinisian ditujukan untuk mendefinisikan apa yang fungsi tersebut lakukan ketika fungsi tersebut dipanggil. Berikut adalah sintaks untuk melakukan pendefinisan fungsi.

```
<return_type> <nama_fungsi>(<parameter1>, <parameter2>, ...)
{
    statement;
    statement;
    ...
    ...
    ...
}
```
Berikut adalah contoh fungsi untuk mencetak string **"Aku Sebuah Fungsi."**.
```c
void cetak()
{
    printf("Aku Sebuah Fungsi\n");
}

int main()
{
    cetak();
    return 0;
}
```

## Prototipe Fungsi

Selain menggunakan pendefisian langsung seperti cara sebelumnya, fungsi juga dapat dibuat dengan prototipe. Prototipe Fungsi (atau biasa disebut Interface Fungsi) adalah deklarasi dari sebuah fungsi tanpa definisinya. Deklarasi sebuah fungsi berisi _return type_, nama fungsi, dan parameter yang terlibat.

Untuk menuliskan prototipe fungsi, sintaksnya sebagai berikut :
```
// Deklarasi
<return_type> <nama_fungsi>(<parameter1>, <parameter2>, ...);
```

Contoh kode program menggunakan prototipe fungsi.
```c
// Prototipe Fungsi
void cetak();

int main()
{
    cetak();
    return 0;
}

// Definisi Fungsi cetak()
void cetak()
{
    printf("Aku Sebuah Fungsi\n");
}
```

## Parameter Fungsi

Parameter pada fungsi bersifat layaknya input yang diberikan kepada sebuah fungsi. Jumlah parameter pada sebuah fungsi bisa dibuat sebanyak-banyaknya sesuai kebutuhan.

Penulisan parameter fungsi sama dengan pendefinisian variable dan tiap parameter dipisahkan oleh operator (`,`).

```
<tipe_data> <nama_parameter_1> , <tipe_data> <nama_parameter_2>, ...
```
Contoh
```c
void cetak(char str[])
{
    printf("%s\n", str);
}
```

## Pemanggilan Fungsi

Untuk memanggil fungsi, dilakukan dengan menulis nama fungsinya diikuti dengan tanda “`()`”. Pabila fungsi tersebut memiliki parameter maka didalam tanda “`()`” dituliskan nilai/variabel/objek untuk dijadikan yang kita sebut dengan argumen dan dipisahkan tiap argumen dengan operator “`,`”. Argumen-argumen yang dimasukkan harus sesuai dengan tipe data parameter fungsinya.

Contoh pemanggilan fungsi.

```c
int main()
{
    cetak();
    tambahkan(2,5);
    cetak("Halo, dunia");
}
```

## Nilai _return_ Fungsi

# Fungsi Rekursif