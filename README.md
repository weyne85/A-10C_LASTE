# DCS LASTE Script
## 📁 Script
### 🛩️ LASTE Wind/Temp Correction — A-10C / A-10C II
<img width="602" height="464" alt="607566030-717ebe49-bb59-497f-95fe-f5d75359b653" src="https://github.com/user-attachments/assets/d6d29a46-fa98-4235-ac76-dc3678fbdf91" />
In an A-10 Thunderbolt II, LASTE stands for **Low Altitude Safety and Targeting Enhancement**.

LASTE is the system that makes low-level A-10 attacks accurate and survivable. It integrates ballistic computation, autopilot modes, and weapon delivery into a single system, using wind and temperature data across multiple altitude layers to calculate correct weapons impact points. Without it properly programmed, your bombs and rockets will not hit where your pipper says they will — this script makes sure you always have the right numbers before you roll in.

- This script pulls live in-mission weather data directly from the pilot's aircraft position and formats it ready to type straight into the CDU scratchpad — no math, no conversion needed.*

**Features**
- Winds and temps at all 4 CDU altitude tiers (00, 02, 08, 26)
- Wind output pre-formatted as 5-digit strings (e.g. 08001)
- Live QNH in inHg for your altimeter
- Local magnetic variation for the theatre
- Per-pilot display — MP safe, blue coalition only
- Built-in step-by-step CDU entry guide in the readout
- F10 menu driven — request or clear on demand

**Requirements**
- MOOSE Framework

**Mission Editor Setup**
1. Create a trigger: TYPE: Mission Start → ACTION: Do Script File → select Moose.lua
2. Create a trigger: TYPE: Once → CONDITION: Time More (5) → ACTION: Do Script File → select A10_laste_Winds_MP.lua

**In-Game Usage**
F10 Other → LASTE → Request LASTE Winds

⚠️ The F10 LASTE menu will only appear if you are seated in an A-10C or A-10C II aircraft slot.

**Setting the correct QNH**
<img width="872" height="778" alt="607564365-fee1c4c6-ccf8-4b70-b357-22a198a648c5" src="https://github.com/user-attachments/assets/7a544593-0cd1-4453-8353-8e8058a01d8f" />

**It is important to set the QNH correctly before entering LASTE data. The QNH displayed in the script output (in inHg) must be dialled into the altimeter pressure knob — the small knob on the lower left of the altimeter. Getting this right ensures your altimeter reads true altitude, which is the foundation for accurate weapons delivery at all altitude tiers.**
