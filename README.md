Tugas 8: 

1. Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat! \
Jawaban: Navigator.push() menambah rute baru yang akan ditampilkan di halaman paling atas pengguna, sedangkan Navigator.pushReplacement() akan menghapus rute yang sedang ditampilkan dan diganti dengan rute baru. \
if (item.name == "Tambah Produk") { \
        Navigator.push(context, \
            MaterialPageRoute(builder: (context) => const ShopFormPage())); \
    } \
Dalam contoh ini, Navigator.push menampilkan ShopFormPage di atas halaman awalnya. Jika diimplementasikan tombol Back, maka ketika ditekan, kita akan kembali ke halaman awal. \
onTap: () { \
        Navigator.pushReplacement( \
        context, \
        MaterialPageRoute( \
            builder: (context) => MyHomePage(), \
        )); \
    }, \
Dalam contoh ini, Navigator.pushReplacement langsung merubah tampilan kita menjadi MyHomePage. Jika diimplementasikan tombol Back, maka jika tombol tersebut ditekan, dan tidak ada page lagi di stack, maka kita akan keluar dari aplikasi.

2. Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing! \
Jawaban: \
•Container: merubah tampilan child widget seperti padding, margin, border, dan background milik child. \
•Row: mengatur child widgetnya dalam urutan horizontal baris. \
•Column: mengatur child widgetnya dalam urutan vertikal kolom. \
•Stack: membentuk 'stack' antara child widgetnya yang ditumpuk satu sama lain. \
•GridView: mengatur child widgetnya dalam format 2D grid. \
•ListView: mengatur child widgetnya dalam format list yang bisa discroll secara horizontal atau vertikal. \
•Expanded: mengatur space kosong di antara child widgetnya. \
Sumber: https://www.educative.io/answers/layouts-in-flutter

3. Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut! \
Jawaban: Elemen input Form yang digunakan adalah TextFormField yang digunakan untuk mengisi input dan TextButton yang digunakan untuk men-submit isi form data tersebut.

4. Bagaimana penerapan clean architecture pada aplikasi Flutter? \
Jawaban: Secara umum, clean architecture terbagi menjadi Presentation Layer(UI), Domain Layer(Business Logic), dan Data Layer. Setiap layer tersebut memiliki aturan tertentu, sebagai contoh Presentation dan Domain Layer tergantung Domain Layer, namun Domain Layer tidak tergantung pada layer lainnya. Clean architecture membantu para developer membedakan masing-masing layer dengan isi mereka satu sama lain. \

5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial) \
Jawaban: Pertama saya membuat shoplistformpage yang akan diisi form data untuk menambah item dengan tiga properti yaitu name, amount, dan description. Input form diimplementasikan dengan textformfield untuk mengisi barangnya dan textbutton untuk di submit. Selanjutnya saya membuat leftdrawer sebagai navigasi penghubung antara shoplistformpage dan halaman utama myhomepage. Namun, kita juga tetap bisa mengakses shoplistformpage dengan menggunakan shopcard tambah item. Kita menggunakan Navigator push untuk pindah ke shoplistformpage. Terakhir, saya memindah shoplistform dan menu.dart ke sebuah folder baru bernama screens agar terpisah antara widgets, tampilan, dan main.dart basis aplikasi.

Tugas 7: 

1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter? \
Jawaban: Dalam flutter, widget stateful adalah widget dinamis yang bisa berubah, sebagai contoh dengan interaksi user suatu widget memunculkan teks, sedangkan widget stateless adalah widget yang sama sekali tidak berubah. \
Sumber: https://docs.flutter.dev/ui/interactivity#:~:text=to%20Managing%20state.-,Stateful%20and%20stateless%20widgets,are%20examples%20of%20stateless%20widgets. \

2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing. \
Jawaban: \
Widget MyApp sebagai basis dari seluruh aplikasi di tugas 7.
Widget Shopcard berfungsi untuk menyimpan objek card-card.
Widget MyHomePage berfungsi sebagai basis tampilan homepage.

3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial) \
Jawaban: \
Pertama, saya menginstall Flutter lalu membuat aplikasi baru bernama inventory_tugas, lalu dalam folder lib, saya membuat file baru menu.dart . Saya memindah class MyHomePage dan _MyHomePageState dari main.dart ke menumdart, lalu menambahkan import package agar main.dart terhubung dengan menu.dart .

Selanjutnya di menu.dart saya mengubah MyHomePage menjadi stateless dengan merubah key dan StatefulWidget menjadi StatelessWidget. Selanjutnya, di luar class MyHomePage saya membuat class ShopCard sebagai basis card-card yang akan pakai, saat class telah dibuat baru saya menambah items yang diinginkan di dalam class MyHomePage, dan menambah properti-peopertinya seperti size dan color. Saat selesai, saya menjalankan programnya dengan menggunakan command flutter run. 
