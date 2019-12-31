---
name: Grove - Relay
category: Actuator
bzurl: https://www.seeedstudio.com/Grove-Relay-p-769.html
oldwikiname:
prodimagename: Twig-Relay.jpg
surveyurl: https://www.surveymonkey.com/r/Grove_Relay
sku: 103020005
tags: io_3v3, io_5v, plat_duino, plat_linkit, plat_bbg, plat_pi,plat_wio
---


<p style=":center"><img src="https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/Twig-Relay.jpg" /></p>




 Modul Grove-Relay adalah saklar digital dengan rangkaian terbuka (normally-open). Dengan ini, anda dapat mengontrol ragkaian tegangan tinggi dengan tegangan rendah, misalnya 5V pada pengontrol. Ada sebuah indikator LED di board, yang akan menyala ketika terminal yang dikontrol aktif.

<iframe width="800" height="450" src="https://www.youtube.com/embed/MwLEawbP0ZU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<p style=":center"><a href="https://www.seeedstudio.com/Grove-Relay-p-769.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/300px-Get_One_Now_Banner-ragular.png" /></a></p>


## Versi


| Parameter     | V1.1     |V1.2     |
| :------------- | :------------- |:------------- |
| Tanggal Rilis Produk      | 27 Januari 2013       |9 Juni 2014|
|Tegangan Kerja|5V|3.3V~5V|
|Arus Kerja|60mA|100mA|
|Siklus Relay|100,000 putaran|100,000 putaran|
|Tegangan Switching Maksimal|250VAC/30VDC|250VAC/30VDC|
|Arus Switching Maksimal|5A|5A|

!!!Tip
    Detail lebih lanjut tentang modul Grove anda dapat mengacu ke [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.



## Memulai

### Bermain dengan Arduino


!!!Catatan
    Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.

#### Bahan yang dibutuhkan

| Seeeduino V4.2 | Base Shield| Grove-Button **x2** |Grove-Relay|
|--------------|-------------|-----------------|-----|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/button_s.jpg)|![](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Thumbnail.jpg)|
|<a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Grove-Button-p-766.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Grove-Relay-p-769.html" target="_blank">Dapatkan Sekarang</a>|



!!!Catatan
    **1** Harap menyambungkan kabel USB dengan hati-hati, agar tidak terjadi kerusakan pada port. Diharapkan menggunakan kabel USB dengan 4 kawat di dalamnya, karena  kabel 2 kawat tidak dapat untuk mentransfer data. Jika anda tidak mempunyai kabel jenis tersebut, anda dapat klik link berikut [here](https://www.seeedstudio.com/Micro-USB-Cable-48cm-p-1475.html) untuk membeli

**2** Setiap modul Grove dilengkapi dengan kabel Grove saat Anda membeli. Jika Anda kehilangan kabel Grove, Anda dapat klik link berikut [here](https://www.seeedstudio.com/Grove-Universal-4-Pin-Buckled-20cm-Cable-%285-PCs-pack%29-p-936.html) untuk membeli



#### Hardware

- **Langkah 1.** Hubungkan Grove-Relay ke port **D4** dari Grove-Base Shield.

- **Langkah 2.** Hubungkan Grove-Button#1 ke port **D2** dari Grove-Base Shield, Hubungkan Grove-Button#2 ke port **D3** dari Grove-Base Shield. 

- **Langkah 3.** Pasang Grove - Base Shield kedalam Seeeduino.

- **Langkah 4.** Hubungkan Seeeduino ke PC lewat kabel Micro-USB.


![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/button-relay.jpg)


!!!Catatan
    Jika anda tidak mempunyai base shield, anda dapat langsung menghubungkan Grove-Relay dan Grove-Button ke board Arduino. Ikuti petunjuk di bawah ini.

| Grove-Relay | Arduino |  Kabel Grove |
|-------------|---------|-----------|
| GND         | GND     | Hitam|
| VCC         | 5V      |Merah|
| SIG         | D4      |Kuning|

| Grove-Button#1 | Arduino |Kabel Grove |
|----------------|---------|-------|
| GND            | GND     |Hitam|
| VCC            | 5V      |Merah|
| SIG            | D2      |Kuning|

| Grove-Button#2 | Arduino |Kabel Grove|
|----------------|---------|----|
| GND            | GND     |Hitam|
| VCC            | 5V      |Merah|
| SIG            | D3      |Kuning|




#### Software


Berikut ini adalah demo yang menunjukkan cara mengontrol Grove - Relay dengan Grove - Button. Ketika satu tombol ditekan, relay akan terhubung. Ketika tombol lainnya ditekan, relay akan terputus.

- **Langkah 1.** Buka Arduino IDE dan salin code berikut kedalam program baru.


```
// Relay Control

void setup()
{
  pinMode(2, INPUT);
  pinMode(3, INPUT);
  pinMode(4, OUTPUT);
}

void loop()
{
  if (digitalRead(2)==HIGH)
  {
    digitalWrite(4, HIGH);
    delay(100);
  }
  if (digitalRead(3)==HIGH)
  {
    digitalWrite(4, LOW);
  }
}

```

- **Langkah 2.** Unggah (upload) program demo. Jika Anda tidak tahu cara mengunggah kode, harap periksa [How to upload code](http://wiki.seeedstudio.com/Upload_Code/).


Selesai mengunggah, jika Anda menekan tombol #1 relay seharusnya aktif; dan jika Anda menekan tombol #2 relay seharusnya tidak aktif.


### Bermain dengan Codecraft

#### Perangkat Keras

**Langkah 1.** Hubungkan Grove - Relay ke port D4, hubungkan dua Grove - Button ke port D2 dan port D3 dari Base Shield.

**Langkah 2.** Pasang Base Shield ke Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda lewat kabel USB.

#### Software

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/),  tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Seret (drag) blok-blok yang ada seperti gambar dibawah ini atau buka file cdc yang dapat diunduh pada akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/cc_Relay.png)

Unggah program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode selesai diunggah. Relay akan menyala saat Anda menekan tombol yang terhubung ke port D2, dan relay akan mati saat Anda menekan tombol yang terhubung ke port D3.


### Bermain dengan Raspberry Pi (dengan Grove Base Hat untuk Raspberry Pi)

#### Hardware

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Relay |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Thumbnail.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Relay-p-769.html)|

