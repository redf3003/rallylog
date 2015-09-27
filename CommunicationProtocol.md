# Introduction #



# Details #

RallyLog implements the [ModBus](http://en.wikipedia.org/wiki/Modbus) RTU Slave Protocol used to communicate with the configuration software


### Registers ###


#### Read Only Registers (Command 3) ####
| **No.** | **Addr.** | **Variable** | **Description** | **Unit** | **Read/Write** |
|:--------|:----------|:-------------|:----------------|:---------|:---------------|
|0        | 0x0       | Status       | Device Status (See Status Table Below) |          | R              |
|1        | 0x1       | Station\_Id  | Station ID      | 0-99     | R              |
|2        | 0x2       | Vbat         | Battery voltage | 0.1V     | R              |
|3        | 0x3       | HW\_VERSION  | Hardware Version | String   | R              |
|4        | 0x4       | FW\_VERSION  | Firmware Version  B2=Minor B1=Major | String   | R              |
|5~7      | 0x5~7     | Rfid\_Tag    | Last RFID Tag Read (5 Bytes)|String    | R              |
|8~11     |0x8~B      | RTC          | Last RTC  Read (See RTC Register Table Below)| BCD      | R              |

#### Read/Write Registers (Read Command 3) (Write Command 6) ####
| **No.** | **Addr.** | **Variable** | **Description** | **Unit** | **Read/Write** |
|:--------|:----------|:-------------|:----------------|:---------|:---------------|
|12       | 0xC       | Periph\_Ctrl | See Peripheral control table below |          | R/W            |
|13       | 0xD       | Station\_Id\_Cfg | Station ID      | 1-99     |W               |
|14~19    | 0xE~13    | Rtc\_Cfg     | RTC Config (See RTC Register Table Below)|          | W              |

### Peripheral Control Table ###

| BIT0 | RFID\_EN | Control the RFID Reader 0=Off 1=On|
|:-----|:---------|:----------------------------------|
| BIT1 | LCD\_BL\_EN | LCD BackLight (Diag Only)         |
| BIT2 | LED\_GRN\_EN | Green LED (Diag Only)             |
| BIT3 | LED\_RED\_EN | Red LED (Diag Only)               |
| BIT4 | BATT\_EN | Enable Battery Read (Diag Only)   |
| BIT5 | RTC\_CLEAR | Clear RTC Fault  1=Clear (Diag Only)|
| BIT6 | RTC\_START | Start RTC 0=Stop 1=Start (Diag Only)|
| BIT7 | Reserved |                                   |
| BIT8 | Reserved |                                   |
| BIT9 | Reserved |                                   |
| BIT10 | Reserved |                                   |
| BIT11 | Reserved |                                   |
| BIT12 | Reserved |                                   |
| BIT13 | Reserved |                                   |
| BIT14 | Reserved |                                   |
| BIT15 | DIAG\_EN | Diagnostic Mode 0=Normal 1=Enable |

### RTC Register Table ###

| BYTE0 | RTC\_Second | Second |0-59|
|:------|:------------|:-------|:---|
| BYTE1 | RTC\_Minute | Minute |0-59|
| BYTE2 | RTC\_Hour   | Hour   | 0-23|
| BYTE3 | RTC\_Day    | Day    |0-31|
| BYTE4 | RTC\_Month  | Month  |1-12|
| BYTE5 | RTC\_Year   | Year   |0-99|
| BYTE6 | RTC\_Cal    | Calibration Drift Correction | 0-63 |


### Status Table ###

| BIT0 | RFID | RFID Reader 0=Off 1=On |
|:-----|:-----|:-----------------------|
| BIT1 | BAT\_LOW| BatteryOK 0=Ok 1=Low   |
| BIT2 | SD\_IN| SD Card Inserted 0=Out 1=In|
| BIT3 | BTN\_LEFT| Left button Pushed     |
| BIT4 | BTN\_MIDDLE| Middle button Pushed   |
| BIT5 | BTN\_RIGHT| Right button Pushed    |
| BIT6 | LCD\_BL | LCD Backlight 0=Off 1=ON |
| BIT7 | Reserved |                        |
| BIT8 | RTC\_STOPPED| RTC Stopped 0=Normal 1=Stopped |
| BIT9 | RTC\_FAULT| RTC Fault 0=Normal 1=Fault|
| BIT10 | Reserved|                        |
| BIT11 | Reserved|                        |
| BIT12 | Reserved|                        |
| BIT13 | Reserved|                        |
| BIT14 | Reserved|                        |
| BIT15 | Reserved|                        |











