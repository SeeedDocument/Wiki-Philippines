---
name: Grove - Tilt Switch
category: Sensor
bzurl: https://seeedstudio.com/Grove-Tilt-Switch-p-771.html
oldwikiname: Grove_-_Tilt_Switch
prodimagename: Tilt1.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/gbtlt.jpg
surveyurl: https://www.research.net/r/Grove-Tilt_Switch
sku: 101020025
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_pi, plat_bbg
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Tilt1.jpg)

Grove-Tilt switch merupakan sebuah tombol yang digunakan sebagai input digital. Di dalam saklar tilt terdapat sepasang bola yang dapat terjadi koneksi dengan pin ketika case-nya tegak. Apabila case-nya miring maka bola tidak akan menyentuh pin sehingga tidak terjadi koneksi. Kabel ini terhubung ke jalur SIG sedangkan NC tidak digunakan pada Grove ini.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-Tilt-Switch-p-771.html)

Fitur
--------

-   Grove Inteface
-   Mudah digunakan
-   Modul Grove yang sederhana

!!!Tip
    Informasi lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)
    
Spesifikasi
--------------

<table border="1" cellspacing="0" width="80%">
<tr>
<th scope="col">
Deskripsi
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
Tegangan Kerja
</th>
<td>
3
</td>
<td>
5.0
</td>
<td>
5.25
</td>
<td>
V
</td>
</tr>
<tr align="center">
<th scope="row">
Connecting Angle
</th>
<td colspan="3">
10° ~170°
</td>
<td>
-
</td>
</tr>
<tr align="center">
<th scope="row">
Disconnect angle
</th>
<td colspan="3">
190° ~350°
</td>
<td>
-
</td>
</tr>
<tr align="center">
<th scope="row">
Electrical Life
</th>
<td colspan="3">
100,000
</td>
<td>
Cycle
</td>
</tr>
</table>

Platform yang didukung
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai

### Bermain dengan Arduino

Pin SIG dari Grove-Tilt Switch secara normal akan menghasilkan logika LOW. Sementara itu ketika Tilt Switch tegak, sepasang bola yang terdapat di dalam tilt switch akan bersentuhan dengan pin maka pin SIG akan berlogika HIGH.

Sketsa berikut menunjukkan aplikasi sederhana menggunakan Tilt Switch dan Grove - Button untuk mengontrol led.

-   Seperti ditunjukkan gambar berikut, Tilt Switch terhubung ke port digital 5 dari Grove - Base Shield dan Grove-Button ke port digital 7. LED terhubung ke port digital 1. Instalasi perangkat keras adalah sebagai berikut:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Digitalv1.0b.jpg)

-   Salin dan tempel kode dibawah ini pada halaman baru sketch Arduino

```
void setup()
{
    pinMode(1, OUTPUT);
    pinMode(5, INPUT);
    pinMode(7, INPUT);
}

void loop()
{
    if (digitalRead(5)==HIGH)
    {
        digitalWrite(1, HIGH);
        delay(100);
        digitalWrite(1, LOW);
    }

    if (digitalRead(7)==HIGH)
    {
        digitalWrite(1, HIGH);
        delay(200);
        digitalWrite(1, LOW);
    }
}
```

-   upload (unggah) kodenya.
-   Kemudian LED akan menyala ketika Anda menekan tombol atau mengaktifkan tilt-switch. Selamat mencoba!

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan Grove - Tilt Switch ke port D5, lalu hubungkan Grove - Button dan Grove - Red LED ke port D7 dan D2 dari Base Shield.

**Langkah 2.** Hubungkan Groove Base Shield ke Seeeduino / Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/cc_Tilt_Switch.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Berhasil
    Ketika kode selesai diupload (unggah), miringkan sakelar tilt atau tekan tombol, kemudian LED akan menyala.

### Bermain dengan Raspberry Pi (Dengan Grove Base Hat for Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Tilt Switch |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Tilt_Switch/raw/master/img/thumbnail.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Tilt-Switch-p-771.html)|

- **Langkah 2**. Pasangkan Grove Base Hat ke Raspberry.
- **Langkah 3**. Hubungkan tilt switch ke port 12 dari Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry ke PC menggunakan kabel USB.


