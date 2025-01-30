---
title: "doc-dianqi"
date: 2024-01-01T23:37:07+08:00
draft: false
excerpt: ""
featured: false
katex: true
tags: [doc]
---

# 电气标准
GB/T 16733 国家标准定制程序的阶段及划分

GB/T 4728.x 电气简图用图形符号\
GB/T 6988.x 电气技术用文件的编制\
GB/T 5094.x 工业系统、装置与设备及工业部产品结构原则与参照代号

# eplan
命名系统
![](/img/Snipaste_2024-07-22_16-14-29.png)

process cell
一个process cell有自己的运行模式，可以独立于其他区域启动和停止\
process cell可以启停一个区域的设备\

1 若是一个集成项目，项目中会由不同的PLC区域组成，所以process cell名称可以按照0001依次递增\
2 若是一个大型流水线，里面的设备按照功能不同由PLC控制，则process cell也可以按照0001依次递增\
3 大型项目中的每一个PLC或单体设备PLC，可按照功能+数字的方式命名，比如PK01(Pack)

unit\
unit可以指一个process cell中某一类设备单元(EM)的集合，比如一个分拣项目的输送线\
也可以指一个流水线中的完成过一个功能的EM集合，比如包装设备中的机械臂组件\

unit的ID由两位数据组成，ID号依次由01开始递增\
1 某一部分的设备由一个一个单个EM组成，他们共同完成了一部分功能\
2 还有一部分设备由于功能需要，由多个section组成，比如机械臂，由于行走和升降两部分组成，跟此机械臂有关联的所有section应为一个unit的ID\

EM\
EM是实现基本系统功能的最小机械/软件构建块，即这是执行一个完整工艺的最小部分\
EM的ID由两位数据组成，ID号依次由01开始顺序递增\

1 若EM的unit只是一些相同功能的EM集合，EM的ID从01开始递增\
2 若EM的unit是一个独立功能的设备，因为该功能已经是标准的，所以EM数量不会变化，unit里的EM ID由01开始顺序递增\

CM\
CM是安装在机械对象上的各种传感器和执行器，它们是控制该机械部分所必须的，主要包括电动机、光电器件、接近开关等为工艺而设计的电子元器件\

CM由5位数字和英文字母组成，前面两位表示CM的功能代码，后面三位表示xx元器件
![](/img/Snipaste_2024-07-26_00-19-27.png)

对应eplan操作
![](/img/Snipaste_2024-07-26_00-26-43.png)



## 符号
符号库->符号(图形、功能点 逻辑连接点、属性)

常用符号：标识字符
![](/img/Snipaste_2024-11-18_00-25-03.png)



## 生产
### 线缆报表




ref
<PLC的标准化应用：基于西门子OMAC的面向对象的编程方法>


























