## Tugas 7

**Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.**
Stateless widget adalah widget yang tidak berubah atau bereaksi terhadap perubahan state. Mereka bersifat statis dan hanya perlu dirender satu kkali. Contohnya seperti Text, Icon, atau Container. Sementara itu, Stateful widget adalah widget yang dapat berubah seiring waktu, biasanya karena ada perubahan data atau interaksi pengguna. Mereka memiliki state yang bisa diperbarui, seperti widget Checkbox, TextField, atau Switch.

**Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.**
`MaterialApp`: Widget utama yang memulai aplikasi berbasis material design. MaterialApp menyediakan konfigurasi global, seperti theme, routes, 
dan home, yang menentukan tema, rute navigasi, dan halaman utama aplikasi.
`ThemeData`: Objek yang menyimpan konfigurasi tema global aplikasi, seperti warna utama, gaya teks, ikon, dan tampilan elemen UI lainnya, sehingga desain aplikasi tetap konsisten.
`Container`: Widget serbaguna yang dapat digunakan untuk membungkus widget lain dengan fitur penyesuaian seperti ukuran, margin, padding, warna latar, dan dekorasi.
`Padding`: Widget yang menambahkan ruang di sekitar widget anak. Padding sering digunakan untuk memberi jarak antar elemen agar tampilan lebih rapi.
`Column`: Widget yang menata anak-anaknya dalam susunan vertikal dari atas ke bawah, cocok untuk tata letak elemen secara berurutan dari atas ke bawah.
`Row`: Widget yang menata anak-anaknya dalam susunan horizontal dari kiri ke kanan, biasanya digunakan untuk menyusun elemen-elemen di dalam baris.
`AppBar`: Widget header di bagian atas halaman, biasanya berisi judul halaman, tombol navigasi, dan ikon aksi. AppBar adalah bagian dari Scaffold.
`Scaffold`: Struktur dasar halaman aplikasi berbasis material design yang menyediakan tata letak utama, termasuk AppBar, body, floatingActionButton, dan drawer.
`InkWell`: Widget yang memberikan efek sentuhan atau "ripple effect" pada widget yang di-klik. Sering digunakan untuk memberikan efek interaktif pada widget seperti gambar atau teks.
`Text`: Widget untuk menampilkan teks di layar. Text mendukung berbagai pengaturan gaya dan penempatan teks.
`TextStyle`: Objek yang digunakan untuk mengatur gaya teks, seperti ukuran font, warna, ketebalan, dan lainnya, yang diterapkan pada widget Text.
`Center`: Widget yang memposisikan widget anak di tengah-tengah area yang tersedia, baik secara vertikal maupun horizontal.

**Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.**
Fungsi setState() digunakan dalam Stateful widget untuk memberi tahu framework bahwa ada perubahan state yang perlu di-render ulang. Semua variabel yang didefinisikan dalam kelas widget yang bersifat dinamis dapat terdampak, terutama yang memengaruhi UI, seperti variabel boolean, string, atau list yang digunakan untuk mengelola status.

**Jelaskan perbedaan antara `const` dengan final.**
const dan final sama-sama digunakan untuk membuat variabel yang nilainya tidak dapat diubah. `const` digunakan untuk nilai yang bersifat tetap secara compile-time, sedangkan final digunakan untuk nilai yang hanya ditetapkan sekali namun baru diketahui di runtime.

**Langkah-Langkah Pengimplementasian:**
1. Membuat file menu.dart.
2. Membuat class MyHomePage dan menambahkan widget AppBar yang memuat judul aplikasi serta widget Padding yang berisi pesan dan tombol-tombol.
3. Membuat class ItemHomePage dan ItemCard yang akan digunakan untuk mendefinisikan tombol-tombol yang ditampilkan pada halaman utama.
4. Mengimplementasikan SnackBar yang akan ditampilkan ketika menekan tombol-tombol pada halaman utama.

## Tugas 8

**Apa kegunaan `const` di Flutter? Jelaskan apa keuntungan ketika menggunakan `const` pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?**
kata kunci `const` digunakan untuk mendeklarasikan nilai atau widget sebagai konstanta, yang artinya nilainya tetap dan tidak akan berubah saat runtime. Penggunaan `const` pada widget memiliki banyak keuntungan, terutama dalam hal kinerja aplikasi. Dengan const, Flutter dapat menghindari pembentukan ulang (rebuilding) widget yang nilainya tidak berubah, sehingga aplikasi dapat berjalan lebih efisien karena mengurangi beban pada UI rendering. Kita sebaiknya menggunakan `const` ketika kita tahu bahwa nilai suatu widget atau objek tidak akan berubah sepanjang siklus hidupnya, misalnya pada teks, ikon, atau padding yang sifatnya statis. Sebaliknya, jika ada kemungkinan bahwa nilai atau tampilan widget akan berubah, misalnya pada widget dinamis yang menampilkan data dari API, maka `const` sebaiknya tidak digunakan.

