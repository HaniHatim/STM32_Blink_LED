# STM32 Onboard LED Blink - First Project

Welcome to our first STM32 project! 🎉

In this project, we demonstrate how to blink the onboard LED of an STM32 Nucleo board. This is a fundamental project to help beginners get started with STM32 development and understand the basics of GPIO (General Purpose Input/Output) control.

You can view the youtube tutorial here: https://youtu.be/Z0HrAgnUz8I?si=JnuyfWkWyYnPfITl

## Board Used

- **STM32 Nucleo-F429ZI**  
  (You can modify this if you're using a different STM32 board)

![Image alt](https://github.com/HaniHatim/STM32_Blink_LED/blob/025cdf3ef6f76d0cd38b3ebeadb9deec866d2a30/Images/STM32_Microcontroller.jpeg)

## What You'll Learn

- Setting up a basic STM32 project
- Configuring GPIO pins
- Toggling an onboard LED using code
- Building and flashing firmware to the board

## Tools & Environment

- **STM32CubeIDE**
- **STM32CubeMX** (optional, for pin configuration)
- **ST-Link Debugger** (comes onboard with Nucleo boards)
- C Programming

## Getting Started

First you would need to install **STM32CubeIDE** and download according to your operating system:

You can find the link here:
https://www.st.com/en/development-tools/stm32cubeide.html

![Image alt](https://github.com/HaniHatim/STM32_Blink_LED/blob/025cdf3ef6f76d0cd38b3ebeadb9deec866d2a30/Images/Screenshot%202025-05-21%20013831.png)

Once you have installed **STM32CubeIDE** create a new STM32 Project:

![Image alt](https://github.com/HaniHatim/STM32_Blink_LED/blob/1749bd27a823ab6c02709676e995e83d486b486c/Images/Screenshot%202025-05-21%20061222.png)

Then take a note of the LED lables, In my case it was PB0 this is important:

![Image alt](https://github.com/HaniHatim/STM32_Blink_LED/blob/fc6faec6700343e0e78dcdf3eee7a140e9ac6d10/Images/Screenshot%202025-05-21%20063711.png)

Once you have done that, exit the .ico file and go into main.c, and type the following code in the screenshot that is within the while loop:

**Notice that first GIOP ends with a B, as we took a note of our LED label PB0 in my case. Therefore I have wrote GPIOB then added a comma then I assigned the pin number GPIO_PIN_0. Regarding GPIO_PIN_SET this is to leave the LED on and GPIO_PIN_RESET is to leave it off. Notice that I have added a delay via HAL_Delay(1000); so that we can distinguish between the states. Time in C is recorded in miliseconds**

![Image alt](https://github.com/HaniHatim/STM32_Blink_LED/blob/b6471095e4dcace5665eef8c4913f8085e87c9fd/Images/Screenshot%202025-05-21%20064046.png)

Once your done, build the file via the hammer in the tool bar and then run the code using the green play button also on the tool bar. And the LED should turn on and off.



