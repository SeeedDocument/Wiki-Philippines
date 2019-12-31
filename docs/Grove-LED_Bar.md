---
name: Grove - LED Bar
category: Display
bzurl: https://seeedstudio.com/Grove-LED-Bar-p-1178.html
oldwikiname: Grove_-_LED_Bar
prodimagename: Grove-LED_Bar-1.jpg
surveyurl: https://www.research.net/r/Grove-LED_Bar
sku: 104030002
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Bar/master/img/Grove-LED_Bar-1.jpg)

Grove - LED Bar terdiri dari 10 bar segment LED  dan chip pengendali LED MY9221. Modul ini dapat digunakan sebagai indikator untuk kapasitas baterai,tegangan, level air, volume musik atau nilai lainnya yang memerlukan tampilan gradien. Ada 10 bar LED dalam LED bar graph: satu merah, satu kuning, satu hijau muda, dan tujuh bar hijau. Kode demo tersedia untuk anda agar dapat membuat sistem ini dengan mudah dan cepat. Modul dapat menyalakan LED secara berurutan dari merah sampai ke hijau, sehingga seluruh LED bar graph menyala pada akhirnya. Ingin tahu lebih lanjut? Silakan buat kode Anda sendiri.

<p style=":center"><a href="https://www.seeedstudio.com/s/Grove-LED-Bar-v2.0-p-2474.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

Versi
--------

| Versi Produk              | Perubahan                                   | Tanggal Rilis |
|------------------------------|-------------------------------------------|---------------|
| Grove – LED Bar V1 | Pertama                                   | Juni 2014     |
| Grove – LED Bar V2 | Mengembangkan Supply Daya                                   | Oktober 2015     |

Fitur - Fitur
--------

-   Input Voltage: 3.3V/5V
-   Each LED segment can be controlled individually via code
-   Intuitive display
-   Flexible power option, supports 3-5.5DC
-   Available demo code
-   Suli-compatible Library

!!!Tips

Selengkapnya tentang modul Grove bisa dilihat di [Grove System](http://wiki.seeedstudio.com/Grove_System/)


## Spesifikasi

| Parameter                                                   | Value/Range  |
|-------------------------------------------------------------|--------------|
| Operating voltage                                           | 3.3/5V       |
| Operation Temperature                                       | -20℃ to +80℃ |
| Peak Emission Wavelength-RED(Current 20mA)                  | 630-637nm    |
| Peak Emission Wavelength-Yellow Green(Current  20mA )       | 570-573nm    |
| Peak Emission Wavelength-Yellow(Current  20mA )             | 585-592nm    |
| Luminous Intensity Per Segment-RED(Current  20mA )          | 50-70mcd     |
| Luminous Intensity Per Segment-Yellow Green(Current  20mA ) | 28-35mcd     |
| Luminous Intensity Per Segment-Yellow(Current  20mA )       | 45-60mcd     |
| LED segment                                                 | 10           |
| Size                                                        | 40mm * 20mm  |


Platform yang didukung
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.

Memulai
-------------

!!!Catatan
    Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.

### Bermain dengan Arduino

**Hardware**

- **Langkah 1.** Siapkan komponen dibawah ini:

| Seeeduino V4.2 | Base Shield|  Grove-LED Bar |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Bar/master/img/Grove-LED_Bar-3.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/s/Grove-LED-Bar-v2.0-p-2474.html)|

- **Langkah 2.** Hubungkan Grove-LED Bar ke port **D8** pada Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-LED_Bar/raw/master/img/seeeduino_ledbar.jpg)

!!!Catatan
    Jika tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-LED Bar ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove-LED Bar |
|---------------|-------------------------|
| 5V           | Red                     |
| GND           | Black                   |
| D9            | White                   |
| D8            | Yellow                  |

**Software**

