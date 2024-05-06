# Experiment-no-6-DC-Motor-Speed-Control-Using-Arduino

###  NAME: PRAJIN S
###  DATE: 08-04-2024
###  ROLL NO : 212223230151
###  DEPARTMENT: ARTIFICIAL INTELLIGENCE AND DATA SCEINCE

### AIM : To control the speed and the direction of a DC motor using L293D driver ic( H- bridge)

### Components Required:
•	Arduino UNO board
•	L293D driver
•	12V DC motor
•	10K ohm potentiometer
•	Pushbutton
•	12V source
•	Breadboard
•	Jumper wires
### THEORY 
The L293D quadruple half-H drivers chip allows us to drive 2 motors in both directions, with two PWM outputs from the Arduino we can easily control the speed as well as the direction of rotation of one DC motor. (PWM: Pulse Width Modulation).
Arduino DC motor control circuit:
Project circuit schematic diagram is the one below.

![image](https://user-images.githubusercontent.com/36288975/167763051-b230c183-afc5-46f2-ba95-0f95e10dd6c9.png)
FIGURE-01 H BRIDGE CIRUCIT INTERFACE 
 
The speed of the DC motor (both directions) is controlled with the 10k potentiometer which is connected to analog channel 0 (A0) and the direction of rotation is controlled with the push button which is connected to pin 8 of the Arduino UNO board. If the button is pressed the motor will change its direction directly.
The L293D driver has 2 VCCs: VCC1 is +5V and VCC2 is +12V (same as motor nominal voltage). Pins IN1 and IN2 are the control pins where:
![image](https://user-images.githubusercontent.com/36288975/167763120-1421c2c5-8381-49eb-b376-03f6e1113b7a.png)
TABLE-01 EXITATION TABLE FOR H BRIDGE 

As shown in the circuit diagram we need only 3 Arduino terminal pins, pin 8 is for the push button which toggles the motor direction of rotation. Pins 9 and 10 are PWM signal outputs, at any time there is only 1 active PWM, this allows us to control the direction as well as the speed by varying the duty cycle of the PWM signal. The active PWM pin decides the motor direction of rotation (one at a time, the other output is logic 0).

### PROGRAM 
```
int i1=5;
int i2=6;
int en=3;
void setup()
{
  pinMode(i1,OUTPUT);
  pinMode(i2,OUTPUT);
  pinMode(en,OUTPUT);
}
void loop()
{
  analogWrite(en,255);
  digitalWrite(i1,HIGH);
  digitalWrite(i2,LOW);
  delay(500);
}
```
### Schematic Simulation
![Screenshot 2024-04-05 161520](https://github.com/Prajin19/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/144979377/875210b8-c270-4f1d-a7ef-264c670c1a56)

FIGURE 02 OFF CONDITION


![Screenshot 2024-04-05 161508](https://github.com/Prajin19/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/144979377/ea66845c-55e1-4978-bb3c-b96e62864b8f)



FIGURE 03 ON CONDITION
### OUTPUT
![Screenshot 2024-04-05 161622](https://github.com/Prajin19/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/144979377/46874da2-3389-47c1-8b19-8f7e98207843)


### GRAPH AND TABULATION 




![Screenshot 2024-04-05 161318](https://github.com/Prajin19/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/144979377/ed8bb82f-43a2-44dc-9864-e64d73b30f28)
FIGURE 04 GRAPH





![Screenshot 2024-04-05 161306](https://github.com/Prajin19/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/144979377/068a966c-a912-44dd-a238-81a15d3b2e96)
TABLE 02


### RESULTS
The speed and the direction of DC motor is controlled using a L293D driver ic( H- bridge) successfully and tabulated.

