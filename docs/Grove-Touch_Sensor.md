---
name: Grove - Touch Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Touch-Sensor-p-747.html
oldwikiname: Grove_-_Touch_Sensor
prodimagename: Grove-Touch_Sensor.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020037 1.jpg
surveyurl: https://www.research.net/r/Grove-Touch_Sensor
sku: 101020037
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Touch_Sensor/master/img/surface.jpg)

Grove - Touch Sensor memungkinkan Anda untuk mengganti penekanan dengan sentuhan. Ini dapat mendeteksi perubahan kapasitansi ketika jari mendekat. Itu berarti tidak masalah jari Anda langsung menyentuh pad atau hanya tetap dekat dengan pad, Grove - Touch Sensor juga akan menghasilkan keluaran HIGH.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Touch-Sensor-p-747.html)

## Spesifikasi

- Tegangan operasi : 2.0 - 5.5V
- Arus Operasi (Vcc=3V):1.5 - 3.0μA
- Arus Operasi (VDD=3V):3.5 - 7.0μA
- Output Response Time: 60 - 220mS
- Chipset : TTP223-BA6

!!!Tips
    Detail lebih lanjut tentang modul Grove silakan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Platform yang Didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri..


**Fitur Pilihan**

| AHLB                     | TOG         | LPMB       | MOTB         | SLRFTB          | RST       | Q           | OPDO            |
|--------------------------|-------------|------------|--------------|-----------------|-----------|-------------|-----------------|
| Output Active High / Low | Toggle mode | Power Mode | Max. On Time | Sampling length | RESET PIN | CMOS Output | Open Drain Mode |
| V                        | V           | 0          | 1            | 1               | X         | V           | X               |
| Active High              | Disabled    | LOW        | Infinite     | 1.6 msec        | N/A       | Present     | N/A             |

## Memulai


### Bermain dengan Arduino

Demo ini akan menunjukkan kepada Anda bagaimana menyalakan / mematikan LED.

#### Perangkat Keras

- **Langkah 1.** Siapkan perangkat di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove-Touch_Sensor |Grove-LED|
|--------------|-------------|-----------------|-----|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Touch_Sensor/raw/master/img/45d_small.jpg)|![enter image description](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Touch-Sensor-p-747.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Red-LED-p-1142.html)|

- **Langkah 2.** Hubungkan Grove-Touch_Sensor ke port **D2** dari Grove-Base Shield.
- **Langkah 3.** Hubungkan Grove-LED ke port **D3** Dari Grove-Base Shield.
- **Langkah 4.** Pasangkan Grove - Base Shield dengan Seeeduino.
- **Langkah 5.** Hubungkan Seeeduino ke PC menggunakan kabel USB .



