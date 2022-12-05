# Converter-Transient-stability-control
当电网发生对称短路故障时，逆变器的稳定性控制策略的simulink模型

模型中采用两种稳定性控制策略，参考自重庆大学姚骏老师的两篇论文：

[1]	Y. Liu, et al, "Transient Stability Enhancement Control Strategy Based on Improved PLL for Grid Connected VSC during Severe Grid Fault," in IEEE Transactions on Energy Conversion, vol. 36, no. 1, pp. 218-229, March 2021.

[2]	裴金鑫,姚骏,黄森,等.电网短路故障下新能源并网变换器的暂态同步机制及其自适应稳定控制策略[J/OL].中国电机工程学报:1-13[2021-12-29].
PEI Jinxin, YAO Jun, HUANG Sen, et al. Transient Synchronization Mechanism and Adaptive Stability Control Strategy for Renewable Energy Grid-connected Converter Under Grid Faults[J/OL]．Proceedings of the CSEE, 1-13[2022-06-11].

本模型不是对上述论文的严格复刻，逆变器并网的单机无穷大系统是我自己搭建的，控制策略是根据老师的论文进行搭建，所以控制参数与文章不同，但是经过运行对比，稳定性效果及频率的暂态过度效果与论文保持一致，各位可自行在本模型中对比加入和不加入稳定性控制的暂态波形。

模型说明：
1.MATLAB版本是2021b，低于此版本不能运行；
2.模型中的两种控制模块在PLL模块中，其中自适应阻尼控制对应文章[1]，自同步控制对应[2]，运行时需先屏蔽其中一个模块；
3.自适应阻尼控制需设置其电压跌落幅值和相角与电网短路点故障模块的电压和相角一致；
4.关于两种策略的具体控制原理自行阅读姚老师的两篇论文，相关控制参数可自行调整观察波形变化。
