# Hardware PWM
Russell Binaco:
By using the CCRX Capture mode, Timer outputs can be driven directly to an output pin. Depending on the board, the on-board LEDs may be a pin option to drive to. 
The MSP430CCR1 output drives LED2 in this manner.
In the code, OUTMOD_7 indicates that the pin is set high on CCR0 reset, and set low on the CCR1 capture, which is the same implementation as in the software PWM code.
All of the boards successfully implement hardware PWM. 

#Implementation note
The G2553 board uses PXSEL and PXSEL2, whereas FR series boards use PXSEL0 and PXSEL1 and the F5529 only uses P1SEL.
This is the signal that chooses CCR1 output on a particular pin.