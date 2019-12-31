---
name: Grove - Rotary Angle Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Rotary-Angle-Sensor-p-770.html
oldwikiname: Grove_-_Rotary_Angle_Sensor
prodimagename: Grove-Rotary_Angle_Sensor.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020017 1.jpg
surveyurl: https://www.research.net/r/Grove-Rotary_Angle_Sensor
sku: 101020017
tags: grove_analog, io_3v3, io_5v, plat_duino, plat_linkit, plat_bbg, plat_wio, plat_pi
---

![](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/rotary.jpg)

Sensor rotary angle menghasilkan output analog antara 0 dan Vcc (5V DC dengan Seeeduino) pada konektor D1-nya, sedangkan konektor D2 tidak digunakan. Jangkauan sudut adalah 300 derajat dengan perubahan nilainya yang linier. Nilai resistansi 10k ohm, cocok untuk penggunaan Arduino. Modul ini juga dikenal sebagai "potensiometer".

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Rotary-Angle-Sensor-p-770.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

Ada produk lain, Grove - Rotary Angle Sensor (P). Apa arti "P"? Dalam produk ini "P" adalah untuk "panel mount". Ini adalah versi turunan dari Grove - Rotary Angle Sensor. Modul ini hampir mirip kecuali Grove connector dipindahkan ke belakang sehingga Anda dapat dengan mudah menggunakannya sebagai perangkat antarmuka yang rapi dan minim kawat.

<table>
    <tr>
        <td>
            <img src="https://raw.githubusercontent.com/SeeedDocument/Grove-Rotary_Angle_Sensor/master/img/Grove-Rotary_Angle_Sensor-P-.jpg">
        </td>
        <td>
            <img src="https://raw.githubusercontent.com/SeeedDocument/Grove-Rotary_Angle_Sensor/master/img/GroveRotaryP_02.jpg">
        </td>
    </tr>
</table>

<p style=":center"><a href="http://www.seeedstudio.com/depot/grove-rotary-angle-sensorp-p-1242.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Versi

| Versi Produk                  | Perubahan                              | Tanggal dirilis |
|-----------------------------------|--------------------------------------|---------------|
|Grove-Rotary Angle Sensor(P) V1.1  | Initial                              | Jan 2013    |   
|Grove-Rotary Angle Sensor V1.2     | Initial                              | May 2014    |    


## Fitur

-   Antarmuka Grove 
-   Mudah digunakan
-   Modul Grove Base 

!!!Tips
    Rincian lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi


<table border="1" cellspacing="0" width="80%">
<tr>
<th scope="col">
Komponen
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
Tegangan
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
VDC
</td>
</tr>
<tr align="center">
<th scope="row">
Sudut putar
</th>
<td>
0
</td>
<td>
~
</td>
<td>
300
</td>
<td>
Deg
</td>
</tr>
<tr align="center">
<th scope="row">
Dimensi
</th>
<td colspan="3">
19x19x30.1
</td>
<td>
mm
</td>
</tr>
</table>

## Platforms yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.

## Memulai

!!!Catatan
    Jika ini adalah pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk melihat ke [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


### Bermain dengan Arduino

**Hardware (Perangkat Keras)**

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove-Rotary Angle Sensor |Grove-LED|
|--------------|-------------|-----------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/rorary_s.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/grove_led.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Rotary-Angle-Sensor-p-770.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-LED-p-767.html)|

- **Langkah 2.** Hubungkan modul Grove-Rotary Angle Sensor ke port **A0** dari Grove-Base Shield.
- **Langkah 3.** Hubungkan modul Grove-LED ke port **D3** dari Grove-Base Shield. 
- **Langkah 4.** Pasangkan modul Grove - Base Shield ke Seeeduino.
- **Langkah 5.** Hubungkan Seeeduino ke PC dengan kabel USB.

