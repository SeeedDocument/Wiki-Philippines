---
name: Grove-LED Button
category: Acator
bzurl: 
oldwikiname: 
prodimagename:
surveyurl: 
sku: 111020044,111020045,111020046
tags: 2-链接 
---


![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/main.jpg)


Grove - LED Button terdiri dari Grove - Yellow Button, Grove - Blue LED Button dan Grove - Red LED Button. Tombol ini dapat bertahan hingga 100.000 kali penekanan. Dengan menggunakan LED ini, Anda dapat menerapkan pada banyak proyek menarik seperti menunjukkan status tombol yang ditunjukkan oleh nyala/padam nya lampu LED. Dalam modul ini terdapat MOSFET N-Channel yang berkualitas tinggi untuk mengontrol LED guna memastikan kecepatan switching dan konsumsi daya yang rendah. Secara keseluruhan, tombol ini terlihat keren kan ? Ini dia ...



<p style=":center"><a href="https://www.seeedstudio.com/Grove-Yellow-LED-Button-p-3101.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/Y.png" height="48" width="300" /></a></p>
<p style=":center"><a href="https://www.seeedstudio.com/Grove-Blue-LED-Button-p-3104.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/B.png" height="48" width="300" /></a></p>
<p style=":center"><a href="https://www.seeedstudio.com/Grove-Red-LED-Button-p-3096.html" target="_blank"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/R.png"  height="48" width="300" /></a></p>

## Versi

| Versi Produk  | Perubahan                                                                                               | Tanggal Rilis |
|------------------|-------------------------------------------------------------------------------------------------------|---------------|
| Grove-LED Button | Initial                                                                                               | Jun 2018      |

## Versi

| Versi Produk  | Perubahan                                                                                               | Tanggal Dirilis |
|------------------|-------------------------------------------------------------------------------------------------------|---------------|
| Grove-LED Button | Initial                                                                                               | Jun 2018      |


## Versi

| Versi Produk  | Perubahan                                                                                               | Tanggal Dirilis |
|------------------|-------------------------------------------------------------------------------------------------------|---------------|
| Grove-LED Button | Initial                                                                                               | Jun 2018      |

## Fitur

- Long operating life
- Mudah digunakan
- Grove Digital interface



## Spesifikasi

|Parameter|Nilai|
|---|---|
|Tegangan Kerja|3.3V/5V|
|Operating Life tanpa beban|100 000 times|
|Arus LED|50mA|
|Press Resistance^1^|<100mΩ|
|Release Resistance^2^|>100MΩ|
|Ukuran|L: 40mm W: 20mm H: 13mm| 
|Berat|4.3g|
|Ukuran Kemasan|L: 140mm W: 90mm H: 10mm|
|Berat Keseluruhan|11g|



!!!Tips
        1,2- Jika anda ingin mengukur hambatan, harap lepaskan penutup dari board ini. Kalau tidak, Anda akan mendapatkan nilai resistansi yang sama dengan resistansi board, bukan resistansi yang sebenarnya.



## Hardware (Perangkat Keras)


### Pin Map


![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/pin_map.jpg)


### Skematik

![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/schematic.jpg)


**SIG1** adalah sinyal kontrol LED, nilai defaultnya adalah LOW. Ketika N-Channel MOSFET non-aktif, maka LED juga akan padam. Ketika SIG1 berlogika LOW, maka N-Channel MOSFET akan aktif, dan lampu LED menyala.

**SIG2** terhubung pada pin button. Dengan resistensi pull-up, nilai default dari **SIG2** berlogika HIGH. Oleh karena itu, ketika Anda tombol ditekan, maka tegangan menjadi turun, dan **SIG2** menjadi LOW.




## Platform yang didukung

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |




## Memulai

!!!Tips
        Pada bagian ini, kami menggunakan Grove - Red LED Button sebagai contoh. Bagian berikut ini juga berlaku untuk Grove - Yellow LED dan Grove - Blue LED.


### Bermain dengan Arduino

#### Hardware (Perangkat Keras)

**Bahan yang dibutuhkan**


