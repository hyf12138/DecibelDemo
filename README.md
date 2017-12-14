# DecibelDemo
前段时间完成项目的一个小功能：检测声音的分贝，通过在网上查找资料整理了一些方法，就把它写成Demo吧

# 示例
![gif](https://github.com/Benight/DecibelDemo/dbGIF.gif)

#总结
  1.苹果给出的方法有两个，一个是：averagePowerForChannel（取麦克风输出电压的平均值），一个是peakPowerForChannel（取麦克风输出电压的瞬时值的），两个方法取值都是（-160，0）
  因此怎么把这个麦克风输出电压转换成我们平时所常用的分贝值，这个过程就比较曲折了，在网上查找了一些资料，找了几种显示比较接近的方法，写在了Demo里
  2.iPhone的输入源是有好几个的（充电的地方有个，前摄像头附件有个，后摄像头附件有个，貌似新出的还有一个，无所谓了），在选输入源的时候还是随机的····这会导致对着底下吹气的时候，有时候吹不到最高（恩，我测的时候就是吹气的，大声在办公室喊，会有异样的眼光的···）
  最后看文档的时候，通过AVAudioSessionPortDescription这个类，最终发现了新大陆，解决了问题

#感谢
在网上找了一些资料，由于项目完成的时间比较久了，再去找以前查找的资料的链接就找不到了，在此感谢所有的分享者