![](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/seeeduino_rotary.jpg)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Rotary Angle Sensor dan Grove-Led ke Seeeduino seperti di bawah ini. Grove-Led harus terhubung ke port PWM. Untuk port Seeeduino terdapat pada port D3,5,6,9,10,11. 

| Seeeduino | Grove-Rotary Angle Sensor | Seeeduino | Grove-LED |
|-----------|---------------------------|-----------|-----------|
| 5V        | Merah                       | 5V        | Merah       |
| GND       | Hitam                     | GND       | Hitam   |
| NC        | Putih                     | NC        | Putih     |
| A0        | Kuning                    | D3        | Kuning    |

**Software (Perangkat Lunak)**

- **Langkah 1.** Silakan salin kode di bawah ini ke Arduino IDE dan upload (unggah) ke arduino. Jika Anda tidak tahu cara mengupload (unggah)kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```c++
/*macro definitions of Rotary angle sensor and LED pin*/

#define ROTARY_ANGLE_SENSOR A0
#define LED 3  //the Grove - LED is connected to PWM pin D3 of Arduino
#define ADC_REF 5 //reference voltage of ADC is 5v.If the Vcc switch on the seeeduino
                    //board switches to 3V3, the ADC_REF should be 3.3
#define GROVE_VCC 5 //VCC of the grove interface is normally 5v
#define FULL_ANGLE 300 //full value of the rotary angle is 300 degrees

void setup()
{
    Serial.begin(9600);
    pinMode(ROTARY_ANGLE_SENSOR, INPUT);
    pinMode(LED,OUTPUT);   
}

void loop()
{   
    float voltage;
    int sensor_value = analogRead(ROTARY_ANGLE_SENSOR);
    voltage = (float)sensor_value*ADC_REF/1023;
    float degrees = (voltage*FULL_ANGLE)/GROVE_VCC;
    Serial.println("The angle between the mark and the starting position:");
    Serial.println(degrees);

    int brightness;
    brightness = map(degrees, 0, FULL_ANGLE, 0, 255);
    analogWrite(LED,brightness);
    delay(500);
}

```

- **Langkah 2.** Sesuaikan Grove-Rotary Angle Sensor dan kita akan melihat Grove-LED mengubah kecerahan cahaya.

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan modul Grove - Rotary Angle Sensor ke port A0, dan Hubungkan modul Grove - Red LED ke port D3 dari modul Base Shield.

**Langkah 2.** Pasangkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Rotary_Angle_Sensor/master/img/cc_Rotary_Angle_Sensor.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode selesai di-upload (unggah), kecerahan LED akan bervariasi tergantung pada sudut sensor, dan nilai sudut akan ditampilkan di Serial Monitor.

### Bermain dengan Raspberry Pi (Menggunakan Grove Base Hat untuk Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Rotary Angle Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/rorary_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Rotary-Angle-Sensor--p-1242.html)|


- **Langkah 2**. Pasangkan modul Grove Base Hat ke Raspberry.
- **Langkah 3**. Hubungkan modul rotary sensor ke port A0 dari Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry Pi ke PC menggunakan kabel USB.


![](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/Rotary_Hat.jpg)


!!! Catatan
    Untuk langkah 3 Anda dapat menghubungkan sensor rotary angle ke **sembarang port Analog** tetapi pastikan Anda mengubah perintah dengan nomor port yang sesuai.


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
python grove_rotary_angle_sensor.py 0

```

Berikut kode grove_rotary_angle_sensor.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveRotaryAngleSensor(ADC):
    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()
    
    @property
    def value(self):
        return self.adc.read(self.channel)


Grove = GroveRotaryAngleSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveRotaryAngleSensor(int(sys.argv[1]))

    while True:
        print('Rotary Value: {}'.format(sensor.value))
        time.sleep(.2)


if __name__ == '__main__':
    main()

```

!!!berhasil
    Jika semua berjalan dengan baik, Anda akan melihat hasilnya sebagai berikut

    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_rotary_angle_sensor.py 0
