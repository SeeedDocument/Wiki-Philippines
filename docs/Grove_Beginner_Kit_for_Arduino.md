---
name: Grove Beginner Kit for Arduino
category: Others
bzurl:  
oldwikiname:  
prodimagename:
surveyurl: 
sku: 110020171
---


## SISTEM GROVE

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/pack.jpg)

Grove merupakan sistem prototip berbentuk modul yang terdiri dari base unit dan berbagai macam modul tambahan yang dilengkapi dengan konektor standar. Base unit merupakan mikroprosesor seperti pada umumnya yang memungkinkan untuk menghubungkan, memproses, dan mengontrol input maupun output dari modul Grove. Setiap modul Grove mempunyai satu fungsi utama, mulai dari tombol sederhana hingga sistem yang lebih kompleks seperti sensor detak jantung. Konektor standar Grove yang dirancang memungkinkan pengguna menjadi lebih mudah dalam merakit atau membongkar modul jika dibandingkan dengan menggunakan kabel atau solder. Hal tersebut membuat sistem pembelajaran pada saat bereksperimen, pengembangan sistem, maupun merancang prototip menggunakan Grove menjadi lebih sederhana.
Grove juga menyediakan Grove to Pin Header Converter atau Grove Base HAT yang dapat digunakan bagi para pengguna yang ingin menggunakan modul sensor dan aktuator milik Grove tanpa disertai development board milik Grove.

![Grove header](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/grove-wire.jpg)![Grove connector](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connector.png)![Grove-jumper wire](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/jumperwire.png)

Pengguna sistem Grove setidaknya perlu memiliki beberapa pengetahuan elektronika dasar. Jika tidak, pengguna harus mengikuti panduan dasar ini untuk mempelajari beberapa operasi dasar pada sistem Grove. Bagian pertama dari panduan ini terdiri dari daftar informasi dasar tentang komponen yang terdapat dalam starter kit, kemudian diikuti dengan pengaturan dasar Arduino IDE untuk Seeeduino Lotus. Selain itu, terdapat pula 11 sesi panduan berisi operasi dasar pada masing-masing komponen dalam starter kit dan aplikasi yang menggabungkan beberapa modul secara bersamaan. Hal tersebut dapat memberikan pengguna beberapa wawasan dan pengetahuan dasar tentang cara menghubungkan dan memprogram sistem Grove.

## KIT GROVE BASE UNTUK ARDUINO


Grove Beginner Kit untuk Arduino berisi satu Development Board Seeeduino Lotus V1.1 (Kompatibel dengan Arduino) dan 8 buah modul. Informasi terperinci tercantum pada penjelasan di bawah ini.

### Development Board

#### Seeeduino Lotus V1.1

Seeeduino Lotus adalah development board dengan mikrokontroler AVR ATMEGA328 tertanam di dalamnya, Seeeduino Lotus merupakan kombinasi dari Seeeduino dan Grove Base Shield. Seeduino Lotus menggunakan mikrokontroler Atmel ATmega328-MU dan chip CP2102N. ATmega328-MU adalah mikrokontroler AVR 8-bit berdaya rendah namun memiliki performa yang tinggi, sedangkan CP2102N adalah chip konverter USB to Serial yang memungkinkan Anda untuk menghubungkan Seeeduino Lotus dengan komputer menggunakan kabel mikro USB. Seeeduino Lotus memiliki 14 input/output Digital (6 dapat digunakan sebagai output PWM) dan 7 Input/output analog, konektor micro USB, header ICSP, 12 konektor Grove, dan tombol reset.


**Fitur**

- Kompatibel penuh dengan Arduino UNO
- Mikrokontroler ATmega328
- 2 konektor Grove on-board
- 14 Pin I/O Digital (6 output PWM)
- 6 Input Analog
- ISP Header
- Kompatibel dengan Shield Arduino UNO-R3
- Pemrograman dan sumber daya melalui mikro USB
- Tegangan kerja 5V
- Mendukung Windows, Mac OS dan Linux

**Hardware (Perangkat Keras)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/pinout.png)

LED-D13: LED terhubung ke pin D13 yang terdapat pada board. LED-D13 ini dapat digunakan sebagai indikator LED on-board untuk program/sketsa.

USB Input: Port USB digunakan untuk menghubungkan board ke PC Anda untuk memberi daya pada board dan sebagai pemrograman. Kabel Micro-USB adalah jenis port USB yang sangat umum, dapat ditemukan pada sebagian besar ponsel Android, dan perangkat lainnya. Anda mungkin memiliki lusinan kabel yang tergeletak di rumah Anda.

Reset : Tombol ini diletakkan pada pinggir board untuk memungkinkan Anda me-reset board Seeeduino bahkan ketika shield dipasang pada board, sedangkan tombol pada board Arduino lainnya ditempatkan di atas yang membuatnya sulit dijangkau ketika shield terpasang.

Power Pins, Analog Pins & Digital Pins: Header tambahan ini tersedia ketika Anda ingin menghubungkan konektor sensor dan aktuator lain yang bukan grove, terutama header daya digunakan ketika Anda ingin memberi daya pada lebih banyak sensor/perangkat.

Grove Connectors: Seeed Studio memiliki beragam sensor/perangkat yang dapat menggunakan koneksi Analog, Digital, I2C, dan koneksi UART. Selain itu, kami menjual konektor Grove independen untuk membantu Anda membuat sambungan sensor Anda sendiri.

ICSP: Ini adalah koneksi ICSP untuk ATmega328P, terletak di posisi ICSP/SPI standar untuk perangkat yang kompatibel dengan Arduino Uno, Due, Mega, dan Leonardo. Pin SPI di port ini: MISO, SCK, dan MOSI, masing-masing juga terhubung ke pin digital 12, 13, dan 11 seperti pada Arduino Uno.

USB 2 Uart: Pinout dari USB-2-Uart. Pad ini dapat digunakan untuk berinteraksi dengan perangkat UART lain dengan cara mengatur ATmega328 pada mode reset. Pad ini membuat Seeeduino Lotus dapat digunakan sebagai board USB2UART.

**Arduino UNO vs Seeeduino Lotus**

|                        | Seeeduino Lotus V1.1 | Arduino Uno R3 |
|:----------------------:|:--------------------:|:--------------:|
|      Tanggal Rilis     |        03/2018       |     02/2016    |
|     Mikrokontroler   |      ATMega328P      |   ATMega328P   |
|    Tegangan kerja  |          5V          |       5V       |
|          Flash         |         32KB         |      32KB      |
|          SRAM          |          2KB         |       2KB      |
|         EEPROM         |          1KB         |       1KB      |
| Antarmuka Sumber Daya |       Micro USB      |  USB, Port DC  |
|    Konektor Grove  |          12          |      None      |

#### Sensor 

**[Grove - Buzzer](https://www.seeedstudio.com/Grove-Buzzer-p-768.html)**


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/buzzer.jpg)

Modul ini menggunakan piezo buzzer sebagai komponen utama, modul ini dapat menghasilkan nada nada tinggi saat modul terhubung ke output digital dan pada saat level logika diatur ke High. Jika tidak, modul dapat menghasilkan berbagai nada sesuai dengan frekuensi yang dihasilkan dari output PWM Analog yang terhubung dengannya. (catatan: rentang frekuensi yang dapat dibedakan oleh telinga manusia normal adalah antara 20Hz dan 20kHz.)

**[Grove - Tilt Switch](https://www.seeedstudio.com/Grove-Tilt-Switch-p-771.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/Tilt.jpg)

Grove-Tilt Switch setara dengan tombol yang dapat digunakan sebagai input digital. Di dalam Tilt Switch terdapat sepasang bola yang melakukan kontak dengan pin ketika case-nya tegak. Miringkan case dan bola tidak menyentuh, sehingga tidak terjadi kontak. Kontak pin tersebut disambung ke jalur SIG, NC tidak digunakan pada modul Grove ini.

**[Grove - Chainable RGB LED](https://www.seeedstudio.com/Grove-Chainable-RGB-Led-V2-0-p-2903.html)**


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/Grove-Chainable_RGB_LED_V2.0.jpg)

Grove - Chainable RGB LED didasarkan pada chip P9813 yang merupakan driver LED penuh warna. Modul ini menyediakan 3 driver arus konstan serta output termodulasi dari 256 warna abu-abu. Modul ini berkomunikasi dengan Mikrokontroler menggunakan transmisi 2-kawat (Data dan Clock). Transmisi 2-kawat ini dapat digunakan untuk menyambungkan modul Grove - Chainable RGB LED tambahan. Regenerasi Clock internal meningkatkan jarak transmisi. Modul Grove ini cocok untuk proyek berbasis LED yang berwarna-warni. 

**[Grove - Light Sensor](https://www.seeedstudio.com/Grove-Light-Sensor-v1-2-p-2727.html)**


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/lightsensor.jpg)

Grove - Light sensor dalam modul ini memafaatkan foto-resistor (resistor bergantung cahaya) untuk mendeteksi intensitas cahaya. Nilai Hambatan foto-resistor berkurang ketika intensitas cahaya meningkat. Chip Dual opAmp LM358 pada board ini menghasilkan tegangan yang sesuai dengan intensitas cahaya (mis. Berdasarkan nilai hambatan). Sinyal outputnya adalah nilai analog, dengan kondisi semakin terang cahayanya, maka semakin besar nilai tegangan analognya.

**[Grove - Line Finder](https://www.seeedstudio.com/Grove-Line-Finder-v1-1-p-2712.html)**


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/linefinder.jpg)

Grove-Line finder dirancang untuk robot yang mengikuti garis/line-following robot. Modul ini memiliki LED pemancar IR dan phototransistor sensitif IR. Modul dapat menampilkan sinyal digital ke mikrokontroler sehingga robot dapat mengikuti garis hitam pada latar belakang putih, ataupun sebaliknya.

**[Grove - LCD RGB Backlight](https://www.seeedstudio.com/Grove-LCD-RGB-Backlight-p-1643.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/LCD.jpg)

Modul Grove-LCD RGB Backlight ini adalah layar LCD 16 Karakter sebanyak 2 baris yang menggunakan antarmuka bus I2C untuk berkomunikasi dengan Board pengembangan. Hal ini akan mengurangi pin header dari 10 menjadi 2 yang sangat nyaman untuk sistem Grove. Modul layar LCD ini juga mendukung karakter khusus, Anda dapat membuat dan menampilkan simbol hati atau stick-man pada modul LCD ini melalui kode program sederhana.

**[Grove - Temperature & Humidity Sensor(DHT11)](https://www.seeedstudio.com/Grove-Temperature-Humidity-Sensor-DHT1-p-745.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/DHT11.jpg)

Temperature & Humidity Sensor menghasilkan output digital pre-kalibrasi. Elemen sensor kapasitif digunakan untuk mengukur kelembaban dan thermistor negative temperature coefficient (NTC) digunakan untuk mengukur suhu. Alat ini memiliki keandalan yang sangat baik dan stabilitas yang baik untuk jangka panjang. Perlu diketahui bahwa sensor ini tidak akan berfungsi untuk suhu di bawah 0 derajat.

**[Grove - 3-Axis Digital Accelerometer](https://www.seeedstudio.com/Grove-3-Axis-Digital-Accelerometer-1-5-p-765.html)**
 

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/3_axis_cover.jpg)

3-Axis Digital Accelerometer adalah bagian penting dalam proyek-proyek seperti deteksi orientasi, deteksi gestur dan deteksi gerak. 3-Axis Digital Accelerometer (± 1.5g) ini didasarkan pada modul konsumsi daya rendah milik Freescale yaitu MMA7660FC. Sensor ini memiliki fitur tahan guncangan yang tinggi hingga 10.000g dan pembacaan sensor yang dapat diakses per detiknya. Untuk aplikasi yang tidak memerlukan rentang pengukuran terlalu besar, modul ini adalah pilihan yang bagus karena tahan lama, hemat energi, dan hemat biaya.

## PERSIAPAN AWAL 

### Persyaratan Minimum

- Grove starter kit
- Kabel micro USB
- Komputer dengan Arduino IDE

### Panduan Dasar 

#### Pengaturan Dasar Arduino IDE

**Langkah 1.** Pasang USB to Serial driver untuk Seeeduino Lotus V1.1

Seeeduino lotus Versi 1.1 dan versi diatasnya mengadaptasi dari chip  CP2102N USB to serial. Seeeduino lotus Versi 1.1 menambahkan dukungan untuk sistem operasi pada Windows, MacOS dan Linux, download (unduh) dan pasang driver yang relevan untuk sistem operasi Anda.
Download links:
Situs Resmi: [CP210x USB to UART Bridge VCP Drivers](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/logo.jpg)

**Instalasi driver**

Windows:

Ekstrak/unzip file driver yang telah di-download (unduh), buka file yang diekstrak dan pilih driver yang relevan sesuai dengan bit sistem operasi Anda, dalam hal ini kami memilih 64bit, pengguna OS 32bit harus memilih file _x86 dan ikuti petunjuk instalasinya.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/win1.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/win2.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/win3.png)

Mac OS:

Klik dua kali file “Silicon Labs VCP Driver.pkg”, dan ikuti panduan pengaturan untuk menginstal.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/mac1.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/mac2.png)

**Langkah 2.** Download (unduh) dan instal (pasang) [Arduino IDE](https://www.arduino.cc/en/Main/Software)

Download (unduh) dan instal (pasang) Arduino IDE sesuai dengan sistem operasi Anda.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard.png)

<b id="step3">Langkah 3.</b> Tambahkan library untuk Seeeduino Lotus

- Buka Arduino | Preferences, dari menu preferences kemudian cari Additional Boards Manager URLS, salin & tempel URL Library ke dalam kotak teks, lalu tekan ok.
Library URL:	https://raw.githubusercontent.com/Seeed-Studio/Seeed_Platform/master/package_seeeduino_boards_index.json

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard1.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard2.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard3.png)

