---
name: Grove Base Kit for Raspberry Pi
category: Others
bzurl:  
oldwikiname:  
prodimagename:
surveyurl: 
sku: 110020169
---


## SISTEM GROVE

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/groveSystem.png)

Grove merupakan sistem prototip berbentuk modul yang terdiri dari base unit dan berbagai macam modul tambahan yang dilengkapi dengan konektor standar. Base unit merupakan mikroprosesor seperti pada umumnya yang memungkinkan untuk menghubungkan, memproses, dan mengontrol input maupun output dari modul Grove. Setiap modul Grove mempunyai satu fungsi utama, mulai dari tombol sederhana hingga sistem yang lebih kompleks seperti sensor detak jantung. Konektor standar Grove yang dirancang memungkinkan pengguna menjadi lebih mudah dalam merakit atau membongkar modul jika dibandingkan dengan menggunakan kabel atau solder. Hal tersebut membuat sistem pembelajaran pada saat bereksperimen, pengembangan sistem, maupun merancang prototip menggunakan Grove menjadi lebih sederhana.
Grove juga menyediakan Grove to Pin Header Converter atau Grove Base HAT yang dapat digunakan bagi para pengguna yang ingin menggunakan modul sensor dan aktuator milik Grove tanpa disertai development board milik Grove.

Pengguna sistem Grove setidaknya perlu memiliki beberapa pengetahuan elektronika dasar. Jika tidak, pengguna harus mengikuti panduan dasar ini untuk mempelajari beberapa operasi dasar pada sistem Grove. Bagian pertama dari panduan ini terdiri dari daftar informasi dasar tentang komponen yang terdapat dalam starter kit, kemudian diikuti dengan pengaturan dasar Arduino IDE untuk Seeeduino Lotus. Selain itu, terdapat pula 11 sesi panduan berisi operasi dasar pada masing-masing komponen dalam starter kit dan aplikasi yang menggabungkan beberapa modul secara bersamaan. Hal tersebut dapat memberikan pengguna beberapa wawasan dan pengetahuan dasar tentang cara menghubungkan dan memprogram sistem Grove.

## KIT GROVE BASE UNTUK RASPBERRY PI

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/kit.jpg)

Grove start kit berisi satu Grove Base Hat (untuk Raspberry Pi) dan 10 modul Grove. Informasi terperinci tercantum pada penjelasan di bawah ini.

### Perincian Produk

#### Grove Base Hat

**[Grove Base Hat untuk Raspberry Pi](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/BaseHat.jpg)

Saat ini, sensor, aktuator, dan layar grove telah tumbuh menjadi keluarga besar. Kedepannya akan semakin banyak modul Grove yang bergabung dengan ekosistem Grove di masa depan. Kami melihat Grove dapat membantu para pengembang, teknisi, guru, siswa, dan bahkan seniman untuk mengembangkan, membuat, dan merealisasikan sebuah sistem. Kami selalu merasa hal ini merupakan tanggung jawab kami untuk membuat modul Grove menjadi lebih kompatibel dengan banyak platform. Oleh karena itu, pada saat ini kami telah menyediakan modul Grove Base Hat untuk Raspberry Pi dan Grove Base Hat untuk Raspberry Pi Zero. Dengan kata lain, kami telah menyediakan Raspberry Pi the Grove System.

Grove Base Hat untuk Raspberry Pi menyediakan port Digital / Analog / I2C / PWM / UART untuk memenuhi semua kebutuhan Anda. Selain itu, terdapat pula built-in MCU dan ADC 12-bit 8-channel yang tersedia juga untuk Raspberry Pi.


**Fitur**

- Support Raspberry 2/3B/3B+/Zero
- build-in MCU
- 12-bit ADC
- Multi-type Grove port


**Gambaran Perangkat Keras**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/pi_pinout.jpg)

GPIO: Pin out yang sama dengan Raspberry Pi.

PWM ：Port PWM terhubung ke GPIO/BCM pin12 (PWM0) dan GPIO/BCM pin13 (PWM1), yang merupakan pin PWM perangkat keras Raspberry Pi. Selain itu, Anda juga dapat menggunakan semua pin GPIO sebagai pin soft PWM.


