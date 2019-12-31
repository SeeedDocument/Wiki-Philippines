---
name: Grove - Water Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html
oldwikiname: Grove_-_Water_Sensor
prodimagename: Grove-Water_Sensor.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020018 1.jpg
surveyurl: https://www.research.net/r/Grove-Water_Sensor
sku: 101020018
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_1.png)

Modul Water Sensor adalah bagian dari sistem Grove. Modul ini menunjukkan apakah sensor kering, lembab atau tenggelam sepenuhnya dalam air dengan mengukur konduktivitas. Sensor memiliki resistor pull-up 1 MΩ. Resistor akan mengambil nilai sensor tertinggi sampai tetesan air paling rendah dari sensor ke ground sebagai jangkauan. Rangkaian ini akan bekerja dengan pin I/O digital Arduino atau dapat menggunakannya dengan pin analog untuk mendeteksi jumlah kontak yang disebabkan air antara ground dan sensor.


<p style=":center"><a href="https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Versi

| Versi Produk              | Perubahan                                                                                                                                                                                    | Tanggal dirilis |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Grove-Water Sensor V1.1 | Initial                                                                                                                                                                                    | July 2014      |


## Fitur


- Antarmuka kompatibel Grove
- Konsumsi daya rendah
- Modul Grove 2.0cm x 2.0cm
- Sensitivitas tinggi

## Ide Aplikasi

- Mendeteksi curah hujan
- Kebocoran cairan
- Detektor overflow tangki

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
Unit
</th>
</tr>
<tr align="center">
<th scope="row">
Tegangan kerja
</th>
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
<th scope="row">
Current
</th>
<td colspan="3">
&lt;20
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<th scope="row">
Suhu kerja
</th>
<td>
10
</td>
<td>
-
</td>
<td>
30
</td>
<td>
℃
</td>
</tr>
<tr align="center">
<th scope="row">
Kelembaban kerja (tanpa kondensasi)
</th>
<td>
10
</td>
<td>
-
</td>
<td>
90
</td>
<td>
 %
</td>
</tr>
</table>

!!!Tip
    Lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai

!!!Catatan
    Jika ini adalah pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk melihat Getting Started with Arduino sebelum memulai.

### Bermain dengan Arduino

#### Hardware (Perangkat Keras)

Hubungkan modul ke modul dasar menggunakan salah satu pin digital. Anda bisa mendapatkan nilai pin sinyal. Ketika ada air di kabel penghantar telanjang, nilainya LOW (0). Kalau tidak, itu akan HIGH (1).

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Water Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_small.png)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html)|

- **Langkah 2.** Hubungkan modul Water Sensor ke port D2 dari Grove-Base Shield.
- **Langkah 3.** Pasangkan modul Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan modul Seeeduino ke PC menggunakan kabel USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/3.jpg)
!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove_Water_Sensor ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove - Water Sensor |
|---------------|-------------------------|
| 5V            | Merah                   |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D2            | Kuning                  |

#### Software (Perangkat Lunak)
- **Langkah 1.** Salin kode ke Arduino IDE dan upload (unggah). Jika Anda tidak tahu cara mengupload (unggah) kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

```c
#define WATER_SENSOR 2

void setup()
{
  Serial.begin (9600);
  pinMode(WATER_SENSOR, INPUT);
}
void loop()
{
  Serial.println(digitalRead(WATER_SENSOR));
  delay(500);
}

```
- **Langkah 2.** Kita akan melihat tampilan output pada terminal seperti di bawah ini.

```c
1
1
0
0
1
1
```

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan modul Grove - Water Sensor ke port D2 dari Base Shield.

**Langkah 2.** Hubungkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/cc_Water_Sensor.png)

Upload (unggah) program ke modul Arduino/Seeeduino.

!!!Sukses
    Ketika kode selesai diupload (unggah), Anda akan melihat layar yang terang ditampilkan di Serial Monitor.

### Bermain dengan Raspberry Pi (menggunakan Grove Base Hat untuk Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Water Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_small.png)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html)

