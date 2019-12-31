---
name: Grove - Light Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Light-Sensor-(P)-v1.1-p-2693.html
oldwikiname: Grove_-_Light_Sensor
prodimagename: cover.jpg
sku: 101020173
tags: io_3v3, io_5v, plat_duino, plat_wio, plat_pi, plat_bbg, plat_linkit
---


![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/cover.jpg)


Modul Grove - Light sensor yang mengintegrasikan foto-resistor (resistor yang bergantung pada cahaya) untuk mendeteksi intensitas cahaya. Resistansi foto-resistor berkurang ketika intensitas cahaya meningkat. Dua chip opAmp LM358 pada modul menghasilkan tegangan yang sesuai dengan intensitas cahaya (mis. berdasarkan nilai resistansi). Sinyal yang dihasilkan berupa sinyal analog dimana semakin terang cahayanya, semakin besar nilainya.

Modul ini dapat digunakan untuk membuat sakelar yang dikendalikan cahaya, seperti mematikan lampu di siang hari dan menyalakan lampu di malam hari.


!!!Perhatian
    Nilai sensor cahaya hanya mencerminkan perkiraan kecenderungan intensitas cahaya, TIDAK mewakili nilai Lumen yang asli.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Versi

| Versi Produk              | Perubahan                                                            | Tanggal Rilis |
|------------------------------|--------------------------------------------------------------------|---------------|
| Grove - Light sensor 1.0     | Pertama                                                            | Apr 28 2013   |
| Grove - Light sensor(P)      | Memindah konektor Grove ke sisi belakang                                  | May 15 2014   |
| Grove - Light sensor(P) V1.1 | Mengganti fotoresistor-5528 dengan LS06-S Vs.Grove - Light sensor(P)  | Dec 31 2015   |
| Grove - Light sensor 1.2     | Mengganti fotoresistor-5528 dengan LS06-S Vs.Grove - Light Sensor 1.0 | Jan 20 2016   |


## Fitur

* Output nilai analog
* Keandalan dan sensibilitas tinggi
* Rangkaian kecil
* Mengenali spektrum yang lebih luas

!!!Tip
    Rincian lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

### Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                        | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Spesifikasi

|Parameter|Nilai|
|-----|--------|
|Tegangan kerja |3~5V|
|Arus kerja|	0.5~3 mA|
|Response time|20-30 milidetik|
|Peak Wavelength|540 nm|
|Berat|4 g|


## Memulai

### Bermain dengan Arduino

#### Hardware (Perangkat Keras)

- Langkah 1. Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4 | Base Shield |Grove - Light Sensor | Grove - LED Bar |
|--------------|----------------------|-----------------|---------------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/light_sensor_s.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_3.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-LED-Bar-v2.0-p-2474.html)|

- Langkah 2. Hubungkan Grove-Light sensor ke port A0 dari Grove-Base Shield.
- Langkah 3. Hubungkan Grove-Led Bar ke port D2 dari Grove-Base Shield.
- Langkah 4. Pasang Grove - Base Shield ke Seeeduino.
- Langkah 5. Hubungkan Seeeduino ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/seeeduino_light.jpg)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Light sensor ke Seeeduino seperti di bawah ini.

| Seeeduino     | Grove-Light sensor     |
|---------------|-------------------------|
| 5V            | Merah                   |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| A0            | Kuning                  |


| Seeeduino     | Grove-Led Bar |
|---------------|-------------------------|
| 5V            | Merah                   |
| GND           | Hitam                   |
| D3            | Putih                   |
| D2            | Kuning                  |

#### Software (Perangkat Lunak)

- Langkah 1. Download (unduh)  [ Grove-LED Bar Library](https://github.com/Seeed-Studio/Grove_LED_Bar/archive/master.zip) dari Github.
- Langkah 2. Lihat [How to install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) untuk menginstal library dari Seeeduino.
- Langkah 3. Salin kode ke Seeeduino IDE dan upload (unggah).

```c

#include <Grove_LED_Bar.h>

Grove_LED_Bar bar(3, 2, 0);  // Clock pin, Data pin, Orientation

void setup()
{
  // nothing to initialize
  bar.begin();
  bar.setGreenToRed(true);
}

void loop()
{

  int value = analogRead(A0);
  value = map(value, 0, 800, 0, 10);

  bar.setLevel(value);
  delay(100);
}
```

- Langkah 2. Led bar akan berubah berdasarkan cahaya.

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan Grove-Light sensor ke port A0 dari Grove-Base Shield.

**Langkah 2.** Pasang modul Base Shield ke modul Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/img/cc_Light_Sensor.png)

