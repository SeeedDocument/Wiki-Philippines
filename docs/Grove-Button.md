---
name: Grove - Button
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Button-p-766.html
oldwikiname: Grove - Button
prodimagename: Button.jpg
surveyurl: https://www.surveymonkey.com/r/grove-button
sku: 101020003
---

![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/Button.jpg)

Grove - Button adalah sebuah tombol yang ditekan sesaat. Groove ini berisi satu tombol "on / off" sesaat yang independen. "Sesaat" berarti tombol kembali dengan sendirinya setelah dilepaskan. Tombol mengeluarkan sinyal HIGH saat ditekan, dan LOW saat dilepaskan. Tanda Sig pada lapisan silk adalah singkatan dari sinyal sedangkan NC(Not used) berarti tidak digunakan sama sekali. Ada dua versi dari tombol ini yang tersedia seperti yang ditunjukkan pada gambar. Satu-satunya perbedaan adalah arah dari Grove socket.

[![](https://github.com/SeeedDocument/Grove_Button/raw/master/image/300px-Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-Button-p-766.html)

## Versi


| Versi Produk              | Perubahan                                                                                                                                                                                   | Tanggal Dirilis |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Grove-Button | Initial                                                                                                                                                                                    | Nov 25 2010      |

## Fitur

- Mudah digunakan tombol ON / OFF
- Menggunakan Kabel Grove 4-pin Standar

!!!Tips
    Detail lebih lanjut tentang modul Grove silakan mengacu ke [Sistem Grove](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi

| Parameter             | Nilai / Rentang  |
|-----------------------|----------------|
| Tegangan operasi     | 3.3 / 5V         |
| Electrical Life       | 200,000 cycles |
| Operation Force       | 100 ± 50gf     |
| Suhu Operasional | -25℃ to +70℃   |
| Ukuran                  | 20mmX20mm      |

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini, tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


##  Memulai


### Bermain dengan Arduino

#### Perangkat Keras
- Langkah 1. Siapkan perangkat di bawah ini :

| Seeeduino V4.2 | Base Shield|  Grove - Button |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Button/raw/master/img/button_s.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Button-p-766.html)|

- Langkah 2. Hubungkan Grove-Button ke port D2 dari Grove-Base Shield.
- Langkah 3. Pasang Grove - Base Shield ke Seeeduino.
- Langkah 4. Hubungkan Seeeduino ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/seeeduino_button.jpg)

!!!Catatan
Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-Button ke Seeeduino dengan konfigurasi seperti di bawah ini.

| Seeeduino       | Grove-Button |
|---------------|-------------------------|
| 5V           | Merah                     |
| GND           | Hitam                   |
| Tidak tersambung | Putih                   |
| D2            | Kuning                  |

#### Software

- Langkah 1. Salin kode ke Arduino IDE dan lakukan upload unggah.

```c
const int buttonPin = 2;     // Nomor pin tombol
const int ledPin =  13;      // Nomor pin LED

// variabel dapat berubah:
int buttonState = 0;         // variabel untuk membaca status tombol

void setup() {
    // inisialisasi pin LED sebagai output:
    pinMode(ledPin, OUTPUT);
    // inisialisasi pin tombol sebagai input:
    pinMode(buttonPin, INPUT);
}

void loop(){
    // baca keadaan nilai tombol:
    buttonState = digitalRead(buttonPin);

    // periksa apakah tombol ditekan.
    // jika ya, status tombol HIGH:
    if (buttonState == HIGH) {
        // nyalakan LED:
        digitalWrite(ledPin, HIGH);
    }
    else {
        // matikan LED:
        digitalWrite(ledPin, LOW);
    }
}
```

- Langkah 2. Kita akan melihat pada board Pin13 LED menyala dan mati.

### Bermain dengan Codecraft

#### Perangkat Keras

**Langkah 1.** Hubungkan Grove - Tombol ke port D2 dari Base Shield.

**Langkah 2.** Hubungkan Base Shield ke Seeeduino / Arduino Anda.

**Langkah 3.** Hubungkan Seeeduino / Arduino ke PC Anda melalui kabel USB.

#### Perangkat Lunak

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), tambahkan dukungan Arduino, dan tarik prosedur utama (main procedure) ke area kerja (working area).

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Panduan untuk Codecraft menggunakan Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Tarik blok seperti gambar di bawah ini atau buka file cdc yang dapat diunduh di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Button/master/img/cc_Button.png)

Unggah program ke Arduino / Seeeduino Anda.

!!!Sukses
     Ketika kode selesai diunggah, LED pada board Arduino / Seeeduino akan menyala ketika Tombol ditekan.

### Bermain Dengan Raspberry Pi (Dengan Grove Base Hat untuk Raspberry Pi)

#### Perangkat keras

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi | Grove - Button |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Button/raw/master/img/button_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Button-p-766.html)

- **Langkah 2**. Pasangkan Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan Grove - Button ke port PWM (port 12) dari Base Hat.
- **Langkah 4**. Hubungkan Raspberry Pi ke PC melalui kabel USB.
![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/with_hat.jpg)


#### Perangkat Lunak

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi lingkungan pengembangan (Development Environment).
- **Langkah 2**. Unduh file sumber dengan melakukan kloning library grove.py.

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Eksekusi perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_button.py 12
```
Jika Anda menghubungkan LED Merah ke port yang berbeda dari Base Hat, sebagai ganti perintah eksekusi **python grove_led.py 12**, Anda harus menjalankan perintah berikut.
```
python grove_button.py portnumber
```


Berikut ini adalah kode grove_button.py.

```python

import time
from grove.button import Button
from grove.factory import Factory