- Buka Tools | Board: | Boards Manager, cari Seeeduino AVR dan klik install untuk memasang library Seeeduino AVR. Anda tidak dapat melihat AVR Seeeduino yang tercantum di jendela Boards Manager, harap ulangi langkah pertama dan pastikan URL yang Anda masukkan sudah benar.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard4.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard5.png)

- Buka Tools | Board: pada pilihan selanjutnya Anda akan menemukan pilihan Seeeduino AVR Board seperti yang ditunjukkan, lalu pilih board yang benar sesuai dengan board yang Anda gunakan, pada panduan ini kita harus memilih Seeeduino Lotus.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard6.png)
	
**Langkah 4.** Hubungkan Seeeduino Lotus

Harap sambungkan Seeeduino Lotus dengan komputer menggunakan kabel Micro-USB. Setelah itu, LED hijau untuk daya pada lotus Seeeduino akan menyala.


![with micro-USB](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/usb.jpg)

**Langkah 5.** Mengatur IDE untuk Seeeduino Lotus

Ikuti langkah-langkah seperti yang ditunjukkan sebelumnya, pilih "Seeeduino Lotus" di bawah Boards Manager.

Pilih perangkat serial board Arduino dari Tools | Serial Port menu. Untuk mengetahui perangkat serial yang benar, Anda dapat memutuskan koneksi board Arduino Anda dan membuka kembali menu; entri yang hilang harusnya merupakan board Arduino. Sambungkan kembali board dan pilih port serial tersebut. Entri yang Anda pilih harus berisi "SLAB_USB".

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard07.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard7.png)


Set “Tools | Programmer” sebagai “AVR ISP”.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard8.png)


### Demo Blink

Setelah semua pengaturan dasar Arduino IDE selesai, sekarang kita dapat menguji kode demo blink pada board pengembangan Seeeduino Lotus. Catatan: Anda harus menyelesaikan langkah-langkah di atas untuk melanjutkan yang berikut ini.

**Pilih Blink Demo Dari Menu**

Pilih File | Examples | 01 Basics | Blink dari menu, contoh kode blink akan muncul di jendela baru.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard9.png)


**Unggah Kode / Unggah code**

Harap pastikan Board, Port, dan Programmer yang dipilih telah benar melalui menu tools.
Sekarang kita dapat mengunggah kode ke board dev Lotus dengan menekan ikon panah kanan di sudut kiri atas IDE.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard10.png)

Setelah kode berhasil diunggah, maka teks “avrdude done. Thank you.” akan muncul di jendela log IDE.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard11.png)

Sekarang Anda akan melihat LED bawaan berkedip dalam interval satu detik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/blink.jpg)


**Penjelasan kode blink**

void setup () adalah fungsi pengaturan hanya berjalan satu kali ketika Anda menekan reset atau menyalakan board.

```C

void setup() {
}

```

inisialisasi pin digital LED_BUILTIN sebagai output.

```C

pinMode(LED_BUILTIN, OUTPUT);

```

void loop () adalah fungsi loop berulang-ulang selamanya.


```C

void loop() {
}

```

digitalWrite () adalah untuk mengatur pin LED_BUILTIN sebagai level tegangan HIGH, yang berarti menyalakan LED. Demikian pula untuk mematikan LED, setel level tegangan ke LOW dengan mengubah kode HIGH menjadi LOW.

```C

digitalWrite(LED_BUILTIN, HIGH);
digitalWrite(LED_BUILTIN, LOW);

```

delay () berarti menjeda sementara program, angka di dalam kurung berarti jumlah waktu (dalam milidetik) untuk jeda (delay).

```C

delay(1000);

```




## Sesi Panduan Grove Starter Kit 10


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/kit.jpg)

### Tujuan

Bagian ini terdiri dari 10 panduan, panduan dapat dibagi menjadi dua bagian, 8 sesi pertama memperkenalkan operasi dasar setiap modul individu dari kit starter ini, dan 2 sesi terakhir menggunakan contoh kasus untuk menunjukkan bagaimana modul dapat dikombinasikan dan diterapkan dalam aplikasi kehidupan nyata.


### Prasyarat

Pengetahuan mendasar tentang pengoperasian Seeeduino Lotus dengan Arduino IDE dan keterampilan pemrograman sangat penting dalam mengikuti panduan ini. Karena itu, pastikan Anda telah menyelesaikan panduan pengaturan dasar di atas dan berhasil memasang USB to Serial driver pada sistem operasi Anda untuk Seeeduino Lotus, menyelesaikan demo LED Blink dan memastikannya sepenuhnya bekerja dengan board Seeeduino Lotus.

### Hasil belajar

- Mampu mengoperasikan Arduino IDE untuk menulis kode untuk Seeeduino Lotus V1.1 untuk menggerakkan modul dari Grove Starter Kit.
- Mampu mengidentifikasi jenis modul yang termasuk dalam Kit ini dan aplikasinya.
- Mampu mendemonstrasikan setiap komponen Grove Starter Kit dan memanfaatkan modul yang relevan untuk proyek Anda sendiri setelah panduan ini

### Sesi 1: Grove - Buzzer


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/buzzer.jpg)

**Tujuan**	

Menggunakan Buzzer untuk menghasilkan suara dan juga mengatur frekuensi tertentu untuk menghasilkan beberapa nada.

**Inti Pengetahuan**

- Modul Buzzer adalah aktuator.
- Menggunakan sinyal digital untuk membuat suara dengung
- Menghasilkan nada tertentu dengan mengatur frekuensi yang sesuai
- Gunakan fungsi tone(pin, frequency, duration) untuk membuat buzzer memutar musik
- Pelajari cara menggunakan "for loop" pada Arduino IDE


**Persyaratan hardware (perangkat keras)**

Persiapan

- Kabel micro-USB
- Komputer yang dilengkapi dengan software Arduino IDE dan driver serial-to-USB yang sudah terpasang


Included in the kit

- Board Dev Seeeduino Lotus V1.1
- Kabel Grove
- Modul Grove – Buzzer


**Koneksi hardware (perangkat keras)**

**Langkah 1.** Gunakan kabel Grove untuk menghubungkan modul Grove - Buzzer ke port D6 Seeeduino Lotus

![D6 with seeeduino](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/buzzer_ard.jpg)

**Langkah 2.** Sambungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB.

**Pemrograman software (perangkat lunak)**	

**Contoh 1** : Menggunakan digital logic high/low untuk membuat bel "buzz"

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```
//assign buzzer as pin 6
#define buzzer 6

void setup()
{
  //set buzzer as output
  pinMode(buzzer, OUTPUT);
}

void loop()
{ //turn on buzzer(set logic level high)
  digitalWrite(buzzer, HIGH);
  //wait 1s
  delay(1000);
  //turn off buzzer(set logic level low)
  digitalWrite(buzzer, LOW);
  //wait 1s
  delay(1000);
}

```
Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

!!!Sukses
	Ketika kode selesai di-upload (unggah), Anda dapat mendengar "buzz" dengan jeda 1 detik di antara suara.

**Contoh 2** : Gunakan frekuensi berbeda untuk membuat bel menghasilkan nada yang berbeda.

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//assign buzzer as pin 6 
#define buzzer 6                

void setup()
{
  /* tone(pin, frequency, duration) */
  //set buzzer pin to play 264Hz for 300ms
  tone(buzzer, 262, 300);
  //wait 1s
  delay(1000);

  //set buzzer pin to play 297Hz for 300ms
  tone(buzzer, 294, 300);
  //wait 1s
  delay(1000);

  //set buzzer pin to play 330Hz for 300ms
  tone(buzzer, 330, 300);
  //wait 1s
  delay(1000);
}

void loop()
{
  // no need to repeat the tone.
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

!!!Sukses
	Ketika kode selesai diupload (unggah), Anda akan mendengar buzzer berbunyi "Do 、 Re 、 Mi".

**Contoh 3** : Menggunakan fungsi tone (pin, frequency, duration) untuk membuat musik dari buzzer	

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C++

// initalise the frequency of the notes
#define NOTE_A4  440
#define NOTE_AS4 466
#define NOTE_C4  262
#define NOTE_D4  294
#define NOTE_E4  330
#define NOTE_F4  349
#define NOTE_G4  392
#define NOTE_C5  523

//assign buzzer as pin 6
#define buzzer 6

// notes in the melody:
int melody[] = {
  NOTE_C4, NOTE_C4, NOTE_D4, NOTE_C4, NOTE_F4, NOTE_E4,
  NOTE_C4, NOTE_C4, NOTE_D4, NOTE_C4, NOTE_G4, NOTE_F4,
  NOTE_C4, NOTE_C4, NOTE_C5, NOTE_A4, NOTE_F4, NOTE_E4, NOTE_D4,
  NOTE_AS4, NOTE_AS4, NOTE_A4, NOTE_F4, NOTE_G4, NOTE_F4
};

// note durations: 4 = quarter note, 8 = eighth note, etc.:
int noteDurations[] = {
  8, 8, 4, 4, 4, 2,
  8, 8, 4, 4, 4, 2,
  8, 8, 4, 4, 4, 4, 4,
  8, 8, 4, 4, 4, 2,
};

void setup() {
  // iterate over the notes of the melody:
  for (int thisNote = 0 ; thisNote < 25 ; thisNote++) {

    // to calculate the note duration, take one second divided by the note type.
    //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
    int noteDuration = 1000 / noteDurations[thisNote];
    tone(buzzer, melody[thisNote], noteDuration);

    // to distinguish the notes, set a minimum time between them.
    int pauseBetweenNotes = noteDuration * 1.30;
    delay(pauseBetweenNotes);
    noTone(buzzer);
  }
}

void loop() {
  // no need to repeat the melody.
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

!!!sukses
	Ketika kode selesai di-upload (unggah), Anda seharusnya dapat mendengar melodi dari buzzer.


**Penjelajahan Lebih Lanjut**

Silahkan checkout repo GitHub milik Brett Hagman "[Tone](https://github.com/bhagman/Tone)" untuk membuat nada dan musik.

### Sesi 2: Grove - Tilt Switch



![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/Tilt.jpg)

**Tujuan**	

Gunakan modul tilt switch untuk menghidupkan/memadamkan LED bawaan pada Seeeduino Lotus, dan juga gunakan tilt switch untuk membuat modul buzzer dari sesi sebelumnya.

**Inti Pengetahuan**

- Tilt Switch adalah modul input sinyal
- Operasi pada tilt switch
- Menggunakan fungsi digitalRead(pin) mendapatkan sinyal logika input dari tilt switch yang HIGH saat saklar on, dan LOW saat saklar off.
- fungsi if(kondisi){}else{} dan operator perbandingan seperti !=(tidak sama dengan), <(kurang dari), <=(kurang dari atau sama dengan), ==(sama dengan),>(lebih besar dari) dan >=(lebih besar dari atau sama dengan).

**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang

Termasuk dalam kit

- Board dev Seeeduino Lotus V1.1
- Kabel Grove
- Grove – Tilt Switch
- Grove – Buzzer
	
**Koneksi hardware (perangkat keras)**

Langkah 1: Hubungkan Grove - Tilt Switch ke port D5 Seeeduino Lotus.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/tilt_ard.jpg)


Langkah 2: Hubungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB

**Pemrograman software (perangkat lunak)**

**Contoh 1** : Mengamati perilaku tilt switch dengan menggunakan Serial Monitor

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//assign name tiltswitchPin to pin 5
#define tiltswitchPin 5
//creates a integer variable called 'val' to store read value
int val;

void setup()
{
  //set pinMode of tiltswitchPin to input
  pinMode(tiltswitchPin, INPUT);
  // opens serial port, sets data rate to 9600 bps
  Serial.begin(9600);
}

void loop()
{ //read the tilt switch input
  val = digitalRead(tiltswitchPin);
  //display the tilt switch status, 1 is on, 0 is off.
  Serial.println(val);
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Buka Serial Monitor

untuk membuka serial monitor,pilih  Tools | Serial Monitor dari menu, atau cukup klik ikon kaca pembesar pada tool. Catatan: Tunggu kode selesai di-upload (unggah) sebelum membuka serial monitor.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard12.png)

Langkah 4: Amati hasil

Miringkan sakelar kemiringan di kedua arah, Anda akan melihat “1” atau “0” ditampilkan di monitor serial, sekarang Anda dapat menemukan orientasi yang tepat untuk tilt switch guna menghidupkan/memadamkan.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/tilt_off&on.jpg)


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard13.png)

**Contoh 2** : Gunakan tilt switch untuk menghidupkan/memadamkan LED on-baord

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//set title of pin 5 as tiltSwitch
#define tiltSwitch 5

