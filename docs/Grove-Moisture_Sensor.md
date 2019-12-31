---
name: Grove - Moisture Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html
oldwikiname: Grove - Moisture Sensor
prodimagename: Moisture_sensor_.jpg
surveyurl: https://www.research.net/r/grove-moisture-sensor
sku: 101020008
---

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/Moisture_sensor_.jpg)

Sensor Kelembaban ini dapat digunakan untuk mendeteksi kelembaban tanah atau menilai jika ada air di sekitar sensor, biarkan tanaman di kebun Anda dapat terbantu ketika mereka kekurangan air. Sensor ini sangat mudah digunakan, Anda cukup memasukkan sensor ke dalam tanah dan membaca datanya. Dengan sensor ini, Anda dapat membuat proyek kecil yang dapat membuat tanaman mengirimkan pesan kepada Anda seperti "Saya haus sekarang, tolong beri saya air."

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Versi

| Versi Produk              | Perubahan                                   | Tanggal Rilis |
|------------------------------|-------------------------------------------|---------------|
| Grove - Moisture Sensor V1.4 | Pertama                                   | Juni 2014     |


## Fitur - Fitur

- Sensor kelembaban tanah berdasarkan pengukuran hambatan dalam tanah
- Mudah digunakan
- Modul Grove berukuran 2.0 cm X 6.0 cm

!!!Tips
    Selengkapnya tentang modul Grove bisa mengacu ke [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi

|Item|Condition|Min|Typical|Max|Unit|
|---|---|---|---|---|---|
|Voltage|-|3.3|-|5|V|
|Current|-|0|-|35|mA|
|Output Value|Sensor in dry soil<br>Sensor in humid soil<br>Sensor in water|0<br>300<br>700<br>|-|300<br>700<br>950|-|


## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Application Ideas

- Berkebun Botani (Botanical Gardening)
- Memantau Kelembaban
- Konsistensi Pengukuran

## Memulai

!!!Catatan
    Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


### Bermain dengan Arduino

**Hardware**

- **Langkah 1.** Siapkan komponen dibawah ini:

| Seeeduino V4.2 | Base Shield|  Grove-Moisture Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)|

- **Langkah 2.** Hubungkan Grove-Moisture Sensor ke port A0 pada Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB. 

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Seeeduino_moisture.jpg)

!!!Catatan
    Jika tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Moisture Sensor ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove-Moisture Sensor |
|---------------|-------------------------|
| 5V           | Red                     |
| GND           | Black                   |
| Not Conencted | White                   |
| A0            | Yellow                  |

**Software**

- **Langkah 1.** Salin kode dibawah ini ke Arduio IDE dan unggah (upload) ke arduino. Jika anda tidak mengetahui cara unggah kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

```c++
int sensorPin = A0;
int sensorValue = 0;

void setup() {
    Serial.begin(9600);
}
void loop() {
    // Membaca nilai kelembaban dari sensor:
    sensorValue = analogRead(sensorPin);
    Serial.print("Moisture = " );
    Serial.println(sensorValue);
    delay(1000);
}
```

- **Langkah 2.** Kita akan melihat tampilan nilai kelembaban pada terminal seperti dibawah ini.

```
Moisture = 0
Moisture = 31
Moisture = 48
Moisture = 139
Moisture = 155
Moisture = 124
Moisture = 236
Moisture = 218
Moisture = 215
Moisture = 221
```

### Bermain dengan Codecraft

#### Hardware

**Langkah 1.** Hubungkan Grove - Moisture Sensor ke port A0 pada Base Shield.

**Langkah 2.** Pasang Grove - Base Shield ke Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda melalui kabel USB.


#### Software

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/),  tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Tarik blok seperti gambar dibawah atau buka file cdc yang mana dapat didownload (diunduh) pada akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Moisture_Sensor/master/img/cc_Moisture_Sensor.png)

Unggah (Upload) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode berhasil di unggah, anda dapat melihat nilai kelembaban yang ditampilkan pada Serial Monitor.

### Bermain dengan Raspberry Pi (Dengan Grove Base Hat untuk Raspberry Pi)

#### Hardware

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi | Grove - Moisture Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)

- **Langkah 2**. Pasang Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan Grove - Moisture Sensor ke port A0 pada Base Hat.
- **Langkah 4**. Hubungkan Raspberry ke PC melalui kabel USB.
![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/with_hat.jpg)