class GroveButton(object):
    def __init__(self, pin):
        # High = ditekan
        self.__btn = Factory.getButton("GPIO-HIGH", pin)
        self.__last_time = time.time()
        self.__on_press = None
        self.__on_release = None
        self.__btn.on_event(self, GroveButton.__handle_event)

    @property
    def on_press(self):
        return self.__on_press

    @on_press.setter
    def on_press(self, callback):
        if not callable(callback):
            return
        self.__on_press = callback

    @property
    def on_release(self):
        return self.__on_release

    @on_release.setter
    def on_release(self, callback):
        if not callable(callback):
            return
        self.__on_release = callback

    def __handle_event(self, evt):
        dt, self.__last_time = evt["time"] - self.__last_time, evt["time"]
        # print("event index:{} event:{} pressed:{}".format(evt["index"], evt["code"], evt["pressed"]))
        if evt["code"] == Button.EV_LEVEL_CHANGED:
            if evt["pressed"]:
                if callable(self.__on_press):
                    self.__on_press(dt)
            else:
                if callable(self.__on_release):
                    self.__on_release(dt)


Grove = GroveButton

def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.GPIO)
    pin = sh.argv2pin()

    button = GroveButton(pin)

    def on_press(t):
        print('Button is pressed')
    def on_release(t):
        print("Button is released, pressed for {0} seconds".format(round(t,6)))

    button.on_press = on_press
    button.on_release = on_release

    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()


```


!!!Sukses
    Jika tidak terjadi kesalahan, anda akan dapat melihat hasinya seperti berikut
```python

pi@raspberrypi:~/grove.py/grove $ python grove_button.py 12
Hat Name = 'Grove Base Hat RPi'
Button is pressed
Button is pressed
Button is pressed
Button is pressed
Button is pressed
Button is pressed
Button is released, pressed for 0.002685 seconds
Button is pressed
Button is released, pressed for 0.219019 seconds
Button is pressed
Button is released, pressed for 0.001372 seconds
Button is pressed
Button is pressed
Button is released, pressed for 0.043143 seconds
Button is pressed
Button is released, pressed for 1.083292 seconds
^CTraceback (most recent call last):
  File "grove_button.py", line 103, in <module>
    main()
  File "grove_button.py", line 99, in main
    time.sleep(1)
KeyboardInterrupt


```

Anda dapat menekan ++ ctrl + c ++ untuk keluar dari program ini.



### Bermain Dengan Raspberry Pi (dengan GrovePi_Plus)

#### Perangkat keras

- Langkah 1. Persiapkan perangkat di bawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Button |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Button/raw/master/img/button_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Button-p-766.html)|

- Langkah 2. Pasangkan GrovePi_Plus ke Raspberry.
- Langkah 3. Hubungkan Grove-Button ke port D3 dari GrovePi Plus.
- Langkah 4. Hubungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove_Button/raw/master/img/rasp_button.jpg)

#### Perangkat lunak

- Langkah 1. Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) ntuk mengkonfigurasi lingkungan pengembangan (Development Environment).
- Langkah 2. Lakukan Git Clone repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```
- Langkah 3. Eksekusi perintah di bawah ini.

```
cd ~/GrovePi/Software/Python
python grove_button.py
```

Ini adalah kode grove_button.py.

```python
import time
import grovepi

# Hubungkan Tombol Grove ke port digital D3
# SIG,NC,VCC,GND
button = 3

grovepi.pinMode(button,"INPUT")

while True:
    try:
        print(grovepi.digitalRead(button))
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- Langkah 4. Kita akan melihat tombol on dan off.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_button.py
0
1
1
1
1
0
0
```

## Sumber-sumber

- **[Eagle&PDF]** [Grove-Button Eagle Files](https://github.com/SeeedDocument/Grove_Button/raw/master/resources/Grove_-_Button_v1.0_Source_File.zip)

- **[More Reading]** [Wooden Laser Gun](http://www.instructables.com/id/DIY-a-Wooden-Laser-Gun-As-a-Xmas-Present-for-Your-/)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Button/master/res/Grove_Button_CDC_File.zip)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Button/master/img/gun.jpg)

Terinspirasi oleh OVERWATCH, kami telah membuat mainan Wooden Laser Gun yang sangat keren untuk bersenang-senang hari ini!

Pistol Laser Kayu dan Target Pistol adalah semua yang didasarkan pada board Arduino yang disebut Seeeduino Lotus. Pemancar laser pada Laser Gun dikendalikan untuk memancarkan pulsa laser untuk "mengaktifkan" Target Gun. Dan ada 3 sensor cahaya pada Gun Target untuk mendeteksi pulsa laser. Sepertinya sangat sederhana bukan? Jika Anda tertarik dengan proyek kami, silakan buat satu untuk diri sendiri atau anak Anda! Ini layak untuk menghabiskan satu hari DIY sebagai hadiah Natal.   


## Proyek

**Grove - Pendahuluan di Tombol & LED String Light** : Pemula - Contoh - Saya yakin pemula akan tersenyum setelah proyek - Kirimkan saya selfie!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-in-a-button-led-string-light-f7e4d6/embed' width='350'></iframe>


**Menggunakan Grove Button Untuk Mengontrol Grove LED**: Cara menghubungkan dan menggunakan Grove Button untuk mengontrol Grove LED socket kit.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/user50338573/using-grove-button-to-control-grove-led-96d00b/embed' width='350'></iframe>

**Modul Tombol dan LED Grove**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/RCtsxwx4OaA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/78lVn_-oYaY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Tech Support / Bantuan

Harap jangan ragu untuk mengirim masukan masalah kepada kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="https://github.com/SeeedDocument/Wiki_Banner/raw/master/new_product.jpg" /></a></p>