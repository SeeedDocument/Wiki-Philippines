---
name: Grove - Switch(P)
category: Sensor
bzurl: https://seeedstudio.com/Grove-Switch(P)-p-1252.html
oldwikiname: Grove_-_Switch(P)
prodimagename: GroveSwitchP_01.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/GroveSwitchP.jpg
surveyurl: https://www.research.net/r/Grove-Switch-P
sku: 101020004
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_pi, plat_bbg
---

![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/switch_p.jpg)

Grove – Switch ini adalah sebuah mini SPDT slide yang cocok digunakan untuk kondisi "ON/OFF" . Modul ini adalah saklar yang handal dengan kualitas pembuatan yang bagus yang kami gunakan di sebagian besar board kami. Anda harus menyimpan beberapa buah untuk prototipe sistem Grove anda.

Apa maksud dari “P” ? “P” adalah singkatan dari "pemasangan panel" (“panel mount”) pada produk ini.

<p style=":center"><a href="http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Versi

| Versi Produk             | Perubahan                                   | Tanggal Rilis |
|------------------------------|-------------------------------------------|---------------|
|Grove-Saklar(P) V1.0          | Awal                                   | Juli 2012      |     


## Fitur - Fitur

-   Grove Interface
-   Mudah digunakan
-   Elemen Grove yang sederhana

!!!Tips
    Detail lebih lanjut tentang modul Grove anda dapat melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi

| Komponen              | Nilai    |
|-----------------------|----------------|
| Tegangan Kerja     | 3.3/5V         |
| Electrical Life       | 10,000 siklus  |
| Kekuatan Kerja      | 200 ± 50gf     |
| Suhu Operasional | -20℃ to +80℃   |
| Ukuran                  | 20mmX20mm      |


## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai

!!!Catatan
    Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


### Bermain dengan Arduino

**Hardware**

- **Langkah 1.** Siapkan peralatan di bawah ini :

| Seeeduino V4.2 | Base Shield|  Grove-Switch(P) |Grove - Purple LED (3mm)|
|--------------|-------------|-----------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/SwitchP_s.jpg)|![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/grove_led_s.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Purple-LED-%283mm%29-p-1143.html)|

- **Langkah 2.** Sambungkan Grove-Saklar(P) ke port **D2**  dari Grove-Base Shield.
- **Langkah 3.** Sambungkan Grove-LED ke port **D6**  dari Grove-Base Shield.
- **Langkah 4.** Pasang Grove - Base Shield ke dalam Seeeduino.
- **Langkah 5.** Sambungkan Seeeduino ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/seeeduino_switch_led.jpg)

!!!Catatan
	Jika Anda tidak mempunyai Grove Base Shield, Anda dapat langsung menghubungkan Grove-Switch(P) dan Grove - Purple LED (3mm) ke Seeeduino seperti di bawah ini.

| Seeeduino | Grove-Switch(P) | Seeeduino | Grove - Purple LED (3mm) |
|-----------|-----------------|-----------|--------------------------|
| 5V        | Merah             | 5V        | Merah                      |
| GND       | Hitam           | GND       | Hitam                    |
| NC        | Putih           | NC        | Putih                    |
| D2        | Kuning          | D6        | Kuning                   |

**Software**

- **Langkah 1.** Silahkan salin code untuk Arduino IDE di bawah ini dan upload (unggah) ke arduino.Jika Anda tidak tahu cara upload (unggah) kode, Silahkan mengecek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```
const int switchPin = 2;     // Nomor dari pin pushbutton
const int ledPin =  6;      // Nomor dari pin LED

int switchState = 0;         // variable untuk membaca status dari pushbutton

void setup() {
    // inisialisasi pin LED sebagai output:
    pinMode(ledPin, OUTPUT);
    // inisialisasi pin switch sebagai input:
    pinMode(switchPin, INPUT);
    Serial.begin(9600);
}

void loop(){
    // Membaca state dari nilai switch:
    switchState = digitalRead(switchPin);

    if (switchState == HIGH) {
        //Menyalakan LED:
        digitalWrite(ledPin, HIGH);
        Serial.println("switch high!");
    }
    else {
        //Mematikan LED:
        digitalWrite(ledPin, LOW);
        Serial.println("switch low");
    }
}

```

