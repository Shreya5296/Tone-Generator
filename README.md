# Tone-Generator

The online simulator works exactly like the actual circuit, we need to do the wiring and all but this time it will be on the simulator.
Simulator Link --- https://wokwi.com/

First, we need to sign up
After signing in you can select the board. As we can see a lot of boards are there, we will select ESP32 BOARD
After selecting ESP32
We can see three buttons over there,
Add component button
Start Simulation
Settings Property

To save, rename, delete, create files, and upload files Click on the small triangle icon next to Library

Step -1:Select the material from the Simulator
● 1 x ESP32
● 1 x Buzzer Click on + Sign and select Buzzer

Step -2: Let’s do connections:
● Click on OLED Black wire and then drag it to the ESP32 GND pin.
● Click on Buzzer Red wire and then drag it to the ESP32 Pin no 26.

Let’s write the code.

Step-1: Define and declare variables:
● Define buzzer and assign I/O pin D26 
Initialize using void setup() function

Step-2: Initialization under setup() function
● void setup() is used to initialize
● Describe pinMode() for Buzzer Pin Mode() :PinMode() will declare Buzzer as digital OUTPUT
● Serial.begin() Serial.begin(9600) is used for data exchange data speed. This tells the Arduino to get ready to exchange messages with the Serial Monitor at a data rate of 9600 bits per second. That's 9600 binary ones or zeros per second and is commonly called a baud rate.
● Syntax for serial.begin : Serial.begin(speed)
● Set up delay()
● digitalWrite() will make the buzzer value LOW a the beginning.

Step-3: Execution of the main process:
void loop() function is used to execute the main process. The active buzzer will only generate a sound when it is electrified. 
If Pin is electrified then using digitalWrite() function changes the state of the Buzzer High or Low.
Set a delay of 100 ms between the HIGH and LOW state of Buzzer

Output:
Click on the Save button and then click on the simulation button
● You will hear the buzzer sound

Suppose we want to play Jingle bells on the buzzer.
1. We must now the piano notes for the Jingle bells.
2. We must have frequencies for notes.
3. Let’s make an array of Melody
4. After making Melody, the next task is to use frequencies
5. Now, you make the connections

The next step is to set the Melody timings, speed, stop time, and rest time between two melodies
Set the MELODY Length, tempo, pause time, and rest time
● Define the datatypes, Int is used for integer values
● MAX_LENGTH is used to the set the size or total time of the MELODY
● Tempo can be defined as the pace or speed at which a section of music is played. Set the tempo
● Set the Pause time between melody
● Set the rest_length between melody
● Define the tone and variable beat and set value =0

To produce a tone, a speaker is pulsated rapidly on and off and this can be done using PWM (PULSE WIDTH MODULATION) to create frequencies.
Our main purpose is to send the Pulse to the speaker to play a tone for a certain amount of time
1. Define the variable elased_time which is used to keep the track of how long we pulsed. long is the data type like int, the only difference is used to store large range values.
2. The BUZZER will only generate a sound when it is electrified. Now make the BUZZER Tone HIGH OR LOW as per duration. If the tone has played less long than 'duration' then make the BUZZER
OUTPUT HIGH.
3. If the tone has played longer than 'duration' then makes the BUZZER OUTPUT LOW.
4. digitalWrite() function changes the state of the Buzzer HIGH or LOW.
5. delay microseconds function stops the program for the amount of time (in microseconds) specified by the parameter.
6. Syntax:delayMicroseconds(us) us: the number of microseconds to pause.
7. Keep track of the tone and how long we pulsed
8. To repeat the melody after rest_count use the for loop
else make the Buzzer LOW

Call the main loop
● Play the loop till MAX_Length
● Set the bear 50
● Duration will be calculated as per tempo and beat
● Call the function playTone()
● Set the pause using delayMicroseconds

Output:
Click on the Save button and then click on the simulation button
● You will hear the melody.
