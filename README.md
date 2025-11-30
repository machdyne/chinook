# Chinook Computer

Chinook is a metacomputer designed by Lone Dynamics Corporation.

![Chinook](https://github.com/machdyne/chinook/blob/aa77e6321abd63277f30fb7f759388b9844e7b1b/chinook.png)

This repo will contain schematics, PCB layouts, pinouts, a 3D-printable case and documentation.

Find more information on the [Chinook product page](https://machdyne.com/product/chinook-computer/).

## Bootloader

Chinook uses the [rv003usb](https://github.com/cnlohr/rv003usb) bootloader to support firmware updates over the USB-C connector. If overwritten, it can be restored with the SWIO pin and an external programmer.

## Linux

Chinook uses a slightly modified [fork](https://github.com/machdyne/linux-ch32v003) of [linux-ch32v003](https://github.com/tvlad1234/linux-ch32v003).

Build with `make -f Makefile.chinook`.

## Power

Chinook can by powered through the barrel jack connector (or the PWRJACK pin) or the USB-C connector.

## Pinouts

### Left connector

This connector is compatible with HC-05/06 bluetooth modules, make sure the pins match the pinout below when plugging the module in (it may need to be upside down).

| Pin | Signal | Description |
| --- | ------ | ----------- |
| 1 | NC | not connected |
| 2 | TX | MCU UART transmit / bluetooth RX |
| 3 | RX | MCU UART receive / bluetooth TX |
| 4 | GND | Ground |
| 5 | PWR5V0 | 5V output |
| 6 | HCEN | High = HC-05/06 UART mode, Low = AT comamnd mode |

### Right connector

This connector is for general purpose I/O and optional power input/output.

| Pin | Signal | Description |
| --- | ------ | ----------- |
| 1 | GPIOA | GPIO / I2C SCL |
| 2 | GPIOB | GPIO / I2C SDA |
| 3 | GPIOC | GPIO / ADC1 |
| 4 | GPIOD | GPIO / ADC0 |
| 5 | SWIO | MCU programming pin |
| 6 | GND | Ground |
| 7 | PWR3V3 | 3.3V output |
| 8 | PWRJACK | Power input (9-15V) connected to barrel jack |

## License

The contents of this repo are released under the [Lone Dynamics Open License](LICENSE.md).

Note: You can use these designs for commercial purposes but we ask that instead of producing exact clones, that you either replace our trademarks and logos with your own or add your own next to ours.
