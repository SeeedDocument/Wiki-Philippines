---
name: Grove - 4-Digit Display
category: Display
bzurl: https://seeedstudio.com/Grove-4-Digit-Display-p-1198.html
oldwikiname: Grove_-_4-Digit_Display
prodimagename: Grove-4_digit_display.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/4-Digital Display.jpg
surveyurl: https://www.research.net/r/Grove-4-Digit_Display
sku: 104030003
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_pi, plat_wio
---

[![](https://raw.githubusercontent.com/SeeedDocument/Grove-4-Digit_Display/master/img/Grove-4_digit_display.jpg)](http://www.seeedstudio.com/depot/grove-4digital-display-p-1198.html)

Modul Grove - 4-Digit Display adalah modul yang memiliki 12-pin. Dalam modul ini, kita memanfaatkan TM1637 untuk menurunkan jumlah pin yang dapat dikendalikan menjadi 2. Artinya, konten dan kecerahan dapat diatur TM1637  hanya melalui 2 pin digital Arduino atau Seeeduino. Untuk proyek yang membutuhkan tampilan alfanumerik, modul ini bisa menjadi pilihan yang tepat.

<p style=":center"><a href="https://www.seeedstudio.com/grove-4digital-display-p-1198.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>


## Versi

| Versi Produk             | Perubahan                                   | Tangal Rilis |
|------------------------------|-------------------------------------------|---------------|
|Grove - 4-Digit Display V1.0  | Pertama                                   | Mei 2012      |     

## Fitur

-   Tampilan 4 digit alpha-numeric berwarna merah
-   Grove kompatibel dengan (Antarmuka) interface (3.3V/5V)
-   8 tingkat kecerahan yang dapat diatur

!!!Tips
    Selengkapnya tentang modul Grove dapat mengacu ke [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi

<table border="1" cellspacing="0" width="80%">
<tr>
<th scope="col">
Item
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
Voltage
</th>
<td>
3.3
</td>
<td>
5.0
</td>
<td>
5.5
</td>
<td>
VDC
</td>
</tr>
<tr align="center">
<th scope="row">
Current
</th>
<td>
0.2
</td>
<td>
27
</td>
<td>
80
</td>
<td>
mA
</td>
</tr>
<tr align="center">
<th scope="row">
Dimensions
</th>
<td colspan="3">
42x24x14
</td>
<td>
mm
</td>
</tr>
<tr align="center">
<th scope="row">
Net Weight
</th>
<td colspan="3">
7±1
</td>
<td>
g
</td>
</tr>
</table>

## Ide Aplikasi

-   Tampilan Waktu
-   Stopwatch
-   Tampilan input sensor

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

**Hardware (Perangkat keras)**

- **Langkah 1.** Siapkan perangkat dibawah ini:

| Seeeduino V4.2 | Base Shield|  Grove-4-Digit Display |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/500px-Grove_-_4_digit_display_s.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/grove-4digital-display-p-1198.html)|

- **Langkah 2.** Hubungkan Grove-4-Digit Display ke port **D2** dari Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/seeeduino_digital_led.jpg)

!!!Catatan

    Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-4-Digit Display ke Seeeduino seperti di bawah ini. Kita juga dapat menghubungkan Grove-4-Digit Display ke port Grove digital lainnya.

| Seeeduino |  Grove-4-Digit Display |
|-----------|-----------------|
| 5V        | Red             |
| GND       | Black           |
| D3        | White (DIO)     |
| D2        | Yellow(CLK)     | 

!!!Peringatan

    Grove-4-Digit Display terdiri dari 4 pin, GND, VCC, DIO, CLK. Kita dapat menghubungkan DIO dan CLK ke pin digital manapun. karena kedua pin tersebut tidak menggunakan protokol I2C.

**Software (Perangkat Lunak)**

- **Langkah 1.** Download (Unduh) [Grove-4-Digit Display Library](https://github.com/Seeed-Studio/Grove_4Digital_Display/archive/master.zip) dan [TimerOne Library](https://code.google.com/p/arduino-timerone/downloads/detail?name=TimerOne-v9.zip&can=2&q=).
- **Langkah 2.** Mengacu pada [How to install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) untuk menginstall library untuk Arduino.
- **Langkah 3.** Ikuti instruksi dibawah ini untuk memilih kode yang akan diakses di Arduino IDE dan melakukan upload (Unggah). Jika anda tidak mengetahui cara unggah kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/). Ada 3 contoh seperti di bawah ini.
    - Clock Display
    - Number Flow
    - Stop Watch

![](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/arduino_example.jpg)

- **Langkah 4.** Kita akan dapat melihat Grove-4-Digit Display aktif menyala.

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan Grove - 4-Digit Display ke port D2 pada Base Shield

**Langkah 2.** Pasang Grove - Base Shield ke Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda melalui kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), Tambahkan dukungan Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    
Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Tarik blok seperti gambar dibawah atau buka file cdc yang mana dapat didownload (diunduh) pada akhir halaman ini.

