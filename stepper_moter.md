# 步进电机
## 42步进电机介绍
[步进电机原理上](http://www.taichi-maker.com/homepage/arduino-tutorial-index/arduino-hardware/motor-4/)  
[步进电机原理下](http://www.taichi-maker.com/homepage/arduino-tutorial-index/arduino-hardware/motor-5/)
## A4988电机驱动板
```
接线方式：
VMOT电机电源12V 旁路电解电容保护
GND电机地
1B1A2A2B黑绿红蓝
VDD逻辑电源
GND逻辑地
ENABLE使能 低有效
MS1MS2MS3细分模式选择 000全步进 一步1.8度
RESET复位与SLEEP睡眠相接
STEP步进引脚 接PWM
DIR方向 低顺时针高逆时针
```
```
电压调节：顺时针增大，逆时针减小
VREF计算公式：VREF=IMAX*RES*8
IMAX:1.5A
RES:常见0.5欧、0.1欧、0.2欧
VREF:小于1.2V
操作方式：VDD接5VGND接地 测量旋钮和地之间电压
```
## 常见问题
* 电机丢步：1.步进电机本身工作力矩不够，没有足够能力带动负载；   
2.步进电机起停的加减速过程不充分，步进电机在加减速过程中失步；   
3.步进电机的电源功率不够导致步进电机的输入功率不够引起失步；   
4.步进电机的驱动电压不够或者驱动电流设定过低；   
5.驱动器或者控制器收到信号干扰；   
6.步进电机系统共振引起步进电机带负载能力下降而导致失步；   
7.驱动器和控制器的信号不匹配；   
8.同步轮或者减速箱的背隙或者来回转到的间隙误差没有在程序上补偿或者补偿值不对；   
9.控制程序本身有问题。  
* 电机响声：电机停止时正常电流声
* A4988发热：电流过大，电机转速过慢
## 相关链接
[A4988驱动NEMA步进电机(42步进电机)–太极创客](http://www.taichi-maker.com/homepage/reference-index/motor-reference-index/arduino-a4988-nema-stepper-motor/#question)  
[A4988驱动模块使用详解（附：电流调节方法）](https://www.cnblogs.com/huayizi/p/9627585.html)  
[步进电机失步（丢步）的原因和对策](https://blog.csdn.net/mao_hui_fei/article/details/78715530)  
