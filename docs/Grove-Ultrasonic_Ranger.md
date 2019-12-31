---
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html
oldwikiname: Grove - Ultrasonic Ranger
prodimagename: 350px-Ultrasonic_Ranger.jpg
surveyurl: https://www.research.net/r/Grove-Ultrasonic-Ranger
sku: 101020010
tags: io_3v3, io_5v, plat_duino, plat_pi
---
![](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic.jpg)

Modul Grove - Ultrasonic ranger ini adalah modul pengukuran jarak non-kontak yang bekerja pada frekuensi 40KHz. Saat kita menyediakan sinyal pemicu (trigger) pulsa dengan periode lebih dari 10uS melalui pin sinyal, Grove_Ultrasonic_Ranger akan mengeluarkan 8 siklus (cycles) pada tingkat frekuensi 40kHz dan mendeteksi gema. Lebar pulsa sinyal gema sebanding dengan jarak yang terukur. Berikut adalah rumusnya: Jarak = sinyal gema saat HIGH*Kecepatan suara (340 m/s)/2. Sinyal Trig dan echo pada Grove_Ultrasonic_Ranger hanya menggunakan 1 pin yaitu pin SIG .

!!!Peringatan

    Jangan memasang modul Grove-Ultrasonic-Ranger saat peralatan kontrolnya sedang menyala, jika tidak maka akan dapat merusak sensor. Area yang diukur tidak boleh kurang dari 0,5 meter persegi dengan permukaan yang halus.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Versi

| Versi Produk              | Perubahan                                                                                                                                                                                    | Tangal Rilis |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Grove-Ultrasonic ranger V1.0 | Pertama                                                                                                                                                                                     | Maret 2012      |
| Grove-Ultrasonic ranger V2.0 | Meningkatkan stabilitas daya dengan board utama bertegangan rendah dengan perubahan di bawah ini: 1. Menambahkan kapasitansi C14 2. Mendesain ulang tata letak (layout) agar lebih rapih 3. Cocok dengan sistem yang memiliki tegangan 3.3V | Juli 2017     |

## Spesifikasi

|Parameter|	Value/Range|
|:------|:------------------|
|Operating voltage|	3.2~5.2V|
|Operating current|	8mA|
|Ultrasonic frequency|	40kHz|
|Measuring range|	2-350cm|
|Resolution|	1cm|
|Output|PWM|
|Size|50mm X 25mm X 16mm|
|Weight|13g|
|Measurement angle|15 degree|
|Working temperature|-10~60 degree C|
|Trigger signal|10uS TTL|
|Echo signal|TTL|


!!!Tips

Selengkapnya tentang modul Grove bisa dilihat di [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai
!!!Catatan

Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.

### Bermain dengan Arduino

#### Hardware

- **Langkah 1.** Siapkan komponen dibawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Ultrasonic Ranger |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic_small.jpg)|
|[Get One Now](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Get One Now](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Get One Now](https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html)|

- **Langkah 2.** Hubungkan Ultrasonic Ranger ke port D7 pada Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/arduino%20connection.jpg)

!!!Catatan

    Jika tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove_Ultrasonic_Ranger ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove-Ultrasonic Ranger |
|---------------|-------------------------|
| 5V           | Red                     |
| GND           | Black                   |
| Not Conencted | White                   |
| D7            | Yellow                  |

#### Software

- **Langkah 1.** Download (Unduh) [ UltrasonicRanger Library](https://github.com/Seeed-Studio/Grove_Ultrasonic_Ranger/archive/master.zip)  dari Github.
- **Langkah 2.** Mengacu pada [How to install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) untuk menginstall library untuk Arduino.
- **Langkah 3.** Salin kode ke Arduino IDE dan upload (Unggah). Jika anda tidak mengetahui cara unggah kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

```
#include "Ultrasonic.h"

Ultrasonic ultrasonic(7);
void setup()
{
	Serial.begin(9600);
}
void loop()
{
	long RangeInInches;
	long RangeInCentimeters;

	Serial.println("The distance to obstacles in front is: ");
	RangeInInches = ultrasonic.MeasureInInches();
	Serial.print(RangeInInches);//0~157 inches
	Serial.println(" inch");
	delay(250);

	RangeInCentimeters = ultrasonic.MeasureInCentimeters(); // dua pengukuran pasti memiliki interval waktu
	Serial.print(RangeInCentimeters);//0~400cm
	Serial.println(" cm");
	delay(250);
}
```

- **Langkah 4.** Kita akan dapat melihat tampilan jarak pada terminal seperti dibawah ini.

```
The distance to obstacles in front is:
2 inches
6 cm
The distance to obstacles in front is:
2 inches
6 cm
The distance to obstacles in front is:
2 inches
6 cm
```

### Bermain dengan Codecraft

#### Hardware

**Langkah 1.** Hubungkan Grove - Ultrasonic Ranger ke port D7 pada Base Shield.

**Langkah 2.** Pasang Grove - Base Shield ke Seeeduino/Arduino anda.

**Langkah 3.** Sambungkan Seeeduino/Arduino ke PC anda melalui kabel USB.

#### Software

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/),  tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Seret (drag) blok-blok yang ada seperti gambar dibawah ini atau buka file cdc yang dapat diunduh pada akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Ultrasonic_Ranger/master/img/cc_Ultrasonic_Ranger.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode berhasil diunggah, anda dapat melihat nilai jarak yang ditampilkan dalam Serial Monitor.

