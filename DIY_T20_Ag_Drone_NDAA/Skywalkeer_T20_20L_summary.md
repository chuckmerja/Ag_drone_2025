# 20L Agricultural Drone Build Specification (NDAA Compliant)

## 1. System Architecture
* **Flight Controller:** Cube Orange+ Standard Set (Blue) - NDAA Compliant, Made in USA/Taiwan.
* **Navigation:** Here4 Blue GPS - Dual-band RTK support, Blue UAS compliant.
* **Telemetry:** [RFD900x-US Bundle](http://googleusercontent.com/shopping_content/2_link) - 915MHz long-range link (20km+).
* **Frame Options:** * Production: Skywalker T20 (Foldable 20L Carbon Fiber).
    * DIY: 1200mm-1600mm heavy-lift octocopter frame.

## 2. Wiring & Port Map (ArduPilot/Cube)
| Device | Port on Cube | Signal Type |
| :--- | :--- | :--- |
| Here4 GPS | CAN 1 | DroneCAN |
| RFD900x | TELEM 1 | Serial/MAVLink |
| Pump ESC | AUX 1 (Servo 9) | PWM |
| Flow Meter | AUX 2 (Servo 10) | PWM/Digital |
| Terrain Radar | CAN 2 | DroneCAN |

## 3. Immediate vs. Deferred Procurement
### **Phase A: Buy Before 12/31/2025 (Compliance Critical)**
These are the "Blue" components that may face price hikes or restricted availability in 2026.
* **Electronics Bundle:** Cube Orange+, Here4 Blue, RFD900x modems.
* **Est. Near-Term Cost:** ~$1,200 - $1,400.

### **Phase B: Buy After 01/01/2026 (Hardware/Structural)**
Frame and propulsion are mechanical parts and less sensitive to the software-based "covered entity" bans.
* **Airframe:** T20 20L Frame + Tank.
* **Propulsion:** 4x Hobbywing X8 Motor/ESC Power Systems.
* **Spraying:** Hobbywing 8L/min Pump + Nozzle kit.
* **Est. Deferred Cost:** ~$2,500 - $3,000.

## 4. Key Setup Parameters (Mission Planner)
* `SPRAY_ENABLE` = 1
* `SERVO9_FUNCTION` = 22 (Pump Control)
* `CAN_P1_DRIVER` = 1 (Enable Here4 GPS)