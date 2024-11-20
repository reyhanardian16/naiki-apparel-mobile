**Nama : Muhammad Reyhan Ardian**  
**NPM : 230627185**  
**Kelas : PBP D**  

## Tugas 7

**Implementasi Checklist**  

  - Membuat sebuah program Flutter baru dengan tema E-Commerce yang sesuai dengan tugas-tugas sebelumnya.  
Dengan menginisialisasi projek flutter dengan flutter create, lalu menambahkan widget-widget didalamnya

  - Membuat tiga tombol sederhana dengan ikon dan teks  
Dengan menambahkan widget itemCard ke dalam myHomePage dengan masing-masing memiliki konteks berupa nama, ikon dan warna

  - Mengimplementasikan warna-warna yang berbeda untuk setiap tombol (Lihat Daftar Produk, Tambah Produk, dan Logout)  
Dengan menambahkan parameter warna pada itemCard dan menambahkan warna yang berbeda pada masing-masing item 

  - Memunculkan Snackbar  
Dengan memanggil fungsi showSnackBar pada saat onTap widget itemCard, dan mengisi parameter yang sesuai

**1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.**  
Stateless widget adalah widget yang tidak memiliki state yang dapat berubah setelah dibuat. 
Stateless widget hanya merender tampilan tersebut hanya ketika pertama kali dipanggil dan tidak akan berubah meskipun terdapat perubahan data didalamnya. 
Stateless widget dapat digunakan untuk elemen yang statis seperti judul, text, icon, gambar, dll
Stateful widget adalah widget yang memiliki state yang bisa berubah saat aplikasi berjalan. 
Saat state berubah (misalnya karena interaksi pengguna atau perubahan data), widget akan merender ulang tampilannya secara otomatis untuk mencerminkan perubahan tersebut. 
Stateful widget dapat digunakan untuk elemen UI yang dinamis atau yang perlu menanggapi interaksi pengguna, seperti tombol yang bisa diaktifkan/nonaktifkan, form input, atau daftar yang dapat diperbarui.

**2. Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.**  
Widget yang digunakan pada proyek ini:
MyHomePage: Widget utama yang berisi widget lainnya
InfoCard: Widget yang berisi nama, kelas, npm
ItemCard: Widget yang berisi tombol lihat produk, tambah produk, dan logout

**3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.**  
Fungsi setState() dalam Flutter adalah metode yang digunakan dalam Stateful Widget untuk memberi tahu framework bahwa state pada widget telah berubah dan tampilan (UI) harus diperbarui. 
Dengan kata lain, setState() adalah cara untuk memicu rebuild dari widget, sehingga perubahan yang terjadi pada data atau variabel tertentu akan langsung terlihat di layar.
Hanya variabel yang ada di dalam state (dideklarasikan di dalam class _MyWidgetState atau class turunan State) yang akan terpengaruh oleh setState(). 
Variabel ini biasanya merupakan properti atau variabel yang sifatnya mutable (bisa berubah), dan didefinisikan di dalam StatefulWidget.

**4. Jelaskan perbedaan antara const dengan final.**  
final digunakan untuk membuat variabel yang hanya bisa diinisialisasi sekali (satu kali saja), tetapi inisialisasinya bisa dilakukan saat runtime (saat aplikasi berjalan).  
const digunakan untuk membuat variabel yang bersifat compile-time constant. Artinya, nilai dari variabel ini sudah harus diketahui saat compile-time (saat aplikasi dikompilasi), bukan saat runtime.


## Tugas 8 

**1. Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?**  
Const di Flutter digunakan untuk membuat sebuah nilai variabel tidak berubah dan konstan pada compile-time. Menggunakan const dapat memberikan keuntangan berupa efisiensi memori dan optimalisasi tender. Const sebaiknya digunakan untuk widget yang statis seperti gambar, ikon, text, dll. Const sebaiknya tidak digunakan pada widget yang dinamis atau memiliki nilai yang selalu berubah  

**2. Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!**  
Column berguna untuk menyusun elemen-elemen secara vertikal, seperti daftar atau form. Kita dapat menggunakan properti mainAxisAlignment untuk mengatur posisi elemen-elemen di sepanjang sumbu utama (dalam hal ini, vertikal). Sementara crossAxisAlignment digunakan untuk mengatur posisi elemen di sepanjang sumbu silang (horizontal). 
````
class ColumnExample extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Contoh Column'),
      ),
      body: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        crossAxisAlignment: CrossAxisAlignment.start,
        children: const [
          Text('Item 1'),
          Text('Item 2'),
          Text('Item 3'),
        ],
      ),
    );
  }
}

