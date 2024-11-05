<blockquote>
Nama : Irfan Rizqi Nurrahman
Kelas : PBP C
NPM : 2306216724
<blockquote>

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

Step 1 : Mengubah Tema warna aplikasi pada main.dart menjadi brown
Step 2 : Mengubah sifat widget menjadi stateless dengan penghapusan informasi dan extends StatelessWidget.
Step 3 : Membuat card sederhana yang berisi informasi pribadi seperti NPM, Nama dan Kelas dengan membuat class Infocard
Step 4 : Membuat Button card sederhana dan iconnya dengan class baru bernama ItemHomepage, lalu tambahkan pada class MyHomePage. Desain interaksi dari tombol tersebut menggunakan class Itemcard.
Step 5 : Mengintegrasikan Infocard dan Itemcard untuk ditampilkan pada MyHomePage.
Step 6 : Flutter anaylyze supaya memastikan tidak ada isu.
Step 7 : Lakukan Git add, commit, and Push ke remote Repository.