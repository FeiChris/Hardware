# STM32F103ZET6

### GPIO通用输入输出

##### 输出

需要配置速度——输出驱动电路的响应速度

​    2MHz   LED，蜂鸣器等普通输出引脚，USART

​    10MHz   I2c

​     50MHz   SPI，FSMC

+   推挽输出   GPIO_Mode_Out_PP

##### 输入

不用配置速度

+   上拉输入       默认引脚为高电平                    GPIO_Mode_IPU
+   下拉输入       默认引脚为低电平                    GPIO_Mode_IPD
+   浮空输入       由外部输入决定        GPIO_Mode_IN_FLOATing

#### 库函数

----

GPIO_Init()                        初始化GPIO

GPIO_SetBits()				 引脚置高电平

GPIO_ResetBits()             引脚置低电平

GPIO_ReadInputDataBit()       读取指定引脚的输入值