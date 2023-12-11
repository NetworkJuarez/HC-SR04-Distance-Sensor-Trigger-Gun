Greeting and salutations to my makeshift simulation of a concept idea that has yet to emerge into the real world. I have created with the components I have available to simulate a motion sensor gun. The objective of the lab experiment would be to utilize the HC SR04 Distance Sensor to capture up to 2cm or 400m (0.8 inch to 157inches) with the input of a button to capture the motion while notifying the user via an LED light bulb to signal the capture is ongoing when the LED light isn’t on. In a real world setting this lab can be utilized in a mobile fashion with two LED lights to signal the user when the gun is ready to capture a distance and when the gun is recording it’s finding. The makeshift miniature lab consists of the following components: Raspberry Pi3, breadboard, 2 different 330 Ohm resistors, 4.7k resistor, HC-SR04 Distance Sensor, a single button, LEDs [just in case one is faulty], jumper wires and an active GitHub account is optional due to anyone can access this website via URL.
In order to replicate this lab, you will need the following items listed below:
Hardware Components:
•	Raspberry Pi 3 
•	Breadboard
•	330 Ohm Resistors [2 of them]
•	4.7k Resistor 
•	HC-SR04 Distance Sensor
•	Button
•	LEDs
•	Jumper Wires
•	Active Github account








Virtual Circuit Design for HC SR04 Distance Sensor Trigger Gun

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/77bc9df9-6824-4cd3-80e5-25efd0122ade)

 
WARNING! You could permanently damage your Pi, so read carefully:
•	Turn off your Raspberry Pi via unplugging it from the power source or an outlet when connecting cables to the GPIO ports.
•	Use a resistor, the LED will consumer as much voltage as it can. This may damage your Raspberry Pi
•	Use a resistor, the return signal from the HC-SR04 Distance Sensor could damage your Raspberry Pi.
•	Do not bend the GPIO pins.
•	Ground yourself electrically before proceeding.
•	I will be referencing the bottom GPIO Header Reference sheet *your raspberry pi may be different from mine use your best educated guess if your unsure where to connect your cables/pins
•	Throughout this documented I utilize colors to assist with the visual aid of those following along. The color of the jumper wire does not impact the overall performance of the design.

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/ee1b8e04-5601-43fe-a654-796865790b4b)

 
We shall proceed within a step-by-step format to ensure no individual is left behind if you want to follow along.
Prep Work
Open your CanaKit Raspberry Pi 3 Complete Starter Kit – 32 Gb Edition 
Install the pre-installed operating system MicroSD into the MicroSD Card Slot.
Plug your mouse and keyboard to any available USB ports that are responsive. 
[Unplug and change the USB port if unresponsive]
Plug HDMI Cable to a Monitor or TV and to your Raspberry Pi. Ensure TV or Monitor is on.
DO not plug in any cables to the 40 pin GPIO Header.
Ensure Raspberry Pi is in working condition once configured power off and unplug the 2.5 MicroUSB Power Adapter.


HC-SR04 Distance Sensor
STEP 1
Obtain the HC-SR04 Distance Sensor [blue rectangle shape component with 4 little metal rods sticking out of it] and plug into it four jumper wires that fit snug not too tight but not too flimsy either.

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/470d6fd8-5066-4ec8-b6f4-5b689ddd1605)
 
Plug the black jumper wire into the breadboard port J2. Plug the blue jumper wire into the breadboard port J3. Plug the yellow jumper wire into the breadboard port J4. Plug the red jumper wire into the breadboard port J5. 


STEP 2
 Plug the 4.7k Resistor into G2 and G7 ports within the breadboard. The resistors placed within the white breadboard helps control the voltage from the HC-SR04 Distance Sensor to the Raspberry Pi. The 330-ohm resistor in conjunction draws a total of 5 volts to not overload either the raspberry pi or HC-SR04 Distance Sensor. The 330-ohm resistor is plugged into the H3 port and the H7 port of the whiteboard.

 ![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/d97e4f9c-ae59-434d-9c3d-3bc0171d23f8)

STEP 3
Plug the black jumper wire into F2 port of the breadboard with the port in the Raspberry Pi registered as GND 6. Plug the yellow jumper wire into F4 of the breadboard into the GPIO 24 port of the Raspberry Pi. Plug the red jumper wire into the F5 of the breadboard into the 5v red 2 port of the Raspberry Pi. Plug the blue jumper wire F7 of the breadboard into GPIO 23 of the Raspberry Pi. 

 ![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/03ee7bf8-1f48-4a4e-bfc2-ecb6f650a8a2)

