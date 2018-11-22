---
title: Finance and Assets
date: 2018-11-08 16:01:49
tags:
---

## 常见概念


#### cpi - 消费物价指数
```
cpi is a standard via compute the weight average of some representive  goods for society,to denote the good price
```

#### PPI - 生产价格指数
```
it is used to statistics the goods price when thy was published from relase line in industry enterprise

```
#### IAV - 工业增加值- all enterprises*(生产的商品price-减去成本)

[质押式回购-目前可以理解为当铺模式](https://wiki.mbalib.com/wiki/%E9%93%B6%E8%A1%8C%E9%97%B4%E8%B4%A8%E6%8A%BC%E5%BC%8F%E5%9B%9E%E8%B4%AD%E5%88%A9%E7%8E%87)








# 货币政策
## 定义
货币政策（Monetary Policy）是一个国家或是经济体的货币权威机构（多数国家由央行来执行）利用控制货币供应量，来达到影响其他经济活动所采取的措施
## 目的
控制货币供应量
## 主要手段
主要手段包括：调节基础利率、调节商业银行保证金、公开市场操作
## 分类
货币政策一般分为：激进的－利率被调节为促进经济增长；中性的－保持经济稳定；从紧的－降低通货膨胀却可能提高失业率


### [基准利率](https://baike.baidu.com/item/%E5%9F%BA%E5%87%86%E5%88%A9%E7%8E%87)
基础的理解是一个指标利率，大家都已这个作为参考，基准利率是金融市场上具有普遍参照作用的利率，其他利率水平或金融资产价格均可根据这一基准利率水平来确定。基准利率是利率市场化的重要前提之一，在利率市场化条件下，融资者衡量融资成本，投资者计算投资收益，以及管理层对宏观经济的调控，客观上都要求有一个普遍公认的基准利率水平作参考。所以，从某种意义上讲，基准利率是利率市场化机制形成的核心。
其中，以同业拆借利率为基准利率的国家有英国的伦敦同业拆放利率(Libor)、美国的美国联邦基准利率(FFR)、日本的东京同业拆借利率(Tibor)、欧盟的欧元银行同业拆借利率(Euribor)等；以回购利率为基准利率的国家有德国(1W和2W回购利率)、法国(1W回购利率)、西班牙(10D回购利率)。 [1] 
在中国，以中国人民银行对国家专业银行和其他金融机构规定的存贷款利率为基准利率。具体而言，一般普通民众把银行一年定期存款利率作为市场基准利率指标，银行则是把隔夜拆借利率作为市场基准利率。




### 主体影响因子
#### 债券本身
1.货币市场
2.外汇市场
3.存贷款利率资金供应量
4.社会投融资体系

#### 宏观经济数据

社会投融资规模




## target

国债10年期利率交叉验证可接受范围[5%]

### problem:是否能抽象成分类问题




# 对冲理论
price(物价cpi,ppi)*y(经济add rate)= m货币供给*v货币流通速度
## 价格
cpi
ppi
rpi
## 经济增长
gdp
工业增加值
## 货币供给
MI
社会融资规模当月值
官方储备资产:外汇储备
## 货币流通速度
人民币存款准备金率:大型存款类金融机构(月)
人民币存款准备金率:中小型存款类金融机构(月)




## 存贷款利率是这一套系统的根本




# 训练集合特征
## 输出
十年期回报率
## 输入
date 日期
cpi  消费物价指数
ppi  生产价格指数
gdp  国民生产总值
r007 银行间回购利率
spot_rate_exchange 人民币离岸汇率
iav 工业增加值

## 模型
## 假设空间
##  mode select
1.linear regression
2.svm
## 参数空间


## 策略

### 损失函数和风险函数
经验风险和结构风险最小
从目前的策略采用国债10年期利率可接受范围[5%]作为输出结果，在此基础上进行预测


## loss function
### 过拟合问题风险防范
















### 训练集合与测试集合划分






## Predict

### make a dataset from wind
#### data pretreatment



### predict mode
#### scheme0
using  machine learning tech stack
#### scheme1
```python
#this output is 10 years  Yield to maturity
def predict(ppi=None,cpi=None,r007 = None):
	ytm = compute(ppi,cpi,r007)
    return ytm
```





# problems
## data pre-dealwithproblem
   缺少的值如何处理
   该选择什么样的模型