!!!Catatan
  - Semua nomor pin yang terdapat pada lapisan silkscreen selain port Grove adalah nomor pin BCM. Perbedaan antara pin BCM dan pin fisik dapat dilihat [di sini](https://www.raspberrypi.org/forums/viewtopic.php?p=726435)
	
  - Dibandingkan dengan perangkat keras PWM, perangkat lunak PWM tidak terlalu akurat dan akan mengalami masalah pada frekuensi tinggi.

  - GPIO / BCM pin18 juga ditandai sebagai PWM0, sebenarnya GPIO / BCM 12 dan GPIO / BCM 18 berbagi saluran PWM yang sama, sehingga tidak dapat mengatur pada rate yang berbeda.

  - Output jack audio juga menggunakan PWM 0 dan PWM 1, sehingga Anda tidak dapat menggunakan output audio dan menggunakan PWM di soket tersebut secara bersamaan.

UART: Port Grove UART terhubung ke GPIO14 (UART0 TX) dan GPIO15 (UART0 RX). UART umumnya digunakan pada Raspberry Pi sebagai cara mudah untuk mengontrolnya pada GPIO, atau mengakses pesan-pesan boot kernel dari konsol serial (diaktifkan secara default). Selain itu, juga dapat digunakan sebagai cara untuk mengaantarmukakan Arduino, bootloaded ATmega, ESP8266, dll dengan Raspberry Pi Anda.

Digital: Board ini mempunyai 6 soket digital Grove yang biasanya menggunakan kabel berwarna kuning (yang terhubung ke pin atas dari 4 pin soket Grove). Kabel Grove adalah kabel sinyal, jadi kami menamakan port digital Grove D5/D16/D18/D22/D24/D26.

Analog ： Seperti yang kita ketahui bahwa Raspberry Pi tidak dapat bekerja dengan sensor analog secara langsung karena tidak memiliki pin ADC. Saat ini, Grove Base Hat telah dilengkapi dengan ADC eksternal 12-bit menggunakan IC MCU STM32 yang berarti Anda dapat menghubungkan sensor analog pada Raspberry Pi Anda. Yang lebih menyenangkan adalah tidak hanya satu tetapi tersedia empat soket analog Grove. Sensor analog mengirimkan tegangan analog ke dalam ADC 12-bit. Setelah itu, ADC akan mengonversi data analog menjadi data digital kemudian ADC memasukkan data digital ke Raspberry Pi melalui antarmuka I2C.

I2C: Terdapat tiga port I2C yang tersedia pada board ini dimana semua port terhubung ke pin I2C dari Raspberry Pi secara langsung. Port ini dapat dianggap sebagai bagian dari hub I2C. Sebagian besar modul Seeed Grove yang baru telah memiliki antarmuka I2C yang dapat berguna dalam membangun sebuah sistem.

SWD ： Kami menggunakan port SWD untuk menuliskan firmware pada modul Base Hat. Selain itu, Anda dapat melihat 3 pin GPIO di bagian ini (pin 9 / pin 10 / pin 11), ketiga pin tersebut tidak digunakan oleh port Grove apa pun sehingga Anda bebas untuk menggunakannya tanpa khawatir tentang pin yang konflik.


#### Modul Grove


**[Grove - Buzzer](https://www.seeedstudio.com/Grove-Buzzer-p-768.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/buzzer.jpg)

Modul ini menggunakan buzzer piezo sebagai komponen utama, buzzer tersebut dapat menghasilkan nada nada tinggi saat terhubung ke output digital dan ketika level logika diatur ke High. Selain itu juga dapat menghasilkan berbagai nada sesuai dengan frekuensi yang dihasilkan dari output PWM Analog yang terhubung dengannya. (catatan: rentang frekuensi yang dapat dibedakan oleh telinga manusia yang normal antara 20 Hz dan 20kHz.)


**[Grove - Red LED Button](https://www.seeedstudio.com/Grove-Red-LED-Button-p-3096.html)**



![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/LEDButton.jpg)

Grove - LED Button terdiri dari Grove - Yellow Button, Grove - Blue LED Button dan Grove - Red LED Button. Tombol ini dapat berfungsi hingga 100.000 kali penekanan. Selain itu, tombol ini juga dilengkapi dengan LED yang sangat berguna untuk menunjukkan status tombol dan dapat diterapkan pada banyak proyek yang menarik.

**[Grove - Light Sensor](https://www.seeedstudio.com/Grove-Light-Sensor-v1-2-p-2727.html)**


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lightsensor.jpg)

Grove - Light sensor mengintegrasikan photo-resistor (resistor bergantung pada cahaya) untuk mendeteksi intensitas cahaya. Resistansi Photo-resistor akan berkurang ketika intensitas cahaya meningkat. Chip opAmp LM358 pada board menghasilkan tegangan yang sesuai dengan intensitas cahaya (berdasarkan nilai resistansi). Sensor ini akan mengeluarkan sinyal output berupa nilai analog. Jika semakin terang cahayanya, maka semakin besar nilai outputnya.

**[Grove - Moisture Sensor](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/Moisture_sensor.jpg)

Moisture Sensor ini dapat digunakan untuk mendeteksi kelembaban tanah atau mengukur kandungan air di sekitar sensor. Sensor ini sangat mudah digunakan karena cukup dengan memasukkan sensor ke dalam tanah dan membaca datanya. Dengan sensor ini, Anda dapat membuat proyek kecil yang dapat mengirimkan pesan kepada Anda seperti "Saya belum disiram, tolong beri saya air sekarang."

**[Grove - mini PIR motion sensor](https://www.seeedstudio.com/Grove-mini-PIR-motion-sensor-p-2930.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/miniPIR.jpg)

Grove - mini PIR motion sensor memungkinkan untuk mendeteksi adanya gerakan, biasanya gerakan manusia selama masih dalam jangkauan sensor. Cukup sambungkan ke Grove - Base shield dan memprogramnya, ketika ada yang bergerak dalam jangkauan pendeteksiannya, sensor akan mengeluarkan logika HIGH pada pin SIG-nya.

**[Grove - Servo](https://www.seeedstudio.com/Grove-Servo-p-1241.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/Servo.jpg)

Grove - Servo adalah motor DC dengan sistem gearing dan sistem umpan balik. Alat ini digunakan dalam mekanisme robot. Modul ini adalah produk bonus untuk pecinta Grove. Kami mengatur servo tiga kabel menjadi konektor standar Grove. Anda dapat mencolokkan dan memainkannya sebagai modul Grove tanpa kabel jumper yang berantakan.

**[Grove - Temperature & Humidity Sensor / Sensor Suhu dan kelembaban （DHT11）](https://www.seeedstudio.com/Grove-Temperature-Humidity-Sensor-DHT1-p-745.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/DHT11.jpg)

Temperature & Humidity Sensor menghasilkan output digital pra-kalibrasi. Sensor ini memiliki elemen uni berupa sensor kapasitif yang akan mengukur suhu dan kelembaban menggunakan Negative Temperature Coefficient (NTC). Alat ini memiliki keandalan yang sangat baik dan stabilitas jangka panjang. Harap dicatat bahwa sensor ini tidak akan berfungsi untuk suhu di bawah 0 derajat.

**[Grove - Relay](https://www.seeedstudio.com/Grove-Relay-p-769.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/Relay.jpg)

Grove - Modul Relay adalah sakelar digital Normally-Open. Melalui modul ini, Anda dapat mengontrol rangkaian tegangan tinggi dengan tegangan rendah, misalnya 5V pada pengontrol. Terdapat LED indikator pada papan yang akan menyala ketika terminal yang dikontrol tertutup.

**[Grove - Ultrasonic Ranger](https://www.seeedstudio.com/Grove-Ultrasonic-Ranger-p-960.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/Ultrasonic.jpg)

Grove - Ultrasonic ranger adalah modul pengukuran jarak non-kontak yang bekerja pada frekuensi 40KHz. Ketika kita memberikan sinyal pemicu pulsa dengan lebih dari 10uS melalui pin sinyal, Grove_Ultrasonic_Ranger akan mengeluarkan 8 siklus dari tingkat siklus 40kHz dan mendeteksi gemanya. Lebar pulsa sinyal gema sebanding dengan jarak yang diukur. Berikut adalah rumusnya: Jarak = lama waktu sinyal gema High * Kecepatan suara (340 m/s) / 2. Sinyal Trig dan echo berbagi 1 SIG pin Grove_Ultrasonic_Ranger.

**[Grove - 16 x 2 LCD (White on Blue)](https://www.seeedstudio.com/Grove-16-x-2-LCD-White-on-Blu-p-3196.html)**

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lcd.jpg)

Modul LCD Grove-162 ini adalah layar LCD 16 Karakter 2 Baris yang menggunakan antarmuka bus I2C untuk berkomunikasi dengan board pengembangan, sehingga ini akan mengurangi pin header dari 10 menjadi 2 yang sangat nyaman untuk sistem Grove. Modul layar LCD ini juga mendukung karakter khusus, Anda dapat membuat dan menampilkan simbol hati atau stick-man pada modul LCD ini melalui konfigurasi kode program yang sederhana.

## PERSIAPAN AWAL 

### Persyaratan Minimum

- Kabel Micro USB
- Raspberry Pi
- Kartu SD
- Grove Base Kit untuk Raspberry Pi

### Panduan Dasar 

#### Pengaturan Dasar Arduino IDE

#### Cara menuliskan img Raspbian

**1. Mengunduh Raspbian Stretch**

Unduh [Raspbian Stretch](https://www.raspberrypi.org/downloads/raspbian/) dari situs web resmi Raspberry Pi lalu pilih versi "with desktop and recommended software".

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss0.png)

**2. Win32 Disk Imager**

- Download (unduh) [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/) dari halaman Sourceforge Project sebagai file pemasang, dan jalankan untuk memasang perangkat lunak.

- Masukkan kartu SD ke pembaca kartu SD Anda lalu sambungkan ke PC Anda.

- Jalankan Win32DiskImager dari desktop atau menu Anda.

- Di dalam kotak perangkat, pilih huruf drive kartu SD yang sesuai. Hati-hati memilih drive yang benar: jika Anda memilih drive yang salah, Anda dapat menghancurkan data di hard disk komputer Anda! Jika Anda menggunakan slot kartu SD di komputer Anda, dan tidak dapat melihat drive di jendela Win32DiskImager, coba gunakan adaptor SD eksternal.	

- Klik 'Write' dan tunggu hingga proses penulisan selesai.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss1.png)

- Selesai.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss2.png)

- Tutup imager dan keluarkan kartu SD 

#### Pengaturan Dasar

**Koneksi Tanpa Kabel dan SSH**

**1.** Buat file bernama "wpa_supplicant.conf" ke dalam folder /boot, dan salin kode berikut.


```txt
country=CN
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
 
network={
ssid="WiFi-name"
psk="WiFi-password"
key_mgmt=WPA-PSK
priority=1
}
```

!!!Catatan
```
Nama ("WiFi-name") dan kata sandi ("WiFi-password") Wi-Fi harus sama dengan Wi-Fi lokal tempat PC Anda terhubung (pastikan PC dan Raspberry Pi Anda berada di LAN yang sama).
```

**2.** Buat file kosong bernama "ssh" ke dalam folder/boot.

**3.** Masukkan Kartu SD dengan Raspbian ke dalam Raspberry Pi.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/sd_card.jpg)

**4.** Hubungkan Raspberry Pi ke sumber daya lalu hidupkan. 

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/power.jpg)

**5.** Buka aplikasi Putty untuk menghubungkan PC ke Raspberry Pi

Unduh putty： [https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss3.png)


**Raspberry Pi**

Default username : pi

Default password : raspberry

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss4.jpg)

**VNC Configuration**

**1.** Buka raspi-config dengan mengetik perintah berikut di terminal.

```bash
sudo raspi-config
```

Arahkan ke bawah hingga Opsi '5 interfacing Options' dan tekan "enter" untuk memilih.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss5.png)

Arahkan ke bawah hingga opsi 'P3 VNC' dan tekan "enter" untuk memilih.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss6.png)

Pilih "Yes" untuk mengaktifkannya.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss7.png)