LED Light
STEP 1
Insert a led resistor that is 330 ohm into the breadboard port 14c and the negative blue port located near the 14a slot. [Reference image] recommend a wooden tabletop.

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/afcb4e60-152b-4112-bb44-7c7618bb60c9)
 
STEP 2
Insert your LED Light into port ensure the short end [negative electrical charge] into port 14e. The long leg [positive electrical charge] plugs itself into 17e. The point of the resistor is to limit the amount of volts needed for the LED light to ensure it ignites while not frying the port on the Raspberry Pi. 

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/083979e5-2e80-4bec-b982-c70e423c97ee)
 
STEP 3
Plug a jumper wire cable into port 17a in the breadboard and link it into the Raspberry Pi clicking into place on slot 6 registered on the GPIO Header card as GPIO 17. 

 .![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/5b54dafc-dffb-468c-9c8b-5be254f8d9be)

View the below image for a visual aid on the Raspberry Pi.

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/599e8826-0465-4001-a9e0-f405d5881c2a)
![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/38a77ab6-93d9-48e9-8324-2a42fc71643d)

 
Button Configuration
STEP 1
Unpackage a breadboard [the white rectangle labeled 1 – 30 top down and A through J left to right] and place it on a hard surface with no static buildup. I recommend a wooden tabletop. 

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/c44d597b-906d-41c0-b865-80ddaf5ce075)

Grab the button rotate and rotate it until it fits on both ends of the breadboard on the following locations: E28, E30, F28, F30. Once pressed into place we move onto the next step plugging in the jumper wires.

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/fe6908a6-824d-4b05-904e-1780639f7b1f)
 

STEP 2
Plug a jumper wire into the breadboard located in 28A then into 30A and on the bottom left blue negative side facing 30A.

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/bb659402-0280-437f-b524-a78106fa6265)
![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/d293a2ce-65b6-493e-a169-083aad1aaa25)

 
The purpose of the configuration of the button is to input a signal into the Raspberry Pi in order to trigger the LED light to go off and cause the HC-SR04 Distance Sensor to capture the surrounding via its echo pin output which records the distance is recorded from the initial trigger via the button to the foreign object and returned via a bounced returning signal.
STEP 3
Plug the yellow jumper wire into the GPIO 3 port within the Raspberry Pi. Plug the white wire into the GND 34 port within the Raspberry Pi. Plug the black jumper wire into GPIO 21 port within the Raspberry Pi.

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/c2207a16-ce99-4666-9657-cf42f0388f23)

Final Configuration
STEP 1
Once the steps for the HC-SR04 Distance Sensor, LED Light and Button configuration the image shall look similar to the following images below. I separated the HC-SR04 Distance Sensor image configuration from the LED Light and button configuration for visual clarity. 

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/d31d583a-2990-426e-a201-2595fac1bc52)
![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/971ea52b-e026-411b-a052-5699fb27fd34)

STEP 2
Reference the GPIO Header sheet accompanied with your raspberry pie and match the jumper wires with the correct positive and negative connection located from the Raspberry Pi to the breadboard. If the LED Light does not ignite diagnose it in steps. Ensure the Raspberry Pi is off/unplugged and attempt to rotate the Led light to test the correct connection point to be accurate. If the LED light does not ignite attempt another LED light and run the process again to ensure the set-up shall be running smoothly.

STEP 3

![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/4eef8038-1f50-40c0-92ca-2bcb6dab5b23)

The end product of the connection points from the breadboard to the Raspberry Pi should look similar to the image provided. The next step to move towards is the code carried within Thonny a python operated program.


Python Code Configuration

```Python

from gpiozero import Button, LED
from time import sleep
import random
from gpiozero import DistanceSensor
from time import sleep

led = LED(17)
player_2 = Button(3)

time = random.uniform(2,4)
sleep(time)
led.on()

sensor = DistanceSensor(echo=23, trigger=24, max_distance=2.0)

while True:
	if player_2.is_pressed:
		print("Registered Distance Test Recorded!")
	 distance = sensor.distance * 100
	 print("Distance: %.2f" % distance)
	 sleep(0.5)
		break
led.off()
```
![image](https://github.com/NetworkJuarez/HC-SR04-Distance-Sensor-Trigger-Gun/assets/150442086/91f30600-d812-4919-8a6c-e1f7ae925d66)
 
The image above is a initial experimental image from creating the code from different lines of trial and error within Thonny. The end result of the lab should include the user clicking the button for an initial capture via the HC-SR04 Distance Sensor accompanied with a displayed text of “Registered Distance Test Recorded”. You can view the videos located on youtube under Network Juarez for simulations of the lab working as intended and unintended.

Youtube URL: https://www.youtube.com/channel/UCfwZH5DUgszeiKwDLK_bRjQ