Rotary Value: 932
Rotary Value: 931
Rotary Value: 931
Rotary Value: 931
Rotary Value: 933
Rotary Value: 931
Rotary Value: 742
Rotary Value: 666
Rotary Value: 666
Rotary Value: 549
Rotary Value: 520
Rotary Value: 499
Rotary Value: 430
Rotary Value: 430
Rotary Value: 321
Rotary Value: 286
Rotary Value: 205
Rotary Value: 127
Rotary Value: 88
Rotary Value: 0
Rotary Value: 0
Rotary Value: 0
Rotary Value: 0
Rotary Value: 0
Rotary Value: 0
Rotary Value: 0
^CTraceback (most recent call last):
  File "grove_rotary_angle_sensor.py", line 66, in <module>
    main()
  File "grove_rotary_angle_sensor.py", line 62, in main
    time.sleep(.2)
KeyboardInterrupt


```


Anda dapat keluar dari program ini hanya dengan menekan ++ctrl+c++.

!!!Perhatian
        Anda mungkin telah memperhatikan bahwa untuk port analog, nomor pin silkscreen adalah sesuatu seperti **A1, A0**, namun dalam perintah kami menggunakan parameter **0** dan **1**, sama seperti port digital.Jadi pastikan Anda pasang modul ke port yang benar, agar tidak terjadi pin yang konflik.



### Bermain dengan Raspberry Pi (menggunakan GrovePi_Plus)

**Hardware (Perangkat Keras)**

- **Langkah 1.** Siapkan peralatan dibawah ini:

| Raspberry pi | GrovePi_Plus |  Grove-Rotary Angle Sensor |Grove-LED|
|--------------|-------------|-----------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/rorary_s.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/grove_led.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Rotary-Angle-Sensor-p-770.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-LED-p-767.html)|


- **Langkah 2.** Pasangkan modul GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan modul Grove-Rotary Angle Sensor ke port **A0** dari GrovePi_Plus.
- **Langkah 4.** Hubungkan modul Grove-LED ke port **D5** dari GrovePi_Plus.
- **Langkah 5.** Hubungkan modul Raspberry ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/img/rpi_rotary.jpg)

**Software (Perangkat Lunak)**

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk konfigurasi pengembangan proyek.
- **Langkah 2.** Download (unduh) kode pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Langkah 3.** Jalankan perintah di bawah ini.


```python
cd ~/GrovePi/Software/Python
python grove_rotary_angle_sensor.py
```

Di bawah ini kode grove_rotary_angle_sensor.py.

```python
import time
import grovepi

# Connect the Grove Rotary Angle Sensor to analog port A0
# SIG,NC,VCC,GND
potentiometer = 0

# Connect the LED to digital port D5
# SIG,NC,VCC,GND
led = 5

grovepi.pinMode(potentiometer,"INPUT")
grovepi.pinMode(led,"OUTPUT")
time.sleep(1)

# Reference voltage of ADC is 5v
adc_ref = 5

# Vcc of the grove interface is normally 5v
grove_vcc = 5

# Full value of the rotary angle is 300 degrees, as per it's specs (0 to 300)
full_angle = 300

while True:
    try:
        # Read sensor value from potentiometer
        sensor_value = grovepi.analogRead(potentiometer)

        # Calculate voltage
        voltage = round((float)(sensor_value) * adc_ref / 1023, 2)

        # Calculate rotation in degrees (0 to 300)
        degrees = round((voltage * full_angle) / grove_vcc, 2)

        # Calculate LED brightess (0 to 255) from degrees (0 to 300)
        brightness = int(degrees / full_angle * 255)

        # Give PWM output to LED
        grovepi.analogWrite(led,brightness)

        print("sensor_value = %d voltage = %.2f degrees = %.1f brightness = %d" %(sensor_value, voltage, degrees, brightness))
    except KeyboardInterrupt:
        grovepi.analogWrite(led,0)
        break
    except IOError:
        print ("Error")

