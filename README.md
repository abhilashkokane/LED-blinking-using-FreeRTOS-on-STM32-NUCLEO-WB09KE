# LED-blinking-using-FreeRTOS-on-STM32-NUCLEO-WB09KE

## Project Overview
This project demonstrates the use of **FreeRTOS** on the **STM32 NUCLEO-WB09KE** development board to implement a basic multitasking system where multiple LEDs are blinked at different rates. The project also integrates **Segger SystemView** for runtime analysis, providing insights into CPU usage, task execution times and system tick behavior.

---

## About STM32 NUCLEO-WB09KE
The **STM32 NUCLEO-WB09KE** board is based on the **STM32WB09** microcontroller from STMicroelectronics. Key features:
- ARM® Cortex®-M0+ 32-bit core
- Ultra-low power wireless MCU with **Bluetooth Low Energy (BLE 5.3)**
- 128 KB Flash memory and 12 KB SRAM
- Integrated ST-LINK debugger/programmer with USB interface

---

## Blinking LEDs using FreeRTOS
In this project, LED blinking is managed using **FreeRTOS tasks** instead of traditional `HAL_Delay()` loops. FreeRTOS provides:
- **Task Scheduling** – Each LED blink pattern is implemented as a separate task. The scheduler ensures fair CPU time allocation.
- **Deterministic Timing** – Using system ticks, tasks are executed at precise intervals.
- **Concurrency** – Multiple LEDs can blink at different frequencies without blocking each other.
- **Scalability** – More tasks (e.g., UART communication, sensor reading) can be easily added.

---

## Runtime Analysis with Segger SystemView
To evaluate system performance, **Segger SystemView** is integrated for real-time tracing and analysis:
- **CPU Usage** – Monitors how much processing time is consumed by tasks vs. idle time.
- **Task Execution Time** – Measures the run time of individual tasks for performance tuning.
- **SysTick Monitoring** – Observes FreeRTOS tick interrupts and scheduler behavior.

---

## Tools & Technologies
- **STM32CubeIDE** – Project development and debugging
- **FreeRTOS** – Real-time operating system
- **Segger SystemView** – Runtime tracing and analysis
- **STM32 NUCLEO-WB09KE** – Target development board

---

## 📷 Demo
(Add screenshot or gif of LEDs blinking + SystemView trace if available)

---
