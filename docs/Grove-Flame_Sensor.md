---
name: Grove - Flame Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Flame-Sensor-p-1450.html
oldwikiname: Grove_-_Flame_Sensor
prodimagename: Flame_Sensor_01.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/Flame Sensor.jpg
surveyurl: https://www.research.net/r/Grove-Flame_Sensor
sku: 101020049
tags: grove_digital, io_5v, plat_duino, plat_linkit
---


![](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/Flame_Sensor_01.jpg)

Grove-Flame Sensor dapat digunakan untuk mendeteksi sumber api atau sumber cahaya dari panjang gelombang yang berkisar antara 760nm - 1100 nm. Modul ini didasarkan pada sensor YG1006 yang merupakan phototransistor silikon NPN kecepatan tinggi dan sensitif. Karena epoksi hitamnya, sensor ini peka terhadap radiasi inframerah. Dalam permainan robot pemadam kebakaran, sensor ini memainkan peran yang sangat penting, dapat digunakan sebagai mata robot untuk menemukan sumber api.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Flame-Sensor-p-1450.html)

## Fitur

- Grove Interface
- Sensitivitas Foto Tinggi
- Waktu Respon yang Cepat
- Mudah digunakan
- Sensitivitas dapat disesuaikan

!!!Tip
    Lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi


<table border="1" cellspacing="0" width="80%">
<tr>
<th scope="col">
Parameter
</th>
<th scope="col">
Min
</th>
<th scope="col">
Typical
</th>
<th scope="col">
Max
</th>
<th scope="col">
Satuan
</th>
</tr>
<tr align="center">
<th scope="row">
Tegangan
</th>
<td>
4.75
</td>
<td>
5.0
</td>
<td>
5.30
</td>
<td>
VDC
</td>
</tr>
<tr align="center">
<th scope="row">
Arus
</th>
<td>
/
</td>
<td>
20
</td>
<td>
/
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<th scope="row">
Rentang Bandwidth Spectral
</th>
<td>
760
</td>
<td>
940
</td>
<td>
1100
</td>
<td>
nm
</td>
</tr>
<tr align="center">
<th scope="row">
Jangkauan deteksi
</th>
<td>
0
</td>
<td>
~
</td>
<td>
1
</td>
<td>
m
</td>
</tr>
<tr align="center">
<th scope="row">
Respon waktu
</th>
<td colspan="3">
15
</td>
<td>
μS
</td>
</tr>
<tr align="center">
<th scope="row">
Suhu operasi
</th>
<td>
-25
</td>
<td>
~
</td>
<td>
85
</td>
<td>
℃
</td>
</tr>
</table>

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai

Modul ini utamanya digunakan untuk mendeteksi cahaya inframerah yang mengeluarkan sinyal digital 0 dan 1 melalui output Komparator. Nilai output akan menjadi 0 ketika cahaya inframerah terdeteksi. Dan sensitivitasnya disesuaikan dengan kepresisian potensiometer.

### Bermain dengan Arduino

#### Hardware (Perangkat Keras)
- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield| Grove-Flame_Sensor |Grove - Red LED|
|--------------|-------------|-----------------|-----|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Flame_Sensor/raw/master/img/45d_small.jpg)|![enter image description](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Flame-Sensor-p-1450.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)|

- **Langkah 2.** Hubungkan modul Grove-Flame_Sensor ke port **D2** dari Grove-Base Shield.
- **Langkah 3.** Hubungkan modul Grove - Red LED ke port **D3** dari Grove-Base Shield.
- **Langkah 4.** Pasangkan modul Grove - Base Shield ke Seeeduino.
- **Langkah 5.** Hubungkan modul Seeeduino ke PC menggunakan kabel USB.