### Bermain dengan Raspberry Pi (Dengan Grove Base Hat untuk Raspberry Pi)

#### Hardware

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Ultrasonic Ranger |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic_small.jpg)|
|[Get ONE Now](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Get ONE Now](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Get ONE Now](https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html)|



- **Langkah 2**. Pasang Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan Grove - Ultrasonic Ranger ke port D5 pada Base Hat.
- **Langkah 4**. Hubungkan Raspberry ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/connect2.jpg)

!!! Catatan
    Untuk Langkah ke 3 anda dapat menghubungkan modul ultrasonic ranger ke **Port GPIO manapun** tetapi pastikan anda telah mengganti perintah sesuai dengan nomor portnya.


#### Software

- **Langkah 1**. Ikuti [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Download (Unduh) file sumbernya dengan menduplikat library grove.py .

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah dibawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_ultrasonic_ranger.py 5 6

```

Berikut adalah kode grove_ultrasonic_ranger.py.

```python

import sys
import time
from grove.gpio import GPIO

usleep = lambda x: time.sleep(x / 1000000.0)

_TIMEOUT1 = 1000
_TIMEOUT2 = 10000

class GroveUltrasonicRanger(object):
    def __init__(self, pin):
        self.dio =GPIO(pin)

    def _get_distance(self):
        self.dio.dir(GPIO.OUT)
        self.dio.write(0)
        usleep(2)
        self.dio.write(1)
        usleep(10)
        self.dio.write(0)

        self.dio.dir(GPIO.IN)

        t0 = time.time()
        count = 0
        while count < _TIMEOUT1:
            if self.dio.read():
                break
            count += 1
        if count >= _TIMEOUT1:
            return None

        t1 = time.time()
        count = 0
        while count < _TIMEOUT2:
            if not self.dio.read():
                break
            count += 1
        if count >= _TIMEOUT2:
            return None

        t2 = time.time()

        dt = int((t1 - t0) * 1000000)
        if dt > 530:
            return None

        distance = ((t2 - t1) * 1000000 / 29 / 2)    # cm

        return distance

    def get_distance(self):
        while True:
            dist = self._get_distance()
            if dist:
                return dist


Grove = GroveUltrasonicRanger


def main():
    if len(sys.argv) < 2:
        print('Usage: {} pin_number'.format(sys.argv[0]))
        sys.exit(1)

    sonar = GroveUltrasonicRanger(int(sys.argv[1]))

    print('Detecting distance...')
    while True:
        print('{} cm'.format(sonar.get_distance()))
        time.sleep(1)

if __name__ == '__main__':
    main()



```

!!!sukses
    
    Jika semuanya berjalan dengan baik, anda akan dapat melihat hasil seperti berikut
    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_ultrasonic_ranger.py 5 6
Detecting distance...
121.757901948 cm
246.894770655 cm
2.60205104433 cm
0.205533257846 cm
0.657706425108 cm
247.433267791 cm
122.485489681 cm
^CTraceback (most recent call last):
  File "grove_ultrasonic_ranger.py", line 110, in <module>
    main()
  File "grove_ultrasonic_ranger.py", line 107, in main
    time.sleep(1)
KeyboardInterrupt


```


Anda dapat keluar dari program ini hanya dengan menekan **ctrl+c** .




### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

#### Hardware

- **Langkah 1.** Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Ultrasonic Ranger |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Ultrasonic_small.jpg)|
|[Get One Now](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Get One Now](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Get One Now](https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html)|


- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove-Ultrasonic ranger ke port **D4** pada GrovePi_Plus.
- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/pi%20connection.jpg)

#### Software

