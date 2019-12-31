---
name: Grove - RTC
category: Sensor
bzurl: https://seeedstudio.com/Grove-RTC-p-758.html
oldwikiname: Grove_-_RTC
prodimagename: Grove-RTC.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020013 1.jpg
surveyurl: https://www.research.net/r/Grove-RTC
sku: 101020013
tags: grove_i2c, io_3v3, io_5v, plat_duino, plat_pi
---

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/45d.jpg)

Modul RTC didasarkan pada chip clock DS1307, yang mendukung protokol I2C. MOdul ini dilengkapi dengan baterai sel Lithium (CR1225). Jam / kalender yang terdapat pada modul ini menyediakan hitungan detik, menit, jam, hari, tanggal, bulan, dan tahun. Tanggal akhir bulan secara otomatis disesuaikan untuk bulan-bulan dengan kurang dari 31 hari, termasuk koreksi untuk tahun kabisat. Jam beroperasi dalam format 24 jam atau 12 jam dengan indikator AM / PM. Dan ini berlaku hingga 2100. Untuk mendapatkan kinerja yang kuat, Anda harus memasukkan sel lithium CR1225 3-Volt ke dalam dudukan baterai. Jika Anda hanya menggunakan daya primer, modul tidak berfungsi secara normal, karena kristal tidak berosilasi.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-RTC-p-758.html)

<div class="admonition note">
<p class="admonition-title">Catatan</p>
Tidak termasuk baterai.
</div>

## Spesifikasi

-   Ukuran PCB: 2.0cm\*4.0cm
-   Interface: 2.0mm pitch pin header
-   Struktur IO: SCL,SDA,VCC,GND
-   ROHS: YES
-   VCC：3.3~5.5V
-   Logic High Level Input ：2.2~VCC+0.3 V
-   Logic Low Level Input ：-0.3~+0.8 V
-   Tegangan baterai：2.0~3.5 V

!!!Tip
    Lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Platforms yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai


### Bermain dengan Arduino

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield| Grove-RTC |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-RTC-p-758.html)|

- **Langkah 2.** Hubungkan modul Grove-RTC ke port **I2C** dari Grove-Base Shield.
- **Langkah 3.** Pasangkan Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC menggunakan kabel USB.


<div class="admonition note">
<p class="admonition-title">Catatan</p>
 Untuk mendapatkan kinerja yang kuat, Anda harus memasukkan sel lithium CR1225 3-Volt ke dalam dudukan baterai. Jika Anda hanya menggunakan daya primer, modul mungkin tidak berfungsi secara normal, karena kristal tidak mungkin berosilasi.
</div>

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/arduino_connection.jpg)

!!!Catatan
    Jika kita tidak memiliki Grove Base Shield, kita juga dapat langsung menghubungkan Grove-RTC ke modul Arduino. Silakan ikuti koneksi di bawah ini.

| Seeeduino_v4 | Grove-RTC  |
|-------------|--------------------------|
| 5V          | VCC                      |
| GND         | GND                      |
| SDA         | SDA                      |
| SCL         | SCL                      |



