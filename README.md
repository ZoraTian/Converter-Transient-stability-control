# Converter-Transient-stability-control
当电网发生对称短路故障时，逆变器的稳定性控制策略的simulink模型
模型中采用两种稳定性控制策略，参考自重庆大学姚骏老师的两篇论文：
[1]	Y. Liu, et al, "Transient Stability Enhancement Control Strategy Based on Improved PLL for Grid Connected VSC during Severe Grid Fault," in IEEE Transactions on Energy Conversion, vol. 36, no. 1, pp. 218-229, March 2021.
[2]	裴金鑫,姚骏,黄森,等.电网短路故障下新能源并网变换器的暂态同步机制及其自适应稳定控制策略[J/OL].中国电机工程学报:1-13[2021-12-29].
PEI Jinxin, YAO Jun, HUANG Sen, et al. Transient Synchronization Mechanism and Adaptive Stability Control Strategy for Renewable Energy Grid-connected Converter Under Grid Faults[J/OL]．Proceedings of the CSEE, 1-13[2022-06-11].
本模型不是对上述论文的严格复刻，逆变器并网的单机无穷大系统是我自己搭建的，控制策略是根据老师的论文进行搭建，所以控制参数与文章不同，但是经过运行对比，稳定性效果及频率的暂态过度效果与论文保持一致，各位可自行在本模型中对比加入和不加入稳定性控制的暂态波形。
========================================
模型说明：
1.MATLAB版本是2021b，低于此版本不能运行；
2.模型中的两种控制模块在PLL模块中，其中自适应阻尼控制对应文章[1]，自同步控制对应[2]，运行时需先屏蔽其中一个模块；
3.自适应阻尼控制需设置其电压跌落幅值和相角与电网短路点故障模块的电压和相角一致；
4.关于两种策略的具体控制原理自行阅读姚老师的两篇论文，相关控制参数可自行调整观察波形变化。

Simulink model of inverter stability control strategy when symmetrical short circuit fault occurs in power grid
Two stability control strategies are adopted in the model, with reference to two papers by Professor Yao Jun of Chongqing University:
[1]	Y.  Liu, et al, "Transient Stability Enhancement Control Strategy Based on Improved PLL for Grid Connected VSC during Severe Grid Fault," in IEEE Transactions on Energy Conversion, vol. 36, no. 1, pp. 218-229, March 2021.
[2] Pei Jinxin, Yao Jun, Huang Sen, etc Transient synchronization mechanism and adaptive stability control strategy of new energy grid connected converter under grid short-circuit fault [J/OL]. Chinese Journal of Electrical Engineering: 1-13 [2021-12-29]
PEI Jinxin, YAO Jun, HUANG Sen, et al. Transient Synchronization Mechanism and Adaptive Stability Control Strategy for Renewable Energy Grid-connected Converter Under Grid Faults[J/OL]．Proceedings of the CSEE, 1-13[2022-06-11].
This model is not a strict replica of the above paper. The single machine infinite bus system with inverter connected to the grid is built by me, and the control strategy is built according to the teacher's paper. Therefore, the control parameters are different from those in the paper. However, through operation comparison, the stability effect and the transient transition effect of frequency are consistent with those in the paper. You can compare the transient waveforms with and without stability control in this model.
========================================
Model description:
1. The MATLAB version is 2021b, and it cannot be run below this version;
2. The two control modules in the model are in the PLL module, of which the adaptive damping control corresponds to the article [1] and the self synchronization control corresponds to [2]. During operation, one of the modules should be shielded first;
3. The adaptive damping control needs to set its voltage drop amplitude and phase angle to be consistent with the voltage and phase angle of the power grid short-circuit point fault module;
4. Read two papers by Mr. Yao about the specific control principles of the two strategies, and the relevant control parameters can be adjusted to observe the waveform changes.
