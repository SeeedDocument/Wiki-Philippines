---
name: Grove - Sound Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Sound-Sensor-p-752.html
oldwikiname: Grove_-_Sound_Sensor
prodimagename: page.jpg
surveyurl: https://www.surveymonkey.com/r/SoundSensor
sku: 101020023
tags: io_3v3, io_5v, plat_duino, plat_linkit, plat_bbg, plat_wio, plat_pi, plat_linkit
---

![](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/img/page_small_1.jpg)

Grove - Sound Sensor dapat mendeteksi intensitas suara dari lingkungan sekitar. Komponen utama modul ini adalah mikrofon sederhana, yang didasarkan pada amplifier LM386 dan mikrofon electret. Output modul ini adalah sinyal analog dan dapat dengan mudah disampel dan telah diuji dengan Seeeduino.

<iframe width="800" height="450" src="https://www.youtube.com/embed/EhZ7uDvoALE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<p style=":center"><a href="http://www.seeedstudio.com/Grove-Sound-Sensor-p-752.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>


## Fitur - Fitur

* Mudah digunakan
* Menyediakan sinyal keluaran (output) analog
* Dapat dengan mudah diintegrasi dengan modul logika pada bagian input pada rangkaian Grove

!!!Peringatan
    Sensor suara ini digunakan untuk mendeteksi apakah ada suara di sekitar atau tidak, tolong jangan gunakan modul untuk mengumpulkan sinyal suara. Misalnya, Anda dapat menggunakannya untuk membuat lampu kontrol suara, tetapi tidak bisa digunakan sebagai alat perekam.

## Spesifikasi

|Item|Value|
|-----|------|
|Operating Voltage Range| 3.3/5 V |
|Operating Current(Vcc=5V)|4~5 mA|
|Voltage Gain(V=6V, f=1kHz)|26 dB|
|Microphone sensitivity(1kHz)|52-48 dB|
|Microphone Impedance|2.2k Ohm|
|Microphone Frequency|16-20 kHz|
|Microphone S/N Radio|54 dB|

!!!Tips

Selengkapnya tentang modul Grove bisa dilihat di [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.



## Memulai

!!!Catatan
    Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.

### Bermain dengan Arduino

**Hardware**

- **Langkah 1.** Siapkan komponen dibawah ini:

|Seeeduino V4.2| Base Shield|Grove-Sound Sensor|
|--------------|------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/img/page_small_1.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Sound-Sensor-p-752.html)|

- **Langkah 2.** Hubungkan Grove-Sound Sensor ke port **A0** pada Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB.   

![](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/img/1_connect.jpg)

!!!Catatan
    Jika tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Sound Sensor ke Seeeduino seperti di bawah ini.

| Seeeduino     | Grove-Sound Sensor      |
|---------------|-------------------------|
| 5V            | Red                     |
| GND           | Black                   |
| A1            | White                   |
| A0            | Yellow                  |

**Software**

- **Langkah 1.** Salin kode dibawah ini ke Arduio IDE dan unggah (upload) ke arduino. Jika anda tidak mengetahui cara unggah kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

```c
// kode uji coba untuk Grove - Sound Sensor
// loovee @ 2016-8-30

const int pinAdc = A0;

void setup()
{
    Serial.begin(115200);
    //Serial.println("Grove - Sound Sensor Test...");
}

void loop()
{
    long sum = 0;
    for(int i=0; i<32; i++)
    {
        sum += analogRead(pinAdc);
    }

    sum >>= 5;

    Serial.println(sum);
    delay(10);
}

```

- **Langkah 2.** Klik pada **Serial > Plotter** untuk mendapatkan kurva perubahan sensor. Buatlah bunyi-bunyian untuk melihat perubahan nilai.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Sound_Sensor/master/images/sound_raw.png)

### Bermain dengan Codecraft

#### Hardware

**Langkah 1.** Hubungkan Grove - Sound Sensor ke port A0 pada Base Shield.

**Langkah 2.** Pasang Grove - Base Shield ke Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda melalui kabel USB.

#### Software

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/),  tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Seret (drag) blok-blok yang ada seperti gambar dibawah ini atau buka file cdc yang dapat diunduh pada akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Sound_Sensor/master/img/cc_Sound_Sensor.png)

Unggah (Upload) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode berhasil diunggah (upload), anda dapat melihat nilai suara yang ditampilkan pada Serial Monitor.

### Bermain dengan Raspberry Pi (Dengan Grove Base Hat untuk Raspberry Pi)

#### Hardware

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Sound Sensor|
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/img/page_small_1.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Sound-Sensor-p-752.html)|



- **Langkah 2**. Pasang Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan Grove - Sound Sensor ke port A0 pada Base Hat.
- **Langkah 4**. Hubungkan Raspberry ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/img/Sound_Hat.jpg)


!!! Note
    Untuk Langkah ke 3 anda dapat menghubungkan modul sound sensor ke **Port Analog manapun** tetapi pastikan anda telah mengganti perintah sesuai dengan nomor portnya.


#### Software

- **Langkah 1**. Ikuti lankah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (development environment).
- **Langkah 2**. Unduh (Download) file sumbernya dengan menduplikat library grove.py .

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Eksekusi perintah dibawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_sound_sensor.py 0

```

Berikut adalah kode grove_sound_sensor.py .

```python

import math
import sys
import time
from grove.adc import ADC


class GroveSoundSensor:

    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def sound(self):
        value = self.adc.read(self.channel)
        return value

Grove = GroveSoundSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveSoundSensor(int(sys.argv[1]))

    print('Detecting sound...')
    while True:
        print('Sound value: {0}'.format(sensor.sound))
        time.sleep(.3)

