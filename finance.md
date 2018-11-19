---
title: Finance and Assets
date: 2018-11-08 16:01:49
tags:
---
# cpi - 消费物价指数
```
cpi is a tsandard via compute the weight average of some representive  goods for society,to denote the good price
```

# PPI - 生产价格指数
```
it is used to statistics the goods price when thy was published from relase line in industry enterprise

```
# IAV - 工业增加值- all enterprises*(生产的商品price-减去成本)

[质押式回购-目前可以理解为当铺模式](https://wiki.mbalib.com/wiki/%E9%93%B6%E8%A1%8C%E9%97%B4%E8%B4%A8%E6%8A%BC%E5%BC%8F%E5%9B%9E%E8%B4%AD%E5%88%A9%E7%8E%87)


# target

国债10年期利率交叉验证可接受范围[5%]

how to implement a python dataframe wevan s
price(物价cpi,ppi)*y(经济add rate)= m货币供给*v货币流通速度

## data pre-dealwithproblem


### 主体影响因子
#### 债券本身
1.货币市场
2.外汇市场
3.存贷款利率资金供应量
4.社会投融资体系

#### 宏观经济数据

社会投融资规模


### 训练集合特征



### 训练集合与测试集合划分






## Predict

### make a dataset from wind
#### data pretreatment


###  mode select
1.linear regression
2.svm
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

















