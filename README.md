<h2> MELODY MEMENTOS </h2><br>
Nama: Veronica Kylie<br>
NPM: 2206029563 <br>
Kelas: PBP D <br>

<details>
<summary>Tugas 7</summary>

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

<details>
<summary>Tugas 8</summary>

### 1. Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!
Navigator.push() digunakan untuk menampilkan halaman baru dan menambahkannya di atas stack halaman-halaman sebelumnya. Ketika pengguna menekan tombol back, pengguna akan kembali ke halaman sebelumnya. Contoh penggunaan Navigator.push() adalah saat berpindah dari halaman utama ke halaman tambah item baru pada tugas individu. Di sisi lain, Navigator.pushReplacement() menampilkan halaman baru dengan menggantikan halaman yang berada di paling atas. Dampaknya pengguna tidak dapat kembali ke halaman sebelumnya menggunakan tombol back. Contoh penggunaan Navigator.pushReplacement() adalah saat melakukan navigasi ke suatu halaman dari sidebar pada tugas individu. Selain itu, situasi yang cocok untuk menggunakan pushReplacement adalah saat pengguna berhasil login dan pindah ke halaman lain.

### 2. Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!
1. Container: digunakan sebagai wadah untuk mengatur tata letak dan memberi styling pada elemen, misalnya padding dan margin.
2. Column: digunakan untuk mengatur elemen secara vertikal
3. Row: digunakan untuk mengatur elemen secara horizontal
4. Center: digunakan untuk mengatur posisi elemen ditengah
5. ListView: digunakan untuk membuat daftar yang bisa discroll
6. Stack: digunakan untuk menumpuk elemen di atas satu sama lain
7. Card: digunakan untuk menampung elemen-elemen lain untuk membuat tampilan seperti kartu
8. Expanded: digunakan untuk mengatur bagian yang mengisi ruang kosong pada Row atau Column
9. Sizedbox: digunakan untuk mengatur ukuran tinggi dan lebar sebuh widget
10. GridView: digunakan untuk menampilkan elemen dengan bentuk tabel
11. Align: digunakan untuk mengatur posisi align dari child terhadap elemen parentnya
12. Padding: digunakan untuk menambahkan padding di sekeliling elemen child
13. Transform: digunakan untuk mengubah ukuran dan posisi elemen child

### 3. Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!
Elemen input yang digunakan pada form tugas ini adalah TextFormField. Saya menggunakan elemen input ini karena semua input yang diminta dari pengguna berupa teks dan jenis elemen input ini cocok untuk input teks.

### 4. Bagaimana penerapan clean architecture pada aplikasi Flutter?
Penerapan clean architecture pada Flutter berarti membagi aplikasi menjadi beberapa lapisan, yaitu:
- Lapisan logika bisnis: merupakan lapisan yang berisi model dan logika bisnis. Flutter biasa menggunakan BLoC (Business Logic Component), Provider, atau Redux untuk mengelola logika bisnis.
- Lapisan data: lapisan yang berhubungan dengan pemanggilan API, basis data, penyimpanan lokal, dan sumber data eksternal lainnya
- Lapisan presentation: merupakan lapisan yang mengatur penggunaan widget untuk membuat tampilan UI 
 
### 5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)
Untuk membuat halaman form baru, saya membuat folder baru bernama screens dan di dalamnya saya membuat file baru bernama shoplist_form.dart. Lalu, file menu.dart saya pindahkan ke folder itu. Pada 
file shoplist_form.dart saya membuat sebuah class baru dan didalamnya membuat tampilannya dengan berbagai widget. Form dibuat dengan widget Form dan inputnya menggunakan TextFormField. Lalu, atribut/propertinya saya isi sesuai kebutuhan. Untuk membuat validasi input, saya menggunakan properti onChanged yang akan mengambil data yang diinput ke dalam sebuah variabel. Lalu, properti validator diisi dengan memastikan tidak kosong atau null. Validasi input pada field jumlah ditambahkan dengan memastikan inputnya angka menggunakan int.tryParse.
Selanjutnya, saya membuat save button dengan widget ElevatedButton dan pada properti onPressed akan dijalankan fungsi untuk memunculkan pop up item berhasil disimpan. Pop up dibuat dengan widget AlertDialog
Selanjutnya, pada menu.dart saya menambahkan di properti onTap pada card yang dibuat. Saya menambahkan ketentuan jika nama item yang dipencet adalah "Tambah Item", maka akan menjalankan push halaman form tambah item.
Terakhir untuk left drawer, saya lakukan dengan membuat folder baru bernama widgets. Disitu saya menambahkan file baru bernama left_drawer.dart. Kemudian, saya menggunakan widget ListTile untuk membuat opsi halaman utama dan tambah item. Di dalam properti onTap, saya menambahkan function untuk mengarahkan ke halaman yang sesuai.
</details>

<details>
<summary>Tugas 9</summary>

