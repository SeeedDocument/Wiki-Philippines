---
name: Grove - PIR Motion Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html
oldwikiname: Grove - PIR Motion Sensor
prodimagename: Breakout_for_LinkIt_Smart_7688_v2.0_product_view_700.jpg
surveyurl: https://www.surveymonkey.com/r/grove-pir-motion-sensor
sku: 101020020
tags: io_3v3, io_5v, plat_duino, plat_pi
---


![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove_-_PIR_Motion_Sensor.jpg)

Sensor ini memungkinkan mendeteksi adanya gerakan, biasanya gerakan manusia yang masih dalam jangkauan. Cukup sambungkan ke Grove - Base shield dan program itu, ketika ada yang bergerak dalam jangkauan pendeteksiannya, sensor akan menampilkan HIGH (1) pada pin SIG.

<p style=":center"><a href="https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>

## Fitur

- Antarmuka kompatibel Grove
- Jarak deteksi yang dapat disesuaikan
- Waktu holding yang bisa disesuaikan

!!!Tip
    Lebih detail mengenai modul Grove silahkan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi

|Parameter	|Nilai/jangkauan
|---|---|
|Tegangan operasi|	3V–5V
|Arus operasi(VCC = 3V) |	100uA
|OArus operasi(VCC = 5V)|	150uA
|Jangkauan ukur	|0.1 - 6m
|Jarak deteksi standar|	3m
|Waktu Holding	|1 - 25s
|Panjang gelombang kerja|7 - 14um
|Sudut deteksi|	120 derajat

## Platforms yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.

## Memulai

!!!Catatan
    Jika ini adalah pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk melihat [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) before the start.

### Bermain dengan Arduino

#### Hardware (Perangkat Keras)


- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Grove - PIR Motion Sensor | Base Shield |
|--------------|----------------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove%20-%20PIR%20Motion%20Sensor_s.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|


- **Langkah 2.** Hubungkan modul Grove - PIR Motion Sensor ke port **D2** dari Grove-Base Shield.

- **Langkah 3.** Pasangkan Grove - Base Shield ke Seeeduino.

- **Langkah 4.** Hubungkan Seeeduino ke PC dengan kabel USB.


![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/connect_arduino.jpg)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-PIR Motion Sensor ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove - PIR Motion Sensor |
|---------------|-------------------------|
| 5V            | Merah                   |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D2            | Kuning                  |



#### Perangkat Lunak

- Salin kode di bawah ini ke Arduino IDE dan upload (unggah). Jika Anda tidak tahu cara mengupload (unggah) kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```c
/*macro definitions of PIR motion sensor pin and LED pin*/
#define PIR_MOTION_SENSOR 2//Use pin 2 to receive the signal from the module


void setup()
{
    pinMode(PIR_MOTION_SENSOR, INPUT);
    Serial.begin(9600);  

}

void loop()
{
    if(digitalRead(PIR_MOTION_SENSOR))//if it detects the moving people?
        Serial.println("Hi,people is coming");
    else
        Serial.println("Watching");

 delay(200);
}

```


!!!Catatan
    Jarak deteksi dan waktu holding dapat disesuaikan dengan menambahkan dua potensiometer tambahan pada modul. Untuk detailnya silakan merujuk ke V1.2 Eagle di bawah ini. Modul ini juga dapat diatur sebagai retriggerable atau un-retriggerable dengan mengganti jumper hat.


Hasilnya harus seperti:


![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/result_arduino.png)

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan modul Grove - PIR Motion Sensor ke port D2 dari Base Shield.

**Langkah 2.** Pasangkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_PIR_Motion_Sensor/master/img/cc_PIR_Motion_Sensor.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode selesai di-upload (unggah), LED akan menyala ketika ada orang datang.

### Bermain dengan Raspberry Pi (menggunakan Grove Base Hat untuk Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - PIR Motion Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove%20-%20PIR%20Motion%20Sensor_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html)|


- **Langkah 2**. Pasangkan modul Grove Base Hat ke Raspberry.
- **Langkah 3**. Hubungkan modul PIR motion sensor ke port 12 dari the Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry Pi ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Motion_Hat.jpg)


!!! Catatan
    Untuk langkah 3 Anda dapat menghubungkan sensor cahaya ke **sembarang port Analog** tetapi pastikan Anda mengubah perintah dengan nomor port yang sesuai.


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengonfigurasi pengembangan proyek.
- **Langkah 2**. Download (unduh) file sumber dengan memperbanyak grove.py library. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_mini_pir_motion_sensor.py 12

```

Berikut kode grove_mini_pir_motion_sensor.py.

```python

import time
from grove.gpio import GPIO


class GroveMiniPIRMotionSensor(GPIO):
    def __init__(self, pin):
        super(GroveMiniPIRMotionSensor, self).__init__(pin, GPIO.IN)
        self._on_detect = None

    @property
    def on_detect(self):
        return self._on_detect

    @on_detect.setter
    def on_detect(self, callback):
        if not callable(callback):
            return

        if self.on_event is None:
            self.on_event = self._handle_event

        self._on_detect = callback

    def _handle_event(self, pin, value):
        if value:
            if callable(self._on_detect):
                self._on_detect()

Grove = GroveMiniPIRMotionSensor


