---
title: Grove - Moisture Sensor
category: Sensor
bzurl: https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html
oldwikiname: Grove - Moisture Sensor
prodimagename: Moisture_sensor_.jpg
surveyurl: https://www.research.net/r/grove-moisture-sensor
sku: 101020008
---

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/Moisture_sensor_.jpg)

This Moisture Senor can be used for detecting the moisture of soil or judge if there is water around the sensor, let the plant in your garden able to reach out for human's help when they are thirsty. This sensor is very easy to use, you can just simply insert in into the soil and read the data. With this sensor, you can make a small project that can let the plant send a message to you like " I am thirsty now, please feed me some water."

<p style="text-align:center"><a href="https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html" target="_blank"><img src="https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/get_one_now_small.png" width="200" height="38"  border=0 /></a></p>

## Version

| Product Version              | Changes                                   | Released Date |
|------------------------------|-------------------------------------------|---------------|
| Grove - Moisture Sensor V1.4 | Initial                                   | June 2014     |


## Features

- Soil moisture sensor based on soil resistivity meansurement
- Easy to use
- 2.0 cm X 6.0 cm grove module

!!!Tip
    More details about Grove modules please refer to [Grove System](http://wiki.seeedstudio.com/Grove_System/)

## Specification

|Item|Condition|Min|Typical|Max|Unit|
|---|---|---|---|---|---|
|Voltage|-|3.3|-|5|V|
|Current|-|0|-|35|mA|
|Output Value|Sensor in dry soil<br>Sensor in humid soil<br>Sensor in water|0<br>300<br>700<br>|-|300<br>700<br>950|-|


## Platforms Supported

| Arduino                                                                                             | Raspberry Pi                                                                                             | BeagleBone                                                                                      | Wio                                                                                               | LinkIt ONE                                                                                         |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/arduino_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/raspberry_pi_logo.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/bbg_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/wio_logo_n.jpg) | ![](https://raw.githubusercontent.com/SeeedDocument/wiki_english/master/docs/images/linkit_logo_n.jpg) |

!!!Caution
    The platforms mentioned above as supported is/are an indication of the module's hardware or theoritical compatibility. We only provide software library or code examples for Arduino platform in most cases. It is not possible to provide software library / demo code for all possible MCU platforms. Hence, users have to write their own software library.


## Application Ideas

- Botanical Gardening
- Moisture Sensoring
- Consistency Measurement

## Getting Started

!!!Note
    If this is the first time you work with Arduino, we firmly recommend you to see [Getting Started with Arduino](http://wiki.seeedstudio.com/Getting_Started_with_Arduino/) before the start.


### Play With Arduino

**Hardware**

- **Step 1.** Prepare the below stuffs:

| Seeeduino V4.2 | Base Shield|  Grove-Moisture Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/seeeduino_v4.2.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/base_shield.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg)|
|[Get One Now](http://www.seeedstudio.com/Seeeduino-V4.2-p-2517.html)|[Get One Now](https://www.seeedstudio.com/Base-Shield-V2-p-1378.html)|[Get One Now](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)|

- **Step 2.** Connect Grove-Moisture Sensor to port A0 of Grove-Base Shield.
- **Step 3.** Plug Grove - Base Shield into Seeeduino.
- **Step 4.** Connect Seeeduino to PC via a USB cable.

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Seeeduino_moisture.jpg)

!!!Note
	If we don't have Grove Base Shield, We also can directly connect Grove-Moisture Sensor to Seeeduino as below.

| Seeeduino       | Grove-Moisture Sensor |
|---------------|-------------------------|
| 5V           | Red                     |
| GND           | Black                   |
| Not Conencted | White                   |
| A0            | Yellow                  |

**Software**

- **Step 1.** Copy the code into Arduino IDE and upload. If you do not know how to upload the code, please check [how to upload code](http://wiki.seeedstudio.com/Upload_Code/).

```c++
int sensorPin = A0;
int sensorValue = 0;

void setup() {
    Serial.begin(9600);
}
void loop() {
    // read the value from the sensor:
    sensorValue = analogRead(sensorPin);
    Serial.print("Moisture = " );
    Serial.println(sensorValue);
    delay(1000);
}
```

- **Step 2.** We will see the moisture display on terminal as below.

```
Moisture = 0
Moisture = 31
Moisture = 48
Moisture = 139
Moisture = 155
Moisture = 124
Moisture = 236
Moisture = 218
Moisture = 215
Moisture = 221
```

### Play With Raspberry Pi

**Hardware**

- **Step 1.** Prepare the below stuffs:

| Raspberry pi | GrovePi_Plus | Grove-Moisture Sensor |
|--------------|-------------|-----------------|
|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/rasp.jpg)|![enter image description here](https://github.com/SeeedDocument/wiki_english/raw/master/docs/images/Grovepi%2B.jpg)|![enter image description here](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/Moisture_sensor_S.jpg)|
|[Get One Now](https://www.seeedstudio.com/Raspberry-Pi-3-Model-B-p-2625.html)|[Get One Now](https://www.seeedstudio.com/GrovePi%2B-p-2241.html)|[Get One Now](https://www.seeedstudio.com/Grove-Moisture-Sensor-p-955.html)|


- **Step 2.** Plug the GrovePi_Plus into Raspberry.
- **Step 3.** Connect Grove-Moisture Sensor to **A0** port of GrovePi_Plus.
- **Step 4.** Connect the Raspberry to PC through USB cable.

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/img/rpi_moisture.jpg)

**Software**

- **Step 1.** Follow [Setting Software](https://www.dexterindustries.com/GrovePi/get-started-with-the-grovepi/setting-software/) to configure the development environment.
- **Step 2.** Git clone the Github repository.

```
cd ~
git clone https://github.com/DexterInd/GrovePi.git

```

-	**Step 3.** Excute below commands to use the Grove-Moisture Sensor to meansure the moisture.


```
cd ~/GrovePi/Software/Python
python grove_moisture_sensor.py
```

Here is the grove_moisture_sensor.py code.

```python
# 	Here are suggested sensor values:
# 		Min  Typ  Max  Condition
# 		0    0    0    sensor in open air
# 		0    20   300  sensor in dry soil
# 		300  580  700  sensor in humid soil
# 		700  940  950  sensor in water


import time
import grovepi

# Connect the Grove Moisture Sensor to analog port A0
# SIG,NC,VCC,GND
sensor = 0

while True:
    try:
        print(grovepi.analogRead(sensor))
        time.sleep(.5)

    except KeyboardInterrupt:
        break
    except IOError:
        print ("Error")
```

- **Step 4.** We will see the moisture display on terminal as below.

```
pi@raspberrypi:~/GrovePi/Software/Python $ python grove_moisture_sensor.py
0
90
130
150
160
218
238
```

### Play With TI LaunchPad

**Hardware**

The following sketch demonstrates a simple application of sensing the moisture in soil.With this, you can know whether your plant needs water or not by observing the result from the output of the sensor

![](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/images/Moisture.jpg)

**Software**

```c
/*
  Moisture-Sensor
  The following sketch demonstrates a simple application of sensing
  the moisture of the soil. You can know whether a plant needs water
  or not by observing the results that the sensor outputs.
  The circuit:
    * Moisture-Sensor attached to pin 24 (J6 plug on Grove Base BoosterPack)
    * one side pin (either one) to ground
    * the other side pin to +VCC
    * LED anode (long leg) attached to RED_LED
    * LED cathode (short leg) attached to ground
  - NOTE:
    This example code is in the public domain.
    http://seeedstudio.com/wiki/Grove_-_Moisture_Sensor
*/
#include "TM1637.h"
/* Macro Define */
#define CLK 39              /* 4-digital display clock pin */
#define DIO 38              /* 4-digiral display data pin */
#define BLINK_LED RED_LED   /* blink led */
#define MOISTURE_PIN 24     /* pin of moisture sensor */
#define THRESHOLD_VALUE 300 /* threshold for watering the flowers */
#define ON HIGH             /* led on */
#define OFF LOW             /* led off */
#define _handle_led(x) digitalWrite(BLINK_LED, x) /* handle led */

/* Global Varibles */
TM1637 tm1637(CLK, DIO);    /* 4-digital display object */
int analog_value = 0;       /* varible to store the value coming from rotary angle
sensor */
int8_t bits[4] = {0};       /* array to store the single bits of the value */
/* the setup() method runs once, when the sketch starts */
void setup() {
/* Initialize 4-digital display */
    tm1637.init();
    tm1637.set(BRIGHT_TYPICAL);
/* declare the red_led pin as an OUTPUT */
    pinMode(BLINK_LED, OUTPUT);
}
/* the loop() method runs over and over again */
void loop() {
    analog_value = analogRead(MOISTURE_PIN); /* read the value from the sensor */
/* if the value is smaller than threshold, turn on led */
    if(analog_value < THRESHOLD_VALUE) {
        _handle_led(ON);
    } else {
        _handle_led(OFF);
    }
    memset(bits, 0, 4); /* reset array when we use it */
    for(int i = 3; i >= 0; i--) {
/* get single bits of the analog value */
        bits[i] = analog_value % 10;
        analog_value = analog_value / 10;
        tm1637.display(i, bits[i]); /* display by 4-digital display */
    }
    delay(200);
}
```

## Resources

- [**Eagle&PDF**][Grove - Moisture Sensor v1.4 Schematic](https://github.com/SeeedDocument/Grove_Moisture_Sensor/raw/master/resources/Grove%20-%20Moisture%20Sensor%20v1.4.zip)


## Tech Support
Please do not hesitate to contact [techsupport@seeed.cc](techsupport@seeed.cc) if you have any technical issue. Or submit the issue into our [forum](http://seeedstudio.com/forum/).
