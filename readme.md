# Ecran ssd1306 sur ESP8266 Mini D1

## GPIO du ESP8266 Mini D1

![ESP8266 Mini D1 GPIO](esp8266-wemos-d1-mini-pinout_1.png)

## Bibliothèque

Ajouter la bibliothèque :

`SP8266 and ESP32 OLED driver for SSD1306 display`

Source : [ThingPulse/esp8266-oled-ssd1306](https://github.com/ThingPulse/esp8266-oled-ssd1306)

## Exemple de code

```cpp
#include "SSD1306.h"

// I2C PIN
#define SCL_PIN 4 // D2 on esp
#define SDA_PIN 5 // D1 on esp

SSD1306  display(0x3C, SCL_PIN, SDA_PIN);

void setup()   {
  display.init();
  display.flipScreenVertically();
  display.drawString(0, 0, "Hello world !");
  display.display();
}

void loop() {
}
```
