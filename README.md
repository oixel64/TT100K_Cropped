# TT100K_Cropped

## 背景

这是我《计算机视觉与模式识别》课程 “交通标志的定位与识别” 综合实验训练分类器所用数据集，好像网络上纯交通标志分类的数据集只有德国的[GTSRB](https://benchmark.ini.rub.de/gtsrb_news.html)等，没有中国的交通标志分类的数据集，我就自己从[TT100K](https://cg.cs.tsinghua.edu.cn/traffic-sign/)中提取做了一个。

## 数据集介绍

TT100K_Cropped 是一个中国交通标志分类数据集，专门从 TT100K 数据集中裁剪出目标图像组成。TT100K 数据集由清华大学和腾讯公司合作创建，包含了从 100,000 张腾讯街景全景图中提取的 30,000 个交通标志实例。TT100K_Cropped 通过裁剪这些标志以专注于标志本身，为交通标志检测和分类任务提供了一个更专注的数据集。

```
.
├── DataSet             从 TT100K 数据集裁剪目标图像得到的数据集
│   ├── test
│   └── train
├── LICENSE
├── README.md
├── code
│   ├── anno_func.py
│   └── example.ipynb   从 TT100K 数据集裁剪目标图像
└── pic
    ├── test_class.png
    ├── train_class.png
    └── u16.jpg
```

## 数据集特点

- **数据来源**: 从 TT100K 数据集中裁剪得到的目标图像。
- **多样性**: 图像涵盖了多种光照和天气条件，具有很高的多样性。
- **类别不平衡**: 数据集各类别样本数不平衡，请格外注意。
- **添加负类**: 添加从 TT100K 数据集的`other`文件夹中随机提取的非交通标志区域

## 数据集类别

![](./pic/u16.jpg)

| Code  | English Name                                                | Chinese Name             |
| ----- | ----------------------------------------------------------- | ------------------------ |
| i1    | Walk                                                        | 步行                     |
| i2    | Non-motorized vehicles                                      | 非机动车行驶             |
| i3    | Round the island                                            | 环岛行驶                 |
| i4    | Motor vehicle                                               | 机动车行驶               |
| i5    | Keep on the right side of the road                          | 靠右侧道路行驶           |
| i6    | Keep on the left side of the road                           | 靠左侧道路行驶           |
| i7    | Drive straight and turn right at  the grade separation      | 立体交叉直行和右转弯行驶 |
| i8    | Drive straight and turn left                                | 立体交叉直行和左转弯行驶 |
| i9    | Honk                                                        | 鸣喇叭                   |
| i10   | Turn right                                                  | 向右转弯                 |
| i11   | Turn left and right                                         | 向左向右转弯             |
| i12   | Turn left                                                   | 向左转弯                 |
| i13   | One way, straight                                           | 直行                     |
| i14   | Go straight and turn right                                  | 直行和向右转弯           |
| i15   | Go straight and turn left                                   | 直行和向左转弯           |
| i150  | Minimum Speed Limit (50)                                    | 最低限速（50）           |
| ip    | Pedestrian Crossing                                         | 人行横道                 |
| p1    | No Overtaking                                               | 超车                     |
| p2    | Ban animal-drawn vehicles entering                          | 禁止畜力车进入           |
| p3    | Ban large passenger vehicles from  entering                 | 禁止大型客车驶入         |
| p4    | Prohibition of electric tricycles                           | 禁止电动三轮车驶入       |
| p5    | No U-turn                                                   | 禁止掉头                 |
| p6    | Prohibition of non-motorized  vehicles                      | 禁止非机动车进入         |
| p7    | No left turn for trucks                                     | 禁止载货汽车左转         |
| p8    | It is forbidden to tow or trailer  vehicles                 | 禁止汽车拖、挂车驶入     |
| p9    | Prohibit pedestrians entering                               | 禁止行人进入             |
| p10   | Prohibit motorized vehicles                                 | 禁止机动车驶入           |
| p11   | Prohibit honking                                            | 禁止鸣喇叭               |
| p12   | Two-wheeled motorcycles are  prohibited                     | 禁止二轮摩托车驶入       |
| p13   | Prohibit certain two types of  vehicles from entering       | 禁止某两种车驶入         |
| p14   | Prohibition straight                                        | 禁止直行                 |
| p15   | No rickshaws are allowed                                    | 禁止人力车进入           |
| p16   | Prohibition of human-powered cargo  tricycles from entering | 禁止人力货运三轮车进入   |
| p17   | Prohibition of human-powered cargo  tricycles from entering | 禁止人力货运三轮车进入   |
| p18   | Prohibition of tricycles and motor  vehicles                | 禁止三轮车机动车通行     |
| p19p  | Prohibited right turn                                       | 禁止向右转弯             |
| p20   | No left or right turn                                       | 禁止向左向右转弯         |
| p21   | Prohibited right turn and straight                          | 禁止直行和向右转弯       |
| p22   | Prohibition of tricycles and motor  vehicles                | 禁止三轮车机动车通行     |
| p23   | Prohibited left turn                                        | 禁止向左转弯             |
| p24   | Prohibition of right turning of  passenger cars             | 禁止小客车右转           |
| p25   | Prohibition of entry of small  passenger cars               | 禁止小客车驶入           |
| p26   | Prohibit laden car into                                     | 禁止载货汽车驶入         |
| p27   | Prohibit entry of vehicles  transporting dangerous goods    | 禁止运输危险物品车辆驶入 |
| p28   | Prohibited left turn and straight                           | 禁止直行和向左转弯       |
| p29   | Prohibit tractors from entering                             | 禁止拖拉机驶入           |
| pa10  | Limit axle load (10t)                                       | 限制轴重(10t)            |
| pb    | No thoroughfare                                             | 禁止通行                 |
| pc    | Parking inspection                                          | 停车检查                 |
| pd    | Customs                                                     | 海关                     |
| pe    | Give Way to Oncoming Vehicles                               | 会车让行                 |
| pg    | Slow down and give way                                      | 减速让行                 |
| ph3.5 | Limit height (3.5m)                                         | 限制高度(3.5m)           |
| pl40  | Limit speed (40)                                            | 限制速度(40)             |
| pm10  | Limit weight (10t)                                          | 限制质量(10t)            |
| pn    | No parking                                                  | 禁止停车                 |
| pne   | No Entry                                                    | 禁止驶入                 |
| pnl   | No long-term parking                                        | 禁止长时停车             |
| pr40  | Speed restrictions lifted                                   | 解除限制速度             |
| ps    | Park to give way                                            | 停车让行                 |
| pw3   | Limit width (3.5m)                                          | 限制宽度(3.5m)           |
| w1    | Dangerous road near the mountain                            | 傍山险路                 |
| w2    | Dangerous road near the mountain                            | 傍山险路                 |
| w3    | Village                                                     | 村庄                     |
| w4    | Embankment road                                             | 堤坝路                   |
| w5    | Embankment road                                             | 堤坝路                   |
| w6    | T-shaped plane crossing                                     | 丁字平面交叉             |
| w7    | Ferry                                                       | 渡口                     |
| w8    | Narrow on both sides                                        | 两侧变窄                 |
| w9    | Watch out for falling rocks                                 | 注意落石                 |
| w10   | Reverse detour                                              | 反向弯路                 |
| w11   | Reverse detour                                              | 反向弯路                 |
| w12   | Manshuiqiao                                                 | 漫水桥                   |
| w13   | Crossroads                                                  | 十字交叉路口             |
| w14   | Crossroads                                                  | 十字交叉路口             |
| w15   | Y-shaped intersection                                       | Y形交叉路口              |
| w16   | Y-shaped intersection                                       | Y形交叉路口              |
| w17   | Y-shaped intersection                                       | Y形交叉路口              |
| w18   | Road Narrows on Left                                        | 左侧变窄                 |
| w19   | Y-shaped intersection                                       | Y形交叉路口              |
| w20   | T intersection                                              | T形交叉路口              |
| w21   | T intersection                                              | T形交叉路口              |
| w22   | T intersection                                              | T形交叉路口              |
| w23   | Roundabout                                                  | 环形交叉路口             |
| w24   | Continuous detour                                           | 连续弯路                 |
| w25   | Slopes                                                      | 连续下坡                 |
| w26   | Uneven road                                                 | 路面不平                 |
| w27   | Watch out for rain (snow) days                              | 注意雨（雪）天           |
| w28   | Low-lying road                                              | 路面低洼                 |
| w29   | High road surface                                           | 路面高突                 |
| w30   | Stroll                                                      | 慢行                     |
| w31   | Up a steep slope                                            | 上陡坡                   |
| w32   | Construction                                                | 施工                     |
| w33   | Cross plane                                                 | 十字平面交叉             |
| w34   | Accident-prone road                                         | 事故易发路段             |
| w35   | Two-way traffic                                             | 双向交通                 |
| w36   | Watch out for wild animals                                  | 注意野生动物             |
| w37   | Tunnel                                                      | 隧道                     |
| w38   | Tunnel driving lights                                       | 隧道开车灯               |
| w39   | Hump bridge                                                 | 驼峰桥                   |
| w40   | Unguarded railway crossing                                  | 无人看守铁路道口         |
| w41   | Down steep slope                                            | 下陡坡                   |
| w42   | Sharp detour                                                | 急弯路                   |
| w43   | Sharp detour                                                | 急弯路                   |
| w44   | Slippery                                                    | 易滑                     |
| w45   | Watch out for semaphores                                    | 注意信号灯               |
| w46   | Someone guards the railway  crossing                        | 有人看守铁路道口         |
| w47   | Narrowing on the right                                      | 右侧变窄                 |
| w48   | Detour right                                                | 右侧绕行                 |
| w49   | Narrow on both sides                                        | 两侧变窄                 |
| w50   | Pay attention to keeping the  distance between cars         | 注意保持车距             |
| w51   | Pay attention to adverse weather  conditions                | 注意不利气象条件         |
| w52   | Pay attention to the disabled                               | 注意残疾人               |
| w53   | Watch out for tidal lanes                                   | 注意潮汐车道             |
| w54   | Pay attention to foggy days                                 | 注意雾天                 |
| w55   | Pay attention to children                                   | 注意儿童                 |
| w56   | Pay attention to non-motorized  vehicles                    | 注意非机动车             |
| w57   | Pay attention to pedestrians                                | 注意行人                 |
| w58   | Pay attention to confluence                                 | 注意合流                 |
| w59   | Pay attention to confluence                                 | 注意合流                 |
| w60   | Crosswinds                                                  | 注意横风                 |
| w61   | Watch out for icing on the road                             | 注意路面结冰             |
| w62   | Watch out for falling rocks                                 | 注意落石                 |
| w63   | Drive With Caution                                          | 注意危险                 |
| w64   | Pay attention to livestock                                  | 注意牲畜                 |
| w65   | Detour on the left                                          | 左侧绕行                 |
| w66   | Left and right detour                                       | 左右绕行                 |
| w67   | Pay attention to the queues of  vehicles ahead              | 注意前方车辆排队         |
| io    | Other signs                                                 | 其他指示标志             |
| wo    | Other warning signs                                         | 其他警告标志             |
| po    | Other prohibition signs                                     | 其他禁止标志             |

## 数据集样本分布

### 训练集

![](./pic/train_class.png)

### 测试集

![](./pic/test_class.png)

## 许可证

本项目基于 MIT 许可证开源，详细信息请参阅 LICENSE 文件。

## 参考

- [TT100K 数据集](https://cg.cs.tsinghua.edu.cn/traffic-sign/)

- [中国交通标志牌数据集TT100K中的类别ID及其图标罗列以及含义详细介绍](https://blog.csdn.net/qq_37346140/article/details/127581223)