![](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/4-Digit_Display.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses

    Ketika kode berhasil di unggah, anda dapat melihat angka tampil bergantian dari 0 ke 9.

### Bermain dengan Raspberry Pi (Dengan Grove Base Hat untuk Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Perangkat yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - 4 Digit Display |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/500px-Grove_-_4_digit_display_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/grove-4digital-display-p-1198.html)|

- **Langkah 2**. Pasang Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan 4-digit display ke port 12 pada Grove Base Hat.
- **Langkah 4**. Hubungkan Raspberry ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/Digit_Hat.jpg)


!!! Catatan
    Untuk Langkah ke 3 anda dapat menghubungkan modul ke **Port GPIO manapun** tetapi pastikan anda telah mengganti perintah sesuai dengan nomor portnya.


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Download (Unduh) file sumbernya dengan menduplikat library grove.py .

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Eksekusi perintah dibawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_4_digit_display.py 12 13

```

Berikut adalah kode grove_4_digit_display.py .

```python

import sys
import time
from grove.gpio import GPIO


charmap = {
    '0': 0x3f,
    '1': 0x06,
    '2': 0x5b,
    '3': 0x4f,
    '4': 0x66,
    '5': 0x6d,
    '6': 0x7d,
    '7': 0x07,
    '8': 0x7f,
    '9': 0x6f,
    'A': 0x77,
    'B': 0x7f,
    'b': 0x7C,
    'C': 0x39,
    'c': 0x58,
    'D': 0x3f,
    'd': 0x5E,
    'E': 0x79,
    'F': 0x71,
    'G': 0x7d,
    'H': 0x76,
    'h': 0x74,
    'I': 0x06,
    'J': 0x1f,
    'K': 0x76,
    'L': 0x38,
    'l': 0x06,
    'n': 0x54,
    'O': 0x3f,
    'o': 0x5c,
    'P': 0x73,
    'r': 0x50,
    'S': 0x6d,
    'U': 0x3e,
    'V': 0x3e,
    'Y': 0x66,
    'Z': 0x5b,
    '-': 0x40,
    '_': 0x08,
    ' ': 0x00
}

ADDR_AUTO = 0x40
ADDR_FIXED = 0x44
STARTADDR = 0xC0
BRIGHT_DARKEST = 0
BRIGHT_DEFAULT = 2
BRIGHT_HIGHEST = 7


