# stream_wahyulak

Praktikum Stream

## Wahyu Laksono Saputra || 362358302107


Soal 3 
Keyword yield* pada kode tersebut memiliki fungsi khusus dalam konteks async generator function:
    1. yield* digunakan untuk mendelegasikan atau menyebarkan (delegate) stream yang ada ke stream utama.
    2. Dalam konteks kode ini, yield* mengembalikan seluruh stream yang dihasilkan oleh Stream.periodic().
    3. Stream.periodic() menghasilkan stream yang mengeluarkan event setiap detik, dengan nilai warna yang berubah secara berurutan dari list colors.
    4. Dengan yield*, setiap event dari stream Stream.periodic() akan secara otomatis ditambahkan ke stream utama yang sedang dibuat.

Soal 4
![Soal 4](<assets/Screenshot (512).png>)
![Soal 4](<assets/Screenshot (513).png>)
![Soal 4](<assets/Screenshot (514).png>)

Soal 5

await for dan listen() adalah dua pendekatan berbeda dalam menangani stream di Dart.
await for bersifat sekuensial dan blocking. Eksekusi kode akan menunggu setiap event stream selesai diproses, mirip iterasi biasa namun asynchronous. Kodenya lebih linear, mudah dibaca, dan mendukung error handling tradisional melalui try-catch. Cocok untuk proses sederhana yang membutuhkan urutan eksekusi.
Sementara listen() adalah metode event-driven non-blocking. Ia memungkinkan penambahan listener tanpa menghentikan eksekusi kode utama, mendukung berbagai callback seperti onDone dan onError. Lebih fleksibel dalam menangani event, tetapi memerlukan manajemen subscription manual.

Soal 6

1. Bagian initState():
    - Membuat instance dari NumberStream
    - Mendapatkan controller stream
    - Mendengarkan (listen) perubahan stream
    - Setiap kali ada event/data baru, update state lastNumber
2. Bagian dispose():
    - Menutup stream controller untuk mencegah memory leak
3. Fungsi addRandomNumber():
    - Membuat angka random antara 0-9
    - Menambahkan angka random ke dalam stream
4. Bagian body:
    - Menampilkan teks dengan nilai terakhir yang diterima dari stream
    - Tombol "New Random Number" yang ketika ditekan akan memanggil addRandomNumber()
Singkatnya, ini adalah contoh implementasi stream sederhana di Flutter:

    - Setiap kali tombol ditekan, akan menghasilkan angka random baru
    - Angka tersebut akan ditampilkan di layar
    - Menggunakan stream untuk mengelola perubahan data secara reaktif

![Soal 6](<Screenshot (515).png>)
![Soal 6](<Screenshot (516).png>)