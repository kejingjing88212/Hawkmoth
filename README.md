Hawkmoth
========


####首要的问题是保证飞行的稳定和可靠。否则一旦从天上掉下来，就损失惨重了。

问题：
目前看来，通讯是一个问题。通讯有两个问题，一个是视频讯号，一个是控制信号。

想法：

智能系统控制一切。

系统被分为很多的模块，基础的模块就是飞行的控制。这很重要，必须保证平稳的飞行在设定高度上。必须有飞行姿态控制系统。这个目前已经有解决方案了。作为一个4轴飞行器，其实只能在4个方向上飞行，前后左右，加上上下，总共是六轴，所以需一个六轴传感器。这个已经有了。

飞行器的状态有9种：

起飞，悬停，向左，向右，向前，向后，降落，停机，关机。

####起飞

######检测阶段：
* 起飞前需要检测电力水平。如果电力不足拒绝起飞。
* 起飞前检测各模块的状态，特别是4个马达是否正常。
* 获取起飞高度，大体上知道我们在那个高度上进行起飞的。
* 检测测距仪是否正常。记录起飞距离（测距仪转至垂直状态，测量距地面的距离，记录这个距离作为降落（停车）的标志）。所以，很 明显，我们需要一个云台，而且要轻的。

######起飞阶段：
检测正常，进入起飞阶段。马达开始加速。注意保持马达的转速一致。如果已经起飞，高度传感器应该能够探测到高度的变化。注意我们的云台还是向下的。

----------------------------------------------
####降落


- - - 
悬停
- - -
前进
- - -
后退
- - -
向左
- - -
向右

电力检测。系统需要检测电力，如果电力不足就自动降落下来。

还有就是需要障碍检测，可能需要一个超声波检测仪，因为飞行速度大约等于步行的速度，所以不需要很先进的障碍检测。检测仪被安装在一个舵机上，可以做水平360度，垂直180度的转向，不需要在4个方向上都安装传感器，这样太费电。当需要向某个方向飞行的时候，舵机先转向，传感器探测前方是否有障碍，如果没有，前进（低速），如果有悬停。