---
name: Grove - Red LED
category: Display
bzurl: https://www.seeedstudio.com/Grove-Red-LED-p-1142.html
oldwikiname:  Grove - Red LED
prodimagename: Grove-LED_Photo.jpg
surveyurl: https://www.research.net/r/Grove_Red_LedLED
sku:  104030005
---

![](https://github.com/SeeedDocument/Raspi_wiki/raw/master/img/red_led.jpg)

Modul Grove - Red LED serupa dengan modul Grove - LED yang memiliki soket untuk LED. Selain itu, modul ini juga memiliki potensiometer yang telah terpasang pada board untuk mengelola kebutuhan daya pada LED. PCB pada modul ini memiliki lubang pemasangan (mounting) yang dapat dipasang pada permukaan prototipe yang diperlukan milik anda. Misalnya, dapat digunakan sebagai lampu indikator untuk menunjukkan adanya daya atau sinyal.


<p style=":center"><a href="https://www.seeedstudio.com/Grove-Red-LED-p-1142.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>



## Versi


| Versi Produk              | Perubahan                                                                                                                                                                                      | Tangal Rilis |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Grove-LED_v1.3 | Pertama                                                                                                                                                                                     | 15 Maret 2016      |

##  Fitur - Fitur

*   Memberikan indikasi dengan cahaya LED untuk proyek Anda.
*   Mendukung berbagai warna LED, LED dipasang ke dudukan (holder) LED daripada disolder pada papan (board).
*   Mendukung kontrol kecerahan dan rentang tegangan input yang lebih tinggi dengan melakukan penyesuaian potensiometer pada board

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.

##  Memulai


### Bermain dengan Arduino

#### Hardware

- Langkah 1. Siapkan komponen dibawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Red LED |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg)|
|[Get ONE Now](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Get ONE Now](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Get ONE Now](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)|

- Langkah 2. Hubungkan Grove-Red LED ke port D2 pada Grove-Base Shield.
- Langkah 3. Pasang Grove - Base Shield ke Seeeduino.
- Langkah 4. Hubungkan Seeeduino ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/seeedstudio_red_led.jpg)

!!!Catatan

    Jika tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Red_Led ke Seeeduino dengan konfigurasi seperti di bawah ini.

| Seeeduino       | Grove-Red Led |
|---------------|-------------------------|
| 5V           | Red                     |
| GND           | Black                   |
| Not Conencted | White                   |
| D2            | Yellow                  |

#### Software

- **Langkah 1**. Salin kode ke Arduino IDE dan unggah (upload).

```
void setup() {
  // inisialisasi digital pin 2  sebagai output.
  pinMode(2, OUTPUT);
}

// Fungsi loop() berjalan terus menerus selamanya
void loop() {
  digitalWrite(2, HIGH);   // Menyalakan LED (HIGH adalah Level Tegangan)
  delay(1000);             // Tunggu 1 detik
  digitalWrite(2, LOW);    // Mematikan LED dengan membuat tegangannya rendah (LOW)
  delay(1000);            // Tunggu 1 detik
}
```

- **Langkah 2**. Kita dapat melihat LED menyala dan padam.

### Bermain dengan Codecraft

#### Hardware

**Langkah 1.** Hubungkan Grove - Red LED ke port D2 pada Base Shield.

**Langkah 2.** Pasang Base Shield pada Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda melalui kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/),  tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    
Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Seret (drag) blok-blok yang ada seperti gambar dibawah ini atau buka file cdc yang dapat diunduh pada akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Red_LED/master/img/cc_LED.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses

    Ketika kode berhasil diunggah, anda dapat melihat lampu LED menyala berkedip.

### Bermain dengan Raspberry Pi (dengan Grove Base Hat untuk Raspberry Pi)

#### Hardware

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Red LED |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)|

- **Langkah 2**. Pasang Grove Base Hat pada Raspberry.
- **Langkah 3**. Hubungkan Red LED  ke port 12 pada Base Hat.
- **Langkah 4**. Hubungkan Raspberry Pi melalui kabel USB.
![](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/BaseHat_LED.jpg)
!!! Catatan

    Untuk langkah 3 anda dapat menghubungkan Red LED ke **Port GPIO manapun** tetapi pastikan anda telah mengganti perintah sesuai dengan nomor portnya.