Pilih "Ok".

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss8.png)

**2.** Pasang VNC Viewer

Unduh [VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss9.png)

Buka VNC Viewer dan masukkan alamat IP Raspberry Pi. Anda dapat menemukan alamat IP dengan mengetik perintah ++ifconfig++ di terminal Raspberry Pi (atau Anda dapat memasukkan raspberrypi.local)

!!!Catatan

		Jika Anda menggunakan raspberrypi.local untuk login Pi Anda, Anda harus memastikan hanya ada satu Raspberry Pi yang digunakan di LAN Anda.

Masukkan nama pengguna dan kata sandi default, dan sekarang Anda dapat memasuki desktop Raspberry Pi dengan jarak jauh!


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss10.png)

Sukses!

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss11.PNG)

**Pengaturan Base Hat**

**1.** Matikan Raspberry Pi

```bash
sudo shutdown -h now
```


Colokkan Grove Base Hat untuk Raspberry Pi ke Raspberry Pi.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/pi&hat.jpg)

**2.** Nyalakan Raspberry Pi dengan kabel micro-usb untuk mengaktifkan I2C

Buka raspi-config dengan mengetik perintah berikut di terminal.

```bash
sudo raspi-config
```

Arahkan ke bawah ke "5 interfacing Options" dan tekan "enter" untuk memilih.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss5.png)

