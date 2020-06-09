# 编程实现崩坏3自动凹分

## 原理

C#调用dm.dll的识图识色，判断战场开始和boss血量，结合时间+boss血量判断出否出分。

调用dm.dll键盘接口实现模拟手打流程，boss动作越简单越容易出分，比如真红月魂，月魂就像木桩一样，基本一次出分。

## 添加流程

1. 继承`AutoPlay`类，复写Action方法，Action方法主要是模拟键盘手打流程，

2. 复写`OnCheckTime`方法，此方法用于判断出分，达到不出分自动重开效果

3. 将刚新建的类实例化添加到`AutoPlayScriptManager`的`scripts`列表


## 已实现战场流程

* 墨炎真VS冰箱31680(up38016)

* 鬼圣迅vs贝贝龙31573(up37888)

* 律山紫vs皮皮马31626(up37952)

* 山粉蓝vs月轮37760(非up31466)


## 原按键精灵项目

[BH3QScript](https://github.com/linyuchen/Bh3QScript)，此项目已停止维护，按键精灵开发体验实在太糟糕，无法忍受。