class Grove4DigitDisplay(object):
    colon_index = 1

    def __init__(self, clk, dio, brightness=BRIGHT_DEFAULT):
        self.brightness = brightness

        self.clk = GPIO(clk, direction=GPIO.OUT)
        self.dio = GPIO(dio, direction=GPIO.OUT)
        self.data = [0] * 4
        self.show_colon = False

    def clear(self):
        self.show_colon = False
        self.data = [0] * 4
        self._show()

    def show(self, data):
        if type(data) is str:
            for i, c in enumerate(data):
                if c in charmap:
                    self.data[i] = charmap[c]
                else:
                    self.data[i] = 0
                if i == self.colon_index and self.show_colon:
                    self.data[i] |= 0x80
                if i == 3:
                    break
        elif type(data) is int:
            self.data = [0, 0, 0, charmap['0']]
            if data < 0:
                negative = True
                data = -data
            else:
                negative = False
            index = 3
            while data != 0:
                self.data[index] = charmap[str(data % 10)]
                index -= 1
                if index < 0:
                    break
                data = int(data / 10)

            if negative:
                if index >= 0:
                    self.data[index] = charmap['-']
                else:
                    self.data = charmap['_'] + [charmap['9']] * 3
        else:
            raise ValueError('Not support {}'.format(type(data)))
        self._show()

    def _show(self):
        with self:
            self._transfer(ADDR_AUTO)

        with self:
            self._transfer(STARTADDR)
            for i in range(4):
                self._transfer(self.data[i])

        with self:
            self._transfer(0x88 + self.brightness)

    def update(self, index, value):
        if index < 0 or index > 4:
            return

        if value in charmap:
            self.data[index] = charmap[value]
        else:
            self.data[index] = 0

        if index == self.colon_index and self.show_colon:
            self.data[index] |= 0x80

        with self:
            self._transfer(ADDR_FIXED)

        with self:
            self._transfer(STARTADDR | index)
            self._transfer(self.data[index])

        with self:
            self._transfer(0x88 + self.brightness)


    def set_brightness(self, brightness):
        if brightness > 7:
            brightness = 7

        self.brightness = brightness
        self._show()

    def set_colon(self, enable):
        self.show_colon = enable
        if self.show_colon:
            self.data[self.colon_index] |= 0x80
        else:
            self.data[self.colon_index] &= 0x7F
        self._show()

    def _transfer(self, data):
        for _ in range(8):
            self.clk.write(0)
            if data & 0x01:
                self.dio.write(1)
            else:
                self.dio.write(0)
            data >>= 1
            time.sleep(0.000001)
            self.clk.write(1)
            time.sleep(0.000001)

        self.clk.write(0)
        self.dio.write(1)
        self.clk.write(1)
        self.dio.dir(GPIO.IN)

        while self.dio.read():
            time.sleep(0.001)
            if self.dio.read():
                self.dio.dir(GPIO.OUT)
                self.dio.write(0)
                self.dio.dir(GPIO.IN)
        self.dio.dir(GPIO.OUT)

    def _start(self):
        self.clk.write(1)
        self.dio.write(1)
        self.dio.write(0)
        self.clk.write(0)

    def _stop(self):
        self.clk.write(0)
        self.dio.write(0)
        self.clk.write(1)
        self.dio.write(1)

    def __enter__(self):
        self._start()

    def __exit__(self, exc_type, exc_val, exc_tb):
        self._stop()


Grove = Grove4DigitDisplay


def main():
    if len(sys.argv) < 3:
        print('Usage: {} clk dio'.format(sys.argv[0]))
        sys.exit(1)

    display = Grove4DigitDisplay(int(sys.argv[1]), int(sys.argv[2]))

    count = 0
    while True:
        t = time.strftime("%H%M", time.localtime(time.time()))
        display.show(t)
        display.set_colon(count & 1)
        count += 1
        time.sleep(1)


if __name__ == '__main__':
    main()

```

!!!sukses
    Jika semuanya berjalan dengan baik, tampilan 4-digit display akan menunjukkan waktu saat ini.


Anda dapat keluar dari program ini hanya dengan menekan **ctrl+c** .


### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

**Hardware (Perangkat Keras)**

- **Langkah 1.** Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove-4-Digit Display |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/500px-Grove_-_4_digit_display_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/grove-4digital-display-p-1198.html)|


- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove - 4-digit display ke port **D5** pada GrovePi_Plus.
- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/image/rpi_digital_led.jpg)

**Software (Perangkat Lunak)**

- **Langkah 1.** Ikuti [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).

- **Langkah 2.** Lakukan Git clone repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Langkah 3.** Eksekusi perintah dibawah ini untuk dapat memantau intensitas suara.


```python
cd ~/GrovePi/Software/Python
python grove_4_digit_display.py
```

Berikut adalah kode grove_4_digit_display.py.

```python
# NOTE: 4x tampilan 7 segment merah dengan kolon dan 8 tingkat kecerahan, tetapi tanpa nilai desimal

import time
import grovepi

# Hubungkan Grove 4 Digit Display ke port digital D5
# CLK,DIO,VCC,GND
display = 5
grovepi.pinMode(display,"OUTPUT")

# Jika anda memiliki sensor analog, sambungkan ke A0 lalu anda dapat memantaunya seperti dibawah ini.
sensor = 0
grovepi.pinMode(sensor,"INPUT")

time.sleep(.5)

