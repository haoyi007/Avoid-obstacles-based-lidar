# Avoid-obstacles-based-on-lidar
You can use this method on your car or UAV.

2018/09/17  haoyi007

1、自主航线的程序框架已经写完，目前在调试，改bug

2、激光雷达产品已经熟悉的差不多了，目前在写接收数据的相关配置。

2018/09/22  haoyi007

1、已经可以读取激光雷达数据，目前做后期处理工作。

2018/09/28  haoyi007

1、激光雷达数据处理板已经可以与MP地面站通信，已经成功上传姿态信息，后面进行程序移植，并测试接收GPS数据。

2018/10/19  haoyi007

1、终于接收到GPS位置数据了，之前一直想接收融合后的位置数据，毕竟融合后的位置更精准一些，但是在上电后gps定位精度不够，飞控可能就不会发送融合后的消息，而且一直在窗口测试，信号估计也不好。今天测试了下接收gps原始数据，总算有位置信息了，不是自己写的，就像个黑匣子，后面应该就方便很多了~还是蛮兴奋的。


2018/11/22  haoyi007

1、自上次MP可以设置航点后，对于写好的航点接收功能一直没有测试，今天测试了下，可以成功运行，后面就赶紧联调一下。慢慢将整套东西装在小车上进行车载运行测试。将丢下的东西再重新捡起来。

2018/12/09  haoyi007

1、基于小车的避障算法移植完成，这周测试下，然后开始装车调试。

2018/12/14  haoyi007

1、激光雷达装车完毕，数据发送显示完毕，进行避障算法调试及小车控制驱动调试。

2018/12/29  haoyi007

1、小车控制驱动调试完成，底层通道分配，手动控制小车已经可以实现。

2019/1/10  haoyi007

1、重新换了个杉川激光雷达，价格便宜，精度更高一些。（之前的激光雷达可能是自己程序执行时间太长，对激光雷达数据没有有效处理，从而产生了影响，可见最好还是有个操作系统，这样写代码方便一些，便于模块化管理和运用）

2、现在的激光雷达换成~hd.s也可以正常用了，之前没有正常用，可能是需要多一步硬件复位的操作

3、后面尽快跑自主航线，将F1板的避障算法优化从而满足激光雷达对处理速度的要求，F1板上的避障算法太耗时了（这就是没有操作系统的弊端，要是有线程的优先级就好了）

