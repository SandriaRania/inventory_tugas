Tugas 7: 

1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter? \
Jawaban: Dalam flutter, widget stateful adalah widget dinamis yang bisa berubah, sebagai contoh dengan interaksi user suatu widget memunculkan teks, sedangkan widget stateless adalah widget yang sama sekali tidak berubah. \
Sumber: https://docs.flutter.dev/ui/interactivity#:~:text=to%20Managing%20state.-,Stateful%20and%20stateless%20widgets,are%20examples%20of%20stateless%20widgets. \

2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing. \
Jawaban: \
Widget MyApp sebagai basis dari seluruh aplikasi di tugas 7.
Widget Shopcard berfungsi untuk menyimpan objek card-card.
Widget MyHomePage berfungsi sebagai basis tampilan homepage.

3. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
Pertama, saya menginstall Flutter lalu membuat aplikasi baru bernama inventory_tugas, lalu dalam folder lib, saya membuat file baru menu.dart . Saya memindah class MyHomePage dan _MyHomePageState dari main.dart ke menumdart, lalu menambahkan import package agar main.dart terhubung dengan menu.dart .

Selanjutnya di menu.dart saya mengubah MyHomePage menjadi stateless dengan merubah key dan StatefulWidget menjadi StatelessWidget. Selanjutnya, di luar class MyHomePage saya membuat class ShopCard sebagai basis card-card yang akan pakai, saat class telah dibuat baru saya menambah items yang diinginkan di dalam class MyHomePage, dan menambah properti-peopertinya seperti size dan color. Saat selesai, saya menjalankan programnya dengan menggunakan command flutter run. 