# 4 Digit Display methods
# grovepi.fourDigit_init(pin)
# grovepi.fourDigit_number(pin,value,leading_zero)
# grovepi.fourDigit_brightness(pin,brightness)
# grovepi.fourDigit_digit(pin,segment,value)
# grovepi.fourDigit_segment(pin,segment,leds)
# grovepi.fourDigit_score(pin,left,right)
# grovepi.fourDigit_monitor(pin,analog,duration)
# grovepi.fourDigit_on(pin)
# grovepi.fourDigit_off(pin)

while True:
    try:
        print ("Test 1) Initialise")
        grovepi.fourDigit_init(display)
        time.sleep(.5)

        print ("Test 2) Set brightness")
        for i in range(0,8):
            grovepi.fourDigit_brightness(display,i)
            time.sleep(.2)
        time.sleep(.3)

        # Atur ke tingkat kecerahan terendah
        grovepi.fourDigit_brightness(display,0)
        time.sleep(.5)

        print ("Test 3) Set number without leading zeros")
        leading_zero = 0
        grovepi.fourDigit_number(display,1,leading_zero)
        time.sleep(.5)
        grovepi.fourDigit_number(display,12,leading_zero)
        time.sleep(.5)
        grovepi.fourDigit_number(display,123,leading_zero)
        time.sleep(.5)
        grovepi.fourDigit_number(display,1234,leading_zero)
        time.sleep(.5)

        print ("Test 4) Set number with leading zeros")
        leading_zero = 1
        grovepi.fourDigit_number(display,5,leading_zero)
        time.sleep(.5)
        grovepi.fourDigit_number(display,56,leading_zero)
        time.sleep(.5)
        grovepi.fourDigit_number(display,567,leading_zero)
        time.sleep(.5)
        grovepi.fourDigit_number(display,5678,leading_zero)
        time.sleep(.5)

        print ("Test 5) Set individual digit")
        grovepi.fourDigit_digit(display,0,2)
        grovepi.fourDigit_digit(display,1,6)
        grovepi.fourDigit_digit(display,2,9)
        grovepi.fourDigit_digit(display,3,15) # 15 = F
        time.sleep(.5)

        print ("Test 6) Set individual segment")
        grovepi.fourDigit_segment(display,0,118) # 118 = H
        grovepi.fourDigit_segment(display,1,121) # 121 = E
        grovepi.fourDigit_segment(display,2,118) # 118 = H
        grovepi.fourDigit_segment(display,3,121) # 121 = E
        time.sleep(.5)

        grovepi.fourDigit_segment(display,0,57) # 57 = C
        grovepi.fourDigit_segment(display,1,63) # 63 = O
        grovepi.fourDigit_segment(display,2,63) # 63 = O
        grovepi.fourDigit_segment(display,3,56) # 56 = L
        time.sleep(.5)

        print ("Test 7) Set score")
        grovepi.fourDigit_score(display,0,0)
        time.sleep(.2)
        grovepi.fourDigit_score(display,1,0)
        time.sleep(.2)
        grovepi.fourDigit_score(display,1,1)
        time.sleep(.2)
        grovepi.fourDigit_score(display,1,2)
        time.sleep(.2)
        grovepi.fourDigit_score(display,1,3)
        time.sleep(.2)
        grovepi.fourDigit_score(display,1,4)
        time.sleep(.2)
        grovepi.fourDigit_score(display,1,5)
        time.sleep(.5)

        print ("Test 8) Set time")
        grovepi.fourDigit_score(display,12,59)
        time.sleep(.5)

        print ("Test 9) Monitor analog pin")
        seconds = 10
        grovepi.fourDigit_monitor(display,sensor,seconds)
        time.sleep(.5)

        print ("Test 10) Switch all on")
        grovepi.fourDigit_on(display)
        time.sleep(.5)

        print ("Test 11) Switch all off")
        grovepi.fourDigit_off(display)
        time.sleep(.5)

    except KeyboardInterrupt:
        grovepi.fourDigit_off(display)
        break
    except IOError:
        print ("Error")

