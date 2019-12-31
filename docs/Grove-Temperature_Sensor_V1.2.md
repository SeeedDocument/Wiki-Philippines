---
name: Grove - Temperature Sensor V1.2
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html
oldwikiname: Grove - Temperature Sensor V1.2
prodimagename: Grove_Temperature_Sensor_View.jpg
surveyurl: https://www.surveymonkey.com/r/Grove-Temperature_Sensor_V1-2
sku: 101020015
tags: io_3v3, io_5v, plat_duino
---


<p style=":center"><img src="https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View.jpg" ></p>




Modul Grove - Temperature Sensor menggunakan [Thermistor](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/NCP18WF104F03RC.pdf) untuk mendeteksi suhu lingkungan sekitarnya. Resistansi (hambatan) termistor akan meningkat ketika suhu sekitarnya menurun. Karakteristik inilah yang kami gunakan untuk menghitung suhu sekitar. Suhu yang dapat dideteksi oleh sensor adalah -40 - 125ºC dengan keakuratan ±1.5ºC

Catatan: Situs wiki ini bekerja dengan Grove - Temperature sensor V1.1, untuk V1.0 silahkan kunjungi [Grove - Temperature Sensor](http://wiki.seeedstudio.com/Grove-Temperature_Sensor)



<p style=":center"><a href="https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>



## Spesifikasi
---
- Voltage: 3.3 ~ 5V
- Zero power resistance: 100 KΩ
- Resistance Tolerance: ±1%
- Operating temperature range: -40 ~ +125 ℃
- Nominal B-Constant： 4250 ~ 4299K

!!!Tips
    Selengkapnya tentang modul Grove bisa dilihat di [Grove System](http://wiki.seeedstudio.com/Grove_System/)


## Platform yang didukung
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Memulai
---
Setelah bagian ini, anda dapat membuat Grove - Temperature Sensor V1.1/1.2 bekerja hanya dengan beberapa langkah.

!!!Catatan
    Jika ini pertama kalinya Anda bekerja dengan Arduino, kami sangat menyarankan Anda untuk membaca [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.

### Bermain dengan Arduino

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan komponen dibawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Temperature Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View_little.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html)|

- **Langkah 2.** Hubungkan Grove - Temperature Sensor ke port **A0** pada Grove-Base Shield.

- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.

- **Langkah 4.** Hubungkan Seeeduino ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/connect_Arduino.jpg)

!!!Catatan
    Jika tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove - Temperature Sensor ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove - Temperature Sensor |
|---------------|-------------------------|
| 5V           | Red                     |
| GND           | Black                   |
| Not Conencted | White                   |
| A0            | Yellow                  |



#### Software

- **Langkah 1.** Jalankan aplikasi Arduino IDE dan klik **File>New** untuk membuka halaman baru. Salin kode berikut ke halaman baru tersebut dan unggah (Upload). Jika anda tidak mengetahui cara mengunggah kode, silahkan cek [How to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```
// Kode Demo untuk Grove - Temperature Sensor V1.1/1.2
// Loovee @ 2015-8-26

#include <math.h>

const int B = 4275;               // Nilai B pada Thermistor
const int R0 = 100000;            // R0 = 100k
const int pinTempSensor = A0;     // Grove - Temperature Sensor dihubungkan ke A0

void setup()
{
    Serial.begin(9600);
}

void loop()
{
    int a = analogRead(pinTempSensor);

    float R = 1023.0/a-1.0;
    R = R0*R;

    float temperature = 1.0/(log(R/R0)/B+1/298.15)-273.15; // Konversi ke suhu melalui datasheet

    Serial.print("temperature = ");
    Serial.println(temperature);

    delay(100);
}
```

**Langkah 2.** Buka **Serial Monitor** pada Arduino IDE dengan klik **Tool-> Serial Monitor**. atau klik ++ctrl+shift+m++ pada keyboard secara bersamaan. Jika semua berjalan dengan baik, anda dapat mengetahui nilai suhu.


Hasilnya akan seperti:

![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_result.jpg)



### Bermain dengan Raspberry Pi (Dengan Grove Base Hat untuk Raspberry Pi)

#### Hardware

- **Langkah 1**. Komponen yang digunakan dalam proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Temperature Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View_little.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html)|


- **Langkah 2**. Pasang Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan Grove - temperature sensor ke port A0 pada Base Hat.
- **Langkah 4**. Hubungkan Raspberry Pi ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Temperature_Hat.jpg)


!!! Catatan
    Untuk Langkah ke 3 anda dapat menghubungkan modul ke **Port GPIO manapun** tetapi pastikan anda telah mengganti perintah sesuai dengan nomor portnya.


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
python grove_temperature_sensor.py 0

```

Berikut adalah kode grove_temperature_sensor.py .

```python

import sys
import time
from grove.factory import Factory


def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.ADC)
    pin = sh.argv2pin()

    sensor = Factory.getTemper("NTC-ADC", pin)

    print('Detecting temperature...')
    while True:
        print('{} Celsius'.format(sensor.temperature))
        time.sleep(1)


if __name__ == '__main__':
    main()

```

!!!sukses
    Jika semuanya berjalan dengan baik, anda dapat melihat hasilnya seperti berikut
    
```python

