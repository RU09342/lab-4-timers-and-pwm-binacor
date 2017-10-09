# Software Debouncing
Russell Binaco:
Software debouncing uses the watchdog timer to cause a 32ms delay when a button is pressed, pausing the program, and only executing the code for the button if the button is still held after 32ms.
Since the WDT shouldn't run normally, it is enabled when the button is pressed and disabled after the delay.
This debouncing eliminates the issue of picking up multiple posedges and/or negedges when pressing a button.
All boards have successfully implemented debouncing.

## Extra Work
### Low Power Modes
LPM0 is used for this implementation; since timers are needed LPM4 cannot be used.