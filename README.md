# AquaTrident
AquaTrident, as its name suggests, is an aquaculture control/feedback system that monitors vital aquatic parameters, such as pH, Turbidity and TDS, designed for monitoring and regulating the environment conditions to be adequate for marine life specific types, in addition to providing real life data of the controlled system. 











<img width="1280" height="902" alt="c2e9d251-4545-43a5-a7b6-ca73751aa066" src="https://github.com/user-attachments/assets/5781a49f-2bdf-47d0-acdf-14e79d5f8ec6" />
<img width="826" height="573" alt="4f7e2d54-9d40-4ce1-b2d0-a852733aa8c2" src="https://github.com/user-attachments/assets/e7a241ce-6d38-4e91-9a53-7d12257c28fa" />
<img width="1312" height="672" alt="image" src="https://github.com/user-attachments/assets/4388f4ac-6c88-4f3a-8bff-953bcc380ae9" />


---
## How to reCreate this project:

### Pre-Construction: - 
1-	Aquaculture system was decided; parameters (pH, TDS, and Turbidity) were acquired from research and setpoints’ windows were established based on Tilapia fish’s vital conditions.
2-	Desired Sensors (pH, TDS, and Turbidity), actuators (water pump, solenoid valve and aerator) and other electronics were identified, purchased and prepared  from storess. 
3-	Datasheets, tutorials, sample codes and calibration procedures were previewed and analyzed providing accurate basic information.
---
### System design and Programming: 
1-	Electric circuit was planned consequently the wiring diagram and pins’ connections were defined as shown in (The 1st and second Image), where this schematic diagram was visualized and simulated using “KiCad” software ensuring right connections. 
2-	Based on sample codes along with modifications, system’s feedback / control logic such as (IF–THEN rules) and (ON/OFF- control) was implemented using “Arduino IDE” software as shown, where if the parameters setpoints’ windows were exceeded, a signal is transmitted activating the actuators to recover the systems optimal conditions, in addition to a database library of 2 different aquatic species ensuring system modifiability.
---
### Construction & Connections:
1-Using bread board and jumper wires, sensors’ signal pins were connected to Arduino’s analog pins (A0, A1, A2) enabling real time monitoring, sensors VCC pins were connected to Arduino’s 5V providing safe operating voltage, and LCD were attached to the Arduino through I2C enabling data logging.
2-Relay modules’ A2 pins were connected to Arduino’s digital pins (D5, D6, D7) along with connecting A1 pins to Arduino’s 5V and connecting all NO pins to actuators positive pins enabling control.
3-All relay’s COM (common) pins were connected to the 12V power supply and finally a common ground was established across all the circuit ensuring a stable and safe circuit. 
4-A Silicon paste coupled with Teflon tape were used to seal glass tank’s leakage, the shelf was fixed on the tank top using glue, then the bread board circuit along side with sensors and actuators were attached properly to the tank. 
--- 
### Calibration:

Two main calibration procedures were followed inside school chemistry lab:
A.	Multipoint (3-point): this method was used to calibrate the pH sensor, where voltage was measured at 3 various standard buffer solutions (4,7,10).
B.	Zero and Span: this method was used to calibrate the TDS and Turbidity sensors, where voltage was measured at (0 ppm) and (0 NTU) respectively then at (1000 ppm) and (3000 NTU) respectively.
Mapping output voltage to standard values, calibration curves were generated at Excel, driving equations that are used in code to convert raw voltage into real accurate measurements, as shown in fig ().


