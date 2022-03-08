# Introduction
* Nowadays, fire incidents have become a critical issue , which must be dealt with on time without any unnecessary delay to avoid the loss in lives and belongings . It is considered a fire situation when the monitored temperature exceeds 50o C. In critical places such as hospitals, schools, and banks, personnel's arrival time to come for help in fire hazards is around 15 minutes .

# Circuit
 ![Screenshot (205)](https://user-images.githubusercontent.com/99093515/155687234-e007d3e6-2a73-495e-a8c2-e099d96192b3.png)

 # Requirements

# **High Level Requriements**
 
|HLR(ID)|Description|
--- | --- | 
|HLR01|	Senses the time to time temperature in the building|
|HLR02|	Compares with the regular room Temperature|	
|HLR03|	Rings the buzzer if temperature is High then room temperature|
|HLR04| Rings the buzzer if any Fire or Smoke is detected in the building|
|HLR05| Shows the status on the LED screen|

## **Low Level Requriements**
   
|LLR(ID)|Description|
--- | --- | 
|LLR01_HLR_01| Smokesensor sends the high if fire/smoke is detected|
|LLR02_HLR_02| Temperature sensor compares the room temperature with avg room temperature|
|LLR03_HLR_02| The sensor sends high if temperature is High else sends low  |
|LLR04_HLR_02| The processor takes the input|	
|LLR05_HLR_02| processor sends high signal to buzzer|
|LLR06_HLR_04| The buzzer rings if the fire/smoke is detected|
|LLR07_HLR_05| The information should be displayed on the LED screen|
|LLR08_HLR_05| if fire is detected print "Fire is Detected"|
|LLR09_HLR_05| if fire is detected print "SAFE"|

# Flowchart
![Screenshot (201)](https://user-images.githubusercontent.com/99093515/155673185-86b5b484-ecd4-4c2a-a20e-8a87da659c1e.png)

# SWOT Analysis
![Screenshot (209)](https://user-images.githubusercontent.com/99093515/155767139-2f27cbc4-3680-4730-848f-09f7cbe574db.png)

# 4W's and 1H
## what
* It is a fire alarm system which is used in helping or alerting the people when fire broke out
## where
* In the offices, schools, buildings, public places, Theatres etc
## when
* useful when the fire broke out
## why
* To alert people as fast as possible and save a lot of injuries
## How
* By ringing the buzzer and displaying on Lcd screen


# Test Plan and Output

## High-Level Requriements

|Test ID| HLR | Description| Inputs|Expected O/P | Actual O/P|
--- | --- | --- | --- | --- | --- |
|TD01|HLR01|when fire is not present|buzzer doesn't ring |o/p on screen "SAFE"|Sucess|
|TD02|HLR02|when fire is introduced near the buzzer|buzzer should ring|o/p on screen "fire detected"|Sucess|
|TD03|HLR03|when smoke is not present|buzzer dosen't ring|o/p on screen "SAFE"|Sucess|
|TD04|HLR04|when smoke is  present|buzzer should ring|o/p on screen "fire detected"|Sucess|


## Low-Level Requriements


|Test ID| LLR | Input| Expected output|message on screen| O/P|
--- | --- | --- | --- | --- | --- |
|TD01|LLR01_HLR01|if no fire detected by flame sensor| no sound generated  |  "SAFE"| no sound|
|TD02|LLR02_HLR01|if no smoke detected by smoke sensor| no sound generated  |  "SAFE"| no sound|
|TD03|LLR03_HLR01|if Temperature of room <45'C| no sound generated  |  "SAFE"| no sound|
|TD04|LLR04_HLR01|if fire detected by flame sensor| sound generated  |  "fire detected"| sound generated|
|TD05|LLR05_HLR02|if Smoke detected by Smoke sensor| sound generated  |  "fire detected"| sound generated|
|TD06|LLR06_HLR02|if Temperature > 45'C|sound generated  |  "fire detected"| sound generated|

#  Block Diagram
![Screenshot (203)](https://user-images.githubusercontent.com/99093515/155674854-22414bf2-e322-4a35-9971-8543407a3dd3.png)

# Components Used
* Micro controller ATMega 328
* Temperature sensor(which is used to check the temperature)
   But instead of the temperature sensor which is not available in the simullIde We are using the Potentiometer.
   Which Acts as a thermistor, Resists the flow of signal at low temperature and allows the flow at the particular and higher than that temperature.
* Buzzer(for cautioning the people)
* Smoke or fire sensor (which is used to detect Smoke or Fire)
* Led (Used as an indicator when the fire or smoke broke out)ss

# Conclusion
The fire detection systems proposed in the literature served fire stopping with no care of the responsiveness. Thus, this study considers the existing issues and build an efficient and effective fire detection system based on IoT technology, gas, temperature, and smoke sensors to collect the data accurately and rapidly
And alert all and help them from escape.

