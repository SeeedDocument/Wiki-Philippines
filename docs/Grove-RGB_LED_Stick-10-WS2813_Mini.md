---
name: Grove - RGB LED Stick (10 WS2813 Mini)
category: Sensor
bzurl: 
oldwikiname: 
prodimagename:
surveyurl: 
sku: 104020131
tags:
---

![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/main.jpg)

Kami mengintegrasikan 10 LED RGB penuh warna pada stick ini, dengan hanya satu pin sinyal anda dapat mengontrol semua LED dengan mudah. Semua LED adalah WS2813 Mini, yang merupakan LED dengan kontrol cerdas dan hemat biaya.

Terlebih lagi, WS2813 mendukung transmisi sinyal breakpoint kontinu, yang berarti Anda dapat terus menggunakan led lain dengan salah satu led rusak.

Anda dapat menggunakan stick kecil ini untuk menciptakan ratusan ribu efek cahaya, kami berharap ini akan membuat Anda merasa lebih menyenangkan.


<p style=":center"><a href="https://www.seeedstudio.com/Grove-RGB-LED-Stick-10-WS2813-Min-p-3226.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>

## Versi

| Versi Produk  | Perubahan                                                                                               | Tanggal Dirilis |
|------------------|-------------------------------------------------------------------------------------------------------|---------------|
| Grove - RGB LED Stick (10 WS2813 Mini) | Initial                                                                                               | Nov 2018      |

## Fitur

- WS2813B IC, 3535 LED
- Intelligent Reverse-connection protection.
- The gray levels of each pixel are of 256, which achieves “256*256*256=16777216” full-color display.
- Refresh frequency mencapai 2KHz
- Serial cascade interface, data receiving and decoding bergantung hanya pada satu jalur sinyal.
- Dual-signal wires version, signal break-point continuous transmission.


### Signal break-point continuous transmission

![](https://github.com/SeeedDocument/Outsourcing/raw/master/104020108/img/LED_RFBP.jpg)

Selama tidak ada dua atau lebih LED yang berdekatan rusak, maka LED yang tersisa akan dapat berfungsi secara normal.


## Spesifikasi

|Item|Nilai|
|---|---|
|Tegangan operasi|3.3V / 5V|
|Suhu Operasional|-25℃ ~ +85℃|
|Suhu penyimpanan|-40℃ ~ +105℃|
|RGB Channel Arus Konstan|16mA|
|Antarmuka|Digital|
|Ukuran|L: 80mm W: 10mm H: 10mm| 
|Berat|3.7g|
|Ukuran paket|L: 150mm W: 100mm H: 25mm|
|Berat kotor|13g|


## Typical Applications

- Dekorasi natal
- Penerangan
- Mainan


## Hardware Overview

### Pin Keluaran

![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/pin_out.jpg)



## Platform yang Didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |


!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan modul perangkat lunak  atau kesesuaian secara teori. Kami hanya menyediakan library atau contoh-contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Mulai


### Bermain dengan Arduino


#### Perangkat Keras
**Bahan yang dibutuhkan**

| Seeeduino V4.2 | Base Shield | Grove - RGB LED Stick (10 WS2813 Mini) |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/thumbnail.jpg)|
|<a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Dapatkan sekarang</a>|<a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Dapatkan sekarang</a>|<a href="https://www.seeedstudio.com/Grove-RGB-LED-Stick-10-WS2813-Min-p-3226.html" target="_blank">Dapatkan sekarang</a>|


!!!Catatan
    **1** Harap sambungkan kabel USB dengan hati-hati, jika tidak Anda bisa saja merusak port. Silakan gunakan kabel USB dengan 4 kabel di dalamnya, kabel USB dengan 2 kabel tidak dapat digunakan untuk mentransfer data. Jika Anda tidak yakin dengan kabel USB yang Anda miliki, Anda dapat klik [disini](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html) untuk membelinya.
    
    **2** Setiap modul Grove dilengkapi dengan kabel Grove saat Anda membelinya. Jika Anda kehilangan kabel Grove, Anda bisa mengklik [disini](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html) untuk membelinya.


!!!Penting
    **1**. Jika Anda menggunakan Arduino UNO sebagai motherboard, disarankan menggunakan catu daya DC. Jika tidak, tegangan ripple maksimum pada VCC dapat melebihi 100mV. Jika Anda menggunakan Seeeduino V4.2 sebagai motherboard, Anda tidak perlu menghubungkan daya DC.

    **2**. Hot swap tidak didukung.


- **Langkah 1.** Hubungkan Grove - RGB LED Stick (10 WS2813 Mini) ke port **D6** dari Grove-Base Shield.

- **Langkah 2.** Pasang Grove - Base Shield ke Seeeduino.

- **Langkah 3.** Hubungkan Seeeduino ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/connect.jpg)

!!!Catatan
        Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan modul ini ke Seeeduino seperti di bawah ini.