Arahkan ke bawah ke P5 I2C dan tekan "enter" untuk memilih.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss13.png)

Pilih "Ya" untuk mengaktifkannya.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss14.png)

Pilih "ok".

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss15.png)

Pilih "Selesai" untuk menyimpan perubahan.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss16.png)

**3.** Instalasi satu-klik, apa pun yang Anda panggil, dengan satu perintah di bawah ini.

```bash
curl -sL https://github.com/Seeed-Studio/grove.py/raw/master/install.sh | sudo bash -s -
```

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ss12.PNG)

jika semuanya berjalan dengan baik, Anda akan melihat pemberitahuan berikut.

```bash
Successfully installed grove.py-0.6
#######################################################
Lastest Grove.py from github install complete   !!!!!
#######################################################
```

**4.** Selain instalasi satu klik, Anda juga bisa [install all the dependencies](https://github.com/Seeed-Studio/grove.py#installation).

                            
**5.** Gandakan repository library python.py terbaru.

```bash
git clone https://github.com/Seeed-Studio/grove.py
```


### Grove – demo LED button

Setelah semua pengaturan dasar Raspberry Pi telah dilakukan, sekarang kita dapat menjalankan kode demo LED. Catatan: Anda harus menyelesaikan langkah-langkah di atas terlebih dahulu untuk melanjutkan yang berikut ini.


**Koneksi Perangkat Keras**

Langkah 1: Hubungkan Grove - Red LED Button ke port D5 Base Hat

Langkah 2: Pasang Base Hat ke Raspberry Pi

Langkah 3: Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB.

![](![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/LEDbutton.png)
	
**Unggah Kode**

Langkah 1: Jalankan perintah berikut untuk membuat file python


```bash
cd grove.py
nano example.py
```

Langkah 2: Salin kode berikut dalam file python

!!!Peringatan
	
	Harap pastikan editor teks dalam format unix.


```python
#!/usr/bin/env python

import time
from grove.grove_ryb_led_button import GroveLedButton

def main():
    ledbtn = GroveLedButton(5)
    
    while True:
        ledbtn.led.light(True)
        time.sleep(1)
        
        ledbtn.led.light(False)
        time.sleep(1)

if __name__ == '__main__':
    main()
```

Langkah 3：Jalankan program

```bash
sudo chmod +x  example.py
sudo ./example.py
```

Ketika Anda menekan tombol LED, LED akan berubah ke mode "ON" dan "OFF" jika Anda menekannya lama. Jika Anda menekan tombol LED dua kali maka LED akan berkedip.


```bash
pi@raspberrypi:~/grove.py $ sudo ./example.py
turn on  LED
turn on  LED
turn off LED
turn on  LED
blink    LED
^CTraceback (most recent call last):
  File "./example.py", line 17, in <module>
    main()
  File "./example.py", line 14, in main
    time.sleep(1)
KeyboardInterrupt
pi@raspberrypi:~/grove.py $ 
```

**Penjelasan kode blink**

Dalam python, ketika modul direferensikan satu sama lain, modul yang berbeda memiliki definisi "__main__" yang berbeda, dan hanya ada satu entri setiap program. Pemilihan program entri tergantung pada nilai __name__. "if__name __=='__ main__'" adalah sama dengan, artinya itu adalah masukan emulasi python.


```python
if __name__ == '__main__':
    main()
```

## Grove Base Kit untuk Raspberry Pi

 Sekarang, apakah Anda siap untuk menjelajahi sistem Grove? Kami telah merancang 8 tutorial untuk Anda mulai dengan beberapa modul Grove dasar. Bagian ini akan mengenalkan Anda bagaimana modul dapat digabungkan dan diterapkan dalam aplikasi kehidupan nyata.


###  Prasyarat

Untuk memulai panduan Grove, Anda harus memiliki pengetahuan dasar tentang Raspberry Pi dan bahasa pemrograman Python. Pastikan Anda telah menyelesaikan tutorial pengaturan dasar di atas dengan sukses dan menyelesaikan demo LED Blink serta memastikan seluruhnya bekerja dengan baik antara Raspberry Pi dengan Grove Base Hat.
 

###  Hasil belajar

- Mampu menggunakan Grove Base Hat untuk membangun aplikasi dengan modul Grove.
- Mampu mendemonstrasikan setiap komponen Grove Starter Kit dan memanfaatkan modul yang relevan untuk proyek Anda sendiri setelah panduan ini.
- Mampu mengidentifikasi jenis modul yang termasuk dalam Kit ini dan aplikasinya.
- Memahami perbedaan antara sinyal analog dan digital.


### Pelajaran 1: Buzzer

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/buzzer.jpg)

**Tujuan**	

Mengetahui penggunaan Buzzer untuk menghasilkan suara dan juga mengatur frekuensi tertentu untuk menghasilkan beberapa nada.


**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer


Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove – Buzzer 


**Koneksi perangkat keras**

**Langkah 1.** Gunakan kabel Grove untuk menghubungkan Grove - Buzzer ke port PWM Base Hat dan hubungkan Grove Base Hat dengan Raspberry Pi dengan cara ditumpuk.

**Langkah 2.** Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB. 

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/buzzer&pi.jpg)