```

- **Langkah 4.** Dapat kita lihat tampilan Grove-4-Digit Display seperti dibawah ini.

```python
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_4_digit_display.py 
Test 1) Initialise
Test 2) Set brightness
Test 3) Set number without leading zeros
Test 4) Set number with leading zeros
Test 5) Set individual digit
Test 6) Set individual segment
Test 7) Set score
Test 8) Set time
Test 9) Monitor analog pin
Test 10) Switch all on
Test 11) Switch all off
```


### Bermain dengan TI LaunchPad

Menampilkan angka (4-Digital-Display)

Contoh ini menunjukkan bagaimana menampilkan beberapa angka digital menggunakan Grove-4-Digital Display.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-4-Digit_Display/master/img/4_digital_display.jpg)

```
/*
 * TM1637.cpp
 * library untuk 4 digit display
 */
#include "TM1637.h"
#define CLK 39 // Pengenalan pin untuk TM1637 dan dapat diganti dengan port lainnya
#define DIO 38
TM1637 tm1637(CLK,DIO);
void setup()
{
    tm1637.init();
    tm1637.set(BRIGHT_TYPICAL);//BRIGHT_TYPICAL = 2,BRIGHT_DARKEST = 0,BRIGHTEST = 7;
}
void loop()
{
    int8_t NumTab[] = {0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15};//0~9,A,b,C,d,E,F
    int8_t ListDisp[4];
    unsigned char i = 0;
    unsigned char count = 0;
    delay(150);
    while(1)
    {
        i = count;
        count ++;
        if(count == sizeof(NumTab)) count = 0;
        for(unsigned char BitSelect = 0;BitSelect < 4;BitSelect ++)
        {
            ListDisp[BitSelect] = NumTab[i];
            i ++;
            if(i == sizeof(NumTab)) i = 0;
        }
        tm1637.display(0,ListDisp[0]);
        tm1637.display(1,ListDisp[1]);
        tm1637.display(2,ListDisp[2]);
        tm1637.display(3,ListDisp[3]);
        delay(300);
    }
}
```

## Sumber - Sumber

- **[Eagle&PDF]** [Grove-4-Digit Display V1.0 Schematic](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/resource/Grove%20-%204-Digit%20Display%20V1.0%20eagle%20files.zip)
- **[Library]** [4-Digit Display library](https://raw.githubusercontent.com/SeeedDocument/Grove-4-Digit_Display/master/res/DigitalTube.zip)
- **[Library]** [TimerOne library](https://code.google.com/p/arduino-timerone/downloads/detail?name=TimerOne-v9.zip&can=2&q=)
- **[Library]** [Four-Digit Display Suli Library](https://github.com/Seeed-Studio/Four_Digit_Display_Suli)
- **[Library]** [CodeCraft Code](https://github.com/SeeedDocument/Grove_4_Digit_Display/raw/master/resource/4-Digit%20Display.zip)
- **[Datasheet]** [TM1637 datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-4-Digit_Display/master/res/TM1637_datasheet.pdf)
- **[More Reading]** [The Wooden Laser Gun](http://www.instructables.com/id/DIY-a-Wooden-Laser-Gun-As-a-Xmas-Present-for-Your-/)

![](https://raw.githubusercontent.com/SeeedDocument/Seeeduino_Lotus/master/img/gun.jpg)

Terinspirasi dari OVERWATCH, Kita dapat membuat Mainan keren pistol laser kayu untuk bersenang-senang saat ini!

Pistol Laser Kayu dan Target Pistol semuanya berdasarkan pada board Arduino yang disebut Seeeduino Lotus. Pemancar laser pada Psitol Laser dikendalikan untuk memancarkan pulsa laser untuk "mengaktifkan" Target Gun. Dan ada 3 sensor cahaya pada Gun Target untuk mendeteksi pulsa laser. Sepertinya sangat sederhana bukan? Jika Anda tertarik dengan proyek kami, silahkan buat satu untuk anda sendiri atau anak Anda! Hal Ini layak untuk menghabiskan satu hari pengerjaan sebagai hadiah Natal.

## Proyek

**MSP430 Alarm Clock with Grove Modules**: Buat jam alarm Anda sendiri menggunakan LaunchPad MSP430F5529 dan Modul SeeedStudio Grove.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/carlosventura/alarm-clock-with-grove-modules-e4e9f1/embed' width='350'></iframe>

**Jam - Grove 4-digit Display menggunakan Photon**:　Jam pertama Anda dengan 4 komponen, berdasarkan Grove dan TM1637.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/clock-grove-4-digit-display-using-photon-7c4369/embed' width='350'></iframe>

## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>