| Seeeduino      |  Kabel Grove       | Grove - RGB LED Stick (10 WS2813 Mini) |
|--------------- |--------------------|-----|
| GND            | Black              | GND |
| 5V or 3.3V     | Red                | VCC |
| Tidak ada koneksi           | White              | NC |
| D6            | Yellow             | SIG |



#### Perangkat Lunak

!!!Perhatian
        Jika ini adalah pertama kalinya Anda menggunakan Arduino, kami sangat menyarankan Anda untuk melihat [Memulai dengan Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


- **Langkah 1.** Unduh [Led_Strip](https://github.com/Seeed-Studio/Seeed_Led_Strip) Library dari Github.

- **Langkah 2.** Mengacu pada [Cara menginstall library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) untuk melakukan instalasi library pada Arduino.

- **Langkah 3.** Nyalakan ulang Arduino IDE. Buka contoh programnya, Anda dapat membukanya dengan tiga cara berikut：
    1. Buka langsung di Arduino IDE melalui langkah : **File --> Examples --> Adafruit_Neopixel --> simple**. 
    ![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/path1.jpg)
    
    2. Buka di komputer Anda dengan mengklik **simple.ino** yang dapat Anda temukan di folder **XXXX\Arduino\libraries\Seeed_Led_Strip-master\examples\simple**, **XXXX** adalah lokasi Anda menginstal Arduino IDE.
    ![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/path2.jpg)
    
    3. Atau, Anda bisa mengklik ikon ![](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/copy.jpg) di sudut kanan atas blok kode untuk menyalin kode berikut ke sketsa baru di Arduino IDE.


```C++
// NeoPixel Ring simple sketch (c) 2013 Shae Erisson
// dirilis dibawah lisensi GPLv3 agar sesuai dengan library AdaFruit NeoPixel

#include "Adafruit_NeoPixel.h"
#ifdef __AVR__
  #include <avr/power.h>
#endif

// Pin mana pada Arduino yang terhubung ke NeoPixels?
// Pada Trinket atau Gemma kami menyarankan untuk mengubahnya ke 1
#define PIN            6

// Berapa banyak NeoPixels yang terpasang pada Arduino?
#define NUMPIXELS      10

// Ketika kita mengatur library NeoPixel, kita beri tahu berapa piksel, dan pin mana yang digunakan untuk mengirim sinyal.
// Perhatikan bahwa untuk strip NeoPixel dengan versi lebih lama Anda mungkin perlu mengubah parameter ketiga - lihat strandtest
// contoh untuk informasi lebih lanjut tentang nilai yang memungkinkan.
Adafruit_NeoPixel pixels = Adafruit_NeoPixel(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);

int delayval = 500; // tunda selama setengah detik

void setup() {
  // Baris ini untuk Trinket 5V 16MHz, Anda dapat menghapus tiga baris ini jika Anda tidak menggunakan Trinket
#if defined (__AVR_ATtiny85__)
  if (F_CPU == 16000000) clock_prescale_set(clock_div_1);
#endif
  // Akhir kode khusus trinket
  pixels.setBrightness(255);
  pixels.begin(); // Melakukan inisialisasi library NeoPixel .
}

void loop() {

  // Untuk satu set NeoPixels, NeoPixel pertama adalah 0, kedua adalah 1, sampai jumlah piksel dikurangi satu.

  for(int i=0;i<NUMPIXELS;i++){

    // pixels.Color mengambil nilai RGB, dari 0,0,0 hingga 255,255,255
    pixels.setPixelColor(i, pixels.Color(0,150,0)); // Warna hijau cukup cerah.

    pixels.show(); // Ini mengirimkan warna piksel yang diperbarui ke perangkat keras.

    delay(delayval); // Tertunda selama periode waktu (dalam milidetik).

  }
}
```

!!!Perhatian
       File library dapat diperbarui. Kode ini mungkin tidak berlaku untuk file library versi terbaru, jadi sebaiknya Anda menggunakan dua metode pertama.


- **Langkah 4.** Unggah kode demo. Jika Anda tidak tahu cara mengunggah kode, silakan cek [Cara mengunggah kode](http://wiki.seeedstudio.com/Upload_Code/).



!!!Sukses
        Jika semuanya berjalan dengan baik, sekarang Anda dapat melihat LED strip bersinar:


![](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/img/test20181210_162208.gif)


## Sumber-sumber

- **[Zip]** [Grove - RGB LED Stick (10 WS2813 Mini) Eagle Files](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/res/Grove%20-%20RGB%20LED%20Stick%20(10-WS2813%20Mini).zip)

- **[Zip]** [Led_Strip Library](https://github.com/Seeed-Studio/Seeed_Led_Strip/archive/master.zip)

- **[PDF]** [Datasheet WS2813-Mini](https://github.com/SeeedDocument/Grove-RGB_LED_Stick-10-WS2813_Mini/raw/master/res/WS2813-Mini.pdf)




## Tech Support / Bantuan

Harap jangan ragu untuk mengirim masukan masalah kepada kami melalui [forum](https://forum.seeedstudio.com/)<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="<img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" />" /></a></p>