---
name: Grove Inventor Kit for micro:bit
category: Tutorial
bzurl:  https://www.seeedstudio.com/Grove-Inventor-Kit-for-micro%3Abit-p-2891.html
oldwikiname: Grove_Inventor_Kit_for_micro:bit
prodimagename: https://statics3.seeedstudio.com/seeed/file/2017-06/bazaar492598_8.jpg
surveyurl: https://www.research.net/r/Grove_Inventor_Kit_for_microbit
sku:    110060762
---
![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/zoro_im_kitbox.jpg)

BBC micro:bit adalah komputer kecil seukuran saku yang dapat dengan mudah mewujudkan kreativitas Anda tanpa banyak pengetahuan tentang kelistrikan dan pemrograman. Terdapat banyak kreasi yang bisa Anda gali dengan menggunakan micro:bit mulai dari robot hingga alat musik. Namun jika Anda ingin membuat lebih banyak hal, rasanya tidak cukup hanya dengan 1 microbit saja. Itulah sebabnya kami memperkenalkan Grove Inventor Kit for micro:bit kepada Anda.

The Grove Inventor Kit for Micro:bit memungkinan untuk membuat kreasi yang bermacam-macam menggunakan Micro:bit. Board utama dalam kit ini adalah Grove shield for micro:bit. Selain itu, Anda juga dapat menggunakan banyak modul Grove termasuk sensor, display, dan aktuator untuk berinteraksi dengan Micro:bit. Jika Anda tidak pernah menggunakan dan tidak tahu apa itu Grove, inilah panduan pengenalan Grove. Yang perlu Anda ketahui adalah bahwa dengan Grove, anda tidak perlu lagi menyolder atau jumper kabel lagi. Pembuatan prototipe Anda akan lebih mudah dan lebih nyaman.

Kami telah menyiapkan 8 modul grove untuk Anda untuk memulai menggunakan micro:bit. Dengan modul grove ini, Anda dapat mengukur jarak dan menampilkan nilai jaraknya, menggunakan gerakan untuk memainkan musik yang berbeda, atau membuat penjaga cerdas untuk meja atau ruangan Anda. Kami telah menyiapkan semua library(paket) yang diperlukan untuk diunduh gratis. Jika Anda seorang pemula dalam penggunaan micro:bit, jangan khawatir karena kami juga menyiapkan 12 proyek berbeda yang dapat mengajarkan Anda langkah demi langkah. Jika Anda adalah pengguna tingkat lanjut, kit ini akan membantu Anda dalam membuat lebih banyak proyek kreatif dibanding lainnya.


!!!Catatan

    - Tegangan keluaran micro:bit sekitar 3.0V, menggunakan microbit atau baterai AA untuk memberi daya pada rangkaian dapat menyebabkan kegagalan fungsi modul Grove yang memerlukan tegangan input tinggi (mis. Grove - Ultrasonic Ranger). Untuk membuat Grove ini berfungsi dengan baik, gunakanlah port micro-USB pada Grove shield microbit untuk memberi daya pada rangkaian.




[![](https://github.com/SeeedDocument/Seeed-WiKi/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png)](https://www.seeedstudio.com/Grove-Inventor-Kit-for-micro%3Abit-p-2891.html)

##  Fitur

  - extension shield dengan periferal yang banyak dan mudah digunakan;
  - 10 modul Grove yang dipilih dengan baik untuk bekerja dengan micro:bit;
  - 12 proyek luar biasa untuk memungkinkan Anda memulai dengan cepat;
  -  Dokumentasi yang baik

##  Ikhtisar Perangkat Keras


![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/first_im.jpg)

###  **Daftar Komponen**
| Nama Komponen | Jumlah |
|--------------------------|-----|
|Grove Shield for micro:bit|  1  |
|Grove - Rotary Angle Sensor(P)| 1 |
|Grove - Speaker | 1 |
|Grove - Ultrasonic Ranger| 1 |
|Grove - Light Sensor v1.2| 1 |
|Grove - WS2812 Waterproof LED Strip - 30 LEDs 1 meter| 1 |
|Grove - Gesture | 1 |
|Grove - 4-Digit Display| 1 |
|Grove - Red LED| 1 |
|Micro USB Cable - 48cm| 1 |
|12 Projects Manual| 1 |
|Kabel Capit Buaya| 10 |
|Kabel Grove| 7 |


##  Memulai

###  Dasar-Dasar Micro:bit

Anda perlu mengetahui beberapa pengetahuan penting jika ini adalah pertama kalinya Anda mengoperasikan Micro:bit. Anda dapat mengklik [ **disini** ](https://microbit.org/code/) untuk mengetahui lebih banyak tentang Micro:bit.

Micro:bit menawarkan dua jenis editor - Editor Blok JavaScript dan Editor Python. JavaScript Block Editor mendukung pemrograman grafis dan mudah dipelajari. Jadi Panduan ini didasarkan pada Editor Blok JavaScript.

Berikut adalah dua langkah sederhana sebelum Anda menikmati kit kami, setelah itu kita dapat memulai program.

####  Langkah 1.Membuka Editor

Silahkan klik untuk membuka **[JavaScript Block Editor](https://makecode.microbit.org/)** , dan Anda akan melihat web pemrograman grafis.


####  Langkah 2.Tambahkan Grove Package
  - Klik gambar gear di sudut kanan atas > pilih **Add Package**

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/0-1.png)

  - Masukan URL proyek **github.com/seeed-studio/pxt-grove**

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/0-2.png)

  - Sekarang anda dapat menemukan **Grove** di toolbar.

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/0-3.png)

### Demo 1. Gesture Recognition

Sensor gestur dapat mengenali 9 gestur berbeda, dalam demo ini, Anda akan belajar cara menampilkan nama gestur yang dikenali pada micro:bit.


#### Daftar Komponen

|Nama Komponen|Jumlah|
|---|---|
|Grove - Gesture|1|
|Grove Shield for micro:bit|1|
|micro:bit|1|
|Grove Universal 4 pin cable|1|
|Micro-USB cable|1|

#### Koneksi

  - Colokkan **micro:bit** ke **Grove Shield for micro:bit**.
  - Hubungkan Grove-Gesture ke port **I2C** micro:bit melalui Grove Universal 4 pin cable.
  - Hubungkan micro:bit ke PC menggunakan kabel Micro-USB.

!!!Peringatan

      -harap pastikan LED Array menghadap ke atas saat Anda mencolokkan micro:bit, atau Anda dapat merusak board.


![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/Gesture%20Recognition.png)


#### Perangkat Lunak
  - Langkah 1:

  Tambahkan Gesture Block

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/1-1.png)

  - Langkah 2:

  Pilih Right, sehingga sensor dapat mengenali kapan Anda menggerakkan tangan Anda dari kanan ke kiri.

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/1-2.png)

  - Langkah 3:

  Tambahkan Basic block **show string** dan masukkan ke dalam Gesture block. Lalu klik dua kali pada tulisan "Hello!", lalu ubah menjadi "Right".

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/1-3.png)

  - Langkah 4:

  Tambahkan "Left" dan "Clockwise" dengan cara yang sama, dan masukkan **show icon** ke dalam "Clockwise".

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/1-4.png)

  - Langkah 5:

  Ketika Anda menyelesaikan semua langkah di atas, ganti nama proyek menjadi "gesture". Kemudian Anda dapat mengunduh proyek ke board Anda. Klik **Download** di sudut kiri bawah, unduh file **microbit-gesture.hex** ke dalam flash pada MICROBIT.


  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/1-5.png)

  Sekarang kerjakan proyek anda.

