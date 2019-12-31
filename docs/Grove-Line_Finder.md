---
name: Grove - Line Finder
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html
oldwikiname: Grove - Line Finder
prodimagename: Grovelinefinder1.jpg
surveyurl: https://www.research.net/r/grove-line-finder
sku: 101020009
---


![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/images/Grovelinefinder1.jpg)

Grove-Line finder dirancang untuk robot yang mengikuti garis. Modul ini memiliki LED IR yang memancarkan cahaya dan phototransistor yang sensitif terhadap IR. Modul ini dapat menampilkan sinyal digital ke mikrokontroler sehingga robot dapat mengikuti garis hitam pada latar belakang putih, atau sebaliknya.

[![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/images/300px-Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html)

## Versi


| Versi Produk              | Perubahan                                                                                                                                                                                    | Tanggal Rilis |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Grove-Line Finder V1.0| Initial                                                                                                                                                                                    | Jan 29 2010      |
| Grove-Line Finder V1.1 | Add test points                                                                                                                                                                                 | Dec 28 2015      |


## Spesifikasi

| Parameter              | Value/Range                                                   |
|------------------------|---------------------------------------------------------------|
| Sumber Daya           | 5                                                             |
| Digital output mode    | TTL (Berlogika High ketika mendeteksi hitam, berlogika Low ketika mendeteksi putih) |
| Konektor              | 4 pin Buckled Grove interface                                 |
| Ukuran             | 20mm*20mm                                                     |
| ROHS                   | Yes                                                           |
| Photo reflective diode | RS-06WD                                                       |
| Komparator             | MV358                                                         |

!!!Tip
    Rincian lebih detail tentang modul Grove silakan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)


## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


##  Memulai

### Bermain dengan Arduino

#### Perangkat Keras

- Langkah 1. Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Button |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/line_finder_s.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html)|

- Langkah 2. Hubungkan Grove-line finder ke port D3 pada Grove-Base Shield.
- Langkah 3. Pasang Grove - Base Shield ke Seeeduino.
- Langkah 4. Hubungkan Seeeduino ke PC menggunakan kabel USB.


![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/seeeduino_line_finder.jpg)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan modul ini ke Seeeduino seperti dibawah ini.

| Seeeduino       | Grove-Line finder |
|---------------|-------------------------|
| 5V           | Merah                     |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D3            | Kuning                  |

#### Software (Perangkat Lunak)

- Langkah 1. Salin kode ke Arduino IDE dan upload (unggah).

```c
//------------------------------------------------------------
//Name: Line finder digital mode
//Function: detect black line or white line
//Parameter:   When digital signal is HIGH, black line
//             When digital signal is LOW, white line
//-------------------------------------------------------------
int signalPin =  3;    // connected to digital pin 3
void setup()   {
  pinMode(signalPin, INPUT); // initialize the digital pin as an output:
  Serial.begin(9600);  // initialize serial communications at 9600 bps:
}
// the loop() method runs over and over again,
// as long as the Arduino has power
void loop()
{
  if(HIGH == digitalRead(signalPin))
    Serial.println("black");
  else  Serial.println("white");  // display the color
  delay(1000);                  // wait for a second
}
```

- Langkah 2. Buka port serial dan kita akan melihat port serial bertuliskan "hitam" ketika sensor diletakkan pada garis hitam dan tulisan "white" pada area putih. 

```
white
white
white
black
black
black
black
black
```

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan a Grove - Line Finder ke port D3 dari modul Base Shield.

**Langkah 2.** Pasangkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Line_Finder/master/img/cc_Line_Finder.png)

Upload (unggah) program ke modul Arduino/Seeeduino.

!!!Sukses
    Ketika kode selesai di-upload (unggah), Anda akan melihat garis ditemukan atau tidak pada Serial Monitor.

### Bermain dengan Raspberry Pi

#### Hardware (Perangkat Keras)

- Langkah 1. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | GrovePi_Plus | Grove - Line Finder |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/line_finder_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Line-Finder-v1.1-p-2712.html)|

- Langkah 2. Pasangkan modul GrovePi_Plus ke Raspberry Pi.
- Langkah 3. Hubungkan Grove-Line Finder ke port D7 dari modul GrovePi_Plus.
- Langkah 4. Hubungkan modul Raspberry Pi ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/img/rasp_line_finder.jpg)

#### Software (Perangkat Lunak)

- Langkah 1. Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk mengonfigurasi pengembangan proyek.
- Langkah 2. Download (unduh) file pada Github repository menggunakan kode berikut.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```
- Langkah 3. Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd ~/GrovePi/Software/Python
python grove_line_finder.py
```

Ini adalah kode grove_line_finder.py.

```python
import time
import grovepi

# Connect the Grove Line Finder to digital port D7
# SIG,NC,VCC,GND
line_finder = 7

grovepi.pinMode(line_finder,"INPUT")

while True:
    try:
        # Return HIGH when black line is detected, and LOW when white line is detected
        if grovepi.digitalRead(line_finder) == 1:
            print ("black line detected")
        else:
            print ("white line detected")

        time.sleep(.5)

    except IOError:
        print ("Error")
```

- Langkah 4. Kita akan melihat garis hitam terdeteksi ketika sensor berada di atas garis hitam.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_line_finder.py 
black line detected
black line detected
white line detected
white line detected

```

## Sumber-sumber

- **[Eagle&PDF]** [Grove-Line Finder Schematic V1.0](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/res/202000970_Grove%20-%20Line%20Finder%EF%BC%88CN%EF%BC%89%20v1.0.zip)
- **[Eagle&PDF]** [Grove-Line Finder Schematic V1.1](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/res/202000932_Grove%20-%20Line%20Finder%20v1.1.zip)
- **[Datasheet]** [LMV358.PDF](https://github.com/SeeedDocument/Grove_Line_Finder/raw/master/res/Lmv358.pdf)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Line_Finder/master/res/Grove_Line_Finder_CDC_File.zip)

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>