pi@raspberrypi:~/grove.py/grove $ python grove_temperature_sensor.py 0
Hat Name = 'Grove Base Hat RPi'
Detecting temperature...
24.7473402633 Celsius
24.7473402633 Celsius
24.7473402633 Celsius
24.7112751977 Celsius
24.7112751977 Celsius
^CTraceback (most recent call last):
  File "grove_temperature_sensor.py", line 53, in <module>
    main()
  File "grove_temperature_sensor.py", line 49, in main
    time.sleep(1)
KeyboardInterrupt

```


Anda dapat keluar dari program ini hanya dengan menekan **ctrl+c** .

!!!Perhatian
        Anda perlu memperhatikan bahwa untuk port analog, nomor pin pada silkscreen adalah sesuatu seperti **A1, A0**, namun dalam perintah kita menggunakan parameter **0** dan **1**, sama seperti port digital. Jadi pastikan Anda menghubungkan modul ke port yang benar,jika tidak, ada kemungkinan terjadinya konflik pin.



### Bermain dengan Raspberry Pi (dengan GrovePi_Plus)

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan komponen dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Temperature Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Ultrasonic_Ranger/raw/master/img/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_View_little.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Temperature-Sensor-p-774.html)|


- **Langkah 2.** Pasang GrovePi_Plus ke Raspberry.

- **Langkah 3.** Hubungkan Grove - Temperature Sensor ke port **A0** pada GrovePi_Plus.

- **Langkah 4.** Hubungkan Raspberry ke PC melalui kabel USB.


![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/connect_pi.jpg)



#### Software

- **Langkah 1.** Ikuti [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengkonfigurasi Lingkungan Pengembangan (development environment).

- **Langkah 2.** Ikuti [Updating the Firmware](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/updating-firmware/) untuk memperbarui firmware terbaru pada GrovePi.

!!!Tips
    Dalam situs wiki ini kita menggunakan alamat (path) **~/GrovePi/** daripada **/home/pi/Desktop/GrovePi**, anda harus memastikan Langkah 2 dan Langkah 3 menggunakan alamat (path) yang sama.

!!!Catatan
    Kami  menyarankan Anda untuk memperbarui firmware, jika tidak untuk beberapa jenis sensor mungkin dapat terjadi masalah


- **Langkah 3.** Lakukan Git clone pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-**Langkah 4.** Jalankan perintah dibawah ini untuk menggunakan Grove - Temperature Sensor untuk mengukur suhu.

```
cd ~/GrovePi/Software/Python
sudo python grove_temperature_sensor.py
```

berikut adalah kode grove_temperature_sensor.py .

```python

# NOTE:
# 	Sensor menggunakan Thremistor untuk mendeteksi suhu lingkungan sekitarnya
# 	Nilai Resistansi (hambatan) Thermistor akan meningkat ketika suhu sekitarnya menurun.
#
# 	ada 3 revisi yaitu 1.0, 1.1 and 1.2, tiap perbaikan menggunakan model thermistor yang berbeda pula.
# 	Setiap datasheet Thermistor menentukan Nominal B-Constant unik yang digunakan dalam rumus perhitungan.
#
# 	Argumen kedua dalam method grovepi.temp()  mendefinisikan versi board mana yang terhubung
# 	Default ke '1.0'. contoh.
# 		temp = grovepi.temp(sensor)        # B value = 3975
# 		temp = grovepi.temp(sensor,'1.1')  # B value = 4250
# 		temp = grovepi.temp(sensor,'1.2')  # B value = 4250

import time
import grovepi

# Hubungkan Grove Temperature Sensor ke port analog A0
# SIG,NC,VCC,GND
sensor = 0

while True:
    try:
        temp = grovepi.temp(sensor,'1.2')
        print("temp =", temp)
        time.sleep(.5)

    except KeyboardInterrupt:
        break
    except IOError:
        print ("Error")

```

Hasilnya harus seperti berikut:

```python

pi@raspberrypi:~/GrovePi/Software/Python $ sudo python grove_temperature_sensor.py

('temp =', 25.28652137917777)
('temp =', 25.28652137917777)
('temp =', 25.28652137917777)
('temp =', 25.28652137917777)
('temp =', 25.368489566400115)
('temp =', 25.61468397498203)
('temp =', 27.43501590142614)
('temp =', 27.85285590636829)
('temp =', 27.18509952680688)
('temp =', 26.852756540240193)

```



## Referensi
---
Jika anda ingin mengetahui bagaimana algoritma suhunya silakan lihat gambar di bawah ini:

![](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/img/Grove_Temperature_Sensor_Basic_Characteristics.jpg)


## Sumber - Sumber
---

- **[Zip]** [Grove - Temperature Sensor v1.1 Eagle File](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/Grove_-_Temperature_sensor_v1.1.zip)
- **[PDF]** [Grove - Temperature Sensor v1.1.PDF](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/Grove_-_Temperature_sensor_v1.1.pdf)
- **[PDF]** [Temperature Sensor datasheet](https://github.com/SeeedDocument/Grove-Temperature_Sensor_V1.2/raw/master/res/NCP18WF104F03RC.pdf)


## Proyek - Proyek

**Modul Grove Sensor Suhu**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/wjL7xOGqAqg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/vI9pkmiK8EM" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>