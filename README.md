# Automated Pet Feeder System

## Table of Contents
1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [System Architecture](#system-architecture)  
4. [Inputs and Outputs](#inputs-and-outputs) 
5. [Usage](#usage)  
6. [Testing and Results](#testing-and-results)  
7. [Limitations and Future Improvements](#limitations-and-future-improvements)  
8. [License](#license) 

---

## Project Overview
The **Automated Pet Feeder System** is designed to automatically feed cats and dogs at scheduled times while monitoring their food consumption. The system integrates a real-time clock, weight sensor, and infrared sensor to ensure proper feeding and alert staff if any issues arise, such as empty food bins or uneaten food.  

---

## Features
- Automatic feeding at scheduled times using a **real-time clock**.  
- Food consumption monitoring using **weight sensors** and **infrared sensors**.  
- Alerts for staff when:  
  - Food is not consumed.  
  - Food bin is empty.  
  - Mechanical or sensor errors occur. 
- Log system for tracking feeding events and issues.  

---

## System Architecture
The system uses a combination of sensors and actuators:  

**Inputs:**  
- **Food bin level sensor (Infrared):** Checks remaining food percentage.  
- **Bowl weight sensor:** Measures food consumption by comparing weight before and after feeding.  
- **Real-time clock:** Tracks current time and triggers scheduled feedings.  

**Outputs:**  
- **Servo motor:** Dispenses food based on schedule and consumption status.  
- **Alert signal:** Notifies staff of issues.  
- **Message log display:** Stores feeding events, issues, and alerts.  

---

## Usage
- The system continuously monitors the current time and scheduled feeding times.  
- When a scheduled feeding time is reached:  
  1. The system checks the food bin level.  
  2. If food is available, the servo motor dispenses the appropriate amount.  
  3. After a wait timer, the bowl weight sensor checks food consumption.  
  4. Logs are updated and alerts are sent to staff if any issues are detected.  

---

## Testing and Results

1. **Normal Feeding (Pet eats as expected):**  
   - Log: “Feeding successful”  
   - Outcome: System operates correctly under normal conditions.

2. **Pet does not eat:**  
   - Log: “Food hasn’t been consumed”  
   - Outcome: Alert staff; configurable timers per pet may improve accuracy.

3. **Food bin empty:**  
   - Log: “Feeding failed – food bin empty”  
   - Outcome: Alert staff; future improvements could include low-food warnings before empty (<10% capacity).

4. **Sensor error:**  
   - Log: “Feeding failed – mechanical error”  
   - Outcome: Staff alerted for troubleshooting; ensures system reliability.

5. **Pet interferes with food (false triggers):**  
   - Possible incorrect logs if pets knock food out of the bowl.  
   - Future improvement: integrate a camera or motion sensor for more accurate monitoring.  

---

## Limitations and Future Improvements
- Designed for **one type of pet** and **dry food only**.  
- Limited storage for multiple pets simultaneously.  
- Requires electricity and proper supervision.  
- Future improvements:  
  - Multi-pet support and customizable feeding portions.  
  - Camera or motion sensors for better consumption monitoring.  
  - Advanced low-food warnings and automatic refill integration.  

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.  