#### Software

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Unduh (Download) file sumbernya dengan menduplikat library grove.py .

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Eksekusi perintah dibawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_moisture_sensor.py 0
```


berikut adalah kode grove_moisture_sensor.py .

```python
#!/usr/bin/env python
# -*- coding: utf-8 -*-
#
# Lisensi MIT (MIT)
#
# Grove Base Hat untuk Raspberry Pi, digunakan untuk menghubungkan sensor grove.
# Copyright (C) 2018  Seeed Technology Co.,Ltd.
'''
Berikut kode untuk
    - Grove - Moisture Sensor <https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html>`_

Contoh:

    .. code-block:: python

        import time
        from grove.grove_moisture_sensor import GroveMoistureSensor

        # connect to alalog pin 2(slot A2)
        PIN = 2

        sensor = GroveMoistureSensor(PIN)

        print('Detecting moisture...')
        while True:
            m = sensor.moisture
            if 0 <= m and m < 300:
                result = 'Dry'
            elif 300 <= m and m < 600:
                result = 'Moist'
            else:
                result = 'Wet'
            print('Moisture value: {0}, {1}'.format(m, result))
            time.sleep(1)
'''
import math
import sys
import time
from grove.adc import ADC

__all__ = ["GroveMoistureSensor"]

class GroveMoistureSensor:
    '''
    Grove Moisture Sensor class

    Args:
        pin(int): number of analog pin/channel the sensor connected.
    '''
    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def moisture(self):
        '''
        Get the moisture strength value/voltage

        Returns:
            (int): voltage, in mV
        '''
        value = self.adc.read_voltage(self.channel)
        return value

Grove = GroveMoistureSensor


def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.ADC)
    pin = sh.argv2pin()

    sensor = GroveMoistureSensor(pin)

    print('Detecting moisture...')
    while True:
        m = sensor.moisture
        if 0 <= m and m < 300:
            result = 'Dry'
        elif 300 <= m and m < 600:
            result = 'Moist'
        else:
            result = 'Wet'
        print('Moisture value: {0}, {1}'.format(m, result))
        time.sleep(1)

if __name__ == '__main__':
    main()
```


!!!sukses
    Jika semuanya berjalan dengan baik, anda dapat melihat hasilnya seperti berikut ini

```python

pi@raspberrypi:~/grove.py/grove $ python grove_moisture_sensor.py 0
Detecting moisture...
Moisture value: 0, Dry
Moisture value: 1, Dry
Moisture value: 25, Dry
Moisture value: 3, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 0, Dry
Moisture value: 1, Dry
^CTraceback (most recent call last):
  File "grove_moisture_sensor.py", line 74, in <module>
    main()
  File "grove_moisture_sensor.py", line 71, in main
    time.sleep(1)
KeyboardInterrupt


```

Anda dapat menggunakan sensor ini untuk mendeteksi kualitas udara. Tekan **ctrl+c** untuk keluar.


!!!Perhatian
        Anda perlu memperhatikan bahwa untuk port analog, nomor pin pada silkscreen adalah sesuatu seperti **A1, A0**, namun dalam perintah kita menggunakan parameter **0** dan **1**, sama seperti port digital. Jadi pastikan Anda menghubungkan modul ke port yang benar,jika tidak, ada kemungkinan terjadinya konflik pin.


### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

**Hardware**

- **Langkah 1.** Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove-Moisture Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)|


- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove-Moisture Sensor ke port **A0** pada GrovePi_Plus.
- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/rpi_moisture.jpg)

**Software**

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2.** Lakukan Git clone pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-	**Langlah 3.** Jalankan perintah dibawah untuk menggunakan Grove-Moisture Sensor untuk mengukur kelembaban.


```
cd ~/GrovePi/Software/Python
python grove_moisture_sensor.py
```

Berikut adalah kode grove_moisture_sensor.py .

```python
# 	Berikut adalah nilai sensor yang disarankan:
# 		Min  Typ  Max  Kondisi
# 		0    0    0    sensor di udara terbuka
# 		0    20   300  sensor di tanah kering
# 		300  580  700  sensor di tanah lembab
# 		700  940  950  sensor di air


import time
import grovepi

# Hubungkan Grove Moisture Sensor ke port analog A0
# SIG,NC,VCC,GND
sensor = 0

while True:
    try:
        print(grovepi.analogRead(sensor))
        time.sleep(.5)

    except KeyboardInterrupt:
        break
    except IOError:
        print ("Error")