#### Software

- **Langkah 1**. Ikuti [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Download (Unduh) file sumbernya dengan menduplikat library grove.py .

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah dibawah ini untuk menjalankan kode.

```
cd yourpath/grove.py/grove
python grove_led.py 12
```
Jika anda menghubungkan Red LED ke port yang berbeda pada Base Hat, bukan mengeksekusi **python grove_led.py 12**, tetapi anda sebaiknya menjalankan perintah berikut.
```
python grove_led.py portnumber
```

Berikut adalah kode grove_led.py .

```python

from grove.gpio import GPIO


class GroveLed(GPIO):
    def __init__(self, pin):
        super(GroveLed, self).__init__(pin, GPIO.OUT)

    def on(self):
        self.write(1)

    def off(self):
        self.write(0)


Grove = GroveLed


def main():
    import sys
    import time

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    led = GroveLed(int(sys.argv[1]))

    while True:
        led.on()
        time.sleep(1)
        led.off()
        time.sleep(1)


if __name__ == '__main__':
    main()


```
!!!Sukses

   Jika semuanya berjalan dengan baik, anda dapat melihat LED menyala dan padam.
     
!!!Perhatian

Untuk sebagian besar modul grove, Anda perlu menambahkan parameter nomor pin, seperti dalam contoh ini `python grove_led.py 12`, **12** adalah pin GPIO yang dipilih dan output dari pin 12 akan menyalakan led.


### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

#### Hardware 

- Langkah 1. Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Red Led |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/Red%20LED_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/s/Grove-Red-LED-p-1142.html)|

- Langkah 2. Pasang GrovePi_Plus ke Raspberry.
- Langkah 3. Hubungkan Grove-Red Led ke port D4 pada GrovePi_Plus.
- Langkah 4. Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/img/rasp_red_led.jpg)

#### Software

- **Langkah 1**. Ikuti [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Lakukan Git clone repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```
- **Langkah 3.** Jalankan perintah dibawah ini.

```
cd ~/GrovePi/Software/Python
python grove_led_blink.py
```

Berikut kode grove_led_blink.py .

```python

import time
from grovepi import *

# Hubungkan Grove LED ke port digital D4
led = 4

pinMode(led,"OUTPUT")
time.sleep(1)

print ("This example will blink a Grove LED connected to the GrovePi+ on the port labeled D4. If you're having trouble seeing the LED blink, be sure to check the LED connection and the port number. You may also try reversing the direction of the LED on the sensor.")
print (" ")
print ("Connect the LED to the port labele D4!" )

while True:
    try:
        #Kedipkan lampu LED
        digitalWrite(led,1)		# Mengirimkan sinyal HIGH untuk menyalakan LED
        print ("LED ON!")
        time.sleep(1)

        digitalWrite(led,0)		# Mengirimkan sinyal LOW untuk mematikan LED
        print ("LED OFF!")
        time.sleep(1)

    except KeyboardInterrupt:	# Matikan LED sebelum berhenti
        digitalWrite(led,0)
        break
    except IOError:				# Print "Eror" jika teradi eror pada komunikasi
        print ("Error")
        
```

- **Langkah 4**. Kita dapat melihat LED menyala dan mati.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_led_blink.py
This example will blink a Grove LED connected to the GrovePi+ on the port labeled D4.
If you're having trouble seeing the LED blink, be sure to check the LED connection and the port number.
You may also try reversing the direction of the LED on the sensor.

Connect the LED to the port labele D4!
LED ON!
LED OFF!
LED ON!
LED OFF!
```


##  Sumber - Sumber

* **[PDF]** [Grove-Red LED Schematic](https://github.com/SeeedDocument/Grove-Red_LED/raw/master/res/Grove-LED_v1.3.pdf)
* **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Red_LED/master/res/Grove_Red_LED_CDC_File.zip)

## Proyek - Proyek

**Using Grove Button To Control Grove LED**: Cara menghubungkan dan menggunakan Grove Button untuk mengontrol Grove LED socket kit.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/user50338573/using-grove-button-to-control-grove-led-96d00b/embed' width='350'></iframe>

**Tombol dan modul LED Grove**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/RCtsxwx4OaA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/78lVn_-oYaY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Tech Support / Bantuan

Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/).

 <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>