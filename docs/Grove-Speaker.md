---
name: Grove - Speaker
category: Actuator
bzurl: https://seeedstudio.com/Grove-Speaker-p-1445.html
oldwikiname: Grove_-_Speaker
prodimagename: Grove_Speaker_01.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/Grove Speaker.jpg
surveyurl: https://www.research.net/r/Grove-Speaker
sku: 107020001
tags: grove_digital, io_5v, plat_duino, plat_wio
---

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/img/Grove_Speaker_01.jpg)

Grove-Speaker adalah modul yang terdiri dari Power Amplification (penguat daya) dan output suara. kerasnya suara dapat disesuaikan dengan potensiometer yang terpasang pada board. Dengan frekuensi input yang berbeda, loud-speaker (pengeras-suara) dapat menghasilkan nada yang berbeda. Masukkan kode musik ke Arduino, dan Buat kotak musik Anda sendiri!

[![](https://raw.githubusercontent.com/SeeedDocument/common/master/Get_One_Now_Banner.png)](http://www.seeedstudio.com/Grove-Speaker-p-1445.html)

Fitur
-------

-   Pengaturan Volume
-   Grove Interface

!!!Tips

Selengkapnya tentang modul Grove bisa dilihat di [Grove System](http://wiki.seeedstudio.com/Grove_System/)


Spesifikasi
-------------

| Item            | Min | Typical | Max | Unit |
|-----------------|-----|---------|-----|------|
| Working Voltage | 4.0 | 5.0     | 5.5 | VDC  |
| Voltage Gain    | -   | -       | 46  | db   |
| Band Width      | -   | -       | 20  | KHz  |

Platform yang didukung
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Peringatan

    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


Penggunaan
-----

### Bermain dengan Arduino

Speaker dapat memancarkan berbagai suara seperti klakson mobil, bel pintu dan suara kontak (ignition). Suara yang berbeda didasarkan pada frekuensi sinyal input.

Anda dapat menyediakan sinyal frekuensi yang berbeda untuk modul ini dengan Arduino. Arduino menghasilkan sinyal ini melalui PWM atau bahkan melalui fungsi digital write dan delay. Di sini kami akan menunjukkan kepada Anda bagaimana menghasilkan sinyal-sinyal ini menggunakan *delay()*, speaker menghasilkan suara bass 1~7.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/img/Tone.jpg)

```
/*Definisi pin Speaker*/
#define SPEAKER 3

int BassTab[]={1911,1702,1516,1431,1275,1136,1012};//bass 1~7

void setup()
{
    pinInit();
}
void loop()
{
        /*Suara bass 1~7*/
    for(int note_index=0;note_index<7;note_index++)
    {
        sound(note_index);
        delay(500);
    }
}
void pinInit()
{
    pinMode(SPEAKER,OUTPUT);
    digitalWrite(SPEAKER,LOW);
}
void sound(uint8_t note_index)
{
    for(int i=0;i<100;i++)
    {
        digitalWrite(SPEAKER,HIGH);
        delayMicroseconds(BassTab[note_index]);
        digitalWrite(SPEAKER,LOW);
        delayMicroseconds(BassTab[note_index]);
    }
}
```
<div class="admonition note">
<p class="admonition-title">Catatan</p>
Karena pengaruh kapasitansi, modul hanya dapat mengeluarkan sinyal bass, dan sinyal treble tidak dapat dipancarkan.
</div>

### Bermain dengan Codecraft

#### Hardware (Perangkat Keras)

**Langkah 1.** Sambungkan Grove - Speaker to port D3 pada Base Shield

**Langkah 2.** Pasang Base Shield pada Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda melalui kabel USB.

#### Software (Perangkat Lunak)

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/),  tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan

Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Tarik blok seperti gambar dibawah atau buka file cdc yang dapat didownload (diunduh) pada akhir halaman ini.

![](https://github.com/SeeedDocument/Grove-Speaker/raw/master/img/Speaker.png)

Upload (unggah) program ke Arduino/Seeeduino anda.

!!!Sukses

    Ketika kode berhasil di unggah, anda dapat mendengar speaker bersuara dari DO Hingga SI.

Sumber-Sumber
--------

-   [File Grove - Speaker Eagle](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Grove-Speaker_Eagle_File.zip)
-   [Cara menghasilkan nada berbeda dengan MCU](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Tone.pdf)
-   [Grove\_-\_Speaker\_v1.0\_brd.pdf](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Grove-Speaker_v1.0_brd.pdf)
-   [Grove\_-\_Speaker\_v1.0\_sch.pdf](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/Grove-Speaker_v1.0_sch.pdf)
-   [Datasheet LM386 Low Voltage Audio Power Amplifier](https://raw.githubusercontent.com/SeeedDocument/Grove-Speaker/master/res/LM386_Low_Voltage_Audio_Power_Amplifier_Datasheet.pdf)
-   [CodeCraft Code](https://github.com/SeeedDocument/Grove-Speaker/raw/master/res/Speaker.zip)


<!-- file ini dibuat dari http://www.seeedstudio.com/wiki/Grove_-_Speaker -->

## Tech Support / Bantuan
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>