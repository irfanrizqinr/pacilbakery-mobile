> Nama : Irfan Rizqi Nurrahman  
> Kelas : PBP C  
> NPM : 2306216724  


## Tugas 7

**1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.**


StatelessWidget adalah widget yang tidak memiliki state atau kondisi yang dapat berubah, sehingga tampilannya tetap sama selama aplikasi berjalan. Ini cocok untuk elemen statis, seperti teks atau ikon tetap. Sebaliknya, StatefulWidget adalah widget dengan state yang bisa berubah, memungkinkan tampilannya diperbarui secara dinamis berdasarkan interaksi atau perubahan data, seperti tombol hitung atau form input. Perbedaan utama keduanya adalah StatelessWidget tidak membutuhkan pembaruan tampilan secara internal, sedangkan StatefulWidget memerlukan metode setState untuk merender ulang saat state berubah.

**2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.**

 - Scaffold: Scaffold menyediakan struktur dasar halaman dengan  AppBar, body, dan area lainnya. Ini membantu membangun halaman aplikasi dengan struktur yang konsisten.

 - AppBar: AppBar adalah bilah di bagian atas layar yang berfungsi sebagai judul aplikasi. Pada proyek ini, AppBar menampilkan judul "PacilBakery" dengan gaya teks putih dan tebal.

 - Padding: Padding menambahkan ruang di sekitar widget yang dibungkusnya. Pada proyek ini, digunakan untuk memberikan jarak di sekitar body halaman dan elemen teks lainnya.

 - Column: Column adalah widget untuk menyusun widget secara vertikal. Di proyek ini, digunakan untuk menyusun InfoCard dan elemen lain secara vertikal di halaman.

 - Row: Row adalah widget untuk menyusun widget secara horizontal. Digunakan untuk menyusun tiga InfoCard agar ditampilkan berdampingan.

 - InfoCard (custom widget): InfoCard adalah widget kustom yang menampilkan informasi pengguna, seperti NPM, nama, dan kelas. Ini menggunakan Card untuk menampilkan data dalam bentuk kartu dengan teks judul dan konten.

 - SizedBox: SizedBox digunakan untuk memberikan jarak vertikal atau horizontal. Pada proyek ini, SizedBox digunakan untuk memberi jarak antara Row yang berisi InfoCard dan elemen di bawahnya.

 - Center: Center digunakan untuk memposisikan widget di tengah area yang tersedia. Di proyek ini, digunakan untuk memastikan Column berisi teks dan grid ditempatkan di tengah halaman.

 - GridView.count: GridView.count menampilkan item dalam bentuk grid dengan jumlah kolom tertentu. Di sini, digunakan untuk menampilkan daftar tombol ItemCard dalam bentuk grid tiga kolom.

 - ItemCard (custom widget): ItemCard adalah widget kustom yang menampilkan setiap item dalam grid. Masing-masing tombol ini berfungsi sebagai shortcut untuk "Lihat Daftar Product", "Tambah Product", atau "Logout" dan memiliki fungsi klik.

 - Card: Card digunakan dalam InfoCard untuk membuat tampilan seperti kartu dengan bayangan di bawahnya, memberikan tampilan terstruktur pada informasi NPM, nama, dan kelas.

 - Material: Material adalah widget dasar yang menampilkan efek visual seperti shadow dan rounded corners. Di sini, Material digunakan dalam ItemCard untuk menampilkan latar belakang berwarna dan bentuk bulat.

 - InkWell: InkWell adalah widget yang menambahkan efek klik pada widget yang dibungkusnya. Dalam ItemCard, InkWell digunakan untuk mendeteksi sentuhan pada tombol dan menampilkan SnackBar.

 - SnackBar: SnackBar adalah elemen notifikasi sementara di bagian bawah layar. Digunakan untuk menampilkan pesan saat tombol dalam ItemCard ditekan, seperti "Kamu telah menekan tombol Lihat Daftar Product".

 - Icon: Icon digunakan untuk menampilkan ikon kecil di setiap ItemCard, membantu pengguna mengidentifikasi fungsi tombol, seperti "Lihat Daftar Product" dengan ikon mood, "Tambah Product" dengan ikon tambah, dan "Logout" dengan ikon logout.

 - Text: Text digunakan untuk menampilkan teks di layar, baik dalam AppBar, InfoCard, ItemCard, maupun teks sambutan. Text dapat dikustomisasi dengan warna, ukuran, dan ketebalan.


