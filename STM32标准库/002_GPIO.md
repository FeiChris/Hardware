# STM32F103ZET6

### GPIO

##### 概述

​			GPIO即通用输入输出，用于数字输入输出，F103ZET6芯片拥有112个 I/O 引脚，分别在GPIOA，GPIOB，GPIOC，GPIOD，GPIOE，GPIOF，GPIOG共7个端口，每个端口有0--15共16个引脚



##### 输入输入

GPIO可以配置8种模式，4种输入，4种输出

-   普通推挽输出      可输出高低电平，常用于LED，蜂鸣器等简单的数字器件
-   普通开漏输出      只能输出低电平，要输出高电平需要外接上拉电阻电源，常用于需要5V的情况
-   复用推挽输出      常用作USART或SPI
-   复用开漏输出      常用于IIC
-   上拉输入             默认上拉至高电平输入
-   下拉输入             默认下拉至低电平输入
-   浮空输入             用于不确定高低电平输入，如外部按键或者USART接收Rx
-   模拟输入             外部模拟信号





##### 输出速度

GPIO输出时需要设置速度，通常为输出信号速度的5—10倍，有三种速度可配置

1.   2Mhz            LED，蜂鸣器等普通设备输出引脚，USART复用输出

2.   10MHz         IIC

3.   50MHz         SPI，FSMC

     

#### 库函数

----

GPIO_DeInit()                   恢复默认值

GPIO_Init()                        初始化GPIO

GPIO_SetBits()				 引脚置高电平

GPIO_ResetBits()             引脚置低电平

GPIO_Write()                    向指定端口写入数据

GPIO_ReadInputDataBit()   	读取指定引脚的输入值（1Bit）

GPIO_ReadINputData()           读取指定端口输入值（16Bit）

GPIO_ReadOutputDataBit()   读取指定引脚的输出值（1Bit）

GPIO_ReadOutputData)()       读取指定端口输出值（16Bit）

GPIIO_EXTLineConfig()            选择用作外部中断/事件的GPIO引脚

GPIO_PinRemapConfig()         改变指定外设的复用引脚映射