<!--link-->
![with_ardu](https://github.com/SeeedDocument/Grove-Flame_Sensor/raw/master/img/with_ardu.jpg)

!!!Catatan
	Jika kami tidak memiliki Grove Base Shield, kami juga dapat langsung menghubungkan Grove_Flame_Sensor ke Seeeduino seperti di bawah ini.

| Seeeduino       |  Grove-Flame_Sensor  |
|---------------|-------------------------|
| 5V            | Merah                   |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D2            | Kuning                  |



| Seeeduino       |  Grove - Red LED |
|---------------|-------------------------|
| 5V            | Merah                   |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D3            | Kuning                  |





#### Software (Perangkat Lunak)


**Langkah 1.** Salin kode dan flash ke Modul kontroler.


Berikut ini kodenya
```c
    /******************************************************************************/

#define FLAME_SENSOR 2 //connect SENSOR to digital pin2
#define LED 3 //connect Grove - LED to pin3

void setup()
{
    pinsInit();
}
void loop()
{
    if(isFlameDetected())
    turnOnLED();
    else turnOffLED();
}
    /********************************/
void pinsInit()
{
    pinMode(FLAME_SENSOR, INPUT);
    pinMode(LED,OUTPUT);
    digitalWrite(LED,LOW);
}
void turnOnLED()
{
    digitalWrite(LED,HIGH);
}
void turnOffLED()
{
    digitalWrite(LED,LOW);
}
boolean isFlameDetected()
{
    if(digitalRead(FLAME_SENSOR))
    return false;
    else return true;
}
```

**Langkah 2.** LED akan menyala ketika ada cahaya inframerah. 

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan module Grove - Flame Sensor ke port D2, dan hubungkan modul Grove - Red LED ke port D3 dari Base Shield.

**Langkah 2.** Pasangkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC dengan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/cc_Flame_Sensor.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode selesai di-upload (unggah), LED akan menyala ketika Sensor Api mendeteksi nyala api.

### Bermain dengan Raspberry Pi

#### Hardware (Perangkat Keras)

- **Langkah 1.** Peralatan yang dibutuhkan pada proyek ini:


| Raspberry pi | GrovePi_Plus | Grove-Flame_Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Flame_Sensor/raw/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Flame-Sensor-p-1450.html)|



- **Langkah 2.** Pasangkan modul GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove-Flame_Sensor ke port **D2** dari GrovePi_Plus.
- **Langkah 4.** Hubungkan modul Raspberry ke PC melalui kabel USB.


![with_rpi](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/with_rpi.jpg)

#### Software (Perangkat Lunak)

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) to configure the development environment.
- **Langkah 2.** Download (unduh) kode pada repositori Github.


```bash
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-	**Langkah 3.** Jalankan perintah di bawah ini untuk menjalankan kode


```bash
cd ~/GrovePi/Software/Python
python grove_flame_sensor.py
```


Berikut ini contoh kode:

```Python
#!/usr/bin/env python
#
# GrovePi Example for using the Grove Flame Sensor (http://www.seeedstudio.com/wiki/Grove_-_Flame_Sensor)
#
# The GrovePi connects the Raspberry Pi and Grove sensors.  You can learn more about GrovePi here:  http://www.dexterindustries.com/GrovePi
#
# Have a question about this example?  Ask on the forums here:  http://forum.dexterindustries.com/c/grovepi
#
'''
## License
The MIT License (MIT)
GrovePi for the Raspberry Pi: an open source platform for connecting Grove Sensors to the Raspberry Pi.
Copyright (C) 2017  Dexter Industries
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
'''
import time
import grovepi

# Connect the Grove Flame Sensor to digital port D2
# SIG,NC,VCC,GND
flame_sensor = 2

grovepi.pinMode(flame_sensor,"INPUT")

while True:
    try:
        print(grovepi.digitalRead(flame_sensor))
        time.sleep(.5)

    except IOError:
        print ("Error")
```


## Rujukan

Sensor dapat mendeteksi sumber cahaya dengan panjang gelombang yang berkisar antara 760nm - 1100 nm. Gambar dibawah ini menunjukkan sensitifitas spektralnya.
![](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/img/Spectral_Sensitive.jpg)

## Sumber - sumber

-  **[Eagle]** [Grove - Flame Sensor Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/res/Grove-Directional_Light_Sensor_Eagle_File.zip)
-  **[Library]** [Github repository for Grove_Flame_Sensor Library](https://github.com/Seeed-Studio/Grove_Flame_Sensor)
-  **[Datasheet]** [LM293D datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/res/LM293D.pdf)
-  **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Flame_Sensor/master/res/Grove_Flame_Sensor_CDC_File.zip)



## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>