| Seeeduino V4.2 | Base Shield| Grove- Red LED Button |
|--------------|-------------|-----------------|
|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_1.jpg)|![enter image description here](https://raw.githubusercontent.com/SeeedDocument/Grove_Light_Sensor/master/images/gs_4.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/IMG_0068a.jpg)|
|<a href="http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Base-Shield-V2-p-1378.html" target="_blank">Dapatkan Sekarang</a>|<a href="https://www.seeedstudio.com/Grove-Red-LED-Button-p-3096.html" target="_blank">Dapatkan Sekarang</a>|



- **Langkah 1.** Hubungkan Grove- Red LED Button ke port **D3** dari Grove-Base Shield.

- **Langkah 2.** Hubungkan Groove Base Shield ke Seeeduino.

- **Langkah 3.** Hubungkan Seeeduino ke PC menggunakan kabel USB.


![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/red%20LED.jpg)



!!!Catatan
	Jika kita tidak memiliki Grove Base Shield, Kita juga dapat langsung menghubungkan modul ini ke Seeeduino seperti dibawah ini.


| Seeeduino     |  Grove- Red LED Button           |
|---------------|-------------------------|
| 5V            | Merah                     |
| GND           | Hitam                   |
| SIG2          | Putih                  |
| SIG1          | Kuning                  |




#### Software (Perangkat Lunak)

!!!Catatan
   Jika ini adalah pertama kalinya Anda bekerja dengan Arduino, kami dengan menyarankan Anda untuk melihat [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) sebelum memulai.


- **Langkah 1.** Open the Arduino IDE and create a new file, then copy the following code into the new file.

```C++
#include "Arduino.h"

//1: toggle mode, 2: follow mode
#define LED_MODE   1

const int ledPin = 3;      // the number of the LED pin, D3
const int buttonPin = 4;    // the number of the pushbutton pin, D4
const boolean breathMode = true;  // if or not the led lights as breath mode when it's on

// Variables will change:
int ledState = LOW;         // the current state of the output pin
int ledFadeValue = 0;
int ledFadeStep = 5;
int ledFadeInterval = 20;   //milliseconds
int buttonState;             // the current reading from the input pin
int lastButtonState = HIGH;   // the previous reading from the input pin

unsigned long lastDebounceTime = 0;  // the last time the output pin was toggled
unsigned long debounceDelay = 50;    // the debounce time; increase if the output flickers
unsigned long lastLedFadeTime = 0;

void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
  digitalWrite(ledPin, ledState);
}

void loop() {
  int reading = digitalRead(buttonPin);

  // If the switch changed, due to noise or pressing:
  if (reading != lastButtonState) {
    // reset the debouncing timer
    lastDebounceTime = millis();
  }

  if ((millis() - lastDebounceTime) > debounceDelay) {
    // whatever the reading is at, it's been there for longer
    // than the debounce delay, so take it as the actual current state:

    // if the button state has changed:
    if (reading != buttonState) {
      buttonState = reading;

#if LED_MODE == 1
      if (buttonState == LOW) {  //button is pressed
          ledState = !ledState;
          ledFadeValue = 0;
          lastLedFadeTime = millis();
      }
#else
      if (buttonState == LOW) {  //button is pressed
        ledState = HIGH;
        ledFadeValue = 0;
        lastLedFadeTime = millis();
      } else {                   //button is released
        ledState = LOW;
      }
#endif
    }
  }

  // set the LED:
  if (breathMode && ledState != LOW) {
    if (millis() - lastLedFadeTime > ledFadeInterval) {
      lastLedFadeTime = millis();
      analogWrite(ledPin, ledFadeValue);
      ledFadeValue += ledFadeStep;
      if (ledFadeValue > 255){
        ledFadeValue = 255 - ledFadeStep;
        ledFadeStep = -ledFadeStep;
      } else if (ledFadeValue < 0) {
        ledFadeValue = 0;
        ledFadeStep = -ledFadeStep;
      }
    }
  } else {
    digitalWrite(ledPin, ledState);
  }

  lastButtonState = reading;
}

```

!!!Tip
    Dalam percobaan ini, kami memilih mode 1 yang merupakan mode toggle, Anda dapat mengubahnya pada baris ke 4 <mark>#define LED_MODE   1</mark> menjadi <mark>#define LED_MODE   2</mark> apabila menggunakan mode ini.

- **Langkah 2.** Upload (unggah) kode demo. Jika Anda tidak tahu cara mengunggah kode, harap baca [How to upload code](http://wiki.seeedstudio.com/Upload_Code/).

- **Langkah 3.** Sekarang, coba tekan tombol Anda. Anda akan melihat nyala LED dengan efek fade on/ fade off.


Hasilnya akan seperti ini:

<p style=":center"><img src="https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/result.gif"  /></p>



### Bermain dengan Raspberry Pi

#### Hardware (Perangkat Keras)

- **Langkah 1**. Peralatan yang dibutuhkan pada proyek ini:

| Raspberry pi | Grove Base Hat for RasPi| Grove - Red LED Button|
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Base_Hat_for_Raspberry_Pi/raw/master/img/thumbnail.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/IMG_0068a.jpg)|
|[Dapatkan Sekarang](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Base-Hat-for-Raspberry-Pi-p-3186.html)|[Dapatkan Sekarang](https://www.seeedstudio.com/Grove-Red-LED-Button-p-3096.html)|

- **Langkah 2**. Hubungkan Grove Base Hat ke Raspberry.
- **Langkah 3**. Hubungkan red LED button ke D5 dari Base Hat.
- **Langkah 4**. Hubungkan modul Raspberry Pi ke PC menggunakan kabel USB.

![](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/img/LED_Hat.jpg)

!!! Catatan
    Untuk Langkah 3 Anda dapat menghubungkan tombol LED ke **setiap Port GPIO** tetapi pastikan Anda mengubah perintah sesuai dengan nomor port yang digunakan.


#### Software (Perangkat Lunak)

- **Langkah 1**. Ikuti [Setting Software](http://wiki.seeedstudio.com/Grove_Base_Hat_for_Raspberry_Pi/#installation) untuk mengonfigurasi development environment.
- **Langkah 2**. Download (unduh) file dengan cara menggandakan library grove.py menggunakan kode berikut. 

```
cd ~
git clone https://github.com/Seeed-Studio/grove.py

```

- **Langkah 3**. Jalankan perintah di bawah ini untuk menjalankan kode.

```
cd grove.py/grove
python grove_ryb_led_button.py 5

```

Berikut ini adalah kode the grove_ryb_led_button.py.

```python

import time
from grove.button import Button
from grove.factory import Factory

class GroveLedButton(object):
    def __init__(self, pin):
        # High = light on
        self.__led = Factory.getOneLed("GPIO-HIGH", pin)
        # Low = pressed
        self.__btn = Factory.getButton("GPIO-LOW", pin + 1)
        self.__on_event = None
        self.__btn.on_event(self, GroveLedButton.__handle_event)

    @property
    def on_event(self):
        return self.__on_event

    @on_event.setter
    def on_event(self, callback):
        if not callable(callback):
            return
        self.__on_event = callback

    def __handle_event(self, evt):
        # print("event index:{} event:{} pressed:{}".format(evt['index'], evt['code'], evt['presesed']))
        if callable(self.__on_event):
            self.__on_event(evt['index'], evt['code'], evt['time'])
            return

        self.__led.brightness = self.__led.MAX_BRIGHT
        event = evt['code']
        if event & Button.EV_SINGLE_CLICK:
            self.__led.light(True)
            print("turn on  LED")
        elif event & Button.EV_DOUBLE_CLICK:
            self.__led.blink()
            print("blink    LED")
        elif event & Button.EV_LONG_PRESS:
            self.__led.light(False)
            print("turn off LED")


Grove = GroveLedButton

def main():
    from grove.helper import SlotHelper
    sh = SlotHelper(SlotHelper.GPIO)
    pin = sh.argv2pin()

    ledbtn = GroveLedButton(pin)

    # remove ''' pairs below to begin your experiment
    '''
    # define a customized event handle your self
    def cust_on_event(index, event, tm):
        print("event with code {}, time {}".format(event, tm))

    ledbtn.on_event = cust_on_event
    '''
    while True:
        time.sleep(1)


if __name__ == '__main__':
    main()


```

!!!berhasil 
    Jika semuanya berjalan dengan baik, Anda akan dapat melihat LED menyala jika Anda menekannya dan mati jika Anda menekannya lama. Jika Anda mengklik dua kali tombol LED, LED akan berkedip.

```python

pi@raspberrypi:~/grove.py/grove $ python grove_ryb_led_button.py 5
Hat Name = 'Grove Base Hat RPi'
turn on  LED
turn on  LED
blink    LED
turn on  LED
turn off LED
^CTraceback (most recent call last):
  File "grove_ryb_led_button.py", line 101, in <module>
    main()
  File "grove_ryb_led_button.py", line 97, in main
    time.sleep(1)
KeyboardInterrupt

```


Anda dapat keluar dari program ini hanya dengan menekan ++ctrl+c++.



## Sumber-sumber

- **[Zip]** [Grove-LED Button Eagle file](https://github.com/SeeedDocument/Grove-Red_LED_Button/raw/master/res/Grove-Red_LED_Button.zip)


## Tech Support / Bantuan
Silakan kirimkan masalah teknis apa pun ke kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>