**Pemrograman Perangkat lunak**	

!!!Catatan

	Pastikan Anda telah menyalin repository library python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python

```bash
cd grove.py
nano lesson_1.py
```

Langkah 2: Salin kode berikut

```python
#!/usr/bin/env python
import time
from mraa import getGpioLookup
from upm import pyupm_buzzer as upmBuzzer

def main():
    # Grove - Buzzer terhubung ke PWM port
    buzzer = upmBuzzer.Buzzer(getGpioLookup('GPIO12'))
    
    CHORDS = [upmBuzzer.BUZZER_DO, upmBuzzer.BUZZER_RE, upmBuzzer.BUZZER_MI, 
        upmBuzzer.BUZZER_FA, upmBuzzer.BUZZER_SOL, upmBuzzer.BUZZER_LA, 
        upmBuzzer.BUZZER_SI]
    for i in range(0, len(CHORDS)):
        buzzer.playSound(CHORDS[i], 500000)
        time.sleep(0.1)
    
    del buzzer
    print('application exiting...')

if __name__ == '__main__':
    main()
```


Langkah 3：Jalankan program

```bash
sudo chmod +x lesson_1.py
sudo ./lesson_1.py
```

Apabila tidak terdapat kesalahan, perhatikan bahwa Buzzer akan berbunyi "Do Re Mi Fa So La Si".

	

### Pelajaran 2: Red LED Button

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/LEDButton.jpg)


**Tujuan**	

Gunakan Grove - Red LED Button digunakan untuk mengontrol kedipan LED dan Grove - Buzzer digunakan untuk membuat efek suara yang berbeda.

**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer

Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove - Red LED Button
- Grove – Buzzer


**Koneksi perangkat keras**

**Langkah 1.** Gunakan kabel Grove untuk menghubungkan Grove - Buzzer ke port PWM dan Grove - Red LED Button ke D5 dari Base Hat. Kemudian hubungkan Grove Base Hat dengan Raspberry Pi dengan cara ditumpuk.


**Langkah 2.** Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB. 

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/Buzzer&Button.png)

**Pemrograman perangkat lunak**	

!!!Catatan

	Pastikan Anda telah menyalin repository library python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python

```bash
cd grove.py
nano lesson_2.py
```

Langkah 2: Salin kode berikut


```python	
#!/usr/bin/env python

import time
from mraa import getGpioLookup
from upm import pyupm_buzzer as upmBuzzer

from grove.button import Button
from grove.grove_ryb_led_button import GroveLedButton

def main():
    # Grove - LED Button terhubung ke port D5
    button = GroveLedButton(5)
    
    # Grove - Buzzer terhubung ke PWM port
    buzzer = upmBuzzer.Buzzer(getGpioLookup('GPIO12'))
    
    def on_event(index, event, tm):
        if event & Button.EV_SINGLE_CLICK:
            print('single click')
            button.led.light(True)
            buzzer.playSound(upmBuzzer.BUZZER_DO, 500000)
            
        elif event & Button.EV_LONG_PRESS:
            print('long press')
            button.led.light(False)
            buzzer.playSound(upmBuzzer.BUZZER_DO, 1000000)
            
    button.on_event = on_event
    
    while True:
        time.sleep(1)

if __name__ == '__main__':
    main()
```

Langkah 3：Jalankan program

```bash	
sudo chmod +x lesson_2.py
sudo ./lesson_2.py
```

