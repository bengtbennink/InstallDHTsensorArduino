# How to install a Humidity and a Temperature sensor to your NodeMCU (DHT)

## Step 1
- Connect the right cable to 5V
- Connect the cable next to the right cable to 3 (or D3)
- Connect the left cable to Ground (GND)

![Connect DHT sensor to you NODEmcu](https://cdn.instructables.com/FBR/21OY/IDFSLSRV/FBR21OYIDFSLSRV.LARGE.jpg)

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

#define DHT11_PIN 3

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
