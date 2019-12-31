---
name: Grove - 3-Axis Digital Accelerometer(±1.5g)
category: Sensor
bzurl: https://seeedstudio.com/Grove-3-Axis-Digital-Accelerometer(±1.5g)-p-765.html
oldwikiname: Grove_-_3-Axis_Digital_Accelerometer(±1.5g)
prodimagename: 3_aix_acc.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/101020039 1.jpg
surveyurl: https://www.research.net/r/Grove-3-Axis_Digital_Accelerometer-1_5g
sku: 101020039
tags: grove_i2c, io_3v3, io_5v, plat_duino, plat_linkit, plat_wio
---

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><div class="center">
<div class="floatnone">
<img src="https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/3_aix_acc.jpg" />
</div>
</div></td>
<td><div class="center">
<div class="floatnone">
<img src="https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Grove-3-Axis_v1.3.jpg" />
</div>
</div></td>
</tr>
<tr class="even">
<td><div style=": center">
Grove - 3-Axis Digital Accelerometer v1.2
</div></td>
<td><div style=": center">
Grove - 3-Axis Digital Accelerometer v1.2b
</div></td>
</tr>
</tbody>
</table>

3-Axis Digital Accelerometer adalah bagian penting dalam proyek-proyek seperti deteksi orientasi, deteksi gerakan dan deteksi motion. 3-Axis Digital Accelerometer (± 1.5g) ini didasarkan pada modul Freescale, MMA7660FC dengan konsumsi daya rendah. Modul ini memiliki fitur hingga 10.000g survivabilitas getaran tinggi dan Sampel yang dapat dikonfigurasi per tingkat Kedua. Untuk aplikasi yang sederhana yang tidak memerlukan rentang pengukuran terlalu besar, ini adalah pilihan yang bagus karena tahan lama, hemat energi, dan hemat biaya.


[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-3-Axis-Digital-Accelerometer(%C2%B11.5g)-p-765.html)


Spesifikasi
--------------

-   Tegangan kerja: 3.0 - 5.5V
-   Arus saat Mode Off: 0.4μA
-   Arus saat Mode Standby: 2μA
-   Arus saat Mode Aktif: 47 μA at 1 ODR
-   Rentang Tes: ±1.5g
-   Sensitivitas: 21LSB/g
-   Kompatibel dengan library Suli

!!!Tips
    Detail lebih lanjut tentang modul Grove silakan merujuk [Grove System](http://wiki.seeedstudio.com/Grove_System/)

Platform yang Didukung
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.



Demonstrasi
-------------

### Dengan [Arduino](/Arduino "Arduino")

Di sini kami akan menunjukkan kepada Anda cara mendapatkan raw data dan data diukur dengan satuan "g" oleh sensor ini.

Hubungkan modul ini ke port I2C dari Grove - Base Shiel d melalui Grove cable.

<div class="admonition note">
<p class="admonition-title">*Catatan</p>
Jika Anda ingin mengaktifkan fungsi Interrupt dari modul ini, Anda perlu menghubungkan pad solder INT yang kami pisah di papan dengan pin Arduino yang mampu mendeteksi ISR (Interrupt Service Routine).
</div>

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Digital_Accelerometer_Sensor_Connector1.5g.jpg)

Instal library yang kami sediakan di bagian [Sumber](/Grove-3-Axis_Digital_Accelerometer-1.5g#resources).

Buka kode secara langsung melalui :File -> Example ->DigitalAccelerometer_MMA7660FC ->MMA7660FC_Demo.

Dalam program ini, informasi percepatan dikirim dari sensor ke Seeeduino melalui jalur I2C dan kemudian Seeeduino menampilkannya ke serial monitor.
Buka serial monitor untuk memeriksa hasilnya.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Grove-3-Axis_Digital_Accelerometer-1.5g-.jpg)

Output dari sensor ini terdiri dari dua bagian: data mentah (raw data) dan informasi akselerasi 3-sumbu yang dikonversi menjadi unit gravitasi, "g".


### Dengan Raspberry Pi

1. Anda perlu memiliki raspberry pi dan grovepi atau grovepi+.

2. Anda seharusnya sudah selesai mengkonfigurasi lingkungan pengembangan (Development Enviroment), jika belum ikuti langkahnya [disini](/GrovePi_Plus).

3. Koneksi

-   Hubungkan sensor ke soket grovepi i2c-x (1 ~ 3) dengan menggunakan grove cable.

4. Berpindah ke direktori demo:

       cd yourpath/GrovePi/Software/Python/

-   Untuk melihat kodenya

```
    nano grove_i2c_accelerometer.py   # "Ctrl+x" to exit #
```
```
    import time
    import grovepi

    # Hubungkan Grove Accelerometer (+/- 1.5g) ke salah satu port I2C contoh I2C-1
    # Perangkat akan dikenali dengan alamt I2C 0x4c
    # SCL,SDA,VCC,GND

    while True:
        try:
            print grovepi.acc_xyz()
            time.sleep(.5)

        except IOError:
            print "Error"
```

5. Jalankan demo.
```
    sudo python grove_i2c_accelerometer.py
```

Referensi
---------

Di bawah ini adalah dua figur yang membantu Anda memahami makna fisik dari hasil pengukuran.

Gambar pertama adalah tentang arah masing-masing sumbu :
![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/MMA7660_Direction.jpg)

Gambar kedua memberikan beberapa contoh :

![](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/img/Sensing_Direction_1.jpg)

Sumber-sumber
---------

-   [Datasheet of MMA7660FC](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/res/MMA7660FC.pdf)
-   [Grove - 3-Axis Digital Accelerometer Eagle File](https://raw.githubusercontent.com/SeeedDocument/Grove-3-Axis_Digital_Accelerometer-1.5g/master/res/Grove-3-Axis_Digital_Accelerometer-1.5g-Eagle_File.zip)
-   [github repository for 3-Axis Digital Accelerometer(±1.5g)](https://github.com/Seeed-Studio/Accelerometer_MMA7660)


## Proyek

**Tilt Activated Spinning Fan Light Stick*** Stik warna LED portabel bereaksi terhadap pola gerakan yang bergetar. Dengan kipas ekstra dan alarm.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/chuartdo/tilt-activated-spinning-fan-light-stick-e05cec/embed' width='350'></iframe>

**Lean Green RC Sailing Machine**
Perangkat yang tersambung ke internet yang mengontrol perubahan data servo dan mengirim data sensor (GPS / gyro / accel / kompas) secara real time melalui GSM.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/anemoi/lean-green-rc-sailing-machine-2cdde5/embed' width='350'></iframe>

<!-- This Markdown file was created from http://www.seeedstudio.com/wiki/Grove_-_3-Axis_Digital_Accelerometer(±1.5g) -->

## Tech Support / Bantuan
Harap jangan ragu untuk mengirim masukan masalah kepada kami melalui  [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>