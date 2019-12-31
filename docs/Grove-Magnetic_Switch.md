---
name: Grove - Magnetic Switch
category: Sensor
bzurl: https://seeedstudio.com/Grove-Magnetic-Switch-p-744.html
oldwikiname: Grove_-_Magnetic_Switch
prodimagename: Magnetic_Switch.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020038 1.jpg
surveyurl: https://www.research.net/r/Grove-Magnetic_Switch
sku: 101020038
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_pi, plat_bbg, plat_wio
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/45d.jpg)

Modul diatas adalah Grove Interface yang kompatibel dengan Magnetic Switch Module. Modul tersebut mengacu pada reed encapsulated dry reed switch CT10. CT10 adalah tipe saklar single-pole, single throw (SPST), memiliki kontak rutenium normally open (keadaan normal sakelar terbuka). Sensor tersebut memiliki tipe ujung ganda (double-ended) dan dapat digerakkan dengan elektromagnet, magnet permanen atau kombinasi keduanya. magnetic switch (Saklar magnetik) adalah alat yang luar biasa bagi para perancang yang ingin menghidupkan dan mematikan sirkuit berdasarkan kedekatan.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Magnetic-Switch-p-744.html)

## Fitur - Fitur

-   Grove compatible interface
-   Modul Grove 2.0cm x 2.0cm
-   Perangkat eksternal minimum
-   Daya 10W
-   Enkapsulasi yang kuat

!!!Tips
    Selengkapnya tentang modul Grove dapat mengacu ke [Sistem Grove](http://wiki.seeedstudio.com/Grove_System/)

## Ide Aplikasi

-   Sensor Jarak / Proximity
-   Sensor Peringatan Keamanan
-   Sensor level
-   Sensor Aliran
-   Penghitung Pulsa

## Spesifikasi

<table border="1">
<tr>
<th scope="col">
Fitur
</th>
<th scope="col">
Min
</th>
<th scope="col">
Norm
</th>
<th scope="col">
Maks
</th>
<th scope="col">
Satuan
</th>
</tr>
<tr align="center">
<td>
Working Voltage
</td>
<td>
4.75
</td>
<td>
5.0
</td>
<td>
5.25
</td>
<td>
V
</td>
</tr>
<tr align="center">
<td>
Switched Power
</td>
<td colspan="3">
10
</td>
<td>
W
</td>
</tr>
<tr align="center">
<td>
Switched Voltage AC,RMS Value(max)
</td>
<td colspan="3">
&lt; 140
</td>
<td>
V
</td>
</tr>
<tr align="center">
<td>
Switched Current DC
</td>
<td colspan="3">
&lt; 500
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<td>
Carry Current DC
</td>
<td colspan="3">
&lt; 0.5
</td>
<td>
A
</td>
</tr>
<tr align="center">
<td>
Contact Resistance
</td>
<td colspan="3">
&lt;200
</td>
<td>
mΩ
</td>
</tr>
<tr align="center">
<td>
Insulation Resistance
</td>
<td colspan="3">
&gt;10<sup>6</sup>
</td>
<td>
MΩ
</td>
</tr>
<tr align="center">
<td>
Operating Temperature
</td>
<td>
-40
</td>
<td>
-
</td>
<td>
125
</td>
<td>
℃
</td>
</tr>
<tr align="center">
<td>
Operate Range
</td>
<td>
10
</td>
<td>
-
</td>
<td>
40
</td>
<td>
AT
</td>
</tr>
</table>

!!!Tips

 Selengkapnya tentang modul Grove dapat mengacu ke [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.



## Memulai

!!!Catatan

Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


### Bermain dengan Arduino

#### Demonstrasi

Pin SIG pada modul dalam keadaan normalnya memiliki output LOW. Ketika magnet mendekati sakelar, magnetic switch (sakelar magnet) terhubung dan pin SIG menghasilkan output HIGH.

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan komponen dibawah ini:

| Seeeduino V4.2 | Base Shield| Grove - Magnetic Switch |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Magnetic-Switch-p-744.html)|

- **Langkah 2.** Hubungkan Grove - Magnetic Switch ke port **D2** dari Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/with_ardu.jpg)

!!!Catatan

    Jika tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Magnetic-Switch ke Seeeduino seperti di bawah ini.