![with_ardu](https://github.com/SeeedDocument/Grove-Touch_Sensor/raw/master/img/with_ardu.jpg)

#### Software
 - **Langkah 1.** Silahkan salin(ctrl+c, ctrl+v) kode program di bawah ini ke skecth Arduino yang baru.
```c
const int TouchPin=2;
const int ledPin=3;

void setup() {
    pinMode(TouchPin, INPUT);
    pinMode(ledPin,OUTPUT);
}

void loop() {
    int sensorValue = digitalRead(TouchPin);
    if(sensorValue==1)
    {
        digitalWrite(ledPin,HIGH);
    }
    else
    {
        digitalWrite(ledPin,LOW);
    }
}
```
**Langkah 2.** Memantau led on and off.

### Bermain dengan Codecraft

#### Hardware

**Langkah 1.** Hubungkan Grove - Touch Sensor ke port D2, and hubungkan Grove - Red LED ke port D3 dari Base Shield.

**Langkah 2.** Pasangkan Base Shield ke  Seeeduino/Arduino anda.

**Langkah 3.** Sambungkan Seeeduino/Arduino to PC anda melalui kabel USB.

#### Software

**Langkah 1.** Buka halaman [Codecraft](https://ide.chmakered.com/), tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Seret (drag) blok-blok yang ada seperti gambar dibawah ini atau buka file cdc yang dapat diunduh pada akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Touch_Sensor/master/image/cc_Touch_Sensor.png)

Upload program ke Arduino/Seeeduino anda.

!!!Sukses
    Saat kode selesai diupload, maka LED akan menyala ketika anda menyentuh Touch Sensor.

### Bermain dengan Raspberry Pi (With Grove Base Hat for Raspberry Pi)

#### Perangkat Keras

- **Langkah 1**. Hal-hal yang digunakan pada proyek ini adalah:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Touch Sensor|
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Touch_Sensor/raw/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Touch-Sensor-p-747.html)|



- **Langkah 2**. Plug the Grove Base Hat into Raspberry.
- **Langkah 3**. Connect the touch sensor to port 12 of the Base Hat.
- **Langkah 4**. Connect the Raspberry Pi to PC through USB cable.


![](https://github.com/SeeedDocument/Grove-Touch_Sensor/raw/master/img/Touch_Hat.jpg)


!!! Note
    Untuk langkah 3 anda dapat menghubungkan touch sensor keto **semua port GPIO** tetapi pastikan anda mengubah perintah dengan nomor pin yang tepat.


#### Software

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Download file sumbernya dengan menduplikasi the grove.py library. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Eksekusi perintah dibawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_touch_sensor.py 12

```

Berikut ini adalah kode untuk grove_touch_sensor.py.

```python

import time
from grove.gpio import GPIO


class GroveTouchSensor(GPIO):
    def __init__(self, pin):
        super(GroveTouchSensor, self).__init__(pin, GPIO.IN)
        self._last_time = time.time()

        self._on_press = None
        self._on_release = None

    @property
    def on_press(self):
        return self._on_press

    @on_press.setter
    def on_press(self, callback):
        if not callable(callback):
            return

        if self.on_event is None:
            self.on_event = self._handle_event

        self._on_press = callback

    @property
    def on_release(self):
        return self._on_release

    @on_release.setter
    def on_release(self, callback):
        if not callable(callback):
            return

        if self.on_event is None:
            self.on_event = self._handle_event

        self._on_release = callback

    def _handle_event(self, pin, value):
        t = time.time()
        dt, self._last_time = t - self._last_time, t

        if value:
            if callable(self._on_press):
                self._on_press(dt)
        else:
            if callable(self._on_release):
                self._on_release(dt)

Grove = GroveTouchSensor


def main():
    import sys

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    touch = GroveTouchSensor(int(sys.argv[1]))

    def on_press(t):
        print('Pressed')
    def on_release(t):
        print("Released.")

    touch.on_press = on_press
    touch.on_release = on_release

    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!sukses
    Jika semuanya berjalan baik dan tidak ada error, maka anda dapat melihat hasilnya sebagai berikut.
    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_touch_sensor.py 12
Pressed
Released.
Pressed
Released.
Pressed
Released.
Pressedw
Released.
^CTraceback (most recent call last):
  File "grove_touch_sensor.py", line 110, in <module>
    main()
  File "grove_touch_sensor.py", line 106, in main
    time.sleep(1)
KeyboardInterrupt

```


Anda dapat keluar dari program dengan menekan tombol ++ctrl+c++.




### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

#### Hardware

- **Langkah 1.** Persiapkan perangkat berikut ini:

<!--false link-->
| Raspberry pi | GrovePi_Plus | Grove-Touch_Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Touch_Sensor/raw/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Touch-Sensor-p-747.html)|


- **Langkah 2.** Pasangkan GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove-Touch_Sensor ke port **D2** GrovePi_Plus.
- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![with_rpi](https://github.com/SeeedDocument/Grove-Touch_Sensor/raw/master/img/with_rpi.jpg)

#### Perangkat Lunak

- **Langkah 1.** Ikuti [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi lingkungan pengembangan (Development Environment).
- **Langkah 2.** Lakukan Git Clone pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-	**Langkah 3.** Eksekusi perintah di bawah ini untuk menggunakan sensor ini, silakan ubah port dari D4 menjadi ke D2.


```bash
python grove_touch_sensor.py
```

```Python
#!/usr/bin/env python
#
# Contoh GrovePi untuk menggunakan Grove Touch Sensor (http://www.seeedstudio.com/wiki/Grove_-_Touch_Sensor)
#
# GrovePi menghubungkan sensor Raspberry Pi dan Grove. Anda dapat mempelajari lebih lanjut tentang GrovePi di sini:  http://www.dexterindustries.com/GrovePi
#
# Punya pertanyaan tentang contoh ini? Tanyakan di forum ini: http://forum.dexterindustries.com/c/grovepi
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

# Hubungkan Grove Touch Sensor ke port digital D2
# SIG,NC,VCC,GND
touch_sensor = 2

grovepi.pinMode(touch_sensor,"INPUT")

while True:
    try:
        print(grovepi.digitalRead(touch_sensor))
        time.sleep(.5)

    except IOError:
        print ("Error")

```
Inilah Hasilnya :

![](https://github.com/SeeedDocument/Grove-Touch_Sensor/raw/master/img/rpi_result.jpg)


## Sumber-sumber


-  **[Eagle]** [Grove-Touch_Sensor Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Touch_Sensor/master/res/Touch_sensor_Eagle_File.zip)
-  **[PDF]** [TTP223](https://raw.githubusercontent.com/SeeedDocument/Grove-Touch_Sensor/master/res/TTP223.pdf)
-  **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Touch_Sensor/master/resource/Grove_Touch_Sensor_CDC_File.zip)


## Proyek

**Menggunakan Grove Touch Sensor Untuk Mengontrol Grove LED**: Cara menghubungkan dan menggunakan Grove Touch Sensor untuk mengontrol Grove LED socket kit.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/user50338573/using-grove-touch-sensor-to-control-grove-led-56a5ed/embed' width='350'></iframe>

**Modul sensor sentuh Grove**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/VFKYYG_hNUE" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/vPkf4czFQsY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


## Tech Support/ Bantuan

Harap jangan ragu untuk mengirim masukan masalah kepada kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>