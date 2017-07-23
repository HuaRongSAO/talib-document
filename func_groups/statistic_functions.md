# Statistic Functions 统计学指标
### BETA - Beta
> 函数名：BETA  
名称：β系数也称为贝塔系数   
简介：一种风险指数，用来衡量个别股票或
股票基金相对于整个股市的价格波动情况
贝塔系数衡量股票收益相对于业绩评价基准收益的总体波动性，是一个相对指标。 β 越高，意味着股票相对于业绩评价基准的波动性越大。 β 大于 1 ，
则股票的波动性大于业绩评价基准的波动性。反之亦然。
用途：   
1）计算资本成本，做出投资决策（只有回报率高于资本成本的项目才应投资）；   
2）计算资本成本，制定业绩考核及激励标准；   
3）计算资本成本，进行资产估值（Beta是现金流贴现模型的基础）；   
4）确定单个资产或组合的系统风险，用于资产组合的投资管理，特别是股指期货或其他金融衍生品的避险（或投机）     

```python
real = BETA(high, low, timeperiod=5)
```

Learn more about the Beta at [tadoc.org](http://www.tadoc.org/indicator/BETA.htm).  
### CORREL - Pearson's Correlation Coefficient (r)
> 函数名：CORREL  
名称：皮尔逊相关系数   
简介：用于度量两个变量X和Y之间的相关（线性相关），其值介于-1与1之间  
皮尔逊相关系数是一种度量两个变量间相关程度的方法。它是一个介于 1 和 -1 之间的值，
其中，1 表示变量完全正相关， 0 表示无关，-1 表示完全负相关。
```python
real = CORREL(high, low, timeperiod=30)
```

Learn more about the Pearson's Correlation Coefficient (r) at [tadoc.org](http://www.tadoc.org/indicator/CORREL.htm).  
### LINEARREG - Linear Regression
>直线回归方程：当两个变量x与y之间达到显著地线性相关关系时,应用最小二乘法原理确定一条最优直线的直线方程y=a+bx,这条回归直线与个相关点的距离比任何其他直线与相关点的距离都小,是最佳的理想直线.
回归截距a：表示直线在y轴上的截距,代表直线的起点.  
回归系数b：表示直线的斜率,他的实际意义是说明x每变化一个单位时,影响y平均变动的数量.
即x每增加1单位,y变化b个单位.  


> 函数名：LINEARREG  
名称：线性回归   
简介：来确定两种或两种以上变量间相互依赖的定量关系的一种统计分析方法  
其表达形式为y = w'x+e，e为误差服从均值为0的正态分布。

```python
real = LINEARREG(close, timeperiod=14)
```

Learn more about the Linear Regression at [tadoc.org](http://www.tadoc.org/indicator/LINEARREG.htm).  
### LINEARREG_ANGLE - Linear Regression Angle
> 函数名：LINEARREG_ANGLE  
名称：线性回归的角度   
简介：来确定价格的角度变化. 
[参考](http://blog.sina.com.cn/s/blog_14c9f45b20102vv8p.md)
```python
real = LINEARREG_ANGLE(close, timeperiod=14)
```

Learn more about the Linear Regression Angle at [tadoc.org](http://www.tadoc.org/indicator/LINEARREG_ANGLE.htm).  
### LINEARREG_INTERCEPT - Linear Regression Intercept
> 函数名：LINEARREG_INTERCEPT  
名称：线性回归截距  
```python
real = LINEARREG_INTERCEPT(close, timeperiod=14)
```

Learn more about the Linear Regression Intercept at [tadoc.org](http://www.tadoc.org/indicator/LINEARREG_INTERCEPT.htm).  
### LINEARREG_SLOPE - Linear Regression Slope
> 函数名：LINEARREG_SLOPE  
名称：线性回归斜率指标

```python
real = LINEARREG_SLOPE(close, timeperiod=14)
```

Learn more about the Linear Regression Slope at [tadoc.org](http://www.tadoc.org/indicator/LINEARREG_SLOPE.htm).  
### STDDEV - Standard Deviation
> 函数名：STDDEV  
名称：标准偏差   
简介：种量度数据分布的分散程度之标准，用以衡量数据值偏离算术平均值的程度。标准偏差越小，这些值偏离平均值就越少，反之亦然。标准偏差的大小可通过标准偏差与平均值的倍率关系来衡量。

```python
real = STDDEV(close, timeperiod=5, nbdev=1)
```

Learn more about the Standard Deviation at [tadoc.org](http://www.tadoc.org/indicator/STDDEV.htm).  
### TSF - Time Series Forecast

> 函数名：TSF  
名称：时间序列预测   
简介：一种历史资料延伸预测，也称历史引伸预测法。是以时间数列所能反映的社会经济现象的发展过程和规律性，进行引伸外推，预测其发展趋势的方法


```python
real = TSF(close, timeperiod=14)
```

Learn more about the Time Series Forecast at [tadoc.org](http://www.tadoc.org/indicator/TSF.htm).  
### VAR - VAR
> 函数名：  VAR
名称：方差   
简介：方差用来计算每一个变量（观察值）与总体均数之间的差异。为避免出现离均差总和为零，离均差平方和受样本含量的影响，统计学采用平均离均差平方和来描述变量的变异程度

```python
real = VAR(close, timeperiod=5, nbdev=1)
```

Learn more about the Variance at [tadoc.org](http://www.tadoc.org/indicator/VAR.htm).  

[文档](../doc_index.md)
[FLOAT_RIGHTAll Function Groups](../funcs.md)