if __name__ == '__main__':
    main()


```

!!!sukses
    
    Jika semuanya berjalan dengan baik, anda dapat melihat hasil seperti berikut.
    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_sound_sensor.py 0 
Detecting sound...
Sound value: 499
Sound value: 525
Sound value: 529
Sound value: 493
Sound value: 457
Sound value: 457
Sound value: 503
Sound value: 537
Sound value: 606
Sound value: 614
Sound value: 661
^CTraceback (most recent call last):
  File "grove_sound_sensor.py", line 67, in <module>
    main()
  File "grove_sound_sensor.py", line 64, in main
    time.sleep(.3)
KeyboardInterrupt

```


Anda dapat keluar dari program ini hanya dengan menekan **ctrl+c** .

!!!Perhatian
        Anda perlu memperhatikan bahwa untuk port analog, nomor pin pada silkscreen adalah sesuatu seperti **A1, A0**, namun dalam perintah kita menggunakan parameter **0** dan **1**, sama seperti port digital. Jadi pastikan Anda menghubungkan modul ke port yang benar,jika tidak, ada kemungkinan terjadinya konflik pin.


### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

**Hardware**

- **Langkah 1.** Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus|Grove-Sound Sensor|Grove-Blue LED|
|--------------|-------------|-----------------|----------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Sound_Sensor/master/images/gs_1.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/img/groveblue%20led.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Sound-Sensor-p-752.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove---Blue-LED-p-1139.html)|

- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.

- **Langkah 3.** Hubungkan Grove-Sound Sensor ke port **A0** pada GrovePi_Plus , dan hubungkan Grove-Blue LED ke port **D5** pada GrovePi_Plus

- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/img/2_connect.jpg)

**Software**

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).

- **Langkah 2.** Ikuti langkah [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/) untuk memperbarui firmware versi terbaru pada GrovePi.


!!!Tips
    Dalam situs wiki ini kita menggunakan alamat (path) **~/GrovePi/** dibandingkan **/home/pi/Desktop/GrovePi**, anda harus memastikan Langkah 2 dan Langkah 3 menggunakan alamat yang sama.


!!!Catatan
    Kami  menyarankan Anda untuk memperbarui firmware, jika tidak untuk beberapa jenis sensor mungkin dapat terjadi masalah.

- **Langkah 3.** Lakukan Git clone pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Langkah 4.** Arahkan alamat (path) ke direktori demo:

```
cd yourpath/GrovePi/Software/Python/
```

berikut adalah kode grove_sound_sensor.py .

```python

#!/usr/bin/env python
#
# Contoh GrovePi untuk menggunakan modul Grove Sound Sensor dan Grove LED
#
# GrovePi terhubung ke Raspberry Pi dan sensor-sensor Grove.  Anda dapat belajar lebih lanjut melalui link berikut  http://www.dexterindustries.com/GrovePi
#
# Modul-modul:
#	 http://www.seeedstudio.com/wiki/Grove_-_Sound_Sensor
#	 http://www.seeedstudio.com/wiki/Grove_-_LED_Socket_Kit
#
# Punya pertanyaan tentang contoh ini? tanyakan pada forum berikut: http://forum.dexterindustries.com/c/grovepi
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

# Hubungkan Grove Sound Sensor ke port analog A0
# SIG,NC,VCC,GND
sound_sensor = 0

# Hubungkan Grove LED ke port digital D5
# SIG,NC,VCC,GND
led = 5

grovepi.pinMode(sound_sensor,"INPUT")
grovepi.pinMode(led,"OUTPUT")

# Batas untuk menyalakan led adalah 400.00 * 5 / 1024 = 1.95v
threshold_value = 400

while True:
    try:
        # Membaca tingkat kebisingan suara
        sensor_value = grovepi.analogRead(sound_sensor)

        # Jika suara bising terjadi, LED menyala terang, jika tidak LED menyala redup
        if sensor_value > threshold_value:
            grovepi.digitalWrite(led,1)
        else:
            grovepi.digitalWrite(led,0)

        print("sensor_value = %d" %sensor_value)
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- **Langkah 5.** Jalankan demo.


```
sudo python grove_sound_sensor.py
```

## Sumber-Sumber

- [**Eagle**][Schematic and PCB in Eagle format](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/resources/Grove%20-%20Sound%20Sensor.zip)
- [**PDF**][Schematic in PDF format](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/res/Grove%20-%20Sound%20Sensor%20v1.6%20Schematic.pdf)
- [**PDF**][PCB in PDF format](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/res/Grove%20-%20Sound%20Sensor%20v1.6%20PCB.pdf)
- [**Datasheet**][LM386.PDF](https://github.com/SeeedDocument/Grove_Sound_Sensor/raw/master/res/LM386.pdf)
- [**Codecraft**][CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Sound_Sensor/master/res/Grove_Sound_Sensor_CDC_File.zip)

## Proyek

**Create a multi-tasking IoT Wi-Fi sensor**: Panduan ini menunjukkan cara membuat sensor yang terhubung ke internet, sambil memanfaatkan fitur multi-task unik dari Energia & TI LaunchPad.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/adrianf/create-a-multi-tasking-iot-wi-fi-sensor-9d7fdf/embed' width='350'></iframe>


**LED Sound Meter using Wio-Link and Node-Red**: SeeedStudio Grove sound sensor dan LED strip yang terhubung ke Wio-Link dikendalikan oleh Node-Red.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/potnik/led-sound-meter-using-wio-link-and-node-red-259e02/embed' width='350'></iframe>

**Sound sensor Grove module**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/N19VfMYyn60" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/NfFlz8KEFxw" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>