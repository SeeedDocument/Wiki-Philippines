---
name: Grove - Loudness Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Loudness-Sensor-p-1382.html
oldwikiname: Grove_-_Loudness_Sensor
prodimagename: LoudnessSensor.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/Loudness Sensor.jpg
surveyurl: https://www.research.net/r/Grove-Loudness_Sensor
sku: 101020063
tags: grove_analog, io_3v3, io_5v, plat_duino, plat_linkit, plat_bbg, plat_pi
---

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/Loudness%20Sensor_new.jpg)

The Grove - Loudness Sensor dirancang untuk mendeteksi suara lingkungan sekitar. Berdasarkan penguat LM2904 dan mikrofon internal, itu memperkuat dan menyaring sinyal frekuensi tinggi yang diterima dari mikrofon, dan menghasilkan sinyal envelop positif. Ini digunakan untuk mengakuisisi sinyal Arduino. Nilai output tergantung pada tingkat input suara. Untuk menghindari gangguan sinyal yang tidak perlu atau noise, sinyal input akan melalui penyaringan dua kali di dalam modul. Terdapat potensiometer yang memungkinkan penyesuaian secara manual untuk penguatan output.

<iframe width="800" height="450" src="https://www.youtube.com/embed/EhZ7uDvoALE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<p style=":center"><a href="http://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Versi

| Versi Produk              | Perubahan                                   | Tanggal Dirilis |
|------------------------------|-------------------------------------------|---------------|
|Grove-Loudness Sensor V0.9b   | Initial                                   | Dec 2012      |     


## Fitur - Fitur

-   Grove Interface
-   Mudah digunakan
-   Basic Grove element

!!!Tips
    Detail tentang modul Grove silakan lihat [Grove System](http://wiki.seeedstudio.com/Grove_System/) 

## Spesifikasi

| Parameter             | Nilai / Rentang            |
|-----------------------|------------------------|
| Tegangan              | 3.5~10 VDC             |
| Frekuensi kerja     | 50~2000 Hz             |
| Sensitivitas           | -48~66 dB              |
| Signal-to-noise Ratio | >58 dB                 |
| Rentang sinyal output   | Sinyal Analog  (0-1023) |


## Platform yang Didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai

!!!Note
    Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


### Bermain dengan Arduino

**Perangkat keras**

- **Langkah 1.** Siapkan perangkat di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove-Loudness Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/LoudnessSensor_s.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html)|

- **Langkah 2.** Hubungkan Grove-Loudness Sensor ke **A0** port Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/seeeduino_loudness.jpg)

!!!Catatan
Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Loudness Sensor ke Seeeduino seperti di bawah ini.

| Seeeduino |  Grove-Loudness Sensor |
|-----------|-----------------|
| 5V        | Merah             |
| GND       | Hitam           |
| NC        | Putih           |
| A0        | Kuning          | 

**Perangkat lunak**

- **Langkah 1.** Silakan salin kode di bawah ini ke Arduino IDE dan unggah ke arduino. Jika Anda tidak tahu cara mengunggah kode, silahkan cek di [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```
int loudness;

void setup()
{
    Serial.begin(9600);
}

void loop()
{
    loudness = analogRead(0);
    Serial.println(loudness);
    delay(200);
}

```

- **Langkah 2.** Buka serial monitor untuk memantau output. Ini akan terjadi perubahan yang signifikan saat meniupkan udara ke arah sensor.

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/seeeduino_serial.png)



### Bermain Dengan Raspberry Pi (Dengan Grove Base Hat untuk Raspberry Pi)

#### Perangkat keras

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi | Grove - Loudness Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/LoudnessSensor_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html)

- **Langkah 2**. Pasang Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan Grove - Loudness Sensor ke port A0 dari Base Hat.
- **Langkah 4**. Hubungkan Raspberry Pi ke PC melalui kabel USB.
![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/withrpi_basehat.jpg)


#### Perangkat lunak

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi lingkungan pengembangan.
- **Langkah 2**. Unduh file sumber dengan mengkloning library grove.py. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3.** Eksekusi perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_loudness_sensor.py 0
```


Berikut ini adalah kode grove_water_sensor.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveLoudnessSensor:

    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def value(self):
        return self.adc.read(self.channel)

Grove = GroveLoudnessSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveLoudnessSensor(int(sys.argv[1]))

    print('Detecting loud...')
    while True:
        value = sensor.value
        if value > 10:
            print("Loud value {}, Loud Detected.".format(value))
            time.sleep(.5)

if __name__ == '__main__':
    main()


```


