# Kerala IoT Challenge Documentation

Foxlab Makerspace in association with GTech - Group of Technology Companies in Kerala is launching our prestigious program  “Kerala IoT Challenge 2021”,  with a vision to mould 100 IoT experts in Kerala, hosting on the MuLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

### Expirement 1 : Hello World LED Blinking
**Components Required**
- Arduino Uno Board
- USB Cable
- LED (Any Color) x 1 Nos
- 220 OHM Resistor X 1 Nos
- Breadboard
- Jumper Wires (Male to Male ) X 2 Nos

**Setup**

![1](https://user-images.githubusercontent.com/80213907/132119329-dc13fdd8-9654-4ad7-b878-0814a6f13167.jpeg)


code

```
int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}
```

### Expirement 2: Traffic Light**
**Components Required**
- Arduino board *1
- USB cable *1
- Red M5 LED*1
- Yellow M5 LED*1
- Green M5 LED*1
- 220Ω resistor *3
- Breadboard*1
- Breadboard jumper wires* several

**Setup**

![2](https://user-images.githubusercontent.com/80213907/132119355-f173c446-5364-4dcb-89de-502519db0687.jpeg)


code
``` 
int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}
```

### Expirement 3: LED Chasing Effect**
**Components Required**
- Led *6
- Arduino board *1
- 220Ω resistor *6
- Breadboard *1
- USB cable*1
- Breadboard wire *13

**Setup**

![3](https://user-images.githubusercontent.com/80213907/132119452-0b2affbf-d818-46a8-846f-33dd6500eb28.jpeg)


code 

```
int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}
```