- **Langkah 1.** Ikuti [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2.** Lakukan Git clone repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Langkah 3.** Jalankan perintah dibawah ini agar dapat menggunakan ultrasonic_ranger untuk mengukur jarak.


```
cd ~/GrovePi/Software/Python
python grove_ultrasonic.py
```

Berikut adalah kode grove_ultrasonic.py .

```python
# GrovePi + Grove Ultrasonic Ranger

from grovepi import *

# Hubungkan Grove Ultrasonic Ranger ke port digital D4
# SIG,NC,VCC,GND

ultrasonic_ranger = 4

while True:
    try:
        # Membaca nilai jarak dari Ultrasonic
        print ultrasonicRead(ultrasonic_ranger)

    except TypeError:
        print "Error"
    except IOError:
        print "Error"
```

- **Langkah 4.** Kita akan melihat tampilan jarak pada terminal seperti dibawah ini. 

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_ultrasonic.py
9
9
9
9
9
9
9
9
9
9
9

```

## Pertanyaan yang sering ditanyakan


**Q1: Bagaimana cara kerja sensor Grove-Ultrasonic?**

- A1: Saat kita menyediakan sinyal pemicu (trigger) pulsa dengan periode lebih dari 10uS melalui pin sinyal, Grove_Ultrasonic_Ranger akan mengeluarkan 8 siklus (cycles) pada tingkat frekuensi 40kHz dan mendeteksi gema. Lebar pulsa sinyal gema sebanding dengan jarak yang diukur. Berikut adalah rumusnya: Jarak = sinyal gema saat HIGH*Kecepatan suara (340 m/s)/2.


**Q2: Mengapa Grove-Ultrasonic sensor hanya memiliki 1 pin sinyal, dibandingkan dengan sensor ultrasonik lainnya yang memiliki Trig dan Echo pin?**

- A2:Sinyal Trig dan echo pada Grove_Ultrasonic_Ranger saling berbagi 1 pin SIG melalui MCU.  

**Q3: Di mana saya dapat menemukan dukungan teknis (technical support) jika saya memiliki masalah lain?**

- A3: Silahkan kirimkan masalah anda melalui email ke techsupport@seeed.cc

**Q4: Bisakah kita menghubungkan beberapa ultrasonik ke satu Arduino?**

- A4: Ya, Berikut contohnya, Satu sensor dihubungkan ke D2 dan lainnya ke D3. 

```c++
#include "Ultrasonic.h"

Ultrasonic ultrasonic1(2);
Ultrasonic ultrasonic2(3);
void setup()
{
    Serial.begin(9600);
}
void loop()
{
    long RangeInCentimeters1;
    long RangeInCentimeters2;

    RangeInCentimeters1 = ultrasonic1.MeasureInCentimeters(); //Dua pengukuran pasti memiliki interval waktu
    Serial.print(RangeInCentimeters1);//0~400cm
    Serial.println(" cm");
    
    RangeInCentimeters2 = ultrasonic2.MeasureInCentimeters(); // Dua pengukuran pasti memiliki interval waktu
    Serial.print(RangeInCentimeters2);//0~400cm
    Serial.println(" cm");
    
    delay(250);
}

```

## Sumber - Sumber

- **[PDF]** [Download (Unduh) Wiki PDF](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Grove-Ultrasonic_Ranger_WiKi.pdf)
- **[PDF]** [Skematik Grove_Ultrasonic Ranger](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Grove_Ultrasonic%20Ranger%20Schematic.pdf)
- **[PDF]** [Ceramic Ultrasonic Sensor NU40C16T/R-1](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/blob/master/res/NU40C16T-R-1.pdf)
- **[Library]** [Library (Pustaka) Grove_Ultrasonic Ranger](https://github.com/Seeed-Studio/Grove_Ultrasonic_Ranger/archive/master.zip)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Ultrasonic_Ranger/master/res/Grove_Ultrasonic_Ranger_CDC_File.zip)
- **[Proyek]** [Helix Berwarna](https://community.seeedstudio.com/project_detail.html?id=138)
- **[Proyek]** [Awan Petir Dalam Ruangan](https://community.seeedstudio.com/project_detail.html?id=182)
- **[Proyek]** [Pengontrol ketinggian air otomatis](https://community.seeedstudio.com/project_detail.html?id=241)
- **[Contoh]** [Contoh pengukuran jarak dan tampilan LED](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Example_Measure_distance_and_led_display.zip)
- **[Contoh]** [Contoh pengukuran dan tampilan jarak](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/res/Example_Measure_and_display_the_distance.zip)

## Proyek

**Hacking the Stairs at Seeed's New Office**: Mengubah tangga di kantor menjadi instalasi interaktif, dan bahkan ini adalah cara yang keren untuk menyampaikan pesan "STAFF ONLY" kepada pengunjung.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/stairs-hackers/hacking-the-stairs-at-seeed-s-new-office-9ef30b/embed' width='350'></iframe>



## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>