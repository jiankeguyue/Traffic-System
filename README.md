# 交通模拟仿真系统 readme

## 0x01 大体介绍

系统采用vue3+springboot架构

前后端目前仍采用的是分离开发



## 0x02 前端

前端采用的是vue3架构，但由于yueji0j1anke的学艺不精，导致现在系统的前端呈现还是乱糟糟的

目前仍采用的是分离开发，切到vue文件夹

```
npm run server
```

端口号默认为9000



api开发平台配置采用了数据集+可视化图层

```
https://console.amap.com/
```

![image-20240505183559820](https://gitee.com/yuejinjianke/tuchuang/raw/master/image/image-20240505183559820.png)

目前几个基本数据集已导入数据库

这是最基本的表结构

```
CREATE TABLE  Places (
    geometry VARCHAR(255),
    address VARCHAR(255),
    adname VARCHAR(255),
    x VARCHAR(255),
    name VARCHAR(255),
    y VARCHAR(255),
    type VARCHAR(255)
);
```

![image-20240505214927016](https://gitee.com/yuejinjianke/tuchuang/raw/master/image/image-20240505214927016.png)





## 0x03 后端

后端采用springboot基本框架，目前已实现车辆信息获取接口、基本类型获取接口，但尚未与前端进行连调





## 0x04 数据库

已基本插入需求数据





## 0x04 现阶段需求

```
1.需求如何生成
2.接单代价计算与货物运输分配
3.车辆位置更新
4.多货运运输需求和多车辆的仿真运行环境。
5.货车奖励、需求更新、运输更新

（1）货物需求可以根据工厂位置和类型持续生成，需求失效后自动消失
（2）各台车辆可自行计算代价并决定是否接单，并行驶到货物需求地（工厂）
（3）n个周期后，运输完成，已完成的货物需求要记录（便于后期统计相关指标成效）。车辆位置要更新。
（4）UI界面上完成更新

CrateGoods：
1、选择一批货主（ID）
2、选择一批货物类型
3、在合理的范围内生成方量和重量
4、设置货物需求消失失效时间。
5、从POI点从选择两点任意的起始点

GoodContrller中实现CrateGoods方法（这个方法可以后续在前端持续调用，如每分钟1次）
```