Upload (unggah) program ke modul Arduino/Seeeduino.

!!!Sukses
    Ketika kode selesai di-upload (unggah), Anda akan melihat layar yang terang ditampilkan di Serial Monitor.

### Bermain dengan Raspberry Pi (menggunakan modul Grove Base Hat untuk Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Light Sensor|
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/light_sensor_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html)|



- **Langkah 2**. Pasang modul Grove Base Hat ke Raspberry.
- **Langkah 3**. Hubungkan modul light sensor ke port A0 dari modul Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry Pi ke PC menggunakan kabel USB.


![](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/Light_Hat.jpg)


!!! Catatan
    Untuk langkah 3 Anda dapat menghubungkan sensor cahaya ke **sembarang port Analog** tetapi pastikan Anda mengubah perintah dengan nomor port yang sesuai.


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengonfigurasi pengembangan proyek.
- **Langkah 2**. Download (unduh) file sumber dengan memperbanyak library grove.py. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_light_sensor_v1_2.py 0

```

Berikut kode grove_light_sensor_v1_2.py.

```python

import math
import sys
import time
from grove.adc import ADC


class GroveLightSensor:

    def __init__(self, channel):
        self.channel = channel
        self.adc = ADC()

    @property
    def light(self):
        value = self.adc.read(self.channel)
        return value

Grove = GroveLightSensor


def main():
    if len(sys.argv) < 2:
        print('Usage: {} adc_channel'.format(sys.argv[0]))
        sys.exit(1)

    sensor = GroveLightSensor(int(sys.argv[1]))

    print('Detecting light...')
    while True:
        print('Light value: {0}'.format(sensor.light))
        time.sleep(1)

if __name__ == '__main__':
    main()

```

!!!Sukses
    Jika semuanya berjalan dengan baik, Anda akan dapat melihat hasil berikut yang sesuai dengan cahaya di sekitarnya
    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_light_sensor_v1_2.py 0
Detecting light...
Light value: 600
Light value: 448
Light value: 267
Light value: 311
Light value: 102
Light value: 82
Light value: 63
Light value: 54
Light value: 49
Light value: 45
Light value: 545
^CTraceback (most recent call last):
  File "grove_light_sensor_v1_2.py", line 67, in <module>
    main()
  File "grove_light_sensor_v1_2.py", line 64, in main
    time.sleep(1)
KeyboardInterrupt

```


Anda dapat keluar dari program ini hanya dengan menekan ++ctrl+c++.

!!!Perhatian
        Anda mungkin telah memperhatikan bahwa untuk port analog, nomor pin silkscreen adalah sesuatu seperti **A1, A0**, namun dalam perintah kami menggunakan parameter **0** dan **1**, sama seperti port digital. Jadi pastikan Anda pasang modul ke port yang benar, agar tidak terjadi pin yang konflik.



### Bermain dengan Raspberry Pi (menggunakan GrovePi_Plus)

#### Hardware (Perangkat Keras)

- Langkah 1. Siapkan peralatan dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Light Sensor | Grove - Red LED |
|--------------|-------------|-----------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/light_sensor_s.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Light-Sensor-v1.2-p-2727.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)|

- Langkah 2. Pasang modul GrovePi_Plus ke Raspberry.
- Langkah 3. Hubungkan modul Grove-light sensor ke port A0 dari GrovePi_Plus.
- Langkah 4. Hubungkan modul Grove-Red Led ke port D4 dari GrovePi_Plus.
- Langkah 5. Hubungkan modul Raspberry ke PC menggunakan USB.

![](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/img/rasp_light.jpg)

#### Software (Perangkat Lunak)

- Langkah 1. Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk konfigurasi pengembangan proyek.
- Langkah 2. Download (unduh) kode pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- Langkah 3. Jalankan perintah dibawah ini.


```
cd ~/GrovePi/Software/Python
python grove_light_sensor.py
```

Dibawah ini kode grove_light_sensor.py.