**3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.**

Fungsi `setState()` dalam Flutter digunakan untuk memperbarui state dari suatu widget secara dinamis dan memastikan perubahan tersebut langsung tercermin dalam tampilan aplikasi. Saat `setState()` dipanggil, Flutter akan merender ulang widget yang dipengaruhi, memungkinkan UI menampilkan nilai terbaru dari variabel dalam state. Hanya variabel-variabel dalam kelas `State` dari widget tersebut yang terdampak, khususnya yang digunakan dalam `build` method. Misalnya, jika variabel `counter` diperbarui melalui `setState()`, maka tampilan yang menampilkan `counter` akan diperbarui untuk mencerminkan perubahan tersebut, menjaga aplikasi tetap interaktif dan responsif.

**4. Jelaskan perbedaan antara const dengan final.**

`final` dan `const` digunakan untuk mendeklarasikan nilai yang tidak berubah, tetapi memiliki perbedaan utama. `final` mengunci nilai setelah inisialisasi pertama kali dan memungkinkan nilainya ditetapkan saat runtime, cocok untuk data yang tetap setelah diinisialisasi, seperti waktu saat program berjalan. Sebaliknya, `const` mengharuskan nilainya diketahui saat kompilasi, memberikan konstanta waktu kompilasi yang benar-benar tetap dan efisien dalam penggunaan memori.

**5. Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.**

- Step 1 : Mengubah Tema warna aplikasi pada main.dart menjadi brown
- Step 2 : Mengubah sifat widget menjadi stateless dengan penghapusan informasi dan extends StatelessWidget.
- Step 3 : Membuat card sederhana yang berisi informasi pribadi seperti NPM, Nama dan Kelas dengan membuat class Infocard
- Step 4 : Membuat Button card sederhana dan iconnya dengan class baru bernama ItemHomepage, lalu tambahkan pada class MyHomePage. Desain interaksi dari tombol tersebut menggunakan class Itemcard.
- Step 5 : Mengintegrasikan Infocard dan Itemcard untuk ditampilkan pada MyHomePage.
- Step 6 : Flutter anaylyze supaya memastikan tidak ada isu.
- Step 7 : Lakukan Git add, commit, and Push ke remote Repository.

## Tugas 8

**1. Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?**

Di Flutter, `const` digunakan untuk membuat objek yang bersifat tetap dan tidak berubah selama runtime, sehingga Flutter dapat mengoptimalkan penggunaan memori dan performa aplikasi. Dengan `const`, objek yang sama hanya akan dibuat sekali dan di-reuse, menghemat memori dan mempercepat rendering karena tidak perlu alokasi ulang. `const` sebaiknya digunakan pada widget atau elemen UI yang statis, seperti teks atau ikon yang tidak berubah, serta pada konfigurasi tetap. Namun, hindari `const` pada widget dinamis atau objek yang membutuhkan data dari variabel atau fungsi yang bisa berubah, seperti `StatefulWidget`.

**2. Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!**


Di Flutter, `Column` dan `Row` adalah widget layout yang digunakan untuk menyusun widget secara vertikal (`Column`) atau horizontal (`Row`). `Column` menempatkan widget dari atas ke bawah, sedangkan `Row` menempatkan widget dari kiri ke kanan. Kedua widget ini mendukung pengaturan posisi dan ruang antar elemen dengan properti seperti `mainAxisAlignment` untuk pengaturan sepanjang arah utama (vertikal di `Column` dan horizontal di `Row`) dan `crossAxisAlignment` untuk arah sebaliknya. `Column` dan `Row` berguna untuk menyusun UI dalam bentuk blok atau baris sederhana. Contoh `Column`: `Column(children: [Text('Item 1'), Text('Item 2')])` menyusun dua teks vertikal; contoh `Row`: `Row(children: [Icon(Icons.star), Text('Rating')])` menyusun icon dan teks secara horizontal.

**3. Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!**


Pada halaman form yang saya buat, elemen input yang digunakan adalah:

- TextFormField: Terdapat tiga TextFormField, yaitu untuk mengisi Product Name, Amount, dan Description. Setiap TextFormField memiliki validator untuk memvalidasi input, misalnya untuk memastikan bahwa Amount harus berupa angka.

