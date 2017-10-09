# Software PWM
Russell Binaco:
Software pulse width modulation is implemented by using Timer_A in upmode: it will count to CCR0, which sets the period by turning on the LED, and CCR1 compare mode can be used to shut off the LED at some value less than CCR0. CCR1/CCR0 *100 is the duty cycle.
A button increases CCR1 by 10% duty cycle each press, going from 0% to 100%.
Each board successfully implemented Software PWM

## Extra Work
### Linear Brightness
By using a switch statement on selected log-based CCR1 values, each increment can increase brightness at a visually linear rate.
All of the boards use this implementation.