**Jelaskan dan bandingkan penggunaan `Column` dan `Row` pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!**
`Column` dan `Row` adalah dua widget layout dasar di Flutter yang berfungsi untuk menyusun widget anak secara vertikal dan horizontal. `Column` akan menyusun widget anak secara vertikal dari atas ke bawah, sementara `Row` menyusun widget anak secara horizontal dari kiri ke kanan. Keduanya sangat berguna dalam membangun UI yang terstruktur, dan dapat dikombinasikan untuk menciptakan tampilan yang kompleks. Penggunaan `Column` lebih cocok untuk elemen-elemen yang disusun berlapis secara vertikal, seperti list item atau form. Sebaliknya, `Row` lebih cocok untuk elemen-elemen yang perlu disusun bersebelahan secara horizontal, seperti tombol-tombol dalam baris atau ikon di samping teks.

Contoh implementasi `Column`:
```
    Column(
        mainAxisAlignment: MainAxisAlignment.start,
        children: [
            Text('Judul'),
            Text('Deskripsi'),
            ElevatedButton(onPressed: () {}, child: Text('Klik Saya')),
        ],
    )

```
Contoh implementasi `Row`   :

```
    Row(
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
        children: [
            Icon(Icons.home),
            Icon(Icons.favorite),
            Icon(Icons.settings),
        ],
    )

```

**Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!**
Elemen input yang saya gunakan dalam tugas ini adalah `TextField`. `TextField` adalah widget dasar untuk menerima input teks dari pengguna. Widget ini memungkinkan pengguna untuk memasukkan teks, yang dapat digunakan untuk formulir, pencarian, atau input data lainnya. `TextField` juga mendukung konfigurasi lanjutan, seperti menambahkan kontrol panjang teks, input multi-baris, pengaturan gaya, serta berbagai metode untuk memvalidasi dan mengelola input. Selain `TextField` terdapat elemen-elemen input lainnya seperti `Checkbox` dan `Switch` untuk memilih opsi on/off, dan `Slider` untuk memilih nilai dalam rentang tertentu. Elemen `Radio` dan `DropdownButton` memungkinkan pengguna memilih satu dari beberapa opsi, sedangkan `DatePicker` dan `TimePicker` digunakan untuk memilih tanggal dan waktu. Ada juga `GestureDetector`, yang mendeteksi interaksi lebih kompleks seperti swipe dan tap pada widget khusus.

**Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?**
Flutter menyediakan `ThemeData`, yang memungkinkan kita mengonfigurasi tema global aplikasi dengan mudah. Tema ini mencakup berbagai elemen UI seperti warna utama, warna aksen, font, bentuk tombol, serta gaya teks untuk header, body, dan lainnya. Untuk menerapkan tema global, kita mendefinisikan `ThemeData` di properti `theme` dan `darkTheme` (untuk tema gelap) pada widget MaterialApp. Dengan begitu, perubahan tema akan diterapkan ke semua widget yang mendukung gaya sesuai dengan tema yang didefinisikan. Pada file `main.dart` saya mengimplementasikan `ThemeData` melalui properti `theme` yang terdapat dalam `MaterialApp`

**Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?**
Dalam tugas ini, saya mengimplementasikan widget `Navigator` dan `MaterialPageRoute`. `Navigator` berfungsi sebagai pengelola rute atau halaman dalam aplikasi. `Navigator` menggunakan konsep tumpukan (stack) untuk menangani perpindahan antarhalaman, di mana setiap halaman baru yang dibuka akan berada di atas tumpukan, dan halaman sebelumnya berada di bawahnya. Setiap kali kita berpindah ke halaman baru, kita menambahkannya ke dalam tumpukan menggunakan metode `Navigator.push()`. Untuk kembali ke halaman sebelumnya, kita bisa menggunakan `Navigator.pop()`, yang menghapus halaman teratas dari tumpukan. `Navigator` memungkinkan perpindahan antarhalaman yang fleksibel, baik menggunakan navigasi yang eksplisit maupun melalui rute bernama (named routes). Sementara itu, `MaterialPageRoute` adalah widget yang digunakan untuk membuat rute baru berbasis material design. `MaterialPageRoute` mengambil widget sebagai argumen builder, yang menentukan halaman baru yang akan ditampilkan, dan juga bisa menerima argumen tambahan untuk dikirim ke halaman tujuan.