def main():
    import sys

    if len(sys.argv) < 2:
        print('Usage: {} pin'.format(sys.argv[0]))
        sys.exit(1)

    pir = GroveMiniPIRMotionSensor(int(sys.argv[1]))

    def callback():
        print('Motion detected.')

    pir.on_detect = callback

    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()

```

!!!sukses
    Jika semuanya berjalan dengan baik, Anda akan dapat melihat hasil berikut

```python

pi@raspberrypi:~/grove.py/grove $ python grove_mini_pir_motion_sensor.py 12
Motion detected.
Motion detected.
Motion detected.
^CTraceback (most recent call last):
  File "grove_mini_pir_motion_sensor.py", line 84, in <module>
    main()
  File "grove_mini_pir_motion_sensor.py", line 80, in main
    time.sleep(1)
KeyboardInterrupt

```

Anda dapat keluar dari program ini hanya dengan menekan ++ctrl+c++.




### Bermain dengan Raspberry Pi (menggunakan GrovePi_Plus)

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - PIR Motion Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Grove%20-%20PIR%20Motion%20Sensor_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-PIR-Motion-Sensor-p-802.html)|


- **Langkah 2.** Pasangkan modul GrovePi_Plus ke Raspberry.

- **Langkah 3.** Hubungkan modul sensor ke port **D8** dari GrovePi_Plus.

- **Langkah 4.** Hubungkan modul Raspberry ke PC dengan kabel USB.


![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/connect_pi.jpg)

#### Software (Perangkat Lunak)


- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk konfigurasi pengembangan proyek.

- **Langkah 2.** ikuti langkah [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/) untuk memperbarui firmware terbaru GrovePi.

!!!Tip
    Di wiki ini kami menggunakan path **~/GrovePi/** sebagai ganti **/home/pi/Desktop/GrovePi**, Anda harus memastikan Langkah 2 dan Langkah 3 menggunakan path yang sama.

!!!Catatan
    Kami sangat menyarankan Anda untuk memperbarui firmware, atau untuk beberapa sensor Anda mungkin mendapatkan kesalahan.


- **Langkah 3.** Download (unduh) kode pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-	**Langkah 4.** Jalankan perintah di bawah ini untuk menggunakan Sensor Gerak PIR untuk memantau pergerakan orang.

```
cd ~/GrovePi/Software/Python
sudo python grove_pir_motion_sensor.py
```

Berikut kode the grove_pir_motion_sensor.py.

```python
import time
import grovepi

# Connect the Grove PIR Motion Sensor to digital port D8
# SIG,NC,VCC,GND
pir_sensor = 8

grovepi.pinMode(pir_sensor,"INPUT")

while True:
    try:
        # Sense motion, usually human, within the target range
        if grovepi.digitalRead(pir_sensor):
            print 'Motion Detected'
        else:
            print '-'

        # if your hold time is less than this, you might not see as many detections
        time.sleep(.2)

    except IOError:
        print "Error"
```

Hasilnya akan seperti dibawah ini:

```python
pi@raspberrypi:~/GrovePi/Software/Python $ sudo python grove_pir_motion_sensor.py

-
-
-
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
Motion Detected
-
-

```

## FAQs

**Q1: Bagaimana cara membuat jarak yang sesuai?**

A1: R2: digunakan untuk mengatur jarak deteksi (koefisien AMP, 2MΩ). R6: digunakan untuk mengatur waktu holding (trigger duty, 100KΩ). 

Jarak deteksi dapat disesuaikan dari 6 meter menjadi hanya beberapa sentimeter. Jika potensiometer diatur ke satu sisi, modul akan terlalu sensitif untuk dipicu oleh lingkungan yang bahkan tidak ada orang yang bergerak sebelumnya. Waktu holding juga dapat disesuaikan dengan potensiometer Delay_time, nilainya sekitar dari 25 detik hingga 1 detik.

Jika R2 dan R6 disolder, pastikan R13 dan R14 kosong.

!!!Catatan
    ada risiko modul rusak. Harap pikirkan sebelum melakukan modifikasi ini.

![](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/img/Resistor.png)


## Sumber - Sumber


- **[Eagle]** [Grove - PIR Motion Sensor Eagle File v1.2](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/res/Grove%20PIR%20Motion%20Sensor_v1_2.zip)
- **[PDF]** [Grove - PIR Motion Sensor v1.2 Schematics](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/resources/Grove_PIR_Sensor_v1.2.pdf)
- **[PDF]** [Grove - PIR Motion Sensor Eagle V1.2 PCB](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/res/Grove%20-%20PIR%20motion%20sensor%20v1.1b%20PCB.pdf)
- **[Library]** [Github repository for PIR Motion Sensor](https://github.com/Seeed-Studio/PIR_Motion_Sensor)
- **[Datasheet]** [BISS0001 Datasheet](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/resources/Twig_-_BISS0001.pdf)
- **[Datasheet]** [Fresnel lens 8120 Datasheet](https://github.com/SeeedDocument/Grove_PIR_Motion_Sensor/raw/master/resources/Fresnel_lens_8120.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_PIR_Motion_Sensor/master/res/Grove_PIR_Motion_Sensor_CDC_File.zip)


## Proyek

**Alarm Pencuri dengan PIR Motion Sensor**: Artikel ini menjelaskan Alarm Pencurian dengan PIR Motion Sensor.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/pooja_baraskar/burglar-alarm-with-pir-motion-sensor-964c42/embed' width='350'></iframe>

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>