void setup()
{ //set pin 5(tilt switch) as input pin
  pinMode(tiltSwitch, INPUT);
  //set pin 13(Builtin LED) as output pin
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{ //read the status of tilt switch
  if (HIGH == digitalRead(tiltSwitch)) {
    /*
       if the logic level of tilt switch
       is high turn on the builtin LED
    */
    digitalWrite(LED_BUILTIN, HIGH);
  } else
  {
    //otherwise turn off the builtin LED
    digitalWrite(LED_BUILTIN, LOW);
  }
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

!!!Sukses
	Sekarang Anda dapat menghidupkan/memadamkan LED bawaan pada Seeeduino Lotus dengan memiringkan tilt switch ke arah yang benar.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/tilt_off&on.jpg)


**Contoh 3** : Gunakan tilt switch untuk jeda dan putar nada dering dari buzzer
Sambungkan modul Grove - Buzzer ke port D6 Seeeduino Lotus

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/buzzer_tilt.jpg)

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

// initalise the frequency of the notes
#define NOTE_A4  440
#define NOTE_AS4 466
#define NOTE_C4  262
#define NOTE_D4  294
#define NOTE_E4  330
#define NOTE_F4  349
#define NOTE_G4  392
#define NOTE_C5  523

// notes in the melody:
int melody[] = {
  NOTE_C4, NOTE_C4, NOTE_D4, NOTE_C4, NOTE_F4, NOTE_E4,
  NOTE_C4, NOTE_C4, NOTE_D4, NOTE_C4, NOTE_G4, NOTE_F4,
  NOTE_C4, NOTE_C4, NOTE_C5, NOTE_A4, NOTE_F4, NOTE_E4, NOTE_D4,
  NOTE_AS4, NOTE_AS4, NOTE_A4, NOTE_F4, NOTE_G4, NOTE_F4
};

// note durations: 4 = quarter note, 8 = eighth note, etc.:
int noteDurations[] = {
  8, 8, 4, 4, 4, 2,
  8, 8, 4, 4, 4, 2,
  8, 8, 4, 4, 4, 4, 4,
  8, 8, 4, 4, 4, 2,
};

//set title of pin 5 as tiltSwitch
#define tiltSwitch 5
//set title of pin 6 as buzzer
#define buzzer 6
// set variable currentNote to store latest note played
int currentNote;

void setup()
{
  //set pin 5(tilt switch) as input pin
  pinMode(tiltSwitch, INPUT);
}

void loop()
{
  /*read the status of tilt switch
if the logic level of tilt switch
is high, start play music */
  if (HIGH == digitalRead(tiltSwitch)) {

for (int thisNote = currentNote ; thisNote < 25 ; thisNote++) {
  // to calculate the note duration, take one second divided by the note type.
  //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
  int noteDuration = 1000 / noteDurations[thisNote];
  tone(buzzer, melody[thisNote], noteDuration);

  // to distinguish the notes, set a minimum time between them.
  int pauseBetweenNotes = noteDuration * 1.30;
  delay(pauseBetweenNotes);

  /*reset the currentNote to the 0
is the music is finished*/
  if (thisNote >= 24) {
currentNote = 0;
  }

  /*druing the music read the status
of tilt switch if the logic level
of tilt switch is LOW, stop play
music and store the previous played
tone and jump to next tone*/
  if (LOW == digitalRead(tiltSwitch)) {

//store the current note(thisNote) to currentNote
currentNote = thisNote;
//set the next note ready to play by increase currentNote by 1 increament
currentNote ++;
/*reset the currentNote to the beginning
  is the music is finished*/
if (currentNote >= 25)
{
  //restart the music from beginning by reset the currentNote to 0,
  currentNote = 0;
}
//if the tilt switch is set to logic level low, stop play music
break;
  }
}
  }
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasil

!!!Sukses
  Sekarang Anda harusnya dapat menjeda nada dering dengan memiringkan tilt switch ke posisi mati, dan melanjutkan nada musik dengan memiringkan sakelar kemiringan ke posisi semula.

**Penjelajahan Lebih Lanjut**

Setelah sesi ini, Anda dapat memasang modul sensor tilt switch ke tutup kotak alat Anda, jadi ketika Anda mengangkat tutupnya, memicu tilt switch untuk menyala, kemudian Anda dapat mengatur penundaan untuk waktu singkat untuk mengaktifkan buzzer untuk membuat beberapa nada yang mengingatkan Anda bahwa tutupnya masih terbuka, jadi Anda tidak akan lupa untuk menutup tutupnya setelah Anda selesai menggunakan kotak peralatan.

### Sesi 3: Grove – Chainable RGB LED

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/Grove-Chainable_RGB_LED_V2.0.jpg)

**Tujuan**	

Gunakan kode untuk mengontrol chainable RGB LED untuk menunjukkan warna berbeda, dan beralih di antara warna dengan menggunakan tilt switch.

**Inti Pengetahuan**

- Grove - Chainable RGB LED adalah aktuator
- Memasukan library untuk modul grove
- Menggunakan fungsi setColorHSB() untuk mengontrol warna, saturasi, dan kecerahan modul LED
- Menggunakan fungsi setColorRGB() untuk mengontrol warna dan kecerahan modul LED
- Menggunakan operasi %(modulo) untuk menemukan sisa, mis. 5%2=1, 9%3=0.
- Menggunakan fungsi switch(val)…case…;


**Persyaratan hardware (perangkat keras)**	

Persiapan

- kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang


Termasuk dalam kit

- Board Dev Seeeduino Lotus V1.1
- Kabel Grove
- Grove – Chainable RGB LED
- Grove – Tilt Switch
- Grove – Buzzer


**Koneksi perangkat keras**

Langkah 1: Sambungkan Grove - Chainable RGB LED ke port D7 dari Seeeduino Lotus, Catatan: harap sambungkan port G|V|DI|CI dari LED seperti yang ditunjukkan di bawah ini.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/rgb_ard.jpg)

Langkah 2: Hubungkan Seeeduino Lotus dengan komputer melalui kabel micro USB.


**Pemrograman perangkat lunak**

**Menambah Library**

Langkah-langkah di bawah ini menunjukkan cara menambahkan [library](https://github.com/pjpmarques/ChainableLED/archive/v1.2.zip) untuk Grove – Chainable RGB LED.

Langkah 1: Buka repositori Github dari URL Library, dan unduh data zip

Carit tombol “Clone or download | Download ZIP” dari halaman Github, Anda harus memilih Download ZIP only, dan harap ingat dimana file zip yang telah Anda unduh dan simpan.

Langkah 2: Pilih “include Library | Add .ZIP Library..

Pilih open Sketch | Include Library | Add .ZIP Library…, di jendela baru yang muncul, pilih file zip yang telah Anda unduh dari langkah terakhir, lalu klik choose.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard14.png)


Langkah 3: Uji apakah library berhasil ditambahkan

Pilih dan buka File | Examples | ChainableLED-1.2 | CycleTroughColors

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/ard15.png)

Unggah Kode: Klik Unggah the code

!!!Sukses
  jika modul LED menyala melalui warna yang berbeda, dari yang Anda tahu Anda telah berhasil memuat Library.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/rgb_flash_8.jpg)

Kesimpulan: Menambahkan library memungkinkan pengguna dengan mudah menambahkan driver sensor lainnya dan library yang dibuat oleh penyedia modul sensor, misalnya, dalam tutorial ini, kami menggunakan fungsi setColorRGB(byte led, byte red, byte green, byte blue) adalah salah satu fungsi yang diterapkan oleh Seeed Studio. Hal ini mengurangi biaya pengembangan pengguna ketika mereka mengadaptasi modul sensor baru. Anda perlu menambahkan lebih banyak library untuk modul grove lainnya nanti.

**Contoh 1** : Gunakan fungsi setColorHSB untuk mengubah warna LED

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C++

//add ChainableLED library to this project
#include <ChainableLED.h>

//set the number of leds linked to the chain
#define NUM_LEDS  1

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

void setup()
{
  //initialise ChainableLED leds
  leds.init();
}
//initialise hue as float point with value of 0.0
float hue = 0.0;
//initialise up as boolean with value of true
boolean up = true;

void loop()
{
  /*for loop is used for loop through
    each LED connected to the chain
    in this case there is only one LED
  */
  for (byte i = 0; i < NUM_LEDS; i++) {

    /*setColorHSB(byte led, float hue, float saturation, float brightness);
       in this case set the first and only chainableLED 0 with changing hue
       and full saturation and half brightness
    */
    leds.setColorHSB(i, hue, 1, 0.5);
    //    delay for 50ms for each color
    delay(50);

    /*if up is true increase
      hue at 0.025 interval
      otherwise decrease hue
      at 0.025 interval
    */
    if (up) {
      hue += 0.025;
    }
    else
    {
      hue -= 0.025;
    }
    /*
      if hue is greater than 1.0
       and up is true set up to false,
       otherwise if hue is less or
       equal to 0.0 and up is not
       ture(! means is not) set up
       to true
    */
    if (hue >= 1.0 && up)
    {
      up = false;
    }
    else if (hue <= 0.0 && !up)
    {
      up = true;
    }
  }
}

