---
name: Grove - Buzzer
category: Actuator
bzurl: https://www.seeedstudio.com/Grove-Buzzer-p-768.html
oldwikiname: Grove - Buzzer
prodimagename: Grove%20Buzzer.jpg
surveyurl: https://www.surveymonkey.com/r/grove-buzzer
sku: 107020000
---


![](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/images/Grove%20Buzzer.jpg)

Modul Grove - Buzzer memiliki [piezo buzzer](https://en.wikipedia.org/wiki/Buzzer#Piezoelectric) sebagai komponen utama. Piezo dapat dihubungkan ke output digital dan akan mengeluarkan nada ketika outputnya bernilai HIGH (1). Selain itu dapat juga dihubungkan ke output modulasi lebar pulsa analog atau pulse-width modulation (PWM) untuk menghasilkan berbagai nada dan efek.

[![](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/images/300px-Get_One_Now_Banner.png)](https://www.seeedstudio.com/Grove-Buzzer-p-768.html)

## Versi


| Versi Produk              | Perubahan                                                                                                                                                                                 | Tanggal Dirilis |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| Grove-Buzzer V1.0| Initial                                                                                                                                                                                    | Nov 25 2010      |
| Grove-Buzzer V1.1 | Add S9013 Transistor                                                                                                                                                                                    | May 30 2014      |


## Fitur

- Buzzer piezoelektrik mudah digunakan
- Menggunakan Kabel Grove 4-pin Standar untuk terhubung ke modul Grove lainnya seperti - [Grove Power Modules](/Grove_System/) dan Grove - Base Shield

!!!Tips
    Rincian lebih detail tentang modul Grove silakan melihat [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Spesifikasi

| Parameter           | Nilai         |
|--------------------|---------------|
| Tegangan kerja     | 3.3V/5V       |
| Output suara       | ≥85dB         |
| Frekuensi resonansi| 2300±300Hz    |

## Platform yang didukung


| Arduino                                                                                             | Raspberry Pi                                                                                           | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kecocokan secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam banyak kasus. Dalam hal ini, kami tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


##  Memulai

### Bermain dengan Arduino

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan - peralatan di bawah ini:

| Seeeduino V4.2 | Base Shield|  Grove - Buzzer |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/img/buzzer_s.jpg)|
|[Dapatkan Sekarang](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Buzzer-p-768.html)|

- **Langkah 2.** Hubungkan Grove-Buzzer ke port D6 dari Grove-Base Shield.
- **Langkah 3.** Pasangkan Grove - Base Shield ke Seeeduino.
- **Langkah 4.** Hubungkan Seeeduino ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/img/seeeduino_buzzer.jpg)

!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan Grove-buzzer ke Seeeduino seperti di bawah ini.

| Seeeduino       | Grove-Buzzer |
|---------------|-------------------------|
| 5V           | Merah                     |
| GND           | Hitam                   |
| Not Conencted | Putih                   |
| D6            | Kuning                  |

#### Software (Perangkat Lunak)

- Langkah 1. Salin kode ke Arduino IDE dan upload (unggah).

```c
void setup()
{
  pinMode(6, OUTPUT);
}

void loop()
{
  digitalWrite(6, HIGH);
  delay(1000);
  digitalWrite(6, LOW);
  delay(1000);
}
```

- Langkah 2. Kita akan mendengar bel berbunyi dan mati.

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Hubungkan Grove - Buzzer ke port D6 dari modul Base Shield.

**Langkah 2.** Pasangkan modul Base Shield ke Seeeduino/Arduino.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC menggunakan kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/), add Arduino support, dan drag prosedur utama ke area kerja yang aktif.

!!!Catatan
    Jika ini pertama kalinya Anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Drag blok seperti gambar di bawah ini atau buka file cdc yang dapat di-download (unduh) di akhir halaman ini.

![cc](https://raw.githubusercontent.com/SeeedDocument/Grove_Buzzer/master/img/cc_Buzzer.png)

Upload (unggah) program ke modul Arduino/Seeeduino.

!!!Sukses
    Ketika kode selesai di-upload (unggah), Anda akan mendengar suara bel putus - putus.

### Bermain dengan Raspberry Pi (menggunakan Grove Base Hat untuk Raspberry Pi)

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove -  Buzzer|
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/img/buzzer_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Buzzer-p-768.html)|

