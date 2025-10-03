# <h1 align="center">Laporan Praktikum Modul 2 <br> Pengenalan C++ Bagian 2 </h1>
<p align="center">Atha Muyassar - 103112430185</p>

## Dasar Teori

Bahasa C++ adalah bahasa tingkat tinggi yang di kembangkan dari bahasa C. C++ terdiri atas preprocessor directive seperti #include <iostream> untuk memanggil pustaka dan fungsi main() sebagai titik awal eksekusi program. C++ juga menyediakan beberapa tipe data seperti int, char, float, double, string, dan bool. untuk input dan output C++ menggunakan cin(input) dan cout(output) yang dimana perlu menggunakan operator >> untuk membaca data dan << untuk menmpilkan data. Ada juga struktur kontrol seperti if, if-else, switch-case, for, while, dan do-while. ada juga kontrol alur khusus seperti break dan continue.

## Guided

### soal 1 ()

```go

```
>Output
>![output](output/gu_1.jpg)

### soal 2 ()

```go

```
>Output
>![output](output/gu_2.jpg)

### soal 3 ()

```go

```
>Output
>![output](output/gu_3.jpg)

### soal 4 ()

```go

```
>Output
>![output](output/gu_4.jpg)

### soal 5 (fungsi)

```go

```
>Output
>![output](output/gu_5.jpg)

### soal 6 ()

```go

```
>Output
>![output](output/gu_6.jpg)

## Unguided

### Soal 1
Buatlah sebuah program untuk melakukan transpose pada sebuah matriks persegi berukuran 3x3. Operasi transpose adalah mengubah baris menjadi kolom dan sebaliknya. Inisialisasi matriks awal di dalam kode, kemudian buat logika untuk melakukan transpose dan simpan hasilnya ke dalam matriks baru. Terakhir, tampilkan matriks awal dan matriks hasil transpose.
Contoh Output:
>![soal](output/ngu!.jpg)

```go

```

> Output
> ![Screenshot bagian x](output/2.jpg)

### Soal 2
Buatlah program yang menunjukkan penggunaan call by reference. Buat sebuah prosedur bernama kuadratkan yang menerima satu parameter integer secara referensi (&). Prosedur ini akan mengubah nilai asli variabel yang dilewatkan dengan nilai kuadratnya. Tampilkan nilai variabel di main() sebelum dan sesudah memanggil prosedur untuk membuktikan perubahannya. 
Contoh Output:
Nilai awal: 5
Nilai setelah dikuadratkan: 25
```go
#include <iostream>
using namespace std;

void kuadratkan(int &n) {
    n = n * n;
}

int main() {
    int nilai;
    cout << "masukan angka: ";
    cin >> nilai;
    cout << "ini angka " << nilai << endl;
    kuadratkan(nilai);
    cout << "setelah dikuadratkan hasilnya menjadi " << nilai << endl;
    return 0;
}
```

> Output
> ![output](output/image.png)

## Referensi

1. https://www.w3schools.com/cpp/default.asp
2. https://www.belajarcpp.com/tutorial/cpp/
3. https://www.petanikode.com/cpp-windows/
4. https://youtube.com/playlist?list=PLZS-MHyEIRo4Ze0bbGB1WKBSNMPzi-eWI&si=1oSxwc95gRfbVdbu
5. 