!!!Sukses
        Apabila tidak terdapat kesalahan, ketika tombol LED ditekan dalam waktu lama, LED akan padam dan buzzer akan berbunyi "Do" yang bernada panjang. Sebaliknya, ketika tombol LED ditekan hanya sekali saja, LED akan menyala dan buzzer akan berbunyi "Do" bernada pendek.


```bash
pi@raspberrypi:~/grove.py $ sudo ./lesson_2.py
single click
single click
single click
long press
single click
long press
long press
Traceback (most recent call last):
  File "./lesson2.py", line 34, in <module>
    main()
  File "./lesson2.py", line 31, in main
    time.sleep(1)
KeyboardInterrupt
^Cpi@raspberrypi:~/grove.py $ 
```

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/LED&Buz_demo.jpg)


### Pelajaran 3: Light Sensor

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lightsensor.jpg)


**Tujuan**	

Dalam pelajaran ini, kami akan menunjukkan kepada Anda bagaimana menggunakan Grove - Light Sensor untuk mengontrol Grove - Servo. Dalam hal ini, sudut rotasi servo akan berubah-ubah sesuai dengan nilai intensitas cahaya.

**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer

Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove - Light Sensor
- Grove - Servo

**Koneksi perangkat keras**

**Langkah 1** Hubungkan Grove - Light Sensor ke port A0 dan Grove - Servo ke port PWM.

**Langkah 2** Hubungkan Base Hat ke Raspberry Pi.

**Langkah 3** Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/servo&light.png)


**Pemrograman perangkat lunak**	

!!!Catatan

	Pastikan Anda telah menyalin repository library python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python


```bash
cd grove.py
nano lesson_3.py
```

Langkah 2: Salin kode berikut

```python	
#!/usr/bin/env python

import time

from grove.grove_servo import GroveServo
from grove.grove_light_sensor_v1_2 import GroveLightSensor

def main():
    # Grove - Servo terhubung ke PWM port
    servo = GroveServo(12)

    # Grove - Light Sensor terhubung ke port A0
    sensor = GroveLightSensor(0)

    while True:
        angle = sensor.light * 180 / 1000
        print('light value {}, turn to {} degree.'.format(sensor.light, angle))
        servo.setAngle(angle)

        time.sleep(1)

if __name__ == '__main__':
    main()
```



Langkah 3：Jalankan program


```bash
sudo chmod +x lesson_3.py
sudo ./lesson_3.py
```

Jika semuanya berjalan dengan baik, perubahan intensitas cahaya akan menghasilkan sudut rotasi servo yang berbeda.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/light_on&off.jpg)



```bash
pi@raspberrypi:~/grove.py $ sudo ./lesson_3.py
light value 300, turn to 113 degree.
light value 80, turn to 80 degree.
light value 166, turn to 165 degree.
light value 498, turn to 132 degree.
light value 601, turn to 60 degree.
light value 200, turn to 21 degree.
light value 459, turn to 99 degree.
light value 172, turn to 173 degree.
light value 319, turn to 138 degree.
^CTraceback (most recent call last):
  File "./lesson3.py", line 23, in <module>
    main()
  File "./lesson3.py", line 20, in main
    time.sleep(1)
KeyboardInterrupt
pi@raspberrypi:~/grove.py $ 
```

### Pelajaran 4: Motion Sensor & Relay

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/pir+relay.jpg)


**Tujuan**	

Gunakan Grove - mini PIR motion sensor digunakan untuk mendeteksi adanya gerakan, aktuator akan menyala jika terdapat orang yang datang.

**Persyaratan Perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer

Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove - mini PIR motion sensor
- Grove - Relay

**Koneksi Perangkat keras**

**Langkah 1** Hubungkan Grove - mini PIR motion sensor ke port D5 dan Grove - Relay ke port D16 pada Base Hat.

**Langkah 2** Pasang Base Hat ke Raspberry Pi


**Langkah 3** Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/pir&relay.png)

**Pemrograman perangkat lunak**	

!!!Catatan

	Pastikan Anda telah menyalin library repository python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python

```bash
cd grove.py
nano lesson_4.py
```


Langkah 2: Salin kode berikut

```python	
#!/usr/bin/env python

import time

from grove.grove_mini_pir_motion_sensor import GroveMiniPIRMotionSensor
from grove.grove_relay import GroveRelay

def main():
    # Grove - mini PIR motion sensor terhubung ke port D5
    sensor = GroveMiniPIRMotionSensor(5)
    
    # Grove - Relay terhubung ke port D16
    relay = GroveRelay(16)
    
    def on_detect():
        print('motion detected')
        
        relay.on()
        print('relay on')
        
        time.sleep(1)
        
        relay.off()
        print('relay off')
    
    sensor.on_detect = on_detect
    
    while True:
        time.sleep(1)

if __name__ == '__main__':
    main()
```

Langkah 3：Jalankan program

```bash	
sudo chmod +x lesson_4.py
sudo ./lesson_4.py
```

Jika semuanya berjalan dengan baik, relay akan hidup / mati ketika mendeteksi adanya gerakan.

```bash	
pi@raspberrypi:~/grove.py $ sudo ./lesson_4.py
motion detected
relay on
relay off
motion detected
relay on
relay off
^CTraceback (most recent call last):
  File "./lesson_4.py", line 33, in <module>
    main()
  File "./lesson_4.py", line 30, in main
    time.sleep(1)
KeyboardInterrupt
pi@raspberrypi:~/grove.py $ 
```

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/pir_light.jpg)

