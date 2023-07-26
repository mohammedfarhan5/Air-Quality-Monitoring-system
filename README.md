# Air-Quality-Monitoring-system
Created an Air quality Monitoring System which measures indoor harmful gases present in air like Carbon Dioxide(CO2),humidity and temperature using MQ135 sensor. The device would be showing the air quality in PPM on the LCD display provided.
# Components Used
Arduino uno R3

16*2 display

MQ135 gas sensor

jumper wires

Bread board

I2C SP serial interface Module Port
# Architecture
![Architecture](https://github.com/mohammedfarhan5/Air-Quality-Monitoring-system/assets/139696698/f194b175-e83c-4956-8e1c-f6d3576ce0c2)
# Software code
void setup() {
  Serial.begin(9600);
}

void loop() {

int analogValue = analogRead(mqPin);

float voltage = analogValue * (5.0 / 1023.0);

float resistance = ((5.0 * 10.0) / voltage) - 10.0;

Serial.print("Analog Value: ");

Serial.print(analogValue);

Serial.print(", Voltage: ");

Serial.print(voltage);

Serial.print("V, Resistance: ");

Serial.print(resistance);

Serial.println("KOhms");

 if (analogValue > smokeThreshold) 
 {
 
Serial.println("Smoke detected!");
}

 delay(1000); 
 
}
# Working


https://github.com/mohammedfarhan5/Air-Quality-Monitoring-system/assets/139696698/beeff61a-cbc4-42b3-abdd-3ef252cede5b

