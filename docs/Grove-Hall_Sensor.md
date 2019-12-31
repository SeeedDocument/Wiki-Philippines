---
name: Grove - Hall Sensor
category: Sensor
bzurl: https://seeedstudio.com/Grove-Hall-Sensor-p-965.html
oldwikiname: Grove_-_Hall_Sensor
prodimagename: Grove-Hall_Sensor_New.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/hall sensor.jpg
surveyurl: https://www.research.net/r/Grove-Hall_Sensor
sku: 101020046
tags: grove_digital, io_5v, plat_duino, plat_linkit
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/img/Grove-Hall_Sensor_New.jpg)

Sensor Hall didasarkan pada Hall Effect, yang merupakan produksi dari perbedaan tegangan pada sebuah konduktor listrik yang mempunyai arah melintang ke arus listrik dalam sebuah konduktor sedangkan medan magnet mempunyai arah tegak lurus terhadap arus. Modul ini dilengkapi dengan saklar continous-time. Output dari modul ini berlogika low (menyala) ketika medan magnet (polaritas selatan) tegak lurus ke sensor Hall melebihi ambang titik operasi BOP dan belogika tinggi (mati) ketika medan magnet menghilang. Sedangkan twig digunakan untuk mengukur RPM.

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/depot/grove-hall-sensor-p-965.html)


## Versi

| Revisi | Deskripsi           | Rilis    |
|----------|------------------------|------------|
| Grove - Hall Sensor v0.9b    | Initial public release | 3,Oct,2011 |


## Fitur

-   Grove Compatible Interface
-   400ns transition period for rise and fall.
-   Continuous-time hall effect sensor
-   Reverse battery protection

!!!Tips
    Rincian lebih detail tentang modul Grove silakan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

    
## Spesifikasi

| Parameter                 | Min | Typical | Max | Unit |
|-----------------------|-----|---------|-----|------|
| Tegangan Suplai        | 3.8 | 5.0     | 24  | V    |
| Arus Suplai       | 4.1 | -       | 24  | mA   |
| Suhu Operasional | -40 | -       | 85  | ºC   |

## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


## Ide Aplikasi

-   RPM meter.
-   Simple dc motor.

## Memulai

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Arduino, kami sangat menyarankan Anda untuk melihat [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


### Bermain dengan Arduino

#### Demonstrasi

Sensor Hall digunakan dengan memanfaatkan interrupt eksternal yang tersedia di arduino / seeeduino. Dalam contoh ini kita menggunakan interrupt 0 yang terdapat pada digital pin 2. Untuk interrupt lainnya, lihat [attachInterrupt()](http://www.arduino.cc/en/Reference/AttachInterrupt).

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield| Grove - Hall Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/img/Grove-Hall_Sensor_New%20_small.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](http://www.seeedstudio.com/depot/grove-hall-sensor-p-965.html)|

- **Langkah 2.** Hubungkan Grove - Hall Sensor ke port D2 dari Grove-Base Shield.
- **Langkah 3.** Pasang Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC menggunakan kabel USB.

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan modul ini ke Seeeduino seperti dibawah ini.

| Seeeduino       | Grove - Hall Sensor |
|---------------|-------------------------|
| 5V           | Merah                     |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D2            | Kuning                  |


#### Software (Perangkat Lunak)

- **Langkah 1.**  Download (unduh) [Hall Sensor Code](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Grove-Hall_Sensor_Demo_Code.zip)

- **Langkah 2.**  Buka salah satu dari dua kode. Misalnya Demo **MagnetControlLED**


- **Langkah 3.**  Salin kode ke Arduino IDE dan upload (unggah). Jika Anda tidak tahu cara mengupload (unggah) kode, harap periksa [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).


```c
/****************************************************************************/	
//	Function: When a magnet whose south pole is facing up is approaching to 
//			  the onboard sensor, the LED will be turned on.Otherwise, the 
//			  LED will be turned off.
//	Hardware: Grove - Hall Sensor, Grove - LED
//	Arduino IDE: Arduino-1.0
//	Author:	 FrankieChu		
//	Date: 	 Jan 20,2013
//	Version: v1.0
//	by www.seeedstudio.com
//
//  This library is free software; you can redistribute it and/or
//  modify it under the terms of the GNU Lesser General Public
//  License as published by the Free Software Foundation; either
//  version 2.1 of the License, or (at your option) any later version.
//
//  This library is distributed in the hope that it will be useful,
//  but WITHOUT ANY WARRANTY; without even the implied warranty of
//  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
//  Lesser General Public License for more details.
//
//  You should have received a copy of the GNU Lesser General Public
//  License along with this library; if not, write to the Free Software
//  Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301 USA
//
/*macro definitions of magnetic pin and LED pin*/
#define HALL_SENSOR 2
#define LED	4//the Grove - LED is connected to D4 of Arduino

void setup()
{
 	pinsInit();
}
 
void loop() 
{
	if(isNearMagnet())//if the hall sensor is near the magnet?
	{
		turnOnLED();
	}
	else
	{
		turnOffLED();
	}
}
void pinsInit()
{
	pinMode(HALL_SENSOR, INPUT);
	pinMode(LED,OUTPUT);
}

/*If the hall sensor is near the magnet whose south pole is facing up, */
/*it will return ture, otherwise it will return false.				*/
boolean isNearMagnet()
{
	int sensorValue = digitalRead(HALL_SENSOR);
	if(sensorValue == LOW)//if the sensor value is LOW?
	{
		return true;//yes,return ture
	}
	else
	{
		return false;//no,return false
	}
}
void turnOnLED()
{
	digitalWrite(LED,HIGH);
}
void turnOffLED()
{
	digitalWrite(LED,LOW);
}
```

- **Langkah 4.**  Ketika magnet yang kutub selatannya menghadap ke atas mendekati sensor onboard, LED akan menyala. Jika tidak, LED akan padam.

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan sensor Grove - Hall ke port D2, dan hubungkan Grove - Red LED ke port D4 dari Base Shield.

**Langkah 2.** Pasang modul Base Shield ke modul Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/img/cc_Hall_Sensor.png)

Upload (unggah) program ke modul Arduino/Seeeduino.

!!!Sukses
    Ketika kode selesai diupload (unggah), LED akan menyala saat Hall Sensor mendeteksi perubahan medan magnet.

## Sumber-sumber

- **[Eagle]** [Grove-Hall Sensor Schematic](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Twig_Hall_Sensor_v0.9b.zip)

- **[Demo]** [Hall Sensor Demo Code](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Grove-Hall_Sensor_Demo_Code.zip)

- **[Datasheet]** [A1101 datasheet](http://www.allegromicro.com/en/Products/Part_Numbers/1101/1101.pdf)

- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove-Hall_Sensor/master/res/Grove_Hall_Sensor_CDC_File.zip)


<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_Hall_Sensor -->

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>