### Pelajaran 5: Ultrasonic Sensor & Relay


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ultra+relay.jpg)


**Tujuan**	

Dalam pelajaran ini, kami menggunakan Grove - Ultrasonic Ranger untuk mendeteksi jarak. Apabila seseorang semakin mendekati sensor, maka lampu pada Grove - Relay akan menyala / "ON".


**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer

Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove - Ultrasonic Ranger
- Grove - Relay

**Koneksi Perangkat keras**

**Langkah 1** Hubungkan Grove - Ultrasonic Ranger ke port D5 dan Grove - Relay ke port D16 pada Base Hat.

**Langkah 2** Pasang Base Hat ke Raspberry Pi


**Langkah 3** Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ultra&relay.png)

**Pemrograman perangkat lunak**	

!!!Catatan

	Pastikan Anda telah menyalin library repository python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python

```bash
cd grove.py
nano lesson_5.py
```

Langkah 2: Salin kode berikut

```python	
#!/usr/bin/env python

import time

from grove.grove_relay import GroveRelay
from grove.grove_ultrasonic_ranger import GroveUltrasonicRanger

def main():
    # Grove - Ultrasonic Ranger terhubung ke port D5
    sensor = GroveUltrasonicRanger(5)
    
    # Grove - Relay terhubung ke port D16
    relay = GroveRelay(16)
    
    while True:
        distance = sensor.get_distance()
        print('{} cm'.format(distance))
        
        if distance < 20:
            relay.on()
            print('relay on')
            
            time.sleep(1)
            
            relay.off()
            print('relay off')
            
            continue
        
        time.sleep(1)

if __name__ == '__main__':
    main()
```


Langkah 3：jalankan programnya

```bash
sudo chmod +x lesson_5.py
sudo ./lesson_5.py
```

Jika semuanya berjalan dengan baik, perubahan intensitas cahaya akan menghasilkan sudut rotasi servo yang berbeda.


```bash	
pi@raspberrypi:~/grove.py $ sudo ./lesson_5.py
253.722585481 cm
253.739028141 cm
252.896341784 cm
1.20442489098 cm
relay on
relay off
4.51762100746 cm
relay on
relay off
253.985668051 cm
^CTraceback (most recent call last):
  File "./lesson_5.py", line 34, in <module>
    main()
  File "./lesson_5.py", line 31, in main
    time.sleep(1)
KeyboardInterrupt
pi@raspberrypi:~/grove.py $ 
```

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/ultra_light.jpg)

Sekarang, bandingkan hasil dari pelajaran empat dan pelajaran lima, apakah anda dapat menyebutkan kelebihan dan kekurangan Grove - mini PIR motion sensor dan Grove Ultrasonic Ranger?


### Pelajaran 6:  LCD

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lcd.jpg)


**Tujuan**	

Menggunakan Grove - Layar LCD 16 * 2 untuk menampilkan "Hello World".

**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer

Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove - 16*2 LCD


**Koneksi perangkat keras**

**Langkah 1** Hubungkan Grove - 16 * 2 LCD ke port I2C dari Base Hat.

**Langkah 2** Masukkan Base Hat ke Raspberry Pi.

**Langkah 3** Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/LCD.png)

**Pemrograman perangkat lunak**	

!!!Catatan

	Pastikan Anda telah menyalin repository library python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python


```bash	
cd grove.py
nano lesson_6.py
```

Step 2: Salin kode berikut


```python	
#!/usr/bin/env python

import time

from grove.display.jhd1802 import JHD1802

def main():
    # Grove - 16x2 LCD(White on Blue) terhubung ke I2C port
    lcd = JHD1802()

    lcd.setCursor(0, 0)
    lcd.write('hello, world!!!')

    print('application exiting...')

if __name__ == '__main__':
    main()
```


Langkah 3：jalankan programnya


```bash
sudo chmod +x lesson_6.py
sudo ./lesson_6.py
```

Anda akan melihat "hello, world !!!" yang ditampilkan pada layar LCD.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/helloworld.jpg)


Jika Anda ingin menggunakan Grove - layar LCD 16*2 dapat digunakan untuk menampilkan beberapa karakter lain, Anda cukup mengubah pada baris kode ++lcd.write ('hello, world !!!')++.


### Pelajaran 7: LCD & Temperature and Humidity Sensor


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lcd+dht11.jpg)


**Tujuan**	

Menggunakan Grove - 16*2 Layar LCD untuk menampilkan data (suhu dan kelembaban) dari Grove - Temperature and Humidity Sensor

**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer

Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove - 16*2 LCD
- Grove - Temperature and Humidity sensor

**Koneksi perangkat keras**

**Langkah 1** Hubungkan Grove - 16*2 LCD ke port I2C dan Grove - Temperature and Humidity Sensor ke port D5.

**Langkah 2** Hubungakn Base Hat ke Raspberry Pi.

**Langkah 3** Hubungkan Raspberry Pi ke sumber daya menggunakan kabel micro USB.


![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/DHT11&LCD.png)

**Pemrograman perangkat lunak**	

!!!Catatan

	Pastikan Anda telah menyalin repository library python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python

```bash	
cd grove.py
nano lesson_7.py
```

Langkah 2: Salin kode berikut

