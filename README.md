# Converter-Transient-stability-control

=======================================================
根据重庆大学姚骏老师的两篇论文的控制策略搭建逆变器并网后电网发生对称短路故障时，逆变器的稳定性控制策略。
姚老师的两篇论文如下：
[1]	Y. Liu, et al, "Transient Stability Enhancement Control Strategy Based on Improved PLL for Grid Connected VSC during Severe Grid Fault," in IEEE Transactions on Energy Conversion, vol. 36, no. 1, pp. 218-229, March 2021.
[2]	裴金鑫,姚骏,黄森,等.电网短路故障下新能源并网变换器的暂态同步机制及其自适应稳定控制策略[J/OL].中国电机工程学报:1-13[2021-12-29]
PEI Jinxin, YAO Jun, HUANG Sen, et al. Transient Synchronization Mechanism and Adaptive Stability Control Strategy for Renewable Energy Grid-connected Converter Under Grid Faults[J/OL]．Proceedings of the CSEE, 1-13
本模型没有对论文进行严格复刻，只是在自己的仿真系统中复刻了上述两种控制策略，经过运行对比，模型中的策略运行效果与论文中的运行效果趋势完全相同，稳定性情况也基本一致。
MATLAB版本为2021b，低于这个版本无法正确运行。
========================================================
模型说明
1.控制策略模块在PLL锁相环中，其中自适应阻尼控制模块对应第一篇论文，自同步稳定控制模块对应第二篇论文，运行时需屏蔽其中一个模块
2.自适应阻尼控制需调整故障电压和故障相位与电网系统中故障模拟模块的参数一致
3.有关控制策略的详细原理请自行阅读上述两篇论文。

According to the control strategy of two papers written by Mr. Yao Jun of Chongqing University, the stability control strategy of the inverter is built when the symmetrical short circuit fault occurs in the grid after the inverter is connected to the grid.
Mr. Yao's two papers are as follows:
[1]	Y.  Liu, et al, "Transient Stability Enhancement Control Strategy Based on Improved PLL for Grid Connected VSC during Severe Grid Fault," in IEEE Transactions on Energy Conversion, vol. 36, no. 1, pp. 218-229, March 2021.
[2] Pei Jinxin, Yao Jun, Huang Sen, et al. Transient synchronization mechanism and adaptive stability control strategy of new energy grid connected converter under grid short-circuit fault [J/OL]. Chinese Journal of Electrical Engineering: 1-13 [2021-1-29]
PEI Jinxin, YAO Jun, HUANG Sen, et al. Transient Synchronization Mechanism and Adaptive Stability Control Strategy for Renewable Energy Grid-connected Converter Under Grid Faults[J/OL]．Proceedings of the CSEE, 1-13
This model does not strictly reproduce the paper, but just replicates the above two control strategies in its own simulation system. After running comparison, the running effect of the strategy in the model is identical to that in the paper, and the stability is basically the same.
The version of MATLAB is 2021b, which cannot run correctly before this version.
========================================================
Model description
1. The control strategy module is in the PLL, where the adaptive damping control module corresponds to the first paper and the self synchronous stability control module corresponds to the second paper. One of the modules needs to be shielded during operation
2. The adaptive damping control needs to adjust the fault voltage and fault phase to be consistent with the parameters of the fault simulation module in the power grid system
3. Please read the above two papers for the detailed principle of control strategy.


