# DT

![image-20201211132740139](C:\Users\lenmonpower\AppData\Roaming\Typora\typora-user-images\image-20201211132740139.png)

* ALL-IN-ONE设计
* 双路模拟量输入
* SWD调试
* 4串口
* 8接口——其中3排针有5V，3.3V供电可选；上方5pin接口有3I/O
* 蜂鸣器和4led灯用于指示

## 待完善

* can——120Ω电阻配合自锁开关实现终端电阻的选择性接入

* 切槽处理，增大热阻，减少芯片温漂

##### 12-16

<img src="C:\Users\lenmonpower\AppData\Roaming\Typora\typora-user-images\image-20201216142013493.png" alt="image-20201216142013493" style="zoom:33%;" />

芯片无法烧录。检查BOOT0，BOOT1的电平，晶振，芯片，2.2uF电容的焊接情况都没有发现问题，最后对照之前的原理图，发现13脚没接3.3V。飞线解决。

复位开关引脚接错导致MCU一直处于复位状态,焊接时调整复位开关方向，只焊了两脚，打胶加固。

##### 1-23

12V转5V的输出电感换成了33uF，spi读书竟然好了不少，不清楚是不是这个原因。意外发现插上j-link后各电源都有压降。