```

- **Step 4.** Kita akan melihat nilai dari kelembaban yang ada pada terminal seperti berikut.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_moisture_sensor.py
0
90
130
150
160
218
238
```

### Bermain dengan TI LaunchPad

**Hardware**

Sketsa (sketch) berikut ini menunjukkan aplikasi sederhana untuk mendeteksi kelembaban di tanah. Dengan ini, anda dapat mengetahui apakah tanaman Anda membutuhkan air atau tidak dengan mengamati hasil dari output sensor.

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/Moisture.jpg)

**Software**

```c
/*
  Moisture-Sensor
  Sketsa (sketch) berikut menunjukkan aplikasi pendeteksi sederhana
  kelembaban tanah. Anda bisa tahu apakah tanaman membutuhkan air
  atau tidak dengan mengamati hasil output sensor.

  Rangkaian:
    * Moisture-Sensor dipasangkan pada pin 24 (J6 Plug pada Grove Base BoosterPack)
    * Satu sisi pin (salah satu) ke ground
    * sisi pin satunya ke +VCC
    * Anoda LED (kaki panjang) dihubungkan ke RED_LED
    * Katoda LED (kaki pendek) dihubungkan ke ground
  - Catatan:
    Contoh kode ini dalam domain publik.
    http://seeedstudio.com/wiki/Grove_-_Moisture_Sensor
*/
#include "TM1637.h"
/* Definisi */
#define CLK 39              /* 4-digital display clock pin */
#define DIO 38              /* 4-digiral display data pin */
#define BLINK_LED RED_LED   /* blink led */
#define MOISTURE_PIN 24     /* pin of moisture sensor */
#define THRESHOLD_VALUE 300 /* threshold for watering the flowers */
#define ON HIGH             /* led on */
#define OFF LOW             /* led off */
#define _handle_led(x) digitalWrite(BLINK_LED, x) /* handle led */

/* Variabel Global */
TM1637 tm1637(CLK, DIO);    /* 4-digital display object */
int analog_value = 0;       /* varibel untuk menyimpan nilai yang berasal dari rotary angle
sensor */
int8_t bits[4] = {0};       /* array untuk menyimpan bit tunggal dari sebuah nilai */
/* metode setup() berjalan sekali, ketika sketsa mulai dijalankan */
void setup() {
/* Inisialisasi 4-digital display */
    tm1637.init();
    tm1637.set(BRIGHT_TYPICAL);
/* deklarasi red_led pin sebagai OUTPUT */
    pinMode(BLINK_LED, OUTPUT);
}
/* metode loop() bekerja berulang-ulang */
void loop() {
    analog_value = analogRead(MOISTURE_PIN); /* read the value from the sensor */
/* jika nilai lebih kecil dari batas (Threshold), nyalakan LED */
    if(analog_value < THRESHOLD_VALUE) {
        _handle_led(ON);
    } else {
        _handle_led(OFF);
    }
    memset(bits, 0, 4); /* reset array when we use it */
    for(int i = 3; i >= 0; i--) {
/* ambil nilai bit tunggal dari nilai analog */
        bits[i] = analog_value % 10;
        analog_value = analog_value / 10;
        tm1637.display(i, bits[i]); /* display by 4-digital display */
    }
    delay(200);
}
```

## Pertanyaan yang sering ditanyakan (FAQs)

**Q1: Apa nilai outputnya? Tegangan atau Hitungan?**

A1: Outputnya merupakan nilai tegangan. Ketika menggunakan analogRead(), 5V akan dibagi dengan 1023. Jadi nilai output = Vout * 1023/5. Semakin tinggi tegangan output, semakin besar nilai kelembabannya.

## Sumber-Sumber

- [**Eagle&PDF**][Grove - Moisture Sensor v1.4 Schematic](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/resources/Grove%20-%20Moisture%20Sensor%20v1.4.zip)
- [**Codecraft**][CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Moisture_Sensor/master/res/Grove_Moisture_Sensor_CDC_File.zip)


## Proyek - Proyek

**Plant Monitoring System using AWS IoT**: Jika anda merencanakan liburan, ini adalah proyek bagus untuk memantau suhu dan kelembaban tanah dari tanaman anda menggunakan dweet.io dan AWS IoT. 

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/carmelito/plant-monitoring-system-using-aws-iot-6cb054/embed' width='350'></iframe>



## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>