- **Langkah 1.** Unduh (Download) [Grove - LED Bar Library](https://github.com/Seeed-Studio/Grove_LED_Bar) dari Github

- **Langkah 2.** Mengacu pada [How to install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) untuk menginstall library untuk Arduino.

- **Langkah 3.** Mulai Ulang (Restart) aplikasi Arduino IDE. Buka contoh “Level” melalui petunjuk berikut : **File --> Examples --> Grove LED Bar --> Level**.

![](https://github.com/SeeedDocument/Grove-LED_Bar/raw/master/img/code.png)

- **Langkah 4.** Unggah (Upload) demo. Jika anda tidak mengetahui cara unggah kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

Hasilnya akan seperti berikut:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Bar/master/img/LED_Bar_shining.gif)

### Bermain dengan Raspberry Pi

**Hardware**

- **Langkah 1.** Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove-LED Bar |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Bar/master/img/Grove-LED_Bar-3.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/s/Grove-LED-Bar-v2.0-p-2474.html)|

- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.

- **Langkah 3.** Hubungkan Grove-LED Bar ke port **D5** pada GrovePi_Plus.

- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-LED_Bar/raw/master/img/rpi_ledbar.jpg)

**Software**

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Eevelopment Environment).

- **Langkah 2.** Ikuti [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/) untuk memperbarui firmware versi terbaru pada GrovePi.


!!!Tips
    Dalam situs wiki ini kita menggunakan alamat (path) **~/GrovePi/** dibandingkan **/home/pi/Desktop/GrovePi**, anda harus memastikan Langkah 2 dan Langkah 3 menggunakan alamat yang sama.


!!!Catatan
    Kami  menyarankan Anda untuk memperbarui firmware, jika tidak untuk beberapa jenis sensor mungkin dapat terjadi masalah

- **Langkah 3.** Lakukan Git clone pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-**Step 4.** Arahkan ke direktori demo:

```
cd yourpath/GrovePi/Software/Python/
```
Berikut kode grove_ledbar.py .

