# **Test Plan and Output**

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

