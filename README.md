<summary>Tugas 7</summary>
<details>

### 1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?
Perbedaan utama antara stateless dan stateful widget adalah kebisaannya untuk diubah setelah diubah setelah dibuat. Stateless widget bersifat immutable, yaitu setelah diciptakan objeknya, propertinya tidak dapat diubah. Di sisi lain, stateful widget bersifat mutable, yaitu dapat berubah setelah dibuat. Jika ada perubahan, stateful widget akan melakukan rebuild untuk menerapkan perubahan yang terjadi.

### 2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.
- MaterialApp: widget yang menginisialisasi projek flutter dan menjadi parent dari semua widget lain
- Scaffold: widget yang memberikan stuktur dasar untuk aplikasinya
- AppBar: widget yang memiliki fungsi seperti navbar
- Text: widget untuk menampilkan tulisan
- SingleChildScrollView: widget yang membuat tampilan aplikasi dapat di-scroll jika ukurannya melebihi ukuran screen
- Padding: widget yang memberikan padding (jarak antara margin dan content)
- Column: widget untuk menampilkan children-nya dalam secara vertikal
- GridView.count: widget untuk menciptakan tampilan seperti tabel dengan jumlah kolom yang ditentukan
- Material: widget yang berguna untuk mengatur background, dalam kasus ini mengatur background dari ItemCard
- InkWell: widget yang membuat ItemCard merespon terhadap sentuhan
- ScaffoldMessenger: widget yang berfungsi menyediakan API untuk memunculkan snackbar
- SnackBar: widget untuk memunculkan pesan singkat di bagian bawah layar untuk periode waktu singkat
- Container: widget untuk menampung isi dari ItemCard
- Center: widget yang berfungsi untuk memposisikan children-nya ditengah
- Icon: widget yang berguna untuk menampilkan ikon
- MyHomePage: widget untuk tampilan utama dari aplikasi

### 3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
Pertama untuk membuat sebuah program Flutter baru saya menjalankan perintah `flutter create melody_mementos`. Kemudian untuk membuat tiga tombol sederhana, saya membuat file baru bernama menu.dart. Di file tersebut saya membuat class MyHomePage yang membuat widget Scaffold sebagai struktur dasar aplikasi saya. Disitu saya menambahkan AppBar yang mengandung judul aplikasi saya. Kemudian di body scaffold saya wrap semua dalam SingleChildScrollView agar halaman dapat di scroll dan di dalamnya saya isi dengan berbagai widget yang saya butuhkan. Untuk menampilkan button itu sendiri saya menggunakan GridView.count dan diisi properti children dengan ketiga tombol yang merupakan objek dari ItemCard. Di dalam class MyHomePage saya membuat sebuah list yang isinya adalah objek Item untuk tiap tombol yang ingin dibuat. Pada class Item dinyatakan 3 atribut, yaitu nama, icon, color (background color button).
Dalam Class ItemCard, akan dibuat sebuah widget material dengan child sebuah widget InkWell. Widget inilah yang dapat membuat button menjadi responsive. Properti onTap diisi dengan sebuah fungsi yang memunculkan sebuah SnackBar dengan pesan sesuai permintaan tugas. Kemudian child dari InkWell ini diisi sebuah Container yang memuat icon dan tulisan dengan memanfaatkan widget Icon dan Text.
Pertanyaan pada README saya jawab dengan mencari informasi dari internet dan dokumentasi flutter.
Bagian bonus dikerjakan dengan mengisi atribut color dengan warna button yang diinginkan saat pembuatan objek Item. Lalu, atribut ini akan dipanggil sebagai isi dari properti color pada widget Material di ItemCard.

</details>
