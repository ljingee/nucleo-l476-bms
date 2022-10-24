# NUCLEO-L476RG BMS Project

## TFT LCD

Driver: ILI9341

Reference: https://www.youtube.com/watch?v=8hypVJ2U7OE&t=104s

SPI Connection:

| NUCLEO-L476RG          | TFT LCD |
|------------------------|---------|
| +5V                    | Vin     |
| GND                    | GND     |
| D13 (PA5, SPI1_SCK))   | CLK     |
| D11 (PA7, SPI1_MOSI)   | MOSI    |
| D10 (PB6, GPIO_Output) | CS      |
| D9 (PC7, GPIO_Output)  | D/C     |
| D8 (PA9, GPIO_Output)  | RESET   |

STM32CubeMX SPI1 Settings:

| Frame Format          | Motorola     |
|-----------------------|--------------|
| Data Size             | 8 Bits       |
| First Bit             | MSB First    |
| Prescaler             | 4            |
| Baud Rate             | 20.0 MBits/s |
| Clock Polarity (CPOL) | Low          |
| Clock Phase (CPHA)    | 1 Edge       |

STM32CubeMX DMA Settings: Add DMA request for SPI1_TX.