# IOE LaOs
IOElectro Oscilloscope and Logic analyzer Software for windows 

![IOE LaOs](https://user-images.githubusercontent.com/64005694/128669961-694f6df9-49ea-4a5c-9213-45637b15288f.jpg)


[**Download software**](https://github.com/simple-oscilloscope/software/releases/latest/download/IOE-LaOs.zip)

### Available hardware
- [Hardware](https://github.com/simple-oscilloscope/simple-oscilloscope-hardware)

### Description
It use serial port by sending and receive some command in baud rate 115200.<br>For pilot chart, 2000 byte of data must be received !

### Commands

| Name               | Command     | I/O  | Example           | Description                                              |
| ------------------ | ----------- | ---- | ----------------- | -------------------------------------------------------- |
| Start              | 's'         | O    | s                 |                                                          |
| Stop               | 'q'         | O    | q                 |                                                          |
| Mode               | 'm'<0 or 1> | O    | m0                | 1: Oscop<br />0: LogicA                                    |
| Sample Time    | 't'<00000 to 65535> | O    | t01000                | Oscop:<br />00000: 0.8uS<br />00001:  1.2uS<br />...<br />LogicA:<br />00100: 100us                         |
| Enable Test Pulse  | 'g'         | O    | g                 |                                                          |
| Disable Test Pulse | 'h'         | O    | h                 |                                                          |
| One Shoot Trigger | 'o'         | O    | o                 |                                                          |
| Data               |             | I    | 0x00 , 0xFF , ... | uint8_t Data[2000]<br />0x00: 0.0 Volt<br />0xFF: 3.3 Volt |