- **Langkah 2**. Pasang Grove Base Hat ke Raspberry.
- **Langkah 3**. Hubungkan Grove - Relay ke port 12 dari Base Hat.
- **Langkah 4**. Hubungkan Raspberry Pi ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Relay_Hat.jpg)

!!! Catatan
    Untuk langkah 3 Anda dapat menghubungkan modul relay ke **GPIO Port manapun** tetapi pastikan Anda mengubah perintah dengan nomor port yang sesuai.


#### Software

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengkonfigurasi Lingkungan Pengembangan (Development Environment).
- **Langkah 2**. Unduh sumber file dengan melakukan duplikasi dari library grove.py . 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Eksekusi perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_relay.py 12

```

Berikut adalah kode grove_relay.py .

```python

from grove.gpio import GPIO


class GroveRelay(GPIO):
    def __init__(self, pin):
        super(GroveRelay, self).__init__(pin, GPIO.OUT)

    def on(self):
        self.write(1)

    def off(self):
        self.write(0)


Grove = GroveRelay


def main():
    import sys
    import time

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    relay = GroveRelay(int(sys.argv[1]))

    while True:
        try:
            relay.on()
            time.sleep(1)
            relay.off()
            time.sleep(1)
        except KeyboardInterrupt:
            relay.off()
            print("exit")
            exit(1)            

if __name__ == '__main__':
    main()



```

!!!Sukses
    Jika semuanya berjalan dengan baik, Anda akan melihat indikator LED berkedip.


Anda dapat keluar dari program ini hanya dengan menekan **ctrl+c**.





### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

#### Hardware

**Bahan yang dibutuhkan**

| Raspberry pi | GrovePi_Plus| Grove-Button  |Grove-Relay|
|--------------|-------------|-----------------|-----|
|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/button_s.jpg)|![](https://github.com/SeeedDocument/Grove-Relay/raw/master/img/Thumbnail.jpg)|
|<a href="https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/GrovePi%2B-p-2241.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Grove-Button-p-766.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Grove-Relay-p-769.html" target="_blank">Dapatkan Sekarang</a>|



- **Langkah 1.** Pasang GrovePi_Plus ke Raspberry.

- **Langkah 2.** Hubungkan Grove-Relay ke port **D4** dari GrovePi_Plus.

- **Langkah 3.** Hubungkan Grove-Button ke port **D3** dari GrovePi_Plus.

- **Langkah 4.** Hubungkan Raspberry ke PC lewat kabel USB.


![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/GrovePiPlus_Grove_relay.jpeg)


#### Software


Jika Anda pertama kali menggunakan GrovePi, tolong ikuti langkah demi langkah. Jika Anda pengguna lama GrovePi, Anda dapat melewatkan **Langkah 1** dan **Langkah 2**.


- **Langkah 1.** Menyiapkan Software. Di command line terminal , ketikkan perintah berikut:

```
sudo curl -kL dexterindustries.com/update_grovepi | bash

