# Power_Management_STM32

## Overview

This project demonstrates three low-power modes of the STM32 Nucleo-F446RE: Sleep, Stop, and Standby modes.

- In Sleep and Stop modes, the MCU can be woken up by pressing the B1 user button (PC13).
- In Standby mode, the MCU can be woken up by a rising edge on the WKUP pin (PA0).
- An ammeter can be connected at JP6 to measure the current consumption in each power mode.

Note: Connect a serial terminal configured for USART2 communication to observe the MCU's behavior.

## Hardware

- STM32 Nucleo-F446RE development board
- USB connection to PC

## Software and Tools

- STM32CubeIDE
- STM32CubeMX
- STM32 HAL
- C programming language

## Features

- Implements Sleep, Stop, and Standby modes using the STM32 HAL power management APIs.
- Configures EXTI interrupts to wake the MCU from Sleep and Stop modes.
- Configures the PWR wake-up pin to resume execution from Standby mode.
- Deinitializes GPIO and UART peripherals before entering low-power modes and reinitializes them after waking up when applicable.
- Uses USART2 to display power-mode status messages on a PC serial terminal.

## Project Structure

- `Core/Inc/` — application header files
- `Core/Src/` — application source files
- `Drivers/` — STM32 HAL and CMSIS dependencies
- `.ioc` — STM32CubeMX configuration file
