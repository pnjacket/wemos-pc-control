# PC Control for Home Assistant using Wemos D1 Mini
I have spent numerous hours to make the Wake-On-LAN function working on the ethernet port of my motherboard and failed miserably. It is very hard to believe that the feature has been there for decades, yet it is often very poorly implemented in my consumer grade motherboards. It also does not help to have different setup steps when upgrade and lose this convenient feature all the time. That is why I have decided to create a small device to handle general PC power controls, such as power on/off, reset, etc, using an external micro controller so that I do not have to worry about it every time the PC is upgraded.

## General architecture
### Microcontroller
There are three major requirements for this
1. Wifi
the Wifi connection is the most important requirement of all because it is how the micro controller will maintain its own connection to the home assistant instead of relying on the computer's connection.
2. UART connection
I would like to recieve a bit of information from the PC than just on/off signal from the motherboard header. This will help me figure out if the computer is ready for the work or hang somewhere. It can be used to grab any information necessary from PC side and send over to the microcontroller so it can be consumed as necessary, and decouples the computer from the home assistant.
3. Price
The last point being the price. I am intending to have this thing created all 4 PCs that I am managing.

There are some options that can be used for this purpose. I have looked into ESP family of microcontrollers, Arduino boards and Raspberry pi(especially Zero w). For the ease of use and avilability, I have decided to go with ESP8266 based Wemos D1 mini. It checks all the boxes and easy to program.


Still writing....