```

Langkah 2: Upload (unggah) code into Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda akan melihat warna LED berubah sesuai dengan nilai warna, yang meningkat dengan kenaikan 0,025 dan ketika nilai warna mencapai 1, nilai warna harus dikurangi dengan penurunan 0,025 hingga nilainya menjadi 0, dan setiap warna harus menyala untuk 50 milidetik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/rgb_flash_8.jpg)

**Contoh 2** : Gunakan fungsi setColorRGB untuk mengubah warna dan kecerahan LED

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C++

/*
   Example of using the ChainableRGB library for controlling a Grove RGB.
   This code fades in an out colors in a strip of leds.
*/

//add ChainableLED library to this project
#include <ChainableLED.h>

//set the number of leds linked to the chain
#define NUM_LEDS  1

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

void setup()
{
  //initialise ChainableLED leds
  leds.init();
}
//initialise power as byte with value of 0
byte power = 0;

void loop()
{
  /*for loop is used for loop through
    each LED connected to the chain
    in this case there is only one LED
  */
  for (byte i = 0; i < NUM_LEDS; i++)
  {
    /*
      % means modulo operation to find remainder
      eg 0 % 2 = 0, 1 % 2 = 1,  2 % 2 = 0...
      setColorRGB(byte led, byte red, byte green, byte blue);
      so in this case the even number of the LED chain
      will fading green color, odd number of the LED
      chain will fading red color, since we count the
      first LED as 0.
    */
    if (i % 2 == 0)
      //brighter red color from 0 to full power
      leds.setColorRGB(i, power, 0, 0);
    else
      //dimmer green color from full power to 0
      leds.setColorRGB(i, 0, 255 - power, 0);
  }
  //set power increment as 10
  power += 10;
  //light 0.5s for each brightness
  delay(500);
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda akan melihat LED warna merah meningkatkan kecerahan di setiap 0,5s, karena kami hanya menetapkan nilai untuk variabel merah dalam fungsi setColorRGB(byte led, byte red, byte green, byte blue).

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/rgb_eg2.jpg)

Jika kita mengubah variabel merah dan hijau dari ini:

```C
leds.setColorRGB(i, power, 0, 0);
```

menjadi ini:

```C
leds.setColorRGB(i, power, 255-power, 0);
```

Perhatikan perbedaannya.

**Contoh 3** : Gunakan tilt switch untuk mengontrol LED dan Buzzer

Hubungkan Grove - Tilt Switch ke port D5 Seeeduino Lotus.

Hubungkan Grove - Buzzer module ke port D6 Seeeduino Lotus.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/rgb_buzzer_tilt.jpg)

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add ChainableLED library to this project
#include <ChainableLED.h>

//set the number of leds linked to the chain
#define NUM_LEDS  1

// initalise the frequency of the notes
#define NOTE_A4  440
#define NOTE_AS4 466
#define NOTE_C4  262
#define NOTE_D4  294
#define NOTE_E4  330
#define NOTE_F4  349
#define NOTE_G4  392
#define NOTE_C5  523

// notes in the melody:
int melody[] = {
  NOTE_C4, NOTE_C4, NOTE_D4, NOTE_C4, NOTE_F4, NOTE_E4,
  NOTE_C4, NOTE_C4, NOTE_D4, NOTE_C4, NOTE_G4, NOTE_F4,
  NOTE_C4, NOTE_C4, NOTE_C5, NOTE_A4, NOTE_F4, NOTE_E4, NOTE_D4,
  NOTE_AS4, NOTE_AS4, NOTE_A4, NOTE_F4, NOTE_G4, NOTE_F4
};

// note durations: 4 = quarter note, 8 = eighth note, etc.:
int noteDurations[] = {
  8, 8, 4, 4, 4, 2,
  8, 8, 4, 4, 4, 2,
  8, 8, 4, 4, 4, 4, 4,
  8, 8, 4, 4, 4, 2,
};

//set title of pin 5 as tiltSwitch
#define tiltSwitch 5
//set title of pin 6 as buzzer
#define buzzer 6

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

// set variable currentNote to store latest note played
int currentNote;
//initialise hue as float point with value of 0.0
float hue = 0.0;
//initialise up as boolean with value of true
boolean up = true;
//initialise power as byte with value of 0
byte power = 0;
//initialise color as integer with value of 0
int color = 0;

void setup()
{
  //set pin 5(tilt switch) as input pin
  pinMode(tiltSwitch, INPUT);
  //initialise ChainableLED leds
  leds.init();
}

void loop()
{
  /*read the status of tilt switch
    if the logic level of tilt switch
    is high, start play music */
  if (HIGH == digitalRead(tiltSwitch)) {

    for (int thisNote = currentNote ; thisNote < 25 ; thisNote++) {
      // to calculate the note duration, take one second divided by the note type.
      //e.g. quarter note = 1000 / 4, eighth note = 1000/8, etc.
      int noteDuration = 1000 / noteDurations[thisNote];
      tone(buzzer, melody[thisNote], noteDuration);

      // to distinguish the notes, set a minimum time between them.
      int pauseBetweenNotes = noteDuration * 1.30;
      delay(pauseBetweenNotes);

      /*reset the currentNote to the 0
        is the music is finished*/
      if (thisNote >= 24) {
        currentNote = 0;
      }

      /*set the LED to loop through
        different colors with different hue*/
      leds.setColorHSB(0, hue, 1, 0.5);

      /*if up is true increase
        hue at 0.025 interval
        otherwise decrease hue
        at 0.025 interval
      */
      if (up) {
        hue += 0.025;
      }
      else
      {
        hue -= 0.025;
      }
      /*if hue is greater than 1.0
         and up is true set up to false,
         otherwise if hue is less or
         equal to 0.0 and up is not
         ture(! means is not) set up
         to true
      */
      if (hue >= 1.0 && up)
      {
        up = false;
      }
      else if (hue <= 0.0 && !up)
      {
        up = true;
      }

      /*druing the music read the status
        of tilt switch if the logic level
        of tilt switch is LOW, stop play
        music and store the previous played
        tone and jump to next tone*/
      if (LOW == digitalRead(tiltSwitch)) {
        /* use switch...case to set the LED loop through three colors
           Red when color = 0 enters case 0
           Green when color = 1 enters case 1
           Blue when color = 2 enters case 2
           reset color to 0 if color is greater or equals 3
        */
        if (color >= 3) {
          color = 0;
        }
        switch (color) {
          case 0:
            //set LED to Red
            leds.setColorRGB(0, 255, 0, 0);
            break;
          case 1:
            //set LED to Green
            leds.setColorRGB(0, 0, 255, 0);
            break;
          case 2:
            //set LED to Blue
            leds.setColorRGB(0, 0, 0, 255);
            break;
        }
        //increase color by 1 increment everytime enter this condition
        color ++;

        //store the thisNote to currentNote
        currentNote = thisNote;
        //set the next note ready to play by increase currentNote by 1 increament
        currentNote ++;
        /*reset the currentNote to the beginning
          is the music is finished*/
        if (currentNote >= 25)
        {
          //restart the music from beginning by reset the currentNote to 0,
          currentNote = 0;
        }
        //if the tilt switch is set to logic level low, stop playing music
        break;
      }
    }
  }
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Dengan memiringkan tilt switch, Anda akan melihat kapan sakelar kemiringan dihidupkan, LED berubah warna bersamaan dengan nada perubahan pada buzzer, ketika sakelar kemiringan mati, LED akan menyala bergantian dari Merah, Hijau dan Biru kemudian buzzer berhenti.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/rgb_eg3.jpg)



**Penjelajahan Lebih Lanjut**

Setelah sesi ini, Anda sekarang dapat menggabungkan modul dari tiga sesi pertama dan berubah menjadi kotak hadiah ulang tahun, di mana Anda dapat menempatkan sensor tilt switch pada tutup kotak, pada saat kotak terbuka, tilt switch akan terpicu, kemudian bel mulai memutar lagu ulang tahun dan lampu LED mulai berkedip lampu warna-warni.

### Sesi 4: Grove - Light Sensor

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/lightsensor.jpg)

**Tujuan**	

Gunakan modul sensor cahaya untuk menghidupkan/memadamakn modul chainable RGB LED, dan mengontrol kecerahan LED sesuai dengan intensitas cahaya sekitar.

**Inti Pengetahuan**

- Modul Sensor Cahaya adalah modul input sinyal Analog
- Menggunakan fungsi map(value, fromLow, fromHigh, toLow, toHigh) untuk memetakan kembali jumlah output Analog dari satu rentang ke rentang lainnya dengan lebih jelas dan praktis.
- Gunakan sensor cahaya sebagai saklar lampu
- Gunakan sensor cahaya untuk mengontrol kecerahan LED dengan mendeteksi kecerahan sekitar

**Persyaratan perangkat keras**	

Persiapan

- kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang

Termasuk dalam kit

- Board dev Seeeduino Lotus V1.1
- Kabel Grove
- Grove – Light Sensor
- Grove – Chainable RGB LED


**Koneksi perangkat keras**

Langkah 1: Hubungkan Grove - modul Light Sensor ke port A0 Seeeduino Lotus

Langkah 2: Hubungkan Grove - Chainable RGB LED  ke port D7 Seeeduino Lotus

Langkah 3: Hubungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/light_rgb.jpg)

**Pemrograman perangkat lunak**

**Contoh 1** : Menggunakan sensor cahaya untuk menghidupkan/memadamkankan LED oleh kecerahan cahaya sekitar

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add ChainableLED library to this project
#include <ChainableLED.h>

//set the number of leds linked to the chain
#define NUM_LEDS  1

/*assign leds as the name of
  the ChainableLED, set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

//naming analog pin A0 as LightSensor
#define LightSensor A0

void setup()
{
  //initialise ChainableLED leds
  leds.init();
}

void loop()
{
  //read the value of Light Sensor and store to value
  int value = analogRead(LightSensor);
  //if Sensor reading is less than 150 turn on LED
  if (value < 150) {
    //turn on LED
    leds.setColorRGB(0, 10, 10, 10);
    //delay for 1s
    delay(1000);
  } else
  {
    //turn off LED
    leds.setColorRGB(0, 0, 0, 0);
    //delay for 1s
    delay(1000);
  }
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Catat jika lampu sekitar menyala, Anda dapat menggunakan tangan untuk menutupi modul sensor cahaya, maka LED akan menyala. ketika cahaya sekitar membuat nilai pembacaan sensor cahaya lebih tinggi dari 150, LED seharusnya padam.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/light_eg1.jpg)

**Contoh 2** : Menggunakan sensor cahaya untuk mengontrol kecerahan LED

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add ChainableLED library to this project
#include <ChainableLED.h>

//set the number of leds linked to the chain
#define NUM_LEDS  1

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

#define LightSensor A0

void setup()
{
  //initialise ChainableLED leds
  leds.init();
  Serial.begin(9400);
}

//initialise hue as float point with value of 0.0
float hue = 0.0;
//initialise up as boolean with value of true
boolean up = true;

void loop()
{
  //read the value of Light Sensor and store to value
  int value = analogRead(LightSensor);
  /*map(value, fromLow, fromHigh, toLow, toHigh)
    Re-maps a number from one range to another
    In this case maping the analog value of light sensor
    ranging from 0-800 to 100-0, so when the brightness
    of surrounding enviroment is high so the sensor reading
    value is high, therefore the maped value should be opposite,
    so the birghtness LED should be dimmer.
    the brightness of chainable LED only accept float number, so
    we divide the maped value with 100. 
  */
  float value_float = map(value, 0, 800, 50, 0) / 100.0;
  /*setColorHSB(byte led, float hue, float saturation, float brightness);
   * use the maped value(value_float) as brightness
  */
  leds.setColorHSB(0, hue, 1, value_float);
  delay(100);

  /*if up is true increase
    hue at 0.025 interval
    otherwise decrease hue
    at 0.025 interval
  */
  if (up) {
    hue += 0.025;
  }
  else
  {
    hue -= 0.025;
  }
  /*if hue is greater than 1.0
     and up is true set up to false,
     otherwise if hue is less or
     equal to 0.0 and up is not
     ture(! means is not) set up
     to true
  */
  if (hue >= 1.0 && up)
  {
    up = false;
  }
  else if (hue <= 0.0 && !up)
  {
    up = true;
  }
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Kecerahan LED akan berkurang ketika kecerahan sekitarnya meningkat. Ketika kecerahan sekitar berkurang, maka kecerahan LED harusnya akan meningkat. Seperti yang ditunjukkan, LED meredup ketika ada cahaya terang yang menyinari sensor cahaya, jika tidak maka LED tersebut akan bersinar cerah.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/light_eg2.jpg)

**Penjelajahan Lebih Lanjut**

Sekarang Anda dapat mengintegrasikan modul sensor cahaya ini ke dalam sistem penerangan koridor rumah untuk mengontrol kecerahan cahaya, pada siang hari sensor cahaya mendeteksi cahaya matahari kemudian meredupkan kecerahan cahaya koridor menjadi rendah, tidak hanya menghemat daya, tetapi juga memperpanjang umur bumi.


### Sesi 5: Grove - Line Finder

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/linefinder.jpg)

**Tujuan**	

Menggunakan line finder untuk mendeteksi garis hitam, dan mengontrol warna LED yang sesuai ketika line finder mendeteksi garis hitam atau bukan.

**Inti Pengetahuan**

- Grove - Line Finder adalah modul input sinyal digital
- Memperbaiki cara menggunakan Serial Monitor
- Menggunakan modul input sinyal untuk mengontrol Grove - LED RGB Chainable

**Persyaratan perangkat keras**	

Persiapan

- kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang

Termasuk dalam kit
  
- Grove – Line Finder
- Grove – Chainable RGB LED

**Koneksi perangkat keras**

Langkah 1: Hubungkan Grove - modul Line Finder ke port D3 Seeeduino Lotus

Langkah 2: Hubungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB

 ![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/line_ard.jpg)

**Pemrograman perangkat lunak**

**Contoh 1** : Menggunakan Serial Monitor untuk menampilkan dan menguji sinyal keluaran dari line finder

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//naming pin3 as singalPin
#define signalPin 3

void setup() {
  // initialize the digital pin as an input:
  pinMode(signalPin, INPUT);
  // opens serial port, sets data rate to 9600 bps
  Serial.begin(9600);
}

void loop() {
  //read the line detector input 
  int val = digitalRead(signalPin);
  
  //display the line detector status, 1 is black, 0 is white.
  Serial.println(val);
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Catatan : Anda harus memberi jarak antara line finder dan objek deteksi setidaknya 5 cm, Anda harus menempelkan pita hitam ke kertas putih atau ubin (atau menggunakan benda hitam) pada saat menguji line finder. Sekarang arahkan line finder ke objek hitam, maka Serial Monitor akan menampilkan 0, dan jika Anda memindahkan line finder dari objek hitam, maka Serial Monitor akan menampilkan 1.

 ![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/line_eg1_1.jpg) 



**Contoh 2** : Menggunakan Line detector untuk menghidupkan atau mematikan Grove - modul LED RGB Chainable.

Hubungkan Grove - LED RGB Chainable ke port D7 pada Seeeduino Lotus

 ![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/line_rgb.jpg)

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add ChainableLED library to this project
#include <ChainableLED.h>

//set the number of leds linked to the chain
#define NUM_LEDS  1

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

//naming pin3 as lineFinder
#define lineFinder 3

void setup() {
  // initialize the digital pin as an input:
  pinMode(lineFinder, INPUT);
  //initialise ChainableLED leds
  leds.init();
}

void loop() {
  /*read the line detector input
   * if detected black(HIGH) turn on LED
  */
  if (HIGH == digitalRead(lineFinder))
  {
    //turn off LED
    leds.setColorRGB(0, 10, 10, 10);
  }
  
  /*read the line detector input
   * if reading Logic low turn off LED
  */
  if (LOW == digitalRead(lineFinder))
  {
    //turn off LED
    leds.setColorRGB(0, 0, 0, 0);
  }
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda harus melihat bahwa jika pencari garis mendeteksi garis hitam, LED akan padam, jika tidak LED akan menyala jika pencari garis tidak dapat mendeteksi garis hitam.

 ![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/line_eg2.jpg)
 

**Contoh 3** : Menggunakan line finder untuk mengontrol LED agar memancarkan warna Merah atau Hijau

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add ChainableLED library to this project
#include <ChainableLED.h>

//set the number of leds linked to the chain
#define NUM_LEDS  1

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

//naming pin3 as lineFinder
#define lineFinder 3

void setup() {
  // initialize the digital pin as an input:
  pinMode(lineFinder, INPUT);
  //initialise ChainableLED leds
  leds.init();
}

void loop() {
  /*read the line detector input
   * if detected black(HIGH) set Green LED
  */
  if (HIGH == digitalRead(lineFinder))
  {
    //Green LED
    leds.setColorRGB(0, 0, 255, 0);
  }
  
  /*read the line detector input
   * if reading Logic low set Red LED
  */
  if (LOW == digitalRead(lineFinder))
  {
    //Red LED
    leds.setColorRGB(0, 255, 0, 0);;
  }
}

```

Langkah 2: Upload (unggah) kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda harus memperhatikan ketika line finder mendeteksi garis hitam, LED akan memancarkan cahaya merah. Namun jika tidak atau jika pencari garis tidak dapat menemukan garis hitam, LED harus memancarkan cahaya Hijau.


 ![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/line_eg3.jpg)


**Penjelajahan Lebih Lanjut**

Sekarang Anda dapat membangun mobil line finder Anda sendiri dengan menggunakan modul line finder ini dan dua motor dengan driver motor (H-bridge), jadi ketika pencari garis mendeteksi garis hitam, aktifkan satu sisi roda motor, setelah line finder dari garis hitam, hentikan sisi berputar dari roda motor, dan aktifkan sisi lain dari roda motor. Sehingga mobil akan berjalan di sepanjang garis hitam dengan bagian depan mobil konstan berbelok ke kiri atau kanan.

### Sesi 6: Grove - LCD RGB Backlight

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/LCD.jpg)

**Tujuan**	

Menggunakan Grove - LCD RGB Backlight screen untuk menampilkan "Hello World" dan beberapa karakter khusus.

**Inti Pengetahuan**

