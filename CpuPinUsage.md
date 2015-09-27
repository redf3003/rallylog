## I/O Summary for Rallylog ##

| **Pin No (Arduino)** | **Pin No (Phy.)** |  **Pin Name** | **I/O** | **Variable** | **Function** | **Note** |
|:---------------------|:------------------|:--------------|:--------|:-------------|:-------------|:---------|
|6                     |                   | ADC6          |I        | ADC\_BAT\_MON | Battery Voltage | 0 - 9.2V |
|2                     |                   | INT0          |I        | nBTN\_LEFT   | Left Button  | not used |
|3                     |                   | INT1          |I        | nBTN\_MIDDLE | Middle Button |          |
|4                     |                   |               |I        | nBTN\_RIGHT  | Right Button | not Used |
|5                     |                   |               |O        | nLED\_GREEN  | Green LED    | Active Low |
|6                     |                   |               |O        | nLED\_RED    | Red LED      | Active Low|
|7                     |                   |               |O        | BAT\_MON\_EN | Enable Battery Monitor Circuit | Active High |
|8                     |                   |               |O        | RFID\_EN     | Enable RFID Reader | Active High |
|9                     |                   |               |I        | RFID\_RX     | Software Serial RX in from RFID Reader |          |
|10                    |                   |CS             |O        | nSD\_CS      | SD Card Select | Active Low |
|11                    |                   |MOSI           |O        | SPI\_MOSI    | SPI MOSI     |          |
|12                    |                   |MISO           |I        | SPI\_MISO    | SPI MISO     |          |
|13                    |                   |SCK            |O        | SPI\_SCK     | SPI SCK      |          |
|14                    |                   |               |I/O      | LCD\_RS      | LCD RS       |          |
|15                    |                   |               |O        | nLCD\_BL     | LCD Backlight enable | Active Low |
|16                    |                   |               |O        | nLCD\_CS     | LCD Select   | Active Low |
|17                    |                   |               |I        | nSD\_CARD\_IN | SD Card Detect | In=High, Out=Low |
