# Electronic Voting Machine using LPC2148 Microcontroller

This project implements a simple and secure **electronic voting system** using the **LPC2148 ARM7 microcontroller**.  
Candidate names are displayed on a 16x2 LCD, and voters cast their votes using push buttons.  
The system records each vote, counts the totals, and displays the final winner.

---

##  Features
- Built using **LPC2148 (ARM7)** microcontroller  
- **16x2 LCD** for displaying candidates and results  
- **Push buttons** for casting votes  
- **LED indicator** for “Voted” status  
- Displays the winning candidate on the LCD screen  

---

##  Circuit Connections

###  LCD (16x2) Connections
| LCD Pin | Function | LPC2148 Pin |
|----------|-----------|-------------|
| 1 (VSS) | GND | GND |
| 2 (VDD) | +5V | +5V |
| 3 (VEE) | Contrast | Potentiometer (middle pin) |
| 4 (RS) | Register Select | P0.8 |
| 5 (RW) | Read/Write | GND |
| 6 (EN) | Enable | P0.9 |
| 11 (D4) | Data Bit 4 | P0.10 |
| 12 (D5) | Data Bit 5 | P0.11 |
| 13 (D6) | Data Bit 6 | P0.12 |
| 14 (D7) | Data Bit 7 | P0.13 |
| 15 (LED+) | Backlight + | +5V |
| 16 (LED–) | Backlight – | GND |

---

###  Push Buttons (Voting Inputs)
| Button | LPC2148 Pin | Description |
|---------|--------------|-------------|
| Button 1 | P1.24 | Candidate 1 |
| Button 2 | P1.25 | Candidate 2 |
| Button 3 | P1.26 | Candidate 3 |

> Each button is connected with a **1 kΩ pull-up resistor** to +5V.  
> One terminal goes to the LPC2148 pin, and the other to GND.

---

###  LED Indicator (Voted Status)
| LED Pin | Connection |
|----------|-------------|
| Anode (+) | +5V via 1 kΩ resistor |
| Cathode (–) | P0.22 |

> LED turns ON when a vote is successfully cast.

---

###  Power & Clock
| Signal | Connection |
|---------|-------------|
| V3A, VREF | +3.3V |
| VSS | GND |
| VBAT | +3.3V |
| XTAL1, XTAL2 | 12 MHz crystal with 22 pF capacitors |

---

##  Working Principle
1. The system initializes and displays candidate names on the LCD.  
2. Voter presses a push button to select their candidate.  
3. The vote is recorded and the “Voted” LED turns ON.  
4. Once voting is complete, the system displays total votes and the winning candidate.

---

##  Tools & Components
- **LPC2148 Development Board**  
- **16x2 LCD Display (LM016L)**  
- **Push Buttons (3 units)**  
- **Yellow LED**  
- **Resistors (1 kΩ)**  
- **Crystal Oscillator (12 MHz)**  
- **Proteus / Keil µVision / Flash Magic**

---

##  Circuit Diagram
*(Insert your Proteus screenshot here)*  
`![Circuit Diagram](path-to-your-image.png)`

---

##  Author
**Tungala Sriram**  
🎓 Electronics and Communication Engineering (ECE)  
🔗 [GitHub Profile](https://github.com/yourusername)

---

## License
This project is open-source under the **MIT License**.
