# Requriements
  
## **High Level Requriements**
 
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