````
Row digunakan untuk menata elemen-elemen secara horizontal, seperti tombol navigasi atau deretan ikon. mainAxisAlignment dalam Row akan mengatur posisi elemen-elemen di sepanjang sumbu horizontal, sedangkan crossAxisAlignment akan mengatur posisi elemen di sepanjang sumbu vertikal.
````
class RowExample extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Contoh Row'),
      ),
      body: Row(
        mainAxisAlignment: MainAxisAlignment.spaceAround,
        crossAxisAlignment: CrossAxisAlignment.center,
        children: const [
          Icon(Icons.home),
          Icon(Icons.star),
          Icon(Icons.settings),
        ],
      ),
    );
  }
}
````
**3. Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!**  
Elemen input yang digunakan dalam tugas ini berupa nama dan deskripsi sebagai String dan harga sebagai integer  

**4. Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?**  
Untuk mengatur tema pada aplikasi flutter secara konsisten, saya bisa mengatur nilai-nilai themeData pada MaterialApp yang bisa berupa warna-warna berbeda untuk elemen yang berbeda, selain merubah nilai pada themeData saya juga dapat mengkonfigurasi tema elemen-elemen secara langsung. Di dalam tugas ini saya mengimplementasikan tema aplikasi di dalam themeData dan pada elemen tombol-tombol menu utama  

**5. Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?**  
Untuk menavigasikan berbagai macam halam di flutter saya dapat menggunakan elemen-elemen yang mengakses navigator untuk menambahkan rute ke tumpukan stack dan menghapus sesuai kebutuhan, implementasinya sendiri dapat berupa tombol atau dropdown yang mengarah ke page lain


## Tugas 9  

**Implementasi Checklist**

 - Mengimplementasikan fitur registrasi akun pada proyek tugas Flutter.
Dengan membuat page registrasi yang akan melakukan request json ke host yang sedang menjalankan projek Django yang telah mengimplementasikan fungsi register

 - Membuat halaman login pada proyek tugas Flutter.
Dengan membuat page login yang akan melakukan request json ke host yang sedang menjalankan projek Django yang telah mengimplementasikan fungsi login

 - Mengintegrasikan sistem autentikasi Django dengan proyek tugas Flutter.
Dengan membuat modul baru di projek django bernama authentication yang berfungsi mengimplementasikan fungsi-fungsi autentikasi dan mengintegrasikan models dengan projek flutter

 - Membuat model kustom sesuai dengan proyek aplikasi Django.
Dengan dibantu oleh quicktype, membuat struktur model yang sesuai dengan projek django agar dapat menerima dan mengirim data yang sesuai menggunakan json

 - Membuat halaman yang berisi daftar semua item yang terdapat pada endpoint JSON di Django yang telah kamu deploy.
Dengan membuat sebuaeh page yang meminta request json pada url projek django

