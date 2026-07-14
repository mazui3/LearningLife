捏人模块
 step1: 名字
 step2: 发型
 step3: 服装
 step4: 问题1,选择了什么专业读大学
 step5: 问题2,想过什么样的人生

event.初始演出

---
专业data:
1. 专业名称
2. 初始每年年薪
3. 上班event时的背景
---
想过什么样的人生data:

---
时间模块:
 - run周loop运行schedule
 - 周结算(call其他系统模块.结算) - 带结局成功判定

---
schedule模块:
1. schedule是否有开启 - 出现在可选calendar中
2. schedule.触发 method
2.1 schedule是否通过前置条件
2.2 schedule对数值的加和减(结算)
2.3 -> 判定schedule是否触发特殊event
3. schedule.data id

schedule的data:
<!-- - (运行时会消耗的)系统.数值 -->
- 开启条件(生意 - 生意有关的搜索数)
- 时间限制
- (当run时可能触发的)特殊event.data id & 概率

---
event的data:
- (运行时会消耗的)系统.数值
- 开启条件
- 时间限制
- 触发条件
- 触发概率
- 成功判定条件
- 显示&图片&立绘的信息

---
系统(写个base然后inherite吧)
>key+子系统

玩家dictionary -> (key, 系统class)

系统class:
1. 系统data
2. 系统.数值
3. 系统.周结算

系统data:
 - 连带schedule & 开启条件(搜索hit数)
 - 给玩家的说明(新数值的说明)
 - (唯一)mission.data
 - (如果有无schedule判定时也能触发)特殊event.data

mission data
 - 成功判定条件
 - 给玩家的说明
---
玩家行动

---
地图模块

建筑物data:
银行(贷款，基金，定期，保险，信用卡)
图书馆(借书，活动，volunteer，做家教)

---
兴趣

兴趣字典(playfab)

 - key word的hit次数
 - key word到系统种类的map(json)
 - key word的map(json)

---
联动APP的二维码生成
