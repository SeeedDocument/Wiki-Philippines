---
name: Grove - Vibration Sensor (SW-420)
category: Sensor
bzurl: 
oldwikiname: 
prodimagename:
surveyurl: 
sku: 101020586
tags:
---

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/main.jpg)

The Grove - Vibration Sensor (SW-420) adalah sensor getaran non-directional dengan sensitivitas yang tinggi. Ketika modul ini dalam keadaaan stabil, rangkaian akan bekerja dan menghasilkan output berlogika high. Ketika terjadi gerakan atau getaran, rangkaian akan tertutup sebentar dan menghasilkan output berlogika low. Pada saat yang sama, Anda juga dapat menyesuaikan sensitivitas sesuai dengan kebutuhan..

Secara keseluruhan, ini adalah modul yang sempurna untuk sensor getaran atau kemiringan.


<p style=":center"><a href="https://www.seeedstudio.com/Grove-Vibration-Sensor-%28SW-420%29-p-3158.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>

## Versi

| Produk Versi  | Perubahan                                                                                               | Tanggal Rilis |
|------------------|-------------------------------------------------------------------------------------------------------|---------------|
| Grove - Vibration Sensor (SW-420) | Initial                                                                                               | Sep 2018      |

## Fitur

- Non-directional
- Sensitifitas tinggi
- Responsif terhadap getaran, dimiringkan
- Tahan air
- Compression resistance


## Spesifikasi

|Parameter|Nilai|
|---|---|
|Tegangan Kerja|3.3V / 5V|
|Antarmuka|Digital|
|Ukuran|L: 40mm W: 20mm H: 10mm| 
|Berat|4.3g|
|Ukuran Kemasan|L: 140mm W: 85mm H: 10mm|
|Berat Keseluruhan|10g|


## Aplikasi

- Mobil, sepeda, sepeda motor dengan alat tanda bahaya
- Game control
- Deteksi gerakan

## Deskripsi Hardware (Perangkat Keras)

### Pin Map

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/pin_map.jpg)


### Skematik

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/Schematic.jpg)


Pertama, mari kita mulai dengan **SW1** yang di sudut kiri bawah. Sebenarnya, **SW1** adalah modul getaran **SW-420**. Ketika modul dalam keadaan stabil, modul dihidupkan. **Pin2** dari **U1A** terhubung ke **GND** melalui **SW1**.

**VR1** adalah potensiometer, **Pin2** dari potensiometer terhubung ke **Pin3** dari **U1A**

**U1A** adalah [comparators](https://en.wikipedia.org/wiki/Comparator). Untuk komparator, 


$$
V_{out} = 
\begin{cases} 
High,  & \mbox{if }V_+ > V_-  \\
Low,  & \mbox{if }V_+ < V_- 
\end{cases}
$$

**V+** terhubung ke **Pin3**, **V-** terhubung ke **Pin2**, **V<sub>out</sub>** terhubung ke **Pin1**.

Untuk **V+** Anda dapat menyesuaikannya dengan memutar potensiometer, misalnya, kita dapat membuatnya $VCC/2$.

Untuk **V-**, itu tergantung pada **SW1(SW-420)**:

- Jika modul ini dalam keadaan stabil, **SW1** akan bekerja, Pin2 dari **U1A** terhubung dengan **GND** melalui **SW1**. Itu akan terjadi seperti ini:


$$
\left. \begin{array}{l}  & V- = 0V \\ & V+ = VCC/2 \end{array} \right\}  V_{out} = High
$$


- Jika modul bergetar atau miring, **SW1** akan bekerja, tegangan pada **V-** akan ditarik oleh **VCC** hingga R1. Setelah **V-** lebih tinggi dari VCC / 2, maka:

$$
\left. \begin{array}{l}  & V- > VCC/2 \\ & V+ = VCC/2 \end{array} \right\}  V_{out} = Low
$$


Sekarang Anda bisa mengatur **V+** untuk menyesuaikan nilai sensitifitasnya, perlu diingat: semakin rendah tegangan **V+**, semakin tinggi sensitifitasnya😆




## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg)  |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.



## Memulai


### Bermain dengan Arduino


#### Hardware (Perangkat Keras)

**Bahan yang dibutuhkan**