```python
import time
import grovepi
import random

# Hubungkan Grove LED Bar ke port digital D5
# DI,DCKI,VCC,GND
ledbar = 5

grovepi.pinMode(ledbar,"OUTPUT")
time.sleep(1)
i = 0

# Metode LED Bar
# grovepi.ledBar_init(pin,orientation)
# grovepi.ledBar_orientation(pin,orientation)
# grovepi.ledBar_setLevel(pin,level)
# grovepi.ledBar_setLed(pin,led,state)
# grovepi.ledBar_toggleLed(pin,led)
# grovepi.ledBar_setBits(pin,state)
# grovepi.ledBar_getBits(pin)

    while True:
        try:
        print "Test 1) Initialise - red to green"
        # ledbar_init(pin,orientation)
        # orientation: (0 = red to green, 1 = green to red)
        grovepi.ledBar_init(ledbar, 0)
        time.sleep(.5)


        print "Test 2) Set level"
        # ledbar_setLevel(pin,level)
        # level: (0-10)
        for i in range(0,11):
            grovepi.ledBar_setLevel(ledbar, i)
            time.sleep(.2)
        time.sleep(.3)

        grovepi.ledBar_setLevel(ledbar, 8)
        time.sleep(.5)

        grovepi.ledBar_setLevel(ledbar, 2)
        time.sleep(.5)

        grovepi.ledBar_setLevel(ledbar, 5)
        time.sleep(.5)


        print "Test 3) Switch on/off a single LED"
        # ledbar_setLed(pin,led,state)
        # led: which led (1-10)
        # state: off or on (0,1)
        grovepi.ledBar_setLed(ledbar, 10, 1)
        time.sleep(.5)

        grovepi.ledBar_setLed(ledbar, 9, 1)
        time.sleep(.5)

        grovepi.ledBar_setLed(ledbar, 8, 1)
        time.sleep(.5)

        grovepi.ledBar_setLed(ledbar, 1, 0)
        time.sleep(.5)

        grovepi.ledBar_setLed(ledbar, 2, 0)
        time.sleep(.5)

        grovepi.ledBar_setLed(ledbar, 3, 0)
        time.sleep(.5)


        print "Test 4) Toggle a single LED"
        # Membalik logika led tunggal - jika sebelumnya menyala, maka led akan padam dan sebaliknya
        # ledbar_toggleLed(ledbar, led)
        grovepi.ledBar_toggleLed(ledbar, 1)
        time.sleep(.5)

        grovepi.ledBar_toggleLed(ledbar, 2)
        time.sleep(.5)

        grovepi.ledBar_toggleLed(ledbar, 9)
        time.sleep(.5)

        grovepi.ledBar_toggleLed(ledbar, 10)
        time.sleep(.5)


        print "Test 5) Set state - control all leds with 10 bits"
        # ledbar_setBits(ledbar, state)
        # state: (0-1023) or (0x00-0x3FF) or (0b0000000000-0b1111111111) or (int('0000000000',2)-int('1111111111',2))
        for i in range(0,32):
            grovepi.ledBar_setBits(ledbar, i)
            time.sleep(.2)
        time.sleep(.3)


        print "Test 6) Get current state"
        # state = ledbar_getBits(ledbar)
        # state: (0-1023) 1 bit untuk setiap 10 LED
        state = grovepi.ledBar_getBits(ledbar)
        print "with first 5 leds lit, the state should be 31 or 0x1F"
        print state

        # bitwise shift 5 bit ke kiri
        state = state << 5
        # nilai state saat ini harusnya 992 atau 0x3E0
        # Ketika menyimpan 5 LED terakhir akan menyala bukan 5 LED awal
        time.sleep(.5)


        print "Test 7) Set state - save the state we just modified"
        # ledbar_setBits(ledbar, state)
        # state: (0-1023) 1 bit untuk setiap 10 LED
        grovepi.ledBar_setBits(ledbar, state)
        time.sleep(.5)


        print "Test 8) Swap orientation - green to red - current state is preserved"
        # ledbar_orientation(pin,orientation)
        # orientation: (0 = red to green, 1 = green to red)
        # Ketika anda membalik orientasi led bar, semua metode tahu cara menangani indeks LED baru
        # Hijau ke Merah
        grovepi.ledBar_orientation(ledbar, 1)
        time.sleep(.5)

        # Merah ke Hijau
        grovepi.ledBar_orientation(ledbar, 0)
        time.sleep(.5)

        # Hijau ke Merah
        grovepi.ledBar_orientation(ledbar, 1)
        time.sleep(.5)


        print "Test 9) Set level, again"
        # ledbar_setLevel(pin,level)
        # level: (0-10)
        # catatan LED merah sekarang berada pada indeks 10 bukan 1
        for i in range(0,11):
            grovepi.ledBar_setLevel(ledbar, i)
            time.sleep(.2)
        time.sleep(.3)


        print "Test 10) Set a single LED, again"
        # ledbar_setLed(pin,led,state)
        # led: which led (1-10)
        # state: Mati atau menyala(0,1)
        grovepi.ledBar_setLed(ledbar, 1, 0)
        time.sleep(.5)

        grovepi.ledBar_setLed(ledbar, 3, 0)
        time.sleep(.5)

        grovepi.ledBar_setLed(ledbar, 5, 0)
        time.sleep(.5)


        print "Test 11) Toggle a single LED, again"
        # ledbar_toggleLed(ledbar, led)
        grovepi.ledBar_toggleLed(ledbar, 2)
        time.sleep(.5)

        grovepi.ledBar_toggleLed(ledbar, 4)
        time.sleep(.5)


        print "Test 12) Get state"
        # state = ledbar_getBits(ledbar)
        # state: (0-1023) 1 bit untuk setiap 10 LED
        state = grovepi.ledBar_getBits(ledbar)

        # 5 LED terakhir menyala, jadi nilai statenya haruslah 992 atau 0x3E0

        # bitwise shift 5 bit ke kanan
        state = state >> 5
        # state sekarang haruslah 31 atau 0x1F


        print "Test 13) Set state, again"
        # ledbar_setBits(ledbar, state)
        # state: (0-1023) 1 bit untuk setiap 10 LED
        grovepi.ledBar_setBits(ledbar, state)
        time.sleep(.5)


        print "Test 14) Step"
        # Melangkah melewati semua 10 LED
        for i in range(0,11):
            grovepi.ledBar_setLevel(ledbar, i)
            time.sleep(.2)
        time.sleep(.3)


        print "Test 15) Bounce"
        # Menyalakan 2 LED pertama
        grovepi.ledBar_setLevel(ledbar, 2)

        # Mengambil state saat ini (yaitu 0x3)
        state = grovepi.ledBar_getBits(ledbar)

        # Memantul ke kanan
        for i in range(0,9):
            # bitwise shift bit ke kiri kemudian memperbarui (update)
            state <<= 1;
            grovepi.ledBar_setBits(ledbar, state)
            time.sleep(.2)

        # Memantul ke kiri
        for i in range(0,9):
            # bitwise shift bit ke kanan dan kemudian (update)
            state >>= 1;
            grovepi.ledBar_setBits(ledbar, state)
            time.sleep(.2)
        time.sleep(.3)


        print "Test 16) Random"
        for i in range(0,21):
            state = random.randint(0,1023)
            grovepi.ledBar_setBits(ledbar, state)
            time.sleep(.2)
        time.sleep(.3)


        print "Test 17) Invert"
        # Nyalakan setiap LED kedua pada 341 atau 0x155
        state = 341
        for i in range(0,5):
            grovepi.ledBar_setBits(ledbar, state)
            time.sleep(.2)

            # bitwise XOR semua 10 LED yang menyala dengan state saat ini
            state = 0x3FF ^ state

            grovepi.ledBar_setBits(ledbar, state)
            time.sleep(.2)
        time.sleep(.3)


        print "Test 18) Walk through all possible combinations"
        for i in range(0,1024):
            grovepi.ledBar_setBits(ledbar, i)
            time.sleep(.1)
        time.sleep(.4)

    except KeyboardInterrupt:
        grovepi.ledBar_setBits(ledbar, 0)
        break
    except IOError:
        print "Error"
```