- **Langkah 2**. Pasangkan modul Grove Base Hat ke Raspberry Pi.
- **Langkah 3**. Hubungkan modul Grove Buzzer ke port PWM dari modul Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry Pi ke PC menggunakan kabel USB.
![](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/connect1.jpg)


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti langkah [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengonfigurasi pengembangan proyek.
- **Langkah 2**. Download (unduh) file sumber dengan memperbanyak library grove.py. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_pwm_buzzer.py
```


Dibawah ini merupakan kode grove_led.py.

```python

from __future__ import print_function

import time
from mraa import getGpioLookup
from upm import pyupm_buzzer as upmBuzzer

def main():
    print("Insert Grove-Buzzer to Grove-Base-Hat slot PWM[12 13 VCC GND]")

    # Grove Base Hat for Raspberry Pi
    #   PWM JST SLOT - PWM[12 13 VCC GND]
    pin = 12
    #
    # Create the buzzer object using RaspberryPi GPIO12
    mraa_pin = getGpioLookup("GPIO%d" % pin)
    buzzer = upmBuzzer.Buzzer(mraa_pin)

    chords = [upmBuzzer.BUZZER_DO, upmBuzzer.BUZZER_RE, upmBuzzer.BUZZER_MI,
              upmBuzzer.BUZZER_FA, upmBuzzer.BUZZER_SOL, upmBuzzer.BUZZER_LA,
              upmBuzzer.BUZZER_SI];

    # Print sensor name
    print(buzzer.name())

    # Play sound (DO, RE, MI, etc.), pausing for 0.1 seconds between notes
    for chord_ind in range (0,7):
        # play each note for a half second
        print(buzzer.playSound(chords[chord_ind], 500000))
        time.sleep(0.1)

    print("exiting application")

    # Delete the buzzer object
    del buzzer

if __name__ == '__main__':
    main()



```
!!!Sukses
    Jika semuanya berjalan dengan baik, bel akan berdering beberapa kali dan kemudian berhenti. Setelah itu, program akan secara otomatis keluar.
     


### Bermain dengan Raspberry Pi (menggunakan GrovePi_Plus)

#### Hardware (Perangkat Keras)

- **Langkah 1.** Siapkan peralatan dibawah ini:

| Raspberry pi | GrovePi_Plus | Grove - Buzzer |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/img/buzzer_s.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Buzzer-p-768.html)|

- **Langkah 2.** Pasangkan modul GrovePi_Plus ke Raspberry.
- **Langkah 3.** Hubungkan Grove-Buzzer ke port D8 dari GrovePi_Plus.
- **Langkah 4.** Hubungkan modul Raspberry ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/img/rasp_buzzer.jpg)

#### Software (Perangkat Lunak)

- **Langkah 1.** Ikuti langkah [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) untuk kofigurasi pengembangan proyek.
- **Langkah 2.** Download (unduh) kode pada repositori Github.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```
- **Langkah 3.** Jalankan perintah dibawah ini.

```
cd ~/GrovePi/Software/Python
python grove_buzzer.py
```

Here is the grove_buzzer.py code.

```python
import time
import grovepi

# Connect the Grove Buzzer to digital port D8
# SIG,NC,VCC,GND
buzzer = 8

grovepi.pinMode(buzzer,"OUTPUT")

while True:
    try:
        # Buzz for 1 second
        grovepi.digitalWrite(buzzer,1)
        print ('start')
        time.sleep(1)

        # Stop buzzing for 1 second and repeat
        grovepi.digitalWrite(buzzer,0)
        print ('stop')
        time.sleep(1)

    except KeyboardInterrupt:
        grovepi.digitalWrite(buzzer,0)
        break
    except IOError:
        print ("Error")
```

- Langkah 4. Kita akan mendengar bel berbunyi dan kemudian diam.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_buzzer.py
start
stop
start
stop
```


### Bermain dengan TI LaunchPad

#### Hardware (Perangkat Keras)

- Contoh ini menunjukkan cara menggunakan modul Grove buzzer untuk memainkan melodi. Modul ini akan mengirimkan gelombang persegi dari frekuensi yang sesuai ke buzzer sehingga menghasilkan nada yang sesuai.

![](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/images/Buzzer.jpg)

#### Software (Perangkat Lunak)

```c
/*
  Buzzer
 The example use a buzzer to play melodies. It sends a square wave of the
 appropriate frequency to the buzzer, generating the corresponding tone.

 The circuit:
 * Buzzer attached to pin39 (J14 plug on Grove Base BoosterPack)
 * one side pin (either one) to ground
 * the other side pin to VCC
 * LED anode (long leg) attached to RED_LED
 * LED cathode (short leg) attached to ground

 * Note:
 This example code is in the public domain.

 http://www.seeedstudio.com/wiki/index.php?title=GROVE_-_Starter_Kit_v1.1b#Grove_-_Buzzer

*/

/* Macro Define */
#define BUZZER_PIN               39            /* sig pin of the buzzer */

int length = 15;         /* the number of notes */
char notes[] = "ccggaagffeeddc ";
int beats[] = { 1, 1, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 1, 2, 4 };
int tempo = 300;

void setup()
{
    /* set buzzer pin as output */
    pinMode(BUZZER_PIN, OUTPUT);
}

void loop()
{
    for(int i = 0; i < length; i++) {
        if(notes[i] == ' ') {
            delay(beats[i] * tempo);
        } else {
            playNote(notes[i], beats[i] * tempo);
        }
        delay(tempo / 2);    /* delay between notes */
    }

}

/* play tone */
void playTone(int tone, int duration) {
    for (long i = 0; i < duration * 1000L; i += tone * 2) {
        digitalWrite(BUZZER_PIN, HIGH);
        delayMicroseconds(tone);
        digitalWrite(BUZZER_PIN, LOW);
        delayMicroseconds(tone);
    }
}

void playNote(char note, int duration) {
    char names[] = { 'c', 'd', 'e', 'f', 'g', 'a', 'b', 'C' };
    int tones[] = { 1915, 1700, 1519, 1432, 1275, 1136, 1014, 956 };

    // play the tone corresponding to the note name
    for (int i = 0; i < 8; i++) {
        if (names[i] == note) {
            playTone(tones[i], duration);
        }
    }
}
```

## Sumber - Sumber

- **[Eagle&PDF]** [Grove - Buzzer Schematic Files v1.1](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/resources/Grove-Buzzer_V1.1_eagle.zip)
- **[Eagle&PDF]** [Grove - Buzzer Schematic Files v1.0](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/resources/Grove_-_Buzzer_v1.0_Source_File.zip)
- **[DataSheet]** [S9013datasheet](https://github.com/SeeedDocument/Grove_Buzzer/raw/master/resources/S9013.pdf)
- **[More Reading]** [Wooden Laser Gun](http://www.instructables.com/id/DIY-a-Wooden-Laser-Gun-As-a-Xmas-Present-for-Your-/)
- **[Codecraft]** [CDC File](https://raw.githubusercontent.com/SeeedDocument/Grove_Buzzer/master/res/Grove_Buzzer_CDC_File.zip)

![](https://raw.githubusercontent.com/SeeedDocument/Grove_Button/master/img/gun.jpg)

Terinspirasi oleh OVERWATCH, kami telah membuat mainan Wooden Laser Gun yang sangat keren untuk bersenang-senang!

Modul Wooden Laser Gun dan Gun Target Pistol didasarkan pada modul Arduino yang disebut Seeeduino Lotus. Pemancar laser pada Laser Gun dikendalikan untuk memancarkan pulsa laser guna "mengaktifkan" Target Gun. Terdapat 3 sensor cahaya pada Gun Target untuk mendeteksi pulsa laser. Terlihat sangat sederhana bukan? Jika Anda tertarik dengan proyek kami, buatlah satu untuk diri sendiri atau untuk anak Anda! Sangat cocok untuk menghabiskan satu hari DIY sebagai hadiah Natal.    

## Proyek

**Grove - Pengantar dalam Buzzer**: Langkah pertama saya dengan komponen Grove 'plug & play'. Ini terutama Buzzer.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-in-a-buzzer-981efd/embed' width='350'></iframe>

**Water Waste Monitor**: Jutaan galon air terbuang setiap tahun. Belajarlah menghemat air menggunakan proyek ini!

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/exp0nge/water-waste-monitor-98378e/embed' width='350'></iframe>


**Modul Buzzer Grove**:
 
<iframe width="560" height="315" src="https://www.youtube.com/embed/XBqvG6R1ueA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/ug8dJHPmdMA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/).
<br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>