# Pygmy

Flight computer design for my TRA L1 certification flight. The name is a play on the fact that it's designed to be small
and also runs on a Pi (Py) chip.

## Motivation

I am a computer systems engineer. I like electronics and computers. I like flying rockets and the challenges of embedded
flight computer systems. Therefore I would like to make a simple flight computer for my simple rocket, since that will
probably be the better engineered part of my L1 flight.

## Components

RP2040-based MCU because this is for an L1 and it does not need to be a beefy, complicated system. It's got everything I
need, good support on the RTOS I'm using (Apache NuttX) and plenty of cheaply available development boards. No floating
point unit but two cores, which should be speedy enough.

- LSM6DSO32 IMU (I2C0)
- EEPROM (I2C0)
- LIS2MDL (I2C0)
- MS5607 (I2C0)
- RN2483 using SMA @433MHz (UART1)
- SAM-M8Q GPS (UART0)
- MicroSD card (SPI0)
- USB-C console/shell
- Arming terminal block
- Voltage regulator for 5V USB or 3V7 Li-Ion/LiPo battery power

With this setup I should be able to debug during ground testing, record plenty of flight data, transmit telemetry and
know everything I need to about my rocket's orientation, acceleration, position and altitude. I can also nicely program
it over USB.

This design is heavily based on the 2025 design of CU InSpace's rocket avionics (which I of course helped to design,
hence my imitation) and the old InSpace telemetry designs. The primary difference is the MCU and also the fact that my
design is a complete single-board design because I naively think I can get the RF stuff good enough for an L1 on the
first try (and I also don't want to pay for and deal with two separate boards).

I am not using an LDO because I want efficiency and we've powered our sensors/RN2483 off of switching regulators before
without any major issues. I'm taking pains to smooth the voltages and isolate the regulator though.