- Memperbaiki cara menambahkan library
- Menguasai dalam memposisikan karakter dan menggunakan kode biner untuk menghasilkan karakter khusus.
- Teks berjalan yang ditampilkan pada layar LCD
- Menggunakan kode karakter bawaan LCD untuk menampilkan karakter khusus, misalnya tanda derajat “°”

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/chartable.png)


**Persyaratan perangkat keras**	

Persiapan

- kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang

Termasuk dalam kit

- Board dev Seeeduino Lotus V1.1
- Kabel Grove
- Grove - LCD RGB Backlight


**Koneksi hardware (perangkat keras)**

Langkah 1: Hubungkan Grove - modul LCD RGB Backlight ke port I2C dari Seeeduino Lotus catatan: itu adalah port I2C yang diikuti oleh satu titik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/lcd_ard.jpg)


Langkah 2: Hubungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB.


**Pemrograman software (perangkat lunak)**

**Menambahkan Library**

Tambah [Library](https://github.com/Seeed- Studio/Grove_LCD_RGB_Backlight/archive/master.zip) untuk Grove - LCD RGB Backlight Screen 

Ikuti instruksi di panduan 3 tentang cara melakukannya <a href="#step3">add library</a>.

**Contoh 1** : Menampilkan Hello World

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//include the rgb_lcd library
#include "rgb_lcd.h"

//assign name lcd to rgb_lcd
rgb_lcd lcd;

void setup() 
{
    // set up the LCD's number of columns and rows:
    lcd.begin(16, 2);
    
    // Print Hello, World! to the LCD.
    lcd.print("Hello, World!");
    delay(1000);
}

void loop() 
{
    // set the cursor to column 0, line 1
    // (note: line 1 is the second row, since counting begins with 0):
    lcd.setCursor(0, 1);
    // print the number of seconds since reset:
    lcd.print(millis()/1000);
    delay(100);
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda akan melihat "Hello, World!" yang ditampilkan di baris pertama dan penghitung waktu mundur di baris kedua.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/helloworld.jpg)

**Contoh 2** : Tampilkan logo Seeed Studio dan gunakan kode karakter bawaan untuk menampilkan teks

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add LCD library
#include "rgb_lcd.h"

//assign lcd as the name of rgb_lcd screen
rgb_lcd lcd;

/*draw customise character
  in this case is the seeed studio logo
*/
byte top_leftleft[8] = {
  B00000,
  B00000,
  B01000,
  B01000,
  B01000,
  B01100,
  B01100,
  B01110
};
byte top_midleft[8] = {
  B00001,
  B00010,
  B00010,
  B00110,
  B00110,
  B00100,
  B01100,
  B01100
};
byte top_midright[8] = {
  B10000,
  B01000,
  B01000,
  B01100,
  B01100,
  B00100,
  B00110,
  B00110
};
byte top_rightright[8] = {
  B00000,
  B00000,
  B00010,
  B00010,
  B00010,
  B00110,
  B00110,
  B01110
};
byte bot_leftleft[8] = {
  B00110,
  B00111,
  B00011,
  B00011,
  B00001,
  B00000,
  B00000,
  B00000
};
byte bot_midleft[8] = {
  B01100,
  B01110,
  B00110,
  B00110,
  B10011,
  B11011,
  B11111,
  B01111
};
byte bot_midright[8] = {
  B00110,
  B01110,
  B01100,
  B01100,
  B11001,
  B11011,
  B11111,
  B11110
};
byte bot_rightright[8] = {
  B01100,
  B11100,
  B11000,
  B11000,
  B10000,
  B00000,
  B00000,
  B00000
};

void setup()
{
  //initialise the lcd screen;
  // set up the lcd's number of columns and rows:
  lcd.begin(16, 2);

  /*create and assign numbers of
    each seeed studio logo elements
  */
  lcd.createChar(0, top_leftleft);
  lcd.createChar(1, top_midleft);
  lcd.createChar(2, top_midright);
  lcd.createChar(3, top_rightright);
  lcd.createChar(4, bot_leftleft);
  lcd.createChar(5, bot_midleft);
  lcd.createChar(6, bot_midright);
  lcd.createChar(7, bot_rightright);


  /* set the cursor to column 4, line 0
    note: line 0 is the first row, since counting begins with 0
    same rule apply to the column as well
  */
  lcd.setCursor(4, 0);
  //Print I and a space to the LCD at column 4, line 0
  lcd.print("I ");
  //set the cursor to column 6, line 0
  lcd.setCursor(6, 0);
  /* Print LOVE by using the LCD character lookup table
     note write() method is mentt to send raw bytes
     print() is mostly intended to format data as ascii.
     this is different way of display text on lcd.
  */
  //character 76 is L on lookup table
  lcd.write(76);
  //the hex number 0x4F(is 79) associates with O on lookup table
  lcd.write(0x4F);
  //character 86 is V on lookup table
  lcd.write(86);
  //character 69 is E on lookup table
  lcd.write(69);
  //set the cursor to column 10, line 0
  lcd.setCursor(10, 0);
  //Print a space and Grove to the LCD
  lcd.write(" Grove");
  //set the cursor to column 4, line 1
  lcd.setCursor(4, 1);
  //Print text Seeed Studio to the LCD
  lcd.print("Seeed Studio");

  //display seeed studio logo
  lcd.setCursor(0, 0);
  lcd.write((unsigned char)0);
  lcd.setCursor(1, 0);
  lcd.write(1);
  lcd.setCursor(2, 0);
  lcd.write(2);
  lcd.setCursor(3, 0);
  lcd.write(3);
  lcd.setCursor(0, 1);
  lcd.write(4);
  lcd.setCursor(1, 1);
  lcd.write(5);
  lcd.setCursor(2, 1);
  lcd.write(6);
  lcd.setCursor(3, 1);
  lcd.write(7);
}

void loop()
{

}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda akan melihat Logo Seeed Studio ditampilkan di 8 blok pertama, diikuti oleh "I Love Grove" di baris pertama, dan "Seeed Studio" di baris kedua.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/lcd_seeed.jpg)

**Contoh 3** : Teks berjalan pada layar LCD

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C


//add LCD library
#include "rgb_lcd.h"

//assign lcd as the name of rgb_lcd screen
rgb_lcd lcd;

/*draw customise character
  in this case is the seeed studio logo
*/
byte top_leftleft[8] = {
  B00000,
  B00000,
  B01000,
  B01000,
  B01000,
  B01100,
  B01100,
  B01110
};
byte top_midleft[8] = {
  B00001,
  B00010,
  B00010,
  B00110,
  B00110,
  B00100,
  B01100,
  B01100
};
byte top_midright[8] = {
  B10000,
  B01000,
  B01000,
  B01100,
  B01100,
  B00100,
  B00110,
  B00110
};
byte top_rightright[8] = {
  B00000,
  B00000,
  B00010,
  B00010,
  B00010,
  B00110,
  B00110,
  B01110
};
byte bot_leftleft[8] = {
  B00110,
  B00111,
  B00011,
  B00011,
  B00001,
  B00000,
  B00000,
  B00000
};
byte bot_midleft[8] = {
  B01100,
  B01110,
  B00110,
  B00110,
  B10011,
  B11011,
  B11111,
  B01111
};
byte bot_midright[8] = {
  B00110,
  B01110,
  B01100,
  B01100,
  B11001,
  B11011,
  B11111,
  B11110
};
byte bot_rightright[8] = {
  B01100,
  B11100,
  B11000,
  B11000,
  B10000,
  B00000,
  B00000,
  B00000
};

void setup()
{
  //initialise the lcd screen;
  //set up the lcd's number of columns and rows:
  lcd.begin(16, 2);
  //wait for 1s
  delay(1000);
}

void loop()
{

  /*create and assign numbers of
    each seeed studio logo elements
  */
  lcd.createChar(0, top_leftleft);
  lcd.createChar(1, top_midleft);
  lcd.createChar(2, top_midright);
  lcd.createChar(3, top_rightright);
  lcd.createChar(4, bot_leftleft);
  lcd.createChar(5, bot_midleft);
  lcd.createChar(6, bot_midright);
  lcd.createChar(7, bot_rightright);

  /* set the cursor to column 4, line 0
    note: line 0 is the first row, since counting begins with 0
    same rule apply to the column as well
  */
  lcd.setCursor(4, 0);
  //Print I and a space to the LCD at column 4, line 0
  lcd.print("I ");
  //set the cursor to column 6, line 0
  lcd.setCursor(6, 0);
  /* Print LOVE by using the LCD character lookup table
     note write() method is mentt to send raw bytes
     print() is mostly intended to format data as ascii.
     this is different way of display text on lcd.
  */
  //character 76 is L on lookup table
  lcd.write(76);
  //the hex number 0x4F(is 79) associates with O on lookup table
  lcd.write(0x4F);
  //character 86 is V on lookup table
  lcd.write(86);
  //character 69 is E on lookup table
  lcd.write(69);
  //set the cursor to column 10, line 0
  lcd.setCursor(10, 0);
  //Print a space and Grove to the LCD
  lcd.write(" Grove");
  //set the cursor to column 4, line 1
  lcd.setCursor(4, 1);
  //Print text Seeed Studio to the LCD
  lcd.print("Seeed Studio");

  //display seeed studio logo
  lcd.setCursor(0, 0);
  lcd.write((unsigned char)0);
  lcd.setCursor(1, 0);
  lcd.write(1);
  lcd.setCursor(2, 0);
  lcd.write(2);
  lcd.setCursor(3, 0);
  lcd.write(3);
  lcd.setCursor(0, 1);
  lcd.write(4);
  lcd.setCursor(1, 1);
  lcd.write(5);
  lcd.setCursor(2, 1);
  lcd.write(6);
  lcd.setCursor(3, 1);
  lcd.write(7);
  
  // scroll 16 positions (string length) to the left
  // to move it offscreen left:
  for (int positionCounter = 0; positionCounter < 16; positionCounter++) {
    // scroll one position left:
    lcd.scrollDisplayLeft();
    // wait a bit:
    delay(200);
  }

  // scroll 32 positions (string length + display length) to the right
  // to move it offscreen right:
  for (int positionCounter = 0; positionCounter < 32; positionCounter++) {
    // scroll one position right:
    lcd.scrollDisplayRight();
    // wait a bit:
    delay(200);
  }

  // scroll 16 positions (display length + string length) to the left
  // to move it back to center:
  for (int positionCounter = 0; positionCounter < 16; positionCounter++) {
    // scroll one position left:
    lcd.scrollDisplayLeft();
    // wait a bit:
    delay(200);
  }
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda akan melihat tampilan teks berjalan, pertama dari kanan ke kiri sampai semua teks menghilang di ujung sisi kiri layar, kemudian teks akan menggulir kembali dari kiri ke kanan.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/lcd_scroll.jpg)

**Penjelajahan Lebih Lanjut**

[Situs Web](https://maxpromer.github.io/LCD-Character-Creator/) ini membantu Anda membuat karakter khusus untuk layar LCD yang didukung oleh Arduino.

### Sesi 7 : Grove - Temperature & Humidity Sensor (DHT11)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/DHT11.jpg)

**Tujuan**

Menggunakan modul sensor DHT11 untuk mendeteksi suhu dan kelembaban di sekitarnya, dan menampilkan data output dari DHT11 ke Layar LCD.

**Inti Pengetahuan**

- DHT11 adalah modul sensor digital
- Memperbaiki cara mengoperasikan Serial Monitor dan Layar LCD
- Menambah Library DHT11 dan pengaturan awal untuk DHT11
- Menggunakan Serial Monitor dan Layar LCD untuk menampilkan data dari sensor DHT11

**Persyaratan hardware (perangkat keras)**	

Persiapan

- kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang

Termasuk dalam kit

- Board Dev Seeeduino Lotus V1.1
- Kabel Grove
- Grove – Temperature &Humidity Sensor(DHT11)

**Koneksi hardware (perangkat keras)**

Langkah 1: Sambungkan modul Grove - Temperature & Humidity Sensor (DHT11) ke port D2 pada Seeeduino Lotus.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/DHT11_ard.jpg)

Langkah 2: Hubungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB

**Pemrograman software (perangkat lunak)**

**Tambahan** [Library](https://github.com/Seeed- Studio/Grove_Temperature_And_Humidity_Sensor/archive/master.zip)

**Contoh 1** : Menggunakan Serial Monitor untuk memantau suhu dan kelembaban di sekitarnya

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add DHT sensor library
#include <DHT.h>

//set digital pin2 as DHTPIN
#define DHTPIN 2
//set the sensor type as DHT 11
#define DHTTYPE DHT11

/*assign dht as the name of DHT sensor
  set the sensor pin as DHTPIN(pin2),
  set the sensor type as DHTTYPE(DHT11)
*/
DHT dht(DHTPIN, DHTTYPE);

void setup() {
  //initialise the dht sensor
  dht.begin();
  // opens serial port, sets data rate to 9600 bps
  Serial.begin(9600);
  //wait for 2s to initialise the board
  delay(2000);
}

void loop() {
  //store the humidity value to h
  int h = dht.readHumidity();
  //store the temperature value to t(in Celsius)
  int t = dht.readTemperature();
  //store the converted temperature value in fahrenheit to f
  int f = dht.convertCtoF(t);
  //display the title Temperature in C:
  Serial.print("Temperature in C: ");
  //display the temperature value t
  Serial.print(t);
  /* note the difference Serial.print()
     and Serial.println(),
     Serial.print() print the data in the same line
     Serial.println() print the data on the new line
     display the temperature unit ºC and change new line
  */
  Serial.println("ºC");
  //display the title Temperature in F:
  Serial.print("Temperature in F: ");
  //display the temperature value f
  Serial.print(f);
  //display the temperature unit ºF and change new line
  Serial.println("ºF");
  //display the title Humidity:
  Serial.print("Humidity: ");
  //display the Humidity value h
  Serial.print(h);
  //display the % sign
  Serial.println("%");
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Buka Serial Monitor

Langkah 4: Amati hasilnya

Anda akan melihat teks serupa dari tampilan data suhu dan kelembaban di serial monitor seperti yang ditunjukkan di bawah ini.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result1.png)

**Contoh 2** : Menggunakan layar LCD untuk menampilkan data dari sensor DHT11

Pertama Hubungkan Grove - modul LCD RGB Backlight ke port I2C dari Seeeduino Lotus catatan: itu adalah port I2C yang diikuti oleh satu titik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/DHT11_lcd.png)

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add DHT sensor library
#include <DHT.h>
//add LCD library
#include <rgb_lcd.h>

