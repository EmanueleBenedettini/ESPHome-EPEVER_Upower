# ESPHome-EPEVER_Upower
Code and instructions for the integration of EPEVER Upower inverters in Home Assistant


In upower.yaml change YOURAPIENCRIPTIONKEY(19), YOUROTAPASSWORD(22) and YOURPASSWORD(31) to match yours.
The code is small enough to fit in an esp01_1M and still provide ota update capability.

I've included my board design made whit eagle, just go to a site like jlcpcb.com and upload the Gerber.zip file. 
You'll need to solder some components:
R5,R6: 3.3k, M1206
R1,R2: 10k, M1206
R4: 120, M1206
U2: AMS1117-3.3, SOT229P700X180-4N
Q1: 2N7002 N-Channel mosfet or similar, SOT23
IC1: MAX485, SO08
C1,C2: 100u 6mm diameter

U1 is the ESP01 and in my case it didnt need to be soldered, it's just a tight fit