# can_bus

#### 介绍

The LseeStudio shield uses MCP2515, MCP2551 and 16MHz oscillator.
It can reuse the SeeeStudio CAN Shield library.

NOTICE: The shiled in picture is an old edition and DOES NOT reserve SCL/SDA pins near AREF pin.

![image](https://gitee.com/sunarvin/can_bus/raw/master/images/CAN-BUS_Shield.jpg)


For waveshare 2-CH CAN HAT, the sentences in config.txt replace the settings in dts/dtb and enable CAN0 and CAN1 on the shield.

dtparam=spi=on
dtoverlay=mcp2515-can1,oscillator=16000000,interrupt=25
dtoverlay=mcp2515-can0,oscillator=16000000,interrupt=23

Then the rpi finds the MCP2515 and inserts can_raw module automatically.