```python	
#!/usr/bin/env python

import time

from grove.grove_temperature_humidity_sensor import DHT
from grove.display.jhd1802 import JHD1802

def main():
    # Grove - 16x2 LCD(White on Blue) terhubung ke I2C port
    lcd = JHD1802()

    # Grove - Temperature&Humidity Sensor terhubung ke port D5
    sensor = DHT('11', 5)

    while True:
        humi, temp = sensor.read()
        print('temperature {}C, humidity {}%'.format(temp, humi))

        lcd.setCursor(0, 0)
        lcd.write('temperature: {0:2}C'.format(temp))

        lcd.setCursor(1, 0)
        lcd.write('humidity: {0:5}%'.format(humi))

        time.sleep(1)

if __name__ == '__main__':
    main()
```

Langkah 3：jalankan program

```bash
sudo chmod +x lesson_7.py
sudo ./lesson_7.py
```

Jika semuanya berjalan dengan baik, anda akan melihat nilai suhu dan kelembaban saat ini yang ditampilkan pada layar LCD


```bash
pi@raspberrypi:~/grove.py $ sudo ./lesson_7.py
temperature 23C, humidity 16%
temperature 22C, humidity 17%
temperature 22C, humidity 17%
^CTraceback (most recent call last):
  File "./lesson_7.py", line 28, in <module>
    main()
  File "./lesson_7.py", line 25, in main
    time.sleep(1)
KeyboardInterrupt
pi@raspberrypi:~/grove.py $
```

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/temp&humi_LCD.jpg)


### Pelajaran 8: LCD & Moisture Sensor & Buzzer

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lcd+moisture+buzzer.jpg)

**Tujuan**	

Use Grove - 16 * 2 LCD to display the current moisture level. When the moisture status is "wet", the Grove - Buzzer should alert you. 

**Persyaratan perangkat keras**

Persiapan

- Kabel micro-USB
- Raspberry Pi 3 Model B
- Komputer

Termasuk dalam kit

- Grove Base Hat
- Kabel Grove
- Grove - 16*2 LCD
- Grove - Moisture Sensor
- Grove - Buzzer

**Koneksi perangkat keras**

**Langkah 1** Hubungkan Grove - 16*2 LCD ke port I2C, Grove - Sensor Kelembaban ke port A0 dan Grove - Buzzer ke port PWM dari Grove Base Hat.

**Langkah 2** Masukkan Base Hat ke Raspberry Pi.


**Langkah 3**  Gunakan micro USB untuk menghubungkan Raspberry Pi dengan PC.

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lesson8.png)

**Pemrograman perangkat lunak**	

!!!Catatan

		Pastikan Anda telah menyalin pustaka repositori python.py ke Raspberry Pi Anda.

Langkah 1: Jalankan perintah berikut untuk membuat file python

```bash
cd grove.py
nano lesson_8.py
```

Langkah 2： Salin kode berikut

```python	
#!/usr/bin/env python

import time
from mraa import getGpioLookup
from upm import pyupm_buzzer as upmBuzzer

from grove.grove_moisture_sensor import GroveMoistureSensor
from grove.lcd.sh1107g import JHD1802

def main():
    # Grove - 16x2 LCD(White on Blue) terhubung ke I2C port
    lcd = JHD1802()
    
    # Grove - Moisture Sensor terhubung ke port A0
    sensor = GroveMoistureSensor(0)
    
    # Grove - Buzzer terhubung ke port PWM
    buzzer = upmBuzzer.Buzzer(getGpioLookup('GPIO12'))
    
    while True:
        mois = sensor.moisture
        if 0 <= mois and mois < 300:
            level = 'dry'
        elif 300 <= mois and mois < 600:
            level = 'moist'
        else:
            level = 'wet'
            buzzer.playSound(upmBuzzer.BUZZER_DO, 200000)
        
        print('moisture: {}, {}'.format(mois, level))
        
        lcd.setCursor(0, 0)
        lcd.write('moisture: {0:>6}'.format(mois))
        
        lcd.setCursor(1, 0)
        lcd.write('{0:>16}'.format(level))
        
        time.sleep(1)

if __name__ == '__main__':
    main()
```


Langkah 3：jalankan program

```bash
sudo chmod +x lesson_8.py
sudo ./lesson_8.py
```

Jika semuanya berjalan dengan baik, Anda akan dapat melihat tingkat kelembaban pada layar LCD. Buzzer digunakan untuk mengingatkan orang setelah tingkat kelembaban mencapai "basah".


```bash	
pi@raspberrypi:~/grove.py $ sudo ./lesson_8.py
moisture: 0, dry
moisture: 0, dry
moisture: 396, moist
moisture: 398, moist
moisture: 407, wet
moisture: 418, wet
^CTraceback (most recent call last):
  File "./lesson_8.py", line 41, in <module>
    main()
  File "./lesson_8.py", line 38, in main
    time.sleep(1)
KeyboardInterrupt
pi@raspberrypi:~/grove.py $
```

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Beginner_Kit_for_RaspberryPi/master/img/lesson8.png)

## BANTUAN / TECH SUPPORT

Harap jangan ragu untuk mengirim masukan masalah kepada kami lewat [forum](https://forum.seeedstudio.com/) atau kirim E-Mail ke [techsupport@seeed.cc](techsupport@seeed.cc).<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>