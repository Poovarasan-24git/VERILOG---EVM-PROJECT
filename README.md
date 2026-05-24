# VERILOG---EVM-PROJECT
You can use the following content in your GitHub README for your EVM project.

# Electronic Voting Machine (EVM) using Verilog

## Project Description

This project implements an **Electronic Voting Machine (EVM)** using **Verilog HDL**. The design simulates a voting system where a user can cast a vote for one among four candidates. Each candidate has an independent vote counter that increments whenever a vote is registered.

The project is developed using basic digital design concepts such as counters, multiplexing logic, sequential circuits, and clock-based operations.

---

## Objective

The objective of this project is to design a simple digital voting system capable of:

* Accepting votes from users
* Identifying the selected candidate
* Counting votes accurately
* Displaying vote counts for each candidate
* Resetting vote counts when required

---

## Features

* Supports **4 candidates**
* Uses **2-bit select lines** to identify candidates
* Uses **individual counters** for vote counting
* Includes **reset functionality**
* Supports simulation and waveform verification
* Designed using Verilog HDL

---

## Working Principle

1. The system starts with all vote counts initialized to zero.
2. A **vote signal** acts as the voting button.
3. A **2-bit select signal (`sel`)** selects the candidate:

   * `00` → TVK
   * `01` → DMK
   * `10` → ADMK
   * `11` → NTK
4. When `vote = 1`, the selected candidate's counter increments by one.
5. Vote counts are stored and updated on every positive clock edge.
6. Reset clears all vote counts.

---

## Block Diagram

```text
                  +------------------+
Vote Signal ----->|                  |
                  |                  |
Select Signal --->|   EVM Controller |
                  |                  |
Clock ----------->|                  |
Reset ----------->|                  |
                  +------------------+
                          |
          ---------------------------------
          |        |        |            |
          ↓        ↓        ↓            ↓
       TVK      DMK      ADMK         NTK
     Counter   Counter  Counter     Counter
          |        |        |            |
          --------------------------------
                          |
                    Display Output
```

---

## Technologies Used

* Verilog HDL
* Vivado/ModelSim simulator
* Digital Logic Design concepts

---

## Verilog Concepts Used

* Sequential circuits
* Counters
* Multiplexing logic
* Clock and reset operations
* Case statements
* Testbench generation

---

## Simulation Result

The simulation verifies that:

* Votes are counted correctly
* Selected candidate count increases
* Reset clears all vote values
* Outputs update according to the clock signal

---

## Future Improvements

* Add password protection
* Restrict multiple voting
* Add debouncing for push buttons
* Display result using 7-segment display
* Automatically identify the winning candidate

---

This project demonstrates the practical implementation of digital design concepts through a real-world application using Verilog HDL.