```

```
sudo reboot
```

```
cd /home/pi/Desktop
```
```
git clone https://github.com/DexterInd/GrovePi.git
```

Untuk detail lebih lanjut tentang bagian ini, silakan mengacu ke[Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/).


- **Langkah 2.** Ikuti langkah [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/) untuk memperbarui firmware versi terbaru dari GrovePi.


!!!Catatan
    Kami  menyarankan Anda untuk memperbarui firmware, jika tidak untuk beberapa jenis sensor mungkin dapat terjadi error.


- **Langkah 3.** Jalankan perintah berikut untuk mendapatkan hasilnya.

```
cd /home/pi/Desktop/GrovePi/Software/Python/
sudo python grove_switch_relay.py
```


Jika Anda ingin melakukan cek pada kodenya, Anda dapat menggunakan perintah berikut:


```
sudo nano grove_switch_relay.py

```

Kode :

```python
# Raspberry Pi + Grove Switch + Grove Relay

import time
import grovepi
# Sambungkan the Grove Switch ke port digital D3
# SIG,NC,VCC,GND

switch = 3
# Sambungkan the Grove Switch ke port digital D4
# SIG,NC,VCC,GND

relay = 4
grovepi.pinMode(switch,"INPUT")
grovepi.pinMode(relay,"OUTPUT")
while True:
    try:
        if grovepi.digitalRead(switch):
            grovepi.digitalWrite(relay,1)
        else:
            grovepi.digitalWrite(relay,0)
            time.sleep(.05)
    except KeyboardInterrupt:
        grovepi.digitalWrite(relay,0)
        break
    except IOError:
        print "Error"
```



### Bermain dengan TI LaunchPad

Mengontrol elektronik lainnya (Relay)

![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/img/Relay.jpg)

Contoh ini menunjukkan cara menggunakan modul Grove-relay untuk mengontrol beban yang lebih besar, misalnya lampu meja. Tegangan 3V dapat menyebabkan relay menyala, sehingga arus dapat mengalir melalui alat elektronik yang terhubung.

```
/*
Relay
The basic Energia example.
This example code is in the public domain.
*/

#define RELAY_PIN 39

// Fungsi setup dieksekusi sekali ketika anda menekan tombol reset :
void setup() {
         pinMode(RELAY_PIN, OUTPUT); // Inisialisasi pin digital sebagai output.
}

// Fungsi loop akan dieksekusi berulang ulang :
void loop() {
         digitalWrite(RELAY_PIN, HIGH); // Mengaktifkan relay (HIGH adalah level tegangan)
         delay(1000);   // Tunda selama 1 detik
         digitalWrite(RELAY_PIN, LOW);   // Mengaktifkan relay (LOW adalah level tegangan)
         delay(1000);   // Tunda selama 1 detik
}
```


## Sumber - sumber

* **[Eagle]** [Grove - Relay Schematic and PCB in Eagle format](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/res/Grove-Relay_Eagle_Files.zip)
* **[PDF]** [Grove - Relay PCB in PDF format](https://github.com/SeeedDocument/Grove-Relay/raw/master/res/Grove%20-%20Relay%20PCB.pdf)
* **[PDF]** [Grove - Relay Schematic in PDF format](https://github.com/SeeedDocument/Grove-Relay/raw/master/res/Grove%20-%20Relay%20Schematic.pdf)
* **[Datasheet]** [HLS8-T73 Series Relay Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/res/Relay_Datasheet.pdf)
* **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Relay/master/res/Grove_Relay_CDC_File.zip)

## Proyek - Proyek

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;}
.tg .tg-yw4l{vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-031e"><iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/sodaqmoja/using-a-switch-to-open-and-close-a-relay-3329ec/embed' width='350'></iframe></th>
    <th class="tg-031e"><iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/rei-vilo/private-iot-with-blynk-on-local-server-619926/embed' width='350'></iframe></th>
    <th class="tg-yw4l"><iframe frameborder='0' height='327.5' scrolling='no' src='https://project.seeedstudio.com/josephroberts/resinified-office-lock-0ca2eb/embed' width='350'></iframe></th>
  </tr>
</table>

**Relay Grove module** :
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/DnHqh_Rupb8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/JOsjUOI9FU8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Bantuan Teknis / Tech Support 
Please submit any technical issue into our [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>