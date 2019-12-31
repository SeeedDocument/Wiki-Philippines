---
name: Grove - Chainable RGB LED
category: Actuator
bzurl: https://seeedstudio.com/Grove-Chainable-RGB-LED-p-850.html
oldwikiname: Grove_-_Chainable_RGB_LED
prodimagename: Chanbalelednb1.jpg
bzprodimageurl: http://statics3.seeedstudio.com/images/product/chanbalelednb1.jpg
surveyurl: https://www.research.net/r/Grove-Chainable_RGB_LED
sku: 104030006
tags: grove_digital, io_3v3, io_5v, plat_duino, plat_linkit, plat_bbg
---

![](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/img/Grove-Chainable_RGB_LED_V2.0.jpg)

**Grove - Chainable RGB LED** adalah modul yang didasarkan pada chip P9813 yang merupakan driver LED penuh warna (full-color). modul ini menyediakan 3 driver arus konstan serta output termodulasi dari 256 warna abu-abu (shades of gray). Modul berkomunikasi dengan MCU menggunakan transmisi 2-kawat (Data dan Clock). Transmisi 2-kawat ini dapat digunakan untuk memubuat kaskade (cascade) modul **Grove - Chainable RGB LED** tambahan. Built-in clock regeneration meningkatkan jarak transmisi. Modul Grove ini cocok untuk proyek berbasis LED yang berwarna-warni.