!!!Tips
    - Anda dapat menemukan blok berdasarkan warna. Misalnya, jika Anda tidak mengetahui dimana **show icon** , karena warnanya biru dan Module **Basic** berwarna biru, Anda dapat menemukannya disekitar module **Basic**  tersebut. Sederhana dan efektif, bukan?
    


### Demo 2. Ultrasonic Meter

Dalam demo ini, Anda akan belajar cara menggunakan sensor ultrasonik untuk mengukur jarak dan menunjukkan nilai pada tampilan.

#### Daftar Komponen
|Nama Komponen|Jumlah|
|---|---|
|Grove - Ultrasonic Ranger|1|
|Grove - 4-Digit Display|1|
|Grove Shield for micro:bit|1|
|micro:bit|1|
|Grove Universal 4 pin cable|2|
|Micro-USB cable|1|

#### Koneksi

  - Colokkan **micro:bit** ke **Grove Shield for micro:bit**.

!!!Peringatan harap pastikan LED Array menghadap ke atas saat Anda mencolokkan micro:bit, atau Anda dapat merusak board.

  - Hubungkan Grove - Ultrasonic Ranger ke port **P0/P14** Pada micro:bit melalui Grove Universal 4 pin cable.
  - Hubungkan Grove- 4-Digit Display ke port **P1/P15** Pada micro:bit melalui Grove Universal 4 pin cable.
  - Hubungkan micro:bit ke PC menggunakan kabel Micro-USB.

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/Ultrasonic_Meter.png)

#### Software (Perangkat Lunak)

  - Langkah 1:

  Tambahkan basic block **on start**, lalu tambahkan blok variabel  **set item to 0**, ganti variabel ‘items’ menjadi ‘Display’. Jika Anda telah berhasil menambahkan  Grove package, ganti "0" dengan Grove block 4-Digit Display di P1 dan P15.

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/2-1.png)

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/2-2.png)

  - Langkah 2:

  Tambahkan basic block forever, lalu tambahkan Grove block item show number 0, ganti nama ‘item’ menjadi ‘Display’, ganti ‘0’ dengan Grove block Ultrasonic Sensor (dalam cm) di P0.

  - Langkah 3:

  Tambahkan basic block pause (ms) (100).

  ![](https://github.com/SeeedDocument/Grove_kit_for_microbit/raw/master/img/2-3.png)

  - Langkah 4:

  Ganti nama Proyek "Ultrasonic Meter", download (unduh) dan mainkan.


## Sumber

  [**Grove Inventor Kit for micro:bit User Manual**](https://github.com/SeeedDocument/Grove_kit_for_microbit/blob/master/res/Guide-Grove%20kit%20for%20microbit.pdf)

  [**micro:bit Getting Started Videos**](http://microbit.org/start/)

  [**About micro:bit**](http://microbit.org/about/)

  [**micro:bit Hardware**](http://microbit.org/guide/hardware/)

  [**micro:bit Apps**](http://microbit.org/code/)

  [**Grove Shield for microbit_eagle file.zip**](https://github.com/SeeedDocument/Bazzar_Attachment/raw/master/103030195/202001587_Grove%20Shield%20for%20BBC%20microbit%20V1.2_eagle%20file.zip)

## Bantuan / Tech Support
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>