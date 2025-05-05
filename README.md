# Embedded and Real-Time Systems: HVAC Control Simulation

![Image](https://github.com/user-attachments/assets/eda90dac-a115-4769-bc3d-afacd4b3fd97)

## Project Overview
This project simulates an HVAC (Heating, Ventilation, and Air Conditioning) control system using **Proteus**. The system monitors temperature and humidity from three sensors, calculates their averages, and controls a heater, cooler, and humidifier based on predefined thresholds. The goal is to maintain optimal environmental conditions by leveraging state machines for device control.

---

## Key Features
1. **Multi-Sensor Input**:  
   - Three DHT22 sensors measure temperature and humidity.  
   - The system calculates the average values for decision-making.

2. **Device Control Logic**:  
   - **Cooler**:  
     - **Low mode**: Activated when temperature > 32°C.  
     - **High mode**: Activated when temperature > 38°C.  
     - Turns off when temperature < 28°C.  
   - **Heater**:  
     - **Low mode**: Activated when temperature < 20°C.  
     - **High mode**: Activated when temperature < 15°C.  
     - Turns off when temperature > 23°C.  
   - **Humidifier**:  
     - **Low mode**: Activated when humidity < 80%.  
     - **High mode**: Activated when humidity < 70%.  
     - Turns off when humidity > 85%.  

3. **State Machine Design**:  
   - Super-states (`Idle`, `Low`, `High`) and sub-states ensure efficient transitions.  
   - Parallel execution for temperature (heater/cooler) and humidity (humidifier) control.  

4. **Proteus Simulation**:  
   - Virtual terminal displays real-time sensor data and averages.  
   - LED indicators show device states (e.g., white LED for cooler in Low mode).  

---

## Project Deliverables
1. **State Diagrams**:  
   - Diagrams for cooler, heater, and humidifier with transitions between `Idle`, `Low`, and `High` states.  
2. **Proteus Simulation**:  
   - Circuit design and screenshots of the simulation in action.  
3. **Documentation**:  
   - Explanation of thresholds, control logic, and hardware setup (e.g., pin assignments for LEDs and sensors).  

---

## Example Simulation Scenarios
- **Cooler Activation**:  
  - When average temperature exceeds 32°C, the cooler starts in Low mode (white LED on).  
  - At 38°C, it switches to High mode (blue LED on).  
- **Humidifier Control**:  
  - Humidifier activates in Low mode (blue LED) when humidity < 80%.  
  - Switches to High mode (purple LED) if humidity drops below 70%.  

---

## Tools Used
- **Proteus**: For circuit design and simulation.  
- **Arduino**: Embedded C code for state machine logic (not included in this README).  

---

## How to Use
1. Open the Proteus simulation file.  
2. Run the simulation to observe device behavior under varying temperature/humidity inputs.  
3. Monitor the virtual terminal for sensor data and state transitions.  

---

**Note**: Full project documentation (including state diagrams and simulation screenshots) is available in the repository.  
