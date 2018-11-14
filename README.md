# How to install a Humidity and a Temperature sensor on Arduino (DHT)

## Step 1
- Connect the right cable 5V
- Connect the cable next to the right cable to 7 (or D7)
- Connect the left cable to Ground (GND)

## Step 2
Download the DHT sensor Library on Arduino 
- Start Arduino
- Tools
- Libraries
- Install library
- Search “DHT sensor library’

![install DHT library](https://i.imgur.com/yO1dXlM.png)


## Step 3
When you’ve downloaded and installed the library, try this example code to see if the DHT sensor works:
```#include <dht.h>

dht DHT;

#define DHT11_PIN 7

void setup(){
  Serial.begin(9600);
}

void loop()
{
  int chk = DHT.read11(DHT11_PIN);
  Serial.print("Temperature = ");
  Serial.println(DHT.temperature);
  Serial.print("Humidity = ");
  Serial.println(DHT.humidity);
  delay(1000);
} 
