## Tugas 7

**Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.**
Stateless widget adalah widget yang tidak berubah atau bereaksi terhadap perubahan state. Mereka bersifat statis dan hanya perlu dirender satu kkali. Contohnya seperti Text, Icon, atau Container. Sementara itu, Stateful widget adalah widget yang dapat berubah seiring waktu, biasanya karena ada perubahan data atau interaksi pengguna. Mereka memiliki state yang bisa diperbarui, seperti widget Checkbox, TextField, atau Switch.

**Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.**
Scaffold: untuk membuat struktur dasar aplikasi seperti AppBar dan Body.
Text: untuk menampilkan teks statis pada aplikasi.

**Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.**
Fungsi setState() digunakan dalam Stateful widget untuk memberi tahu framework bahwa ada perubahan state yang perlu di-render ulang. Semua variabel yang didefinisikan dalam kelas widget yang bersifat dinamis dapat terdampak, terutama yang memengaruhi UI, seperti variabel boolean, string, atau list yang digunakan untuk mengelola status.

**Jelaskan perbedaan antara const dengan final.**
const dan final sama-sama digunakan untuk membuat variabel yang nilainya tidak dapat diubah. const digunakan untuk nilai yang bersifat tetap secara compile-time, sedangkan final digunakan untuk nilai yang hanya ditetapkan sekali namun baru diketahui di runtime.

**Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.**
Implementasi checklist dilakukan dengan memanfaatkan widget Checkbox dalam widget ListView. Setiap item checklist disimpan dalam list boolean untuk melacak status terpilih, dan setState() digunakan untuk memperbarui tampilan saat pengguna mengklik salah satu checklist tersebut.