Versi
---
| Perbaikan | Deskripsi                                              | Rilis      |Cara Membeli|
|----------|-----------------------------------------------------------|--------------|--------------|
| v1    | rilis publik pertama (beta)                             | 5 Mei 2011  |[![](https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png)](https://www.seeedstudio.com/Grove-Chainable-RGB-LED-p-850.html)|
| v2    | Mengganti P9813S16 dengan P9813S14 dan mengubah Grove connector dari Vertikal ke horizontal | 19 April 2016  |[![](https://raw.githubusercontent.com/SeeedDocument/Seeed-WiKi/master/docs/images/get_one_now_small.png)](https://www.seeedstudio.com/Grove-%E2%80%93-Chainable-RGB-Led-V2.0-p-2903.html)|

Spesifikasi
-------------

-   Operating Voltage: 5V
-   Operating Current: 20mA
-   Communication Protocol: Serial

!!!Tips 
    Selengkapnya tentang modul Grove bisa mengacu ke [Grove System](http://wiki.seeedstudio.com/Grove_System/)

Platform yang didukung
-------------------

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo.jpg) |

!!!Peringatan
    Platform yang didukung dan disebutkan diatas merupakan keterangan perangkat lunak modul atau kompatibilitas secara teori. Kami hanya menyediakan library atau contoh kode untuk platform Arduino dalam kasus yang umum. Dalam hal ini,tidak memungkinkan menyediakan library kode demo untuk semua platform MCU lainnya. Oleh karena itu, pengguna harus membuat library mereka sendiri.


Penggunaan
-----

### Bermain dengan [Arduino](/Arduino "Arduino")

Saat anda memiliki Grove - Chainable RGB LED, Anda mungkin berpikir bagaimana saya dapat menyalakannya. Sekarang kami akan menunjukkan kepada Anda melalui demo ini: semua siklus (cycles) warna RGB dengan cara yang serupa.

Untuk menyelesaikan demo ini, Anda dapat menggunakan satu atau lebih Grove - Chainable RGB LED. Perhatikan bahwa antarmuka (interface) IN dari satu Grove - Chainable RGB LED harus terhubung ke pin D7/D8 pada [Grove - Base Shield](/Base_Shield_V2 "Grove - Base Shield") dan antarmuka (interface) OUT-nya terhubung ke antarmuka IN dari Grove - RGB Chainable RGB LED lainnya, menyambungkan lebih banyak LED dengan cara ini.

-   Unduh (Download) [Chainable LED Library](https://github.com/pjpmarques/ChainableLED) dan lakukan instalasi ke Library di Arduino. Terdapat panduan tentang [how to install Arduino Library](/How_to_install_Arduino_Library) dalam halaman situs wiki.
-   Buka contoh CycleThroughColors melalui alamat (path): **File->Examples->ChainableLED_master** dan Unggah (upload) contoh tersebut ke Seeeduino.

```

/* 
 * Contoh menggunakan library ChainableRGB untuk mengontrol Grove RGB.
 * Kode ini berfungsi untuk semua siklus warna dengan cara yang serupa. hal ini diselesaikan menggunakan ruang warna HSB.
 */


#include <ChainableLED.h>

#define NUM_LEDS  5

ChainableLED leds(7, 8, NUM_LEDS);

void setup()
{
  leds.init();
}

float hue = 0.0;
boolean up = true;

void loop()
{
  for (byte i=0; i<NUM_LEDS; i++)
    leds.setColorHSB(i, hue, 1.0, 0.5);
    
  delay(50);
    
  if (up)
    hue+= 0.025;
  else
    hue-= 0.025;
    
  if (hue>=1.0 && up)
    up = false;
  else if (hue<=0.0 && !up)
    up = true;
}

```

Anda dapat mengamati bagian ini: warna-warna pada 5 LED akan mengalami gradien secara konsisten.

**Extended application:**
Berdasarkan pada [Chainable LED Library](https://github.com/pjpmarques/ChainableLED), kami telah merancang demo ini: Warna RGB bervariasi dengan suhu yang terukur oleh Grove - temperature. Warna RGB bervariasi dari hijau ke merah ketika suhu dari 25 hingga 32 derajat. Kode pengujian ditunjukkan di bawah ini. Lakukan jika Anda tertarik membuatnya.

```
    // demo  suhu -> rgbLED
    // suhu dari rentang 25 - 32, rgbLed menyala dari hijau -> merah
    // Pasangkan Grove-temperature ke pin A0
    // LED dipasangkan ke D7,D8

    #include <Streaming.h>
    #include <ChainableLED.h>

    #define TEMPUP 32
    #define TEMPDOWN 25

    ChainableLED leds(7, 8, 1); // hubungkan ke pin7 dan pin8 , satu led

    int getAnalog() // ambil nilai dari A0
    {
        int sum = 0;
        for(int i=0; i<32; i++)
        {
            sum += analogRead(A0);
        }

        return sum>>5;
    }

    float getTemp() // ambil nilai suhu
    {
        float temperature = 0.0;
        float resistance = 0.0;
        int B = 3975; //Nilai B pada thermistor

        int a = getAnalog();

        resistance = (float)(1023-a)*10000/a; //Membaca nilai resistansi dari sensor;
        temperature = 1/(log(resistance/10000)/B+1/298.15)-273.15; //Konversi ke suhu mengacu pada datasheet ;
        return temperature;
    }

    void ledLight(int dta) // nyalakan led
    {

        dta = dta/4; // 0 - 255

        int colorR = dta;
        int colorG = 255-dta;
        int colorB = 0;

        leds.setColorRGB(0, colorR, colorG, colorB);
    }

    void setup()
    {
        Serial.begin(38400);
        cout << "hello world !" << endl;
    }

    void loop()
    {
        float temp = getTemp();
        int nTemp = temp*100;

        nTemp = nTemp > TEMPUP*100 ? TEMPUP*100 : (nTemp < TEMPDOWN*100 ? TEMPDOWN*100 : nTemp);
        nTemp = map(nTemp, TEMPDOWN*100, TEMPUP*100, 0, 1023);
        ledLight(nTemp);
        delay(100);
    }
```

### Bermain dengan Codecraft

#### Hardware

**Langkah 1.** Hubungkan Grove - Chainanle RGB LED ke port D7 pada Base Shield

**Langkah 2.** Pasang Grove - Base Shield ke Seeeduino/Arduino anda.

**Langkah 3.** Hubungkan Seeeduino/Arduino ke PC anda melalui kabel USB.

#### Software

**Langkah 1.** Buka [Codecraft](https://ide.chmakered.com/),  tambahkan dukungan pada Arduino, dan tarik Prosedur Utama (main procedure) ke area kerja (working area).

!!!Catatan
    Jika ini pertama kalinya anda menggunakan Codecraft, lihat juga [Guide for Codecraft using Arduino](http://wiki.seeedstudio.com/Guide_for_Codecraft_using_Arduino/).

**Langkah 2.** Seret (drag) blok-blok yang ada seperti gambar dibawah ini atau buka file cdc yang dapat diunduh pada akhir halaman ini.

![](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/img/Chainable_RGB_LED.png)

Unggah (Upload) program ke Arduino/Seeeduino anda.

!!!Sukses
    Ketika kode berhasil di unggah, anda dapat melihat LED fade in dan fade out.

### Bermain dengan Raspberry Pi

1.Anda harus sudah memiliki raspberry pi dan grovepi atau grovepi+.

2.Anda harus sudah selesai mengkonfigurasi lingkungan pengembangan (development enviroment), Jika tidak ikuti petunjuk berikut [here](/GrovePi_Plus).

3.Koneksi

-   Hubungkan sensor ke soket D7 grovepi dengan menggunakan kabel grove.

4.Arahkan ke direktori demo:

```
    cd yourpath/GrovePi/Software/Python/
```

-   Untuk melihat kode
```
     nano grove_chainable_rgb_led.py   # "Ctrl+x" to exit #
```
```
    import time
    import grovepi

    # Hubungkan LED pertama dengan Chainable RGB LED chain ke port digital D7
    # In: CI,DI,VCC,GND
    # Out: CO,DO,VCC,GND
    pin = 7

    # Saya memiliki 10 LED yang terhubung seri dengan LED pertama yang terhubung ke GrovePi dan terakhir yang tidak tersambung
    # Soket input LED pertama terhubung ke GrovePi, soket output terhubung ke input LED kedua dan seterusnya
    numleds = 1  

    grovepi.pinMode(pin,"OUTPUT")
    time.sleep(1)

    # Metode Chainable RGB LED
    # grovepi.storeColor(red, green, blue)
    # grovepi.chainableRgbLed_init(pin, numLeds)
    # grovepi.chainableRgbLed_test(pin, numLeds, testColor)
    # grovepi.chainableRgbLed_pattern(pin, pattern, whichLed)
    # grovepi.chainableRgbLed_modulo(pin, offset, divisor)
    # grovepi.chainableRgbLed_setLevel(pin, level, reverse)

    # uji coba warna menggunakan grovepi.chainableRgbLed_test()
    testColorBlack = 0   # 0b000 #000000
    testColorBlue = 1    # 0b001 #0000FF
    testColorGreen = 2   # 0b010 #00FF00
    testColorCyan = 3    # 0b011 #00FFFF
    testColorRed = 4     # 0b100 #FF0000
    testColorMagenta = 5 # 0b101 #FF00FF
    testColorYellow = 6  # 0b110 #FFFF00
    testColorWhite = 7   # 0b111 #FFFFFF

    # Pola dalam penggunaan grovepi.chainableRgbLed_pattern()
    thisLedOnly = 0
    allLedsExceptThis = 1
    thisLedAndInwards = 2
    thisLedAndOutwards = 3

    try:

        print "Test 1) Initialise"

        # inisialisasi rantai LED
        grovepi.chainableRgbLed_init(pin, numleds)
        time.sleep(.5)

        # ubah warna menjadi warna hijau
        grovepi.storeColor(0,255,0)
        time.sleep(.5)

        # atur led 1 menjadi warna green
        grovepi.chainableRgbLed_pattern(pin, thisLedOnly, 0)
        time.sleep(.5)

        # ubah warna menjadi merah
        grovepi.storeColor(255,0,0)
        time.sleep(.5)

        # atur led 10 menjadi warna merah
        grovepi.chainableRgbLed_pattern(pin, thisLedOnly, 9)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 2a) Test Patterns - black"

        # uji coba pola 0 - hitam (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(1)


        print "Test 2b) Test Patterns - blue"

        # uji coba pola 1 biru
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlue)
        time.sleep(1)


        print "Test 2c) Test Patterns - green"

        # uji coba pola 2 hijau
        grovepi.chainableRgbLed_test(pin, numleds, testColorGreen)
        time.sleep(1)


        print "Test 2d) Test Patterns - cyan"

        # uji coba pola 3 cyan
        grovepi.chainableRgbLed_test(pin, numleds, testColorCyan)
        time.sleep(1)


        print "Test 2e) Test Patterns - red"

        # uji coba pola 4 merah
        grovepi.chainableRgbLed_test(pin, numleds, testColorRed)
        time.sleep(1)


        print "Test 2f) Test Patterns - magenta"

        # uji coba pola 5 magenta
        grovepi.chainableRgbLed_test(pin, numleds, testColorMagenta)
        time.sleep(1)


        print "Test 2g) Test Patterns - yellow"

        # uji coba pola 6 kuning
        grovepi.chainableRgbLed_test(pin, numleds, testColorYellow)
        time.sleep(1)


        print "Test 2h) Test Patterns - white"

        # uji coba pola 7 putih
        grovepi.chainableRgbLed_test(pin, numleds, testColorWhite)
        time.sleep(1)


        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 3a) Set using pattern - this led only"

        # ubah warna menjadi merah
        grovepi.storeColor(255,0,0)
        time.sleep(.5)

        # atur led 3 menjadi merah
        grovepi.chainableRgbLed_pattern(pin, thisLedOnly, 2)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 3b) Set using pattern - all leds except this"

        # ubah warna menjadi warna biru
        grovepi.storeColor(0,0,255)
        time.sleep(.5)

        # atur semua LED kecuali untuk 3 tetap warna biru
        grovepi.chainableRgbLed_pattern(pin, allLedsExceptThis, 3)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 3c) Set using pattern - this led and inwards"

        # ubah warna menjadi hijau
        grovepi.storeColor(0,255,0)
        time.sleep(.5)

        # atur led 1-3 menjadi hijau
        grovepi.chainableRgbLed_pattern(pin, thisLedAndInwards, 2)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 3d) Set using pattern - this led and outwards"

        # ubah warna menjadi hijau
        grovepi.storeColor(0,255,0)
        time.sleep(.5)

        # atur led 7-10 menjadi hijau
        grovepi.chainableRgbLed_pattern(pin, thisLedAndOutwards, 6)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 4a) Set using modulo - all leds"

        # ubah warna menjadi warna hitam (sepenuhnya mati)
        grovepi.storeColor(0,0,0)
        time.sleep(.5)

        # atur semua led menjadi hitam
        # offset 0 berarti mulai dari led pertama
        # divisor 1 berarti setiap led
        grovepi.chainableRgbLed_modulo(pin, 0, 1)
        time.sleep(.5)

        # ubah warna menjadi warna putih (sepenuhnya menyala)
        grovepi.storeColor(255,255,255)
        time.sleep(.5)

        # atur semua led menjadi putih
        grovepi.chainableRgbLed_modulo(pin, 0, 1)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 4b) Set using modulo - every 2"

        # ubah warna menjadi warna merah
        grovepi.storeColor(255,0,0)
        time.sleep(.5)

        # aur tiap led kedua menyala merah
        grovepi.chainableRgbLed_modulo(pin, 0, 2)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)


        print "Test 4c) Set using modulo - every 2, offset 1"

        # ubah warna menjadi warna hijau
        grovepi.storeColor(0,255,0)
        time.sleep(.5)

        # atur setiap led kedua menjadi berwarna hijau, offset 1
        grovepi.chainableRgbLed_modulo(pin, 1, 2)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 4d) Set using modulo - every 3, offset 0"

        # ubah warna ke warna merah
        grovepi.storeColor(255,0,0)
        time.sleep(.5)

        # atur setiap led ketiga menjadi berwarna merah
        grovepi.chainableRgbLed_modulo(pin, 0, 3)
        time.sleep(.5)

        # ubah warna menjadi warna hijau
        grovepi.storeColor(0,255,0)
        time.sleep(.5)

        # atur setiap led ketiga menjadi berwarna hijau, offset 1
        grovepi.chainableRgbLed_modulo(pin, 1, 3)
        time.sleep(.5)

        # ubah warna menjadi warna biru
        grovepi.storeColor(0,0,255)
        time.sleep(.5)

        # atur setiap led ketiga menjadi berwarna biru blue, offset 2
        grovepi.chainableRgbLed_modulo(pin, 2, 3)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 4e) Set using modulo - every 3, offset 1"

        # ubah warna menjadi warna kuning
        grovepi.storeColor(255,255,0)
        time.sleep(.5)

        # atur setiap led keempat led menjadi berwarna kuning
        grovepi.chainableRgbLed_modulo(pin, 1, 3)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)


        print "Test 4f) Set using modulo - every 3, offset 2"

        # ubah warna menjadi warna magenta
        grovepi.storeColor(255,0,255)
        time.sleep(.5)

        # atur setiap led keempat menjadi warna magenta
        grovepi.chainableRgbLed_modulo(pin, 2, 3)
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 5a) Set level 6"

        # ubah warna menjadi warna hijau
        grovepi.storeColor(0,255,0)
        time.sleep(.5)

        # atur led 1-6 menjadi warna hijau
        grovepi.write_i2c_block(0x04,[95,pin,6,0])
        time.sleep(.5)

        # jeda (pause) agar anda dapat melihat apa yang terjadi
        time.sleep(2)

        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        time.sleep(.5)


        print "Test 5b) Set level 7 - reverse"

        # ubah warna menjadi warna merah
        grovepi.storeColor(255,0,0)
        time.sleep(.5)

        # atur led 4-10 menjadi warna merah
        grovepi.write_i2c_block(0x04,[95,pin,7,1])
        time.sleep(.5)


    except KeyboardInterrupt:
        # reset (semua mati)
        grovepi.chainableRgbLed_test(pin, numleds, testColorBlack)
        break
    except IOError:
        print "Error"
```

-   Perhatikann bahwa ada sesuatu yang harus anda cermati:

```
    pin = 7         #setting up the output pin
    numleds = 1     #how many leds you plug
```

-   adapun metode yang dapat anda lihat dalam grovepi.py adalah:

```
    storeColor(red, green, blue)
    chainableRgbLed_init(pin, numLeds)
    chainableRgbLed_test(pin, numLeds, testColor)
    chainableRgbLed_pattern(pin, pattern, whichLed)
    chainableRgbLed_modulo(pin, offset, divisor)
    chainableRgbLed_setLevel(pin, level, reverse)
```

5.Jalankan demo.
```
    sudo python grove_chainable_rgb_led.py
```

6.Demo ini mungkin tidak bekerja jika grovepi anda tidak menggunakan firmware terbaru, jika hal ini terjadi segera perbarui (update) firmware.
```
    cd yourpath/GrovePi/Firmware
    sudo ./firmware_update.sh
```

### Dengan Beaglebone Green

Untuk mulai mengedit program pada BBG, anda dapat menggunakan IDE Cloud9.

Sebagai latihan sederhana untuk mengenal IDE Cloud9, dengan membuat aplikasi sederhana untuk mengedipkan salah satu dari 4 LED yang dapat diprogram menggunakan BeagleBone menjadi awal yang baik.

Jika ini pertama kalinya anda menggunakan IDE Cloud9, silahkan ikuti petunjuk melalui langkah berikut [**link**](/BeagleBone_Green).

**Langkah 1:** Atur soket Grove - UART sebagai soket Grove - GPIO, ikuti petunjuk melalui langkah berikut [**link**](http://www.seeedstudio.com/recipe/362-how-to-use-the-grove-uart-port-as-a-gpio-on-bbg.html).

**Langkah 2:** klik simbol "+" di sebelah kanan atas untuk membuat file baru.

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Chainable_RGB_LED/master/img/C9-create-tab.png)

![](https://raw.githubusercontent.com/SeeedDocument/Grove-Chainable_RGB_LED/master/img/C9_newfile.jpg)

**Langkah 3:** Salin (copy) dan sisipkan (paste) kode berikut ke dalam tab baru

```
import time
import Adafruit_BBIO.GPIO as GPIO
 
CLK_PIN = "P9_22"
DATA_PIN = "P9_21"
NUMBER_OF_LEDS = 1
 
class ChainableLED():
    def __init__(self, clk_pin, data_pin, number_of_leds):
        self.__clk_pin = clk_pin
        self.__data_pin = data_pin
        self.__number_of_leds = number_of_leds
 
        GPIO.setup(self.__clk_pin, GPIO.OUT)
        GPIO.setup(self.__data_pin, GPIO.OUT)
 
        for i in range(self.__number_of_leds):
            self.setColorRGB(i, 0, 0, 0)
 
    def clk(self):
        GPIO.output(self.__clk_pin, GPIO.LOW)
        time.sleep(0.00002)
        GPIO.output(self.__clk_pin, GPIO.HIGH)
        time.sleep(0.00002)
 
    def sendByte(self, b):
        "Send one bit at a time, starting with the MSB"
        for i in range(8):
            # If MSB is 1, write one and clock it, else write 0 and clock
            if (b & 0x80) != 0:
                GPIO.output(self.__data_pin, GPIO.HIGH)
            else:
                GPIO.output(self.__data_pin, GPIO.LOW)
            self.clk()
 
            # Advance to the next bit to send
            b = b << 1
 
    def sendColor(self, red, green, blue):
        "Start by sending a byte with the format '1 1 /B7 /B6 /G7 /G6 /R7 /R6' "
        #prefix = B11000000
        prefix = 0xC0
        if (blue & 0x80) == 0:     
            #prefix |= B00100000
            prefix |= 0x20
        if (blue & 0x40) == 0:     
            #prefix |= B00010000
            prefix |= 0x10
        if (green & 0x80) == 0:    
            #prefix |= B00001000
            prefix |= 0x08
        if (green & 0x40) == 0:    
            #prefix |= B00000100
            prefix |= 0x04
        if (red & 0x80) == 0:      
            #prefix |= B00000010
            prefix |= 0x02
        if (red & 0x40) == 0:      
            #prefix |= B00000001
            prefix |= 0x01
        self.sendByte(prefix)
 
        # Sekarang kirim 3 warna
        self.sendByte(blue)
        self.sendByte(green)
        self.sendByte(red)
 
    def setColorRGB(self, led, red, green, blue):
        # Kirim data frame awalan (32x '0')
        self.sendByte(0x00)
        self.sendByte(0x00)
        self.sendByte(0x00)
        self.sendByte(0x00)
 
        # Kirim  data warna untuk masing-masing led
        for i in range(self.__number_of_leds):
            '''
            if i == led:
                _led_state[i*3 + _CL_RED] = red;
                _led_state[i*3 + _CL_GREEN] = green;
                _led_state[i*3 + _CL_BLUE] = blue;
            sendColor(_led_state[i*3 + _CL_RED],
                      _led_state[i*3 + _CL_GREEN],
                      _led_state[i*3 + _CL_BLUE]);
            '''
            self.sendColor(red, green, blue)
 
        # mengakhiri data frame (32x "0")
        self.sendByte(0x00)
        self.sendByte(0x00)
        self.sendByte(0x00)
        self.sendByte(0x00)
 
 
# Catatan: Gunakan P9_22(UART2_RXD) dan P9_21(UART2_TXD) sebagai GPIO.
# Hubungkan Grove - Chainable RGB LED ke port UART Grove pada Beaglebone Green.
if __name__ == "__main__":
    rgb_led = ChainableLED(CLK_PIN, DATA_PIN, NUMBER_OF_LEDS)
 
    while True:
        # Parameter pertama: NUMBER_OF_LEDS - 1; parameter lainnya: nilai RGB.
        rgb_led.setColorRGB(0, 255, 0, 0)
        time.sleep(2)
        rgb_led.setColorRGB(0, 0, 255, 0)
        time.sleep(2)
        rgb_led.setColorRGB(0, 0, 0, 255)
        time.sleep(2)
        rgb_led.setColorRGB(0, 0, 255, 255)
        time.sleep(2)
        rgb_led.setColorRGB(0, 255, 0, 255)
        time.sleep(2)
        rgb_led.setColorRGB(0, 255, 255, 0)
        time.sleep(2)
        rgb_led.setColorRGB(0, 255, 255, 255)
        time.sleep(2)
```

**Langkah 4:** Simpan file dengan cara klik simbol disk dan beri nama file dengan ektensi file .py .

**Langkah 5:** Hubungkan Grove Chainable RGB LED ke soket Grove UART pada BBG.

**Langkah 6:** Jalankan kodenya. Anda dapat memperhatikan RGB LED berubah warnanya setiap 2 detik.

Sumber-sumber
---------

-   **[Library]**[Chainable RGB LED Library for the P9813](https://github.com/pjpmarques/ChainableLED)
-   **[Library]**[Github repository for Chainable RGB LED Library (new)](https://github.com/Seeed-Studio/Grove_Chainable_RGB_LED)
-   **[Library]** [CodeCraft Code](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/res/Chainable%20RGB%20LED.zip)
-   **[Eagle]**[Chainable RGB LED eagle file V1](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/res/Chainable_RGB_LED_eagle_file%20V1.zip)
-   **[Eagle]**[Chainable RGB LED eagle file V2](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/res/Grove%20-%20Chainable%20RGB%20LED%20v2.0.zip)
-   **[PDF]**[Chainable RGB LED SCH file V1](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/res/CRGBled%20v1_SCH.pdf)
-   **[PDF]**[Chainable RGB LED SCH file V2](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/res/Grove%20-%20Chainable%20RGB%20LED%20v2.0%20SCH.pdf)
-   **[PDF]**[Chainable RGB LED PCB file V1](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/res/CRGBled%20V1_PCB.pdf)
-   **[PDF]**[Chainable RGB LED PCB file V2](https://github.com/SeeedDocument/Grove-Chainable_RGB_LED/raw/master/res/Grove%20-%20Chainable%20RGB%20LED%20v2.0%20PCB.pdf)
-   **[Datasheet]**[P9813 Datasheet](https://raw.githubusercontent.com/SeeedDocument/Grove-Chainable_RGB_LED/master/res/P9813_datasheet.pdf)


<!-- File panduan ini dibuat dari http://www.seeedstudio.com/wiki/Grove_-_Chainable_RGB_LED -->


## Proyek - Proyek

**Grove - Introduction to Chainable LED**: Proyek ini menunjukan kepada anda cara menghubunngkan chainable LED ke Grove.
<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/ingo-lohs/grove-introduction-to-chainable-led-d668b7/embed' width='350'></iframe>

**DIY a device for explaining RGB color model**

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/kevin-lee2/diy-a-device-for-explaining-rgb-color-model-496cbc/embed' width='350'></iframe>

**Security Access Using Seeeduino Lotus**: Ketika anda mengetuk pintu atau dekat dengan pintu, pintu akan membuka secara otomatis.

<iframe frameborder='0' height='327.5' scrolling='no' src='https://www.hackster.io/limanchen/security-access-using-seeeduino-lotus-7eb90f/embed' width='350'></iframe>

## Tech Support / Bantuan Teknis
Silahkan kirim masalah teknis apa pun kepada kami melalui [forum](http://forum.seeedstudio.com/). <br /><p style="text-align:center"><a href="https://www.seeedstudio.com/act-4.html?utm_source=wiki&utm_medium=wikibanner&utm_campaign=newproducts" target="_blank"><img src="http://digiwarestore.com/img/cms/poster/b_seeed_studio.jpg" /></a></p>