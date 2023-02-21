# STM32F103ZET6

### GPIO

##### 概述

​			GPIO即通用输入输出，用于数字输入输出，F103ZET6芯片拥有112个 I/O 引脚，分别在GPIOA，GPIOB，GPIOC，GPIOD，GPIOE，GPIOF，GPIOG共7个端口，每个端口有0--15共16个引脚



##### 输入输入

GPIO可以配置8种模式，4种输入，4种输出

-   普通推挽输出
-   普通开漏输出
-   复用推挽输出
-   复用开漏输出
-   上拉输入
-   下拉输入
-   浮空输入
-   模拟输入

#### 库函数

----

GPIO_Init()                        初始化GPIO

GPIO_SetBits()				 引脚置高电平

GPIO_ResetBits()             引脚置低电平

GPIO_ReadInputDataBit()       读取指定引脚的输入值