!!!Sukses
    Jika semuanya berjalan dengan baik, Anda akan dapat melihat hasilnya seperti berikut:
```python

pi@raspberrypi:~/grove.py/grove $ python grove_loudness_sensor.py 0
Detecting loud...
Loud value 15, Loud Detected.
Loud value 11, Loud Detected.
Loud value 250, Loud Detected.
Loud value 429, Loud Detected.
Loud value 203, Loud Detected.
Loud value 16, Loud Detected.
Loud value 11, Loud Detected.
^CTraceback (most recent call last):
  File "grove_loudness_sensor.py", line 68, in <module>
    main()
  File "grove_loudness_sensor.py", line 65, in main
    time.sleep(.5)
KeyboardInterrupt


```

Anda dapat menggunakan sensor ini untuk mendeteksi intensitas suara atau kebisingan. Tekan ++ ctrl + c ++ untuk keluar.


!!!Perhatikan
        Anda mungkin perlu memperhatikan bahwa untuk port analog, nomor pin layar silk tertulis  seperti **A1, A0**, namun dalam perintah kita menggunakan parameter **0** dan **1**, sama seperti port digital. Jadi pastikan Anda memasang modul ke port yang benar, jika tidak, mungkin akan ada masalah pada pin.

         


### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

**Perangkat keras**

- **Langkah 1.** Siapkan perangkat di bawah ini:

| Raspberry pi | GrovePi_Plus | Grove-Loudness Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/LoudnessSensor_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Loudness-Sensor-p-1382.html)|


- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove-Loudness Sensor ke **A0** port GrovePi_Plus.
- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/img/rpi_loudness.jpg)

**Perangkat lunak**

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2.** lakukan Git clone untuk repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Langkah 3.** Eksekusi perintah di bawah ini untuk memantau kebisingan.

```python
cd ~/GrovePi/Software/Python
python grove_loudness_sensor.py
```

Berikut adalah kode grove_loudness_sensor.py.

```python
import time
import grovepi

# Hubungkan Grove Loudness Sensor ke port analog A0
# SIG,NC,VCC,GND
loudness_sensor = 0

while True:
    try:
        # Baca level suara
        sensor_value = grovepi.analogRead(loudness_sensor)

        print("sensor_value = %d" %sensor_value)
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- **Langkah 4.** Kita akan melihat kondisi kebisingan seperti di bawah ini.

```python
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_loudness_sensor.py
sensor_value = 135
sensor_value = 23
sensor_value = 196
sensor_value = 258
sensor_value = 98
sensor_value = 131
```

## FAQ

- Q1: Apa perbedaan antara sensor Grove-Loudness dan Grove - Sound Sensor?
    - A1: Sensor Grove-Loudness memiliki potensiometer untuk menyesuaikan output gain .

## Sumber-sumber

- **[Eagle&PDF]** [Grove - Loudness Sensor Schematic](https://github.com/SeeedDocument/Grove-Loudness_Sensor/raw/master/res/Grove%20-%20Loudness%20Sensor%20Eagle%20File_v0.9b.zip)
- **[Datasheet]** [LM2904DR Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Loudness_Sensor/master/res/LM2904DR.pdf)

## Proyek

**Solar Powered Environmental Monitoring**: Solar-powered open source kit adalah Kit open source bertenaga surya untuk memantau kualitas udara, intensitas suara, kelembaban, dan suhu.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/taifur/solar-powered-environmental-monitoring-kit-b1d03d/embed' width='350'></iframe>

**The Da Vinci Code**: Karya ini menggabungkan seni dan elektronik. Bagian seni membuat kerangka dan terdiri dari 11 lapisan papan  dengan serat kerapatan yang menengah.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/coding-with-da-vince/the-da-vinci-code-3b91a8/embed' width='350'></iframe>


## Tech Support / Bantuan
Harap jangan ragu untuk mengirim masukan masalah kepada kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>