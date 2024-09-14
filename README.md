[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/roshanlam/ReadMeTemplate/">
    <img src="./logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">USB OTA Firmware Integrated Custom STM Board</h3>

  <p align="center">
    USB & OTA Bootloader Firmware with Custom STM32 Board Design and Integrated Wi-Fi!
    <br />
    <a href="https://github.com/roshanlam/ReadMeTemplate/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/roshanlam/ReadMeTemplate/">View Demo</a>
    ·
    <a href="https://github.com/roshanlam/ReadMeTemplate/issues">Report Bug</a>
    ·
    <a href="https://github.com/roshanlam/ReadMeTemplate/issues">Request Feature</a>
    ·
    <a href="https://github.com/roshanlam/ReadMeTemplate/pulls">Send a Pull Request</a>
  </p>
</p>

## Table of Contents

- [USB-OTA-Firmware-Integrated-Custom-STM-Board](#usb-ota-firmware-integrated-custom-stm-board)
  - [Table of Contents](#table-of-contents)
  - [About The Project](#about-the-project)
    - [Project Workflow](#project-workflow)
    - [STM32 USB Bootloader](#stm32-usb-bootloader)
    - [STM32 OTA Bootloader](#stm32-ota-bootloader)
    - [STM32 Custom Developement Board](#stm32-custom-developement-board)
  - [Contributor](#contributor)
  - [Resources](#resources)
  - [Acknowledgements](#acknowledgements)

<!-- ABOUT THE PROJECT -->
## About The Project
[Screenshould should include USB OTA detected screenshot and PCB image]
[![Product Name Screen Shot][product-screenshot]](https://example.com)

The project involves developing a custom STM32 board with integrated USB and Over-the-Air (OTA) bootloader capabilities, featuring an onboard ESP32 Wi-Fi module. Users can flash firmware onto the STM32 microcontroller either through USB using DFU mode or wirelessly via Wi-Fi for remote updates. The USB bootloader ensures secure and validated firmware updates, while the OTA bootloader simplifies wireless updates without requiring physical access. The custom PCB is designed around the STM32F103 microcontroller, optimized for seamless USB and Wi-Fi communication. The onboard ESP32 enables the board to be used in various Wi-Fi-based projects, including IoT applications and remote monitoring systems. This makes the board highly versatile for developers working on embedded and network-connected systems.

<!-- ROADMAP -->
## Project Workflow


- **Implemented USB Bootloader**: Developed a USB bootloader using DFU mode for firmware updates via USB.

- **Implemented OTA Bootloader**: Developed an OTA bootloader using the onboard ESP32 Wi-Fi module, enabling wireless firmware updates.

- **Custom STM Board Design**: Designed a custom PCB for the STM32F103 microcontroller in KiCad, optimized for USB and Wi-Fi communication.

- **Currently Manufacturing and Testing**: The board is in the manufacturing stage. After that, I will proceed with assembly and testing.
  

## STM32 USB DFU Bootloader
![Screenshot from 2024-09-14 20-33-01](https://github.com/user-attachments/assets/9d402195-a547-463c-9dd0-7403b293701a)

The USB DFU Bootloader is a custom firmware update solution designed for STM32 microcontrollers, leveraging the USB Device Firmware Upgrade (DFU) protocol for standardized and efficient firmware updates. It initializes the USB peripheral and handles DFU control and data transfer requests through a dedicated state machine. The bootloader is placed in the flash memory's beginning and checks for boot conditions to decide whether to enter DFU mode or execute the main application. A post-build script for STM32CubeIDE automates firmware uploading using STM32CubeProgrammer, ensuring streamlined deployment and updates. This implementation supports reliable firmware management and easy upgrades in a standardized manner.

- **USB DFU bootloader sequence:**

![Screenshot from 2024-09-14 19-51-09](https://github.com/user-attachments/assets/24cde5f7-1ba8-4b21-931d-8e63031bc1cd)


## STM32 OTA Bootloader

![Screenshot from 2024-09-14 22-02-10](https://github.com/user-attachments/assets/a09a670c-4588-4679-bcb2-071e1805a806)

The STM32 OTA Bootloader enables firmware updates over UART using an ESP32 as the host for over-the-air (OTA) updates. The custom bootloader on the STM32 receives the new firmware from the ESP32, writes it to flash memory (128 KB in size), and verifies the integrity using a verifyFlashedData function to ensure data accuracy.

The ESP32 communicates with the STM32 via UART, transferring the firmware in chunks and triggering a reboot once the transfer is complete. Error handling is implemented to prevent booting corrupted firmware, ensuring the system only runs verified updates. The bootloader also carefully manages flash memory, avoiding conflicts with existing data.

This implementation allows remote firmware updates without physical access, making it ideal for field-deployed systems requiring periodic updates.
## STM32 Custom Developement Board

## Hardware and Software Used

## Features of custom dev board

<!-- CONTRIBUTING -->
## Contributor
- [Suraj Sonawane](https://github.com/SurajSonawane2415/) - [mail](mailto:surajsonawane0215@gmail.com)

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
I would like to express my heartfelt gratitude to [Prof. Sidharth Tallur](https://www.ee.iitb.ac.in/web/people/siddharth-tallur/) for his invaluable guidance and support throughout my internship at [WEL Lab, IIT Bombay.](https://www.ee.iitb.ac.in/~wel_iitb/index.php) I also extend my sincere thanks to Mr. Ankur Agrawal, Maheshwar Manghgat, and Amit Shete for providing the resources and creating a supportive environment that greatly facilitated my learning and growth during this period..

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[forks-shield]: https://img.shields.io/github/forks/roshanlam/ReadMeTemplate?style=for-the-badge
[forks-url]: https://github.com/roshanlam/ReadMeTemplate/network/members
[stars-shield]: https://img.shields.io/github/stars/roshanlam/ReadMeTemplate?style=for-the-badge
[stars-url]: https://github.com/roshanlam/ReadMeTemplate/stargazers
[issues-shield]: https://img.shields.io/github/issues/roshanlam/ReadMeTemplate?style=for-the-badge
[issues-url]: https://github.com/roshanlam/ReadMeTemplate/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/roshan-lamichhane