//set digital pin2 as DHTPIN
#define DHTPIN 2
//set the sensor type as DHT 11
#define DHTTYPE DHT11

/*assign dht as the name of DHT sensor
  set the sensor pin as DHTPIN(pin2),
  set the sensor type as DHTTYPE(DHT11)
*/
DHT dht(DHTPIN, DHTTYPE);

//assign lcd as the name of rgb_lcd screen
rgb_lcd lcd;

void setup() {
  //initialise the dht sensor
  dht.begin();
  //initialise the lcd screen;
  //set up the lcd's number of columns and rows:
  lcd.begin(16, 2);
  //wait for 2s
  delay(2000);
}

void loop() {
  //store the humidity value to h
  int h = dht.readHumidity();
  //store the temperature value to t(in Celsius)
  int t = dht.readTemperature();
  
  //set the LCD cursor to column 0, line 0
  lcd.setCursor(0, 0);
  //Print text temperature: to the LCD
  lcd.print("Temperature:");
  //set the LCD cursor to column 12, line 0
  lcd.setCursor(12, 0);
  //Print temperature value t to the LCD
  lcd.print(t);
  //set the LCD cursor to column 14, line 0
  lcd.setCursor(14, 0);
  //Print temperature º is character 223 on lookup table
  lcd.write(223);
  //Print C to the LCD
  lcd.print("C");
  
  //set the LCD cursor to column 0, line 1
  lcd.setCursor(0, 1);
  //Print text Humidity: to the LCD
  lcd.print("Humidity: ");
  //set the LCD cursor to column 10, line 1
  lcd.setCursor(10, 1);
  //Print humidity value h to the LCD
  lcd.print(h);
  //set the LCD cursor to column 12, line 1
  lcd.setCursor(12, 1);
  //Print sign % to the LCD
  lcd.print("%");
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Anda dapat melihat tampilan suhu dan kelembaban ruangan saat ini di layar LCD.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/DHT11_result.jpg)

**Penjelajahan Lebih Lanjut**

Setelah sesi ini, Anda dapat membuat stasiun cuaca sendiri dengan menggunakan sensor DHT11 dan Grove - LCD RGB Backlight display.

### Sesi 8: Grove - 3-Axis Digital Accelerometer

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/3_axis_cover.jpg)

**Tujuan**	

Mempelajari cara mengoperasikan 3-axis digital accelerometer dengan mengamati data output yang ditampilkan pada layar LCD.

**Inti Pengetahuan**

- Menggunakan serial monitor untuk menunjukkan nilai offset dan percepatan dari 3-axis accelerometer, menemukan hubungan antara data output dan posisi dari 3-axis accelerometer.
- Menggunakan data offset dari 3-axis accelerometer untuk menghitung nilai pitch dan roll, dan mengamati perubahan data relatif terhadap posisi dari 3-axis accelerometer.
- Pelajari cara menggunakan tilt switch untuk membalik di antara halaman layar LCD, sehingga data besar dari 3-axis accelerometer dapat ditampilkan dengan jelas.


**Persyaratan hardware (perangkat keras)**	

Persiapan

- kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang

Termasuk dalam kit

- Board Dev Seeeduino Lotus V1.1
- Kabel Grove
- Grove – 3-Axis Digital Accelerometer
- Grove - LCD RGB Backlight
- Grove – Tilt Switch	


**Koneksi hardware (perangkat keras)**

Langkah 1: Hubungkan modul Grove - 3-Axis Digital Accelerometer ke port I2C dari Seeeduino Lotus. Catatan: itu adalah port I2C diikuti oleh dua titik.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/3_axis_ard.jpg)

Langkah 2: Hubungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB.

**Pemrograman software (perangkat lunak)**

**Menambah Library**

Tambahkan [3-axis accelerometer driver Library](https://github.com/Seeed-Studio/Accelerometer_MMA7660/archive/master.zip) ke dalam Arduino IDE

**Contoh 1** : Menggunakan Serial Monitor untuk menampilkan data keluaran dari 3-axis accelerometer

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add accelemeter library
#include "MMA7660.h"

//assign accelemeter as the name of MMA7660 accelemeter
MMA7660 accelemeter;

void setup()
{
  //initialise the accelemeter
  accelemeter.init();
  // opens serial port, sets data rate to 9600 bps
  Serial.begin(9600);
}
void loop()
{
  //initialise x, y, z as int8_t
  int8_t x;
  int8_t y;
  int8_t z;
  //initialise ax, ay, az as float
  float ax, ay, az;
  //get x y z offset value from accelemeter
  accelemeter.getXYZ(&x, &y, &z);
  //display title x =
  Serial.print("x = ");
  //display value of x
  Serial.println(x);
  //display title y =
  Serial.print("y = ");
  //display value of y
  Serial.println(y);
  //display title z =
  Serial.print("z = ");
  //display value of z
  Serial.println(z);
  
  //get ax ay az acceleration value from accelemeter
  accelemeter.getAcceleration(&ax, &ay, &az);
  //display title accleration of X/Y/Z: 
  Serial.println("accleration of X/Y/Z: ");
  //display value of ax
  Serial.print(ax);
  //display unit g
  Serial.println(" g");
  //display value of ay
  Serial.print(ay);
  //display unit g
  Serial.println(" g");
  //display value of az
  Serial.print(az);
  //display unit g
  Serial.println(" g");
  //display ************* as divider to make thing prettier
  Serial.println("*************");
  //wait for 0.5s
  delay(500);
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Buka Serial Monitor

Langkah 4: Amati hasilnya

Harap perhatikan perubahan data dengan memposisikan 3-axis accelerometer seperti pada gambar di bawah ini.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result2.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result3.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result4.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result5.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result6.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result7.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result8.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result9.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result10.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result11.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result12.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result13.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result14.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result15.png)

**Contoh 2** : Menggunakan data dari 3-axis accelerometer untuk menghitung nilai Pitch dan Roll

Latar belakang pengetahuan :

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/aircraft.png)

seperti yang ditunjukkan pada gambar di atas:

Pitch (Sumbu melintang) θ: Berasal dari pusat gravitasi dan diarahkan ke kanan, sejajar dengan garis yang ditarik dari wingtip to wingtip. Gerakan tentang sumbu ini disebut pitch. Lift adalah kontrol utama pitch. (Aircraft principal axes 2018)

Yaw (Sumbu vertikal) ψ: Berasal dari pusat gravitasi dan diarahkan ke bagian bawah pesawat, tegak lurus terhadap sayap dan ke garis referensi badan pesawat. Gerak tentang sumbu ini disebut yaw. Gerakan menguap positif menggerakkan hidung pesawat ke kanan. Kemudi adalah kontrol utama yaw. (Aircraft principal axes 2018)

Roll (Sumbu longitudinal) Φ: Berasal dari pusat gravitasi dan diarahkan ke depan, sejajar dengan garis referensi badan pesawat. Gerak tentang sumbu ini disebut roll. Perpindahan sudut tentang sumbu ini disebut bank. [3] Gerakan memutar positif mengangkat sayap kiri dan menurunkan sayap kanan. (Aircraft principal axes 2018)

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

#include <Wire.h>
//add accelemeter library
#include "MMA7660.h"

//assign accelemeter as the name of MMA7660 accelemeter
MMA7660 accelemeter;

//set value 0.5 to alpha
const float alpha = 0.5;

//initialise fXg, fYg, fZg as double with value of 0
double fXg = 0;
double fYg = 0;
double fZg = 0;
//initialise pitch and roll as double
double pitch, roll;

void setup()
{
  //initialise the accelemeter
  accelemeter.init();
  // opens serial port, sets data rate to 9600 bps
  Serial.begin(9600);
}
void loop()
{
  //initialise x, y, z as int8_t
  int8_t x;
  int8_t y;
  int8_t z;
  //get x y z offset value from accelemeter
  accelemeter.getXYZ(&x, &y, &z);

  //Low Pass Filter to reduce the noise
  fXg = x * alpha + (fXg * (1.0 - alpha));
  fYg = y * alpha + (fYg * (1.0 - alpha));
  fZg = z * alpha + (fZg * (1.0 - alpha));

  //Roll & Pitch Equations
  roll  = (atan2(-fYg, fZg) * 180.0) / M_PI;
  pitch = (atan2(fXg, sqrt(fYg * fYg + fZg * fZg)) * 180.0) / M_PI;
  //display title roll =
  Serial.print("roll = ");
  //display the roll value
  Serial.println(roll);
  //display title pitch =
  Serial.print("pitch = ");
  //display the pitch value
  Serial.println(pitch);
  delay(500);
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Letakkan 3-axis accelerometer pada permukaan yang rata seperti yang ditunjukkan di bawah ini.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/3_axis.jpg)


Amati data Roll
Balik ke atas/bawah 3-axis accelerometer sesuai dengan panah hijau pada gambar di atas, sekarang nilai roll akan meningkat ketika Anda balik ke bawah, dan menurun saat balik ke atas. Selain itu, nilai roll bernilai positif ketika balik ke bawah (ditempatkan sejajar dengan level air), dan bernilai negatif ketika dibalik ke atas.

Amati data Pitch
Miringkan ke kiri/kanan 3-axis accelerometer sesuai dengan panah merah pada gambar di atas, sekarang nilai pitch harus meningkat ketika Anda memiringkan ke kanan, berkurang ketika miring ke kiri. Selain itu, nilai pitch positif ketika miring ke kanan (sejajar dengan level air), dan negatif bila miring ke kiri.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result2.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result16.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result10.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result17.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result8.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result18.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result4.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result19.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result6.jpg)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/result20.png)


Sekarang kita dapat menggunakan 3-axis accelerometer untuk mengontrol atau memperbaiki arah pesawat udara atau mobil, dengan menyelipkan data pitch and roll untuk mengontrol sinyal guna mengontrol aktuator. Teknologi yang sama diterapkan pada penyesuaian layar otomatis pada ponsel ketika Anda memiringkan ponsel dari portrait menjadi landscape.


**Contoh 3** : Menggunakan layar LCD untuk menampilkan data output dari 3-axis accelerometer

Hubungkan Grove - Tilt Switch ke port D5 Seeeduino Lotus, dan hubungkan Grove - LCD RGB Backlight module ke port I2C. dari Seeeduino Lotus, CATATAN: itu adalah port I2C yang diikuti oleh satu titik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/3_axis_lcd_tilt.jpg)

Di sini kita menggunakan tilt switch untuk membalik halaman pada layar LCD untuk menunjukkan set data yang berbeda, ketika tilt switch ON layar LCD akan menampilkan data X, Y, Z Roll dan Pitch. Ketika tilt switch pada posisi OFF posisi LCD Layar akan menampilkan data percepatan aX, aY, aZ di setiap arah secara relatif.

Langkah 1: Salin kode berikut ke dalam Arduino IDE