![](https://github.com/SeeedDocument/Grove-Tilt_Switch/raw/master/img/Tilt_Hat.jpg)

!!! Catatan
    Untuk langkah 3, tilt switch dapat dihubungkan ke ** Port GPIO ** tetapi pastikan Anda mengubah perintah dengan nomor port yang sesuai.


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengonfigurasi the development environment.
- **Langkah 2**. Download (unduh) kode grove.py pada repositori Github. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_tilt_switch.py 12

```

Berikut ini adalah kode grove_tilt_switch.py.

```python

import time
from grove.gpio import GPIO


class GroveTiltSwitch(GPIO):
    def __init__(self, pin):
        super(GroveTiltSwitch, self).__init__(pin, GPIO.IN)
        self._on_trigger = None
        self._on_release = None

    @property
    def on_trigger(self):
        return self._on_trigger

    @on_trigger.setter
    def on_trigger(self, callback):
        if not callable(callback):
            return

        if self.on_event is None:
            self.on_event = self._handle_event

        self._on_trigger = callback

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

        if value:
            if callable(self._on_trigger):
                self._on_trigger()
        else:
            if callable(self._on_release):
                self._on_release()

Grove = GroveTiltSwitch


def main():
    import sys

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    swicth = GroveTiltSwitch(int(sys.argv[1]))

    def on_trigger():
        print('Triggered')
    def on_release():
        print("Released.")

    swicth.on_trigger = on_trigger
    swicth.on_release = on_release

    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!sukses
    Jika semuanya berjalan dengan baik, Anda akan dapat melihat hasil berikut ketika Anda menyentuh tilt switch.

```python

pi@raspberrypi:~/grove.py/grove $ python grove_tilt_switch.py 12
Triggered
Released.
Triggered
^CTraceback (most recent call last):
  File "grove_tilt_switch.py", line 106, in <module>
    main()
  File "grove_tilt_switch.py", line 102, in main
    time.sleep(1)
KeyboardInterrupt

```


Anda dapat keluar dari program ini hanya dengan menekan ++ctrl+c++.




### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)


### dengan Raspberry Pi

1.Anda harus memiliki Raspberry Pi dan Grovepi atau Grovepi +. 

2. Anda seharusnya sudah selesai mengkonfigurasi development environment, jika tidak ikuti [here](/GrovePi_Plus).

3.Koneksi

-   Hubungkan Tilt_Switch ke soket grovepi D3 dengan menggunakan kabel grove.

4.Arahkan ke direktori demo:
```
       cd yourpath/GrovePi/Software/Python/
```
-   Untuk melihat kodenya
```
    nano grovepi_tilt_switch.py   # "Ctrl+x" to exit #
```
```
    import time
    import grovepi

    # Connect the Grove Tilt Switch to digital port D3
    # SIG,NC,VCC,GND
    tilt_switch = 3

    grovepi.pinMode(tilt_switch,"INPUT")

    while True:
        try:
            print grovepi.digitalRead(tilt_switch)
            time.sleep(.5)

        except IOError:
            print "Error"
```

5.Jalankan demonya.

```
    sudo python grove_tilt_switch.py
```

6.Hasil: Letakkan sensor tegak di satu sisi, pin SIG akan berlogikan HIGH.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Grovepi_tilt_Switch_00.png)



Rujukan
---------

Sudut pengoperasian Grove-Tilt Switch seperti yang ditunjukkan di bawah ini:

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/img/Tilt_Switch_Operate.jpg)

<div class="admonition note">
<p class="admonition-title">Catatan</p>
Tanda J1 di Grove adalah terminal referensi.
</div>



Sumber-sumber
---------

-   [Grove - Tilt Switch v1.0 Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove-Tilt_Switch_v1.0_Source_File.zip)
-   [Grove - Tilt Switch v1.1 PDF File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove-Tilt_Switch_v1.1_PDF_File.pdf)
-   [Grove - Tilt Switch v1.1 Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove-Tilt_Switch_v1.1_Eagle_File.zip)
-   [SW200D Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/SW200D_datasheet.pdf)
-   [Codecraft CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Tilt_Switch/master/res/Grove_Tilt_Switch_CDC_File.zip)


<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Tilt_Switch -->

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>