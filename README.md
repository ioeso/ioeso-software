# IOE LaOs
IOElectro LaOs (Oscilloscope and Logic analyzer) Software for windows 

![IOE LaOs](https://user-images.githubusercontent.com/64005694/128121791-bf230be6-1b4f-4b07-9fdd-b04a75292165.jpg)

[**Download software**](https://github.com/ioelectro/ioe-laos/releases)

### Available hardware
- [STM32F0](https://github.com/ioelectro/stm32f0-laos)

### Description
It use serial port by sending and receive some command in baud rate 115200.<br>For pilot chart, 2000 byte of data must be received !

### Commands

| Name               | Command     | I/O  | Example           | Description                                              |
| ------------------ | ----------- | ---- | ----------------- | -------------------------------------------------------- |
| Start              | 's'         | O    | s                 |                                                          |
| Stop               | 'q'         | O    | q                 |                                                          |
| Mode               | 'm'<0 or 1> | O    | m0                | 1: Oscop<br />0: LogicA                                    |
| ADC Sample Time    | 'a'<0 to 7> | O    | a0                | 0: 0.8uS<br />1:  1.2uS<br />...                         |
| Enable Test Pulse  | 'g'         | O    | g                 |                                                          |
| Disable Test Pulse | 'h'         | O    | h                 |                                                          |
| Data               |             | I    | 0x00 , 0xFF , ... | uint8_t Data[2000]<br />0x00: 0.0 Volt<br />0xFF: 3.3 Volt |