- **Langkah 2.** Ketika Anda menyalakan saklar maka lampu LED menyala. Anda juga dapat melihat Serial output seperti di bawah ini. 

```
switch high!
switch high!
switch high!
```

### Bermain dengan Raspberry Pi (dengan Grove Base Hat for Raspberry Pi)

#### Hardware

- **Langkah 1**. Menggunakan beberapa komponen di bawah ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Switch P |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/SwitchP_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html)|


- **Langkah 2**. Pasang Grove Base Hat ke dalam Raspberry.
- **Langkah 3**. Sambungkan Switch ke port 12 dari Base Hat.
- **Langkah 4**. Sambungkan Raspberry Pi ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/Switch_Hat.jpg)


!!! Catatan
    Untuk langkah 3 Anda dapat menghubungkan saklar ke **GPIO Port manapun** tapi pastikan Anda mengubah perintah dengan menggunakan nomor port yang sesuai.


#### Software

- **Langkah 1**. Ikuti langkah dari [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Unduh file sumber (source)dengan melakukan kloning dari library grove.py . 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Eksekusi perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_switch.py 12

```

Dibawah ini adalah kode dari grove_switch.py .

```python


import time
from grove.gpio import GPIO


class GroveTiltSwitch(GPIO):
    def __init__(self, pin):
        super(GroveTiltSwitch, self).__init__(pin, GPIO.IN)

    @property
    def state(self):
        return super(GroveTiltSwitch, self).read()


Grove = GroveTiltSwitch


def main():
    import sys

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    swicth = GroveTiltSwitch(int(sys.argv[1]))


    while True:
        if swicth.state is 1:
            print("on")
        else:
            print("off")
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!Sukses

    Jika semuanya berjalan dengan baik, Anda akan dapat melihat hasilnya seperti berikut
    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_switch.py 12
off
off
on
off
on
on
off
^CTraceback (most recent call last):
  File "grove_switch.py", line 70, in <module>
    main()
  File "grove_switch.py", line 66, in main
    time.sleep(1)
KeyboardInterrupt


```


Anda dapat keluar dari program ini hanya dengan menekan **ctrl+c**.



### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

**Perangkat Keras**

- **Langkah 1.** Siapkan peralatan di bawah ini :

| Raspberry pi | GrovePi_Plus | Grove-Switch(P) |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/SwitchP_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/Grove-Switch(P)-p-1252.html)|


- **Langkah 2.** Pasang GrovePi_Plus ke dalam Raspberry.
- **Lagkah 3.** Sambungkan Grove-Switch(P) ke port **D3**  dari GrovePi_Plus.
- **Step 4.** Sambungkan Raspberry ke PC melalui kabel USB.

![](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/img/rpi_switch.jpg)

**Software**

- **Langkah 1.** Ikuti langkah dari [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi perkembangan.
- **Langkah 2.** Lakukan Git Clone pada repositori github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

- **Langkah 3.**Eksekusi perintah di bawah ini untuk memantau status switch.


```python
cd ~/GrovePi/Software/Python
python grove_switch.py
```

Berikut ini adalah kode grove_switch.py .

```python
import time
import grovepi

# Hubungkan Grove Switch ke port  digital D3
# SIG,NC,VCC,GND
switch = 3

grovepi.pinMode(switch,"INPUT")

while True:
    try:
        print(grovepi.digitalRead(switch))
        time.sleep(.5)

    except IOError:
        print ("Error")
```

- **Langkah 4.** Anda akan melihat status saklar seperti dibawah ini.

```python
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_switch.py 
1
1
0
0
0
```

## Sumber - sumber

- **[Eagle&PDF]** [Grove-Switch(P) Schematic](https://github.com/SeeedDocument/Grove-Switch-P/raw/master/res/Grove-Switch-P-Eagle_File_v1.0.zip)

## Projek

**Using a Switch to Open and Close a Relay***: Anda akan mempelajari nilai dari saklar (switch), dengan fungsi High dan Low. Selain itu, Anda akan belajar cara menggunakan relay sebagai aktuator.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/sodaqmoja/using-a-switch-to-open-and-close-a-relay-3329ec/embed' width='350'></iframe>

## Tech Support
Please submit any technical issue into our [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>