```
class ProductEntryPage extends StatefulWidget {
  const ProductEntryPage({super.key});

  @override
  State<ProductEntryPage> createState() => _ProductEntryPageState();
}

class _ProductEntryPageState extends State<ProductEntryPage> {
  Future<List<ProductEntry>> fetchProduct(CookieRequest request) async {
    // TODO: Ganti URL dan jangan lupa tambahkan trailing slash (/) di akhir URL!
    final response = await request.get('http://127.0.0.1:8000/json/');

    // Melakukan decode response menjadi bentuk json
    var data = response;

    // Melakukan konversi data json menjadi object MoodEntry
    List<ProductEntry> listProduct = [];
    for (var d in data) {
      if (d != null) {
        listProduct.add(ProductEntry.fromJson(d));
      }
    }
    return listProduct;
  }

  @override
  Widget build(BuildContext context) {
    final request = context.watch<CookieRequest>();
    return Scaffold(
      appBar: AppBar(
        title: const Text('Product List'),
      ),
      drawer: const LeftDrawer(),
      body: FutureBuilder(
        future: fetchProduct(request),
        builder: (context, AsyncSnapshot snapshot) {
          if (snapshot.data == null) {
            return const Center(child: CircularProgressIndicator());
          } else {
            if (!snapshot.hasData) {
              return const Column(
                children: [
                  Text(
                    'Belum ada produk pada Naiki Apparel.',
                    style: TextStyle(fontSize: 20, color: Color(0xff59A5D8)),
                  ),
                  SizedBox(height: 8),
                ],
              );
            } else {
              return ListView.builder(
                  itemCount: snapshot.data!.length,
                  itemBuilder: (_, index) {
                    final product = snapshot.data![index];

                    return GestureDetector(
                      onTap: () {
                        Navigator.push(
                          context,
                          MaterialPageRoute(
                            builder: (context) =>
                                ProductDetailPage(product: product),
                          ),
                        );
                      },
                      child: Container(
                        margin: const EdgeInsets.symmetric(
                            horizontal: 16, vertical: 12),
                        padding: const EdgeInsets.all(20.0),
                        child: Column(
                          mainAxisAlignment: MainAxisAlignment.start,
                          crossAxisAlignment: CrossAxisAlignment.start,
                          children: [
                            Text(
                              "${snapshot.data![index].fields.name}",
                              style: const TextStyle(
                                fontSize: 18.0,
                                fontWeight: FontWeight.bold,
                              ),
                            ),
                            const SizedBox(height: 10),
                            Text("Rp ${snapshot.data![index].fields.price}"),
                            const SizedBox(height: 10),
                            Text("${snapshot.data![index].fields.size}"),
                            const SizedBox(height: 10),
                            Text("${snapshot.data![index].fields.description}")
                          ],
                        ),
                      ),
                    );
                  });
            }
          }
        },
      ),
    );
  }
}
```

- Membuat halaman detail untuk setiap item yang terdapat pada halaman daftar Item.
Dengan membuat halaman yang menampilka seluruh detail pada Product dan menambahkan gesture detector pada tiap product di productlist untuk meredirect ke halaman detail

 - Melakukan filter pada halaman daftar item dengan hanya menampilkan item yang terasosiasi dengan pengguna yang login.
Dengan menggunakan cookies untuk hanya mengambil data produk yang diasosiasikan terhadap user tersebut

**1. Jelaskan mengapa kita perlu membuat model untuk melakukan pengambilan ataupun pengiriman data JSON? Apakah akan terjadi error jika kita tidak membuat model terlebih dahulu?**  
Karena kita harus memastikan bahwa struktur data yang dikirim dan yang diterima sesuai dan dengan menggunakan json,  kita dapat melakukan manajemen data lebih mudah dan model dapat memberikan error jika terdapat struktur data yang tidak sesuai.
 
**2. Jelaskan fungsi dari library http yang sudah kamu implementasikan pada tugas ini**  
Library http yang diimplementasikan dalam tugas ini berfungsi untuk melakukan request http, mengirim data dalam bentuk JSON dan mengambil data dari server yang kemudian diparse agar dapat digunakan di dalam flutter
 
**3. Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.**  
Fungsi dari CookieRequest digunakan untuk menangani request HTTP sambil menyimpan dan mengelola cookie autentikasi, sehingga memungkinkan server django mengenali request yang telah diautentikasi tanpa hharus mengirim ulang token pengguna
 
**4. Jelaskan mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter.**  
Pengiriman data dimulai dari page ProductForm pada projek flutter yang kemudian mengirimkan model data dalam bentuk json menggunakan request HTTP Post. Kemudian django menerima data tersebut dalam fungsi tersendiri yang menambahkan data tersebut ke dalam database.  
Untuk proses tampilan data dimulai dari mengambil data json yang terdapat pada host lalu diparse menjadi model dart yang kemudian ditampilkan pada page ProductEntryPage
 
**5. Jelaskan mekanisme autentikasi dari login, register, hingga logout. Mulai dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.**  
Autentikasi mulai dari memasukkan data register atau login berupa username dan username pada flutter yang kemudian mengirimkan request post ke django yang kemudian memvalidasikan data tersebut jika pengguna memang ada di database untuk login atau memeriksa apakah data untuk register valid, jika login berhasil flutter menyimpan cookie autentikasi tersebut.  
Ketika pengguna ingin logout flutter akan mengirimkan request post ke auth/logout dan menghapus sesi login.

 