#### Software (Perangkat Lunak)
**Langkah 1.** Download (unduh) [RTC Library](https://github.com/Seeed-Studio/RTC_DS1307/archive/master.zip).

**Langkah 2.** Lihat [How to install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) untuk menginstal library Arduino.


**Langkah 3.** Buat sketsa Arduino baru dan tempel kode di bawah ini atau buka kode secara langsung oleh path: **File -> Example ->RTC->SetTimeAndDisplay**.

  ![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/library%20example.jpg)


```c++     
#include <Wire.h>
#include "DS1307.h"

DS1307 clock;//define a object of DS1307 class
void setup()
{
    Serial.begin(9600);
    clock.begin();
    clock.fillByYMD(2013,1,19);//Jan 19,2013
    clock.fillByHMS(15,28,30);//15:28 30"
    clock.fillDayOfWeek(SAT);//Saturday
    clock.setTime();//write time to the RTC chip
}
void loop()
{
    printTime();
}
    /*Function: Display time on the serial monitor*/
void printTime()
{
    clock.getTime();
    Serial.print(clock.hour, DEC);
    Serial.print(":");
    Serial.print(clock.minute, DEC);
    Serial.print(":");
    Serial.print(clock.second, DEC);
    Serial.print("  ");
    Serial.print(clock.month, DEC);
    Serial.print("/");
    Serial.print(clock.dayOfMonth, DEC);
    Serial.print("/");
    Serial.print(clock.year+2000, DEC);
    Serial.print(" ");
    Serial.print(clock.dayOfMonth);
    Serial.print("*");
    switch (clock.dayOfWeek)// Friendly printout the weekday
    {
        case MON:
        Serial.print("MON");
        break;
        case TUE:
        Serial.print("TUE");
        break;
        case WED:
        Serial.print("WED");
        break;
        case THU:
        Serial.print("THU");
        break;
        case FRI:
        Serial.print("FRI");
        break;
        case SAT:
        Serial.print("SAT");
        break;
        case SUN:
        Serial.print("SUN");
        break;
    }
    Serial.println(" ");
}
```

**Langkah 4.**  Atur waktu. Ubah fungsi ke tanggal/waktu saat ini. Harap perhatikan format tanggal/waktunya.

```c
clock.fillByYMD(2013,1,19);//Jan 19,2013
clock.fillByHMS(15,28,30);//15:28 30"
clock.fillDayOfWeek(SAT);//Saturday
```

**Langkah 5.** Upload (unggah) kode dan buka serial monitor untuk menerima data sensor
![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/arduino%20result.png)



### Bermain dengan Raspberry Pi

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan dibawah ini:


| Raspberry pi | GrovePi_Plus | Grove-RTC |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/45d_small.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-RTC-p-758.html)|



- **Langkah 2.** Pasangkan modul GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan modul Grove-RTC ke prot **I2C** dari GrovePi_Plus.
- **Langkah 4.** Hubungkan modul Raspberry ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/rasp_connection.jpg)

#### Software (Perangkat Lunak)


