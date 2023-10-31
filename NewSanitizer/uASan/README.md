# ASan for Cortex-M

I have deal with bugs in programs, servers and my bicycles from time to time in the past few months, and recently also in embedded devices. :-)

And today I realized that an ASan like stuff could be doable on my STM32 F103/F407/F429 (Cortex-M) toy boards, for both bug detection and capability exploration against those bare-metal programs. This idea really excites me!

 - Toolchain
   - LLVM Embedded Toolchain for Arm
     - https://developer.arm.com/Tools%20and%20Software/LLVM%20Toolchain
     - https://github.com/ARM-software/LLVM-embedded-toolchain-for-Arm
   - Arm GNU Toolchain
     - https://developer.arm.com/Tools%20and%20Software/GNU%20Toolchain
     - https://developer.arm.com/downloads/-/arm-gnu-toolchain-downloads
   - I won't use [Arm Compiler for Embedded](https://developer.arm.com/en/dev2/Tools%20and%20Software/Arm%20Compiler%20for%20Embedded), although it's used most frequently in my past EE life...
 - Reading
   - [ASAN on embedded platform (Cortex-M) ?](https://groups.google.com/g/address-sanitizer/c/2nWqFgNiWH8)
   - [Finding Memory Bugs with Google Address Sanitizer (ASAN) on Microcontrollers](https://mcuoneclipse.com/2021/05/31/finding-memory-bugs-with-google-address-sanitizer-asan-on-microcontrollers/)
   - https://github.com/ErichStyger/mcuoneclipse/tree/master/Examples/MCUXpresso/tinyK22/tinyK22_FreeRTOS_ASAN
   - [STM32F1 Series Documentation](https://www.st.com/en/microcontrollers-microprocessors/stm32f1-series/documentation.html)
   - [STM32F4 Series Documentation](https://www.st.com/en/microcontrollers-microprocessors/stm32f4-series/documentation.html)
   - [The Definitive Guide to ARM Cortex-M3 and Cortex-M4 Processors](https://www.oreilly.com/library/view/the-definitive-guide/9780124080829/)
   - [Retargeting printf via ITM](https://electronics.stackexchange.com/questions/152315/printf-style-debugging-via-swd)
   - [OpenOCD](https://openocd.org/)
