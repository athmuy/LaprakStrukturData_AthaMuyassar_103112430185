# <h1 align="center">Laporan Praktikum Modul 2 <br> Pengenalan C++ Bagian 2 </h1>
<p align="center">Atha Muyassar - 103112430185</p>

## Dasar Teori

Array 2 dimensi adalah struktur data yang digunakan untuk menyimpan sekumpulan data dalam bentuk baris dan kolom sehingga menyerupai tabel atau matriks, di mana setiap elemennya diakses dengan indeks [baris][kolom] dan banyak digunakan untuk merepresentasikan data berbentuk grid, seperti matriks matematika, papan permainan, atau citra digital. Dalam pemanggilan fungsi, terdapat dua konsep penting yaitu call by pointer dan call by reference. Call by pointer adalah mekanisme di C/C++ di mana alamat memori suatu variabel dikirim ke fungsi menggunakan pointer sehingga fungsi dapat langsung mengubah nilai asli dari variabel tersebut dengan memanfaatkan operator * (dereferensi) dan & (alamat). Sementara itu, call by reference adalah mekanisme khusus di C++ yang mirip dengan call by pointer, tetapi lebih sederhana karena menggunakan tanda & pada parameter fungsi, sehingga variabel yang dikirim tidak disalin melainkan dirujuk secara langsung, membuat perubahan dalam fungsi juga berpengaruh pada variabel aslinya tanpa perlu menggunakan operator dereferensi. 

## Guided

### soal 1 (Call by pointer)

Program ini digunakan untuk menukar nilai dua variabel dengan menggunakan pointer. Fungsi tukar memanfaatkan alamat memori (&a dan &b) sehingga perubahan yang dilakukan di dalam fungsi langsung memengaruhi nilai variabel aslinya. Dengan cara ini, nilai a dan b berhasil ditukar tanpa perlu mengembalikan nilai dari fungsi.
```go
#include <iostream>
using namespace std;

void tukar(int *px, int *py)
{
    int temp = *px;
    *px = *py;
    *py = temp;
}

int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(&a, &b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}
```
>Output
>![output](output/gu_1.jpg)

### soal 2 (Call by referance)

Program ini digunakan untuk menukar nilai dua variabel dengan memanfaatkan parameter referensi. Dengan cara ini, perubahan yang dilakukan dalam fungsi langsung memengaruhi variabel aslinya. Hasilnya, nilai a dan b berhasil ditukar dari 10 dan 20 menjadi 20 dan 10.
```go
#include <iostream>
using namespace std;

void tukar(int &x, int &y)
{
    int temp = x;
    x = y;
    y = temp;
}

int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(a, b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}
```
>Output
>![output](output/gu_2.jpg)


## Unguided

### Soal 1
Buatlah sebuah program untuk melakukan transpose pada sebuah matriks persegi berukuran 3x3. Operasi transpose adalah mengubah baris menjadi kolom dan sebaliknya. Inisialisasi matriks awal di dalam kode, kemudian buat logika untuk melakukan transpose dan simpan hasilnya ke dalam matriks baru. Terakhir, tampilkan matriks awal dan matriks hasil transpose.
Contoh Output:
>![soal](output/soal_gu_1.jpg)

```go
#include <iostream>
using namespace std;

int main() {
    int matriks_awal[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9} };
    
    int matriks_transpose[3][3];

    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            matriks_transpose[j][i] = matriks_awal[i][j];
        }
    }

    cout << "matriks awal adalah :" << endl;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << matriks_awal[i][j] << " ";
        }
        cout << endl;
    }

    cout << "\nsetelah di transpose menjadi :" << endl;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << matriks_transpose[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}
```

> Output
> ![Screenshot bagian x](output/ung_1.jpg)

Program ini digunakan untuk melakukan transpose matriks berukuran 3x3, yaitu menukar baris menjadi kolom dan kolom menjadi baris. Proses ini dilakukan dengan memanfaatkan array 2 dimensi dan perulangan bersarang (for di dalam for).

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
> ![output](output/ung_2.jpg)

Program ini digunakan untuk menghitung kuadrat dari sebuah bilangan dengan memanfaatkan fungsi yang menggunakan parameter referensi. Dengan cara ini, variabel asli langsung dimodifikasi di dalam fungsi tanpa perlu mengembalikan nilai.

## Referensi

1. https://www.w3schools.com/cpp/cpp_arrays_multi.asp
2. https://www.w3schools.com/cpp/cpp_pointers.asp
3. https://www.w3schools.com/cpp/cpp_references.asp
4. https://www.belajarcpp.com/tutorial/cpp/multidimensional-array/
5. https://www.belajarcpp.com/tutorial/cpp/pointer/
6. https://www.belajarcpp.com/tutorial/cpp/reference/