| Seeeduino | Grove-Magnetic_Switch |
|------|----------------------------|
| 5V   | Red                        |
| GND  | Black                      |
| NC   | White                      |
| D2   | Yellow                     |

#### Software (Perangkat Lunak)

- **Langkah 1.** Salin kode ke Arduino IDE lalu upload (unggah). Jika Anda tidak tahu cara mengunggah kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

```c
/*******************************************************************************/

/*Inisialisasi makro dari pin magnetic dan pin LED*/
#define MAGNECTIC_SWITCH 2
#define LED 13//the on board LED of the Arduino or Seeeduino

void setup()
{
    pinsInit();
}

void loop() 
{
    if(isNearMagnet())//if the magnetic switch is near the magnet?
    {
        turnOnLED();
    }
    else
    {
        turnOffLED();
    }
}
void pinsInit()
{
    pinMode(MAGNECTIC_SWITCH, INPUT);
    pinMode(LED,OUTPUT);
}

/*Jika magnetic switch (Sakelar magnetik) berada di dekat magnet, nilai returnnya menjadi true, */
/*jika tidak maka nilai returnnya menjadi false                                */
boolean isNearMagnet()
{
    int sensorValue = digitalRead(MAGNECTIC_SWITCH);
    if(sensorValue == HIGH)//if the sensor value is HIGH?
    {
        return true;//yes,return ture
    }
    else
    {
        return false;//no,return false
    }
}
void turnOnLED()
{
    digitalWrite(LED,HIGH);
}
void turnOffLED()
{
    digitalWrite(LED,LOW);
}
```

- **Langkah 2.**  Kemudian LED menyala ketika ada gaya Magnetik yang mendekati sakelar. Selamat mencoba!

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan Grove - Magnetic Switch ke port D2 dari Base Shield.

**Langkah 2.** Pasang Base Shield ke Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda melalui kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), Tambahkan dukungan Arduino, dan tarik Prosedur Utama ke area kerja.

!!!Catatan
    Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Panduan untuk Codecraft menggunakan Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Seret blok seperti gambar dibawah atau buka file cdc yang dapat didownload (diunduh) pada akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/cc_Magnetic_Switch.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses

    Ketika kode selesai diunggah, gerakkan magnet mendekati magnetic switch (Sakelar Magnetik) dan Anda akan melihat LED pada pin 13 pada Arduino menyala.

### Bermain dengan Raspberry Pi

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Magnetic Switch |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Magnetic-Switch-p-744.html)|

- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.
- **Lagkah 3.** Hubungkan Grove-Magnetic-Switch ranger ke port **D2** dari GrovePi_Plus.
- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/with_rpi.jpg)

#### Software (Perangkat Lunak)

- **Langkah 1.** Ikuti [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).

- **Langkah 2.** Arahkan ke direktori demo:

```
cd yourpath/GrovePi/Software/Python/
```

- **Langkah 3.** Melihat kode (demo ini memiliki penggunaan yang sama dengan tilt switch)

```
nano grovepi_tilt_switch.py   # "Ctrl+x" to exit #
```

```py
import time
import grovepi

# Hubungkan Grove Tilt Switch ke port digital D2
# SIG,NC,VCC,GND
tilt_switch = 2

grovepi.pinMode(tilt_switch,"INPUT")

while True:
    try:
        print grovepi.digitalRead(tilt_switch)
        time.sleep(.5)

    except IOError:
        print "Error"
```

- **Step 4.** Jalankan demonya.

```
sudo python grovepi_tilt_switch.py
```

- **Step 5.** Hasil

Letakkan magnet diatas sensor, pin SIG akan menghasilkan output HIGH.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/img/Grovepi_tilt_Switch_00.png)

## Sumber-Sumber
- **[Eagle]**  [Grove-Magnetic Switch v0.9 Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Magnetic_Switch.zip)

- **[Eagle]**  [Grove-Magnetic Switch v1.3 Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove-Magnetic_Switch_v1.3_Eagle_File.zip)

- **[PDF]**  [Grove-Magnetic Switch v1.3 PDF File](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove-Magnetic_Switch_v1.3_PDF_File.pdf)

- **[Datasheet]**  [CT10 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/CT10.pdf)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Magnetic_Switch/master/res/Grove_Magnetic_Switch_CDC_File.zip)

<!-- file ini dibuat dari http://www.seeedstudio.com/wiki/Grove_-_Magnetic_Switch -->

## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>