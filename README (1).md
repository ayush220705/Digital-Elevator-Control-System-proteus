# Digital Elevator Control System

A digital logic-based elevator control system designed and simulated in **Proteus Design Suite** using 74-series logic ICs.

The system allows a user to select a destination floor, compares it with the current floor, determines whether the elevator should move UP or DOWN, and displays the floor using 7-segment displays.

---

## Project Overview

This project demonstrates an elevator control system implemented using **solid-state digital logic**, without a microcontroller.

The system uses counters, comparators, flip-flops, logic gates, and 7-segment display drivers for floor selection, floor storage, floor comparison, direction control, and floor indication.

---

## Working Principle

The selected floor is stored using the **74LS174 register**. The **7485 magnitude comparator** compares the selected floor with the current floor.

    Floor Selection
           |
           v
    74LS174 Register
           |
           v
    7485 Comparator
           |
       +---+---+
       |   |   |
       v   v   v
      UP  STOP DOWN
       |   |   |
       +---+---+
           |
           v
    74191 UP/DOWN Counter
           |
           v
    7447 BCD Decoder
           |
           v
    7-Segment Display

### Direction Logic

| Condition | Action |
|---|---|
| Current Floor < Selected Floor | UP |
| Current Floor > Selected Floor | DOWN |
| Current Floor = Selected Floor | STOP |

---

## Components Used

| Component | Function |
|---|---|
| **74191** | 4-bit UP/DOWN counter |
| **7485** | 4-bit magnitude comparator |
| **74LS174** | D-type flip-flop register |
| **7447** | BCD-to-7-segment decoder |
| **7408** | AND gates |
| **7432** | OR gates |
| **NOT Gates** | Signal inversion |
| **7-Segment Displays** | Floor indication |
| **Logic Switches** | Floor selection |
| **Clock Source** | Counting pulses |

---

## System Architecture

The system is divided into several functional sections.

### 1. Input Interface

Logic switches are used to select the desired destination floor.

### 2. Memory Section

The selected floor is stored using the **74LS174 flip-flop register**.

### 3. Comparator Section

The **7485 comparator** compares the selected floor with the current floor.

### 4. Control Logic

Logic gates generate the required **UP, DOWN, or STOP** control signals.

### 5. Counter Section

The **74191 counter** tracks the elevator's current floor by incrementing or decrementing according to the movement direction.

### 6. Display Section

The **7447 decoder** converts the counter output for display on the 7-segment display.

---

## Proteus Simulation

The complete circuit was implemented and tested using **Proteus Design Suite**.

The input switches can be changed to test different floor selections. The comparator determines the movement direction and the counter updates the current floor.

### Circuit Diagram

![Digital Elevator Control System](Images/elevator-circuit.png)

---

## Key Features

- Digital floor selection
- Automatic UP/DOWN control
- Current floor tracking
- Comparator-based control
- 7-segment floor display
- Flip-flop based floor storage
- Solid-state digital logic
- No microcontroller required
- Proteus simulation

---

## Objectives

- Understand combinational and sequential digital logic.
- Design an elevator control system using 74-series ICs.
- Implement floor comparison and direction control.
- Demonstrate digital counting and state tracking.
- Simulate a real-world elevator control concept using Proteus.

---

## Software Used

**Proteus Design Suite**

---

## Project Files

- [Project Report](Documentation/DEC_Project_Report.docx)
- [Proteus Simulation](Proteus/Digital_Elevator_Control_System.pdsprj)
- [Circuit Image](Images/elevator-circuit.png)

---

## How to Run

1. Download or clone this repository.
2. Open the `Proteus` folder.
3. Open `Digital_Elevator_Control_System.pdsprj`.
4. Run the simulation in Proteus.
5. Use the input switches to select a destination floor.
6. Observe the UP/DOWN control.
7. Monitor the current floor on the 7-segment display.

> **Note:** A compatible version of Proteus Design Suite is required.

---

## Future Scope

- Physical PCB implementation
- Multi-floor request handling
- Automatic door control
- Emergency stop system
- Weight/load sensing
- Advanced elevator scheduling
- Microcontroller-based expansion

---

## Author

**Ayushman Sethy**  
**B324011**  
**IIIT Bhubaneswar**  
**Electrical & Electronics Engineering**

---

## Documentation

For detailed information about the project, refer to the [Project Report](Documentation/DEC_Project_Report.docx).

---

## License

This project is created for educational and academic purposes.