| Seeeduino V4.2 | Base Shield | Grove - Vibration Sensor|Grove - Buzzer|
|--------------|-------------|-----------------|----|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/thumbnail.jpg)|![](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/img/buzzer_s.jpg)|
|<a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Grove-Vibration-Sensor-%28SW-420%29-p-3158.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Grove-Buzzer-p-768.html" target="_blank">Dapatkan Sekarang</a>|


!!!note
    **1** Harap sambungkan kabel USB dengan hati-hati, jika tidak Anda dapat merusak port-nya. Silakan gunakan kabel USB dengan 4 kabel di dalamnya, karena kabel USB yang hanya mempunyai 2 kabel tidak dapat mentransfer data. Jika Anda tidak yakin dengan kabel yang Anda miliki, Anda dapat mengklik [here](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html) untuk membeli.
    
    **2** Setiap modul Grove dilengkapi dengan kabel Grove saat Anda membeli. Jika Anda kehilangan kabel Grove, Anda bisa mengklik [here](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html) untuk membeli.



- **Langkah 1.** Hubungkan Grove - Vibration Sensor (SW-420) ke port **D2** dari Base Shield.

- **Langkah 2.** Hubungkan Grove - Buzzer ke port **D3** dari modul Base Shield.

- **Langkah 3.** Pasangkan modul Grove - Base Shield ke Seeeduino.

- **Langkah 4.** Hubungkan Seeeduino ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/img/connect.JPG)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan modul ke Seeeduino seperti dibawah ini.



| Seeeduino     |  Grove - Vibration Sensor         |
|---------------|-------------------------|
| 5V            | Merah                     |
| GND           | Hitam                   |
| NC           | Putih                   |
| D2           | Kuning                   |



| Seeeduino     |  Grove - Buzzer         |
|---------------|-------------------------|
| 5V            | Merah                     |
| GND           | Hitam                   |
| NC           | Putih                   |
| D3           | Kuning                   |


#### Software (Perangkat Lunak)

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Arduino, kami sangat menyarankan Anda untuk melihat [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


- **Langkah 1.** Buka Arduino IDE Anda, dan buka lembar kerja baru.

- **Langkah 2.** Salin semua kode di bawah ini, atau Anda cukup mengklik gambar ![](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/copy.jpg) di sudut kanan atas blok kode untuk menyalin kode berikut ke lembar kerja baru.

```C++
// constants won't change. They're used here to set pin numbers:
const int buttonPin = 2;     // the number of the pushbutton pin
const int buzzer =  3;      // the number of the buzzer pin

// variables will change:
int buttonState = 0;         // variable for reading the pushbutton status

void setup() {
  // initialize the LED pin as an output:
  pinMode(buzzer, OUTPUT);
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);
}

void loop() {
  // read the state of the pushbutton value:
  buttonState = digitalRead(buttonPin);

  // check if the pushbutton is pressed. If it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    digitalWrite(buzzer, LOW);
  } else {
    // turn LED off:
    digitalWrite(buzzer, HIGH);
  }
}
```

- **Langkah 3.** Upload (unggah) kode demo. Jika Anda tidak tahu cara mengupload (unggah) kode, harap periksa [How to upload code](http://wiki.seeedstudio.com/Upload_Code/).

!!!berhasil
    Jika semuanya berjalan dengan baik, setiap kali Anda bergerak atau mengguncang atau memiringkan Grove - Vibration Sensor maka Grove - buzzer akan berdering.

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan Grove - Vibration Sensor pada port D2, dan hubungkan Grove - Buzzer pada port D3 dari Base Shield.

**Langkah 2.** Hubungkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/master/img/cc_Vibration_Sensor.png)

Upload (unggah) program ke modul Arduino/Seeeduino.

!!!Sukses
    Ketika kode selesai di-upload (unggah), bel akan berbunyi bip saat sensor getaran mendeteksi getaran.

## Sumber-sumber

- **[Zip]** [Grove - Vibration Sensor (SW-420) eagle files](https://github.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/raw/master/res/Grove%20-%20Vibration%20Sensor%20(SW-420)%20v1.1.zip)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Sensor-SW-420/master/res/Grove_Vibration_Sensor_CDC_File.zip)

## Proyek

Ini adalah video pengantar produk ini, demo sederhana, Anda dapat mencobanya.

<iframe width="560" height="315" src="https://www.youtube.com/embed/oFmvKxoZIuw?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>



## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>