- ElevatedButton: Sebuah tombol bertuliskan "Add to Cart" yang mengirimkan data dari form jika semua input valid. Tombol ini menggunakan properti onPressed untuk memeriksa validasi form dan menampilkan AlertDialog ketika berhasil.

Selain elemen input yang saya gunakan, terdapat beberapa elemen input lain yang disediakan oleh Flutter tetapi tidak digunakan pada project ini, yakni:

- DropdownButton: Berguna untuk menampilkan daftar opsi yang bisa dipilih, yang mungkin lebih sesuai untuk memilih jenis produk daripada TextFormField.

- Checkbox: Dapat digunakan untuk memberikan opsi yang bersifat boolean (true/false), misalnya jika ada opsi tambahan untuk memilih jenis topping atau layanan tambahan.

- Radio Button: Berguna untuk memilih satu dari beberapa opsi, seperti memilih ukuran roti (kecil, sedang, besar).

- Switch: Biasanya digunakan untuk memilih opsi aktif atau non-aktif, misalnya untuk menandai apakah pengguna ingin menerima notifikasi tentang pembelian.

- Slider: Cocok untuk memilih rentang nilai, seperti memilih kuantitas jika ingin menyediakan cara input yang lebih interaktif dibandingkan memasukkan angka secara langsung.

- DatePicker dan TimePicker: Ini berguna jika form memerlukan input tanggal atau waktu, misalnya jika pengguna ingin memilih tanggal pengiriman.

**4. Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?**

saya mengatur berbagai elemen seperti warna primer, warna latar belakang, gaya teks, dan lainnya pada `main.dart`. Kemudian saya bisa implementasikan pada widget widget yang saya buat dengan memanggil `Theme.of(context).colorScheme.primary` atau `Theme.of(context).textTheme`.

**5. Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?**

Untuk mengimplementasikan navigasi pada Flutter, sebenarnya sudah disediakan sistem yang cukup lengkap untuk melakukan navigasi antar halaman. Saya melakukan routing kepada tiap halaman menggunakan `pushreplacement()`. Method `pushReplacement()` menghapus route yang sedang ditampilkan kepada pengguna dan menggantinya dengan suatu route. Method ini menyebabkan aplikasi untuk berpindah dari route yang sedang ditampilkan kepada pengguna ke suatu route yang diberikan. Saya juga menggunakan navigasi `Push()` pada button sehingga pengguna bisa kembali pada halaman yang sebelumnya.


## Tugas 9

**1. Jelaskan mengapa kita perlu membuat model untuk melakukan pengambilan ataupun pengiriman data JSON? Apakah akan terjadi error jika kita tidak membuat model terlebih dahulu?**

Membuat model untuk pengambilan atau pengiriman data JSON penting karena model berfungsi sebagai struktur atau kerangka yang memastikan data diproses sesuai format yang diharapkan. Dengan model, data JSON dapat diubah menjadi objek yang lebih mudah dikelola di kode, sehingga validasi dan manipulasi data menjadi lebih aman dan terstruktur. Jika kita tidak membuat model, pengolahan data JSON masih bisa dilakukan, tetapi lebih rentan terhadap error karena data yang diterima atau dikirim mungkin tidak sesuai format yang diharapkan. Hal ini dapat menyebabkan kesalahan parsing, kesalahan tipe data, atau bahkan runtime error saat mengakses properti yang tidak ada. Model juga meningkatkan keterbacaan kode dan mengurangi risiko bug.

**2. Jelaskan fungsi dari library http yang sudah kamu implementasikan pada tugas ini**

Library `http` dalam Flutter berfungsi untuk mempermudah aplikasi berkomunikasi dengan server melalui protokol HTTP. Dengan library ini, kita dapat mengirim permintaan HTTP seperti `GET`, `POST`, `PUT`, atau `DELETE` untuk mengambil atau mengirim data ke API. Library ini menangani proses pengiriman request, penerimaan response, dan pengelolaan error dengan cara yang lebih sederhana dan terstruktur. Selain itu, library `http` mendukung manipulasi header, encoding data, serta parsing response menjadi format seperti JSON atau teks, sehingga cocok digunakan dalam pengembangan aplikasi berbasis web service.