```

- **Langkah 4.** Sesuaikan Grove-Rotary Angle Sensor dan kita akan melihat Grove-LED mengubah kecerahan nyala.



### Bermain dengan TI LaunchPad

**Membaca Potensiometer (Rotary Angle Sensor)**

Contoh ini menunjukkan cara membaca output analog yang berasal dari modul potensiometer Grove. Kami akan menggabungkan beberapa modul Grove dalam contoh ini! Dengan memutar kenop potensiometer, kami akan menampilkan nilai pembacaan analog pada tampilan Grove-4 digital.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Rotary_Angle_Sensor/master/img/Angle_sensor.jpg)

```
/*
    Rotary Angle Sensor
    Demonstrates analog input by reading an analog sensor on J16 of the Grove Base BoosterPack. The speed of the red LED on the LaunchPad will change depending on the position of the potentiometer knob. This example will also display the analog reading value on the Grove 4-digital display.

    The circuit:
    * Potentiometer attached to pin 24 (J6 on Grove Base BoosterPack)
    * center pin of the potentiometer to the analog pin
    * one side pin (either one) to ground
    * the other side pin to VCC (3.3V)

    * Note: Because of unstable of the voltage, the value of the rotary angle sensor
            varies slightly from run to run even you don't touch it.  

    Created by Oliver Wang

    This example code is in the public domain.

    http://www.seeedstudio.com/wiki/GROVE_-_Starter_Kit_v1.1b#Grove_-_Rotary_Angle_Sensor
    */

#include "TM1637.h"

/* Macro Define */
#define CLK               39                  /* 4-digital display clock pin */
#define DIO               38                /* 4-digital display data pin */
#define ROTARY_ANGLE_P    24               /* pin of rotary angle sensor */

/* Global Variables */
TM1637 tm1637(CLK, DIO);                  /* 4-digital display object */
int analog_value = 0;                     /* variable to store the value coming from rotary angle sensor */

int8_t bits[4] = {0};                     /* array to store the single bits of the value */

/* the setup() method runs once, when the sketch starts */
void setup() {

    /* Initialize 4-digital display */
    tm1637.init();
    tm1637.set(BRIGHT_TYPICAL);

}

/* the loop() method runs over and over again */
void loop() {   

    analog_value = analogRead(ROTARY_ANGLE_P);      /* read the value from the sensor */
    memset(bits, 0, 4);                             /* reset array when we use it */
    for(int i = 3; i >= 0; i--) {
        /* get single bits of the analog value */
        bits[i] = analog_value % 10;
        analog_value = analog_value / 10;  
        tm1637.display(i, bits[i]);                 /* display by 4-digital display */
    }
    delay(100);
}
```


## Sumber - Sumber

-  **[Eagle&PDF]** [Grove-Rotary Angle Sensor v1.2 Schematic File](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/res/Grove%20-%20Rotary%20Angle%20Sensor%20v1.2.zip)
-  **[Eagle&PDF]** [Grove - Rotary Angle Sensor(P) v1.1 Schematic File](https://github.com/SeeedDocument/Grove-Rotary_Angle_Sensor/raw/master/res/Grove%20%20-%20Rotary%20Angle%20Sensor(P)%20v1.1.zip)
-  **[Library]** [Github repository for Rotary Angle Sensor](https://github.com/Seeed-Studio/Grove_Rotary_Angle_Sensor)
-  **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Rotary_Angle_Sensor/master/res/Grove_Rotary_Angle_Sensor_CDC_File.zip)

## Proyek

**Menggunakan Grove-Rotary Angle Sensor(P) untuk mengontrol Grove LED**: Proyek ini menggunakan Arduino/Genuino 101 untuk mengontrol tingkat kecerahan LED melalui Grove-Rotary Angle Sensor(P).

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/user50338573/using-grove-rotary-angle-sensor-p-to-control-grove-led-725e32/embed' width='350'></iframe>

**Modul Rotary Angle Grove**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/31RaX7JGv5s" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/xx7hMoFQohY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>