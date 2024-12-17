# stream_wahyulak

Praktikum Stream

## Wahyu Laksono Saputra || 362358302107


Soal 3 
Keyword yield* pada kode tersebut memiliki fungsi khusus dalam konteks async generator function:
    1. yield* digunakan untuk mendelegasikan atau menyebarkan (delegate) stream yang ada ke stream utama.
    2. Dalam konteks kode ini, yield* mengembalikan seluruh stream yang dihasilkan oleh Stream.periodic().
    3. Stream.periodic() menghasilkan stream yang mengeluarkan event setiap detik, dengan nilai warna yang berubah secara berurutan dari list colors.
    4. Dengan yield*, setiap event dari stream Stream.periodic() akan secara otomatis ditambahkan ke stream utama yang sedang dibuat.

