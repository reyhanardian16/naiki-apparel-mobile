Nama : Muhammad Reyhan Ardian

NPM : 230627185

Kelas : PBP D

Implementasi Checklist
  1. Membuat sebuah program Flutter baru dengan tema E-Commerce yang sesuai dengan tugas-tugas sebelumnya.

Dengan menginisialisasi projek flutter dengan flutter create, lalu menambahkan widget-widget didalamnya

  2. Membuat tiga tombol sederhana dengan ikon dan teks

Dengan menambahkan widget itemCard ke dalam myHomePage dengan masing-masing memiliki konteks berupa nama, ikon dan warna

  3. Mengimplementasikan warna-warna yang berbeda untuk setiap tombol (Lihat Daftar Produk, Tambah Produk, dan Logout).

Dengan menambahkan parameter warna pada itemCard dan menambahkan warna yang berbeda pada masing-masing item 

  4. Memunculkan Snackbar

Dengan memanggil fungsi showSnackBar pada saat onTap widget itemCard, dan mengisi parameter yang sesuai



Pertanyaan

  1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.

Stateless widget adalah widget yang tidak memiliki state yang dapat berubah setelah dibuat. 
Stateless widget hanya merender tampilan tersebut hanya ketika pertama kali dipanggil dan tidak akan berubah meskipun terdapat perubahan data didalamnya. 
Stateless widget dapat digunakan untuk elemen yang statis seperti judul, text, icon, gambar, dll

Stateful widget adalah widget yang memiliki state yang bisa berubah saat aplikasi berjalan. 
Saat state berubah (misalnya karena interaksi pengguna atau perubahan data), widget akan merender ulang tampilannya secara otomatis untuk mencerminkan perubahan tersebut. 
Stateful widget dapat digunakan untuk elemen UI yang dinamis atau yang perlu menanggapi interaksi pengguna, seperti tombol yang bisa diaktifkan/nonaktifkan, form input, atau daftar yang dapat diperbarui.

  2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.

Widget yang digunakan pada proyek ini:
MyHomePage: Widget utama yang berisi widget lainnya
InfoCard: Widget yang berisi nama, kelas, npm
ItemCard: Widget yang berisi tombol lihat produk, tambah produk, dan logout

  3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.

Fungsi setState() dalam Flutter adalah metode yang digunakan dalam Stateful Widget untuk memberi tahu framework bahwa state pada widget telah berubah dan tampilan (UI) harus diperbarui. 
Dengan kata lain, setState() adalah cara untuk memicu rebuild dari widget, sehingga perubahan yang terjadi pada data atau variabel tertentu akan langsung terlihat di layar.
Hanya variabel yang ada di dalam state (dideklarasikan di dalam class _MyWidgetState atau class turunan State) yang akan terpengaruh oleh setState(). 
Variabel ini biasanya merupakan properti atau variabel yang sifatnya mutable (bisa berubah), dan didefinisikan di dalam StatefulWidget.

  4. Jelaskan perbedaan antara const dengan final.

final digunakan untuk membuat variabel yang hanya bisa diinisialisasi sekali (satu kali saja), tetapi inisialisasinya bisa dilakukan saat runtime (saat aplikasi berjalan).

const digunakan untuk membuat variabel yang bersifat compile-time constant. Artinya, nilai dari variabel ini sudah harus diketahui saat compile-time (saat aplikasi dikompilasi), bukan saat runtime.