```C

//add accelemeter library
#include "MMA7660.h"
//add LCD library
#include <rgb_lcd.h>


//assign name tiltswitchPin to pin 5
#define tiltswitchPin 5

//assign accelemeter as the name of MMA7660 accelemeter
MMA7660 accelemeter;
//assign lcd as the name of rgb_lcd screen
rgb_lcd lcd;

//set value 0.5 to alpha
const float alpha = 0.5;

//initialise fXg, fYg, fZg as double with value of 0
double fXg = 0;
double fYg = 0;
double fZg = 0;
//initialise pitch and roll as double

void setup()
{
  //initialise the accelemeter
  accelemeter.init();
  //initialise the lcd screen;
  //set up the lcd's number of columns and rows:
  lcd.begin(16, 2);
  //set pinMode of tiltswitchPin to input
  pinMode(tiltswitchPin, INPUT);
  //wait for 2s
  delay(2000);

}
void loop()
{
  /*if tilt switch is on display X, Y, Z, Roll and Pitch data
    if tilt switch is off display X, Y, Z acceleration data
  */
  if (HIGH == digitalRead(tiltswitchPin))
  {
    //initialise x, y, z as int8_t, pitch and roll as double
    int8_t x;
    int8_t y;
    int8_t z;
    double roll;
    double pitch;
    //get x y z offset value from accelemeter
    accelemeter.getXYZ(&x, &y, &z);

    //Low Pass Filter to reduce the noise
    fXg = x * alpha + (fXg * (1.0 - alpha));
    fYg = y * alpha + (fYg * (1.0 - alpha));
    fZg = z * alpha + (fZg * (1.0 - alpha));

    //Roll & Pitch Equations
    roll  = (atan2(-fYg, fZg) * 180.0) / M_PI;
    pitch = (atan2(fXg, sqrt(fYg * fYg + fZg * fZg)) * 180.0) / M_PI;
    //reset the lcd screen
    lcd.clear();
    //set the LCD cursor to column 0, line 0
    lcd.setCursor(0, 0);
    //display text x:
    lcd.print("x:");
    //display value of x
    lcd.print(x);
    //set the LCD cursor to column 5, line 0
    lcd.setCursor(5, 0);
    //display text y:
    lcd.print("y:");
    //display value of y
    lcd.print(y);
    //set the LCD cursor to column 10, line 0
    lcd.setCursor(10, 0);
    //display text z:
    lcd.print("z:");
    //display value of z
    lcd.print(z);

    //set the LCD cursor to column 0, line 1
    lcd.setCursor(0, 1);
    //display text R:
    lcd.print("R:");
    //display value of roll
    lcd.print(roll);
    //set the LCD cursor to column 8, line 1
    lcd.setCursor(8, 1);
    //display text P:
    lcd.print("P:");
    //display value of pitch
    lcd.print(pitch);
  } else
  {
    //initialise ax, ay, az as float
    float ax, ay, az;
    //get ax ay az acceleration value from accelemeter
    accelemeter.getAcceleration(&ax, &ay, &az);
    //reset the lcd screen
    lcd.clear();
    //set the LCD cursor to column 0, line 0
    lcd.setCursor(0, 0);
    //display text ax:
    lcd.print("ax:");
    //display value of ax
    lcd.print(ax);
    //set the LCD cursor to column 8, line 0
    lcd.setCursor(8, 0);
    //display text ay:
    lcd.print("ay:");
    //display value of ay
    lcd.print(ay);
    //set the LCD cursor to column 0, line 1
    lcd.setCursor(0, 1);
    //display text az:
    lcd.print("az:");
    //display value of az
    lcd.print(az);
  }
  //wait 0.5s
  delay(500);
}

```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

Pertama, uji coba apakah tilt switch mengubah halaman layar LCD. Kemudian Anda dapat memutar 3-axis accelerometer untuk mengamati perubahan data sesuai dengan rotasi. Pahami mengenai data output yang terkait dengan orientasi 3-axis accelerometer.

Tampilkan kecepatan, pitch, dan roll saat tilt switch on/off:

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/3_axis_tilt_on&off.jpg)

**Penjelajahan Lebih Lanjut**

Setelah bermain-main dengan modul accelerometer digital, Anda dapat membayangkan bahwa accelerometer adalah salah satu modul terpenting yang dapat ditemukan dalam sistem panduan roket bersama dengan modul lain seperti GPS dan gyro dll. Accelerometer juga digunakan di ponsel untuk mendeteksi apakah Anda telepon dalam mode portrait menjadi mode landscape, sehingga layar dapat menyesuaikan sesuai posisinya.



### Sesi 9: Smart Garden


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/smartgarden.png)

**Tujuan**

Untuk membuat sensor dan sistem pengingat Smart Garden dengan menggabungkan modul Grove starter kit.

**Inti Pengetahuan**

- Belajar cara menggabungkan beberapa modul ke dalam satu aplikasi
- Belajar cara membuat kode untuk beberapa perangkat di Arduino IDE
- Memakai banyak modul untuk mendeteksi dan menganalisis lingkungan dari tanaman, dan meningkatkan keterampilan berpikir logis

**Menggunakan Analisis Kasus**

**Modul Sensor**

Gunakan modul DHT11 untuk memantau lingkungan sekitar tanaman, menggunakan sensor cahaya untuk mendeteksi intensitas cahaya di sekitarnya.


**Modul Aktuator**

Menggunakan buzzer untuk membuat nada dan LCD untuk memberi tahu pesan peringatan yang berbeda:

- peringatan 1: suhu sekitar lebih tinggi dari 38°C
- peringatan 2: kelembaban di sekitarnya lebih rendah dari 40%
- peringatan 3: Intensitas cahaya lebih rendah dari 50
- peringatan 4: ingatkan pengguna untuk menyiram tanaman


Menggunakan tampilan layar LCD:

- status 1: Tampilkan suhu
- status 2: Perlihatkan kelembaban
- status 3: ingatkan pengguna untuk menyiram tanaman

Gunakan tilt switch untuk mengatur ulang/Reset peringatan.

**Diagram Alir**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/flowchart.png)

**Persyaratan hardware (perangkat keras)**

Persiapan

	- Kabel micro-USB
	- Komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang
	- DIY Acrylic Frame


Termasuk dalam kit

	- Board Dev Seeeduino Lotus V1.1
	- Kabel Grove
	- Grove – Buzzer
	- Grove – Chainable RGB LED
	- Grove – Light Sensor
	- Grove - LCD RGB Backlight
	- Grove – Temperature &Humidity Sensor(DHT11)
	- Grove – Tilt Switch

**Koneksi perangkat keras**

Langkah 1: Hubungkan modul Grove - Buzzer ke port D6 Seeeduino Lotus

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/buzzer_ard.jpg)

Hubungkan Grove - LED RGB Chainable ke port D7 dari Seeeduino Lotus

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect1.jpg)

Hubungkan Grove - modul Light Sensor ke port A0 Seeeduino Lotus

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect2.jpg)

Hubungkan modul Grove - LCD RGB Backlight ke port I2C dari Seeeduino Lotus. Catatan: itu adalah port I2C diikuti oleh satu titik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect3.jpg)

Sambungkan modul Grove - Temperature & Humidity Sensor (DHT11) ke port D2 Seeeduino Lotus.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect4.jpg)

Hubungkan Grove - Tilt Switch ke port D5 Seeeduino Lotus.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect5.jpg)

Pasangkan semua komponen bersama pada DIY Acrylic Frame

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/smartgarden1.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/smartgarden2.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/smartgarden3.png)

Langkah 2: Hubungkan Seeeduino Lotus dengan komputer menggunakan kabel micro USB.


**Pemrograman perangkat lunak**

Langkah 1: Tambahkan [TimeLib Library](https://github.com/PaulStoffregen/Time/archive/master.zip) ke Arduino IDE
Untuk informasi lebih lanjut, silahkan kunjungi [Arduino TimeLib tutorial](http://playground.arduino.cc/code/time)

Langkah 2: Salin kode berikut ke dalam Arduino IDE

```C

//add DHT sensor library
#include <DHT.h>
//add LCD library
#include <rgb_lcd.h>
//add ChainableLED library to this project
#include <ChainableLED.h>
//add Timelib library
#include <TimeLib.h>

//assign default time as epoch time 1514764800 which is 00:00:00 Jan 1 2018
long DEFAULT_TIME = 1514764800;
long waterTime = DEFAULT_TIME + 86400;

//set the number of leds linked to the chain
#define NUM_LEDS  1

//assign LightSensor as A0
#define LightSensor A0
//set digital pin2 as DHTPIN
#define DHTPIN 2
//set title of pin 5 as tiltSwitch
#define tiltSwitch 5
//assign buzzer as pin 6
#define buzzer 6

//set the sensor type as DHT 11
#define DHTTYPE DHT11

/*assign dht as the name of DHT sensor
  set the sensor pin as DHTPIN(pin2),
  set the sensor type as DHTTYPE(DHT11)
*/
DHT dht(DHTPIN, DHTTYPE);

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

//assign lcd as the name of rgb_lcd screen
rgb_lcd lcd;

void setup()
{
  //
  setTime(DEFAULT_TIME);
  //initialise the dht sensor
  dht.begin();
  //initialise the lcd screen;
  //set up the lcd's number of columns and rows:
  lcd.begin(16, 2);
  //initialise ChainableLED leds
  leds.init();
  //set pin 5(tilt switch) as input pin
  pinMode(tiltSwitch, INPUT);
  delay(1000);
}
int mode = 0;
void loop()
{
  //-------------DHT---------------------
  //store the humidity value to h
  int h = dht.readHumidity();

  //store the temperature value to t(in Celsius)
  int t = dht.readTemperature();

  int value = analogRead(LightSensor);
  float value_float = map(value, 0, 800, 50, 0) / 100.0;

  leds.setColorHSB(0, 0, 0, value_float);

  //initialise mode to 0, then set to case 0;

  //temperature exceed 38 degrees, then set to case 1;
  if (t > 38) {
    mode = 1;
  }
  //Humidity is less than 40 %, then set to case 2;
  if (h < 40)
  {
    mode = 2;
  }
  //LightSensor reading value is less than 50, then set to case 3;
  if (value < 50)
  {
    mode = 3;
  }
  //current time is greate or equals to waterTime(24 hour ahead), then set to case 4;
  if (now() >= waterTime  ) {
    mode = 4;
  }

  switch (mode) {
    case 0:
      //set the LCD cursor to column 0, line 0
      lcd.clear();
      lcd.setCursor(0, 0);
      //Print text temperature: to the LCD
      lcd.print("Temperature:");
      //set the LCD cursor to column 12, line 0
      lcd.setCursor(12, 0);
      //Print temperature value t to the LCD
      lcd.print(t);
      //set the LCD cursor to column 14, line 0
      lcd.setCursor(14, 0);
      //Print temperature º is character 223 on lookup table
      lcd.write(223);
      //Print C to the LCD
      lcd.print("C");

      //set the LCD cursor to column 0, line 1
      lcd.setCursor(0, 1);
      //Print text Humidity: to the LCD
      lcd.print("Humidity: ");
      //set the LCD cursor to column 10, line 1
      lcd.setCursor(10, 1);
      //Print humidity value h to the LCD
      lcd.print(h);
      //set the LCD cursor to column 12, line 1
      lcd.setCursor(12, 1);
      //Print sign % to the LCD
      lcd.print("%");
      break;
    case 1:
      tone(buzzer, 262, 300);
      leds.setColorRGB(0, 255, 0, 0);
      lcd.clear();
      lcd.setCursor(0, 0);
      lcd.print("Temperature too ");
      lcd.setCursor(0, 1);
      lcd.print("High!!");
      if (HIGH == digitalRead(tiltSwitch))
      {
        leds.setColorRGB(0, 0, 0, 0);
        mode = 0;
      }
      break;
    case 2:
      tone(buzzer, 294, 300);
      leds.setColorRGB(0, 255, 0, 0);
      lcd.clear();
      lcd.setCursor(0, 0);
      lcd.print("Warning! Too Dry");
      if (HIGH == digitalRead(tiltSwitch))
      {
        leds.setColorRGB(0, 0, 0, 0);
        mode = 0;
      }
      break;
    case 3:
      tone(buzzer, 330, 300);
      leds.setColorRGB(0, 255, 0, 0);
      lcd.clear();
      lcd.setCursor(0, 0);
      lcd.print("Not Enough Light");
      lcd.setCursor(0, 1);
      lcd.print("Check the LED..");
      if (HIGH == digitalRead(tiltSwitch))
      {
        leds.setColorRGB(0, 0, 0, 0);
        mode = 0;
      }
      break;
    case 4:
      tone(buzzer, 349, 300);
      leds.setColorRGB(0, 255, 0, 0);
      lcd.clear();
      lcd.setCursor(0, 0);
      lcd.print("Time to water");
      lcd.setCursor(0, 1);
      lcd.print("the plants");
      if (HIGH == digitalRead(tiltSwitch))
      {
        waterTime = now() + 86400;
        mode = 0;
      }
      break;

  }
}

```

Langkah 3: Unggah kode ke Seeeduino Lotus

Langkah 4: Amati hasilnya

Dalam kondisi normal, LED menyinari cahaya putih dan layar LCD menunjukkan suhu dan kelembaban.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden.png)

4 status peringatan

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden1.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden2.png)
![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden3.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden4.png)

Peringatan LED merah

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden5.png)

Setel ulang/Reset peringatan dengan menggunakan tilt switch

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden6.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/garden7.png)



### Sesi 10: Smart Cup

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/smartcup.png)

**Tujuan**

Membuat smart cup dengan menggunakan buzzer, LED RGB, 3-Axis Accelerometer dan layar LCD. Smart cup akan mengingatkan pengguna untuk minum air pada periode waktu tertentu. Smart cup juga dapat mendeteksi jika pengguna mengkonsumsi air, layar LCD akan menampilkan waktu hitung mundur untuk mengingatkan pengguna kapan waktu berikutnya untuk minum air.


**Inti Pengetahuan**

- Pemeriksaan Library TimeLib pada pengaturan dan kontrol waktu dengan Lotus.
- Memperbaiki tampilan dan teks bergulir pada layar LCD
- Memperbaiki operasi if…else…and switch…case… dengan operator logika ||(atau) dan &&(dan).
- lebih lanjut memeriksa aplikasi membaca nilai pitch and roll dari 3-Axis Accelerometer.
- Menggunakan contoh BlinkWithoutDelay untuk menghindari penggunaan fungsi delay yang mencegah fungsi penundaan melewatkan timer sistem.
- Mempelajari cara membuat dan memanggil fungsi yang disesuaikan, hasil kembali bisa Boolean(true/false), atau nilai variabel dengan menggunakan return X.

**Menggunakan Analisa Kasus**

**Modul Sensor**

Membandingkan data pitch and roll dari pembacaan 3-axis accelerometer untuk mendeteksi apakah botol dimiringkan atau tidak. Oleh karena itu, proyek ini  akan mengenali apakah pengguna minum air atau tidak. jika botol dimiringkan, langkah selanjutnya adalah mendeteksi apakah botol telah diletakkan kembali di atas meja, begitu botol berada di atas meja, data pitch and roll dari 3-axis accelerometer akan mengkalibrasi nilai maksimum dan minimum untuk membandingkan.