- **Langkah 5.** Jalankan demo.

```
sudo python grove_ledbar.py
```

Sumber-Sumber
---------

-   [**Eagle&PDF**][Grove - LED Bar Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Bar/master/res/Grove-LED_Bar_v1.0.zip)
-   [**Library**][Grove - LED Bar Library](https://github.com/Seeed-Studio/Grove_LED_Bar)
-   [**Library**][Suli-compatible Library](https://github.com/Seeed-Studio/LED_Bar_Suli)
-   [**Datasheet**][MY9221 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-LED_Bar/master/res/MY9221_DS_1.0.pdf)
-   [**More Reading**][Wooden Laser Gun](http://www.instructables.com/id/DIY-a-Wooden-Laser-Gun-As-a-Xmas-Present-for-Your-/)



## Proyek

**Grove LED Bar v2.0**: Calliope Mini dilengkapi dengan dua konektor Grove. Dalam proyek ini, waktunya mengeksplorasi, bagaimana berbicara dengan bagian-bagian Seeed Grove ini.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/luuc/grove-led-bar-v2-0-c4b74f/embed' width='350'></iframe>

**Grove LED Bar Controller with the Bean+**: Mempelajari dasar-dasar penggunaan komponen Grove yang populer dengan LightBlue Bean+ baru untuk memulai membangun proyek Anda sendiri!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/karel/grove-led-bar-controller-with-the-bean-c3b81e/embed' width='350'></iframe>


## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>