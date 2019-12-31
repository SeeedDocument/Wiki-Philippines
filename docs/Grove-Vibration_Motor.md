---
name: Grove - Vibration Motor
category: Actuator
bzurl: https://seeedstudio.com/Grove-Vibration-Motor-p-839.html
oldwikiname: Grove_-_Vibration_Motor
prodimagename: Gvib.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/gvib.jpg
surveyurl: https://www.research.net/r/Grove-Vibration_Motor
sku: 105020003
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/img/Gvib.jpg)

Ini adalah modul motor getar yang cocok digunakan sebagai indikator yang tidak dapat didengar. Pada saat input berlogika HIGH, motor akan bergetar mirip seperti ponsel pada saat mode diam atau silent.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Vibration-Motor-p-839.html)

## Versi

| Perubahan | Deskripsi                                                    | Tanggal Dirilis       |
|----------|----------------------------------------------------------------|---------------|
| v0.9b    | Initial public release                                         | May 10, 2011  |
| v1.0     | Directly uses an I/O port to drive Vibration Motor             | Nov 5, 2011   |
| v1.2     | Transistor added, uses bigger current to drive Vibration Motor | July 11, 2013 |

## Fitur

-   Kompatibel dengan modul Grove
-   Tidak menimbulkan suara
-   Konsumsi daya rendah
-   Keandalan yang tinggi

!!!Tip
    Rincian lebih detail tentang modul Grove silakan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi

<table border="1" cellspacing="0" width="80%">
<tr>
<th scope="col">
Deskripsi
</th>
<th scope="col">
Min
</th>
<th scope="col">
Typ
</th>
<th scope="col">
Max
</th>
</tr>
<tr align="center">
<th scope="row">
Tegangan Kerja
</th>
<td>
3.0V
</td>
<td>
5.0V
</td>
<td>
5.5V
</td>
</tr>
<tr align="center">
<th scope="row">
Control Mode
</th>
<td colspan="3" rowspan="1">
Logic Level
(Ketika berlogika HIGH, motor ON. Ketika berlogika LOW, motor OFF)
</td>
</tr>
<tr align="center">
<th scope="row">
Kecepatan
</th>
<td colspan="3" rowspan="1">
9000 rpm
</td>
</tr>
</table>

## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai

!!!Catatan
   Jika ini adalah pertama kalinya Anda bekerja dengan Arduino, kami dengan menyarankan Anda untuk melihat [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.

### Bermain dengan Arduino

Untuk membuat motor bergetar semudah menyalakan LED. Berikut adalah contoh yang menunjukkan cara menghidupkan motor getar.

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Vibration Motor |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/img/Gvib_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Vibration-Motor-p-839.html)|

- **Langkah 2.** Hubungkan Grove - Vibration Motor ke Grove-Base Shield pin D2.
- **Langkah 3.** Pasangkan Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove-Vibration_Motor/raw/master/img/vibration_motor.png)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove - Vibration Motor ke Seeeduino seperti dibawah ini.

| Seeeduino       | Grove - Vibration Motor |
|---------------|-------------------------|
| 5V            | Merah                     |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D2            | Kuning                  |

#### Software (Perangkat Lunak)

- **Langkah 1.** Salin kode ke Arduino IDE dan upload (unggah). Jika Anda tidak tahu cara mengupload (unggah) kode, coba lihat [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

```c
int MoPin = 2;    // vibrator Grove connected to digital pin 9

void setup()  {
    pinMode( MoPin, OUTPUT );
}

void loop()  {

    digitalWrite(MoPin, HIGH);
    delay(1000);

    digitalWrite(MoPin, LOW);
    delay(1000);
}

```

- **Langkah 2.** Sekarang, coba rasakan getaran yang dihasilkan oleh motor getar!

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan Grove - Vibration Motor ke port D2 dari modul Base Shield.

**Langkah 2.** Pasangkan modul Grove - Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://github.com/SeeedDocument/Grove-Vibration_Motor/raw/master/img/cc_Vibration_Motor.png)

Upload (unggah) program ke modul Arduino/Seeeduino.

!!!Sukses
    Ketika kode selesai di-upload (unggah), Anda akan merasakan getaran dari motor getar.

### Bermain dengan Raspberry Pi

#### Hardware (Perangkat Keras)

- **Langkah 1.** Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | GrovePi_Plus | Grove - Vibration Motor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/img/Gvib_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Vibration-Motor-p-839.html)|

- **Langkah 2.** Hubungkan GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove - Vibration Motor ranger ke GrovePi_Plus port ke **D8**.
- **Langkah 4.** Hubungkan modul Raspberry Pi ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

- **Langkah 1.** Arahkan ke direktori demo:

```
cd yourpath/GrovePi/Software/Python/
```

- **Langkah 2.** Jalankan perintah di bawah ini untuk menjalankan kode

```
nano grove_vibration_motor.py   # "Ctrl+x" to exit #
```

```python
import time
import grovepi

# Connect the Grove Vibration Motor to digital port D8
# SIG,NC,VCC,GND
vibration_motor = 8

grovepi.pinMode(vibration_motor,"OUTPUT")

while True:
    try:
        # Start vibrating for 1 second
        grovepi.digitalWrite(vibration_motor,1)
        print 'start'
        time.sleep(1)

        # Stop vibrating for 1 second, then repeat
        grovepi.digitalWrite(vibration_motor,0)
        print 'stop'
        time.sleep(1)

    except KeyboardInterrupt:
        grovepi.digitalWrite(vibration_motor,0)
        break
    except IOError:
        print "Error"
```

- **Langkah 3.** Jalankan demonya.

```
sudo python grove_vibration_motor.py
```


## Sumber-sumber

- **[Eagle]** [Grove - Vibration Motor Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/res/Grove-Vibration_Motor_Eagle_Files.zip)

- **[Datasheet]** [S9013 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/res/S9013.pdf)

- **[Datasheet]** [ANDA-B1020 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Vibration_Motor/master/res/ANDA-B1020_datasheet.pdf)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Vibration_Motor/master/resource/Grove_Vibration_Motor_CDC_File.zip)



<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Vibration_Motor -->

## Proyek 

**Grove - Aplikasi Vibration Motor - hanya untuk orang dewasa**: Beginner-Example

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-in-a-vibration-motor-only-for-adults-2acfc2/embed' width='350'></iframe>


**Terinspirasi dari OVERWATCH, kami telah membuat mainan Wooden Laser Gun yang keren untuk bersenang-senang hari ini!**

Wooden Laser Gun dan Gun Target semuanya didasarkan pada board Arduino yang disebut Seeeduino Lotus. Pemancar laser pada Laser Gun dikendalikan untuk memancarkan pulsa laser untuk "mengaktifkan" Gun Target. Terdapat 3 sensor cahaya pada Gun Target untuk mendeteksi pulsa laser. Sepertinya sangat sederhana bukan? Jika Anda tertarik dengan proyek kami, silakan buat satu untuk diri sendiri atau untuk anak Anda! Proyek ini cocok digunakan untuk menghabiskan DIY dalam satu hari sebagai hadiah Natal.    

[![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Lotus/master/img/gun.jpg)](http://www.instructables.com/id/DIY-a-Wooden-Laser-Gun-As-a-Xmas-Present-for-Your-/)

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>