**3. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.**

`CookieRequest` adalah library yang digunakan untuk mengelola sesi autentikasi berbasis cookie dalam aplikasi Flutter, terutama saat berkomunikasi dengan server Django. Fungsinya mencakup pengiriman permintaan HTTP seperti login, logout, atau akses data, serta secara otomatis menyimpan dan menyertakan cookie sesi dalam setiap permintaan ke server. Membagikan instance `CookieRequest` ke semua komponen aplikasi penting agar setiap komponen dapat berbagi status autentikasi dan sesi yang konsisten. Dengan begitu, status login pengguna dapat dipantau secara global, data pengguna yang disimpan dalam cookie dapat diakses dengan mudah, dan pengalaman pengguna menjadi lebih mulus tanpa perlu membuat ulang atau menyinkronkan sesi secara manual di berbagai bagian aplikasi.

**4. Jelaskan mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter.**

Mekanisme pengiriman data di Flutter dimulai dari input data oleh pengguna melalui widget seperti TextField atau Form. Data tersebut ditangkap oleh controller (misalnya TextEditingController) dan kemudian diproses, seperti validasi atau manipulasi. Setelah itu, data dikirim ke server menggunakan library seperti http atau CookieRequest, dengan metode HTTP (POST, PUT, dll.), biasanya dalam format JSON. Server menerima data, memprosesnya sesuai logika backend, dan mengembalikan response. Response ini kemudian diolah di Flutter, biasanya dengan decoding JSON menggunakan library seperti dart:convert, untuk diubah menjadi objek atau model. Hasilnya ditampilkan ke pengguna melalui widget Flutter, seperti ListView atau Text, sehingga pengguna dapat melihat data yang dikirim atau hasil dari pengolahannya secara real-time.

**5. Jelaskan mekanisme autentikasi dari login, register, hingga logout. Mulai dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.**

Mekanisme autentikasi dari login, register, hingga logout mencakup beberapa tahap sebagai berikut:

**Register**: Pengguna menginput data akun, seperti username, password, dan informasi lainnya melalui form di Flutter. Data ini dikirim ke server Django menggunakan metode HTTP POST. Django memproses data, memvalidasi formatnya, dan menyimpan akun baru di database jika valid. Response sukses atau error dikembalikan ke Flutter, dan pesan tersebut ditampilkan kepada pengguna.

**Login**: Pengguna menginput username dan password melalui Flutter. Data ini dikirim ke endpoint login Django menggunakan metode HTTP POST. Django memvalidasi kredensial, mencocokkan username dan password dengan data di database. Jika valid, Django membuat sesi dan mengirimkan cookie sesi kepada Flutter melalui response. Cookie ini disimpan di sisi Flutter, biasanya menggunakan library seperti `CookieRequest`, untuk digunakan dalam permintaan berikutnya.

**Menu Setelah Login**: Setelah login berhasil, Flutter memanfaatkan cookie sesi untuk mengakses endpoint yang membutuhkan autentikasi. Django memverifikasi cookie ini pada setiap permintaan. Jika sesi valid, Django mengembalikan data yang diminta, seperti informasi menu atau halaman khusus pengguna yang telah login, yang kemudian ditampilkan di Flutter.

**Logout**: Saat logout, Flutter mengirim permintaan ke endpoint logout Django menggunakan metode HTTP POST atau GET, menyertakan cookie sesi. Django menghapus sesi tersebut dari server, sehingga cookie sesi tidak lagi valid. Setelah logout berhasil, Flutter menghapus cookie lokal dan mengarahkan pengguna kembali ke halaman login.

Mekanisme ini memastikan bahwa hanya pengguna yang terautentikasi yang dapat mengakses fitur-fitur tertentu, dengan mengandalkan cookie untuk menjaga status autentikasi di antara permintaan.

**6. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).**

Step 1 : Setup Autentikasi pada Django untuk Flutter
Step 2 : Integrasi Sistem Autentikasi pada Flutter
Step 3 : Pembuatan Model Kustom
Step 4 : Menambahkan Dependensi HTTP
Step 5 : Melakukan Fetch Data dari Django
Step 6 : Integrasi Form Flutter Dengan Layanan Django
Step 7 : Implementasi Fitur Logout