**Modul Aktuator**

Menggunakan buzzer untuk membuat nada yang berbeda untuk mengingatkan kondisi yang berbeda:

- status 1: saat penghitung waktu mundur 30 menit selesai, buzzer akan mengingatkan pengguna untuk minum air.
- status 2: buzzer akan berdengung jika botol tidak berada di atas meja.

Menggunakan tampilan layar LCD

- status 1: menghitung mundur timer
- status 2: ingatkan pengguna untuk minum air
- status 3: memberi selamat kepada pengguna karena telah minum air
- status 4: memberi informasi kepada pengguna untuk mengembalikan air setelah selesai minum


**Diagram Alir**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/flowchart1.png)

**Persyaratan hardware (perangkat keras)**	

Persiapan

- kabel micro-USB
- komputer dengan Arduino IDE dan driver serial-to-USB yang sudah terpasang

Termasuk dalam kit

- Board Dev Seeeduino Lotus V1.1
- Kabel Grove
- Grove – Buzzer
- Grove – LED Chainable RGB LED
- Grove - LCD RGB Backlight
- Grove – 3-Axis Digital Accelerometer

**Koneksi hardware (perangkat keras)**

Langkah 1: Hubungkan modul Grove - Buzzer ke port D6 Seeeduino Lotus


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/buzzer_ard.jpg)

Hubungkan Grove - LED RGB Chainable ke port D7 dari Seeeduino Lotus

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect1.jpg)


Hubungkan modul Grove - LCD RGB Backlight ke port I2C dari Seeeduino Lotus. Catatan: itu adalah port I2C diikuti oleh satu titik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect6.jpg)
 
Hubungkan modul Grove - 3-Axis Digital Accelerometer ke port I2C dari Seeeduino Lotus. Catatan: itu adalah port I2C diikuti oleh dua titik.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/connect7.jpg)

Pasang semua komponen menjadi satu pada gelas.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/smartcup.png)

**Pemrograman software (perangkat lunak)**

Langkah 1: Tambahkan [TimeLib Library](https://github.com/PaulStoffregen/Time/archive/master.zip) ke Arduino IDE

Salin kode berikut ke dalam Arduino IDE

```C

//add LCD library
#include <rgb_lcd.h>
//add accelerometer library
#include "MMA7660.h"
//add Timelib library
#include <TimeLib.h>
//add ChainableLED library to this project
#include <ChainableLED.h>

//assign default time as epoch time 1514764800 which is 00:00:00 Jan 1 2018
long DEFAULT_TIME = 1514764800;
//set drinkTime at 30mins(1800s) after default time
//long drinkTime = DEFAULT_TIME + 1800;
long drinkTime = DEFAULT_TIME + 10;
int lastDrink, seconds;
//will store lastest time in milliseconds
unsigned long previousMillis = 0;

//set the number of leds linked to the chain
#define NUM_LEDS  1

//assign buzzer as pin 6
#define buzzer 6

//assign accelerometer as the name of MMA7660 accelerometer
MMA7660 accelerometer;

//assign lcd as the name of rgb_lcd screen
rgb_lcd lcd;

/*assign leds as the name of
  the ChainableLED set the
  pin of the ChainableLED to
  pin7(clock pin) and pin8(data pin)
  and number of the leds*/
ChainableLED leds(7, 8, NUM_LEDS);

//set motion check tolerance value
int tolerance = 50;
//initalise the calibrated and moveDetedted as false
boolean calibrated = false;
boolean moveDetected = false;

//set int8_t for accelerometer reading value x, y, z
int8_t x;
int8_t y;
int8_t z;

//initialise fXg, fYg, fZg as double with value of 0
double fXg = 0;
double fYg = 0;
double fZg = 0;
//initialise pitch and roll as double
double p, r;

//Accelerometer limits
double rMin; //Minimum roll Value
double rMax; //Maximum roll Value
double rVal; //Current roll Value

double pMin; //Minimum pitch Value
double pMax; //Maximum pitch Value
double pVal; //Current pitch Value

//set value 0.5 to alpha for low pass filter tolerance
const float alpha = 0.5;

//iinitialise mode to set the default switch case to first(count from 0)
int mode = 0;

void setup()
{
  //set the system time to 00:00:00 Jan 1 2018
  setTime(DEFAULT_TIME);
  //initialise the accelerometer
  accelerometer.init();
  //initialise ChainableLED leds
  leds.init();
  //initialise the lcd screen;
  //set up the lcd's number of columns and rows:
  lcd.begin(16, 2);
  //calibrate the accelerometer for at the begining
  calibrateAccel();
  //wait for 2
  delay(2000);
}

//setup accelerometer reading function output mapped value of roll and pitch
void Accel() {
  accelerometer.getXYZ(&x, &y, &z);

  //Low Pass Filter to reduce the noise
  fXg = x * alpha + (fXg * (1.0 - alpha));
  fYg = y * alpha + (fYg * (1.0 - alpha));
  fZg = z * alpha + (fZg * (1.0 - alpha));

  r  = (atan2(-fYg, fZg) * 180.0) / M_PI;
  p = (atan2(fXg, sqrt(fYg * fYg + fZg * fZg)) * 180.0) / M_PI;
  r = map(r, -90, 90, 0, 180);
  p = map(p, -90, 90, 0, 180);
  return r;
  return p;
}

//setup function for calibrate the accelerometer
void calibrateAccel() {
  //reset moveDetected to false
  moveDetected = false;

  //call accelerometer reading funtion
  Accel();

  //assign the reading of roll and pitch
  rVal = r;
  rMin = rVal;
  rMax = rVal;

  pVal = p;
  pMin = pVal;
  pMax = pVal;

  //calibrate the Accelerometer
  for (int i = 0; i < 50; i++) {
    //call accelerometer reading funtion
    Accel();
    /*--calibrate roll---*/
    //assign the reading of roll to rVal
    rVal = r;
    //evaluate if the new reading is greater than stored Maximum value
    if (rVal > rMax) {
      //if new reading value is greater save new value to rMax
      rMax = rVal;
      //evaluate if the new reading is less than stored Minimum value
    } else if (rVal < rMin) {
      //if new reading value is less save new value to rMin
      rMin = rVal;
    }

    /*--calibrate pitch---*/
    //assign the reading of pitch to pVal
    pVal = p;
    //evaluate if the new reading is greater than stored Maximum value
    if (pVal > pMax) {
      //if new reading value is greater save new value to pMax
      pMax = pVal;
      //evaluate if the new reading is less than stored Minimum value
    } else if (pVal < pMin) {
      //if new reading value is less save new value to pMin
      pMin = pVal;
    }
    //Delay 10ms between readings
    delay(10);
  }
  //set the calibrated to true
  calibrated = true;
}

//drinking function check if the bottle is tilting output ture/false
boolean drinking() {
  //initialise tilting as false
  boolean tilting = false;
  //reading from accelerometer
  Accel();

  rVal = r;
  pVal = p;
  /*evaluate if new roll value is greater than the maximum value or
     less than the minimum value saved previously.
     || means or
     if rolling is happening then set tilting to ture
     if pitch is happening then set tilting to ture
  */
  if (rVal > (rMax + tolerance) || rVal < (rMin - tolerance)) {
    tilting = true;
  }

  if (pVal > (pMax + tolerance) || pVal < (pMin - tolerance)) {
    tilting = true;
  }
  //output tilting
  return tilting;
}

//mothin function
void Motion() {
  //don't check for movement until recalibrated again
  calibrated = false;
}

void loop()
{
  /*evaluate if current time is greate or equals
    to drinkTime(30mins ahead), then switch to case 1;
    its time to drink
  */
  if (now() >= drinkTime  ) {
    //switch to case 1
    mode = 1;
  }
  //evaluate if the accelerometer is calibrated
  if (calibrated) {
    //evaluate if the bottle is tilted
    if (drinking()) {
      //switch to case 2
      mode = 2;
      //set moveDetected to true
      moveDetected = true;
    }
  }
  //evaluate if the moveDetected is true
  if (moveDetected) {
    //call motion function
    Motion();
  }
  //save current time in millisecond
  unsigned long currentMillis = millis();
  switch (mode) {
    /*Case 0:
      mode to display countdonw time if nothing happened
    */
    case 0:
      //minutes to drink water
      lastDrink = (drinkTime - now()) / 60;
      //seconds to drink water
      seconds = (drinkTime - now()) % 60;

      leds.setColorHSB(0, 0, 0, 0);

      /*refesh the LCD for 1s without using delay, refer
         to Example "BlinkWithoutDelay", so the system
         won't stop and wait
      */
      if (currentMillis - previousMillis >= 1000) {
        // save the last time you refreshed the LCD
        previousMillis = currentMillis;
        lcd.clear();
        lcd.setCursor(0, 0);
        lcd.print("Countdown to dri");
        lcd.setCursor(0, 1);
        lcd.print("nk water: ");
        lcd.setCursor(10, 1);
        lcd.print(lastDrink);
        lcd.print(":");
        lcd.print(seconds);
      }
      break;
    /*Case 1:
       reached 30mins time to drink some water
       with buzzer alarm and LCD display time
       to drink some water
    */
    case 1:
      tone(buzzer, 262, 300);
      leds.setColorRGB(0, 255, 0, 0);
      lcd.clear();
      lcd.setCursor(0, 0);
      lcd.print("Time to drink");
      lcd.setCursor(0, 1);
      lcd.print("Some water");
      break;
    /*Case 2:
       detect if the wate bottle is tilted
       therefore user is drinking some water
       and recalibrate the sensor(accelerometer)
       once the bottle has been put on a flat
       surface if the bottle is still tilted or
       not sitting flat(accelerometer reading
       is not around 90 degrees), enter case 3
       detected the bottle is resting still enter
       to case 0 and reset the drink time to 30mins
       ahead
    */
    case 2:
      //stop buzzer
      noTone(buzzer);
      //update drinkTime
      drinkTime = now() + 1800;
      leds.setColorRGB(0, 0, 255, 0);
      //display message
      lcd.clear();
      lcd.setCursor(0, 0);
      lcd.print("Well Done remind");
      lcd.setCursor(0, 1);
      lcd.print("you in 30mins");
      //wait for 5s for user to drink
      delay(5000);
      //reading accelerometer value
      Accel();
      //evaluate if the bottle is resting on flat
      if (r > 80 && r < 100 && p > 80 && p < 100) {
        //evaluate if the accelerometer calibrated
        if (!calibrated) {
          //calibrate accelerometer
          calibrateAccel();
        }
        else
        { //switch to mode 0
          mode = 0;
          //update drinkTime
          drinkTime = now() + 1800;
          leds.setColorRGB(0, 0, 0, 0);
        }
      }
      else
      { //if bottle is not resting on flat switch to mode 3
        mode = 3;
        leds.setColorRGB(0, 0, 0, 0);
      }
      break;
    /*case 3
       if the bottle is not resting on flat surface,
       display message with scrolling "plaase put
       down water bottle when finished!", then check
       if the bottle is resting still, if so, recalibrate
       accelerometer and once recalibrated switch back to
       case 0 and reset drink time to 30mins ahead
    */
    case 3:
      //update drinkTime
      drinkTime = now() + 1800;

      leds.setColorRGB(0, 0, 0, 255);
      //display message with autoscroll
      lcd.clear();
      lcd.setCursor(0, 0);
      lcd.print("Please put down water");
      lcd.setCursor(0, 1);
      lcd.print("bottle when finished!");
      for (int positionCounter = 0; positionCounter < 5; positionCounter++) {
        // scroll one position left:
        lcd.scrollDisplayLeft();
        // wait a bit:
        delay(200);
      }
      for (int positionCounter = 0; positionCounter < 5; positionCounter++) {
        // scroll one position right:
        lcd.scrollDisplayRight();
        // wait a bit:
        delay(200);
      }
      for (int positionCounter = 0; positionCounter < 5; positionCounter++) {
        // scroll one position left:
        lcd.scrollDisplayLeft();
        // wait a bit:
        delay(200);
      }

      //reading accelerometer value
      Accel();
      //evaluate if the bottle is resting on flat
      if (r > 80 && r < 100 && p > 80 && p < 100) {
        //evaluate if the accelerometer calibrated
        if (!calibrated) {
          //calibrate accelerometer
          calibrateAccel();
        }
        else
        { //switch to mode 0
          mode = 0;
          //update drinkTime
          drinkTime = now() + 1800;
          leds.setColorRGB(0, 0, 0, 0);
        }
      }
      break;
  }
  delay(1);
}


```

Langkah 2: Unggah kode ke Seeeduino Lotus

Langkah 3: Amati hasilnya

4 Keadaan pada smart cup

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/cup1.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/cup2.png)


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/cup3.png)![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_Arduino/master/img/cup4.png)


## Referensi

Aircraft principal axes. Diakses pada 27 November 2018. https://en.wikipedia.org/wiki/Aircraft_principal_axes.

## LAMPIRAN

Semua [Kode](https://github.com/peterpanstechland/Grove_starter_kit.git) dalam dokumen ini tersedia di Github.

## BANTUAN / TECH SUPPORT

Harap jangan ragu untuk mengirim masukan masalah kepada kami lewat [forum](https://forum.seeedstudio.com/) atau kirim E-Mail ke [techsupport@seeed.cc](techsupport@seeed.cc).<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>