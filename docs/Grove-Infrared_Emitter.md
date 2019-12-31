---
name: Grove - Infrared Emitter
category: Actuator
bzurl: https://seeedstudio.com/Grove-Infrared-Emitter-p-993.html
oldwikiname: Grove_-_Infrared_Emitter
prodimagename: Grove-Infrared_Emitter.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020026 1.jpg
surveyurl: https://www.research.net/r/Grove-Infrared_Emitter
sku: 101020026
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_pi, plat_wio
---

![](https://github.com/SeeedDocument/Grove-Infrared_Emitter/raw/master/img/main.jpg)

Infrared Emitter digunakan untuk mengirimkan sinyal inframerah melalui LED inframerah, sementara di sisi lain terdapat **Infrared receiver** yang digunakan untuk menangkap sinyal inframerah. LED inframerah seperti LED lainnya, dengan warnanya berpusat di sekitar 940nm. Modul ini tidak hanya dapat menggunakan emitor untuk mengirimkan data atau perintah, tetapi juga dapat mengontrol alat rumah Anda menggunakan Arduino dalam jarak jauh. Infrared Emitter dapat mengirimkan sinyal hingga 10 meter. Melampaui 10 meter, penerima mungkin tidak mendapatkan sinyal. Dalam mengembangkan suatu proyek, kami sering menggunakan 2 modul yaitu  [Infrared Receiver](http://wiki.seeedstudio.com/Grove-Infrared_Receiver) dan Grove - Infrared Emitter yang bekerja bersamaan.




<p style=":center"><a href="http://www.seeedstudio.com/Grove-Infrared-Emitter-p-993.html" target="_blank"><img src="https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png" width="210" height="41"  border=0 /></a></p>




## Versi

versi Produk | Perubahan |	Tanggal Dirilis
--|--|--
Grove - Infrared Emitter v1.0	| Initial |	Nov. 01 2015
Grove - Infrared Emitter v1.1	| Change the Infrared transmitting tube location  |	Jul. 24 2016
Grove - Infrared Emitter v1.2	| Change the valnue of C1 to make the power more stable  |	Dec. 14 2016

## Applikasi
- Infrared remote control dengan kebutuhan daya tinggi
- Sistem transmisi free air
- Inframerah untuk penghitung optik dan pembaca kartu

##　Spesifikasi

| Parameter               | Value/Range   |
|-------------------------|---------------|
| Tegangan Operasional       | 3.3/5V        |
| Peak wavelength         | 940nm         |
| Angle of half intensity | ϕ = ± 17°     |
| Radiant Intensity       | 72 mW/sr      |
| Jarak                | 10 meter(MAX) |
| Suhu Operasional   | -40℃ to +80℃  |
| Ukuran                    | 20mmX20mm     |

!!!Tip
    Rincian lebih detail tentang modul Grove silakan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)
    



## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.




## Memulai

Grove - Infrared Emitter dapat mengirim data sementara Grove - Infrared Receiver akan menerimanya.


### Bermain dengan Arduino

!!!Catatan
   Jika ini pertama kalinya Anda menggunakan Arduino, kami sangat menyarankan Anda untuk melihat [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield| Grove - Infrared Emitter | Grove - Infrared Receiver
|--------------|-------------|-----------------|-----|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduinoX2.png)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/baseshiledX2.png)|![enter image description here](https://github.com/SeeedDocument/Grove-Infrared_Emitter/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Infrared_Receiver/raw/master/img/little.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Infrared-Emitter-p-993.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Infrared-Receiver-p-994.html)|

- **Langkah 2.** Hubungkan Grove - Infrared Emitter pada port **D3** dari Grove-Base Shield.
              
- **Langkah 3.** Hubungkan Grove - Infrared Receiver pada port **D2** dari Grove-Base Shield lainnya.

- **Langkah 4.** Pasang Grove - Base Shield ke Seeeduino.

- **Langkah 5.** Hubungkan Seeeduino ke PC menggunakan kabel USB.



![](https://github.com/SeeedDocument/Grove-Infrared_Emitter/raw/master/img/connect.jpg)


!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan modul ini ke Seeeduino seperti dibawah ini.



| Seeeduino       | Grove - Infrared Emitter |
|---------------|-------------------------|
| 5V           | Merah                    |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D3            | Kuning                  |


| Seeeduino       | Grove - Infrared Receiver |
|---------------|-------------------------|
| 5V           | Merah                     |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D2            | Kuning                  |



#### Software (Perangkat Lunak)

- **Langkah 1.** Download (unduh)  [IRSendRev-master library](https://github.com/Seeed-Studio/IRSendRev) dari Github.

- **Langkah 2.** Lihat [How to install library](http://wiki.seeedstudio.com/How_to_install_Arduino_Library) untuk menginstal library untuk Arduino.

- **Langkah 3.** Restart Arduino IDE. Kemudian buka contoh `recv` melalui path ini: **File->Examples->Grove - Infrared Receiver  And Emitter->recv**. 

![](https://github.com/SeeedDocument/Grove-Infrared_Receiver/raw/master/img/path.png)


Atau Anda dapat membuka sketsa baru dan menyalin kode di bawah ini ke IDE Arduino Anda.

```c++

#include <IRSendRev.h>

#define BIT_LEN         0
#define BIT_START_H     1
#define BIT_START_L     2
#define BIT_DATA_H      3
#define BIT_DATA_L      4
#define BIT_DATA_LEN    5
#define BIT_DATA        6

const int pinRecv = 2;              // ir receiver connect to D2

void setup()
{
    Serial.begin(115200);
    IR.Init(pinRecv);
    Serial.println("init over");
}

unsigned char dta[20];

void loop()
{
    if(IR.IsDta())                  // get IR data
    {
        IR.Recv(dta);               // receive data to dta

        Serial.println("+------------------------------------------------------+");
		Serial.print("LEN = ");
        Serial.println(dta[BIT_LEN]);
        Serial.print("START_H: ");
        Serial.print(dta[BIT_START_H]);
        Serial.print("\tSTART_L: ");
        Serial.println(dta[BIT_START_L]);
        
        Serial.print("DATA_H: ");
        Serial.print(dta[BIT_DATA_H]);
        Serial.print("\tDATA_L: ");
        Serial.println(dta[BIT_DATA_L]);
        
        Serial.print("\r\nDATA_LEN = ");
        Serial.println(dta[BIT_DATA_LEN]);
        
		Serial.print("DATA: ");
        for(int i=0; i<dta[BIT_DATA_LEN]; i++)
        {
            Serial.print("0x");
            Serial.print(dta[i+BIT_DATA], HEX);
            Serial.print("\t");
        }
        Serial.println();
		
		Serial.print("DATA: ");
        for(int i=0; i<dta[BIT_DATA_LEN]; i++)
        {
            Serial.print(dta[i+BIT_DATA], DEC);
            Serial.print("\t");
        }
        Serial.println();
        Serial.println("+------------------------------------------------------+\r\n\r\n");
    }
}

```

- **Langkah 4.** Upload (unggah) demo `recv` ke seeeduino yang terhubung dengan Grove - Infrared Receiver. Jika Anda tidak tahu cara mengupload (unggah) kode, silahkan cek [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

- **Langkah 5.** Buka contoh `send` melalui path berikut: **File->Examples->Grove - Infrared Receiver  And Emitter->send**. 

Atau Anda dapat membuka sketsa baru dan menyalin kode di bawah ini ke IDE Arduino Anda.

```
#include <IRSendRev.h>

#define BIT_LEN         0
#define BIT_START_H     1
#define BIT_START_L     2
#define BIT_DATA_H      3
#define BIT_DATA_L      4
#define BIT_DATA_LEN    5
#define BIT_DATA        6

const int ir_freq = 38;                 // 38k

unsigned char dtaSend[20];

void dtaInit()
{
    dtaSend[BIT_LEN]        = 11;			// all data that needs to be sent
    dtaSend[BIT_START_H]    = 179;			// the logic high duration of "Start"
    dtaSend[BIT_START_L]    = 90;			// the logic low duration of "Start"
    dtaSend[BIT_DATA_H]     = 11;			// the logic "long" duration in the communication
    dtaSend[BIT_DATA_L]     = 33;			// the logic "short" duration in the communication
    
    dtaSend[BIT_DATA_LEN]   = 6;			// Number of data which will sent. If the number is other, you should increase or reduce dtaSend[BIT_DATA+x].
    
    dtaSend[BIT_DATA+0]     = 128;			// data that will sent
    dtaSend[BIT_DATA+1]     = 127;
    dtaSend[BIT_DATA+2]     = 192;
    dtaSend[BIT_DATA+3]     = 63;
	dtaSend[BIT_DATA+4]     = 192;
    dtaSend[BIT_DATA+5]     = 63;
}

void setup()
{
    dtaInit();
}

void loop()
{
    IR.Send(dtaSend, 38);
    
    delay(2000);
}


```

- **Langkah 6.** Upload (unggah) demo `send` ke seeeduino yang terhubung dengan Grove - Infrared Emitter. 


- **Langkah 7.** Buka **Serial Monitor** Arduino IDE dengan mengklik **Tool-> Serial Monitor**. Atau tekan tombol ++ctrl+shift+m++ secara bersamaan.


Jika semuanya berjalan dengan baik, hasilnya akan seperti:


![](https://github.com/SeeedDocument/Grove-Infrared_Emitter/raw/master/img/results.png)



## Sumber-sumber

- **[Zip]**  [Grove-Infrared Emitter eagle files](https://raw.githubusercontent.com/SeeedDocument/Grove-Infrared_Emitter/master/res/Grove-Infrared_Emitter_eagle_files.zip)
- **[Lib]**  [IR Send and Receiver Library](https://github.com/Seeed-Studio/IRSendRev)
- **[Pdf]**  [TSAL6200 Datasheet](http://www.vishay.com/docs/81010/tsal6200.pdf)

## Proyek

**Komunikasi IR LaunchPad ke LaunchPad**: Kirim tulisan dari satu LaunchPad ke LaunchPad lainnya menggunakan Grove IR emitter dan receiver!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ctroberts/ir-launchpad-to-launchpad-communication-0dd109/embed' width='350'></iframe>




## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>