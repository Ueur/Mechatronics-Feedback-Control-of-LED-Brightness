# Mechatronics - Feedback Control of LED Brightness
This is the second to last project of the course MECH_ENG_333, which I took in the winter of 2021. It uses C, PuTTY, and MATLAB to use feedback control to alter the brightness of an LED. This project uses counter/timer, output compare, and analog input peripherals, as well as the parallel master port for the LCD screen. The sensor that measures the brightness of the LED tracks the desired brightness, as shown by the square waves in MATLAB in the demo video, demonstrating that the feedback control is successful.

It is coded in C, and the PIC32 microcontroller is wired to generate a pulse-width modulation waveform that serves as the reference in which the brightness of the LED emulates. The efficacy of this feedback control is measured by a photoelectric sensor, communicated to the computer via PuTTY, and plotted in MATLAB. Feedback control is used in many technologies, from adjusting the temperature on the thermostat to the speed on a car.

## How to run

1. Wire the circutboard as shown in the picture in the assignment writeup.
2. Load talkingPIC.c navigating to the "project" folder in the command prompt. 
3. Build the project by typing ```make```, which would assemble the C files into O object files.
4. Put the PIC32 into receive mode by pressing the RESET and USER buttons on the microcontroller.
5. Run ```make write```, which would activate the bootloader utility nu32utility and program the PIC32 with out.hex.
6. Open a serial port in MATLAB by running talkingPIC.m. 
7. PIC32 will send 200 plot points to MATLAB running the code in pid_plot.m

## Notes

The final iteration of the project is in the "project" folder. The resistor values, amongst others, can be changed and modified according to need. A working video is available in this repository in "demo", as well as the assignment write-up.

## License

[MIT](https://choosealicense.com/licenses/mit/) 
