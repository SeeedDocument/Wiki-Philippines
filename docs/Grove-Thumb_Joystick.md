---
name: Grove - Thumb Joystick
category: Sensor
bzurl: https://seeedstudio.com/Grove-Thumb-Joystick-p-935.html
oldwikiname: Grove_-_Thumb_Joystick
prodimagename: Bgjoy1.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/bgjoy1.jpg
surveyurl: https://www.research.net/r/Grove-Thumb_Joystick
sku: 101020028
tags: grove_analog, io_3v3, io_5v, plat_duino,plat_pi
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/Bgjoy1.jpg)

Grove - Thumb Joystick adalah modul yang kompatibel dengan Grove yang sangat mirip dengan joystick 'analog' pada pengontrol PS2 (PlayStation 2). Sumbu X dan Y terdiri dari dua potensiometer ~ 10 k yang mengontrol pergerakan 2D dengan menghasilkan sinyal analog. Joystick juga memiliki tombol yang dapat digunakan untuk aplikasi khusus. Ketika modul dalam mode kerja, itu akan menampilkan dua nilai analog yang mewakili dua arah. Dibandingkan dengan joystick normal, nilai outputnya dibatasi untuk rentang yang lebih kecil (yaitu 200 ~ 800), hanya ketika ditekan bahwa nilai X akan diatur ke 1023 dan MCU dapat mendeteksi penekanan.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Thumb-Joystick-p-935.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Versi

| Versi Produk              | Perubahan                                                                                                                                                                                    | Tanggal dirilis |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Grove - Thumb Joystick V1.1 | Initial                                                                                                                                                                                    | Oct 2016      |

## Spesifikasi

| Deskripsi                                | Min  | Typical | Max  | Unit |
|-------------------------------------|------|---------|------|------|
| Tegangan kerja                     | 4.75 | 5.0     | 5.25 | V    |
| Nilai Output Analog （X coordinate） | 206  | 516     | 798  | \    |
| Nilai Output Analog （Y coordinate） | 203  | 507     | 797  | \    |


!!!Tip
    Lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

Platform yang didukung
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai

!!!Catatan
    Jika ini adalah pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk melihat [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) before the start.

### Bermain dengan Arduino

#### Demonstrasi
The Grove - Thumb Joystick adalah perangkat analog yang mengeluarkan sinyal analog mulai dari 0 hingga 1023. Maka, diharuskan menggunakan port analog Arduino untuk membaca nilai tersebut.

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Thumb Joystick |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/Bgjoy1_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Thumb-Joystick-p-935.html)|

- **Langkah 2.** Hubungkan modul Grove - Thumb Joystick ke port **A0/A1** dari Grove - Base Shield dengan menggunakan kabel 4-pin grove.
- **Langkah 3.** Pasangkan modul Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan modul Seeeduino ke PC dengan kabel USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/Grove-Thumb_Joystick.jpg)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Thumb Joystick ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove - Thumb Joystick |
|-----------------|-------------------------|
| 5V              | Merah                   |
| GND             | Hitam                   |
| A1              | Putih                   |
| A0              | Kuning                  |

#### Software (Perangkat Lunak)

- **Langkah 1.** Copy dan paste kode dibawah ini ke Arduino.

```c
/*
  Thumb Joystick demo v1.0
  by:http://www.seeedstudio.com
  connect the module to A0&A1 for using;
*/

void setup()
{
    Serial.begin(9600);
}

void loop()
{
    int sensorValue1 = analogRead(A0);
    int sensorValue2 = analogRead(A1);

    Serial.print("The X and Y coordinate is:");
    Serial.print(sensorValue1, DEC);
    Serial.print(",");
    Serial.println(sensorValue2, DEC);
    Serial.println(" ");
    delay(200);
}
```

- **Langkah 2.** Anda dapat memeriksa nilai-nilai sinyal output analog dengan membuka Serial Monitor.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/Grove-Thumd_Joystick_Result.jpg)

Nilai output dari port analog Arduino dapat dikonversi ke resistansi yang sesuai dengan menggunakan rumus: R=(float)(1023-sensorValue)\*10/sensorValue.

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan modul Grove - Thumb Joystick ke port A0 dari Base Shield.

**Langkah 2.** Pasangkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan modul Seeeduino/Arduino ke PC dengan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/cc_Thumb_Joystick.png)