# 选型
~~[电气元器件目录](https://www.kdocs.cn/l/cm6cAsgwQNDD)~~

[eclass standard](https://eclass.eu/zh/%E6%A0%87%E5%87%86-eclass/%E5%9C%A8eclass%E6%A0%87%E5%87%86%E4%B8%AD%E6%90%9C%E7%B4%A2/show?tx_eclasssearch_ecsearch%5Bdischarge%5D=0&tx_eclasssearch_ecsearch%5Bid%5D=27000000&tx_eclasssearch_ecsearch%5Blanguage%5D=3&tx_eclasssearch_ecsearch%5Bversion%5D=14.0&cHash=8fa9d83b7192212f5ee7556832c45609)

xx工作原理:\
xx参数：\
xx厂家/型号：\
xx购买渠道：\
xx设计文件:

## 接近开关
接近开关工作原理:[NPN接近开关工作过程](https://www.bilibili.com/video/BV1R541127Eq/?spm_id_from=333.337.search-card.all.click&vd_source=5f0df1465c2a6217cdfee2c39bf1d4db)
接近开关参数：
接近开关厂家/型号：
接近开关购买渠道：
接近开关设计文件:


## 断路器

断路器工作原理:
断路器参数：
断路器厂家/型号：
断路器购买渠道：
断路器设计文件:


![](/img/Snipaste_2024-11-14_22-26-14.png)
MCB断路器选型

    ACB-万能式（框架式）断路器 断路器DZ5
    MCCB-塑壳断路器
    MCB-微型断路器
    ELCB-漏电断路器 漏电断路器DZL18-20/2
    主要区别是：
    1、分断能力不同，ACB的分断能力相对较高，MCCB次之，MCB最差，当然现在有不少的MCCB的生产企业能够将MCCB的分断能力作到很高，但稳定和可靠性不好；
    2、安装的位置不同，ACB多被采用作为主断路器，因为它本身具有延时功能，能够延时分断和脱扣，而且还具有很好的通信功能和选择性，而MCCB多被采用作为配电电器，在线路的中间位置，因为它只具备分断能力和反时限脱扣能力，不具备选择性，多以只能作为下级保护开关 紧急停止开关HW ；MCB多被用在负载端，因为它的分断能力相对比较低一半为6000A和4500A；
    3、外形尺寸也相差很大，MCB的体积小，安装方便，ACB的体积最大，安装繁杂，MCCB处中间。



## 电线电缆
电线工作原理:
电线参数：载流量 颜色
电线厂家/型号：rvb rv rvsA
	已选型：bvr0.3 bvr0.5 bvr1.5 bvr2.5
	适用范围：各种移动电器、仪表、电信设备、自动化装置接线用，也可作为内部安装线，安装时环境温度不低于-15℃
	温度范围：-15℃~70℃
电线购买渠道：
电线设计文件:






ref:
search in 国家标准网: 450/750 电线 \
指定电线电缆标准的组织为：全国电线电缆标准化技术委员会 \
![](/img/Snipaste_2024-07-12_08-12-03.png)

依据标准：GB5023.x 额定电压450∕750V及以下聚氯乙烯绝缘电缆\

[统计局产品名册--电线电缆](https://www.stats.gov.cn/sj/tjbz/tjypflml/2010/39/3909.html)
![](/img/Snipaste_2024-07-12_10-43-18.png)

- 电气装备用电线电缆
- 型号
![](/img/Snipaste_2024-07-12_11-25-39.png)
- 产品
![](/img/Snipaste_2024-07-12_11-29-33.png)
![](/img/Snipaste_2024-07-12_11-32-25.png)

- 绝缘导线
![](/img/Snipaste_2024-07-12_11-04-05.png)
绝缘导线型号定义:
![](/img/Snipaste_2024-07-12_11-05-03.png)

现场电线型号：\
RV AVVR	
BVR 软导线

- 截面积计算
在不需考虑允许的电压损失和导线机械强度的一般情况下，可只按导线的允许截流量来选择导线的面积

有两种计算方式：\
1· 查表 \
裸电线：
![](/img/Snipaste_2024-07-12_11-42-31.png)
![](/img/Snipaste_2024-07-12_11-43-13.png)
绝缘导线：
![](/img/Snipaste_2024-07-12_11-44-01.png)
![](/img/Snipaste_2024-07-12_11-44-29.png)
![](/img/Snipaste_2024-07-12_11-44-49.png)
![](/img/Snipaste_2024-07-12_11-48-04.png)
![](/img/Snipaste_2024-07-12_11-48-28.png)
![](/img/Snipaste_2024-07-12_11-48-43.png)
![](/img/Snipaste_2024-07-12_11-49-03.png)
![](/img/Snipaste_2024-07-12_11-49-26.png)
2 电工口诀\
(ps. 铝芯绝缘导线明敷、环境温度为25摄氏度的条件为计算标准，载流量=截面积 乘以 一定倍数) \
10下五，100上2\
![](/img/Snipaste_2024-07-12_11-54-12.png)
25、35、四、三界\
70、95，两倍半\
穿管、温度，八、九折\
(ps. 导线不明敷，温度超过25摄氏度，载流量打八折后再打九折: 0.8*0.9 = 0.72)\
裸线加一半，铜线升级算\
(ps. 铜线截面积按照截面积排列顺序提升一级)


-ref
<最新实用电工手册.pdf>\
<电工基础 微课版>\
<实用电工速查速算手册.pdf>


## 端子
端子工作原理:
端子参数：载流量
	已选型：E1510 E2512 E0510
	类型：针形母端子 管型冷压端子 Y型绝缘压着端子 O型冷压着端子 uk系列端子 tb系列接线端子 pt直通式端子/pt直插自锁式端子
端子厂家/型号：
端子购买渠道：
端子设计文件:


[ref 端子](https://dxr54gq30qo.feishu.cn/wiki/UQnJw306eivn4vk3OwtcD5NUndb?sheet=A891K5)


[ref - xx](https://plastics-rubber.basf.com/global/zh/performance_polymers/industries/pp_electronics_and_electric/applications/application_terminal_blocks)\
在电气技术领域，端子用于连接电线和导线。在连接状态下，必须确保接触的连续性和安全性－机械固定装置确保做到这一点。接线盒可以在一条支承轨上任意并行排列，并很容易通过卡住方式进行固定。
这就定义了材料必须具备的机械性能：此用途的塑料必须具有较高的延展性能和良好的韧性－否则，在卡进去的时候就有断裂的危险。用于导线连接要求具有足够的刚性和强度。
凡是有电流通过的地方，就可能溅出火花，产生火灾－因此，最高防火性能要求是该行业的标准（UL94V-0、GWEPT960）。高度耐温度变化以及良好的耐热老化性能同样是必要前提。

在电气技术领域，端子用于连接电线和导线。在连接状态下，必须确保接触的连续性和安全性－机械固定装置确保做到这一点。接线盒可以在一条支承轨上任意并行排列，并很容易通过卡住方式进行固定。
这就定义了材料必须具备的机械性能：此用途的塑料必须具有较高的延展性能和良好的韧性－否则，在卡进去的时候就有断裂的危险。用于导线连接要求具有足够的刚性和强度。
凡是有电流通过的地方，就可能溅出火花，产生火灾－因此，最高防火性能要求是该行业的标准（UL94V-0、GWEPT960）。高度耐温度变化以及良好的耐热老化性能同样是必要前提。
塑料具有绝缘性能，因此原则上适用于电气技术。此外，用于接线盒时还要求塑料具有较高的耐泄漏电流稳定性（CTI 600）。
WMF SERIES
端子以大批量方式通过注塑成型工艺进行生产。经济性制造要求生产周期短，而且注塑成型工具和机械的维护费用低。同样，用塑料还必须能生产出壁厚非常薄（0.4毫米）的产品。
此外，材料良好的染色性也扮演着重要的角色：接线盒的不同颜色是不同功能（例如零线、地线等）的区分标志，以保证安全安装。

由于这种高要求，我们使用未增强的聚酰胺作为材料。在巴斯夫广泛的产品线中，PA66/6共聚聚酰胺(UItramidθ?C3U)特别适合用于接线盒。



## 电磁阀
电磁阀工作原理:
电磁阀参数：管道参数、流体参数、压力参数、电气参数、动作方式、特殊要求
	管道参数：1、按照现场管道内径尺寸或流量要求来确定通径(DN)尺寸。
 		  2、接口方式，一般>DN50要选择法兰接口，≤DN50则可根据用户需要自由选择。
	流体参数：
		流体粘度：50cSt以下可任意选择，超过此值则需要高粘度电磁阀
	压力参数：直动式、分步直动式、先导式(压力低可选)
	电气：AC220 DC24
	持续工作时间长短：
	环境要求辅助选择：

	已选型：E1510 E2512 E0510
	类型：针形母端子 管型冷压端子 Y型绝缘压着端子 O型冷压着端子 uk系列端子 tb系列接线端子 pt直通式端子/pt直插自锁式端子
电磁阀厂家/型号：
电磁阀购买渠道：
电磁阀设计文件:





33.5 4V210-08 [以赛亚 电磁阀](https://item.taobao.com/item.htm?spm=a21n57.1.item.2.66ea1b92u2wZmA&priceTId=2150429817207644299582343e3bd4&utparam=%7B%22aplus_abtest%22:%22f069509970c538e5af0666f8014154d5%22%7D&id=550811168935&ns=1&abbucket=9)

[电磁阀选型指南](http://www.hzkwv.com/news/jsnews/DianCiFaXuanXingZhiNan/)








# 电路模型和电路定律

#### 能量 功 功率
$$\mathrm{d}W=u \mathrm{d}q$$
$$p=\frac{\mathrm{d}W}{\mathrm{d}t}=ui$$
$$W(t) = \int \mathrm{d}W = \int_{q(t_0)}^{q(t)}u \mathrm{d}q = \int_{t_0}^{t}u (\xi) i(\xi)\mathrm{d}\xi $$


#### 电阻元件
$$u=Ri$$
$$G=\frac{1}{R}$$
$$i=Gu$$
$$\begin{aligned}p&=ui=Ri^{2}=\frac{u^{2}}{R}\\&=Gu^{2}=\frac{i^{2}}{G}\end{aligned}$$
$$W = \int_{t_{0}}^{t}Ri^{2} ( \xi ) \mathrm{d}\xi $$

#### 电容元件
$$q=Cu$$ \\C是电容元件的参数
$$i=\frac{\mathrm{d}q}{\mathrm{d}t}=\frac{\mathrm{d}( Cu)}{\mathrm{d}t}=C \frac{\mathrm{d}u}{\mathrm{d}t}$$
$$q = \int i \mathrm{d}t$$
$$q = \int_{-\infty}^{t}i \mathrm{d}\xi = \int_{-\infty}^{t_{0}}i \mathrm{d}\xi + \int_{t_{0}}^{t}i \mathrm{d}\xi = q ( t_{0} ) + \int_{t_{0}}^{t}i \mathrm{d}\xi $$
$$q(t) = q(0) + \int_{0}^{t}i \mathrm{d}\xi $$
$$u\left(t\right) = u\left(t_{0}\right) + \frac{1}{C} \int_{t_{0}}^{t}i \mathrm{d}\xi $$
$$p=ui=Cu \frac{\mathrm{d}u}{\mathrm{d}t}$$

$$
\begin{aligned}
\mathbf{W}\_{v} &= \int\_{-\infty}^t u\left(\xi\right) i\left(\xi\right) \mathrm{d}\xi \\
&= \int\_{-\infty}^t C u\left(\xi\right) \frac{\mathrm{d}u\left(\xi\right)}{\mathrm{d}\xi} \mathrm{d}\xi \\
&= C \int\_{u(-\infty)}^{u(t)} u(\xi) \mathrm{d}u(\xi) \\
&= \frac{1}{2} C u^{2}(t) - \frac{1}{2} C u^{2}(-\infty)
\end{aligned}
$$

$$W_{C}(t)=\frac{1}{2}Cu^{2}(t)$$

$$\begin{aligned}W_{c}&= C\int_{u(t_{1})}^{u(t_{2})}u \mathrm{d}u = \frac{1}{2} Cu^{2}(t_{2}) - \frac{1}{2}Cu^{2}(t_{1})\\&=W_{C}(t_{2})-W_{C}(t_{1})\end{aligned}$$


#### 电感元件
![](/img/Snipaste_2024-11-09_20-32-43.png)

$$\Psi_{L}=N\Phi_{L}$$
$$u=\frac{\mathrm{d}\Psi_L}{\mathrm{d}t}$$
$$\Psi=Li$$  \\L 自感系数
![](/img/Snipaste_2024-11-09_20-35-58.png)
$$u=L\frac{\mathrm{d}i}{\mathrm{d}t}$$
$$i = \frac{1}{L} \int u \mathrm{d}t$$
$$i = \frac{1}{L}\int_{-\infty}^{t}u \mathrm{d}\xi = \frac{1}{L}\int_{-\infty}^{t_{0}}u \mathrm{d}\xi + \frac{1}{L}\int_{t_{0}}^{t}u \mathrm{d}\xi = i( t_{0} ) + \frac{1}{L}\int_{t_{0}}^{t}u \mathrm{d}\xi $$

$$\Psi_{L} = \Psi_{L}( t_{0} ) + \int_{t_{0}}^{t}u \mathrm{d}\xi $$

$$p=ui=Li \frac{\mathrm{d}i}{\mathrm{d}t}$$

$$\begin{aligned}
\mathbf{W}_{L}(t)& = \int_{-\infty}^{t}p \mathrm{d}\xi = \int_{-\infty}^{t}Li \frac{\mathrm{d}i}{\mathrm{d}\xi}\mathrm{d}\xi = \int_{0}^{i(t)}Li \mathrm{d}i \\
&=\frac12Li^2(t)=\frac12\frac{\Psi_{L}^2(t)}L
\end{aligned}$$

$$\begin{aligned}W_{l.}&= L\int_{t(t_{1})}^{t(t_{2})}i \mathrm{d}i = \frac{1}{2}Li^{2}(t_{2}) - \frac{1}{2}Li^{2}(t_{1})\\&=W_{L}(t_{2})-W_{L}(t_{1})\end{aligned}$$

![](/img/Snipaste_2024-11-09_20-43-38.png)
$$\frac{1}{C_{\mathrm{eq}}}=\frac{1}{C_{1}}+\frac{1}{C_{2}}+\cdots+\frac{1}{C_{n}}$$
![](/img/Snipaste_2024-11-09_20-44-39.png)
$$C_{\mathrm{eq}}=C_{1}+C_{2}+\cdots+C_{n}$$
![](/img/Snipaste_2024-11-09_20-45-20.png)
$$L_{m_{1}}=L_{1}+L_{2}+\cdots+L_{n}$$
![](/img/Snipaste_2024-11-09_20-45-55.png)
$$\frac{1}{L_{\alpha}}=\frac{1}{L_{1}}+\frac{1}{L_{2}}+\cdots+\frac{1}{L_{n}}$$



#### 电压源和电流源
《电源》p18. 

电压源、电流源常伴随着“独立”二字出现



常见实际电源(如发电机、蓄电池等)的工作机理比较接近电压源，其电路模型是电压源与电阻的串联组合。像光电池一类器件，工作时的伏安特性比较接近电流源，其电路模型是电流源与电阻的并联组合。另外，专门设计的电子电路可以作为电流源而广泛用于集成电路中


$$\begin{aligned}
u_{\mathrm{s}}(t)& = U_{_m}\cos\left(\frac{2\pi}{T}t+\phi \right) \\
&=U_{m}\cos(2\pi ft+\phi) \\
&=U_{_m}\cos( \omega t+\phi )
\end{aligned}$$


![](/img/Snipaste_2024-11-02_20-48-45.png)

#### 基尔霍夫定律
集总电路：是由许多由电源、电阻、电容、电感等集总元件所组成的电路
电路元件的所有电流过程都集中在元件内部空间的各个点上

集总元件：元件大小远小于电路工作频率相对之电磁波波长时，对所有元件的统称。对于信号而言，不论任何时刻，元件特性始终保持固定，与频率无关





电阻电路等效变换
电阻电路一般分析
电路定理
储能元件
一阶电路和二阶电路的时域分析
向量法
正弦稳态电路分析
含有耦合电感的电路
电路的频率响应
三相电路
非正弦周期电流电路和信号频谱
线性动态电路的复频域分析
电路的矩阵方程式
二端口网络
非线性电路
均匀传输线

- [ ] 配电计算
































# 电路设计



## 人体安全

![](/img/Snipaste_2024-11-09_21-03-11.png)
[ref](https://lp-cn1-wechat-production.merklechina.com/post/digikey/technical_article/1106/)


iec 60479 《电流体通过人体时的效应》

感觉阈值--人体能感觉出的最小电流值，一般为0.5mA，次之与电流通过的持续时间长短无关
摆脱阈值--成年男性 10mA，手掌心肌肉电流超过此值，手掌心肌肉反应是不依人的意识摆脱带电导体
心室纤维性颤动阈值--
![](/img/Snipaste_2024-11-09_07-17-11.png)

Ib<30mA，就不会发生心室纤颤而导致死亡，RCD的额定动作电流取值为30mA

![](/img/Snipaste_2024-11-09_07-21-03.png)
干燥：48v以下
潮湿：36v以下面
淋浴：6v以下

手持式、移动式设备，如果绝缘损坏，通过人体的电流大于10mA，人体不饿能脱离与电的接触，所以需要加RCD
对于固定式设备和配电线路，因往往能及时摆脱设备故障，其要求可以降低

直流电通过人体同样会产生各种效应，直流电的阈值为2mA，没有明确拜托阈值，xx
iec标准将引起心室纤颤的直流预期接触电压限值取为120v


## 电击防护
直接防护\
1 绝缘层覆盖\
2 遮拦或外护物 | xx防护等级\
3 阻挡物 | 栏杆、网屏、栅栏\
4 带电部分置于伸臂范围之外 | iec规定2.5m\
5 30mA RCD 附加防护\
	rcd回路没有剩余电流，不跳闸\
	rcd断开时间长，可能造成人体损伤\
	
间接防护


## 低压配电网

浪涌
短路

接地
![](/img/Snipaste_2024-07-12_17-42-27.png)
如图，

系统接地
![](/img/Snipaste_2024-07-12_18-55-27.png)
如图：雷电浪涌会在电路中产生极大的瞬态电流 \
电源端接地，瞬态电流绕着大地回到电源负极，起到了对负载电器的保护作用


中性线接地(保护接地)
[楼宇小区供电系统接地方式分析（TN-S系统）](https://www.bilibili.com/video/BV1Y2421w7dx/?spm_id_from=333.337.search-card.all.click&vd_source=5f0df1465c2a6217cdfee2c39bf1d4db)

中性线N取自于电力变压器低压侧按星形联结的三项绕组公共端。中性线N和相线一同为使用相电压的负载提供电能，同时中性线上也流过三相系统中的不平衡和单项电流。\
保护线PE则取自于接地点，其用途是保护人身安全，一般用于连接带电负荷的金属外壳、构架等，以及平时可能不带电但发生故障时可能带电的设备外露可导电部分。\
IEC标准规定自变压器中性线引出的PEN线(或N线)必须绝缘，并只能在低压配电盘内一点与接地的PE母排连接而实现系统接地，在这点以外任何之处不得再次接地，否则将有部分中性线电流通过非正规路径返回电源。\
IEC规定包含PE线的PEN线上不允许装设开关和熔断器以杜绝PE线被切断。

![](/img/Snipaste_2024-07-12_19-16-55.png)
![](/img/Snipaste_2024-07-12_19-17-13.png)

接地系统
![](/img/Snipaste_2024-07-12_19-19-34.png)
![](/img/Snipaste_2024-07-12_19-32-10.png)
低压配电网考虑三个问题：\
1 电气系统中的中性线及电器设备外露导电部分与接地极的连接方式\
2 采用专用的PE保护线还是采用与中性线合一的PEN保护线\
3 采用只能切断较大故障电流的过流保护电器还是采用能检测和切断较小的剩余电流的保护电器作为低压成套开关的接地故障防护

TN系统
特征：\
1 强制性要求将用电设备外露导电部分和中性点接通并接地\
2 TN接地系统中的单相接地故障被放大为短路故障\
3 在TN接地系统中发生第一次接地故障时就能切断电源

TN系统属于大电流接地系统，因此在TN系统下可利用断路器或熔断器的短路保护作用来执行给单项接地故障保护

TN-C(combine)
特征：能同时承载三相不平衡电流和高次谐波电流。为此，TN-C的PEN线应当在用电设备内与若干接地极相连。\
TN-C系统的PEN线定义中，“保护线”功能优于“中性线”功能，所以PEN线首先接入用电设备的接地接线端子，然后再用连接片接到中性线端子。

TN-S()

<低压成套开关设备的原理及其控制技术.pdf>\

# 短路过程
[cousera-电力系统分析](/img/https://www.icourse163.org/learn/NJTU-1003359009?tid=1473275479#/learn/content?type=detail&id=1260965142&cid=1297838221)



# 触摸屏
IT6070T
控件
按钮

宏指令

 ref
[INOVANVE IT6070T](https://www.jianguoyun.com/p/DRUuw8gQ5rjkDBjzgNAFIAA)


# plc
sfc编程：

步转移条件：外部触发、外部状态变化

- 外部触发：

\     \blank 条件\\[pos] transfer xx-> 状态转移点\\<>状态变化


动力源：
	电机：步进电机、伺服电机、三相异步电机
	气缸：
	液压缸：
传动系统：
	机械传动：齿轮、丝杆
	电传动
	气传动
	液压传动


## simen(西门子)
### 型号：smart 200
### IO分配
### 地址及数据类型
### 指令

### 型号：tia 1200
### IO分配
### 地址及数据类型
### 指令


## 三菱
### 型号
### IO分配
### 地址及数据类型
### 指令


## ormon(欧姆龙)
[ormon plc仿真环境搭建及通信](https://blog.csdn.net/yjg428/article/details/130483821)
(ormon sysmac cp1h)
### 型号
![](/img/Snipaste_2024-07-29_08-12-03.png)
### IO分配

![](/img/Snipaste_2024-07-29_08-10-10.png)
![](/img/Snipaste_2024-07-29_08-10-38.png)


### 地址及数据类型
#### 寻址方式
##### 变址寻址
##### 固定地址
保持区H\
范围：H0.00-->H511.15

数据存储器D\
范围：D0-->D32767

###### IO存储区
![](/img/Snipaste_2024-07-29_07-53-34.png)
![](/img/Snipaste_2024-07-29_07-58-03.png)
###### 数据区
![](/img/Snipaste_2024-07-29_08-01-20.png)
![](/img/Snipaste_2024-07-29_08-01-50.png)
![](/img/Snipaste_2024-07-29_08-02-18.png)
![](/img/Snipaste_2024-07-29_08-02-40.png)
![](/img/Snipaste_2024-07-29_08-03-05.png)
![](/img/Snipaste_2024-07-29_08-03-25.png)
![](/img/Snipaste_2024-07-29_08-03-48.png)
![](/img/Snipaste_2024-07-29_08-04-59.png)

### 指令
![](/img/Snipaste_2024-07-30_08-14-27.png)
#### 高速计数器

## ref
[ormon sysmac cp1h handbook](https://www.jianguoyun.com/p/DTzP450Q5rjkDBjrgNAFIAA)\



## 汇川
### st语言

![](/img/Snipaste_2024-11-11_16-08-28.png)

位软元件
![](/img/Snipaste_2024-11-11_16-09-04.png)

#### 数据类型
a:=10#1000

#### 变量
可以在LiteST程序编辑中直接编写变量，然后按ENTER键或者鼠标点击程序基本块外区域自动弹出变量定义
框声明。变量类型默认是INT型，调用函数、指令时可以自动识别数据类型。

#### 指令
- 流程控制指令
IF
CASE
WHILE
REPEAT
FOR
EXIT
CONTINUE
RETURN

- 定时器指令
TPR \\脉冲定时器 
TONR \\接通延时定时
TACR \\关闭延时定时
TOFR \\时间累加定时

- 中断指令
EI \\开启中断
DI \\关闭中断

- 上升下降沿
R_TRIG \\上升沿检测触发器
F_TRIG \\下降沿检测触发器

- 置位复位
ZSET \\批量置位
ZRST \\批量复位

- 指令速查表 H5U & Easy
![](/img/Snipaste_2024-11-11_15-49-58.png)
![](/img/Snipaste_2024-11-11_15-50-38.png)
![](/img/Snipaste_2024-11-11_15-51-41.png)
![](/img/Snipaste_2024-11-11_15-52-01.png)
![](/img/Snipaste_2024-11-11_15-53-20.png)
![](/img/Snipaste_2024-11-11_15-54-26.png)
![](/img/Snipaste_2024-11-11_15-54-44.png)


# 电气产品


## 线缆
- 标识
[GB∕T 4026-2019 人机界面标志标识的基本和安全规则设备端子、导体终端和导体的标识](https://www.jianguoyun.com/p/DR59jPAQmdvgDBjJ_9kFIAA)\
[GBT 4025-2010 人机界面标志标识的基本和安全规则 指示器和操作器件的编码规则](https://www.jianguoyun.com/p/DfOXUVMQmdvgDBjQ_9kFIAA)

- 线缆颜色
iec 60757
![](/img/Snipaste_2024-11-04_13-22-35.png)

- 导体标识 端子标识

![](/img/Snipaste_2024-11-04_13-27-10.png)
![](/img/Snipaste_2024-11-04_13-27-49.png)


下列颜色允许用于导体的标识：\
黑色、棕色、红色、橙色、黄色、绿色、蓝色、紫色、灰色、白色、粉红色、青绿色

颜色标识应在终端和导体全长使用，并推荐在导体全场采用绝缘颜色或颜色标志。在终端和连接点使用颜色标识的裸导体除外

- 单色使用
中性或中间导体：推荐使用不饱和蓝色\
交流系统：优先使用黑色、棕色、灰色\
直流系统：线导体正极用红色，负极用白色\
功能接地：优先使用粉红色

- 双色组合
保护导体：绿-黄双色组合，(在颜色的标识别的任一15mm长导体上，一种颜色覆盖导体表面的30%~70%)
绿黄组合限制在保护导体，不能跟其他颜色混合

- 文字标识
中性导体:N\
保护导体:PE\
PEN导体:PEN\
PEL\
PEM\
保护联结导体:PB\
线导体：\
"L"开头，后缀:\
--交流电路，从数字"1"开始顺序编号\
--直流电路，在正极端加标识"+"，负极端加"-"

E0508
![](/img/Snipaste_2024-11-04_14-08-08.png)
![](/img/Snipaste_2024-11-04_14-09-01.png)
![](/img/Snipaste_2024-11-04_14-09-38.png)


- 位置编码
1 作为主代码\
2 作为主代码的辅助代码，例如，形状代码作为颜色代码的补充\
位置代码主要用于过程状态和设备状态指示
![](/img/Snipaste_2024-07-15_14-09-54.png)

- 其他编码
![](/img/Snipaste_2024-07-15_14-10-21.png)
![](/img/Snipaste_2024-07-15_14-10-38.png)
![](/img/Snipaste_2024-07-15_14-11-17.png)
- 不发光操作器件
![](/img/Snipaste_2024-07-15_14-46-04.png)
- 发光操作器件
![](/img/Snipaste_2024-07-15_14-50-28.png)