### 1. Apakah bisa kita melakukan pengambilan data JSON tanpa membuat model terlebih dahulu? Jika iya, apakah hal tersebut lebih baik daripada membuat model sebelum melakukan pengambilan data JSON?
Ya, pengambilan data JSON tanpa membuat model dapat dilakukan. Hal ini berarti kita menerima data json dan akan diproses sesuai struktur data default yang ada di bahasa pemrograman kita. Namun, lebih baik untuk membuat model terlebih dahulu. Hal ini membuat kode kita lebih mudah untuk di-maintain, berfungsi sebagai dokumentasi, memvalidasi data yang masuk, dan menjaga konsistensi dalam kode.

### 2. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
CookieRequest berfungsi untuk mengelola permintaan request yang berhubungan dengan cookie dalam aplikasi. Class ini akan melacak informasi terkait sesi pengguna agar tetap terjaga informasinya selama pengguna menggunakan aplikasi.

Instance CookieRequest dibagikan ke semua komponen untuk menjamin bahwa manajemen cookie dilakukan dengan seragam di seluruh aplikasi tersebut sehingga sesi pengguna akan dikelola secara konsisten.

### 3. Jelaskan mekanisme pengambilan data dari JSON hingga dapat ditampilkan pada Flutter.
Pertama, perlu import library dan package yang dibutuhkan untuk melakukan convert dan http request. Selanjutnya, dilakukan fetch data dengan hit endpoint yang akan memberikan kita data json. Selanjutnya, perlu dilakukan parsing atau mengubah response agar dikenali sebagai bentuk json. Terakhir, untuk menampilkan data di flutter dapat menggunakan berbagai widget. Pada kasus ini, saya menggunakan ListView.builder dan widget Text di dalamnya untuk menampilkan data, seperti contoh berikut `Text("${snapshot.data![index].fields.description}")`

### 4. Jelaskan mekanisme autentikasi dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
Menggunakan package pbp_django_auth, saya membuat CookieRequest baru untuk sesi tersebut. Selanjutnya, akan dilakukan autentikasi dengan mengirimkan username dan password yang dimasukkan user ke endpoint untuk login yang ada di Django. Function pada Django akan mengembalikan sebuah response tergantung keberhasilan dari proses autentikasi. Jika response yang diberikan berhasil, maka akan ditampilkan menu. Namun, jika gagal akan tetap di page login.

### 5. Sebutkan seluruh widget yang kamu pakai pada tugas ini dan jelaskan fungsinya masing-masing.
- TextField: digunakan untuk menerima input dari pengguna.
- ElevatedButton: digunakan untuk membuat tombol dengan efek elevasi saat ditekan.
- ListView.builder: digunakan untuk membuat daftar item yang dapat discroll.
- LeftDrawer: digunakan untuk menampilkan sejenis navbar di sebelah kiri screen. Merupakan widget kustom.
-  SizedBox: digunakan untuk memberi jarak antarwidget.
- TextButton: digunakan untuk menampilkan tombol dalam teks.
- FutureBuilder: digunakan untuk membangun widget berdasarkan hasil terbaru dari menjalankan function pada Future.

### 6. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).
Pertama saya membuat app baru pada django yang bernama authentication. Saya menginstall library corsheaders dan menambahkan kedua hal tadi ke installed apps di settings.py. Selain itu, di flutter juga saya menambahkan setting agar bisa mengakses internet. Selanjutnya, saya menambahkan function untuk login dan logout, serta routing yang diperlukan. Lalu, saya membuat page yang dibutuhkan untuk login dan mengatur (di main.dart) agar page yang pertama terbuka adalah login. Saya juga menambahkan else if jika card logout dipencet, maka akan melakukan logout dan kembali ke halaman login. Selanjutnya, saya membuat model kustom sesuai yang saya memiliki dengan memasukkan json dari model saya ke QuickType. Saya memasukkan code dari situ ke lib/models/item.dart. Kemudian, saya melakukan integrasi untuk bisa menambahkan item baru dari flutter dengan membuat function create_product_flutter di main/views.py pada Django, tidak lupa routingnya juga. Lalu, di flutter saya menambahkan agar saat button submit pada form dipencet maka akan mengirimkan data yang dimasukkan ke endpoint create_product_flutter tadi dan akan ditampilkan behavior sesuai dengan response dari function pada Django tadi.

Saya menampilkan daftar item yang ada dengan membuat file baru di screens, dimana disitu terjadi fetch data dari web yang sudah di deploy dan menampilkannya pada flutter. Saya juga membuat setiap produk memiliki properti onTap yang akan menampilkan halaman baru untuk menampilkan detail semua atribut dari produk itu. Penampilan detail ini dilakukan dengan detail.dart yang menerima argumen berupa semua atribut dari produk itu. Jadi, tidak terjadi fetching lagi. Selanjutnya saya menambahkan opsi untuk ke page daftar item dari left drawer. 

</details>