Download (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode selesai di-download (unggah), Anda akan melihat koordinat X dan Y ditampilkan di Serial Monitor.

### Bermain dengan Raspberry Pi (menggunakan Grove Base Hat untuk Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Thumb Joystick |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/Bgjoy1_small.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Thumb-Joystick-p-935.html)|



- **Langkah 2**. Pasangkan modul Grove Base Hat ke Raspberry.
- **Langkah 3**. Hubungkan modul Thumb Joystick  ke port A0 dari Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry Pi ke PC dengan kabel USB.


![](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/Thumb_Hat.jpg)


!!! Catatan
    Untuk langkah 3 Anda dapat menghubungkan sensor cahaya ke **sembarang port Analog** tetapi pastikan Anda mengubah perintah dengan nomor port yang sesuai.


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengonfigurasi pengembangan proyek.
- **Langkah 2**. Download (unduh) file sumber dengan memperbanyak grove.py library. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_thumb_joystick.py 0

```
!!!Catatan
    Anda dapat menjalankan program dengan ++ python grove_thumb_joystick.py pin ++, dimana pin bisa menjadi salah satu dari {0, 2, 4, 6} dalam grup ADC dan menghubungkan perangkat ke slot yang sesuai {A0, A2, A4, A6}.

Berikut kode grove_thumb_joystick.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveThumbJoystick:

    def __init__(self, channelX, channelY):
        self.channelX = channelX
        self.channelY = channelY
        self.adc = ADC()

    @property
    def value(self):
        return self.adc.read(self.channelX), self.adc.read(self.channelY)

Grove = GroveThumbJoystick


def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.ADC)
    pin = sh.argv2pin()

    sensor = GroveThumbJoystick(int(pin), int(pin + 1))

    while True:
        x, y = sensor.value
        if x > 900:
            print('Joystick Pressed')
        print("X, Y = {0} {1}".format(x, y))
        time.sleep(.2)

if __name__ == '__main__':
    main()


```

!!!sukses
    Jika semuanya berjalan dengan baik, Anda akan dapat melihat hasil berikut
    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_thumb_joystick.py 0
Hat Name = 'Grove Base Hat RPi'
X, Y = 506 484
X, Y = 484 484
X, Y = 506 484
X, Y = 506 487
Joystick Pressed
X, Y = 999 485
X, Y = 310 736
X, Y = 681 484
Joystick Pressed
X, Y = 999 277
Joystick Pressed
X, Y = 999 487
X, Y = 506 484
X, Y = 501 486
X, Y = 509 484
X, Y = 511 486
X, Y = 510 485
^CTraceback (most recent call last):
  File "grove_thumb_joystick.py", line 69, in <module>
    main()
  File "grove_thumb_joystick.py", line 66, in main
    time.sleep(.2)
KeyboardInterrupt

```


Anda dapat keluar dari program ini hanya dengan menekan ++ctrl+c++.

!!!Perhatian
        Anda mungkin telah memperhatikan bahwa untuk port analog, nomor pin silkscreen adalah sesuatu seperti **A1, A0**, namun dalam perintah kami menggunakan parameter **0** dan **1**, sama seperti port digital. Jadi pastikan Anda pasang modul ke port yang benar, agar tidak terjadi pin yang konflik.




### Bermain dengan Raspberry Pi (menggunakan GrovePi_Plus)

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Thumb Joystick |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/Bgjoy1_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Thumb-Joystick-p-935.html)|


- **Langkah 2.** Pasangkan modul GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan modul Grove-Thumb Joystick ke port **A0** dari GrovePi_Plus.
- **Langkah 4.** Hubungkan modul Raspberry ke PC dengan kabel USB.

![](https://github.com/SeeedDocument/Grove-Thumb_Joystick/raw/master/img/Pi_Joystick%20connection.jpg)

#### Software (Perangkat Lunak)

- **Langkah 1.** Arahkan ke direktori demo:

```
cd yourpath/GrovePi/Software/Python/

```

- **Langkah 2.**  Untuk melihat kode

```
nano grove_thumb_joystick.py   # "Ctrl+x" to exit #
```

```python
import time
import grovepi

# Connect the Grove Thumb Joystick to analog port A0

# GrovePi Port A0 uses Arduino pins 0 and 1
# GrovePi Port A1 uses Arduino pins 1 and 2
# Don't plug anything into port A1 that uses pin 1
# Most Grove sensors only use 3 of their 4 pins, which is why the GrovePi shares Arduino pins between adjacent ports
# If the sensor has a pin definition SIG,NC,VCC,GND, the second (white) pin is not connected to anything

# If you wish to connect two joysticks, use ports A0 and A2 (skip A1)

# Uses two pins - one for the X axis and one for the Y axis
# This configuration means you are using port A0
xPin = 0
yPin = 1
grovepi.pinMode(xPin,"INPUT")
grovepi.pinMode(yPin,"INPUT")

# The Grove Thumb Joystick is an analog device that outputs analog signal ranging from 0 to 1023
# The X and Y axes are two ~10k potentiometers and a momentary push button which shorts the x axis

# My joystick produces slightly different results to the specifications found on the url above
# I've listed both here:

# Specifications
#     Min  Typ  Max  Click
#  X  206  516  798  1023
#  Y  203  507  797

# My Joystick
#     Min  Typ  Max  Click
#  X  253  513  766  1020-1023
#  Y  250  505  769
while True:
    try:
        # Get X/Y coordinates
        x = grovepi.analogRead(xPin)
        y = grovepi.analogRead(yPin)

        # Calculate X/Y resistance
        Rx = (float)(1023 - x) * 10 / x
        Ry = (float)(1023 - y) * 10 / y

        # Was a click detected on the X axis?
        click = 1 if x >= 1020 else 0

        print "x =", x, " y =", y, " Rx =", Rx, " Ry =", Ry, " click =", click
        time.sleep(.5)

    except IOError:
        print "Error"
```

- **Langkah 3.** Jalankan demo.

```
sudo python grove_thumb_joystick.py
```

- **Langkah 4.** Kita akan melihat tampilan output pada terminal seperti di bawah ini.

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/img/pi_result.png)|

Sumber - Sumber
---------

- **[Eagle]** [Grove-Thumb Joystick Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/res/Eagle_Design_Files.zip)
- **[Datasheet]** [Analog Joystick Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/res/Analog_Joystick_Datasheet.jpg)
- **[PDF]** [Joystick Schematic PDF File](https://github.com/SeeedDocument/Grove-Thumb_Joystick/raw/master/res/Joystick.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Thumb_Joystick/master/res/Grove_Thumb_Joystick_CDC_File.zip)

## Proyek

**Raspberry pi music server**: Langkah pertama untuk proyek Raspberry Pi.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/kishima7/raspberry-pi-music-server-f5a0ae/embed' width='350'></iframe>

**Membuat pengontrol minecraft sendiri**: Membuat pengontrol minecraft sendiri dengan GrovePi.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/dexterindustries/build-a-custom-minecraft-controller-d55d9c/embed' width='350'></iframe>

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>