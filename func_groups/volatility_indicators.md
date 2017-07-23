# Volatility Indicator Functions 波动率指标函数
### ATR - Average True Range

> 函数名：ATR  
名称：真实波动幅度均值   
简介：真实波动幅度均值（ATR)是
以 N 天的指数移动平均数平均後的交易波动幅度。 
计算公式：一天的交易幅度只是单纯地 最大值 - 最小值。  
而真实波动幅度则包含昨天的收盘价，若其在今天的幅度之外：  
真实波动幅度 = max(最大值,昨日收盘价) − min(最小值,昨日收盘价) 真实波动幅度均值便是「真实波动幅度」的 N 日 指数移动平均数。  

特性：：  
* 波动幅度的概念表示可以显示出交易者的期望和热情。  
* 大幅的或增加中的波动幅度表示交易者在当天可能准备持续买进或卖出股票。  
* 波动幅度的减少则表示交易者对股市没有太大的兴趣。  

NOTE: The ``ATR`` function has an unstable period.  

```python
real = ATR(high, low, close, timeperiod=14)
```

Learn more about the Average True Range at [tadoc.org](http://www.tadoc.org/indicator/ATR.htm).  
### NATR - Normalized Average True Range
> 函数名：NATR  
名称：归一化波动幅度均值   
简介：归一化波动幅度均值（NATR)是

NOTE: The ``NATR`` function has an unstable period.  
```python
real = NATR(high, low, close, timeperiod=14)
```

Learn more about the Normalized Average True Range at [tadoc.org](http://www.tadoc.org/indicator/NATR.htm).  
### TRANGE - True Range

> 函数名：TRANGE  
名称：真正的范围   

```python
real = TRANGE(high, low, close)
```

Learn more about the True Range at [tadoc.org](http://www.tadoc.org/indicator/TRANGE.htm).  

[Documentation Index](../doc_index.md)
[FLOAT_RIGHTAll Function Groups](../funcs.md)
