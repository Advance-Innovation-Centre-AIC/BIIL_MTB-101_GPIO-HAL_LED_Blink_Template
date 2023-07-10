# BIIL_MTB-101_GPIO_LED_Blink_Template
### Lab Objective:
The objective of this lab is to familiarize students with the basic concepts of GPIO (General Purpose Input Output) using a PSoC 6 microcontroller from Cypress (CY8CKIT-062S2-43012 Infineon Board). By the end of this lab, students should be able to initialize GPIOs, manipulate GPIO states, and create basic delay functions.

### Lab Description:
In this lab, students will be tasked with programming a PSoC 6 microcontroller to control an LED through a GPIO. The LED will be made to blink at a regular interval, demonstrating basic GPIO output functionality.

### The code will:
1. Initialize the board and all necessary peripherals.
2. Initialize a GPIO pin (connected to the LED) as an output.
3. Create an infinite loop where it:
    - Drives the LED GPIO pin low, turning the LED on.
    - Waits for 250 milliseconds.
    - Drives the LED GPIO pin high, turning the LED off.
    - Waits for another 250 milliseconds.
This sequence will result in the LED blinking on and off every 250 milliseconds.

## 🔥 Requirements
| Resources                                  | Links                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Computer                                   | 💻                                                                                                    |
| ModusToolbox™ software v3.0 or later       | [Link](https://www.infineon.com/modustoolbox)                                                         |
| CY8CKIT-062S2-43012 Infineon Board         | [Link](https://github.com/Advance-Innovation-Centre-AIC/BIIL_MTB-100_Hello_World_and_LED_Blinking_Programming_Template/assets/88732241/0215501d-b774-4045-8e64-ef49e28d8404) |
| Technical Report | [dropbox](https://www.dropbox.com/scl/fi/amaxc94pte0ut2i1r5ewx/Technical-Report-Lab00.paper?rlkey=b3xm3vrerz9xgv1glb30cvy9z&dl=0)



## 🚩 Let start
- 👉  Open Eclipse IDE ModusToolbox               
![image](https://github.com/Advance-Innovation-Centre-AIC/BIIL_MTB-100_Hello_World_and_LED_Blinking_Programming_Template/assets/88732241/276b5ee3-7752-488c-baa7-3b55f6615b27)                 

- 👉  Select board    
![image](https://github.com/Advance-Innovation-Centre-AIC/BIIL_MTB-100_Hello_World_and_LED_Blinking_Programming_Template/assets/88732241/df637b74-1bee-4c0c-9bdc-4b70d7f0cee8)

- 👉  Select Application         

#### Note add pic....

    - Coding:
    ```
    for (;;)
    {
      	 /* Drive CYBSP_USER_LED low (LED on) */
  		cyhal_gpio_write(CYBSP_USER_LED, 1);
  
  		/* Wait 250 ms */
  		cyhal_system_delay_ms(250);
  
  		/* Drive CYBSP_USER_LED high (LED off) */
  		cyhal_gpio_write(CYBSP_USER_LED, 1);
  
  		/* Wait 250 ms */
  		cyhal_system_delay_ms(250);
    }
    ```
    - `for (;;) { ... }`: This is an infinite loop. Everything within this loop will be repeated indefinitely. This is common in embedded systems where the program is meant to run until the device is powered off.
    - `cyhal_gpio_write(CYBSP_USER_LED, 0);`: This sets the state of the CYBSP_USER_LED GPIO pin to low (0 volts), which typically turns the LED on.
    - `cyhal_system_delay_ms(250);`: This waits for 250 milliseconds.
    - `cyhal_gpio_write(CYBSP_USER_LED, 1);`: This sets the state of the CYBSP_USER_LED GPIO pin to high (usually 3.3 or 5 volts, depending on the microcontroller), which typically turns the LED off.
    -`cyhal_system_delay_ms(250);`: This waits for another 250 milliseconds.

This sequence makes the LED blink - it will be on for a quarter of a second, then off for a quarter of a second, continuously.
- 👉  Build Application      

- 👉  Launching Program
  - Before launching the program to the board, make sure that you have already connected the board to the computer through USB cable.        
![image](https://github.com/Advance-Innovation-Centre-AIC/BIIL_MTB-100_Hello_World_and_LED_Blinking_Programming_Template/assets/88732241/7a6bb6ef-cb63-4613-98a1-42f9617ad724)
  - Launching Program    

- 👉  Check the Result
  - You will see `Hello World!!!` on the serial terminal.         
   ![image](https://github.com/Advance-Innovation-Centre-AIC/BIIL_MTB-100_Hello_World_and_LED_Blinking_Programming_Template/assets/88732241/2eb45911-1df7-4581-9e73-2e79c28364a5)
  - LED Blinking        
    ![image](https://github.com/Advance-Innovation-Centre-AIC/BIIL_MTB-100_Hello_World_and_LED_Blinking_Programming_Template/assets/88732241/e43ee093-c57b-4d65-81a2-e8326e729b74)

### 🎉  Congratulations! You can now complete Lab100 by creating, building, and launching the application program.


## Supported toolchains (make variable 'TOOLCHAIN')

- GNU Arm&reg; embedded compiler v10.3.1 (`GCC_ARM`) - Default value of `TOOLCHAIN`
- Arm&reg; compiler v6.16 (`ARM`)
- IAR C/C++ compiler v9.30.1 (`IAR`)

## Supported kits (make variable 'TARGET')

- [PSoC&trade; 62S2 Wi-Fi Bluetooth&reg; pioneer kit](https://www.infineon.com/CY8CKIT-062S2-43012) (`CY8CKIT-062S2-43012`)
- [PSoC&trade; 62S1 Wi-Fi Bluetooth&reg; pioneer kit](https://www.infineon.com/CYW9P62S1-43438EVB-01) (`CYW9P62S1-43438EVB-01`)
- [PSoC&trade; 62S1 Wi-Fi Bluetooth&reg; pioneer kit](https://www.infineon.com/CYW9P62S1-43012EVB-01) (`CYW9P62S1-43012EVB-01`)
- [PSoC&trade; 62S3 Wi-Fi Bluetooth&reg; prototyping kit](https://www.infineon.com/CY8CPROTO-062S3-4343W) (`CY8CPROTO-062S3-4343W`)


## Related resources
Resources  | Links
-----------|----------------------------------
ModusToolbox™ Software Training | [link](https://www.dropbox.com/sh/waj898o4o8eccx0/AAB3hBBaIQo2OvJ5-fubGJIha/training-modustoolbox-level1-getting-started-master/Manual/Ch2-Tools.pdf?dl=0)



## Other resources

Infineon provides a wealth of data at www.infineon.com to help you select the right device, and quickly and effectively integrate it into your design.


## Document history

Document title: *BILL_MTB-101* – *GPIO LED Blink Template*

 Version | Description of change
 ------- | ---------------------
 1.0.0   | Lab101: Introduction to GPIO control with PSoC 6, featuring an LED blinking .


## Authors:
- *Assoc. Prof. Wiroon Sriborrirux*
- *Mr. Sriengchhun Chheang*
- *Mr. Sabol Socare*
<br>

<br>

---------------------------------------------------------

© BDH Corporation, 2022-2023