- **Langkah 2**. Pasangkan modul Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan modul Grove - Water Sensor ke port A0 dari Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry Pi ke PC menggunakan kabel USB.
![](https://github.com/SeeedDocument/Grove-Water_Sensor/raw/master/img/with_rpi_basehat.jpg)


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengonfigurasi pengembangan proyek.
- **Langkah 2**. Download (unduh) file sumber dengan memperbanyak grove.py library. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3.** Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_water_sensor.py 0
```


Berikut kode grove_water_sensor.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveWaterSensor:

    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def value(self):
        return self.adc.read(self.channel)

Grove = GroveWaterSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveWaterSensor(int(sys.argv[1]))

    print('Detecting ...') 
    while True:
        value = sensor.value        
        if sensor.value > 800:
            print("{}, Detected Water.".format(value))
        else:
            print("{}, Dry.".format(value))

        time.sleep(.1)

if __name__ == '__main__':
    main()


```


!!!sukses
    Jika semuanya berjalan dengan baik, Anda akan dapat melihat hasil berikut
```python

pi@raspberrypi:~/grove.py/grove $ python grove_water_sensor.py 0
Detecting ...
612, Dry.
749, Detected Water.
829, Dry.
357, Dry.
98, Dry.
352, Dry.
517, Dry.
718, Detected Water.
868, Detected Water.
581, Dry.
90, Dry.
326, Dry.
451, Dry.
666, Dry.
867, Detected Water.
684, Dry.
100, Dry.
^CTraceback (most recent call last):
  File "grove_water_sensor.py", line 71, in <module>
    main()
  File "grove_water_sensor.py", line 62, in main
    value = sensor.value        
  File "grove_water_sensor.py", line 48, in value
    return self.adc.read(self.channel)
  File "/usr/local/lib/python2.7/dist-packages/grove/adc.py", line 66, in read
    return self.read_register(addr)
  File "/usr/local/lib/python2.7/dist-packages/grove/adc.py", line 84, in read_register
    return self.bus.read_word_data(self.address, n)
  File "/home/pi/.local/lib/python2.7/site-packages/smbus2/smbus2.py", line 396, in read_word_data
    ioctl(self.fd, I2C_SMBUS, msg)
KeyboardInterrupt


```

Anda dapat menggunakan sensor ini untuk mendeteksi air. Tekan ++ctrl+c++ untuk keluar.


!!!Perhatian
        Anda mungkin telah memperhatikan bahwa untuk port analog, nomor pin silkscreen adalah **A1, A0**, namun dalam perintah kami menggunakan parameter **0** dan **1**, sama seperti port digital. Jadi pastikan Anda pasang modul ke port yang benar, jika tidak mungkin ada konflik pin.


### Bermain dengan Raspberry Pi(menggunakan GrovePi_Plus)

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Water Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/Grove-Water_Sensor_small.png)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Water-Sensor-p-748.html)|


- **Langkah 2.** Pasangkan modul GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan modul Grove-Water Sensor ke port **D2** dari GrovePi_Plus.
- **Langkah 4.** Hubungkan modul Raspberry ke PC menggunakan kabel USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/img/7.jpg)
#### Software (Perangkat Lunak)

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk konfigurasi pengembangan proyek.
- **Langkah 2.** Arahkan ke direktori demo:

```
cd yourpath/GrovePi/Software/Python/
```

-	**Langkah 3.** Untuk melihat kode

```
nano grove_water_sensor.py
```

```python
import time
import grovepi

# Connect the Grove Water Sensor to digital port D2
# SIG,NC,VCC,GND
water_sensor = 2

grovepi.pinMode(water_sensor,"INPUT")

while True:
    try:
        print grovepi.digitalRead(water_sensor)
        time.sleep(.5)

    except IOError:
        print "Error"
```

-	**Langkah 4.** Jalankan demo.

```
sudo python grove_water_sensor.py
```

- **Langkah 5.** Kita akan melihat tampilan output pada terminal seperti di bawah ini.

```
1
1
0
0
1
```

## Sumber - Sumber

- **[Eagle]** [Grove Water Sensor Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/res/Water_sensor.zip)
- **[Library]** [Demo code for Grove Water Sensor](https://github.com/Seeed-Studio/Grove_Water_Sensor)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Water_Sensor/master/res/Grove_Water_Sensor_CDC_File.zip)

<!-- This Markdown file was created from http://wiki.seeedstudio.com/Grove-Water_Sensor/ -->

## Proyek 

**Smart Crops: Menerapkan IoT di Pertanian Konvensional!**: Misi kami dengan alam adalah untuk melestarikannya, merancang, dan menerapkan teknologi pemantauan dengan bantuan IoT melalui Helium.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/gabogiraldo/smart-crops-implementing-iot-in-conventional-agriculture-3674a6/embed' width='350'></iframe>

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>