- **Langkah 1.** Ikuti langkah [Setting Perangkat Lunak](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk konfigurasi pengembangan proyek.
- **Langkah 2.** Download (unduh) kode pada repositori Github.

```bash
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-	**Langkah 3.** Jalankan perintah dibawah ini untuk menggunakan sensor


```bash
cd ~/GrovePi/Software/Python
python grove_i2c_rtc.py
```
Here is the code

```Python
#!/usr/bin/env python
#
# GrovePi Example for using the Grove I2C RTC (http://www.seeedstudio.com/wiki/Grove_-_RTC)
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

# Connect the Grove Real Time Clock to any I2C port eg. I2C-1
# Can be found at I2C address 0x68
# SCL,SDA,VCC,GND

while True:
    try:
        print(grovepi.rtc_getTime())
        time.sleep(.5)

    except IOError:
        print ("Error")
```

-	**Langkah 4.** Berikut hasilnya.

  ![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/rpi_display.jpg)

**Demo 2: Grove_rtc**

Anda juga dapat menggunakan demo ini untuk menunjukkan waktu umum. Buatlah grove_rtc.py dan salin kode di bawah ini.

```python
    '''
     * Grove-RTC.py
     * Demo for Raspberry Pi
     *
     * Copyright (c) 2014 seeed technology inc.
     * Website    : community.seeedstudio.com/
     * Author     : Lambor
     * Create Time: Nov 2014
     * Change Log :
     *
     * The MIT License (MIT)
     *
     * Permission is hereby granted, free of charge, to any person obtaining a copy
     * of this software and associated documentation files (the "Software"), to deal
     * in the Software without restriction, including without limitation the rights
     * to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
     * copies of the Software, and to permit persons to whom the Software is
     * furnished to do so, subject to the following conditions:
     *
     * The above copyright notice and this permission notice shall be included in
     * all copies or substantial portions of the Software.
     *
     * THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
     * IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
     * FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
     * AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
     * LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
     * OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
     * THE SOFTWARE.
     '''

    #!/usr/bin/python
import time
import smbus


    bus = smbus.SMBus(1)    # 0 = /dev/i2c-0 (port I2C0), 1 = /dev/i2c-1 (port I2C1)   

class DS1307():     
        def __init__(self):
            self.MON = 1
            self.TUE = 2
            self.WED = 3
            self.THU = 4
            self.FRI = 5
            self.SAT = 6
            self.SUN = 7
            self.DS1307_I2C_ADDRESS = 0x68

            print 'begin'

        def decToBcd(self, val):
            return ( (val/10*16) + (val%10) )

        def bcdToDec(self,  val):
            return ( (val/16*10) + (val%16) )

        def begin(self, news):
            print news

        def startClock(self):   
            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            self.second = bus.read_byte(self.DS1307_I2C_ADDRESS) & 0x7f
            bus.write_byte_data(self.DS1307_I2C_ADDRESS, 0x00, self.second)

            print 'startClock..'

        def stopClock(self):                        
            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            self.second = bus.read_byte(self.DS1307_I2C_ADDRESS) | 0x80
            bus.write_byte_data(self.DS1307_I2C_ADDRESS, 0x00, self.second)         

            print 'stopClock..'

        def setTime(self):
            data = [self.decToBcd(self.second), self.decToBcd(self.minute), \
                    self.decToBcd(self.hour), self.decToBcd(self.dayOfWeek), \
                    self.decToBcd(self.dayOfMonth), self.decToBcd(self.month), \
                    self.decToBcd(self.year)]

            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            bus.write_i2c_block_data(self.DS1307_I2C_ADDRESS,0x00,data)

            print 'setTime..'

        def getTime(self):
            bus.write_byte(self.DS1307_I2C_ADDRESS, 0x00)
            data = bus.read_i2c_block_data(self.DS1307_I2C_ADDRESS,0x00)
            #A few of these need masks because certain bits are control bits
            self.second = self.bcdToDec(data[0] & 0x7f)
            self.minute = self.bcdToDec(data[1])
            self.hour = self.bcdToDec(data[2] & 0x3f)  #Need to change this if 12 hour am/pm
            self.dayOfWeek = self.bcdToDec(data[3])
            self.dayOfMonth = self.bcdToDec(data[4])
            self.month = self.bcdToDec(data[5])
            self.year = self.bcdToDec(data[6])

            print 'getTime..'

        def fillByHMS(self, _hour,  _minute,  _second):
            self.hour = _hour
            self.minute = _minute
            self.second = _second

            print 'fillByHMS..'

        def fillByYMD(self, _year,  _month,  _day):     
            self.year = _year - 2000
            self.month = _month;
            self.dayOfMonth = _day

            print 'fillByYMD..'

        def fillDayOfWeek(self,  _dow):     
            self.dayOfWeek = _dow

            print 'fillDayOfWeek..'

    if __name__ == "__main__":
        clock = DS1307()
        clock.fillByYMD(2015,3,5)
        clock.fillByHMS(12,42,30)
        clock.fillDayOfWeek(clock.THU)  
        clock.setTime()
        while True:     
            clock.getTime()
            print clock.hour, ":", clock.minute, ":", \
                    clock.second, " ", clock.dayOfMonth, "/", \
                    clock.month, "/", clock.year,"  ", "weekday", \
                    ":", clock.dayOfWeek            
            time.sleep(1)
```

 Jalankan perintah dibawah ini

```bash
    sudo python grove_rtc.py
```

Hasilnya akan seperti dibawah ini.

![](https://github.com/SeeedDocument/Grove-RTC/raw/master/img/rpi_display2.jpg)


## Sumber - Sumber


- **[Eagle]** [Grove-RTC in Eagle format](https://raw.githubusercontent.com/SeeedDocument/Grove-RTC/master/res/Real_Time_Clock.zip)
- **[PDF]** [Grove-RTC Schematic in PDF format](https://github.com/SeeedDocument/Grove-RTC/raw/master/res/Grove%20-%20RTC%20v1.1%20Sch.pdf)
- **[PDF]** [Grove-RTC PCB in PDF format](https://github.com/SeeedDocument/Grove-RTC/raw/master/res/Grove%20-%20RTC%20v1.1%20PCB.pdf)
- **[Library]**[Github repository for RTC](https://github.com/Seeed-Studio/RTC_DS1307/archive/master.zip)
- **[Datasheet]** [DS1307 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-RTC/master/res/DS1307.pdf)

## Proyek

**Menggunakan Real Time Clock dengan Arduino**: Pernah ingin membuat proyek yang akan aktif sesuai dengan jadwal tertentu? Dengan menggunakan modul Real Time Clock (RTC) adalah cara yang tepat!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/robotgeek-projects-team/using-a-real-time-clock-with-arduino-6b3896/embed' width='350'></iframe>

**Colorful Clock**: Jam ini akan menunjukkan level energi dan memberi salam saat anda mendekat

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/zou-wei/colorful-clock-4cea6b/embed' width='350'></iframe>

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>