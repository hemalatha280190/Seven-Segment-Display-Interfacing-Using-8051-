# Seven Segment Display Interfacing Using 8051
## Aim:
To interface a seven-segment display with the 8051 microcontroller and display digits 0 to 9 sequentially using an assembly language program in Keil and simulate it in Proteus.
## Apparatus Required:
<br>Laptop with Keil uVision software
<br>Proteus Design Suite
## Circuit Diagram Setup in Proteus:
1.	Open Proteus and create a new project.
2.	Add the following components from the library:
<br>8051 Microcontroller (AT89C51)
<br>Seven Segment Display (Common Anode/Cathode)
<br>Resistors (330Ω)
3.	Connect:
<br>Seven Segment Display to Port P2 of the microcontroller.
<br>Power (VCC & GND) and appropriate resistors.
4.	Save the design and proceed to programming in Keil.
## Algorithm:
1.	Load DPTR with the address of the lookup table containing seven-segment hex values.
2.	Load R1 with 10 (loop counter for digits 0-9).
3.	Fetch digit patterns from the lookup table and send them to P2.
4.	Call a delay subroutine.
5.	Increment DPTR to get the next digit pattern.
6.	Repeat steps 3-5 until all 10 digits are displayed.
7.	Repeat the process infinitely.
## Program:
## Explanation:
1.Lookup Table (0100H - 0109H): Stores hexadecimal values for displaying digits 0-9.
2.MOVC A, @A+DPTR: Retrieves the corresponding segment pattern for the digit.
3.MOV P2, A: Sends data to Port 2, which is connected to the seven-segment display.
4.ACALL D: Calls the delay subroutine to maintain visibility of each digit.
5.Delay Subroutine: Creates a time delay using nested loops.
6.SJMP L: Runs the digit display sequence in an infinite loop.
## Simulation in Proteus:
1.	Open Proteus and load the HEX file generated from Keil.
2.	Connect P2 of the microcontroller to the seven-segment display.
3.	Run the simulation and observe the digits 0 to 9 appearing sequentially.
## Output:
The seven-segment display will show digits 0 to 9 sequentially with a delay between each digit.
## Result:
The seven-segment display has been successfully interfaced with the 8051 microcontroller, and the digits 0 to 9 are displayed sequentially using Keil and Proteus.