```python
import time
import grovepi

# Connect the Grove Light Sensor to analog port A0
# SIG,NC,VCC,GND
light_sensor = 0

# Connect the LED to digital port D4
# SIG,NC,VCC,GND
led = 4

# Turn on LED once sensor exceeds threshold resistance
threshold = 10

grovepi.pinMode(light_sensor,"INPUT")
grovepi.pinMode(led,"OUTPUT")

while True:
    try:
        # Get sensor value
        sensor_value = grovepi.analogRead(light_sensor)

        # Calculate resistance of sensor in K
        resistance = (float)(1023 - sensor_value) * 10 / sensor_value

        if resistance > threshold:
            # Send HIGH to switch on LED
            grovepi.digitalWrite(led,1)
        else:
            # Send LOW to switch off LED
            grovepi.digitalWrite(led,0)

        print("sensor_value = %d resistance = %.2f" %(sensor_value,  resistance))
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- Langkah 4. Lampu led akan nyala jika sensor cahaya ditutupi.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_light_sensor.py
sensor_value = 754 resistance = 3.57
sensor_value = 754 resistance = 3.57
sensor_value = 752 resistance = 3.60
sensor_value = 752 resistance = 3.60
sensor_value = 752 resistance = 3.60
sensor_value = 313 resistance = 22.68
sensor_value = 155 resistance = 56.00
sensor_value = 753 resistance = 3.59
```


## Sumber - Sumber

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/res/Grove_Light_Sensor_CDC_File.zip)
- **[Eagle&PDF]** [Eagle File for Grove - Light Sensor V1.0](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/resources/Grove%20-%20Light%20Sensor.zip)
- **[Eagle&PDF]**  [Eagle File for Grove - Light Sensor(P) V1.0](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/resources/Grove%20-%20Light%20Sensor%28P%29.zip)
- **[Eagle&PDF]**  [Eagle File for Grove - Light Sensor(P) V1.1](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/resources/Grove%20-%20Light%20Sensor%28P%29%20v1.1.zip)
- **[Datasheet]** [LS06-MΦ5 Reference Information](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/res/LS06-M%CE%A65_datasheet.pdf)
- **[Datasheet]**  [LM358.PDF](https://github.com/SeeedDocument/Grove_Light_Sensor/raw/master/res/LM358.pdf)
- **[More Reading]** Secret Box

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/secret_box.png)

Disini kami akan menunjukkan proyek yang dapat dibuat dengan Grove - Light Sensor bernama Secret Box. Pertama, anda membutuhkan satu buah kotak, dapat berupa kotak kertas atau kotak kayu atau kotak sembarang. Masukkan sesuatu ke dalam kotak tersebut, karena kami menamakannya kotak rahasia, itu berarti kami tidak ingin ada orang yang membukanya, dan sebaliknya akan ada alarm untuk memberi tahu Anda.

Di sini kami menggunakan LinkIt ONE sebagai pengontrol, yang merupakan modul kompatibel dengan Arduino dan terdiri dari banyak fungsi. Dan Anda perlu hal-hal di bawah ini:

* [LinkIt ONE](http://www.seeedstudio.com/LinkIt-ONE-p-2017.html)
* Grove - Light Sensor
* Grove - Base Shield
* Kartu Sim

Sambungkan Grove - Light Sensor ke port A0 atau Base Shield, dan buka Arduino IDE, salin kode di bawah ini dan upload (unggah) contohnya ke LinkIt ONE. Kemudian seseorang membuka kotak itu, lampu akan mendeteksinya, dan mengirimi Anda SMS.

```c
// demo of Grove Starter kit for LinkIt ONE
// Secret box

#include <LGSM.h>

char num[20] = "13425171053";           // your number write here
char text[100] = "Warning: Your box had been opened!!";    // what do you want to send


const int pinLight = A0;                // light sensor connect to A0

bool isLightInBox()
{
    return (analogRead(pinLight)<50);   // when get data less than 50, means light sensor was in box
}

void setup()
{
    Serial.begin(115200);

    while(!isLightInBox());             // until put in box
    delay(2000);
}


void loop()
{
    if(!isLightInBox())                 // box is open
    {
        Serial.println("box had been opened");

        while(!LSMS.ready())
        {
            delay(1000);
        }

        Serial.println("SIM ready for work!");
        LSMS.beginSMS(num);
        LSMS.print(text);

        if(LSMS.endSMS())
        {
            Serial.println("SMS is sent");
        }
        else
        {
            Serial.println("SMS send fail");
        }

        while(!isLightInBox());             // until put in box
        delay(2000);
    }

    delay(10);
}
```

Selamat bersenang-senang.

## Proyek

**Grove - Pengantar dalam Light Sensor**:

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-in-a-light-sensor-a55efd/embed' width='350'></iframe>

**Lingkungan Sekitar Cube! Ketahui Media di Bawah Anda menggunakan Sigfox**: Sebuah kubus dengan semua sensor yang diperlukan, cocok untuk berbagai aplikasi seperti pertanian, pengawasan, dll.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/dhairya-parikh/the-environment-cube-know-the-land-beneath-you-using-sigfox-952f29/embed' width='350'></iframe>


**Modul Light sensor Grove**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZvFswNYY2mU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/GOROc2f5Xkg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>