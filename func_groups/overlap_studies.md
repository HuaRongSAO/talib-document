# Overlap Studies Functions 重叠研究指标
### BBANDS - Bollinger Bands

> 函数名：BBANDS   
名称： 布林线指标  
简介：其利用统计原理，求出股价的标准差及其信赖区间，从而确定股价的波动范围及未来走势，利用波带显示股价的安全高低价位，因而也被称为布林带。    
分析和应用：
[百度百科](https://baike.baidu.com/item/bollinger%20bands/1612394?fr=aladdin) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/56d0d9be66b4f7a0?rid=53)   

```python
upperband, middleband, lowerband = BBANDS(close, timeperiod=5, nbdevup=2, nbdevdn=2, matype=0)
```

Learn more about the Bollinger Bands at [tadoc.org](http://www.tadoc.org/indicator/BBANDS.htm).  
### DEMA - Double Exponential Moving Average  双移动平均线

> 函数名：DEMA   
名称： 双移动平均线  
简介：两条移动平均线来产生趋势信号，较长期者用来识别趋势，较短期者用来选择时机。正是两条平均线及价格三者的相互作用，才共同产生了趋势信号。    
分析和应用：
[百度百科](https://baike.baidu.com/item/%E5%8F%8C%E7%A7%BB%E5%8A%A8%E5%B9%B3%E5%9D%87%E7%BA%BF/1831921?fr=aladdin) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/a04d723659318237)   

```python
real = DEMA(close, timeperiod=30)
```

Learn more about the Double Exponential Moving Average at [tadoc.org](http://www.tadoc.org/indicator/DEMA.htm).  
### EMA - Exponential Moving Average

> 函数名：EMA   
名称： 指数平均数  
简介：是一种趋向类指标，其构造原理是仍然对价格收盘价进行算术平均，并根据计算结果来进行分析，用于判断价格未来走势的变动趋势。  
[百度百科](https://baike.baidu.com/item/EMA/12646151) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/b7a39d74783ad689?rid=589)   


NOTE: The ``EMA`` function has an unstable period.  
```python
real = EMA(close, timeperiod=30)
```

Learn more about the Exponential Moving Average at [tadoc.org](http://www.tadoc.org/indicator/EMA.htm).  
### HT_TRENDLINE - Hilbert Transform - Instantaneous Trendline
NOTE: The ``HT_TRENDLINE`` function has an unstable period.  

> 函数名：HT_TRENDLINE   
名称： 希尔伯特瞬时变换  
简介：是一种趋向类指标，其构造原理是仍然对价格收盘价进行算术平均，并根据计算结果来进行分析，用于判断价格未来走势的变动趋势。  
[百度文库](https://wenku.baidu.com/view/0e35f6eead51f01dc281f18e.html) 

```python
real = HT_TRENDLINE(close)
```

Learn more about the Hilbert Transform - Instantaneous Trendline at [tadoc.org](http://www.tadoc.org/indicator/HT_TRENDLINE.htm).  
### KAMA - Kaufman Adaptive Moving Average 考夫曼的自适应移动平均线

> 函数名：KAMA   
名称： 考夫曼的自适应移动平均线  
简介：短期均线贴近价格走势，灵敏度高，但会有很多噪声，产生虚假信号；长期均线在判断趋势上一般比较准确
，但是长期均线有着严重滞后的问题。我们想得到这样的均线，当价格沿一个方向快速移动时，短期的移动
平均线是最合适的；当价格在横盘的过程中，长期移动平均线是合适的。  
[参考1](http://blog.sina.com.cn/s/blog_62d0bbc701010p7d.html) 
[参考2](https://wenku.baidu.com/view/bc4bc9c59ec3d5bbfd0a7454.html?from=search)

NOTE: The ``KAMA`` function has an unstable period.  
```python
real = KAMA(close, timeperiod=30)
```

Learn more about the Kaufman Adaptive Moving Average at [tadoc.org](http://www.tadoc.org/indicator/KAMA.htm).  
### MA - Moving average  移动平均线

> 函数名：MA   
名称： 移动平均线  
简介：移动平均线，Moving Average，简称MA，原本的意思是移动平均，由于我们将其制作成线形，所以一般称之为移动平均线，简称均线。它是将某一段时间的收盘价之和除以该周期。 比如日线MA5指5天内的收盘价除以5 。  
[百度百科](https://baike.baidu.com/item/%E7%A7%BB%E5%8A%A8%E5%B9%B3%E5%9D%87%E7%BA%BF/217887?fromtitle=MA&fromid=1511750#viewPageContent) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/a04d723659318237?rid=96)   


```python
real = MA(close, timeperiod=30, matype=0)
```

### MAMA - MESA Adaptive Moving Average
NOTE: The ``MAMA`` function has an unstable period.  
```python
mama, fama = MAMA(close, fastlimit=0, slowlimit=0)
```

Learn more about the MESA Adaptive Moving Average at [tadoc.org](http://www.tadoc.org/indicator/MAMA.htm).  
### MAVP - Moving average with variable period
```python
real = MAVP(close, periods, minperiod=2, maxperiod=30, matype=0)
```

### MIDPOINT - MidPoint over period
```python
real = MIDPOINT(close, timeperiod=14)
```

Learn more about the MidPoint over period at [tadoc.org](http://www.tadoc.org/indicator/MIDPOINT.htm).  
### MIDPRICE - Midpoint Price over period
```python
real = MIDPRICE(high, low, timeperiod=14)
```

Learn more about the Midpoint Price over period at [tadoc.org](http://www.tadoc.org/indicator/MIDPRICE.htm).  
### SAR - Parabolic SAR  抛物线指标

> 函数名：SAR   
名称： 抛物线指标  
简介：抛物线转向也称停损点转向，是利用抛物线方式，随时调整停损点位置以观察买卖点。由于停损点（又称转向点SAR）以弧形的方式移动，故称之为抛物线转向指标    。  
[百度百科](https://baike.baidu.com/item/SAR/2771135#viewPageContent) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/d9d94e65be7f6b5e)   


```python
real = SAR(high, low, acceleration=0, maximum=0)
```

Learn more about the Parabolic SAR at [tadoc.org](http://www.tadoc.org/indicator/SAR.htm).  
### SAREXT - Parabolic SAR - Extended
```python
real = SAREXT(high, low, startvalue=0, offsetonreverse=0, accelerationinitlong=0, accelerationlong=0, accelerationmaxlong=0, accelerationinitshort=0, accelerationshort=0, accelerationmaxshort=0)
```

### SMA - Simple Moving Average 简单移动平均线

> 函数名：SMA  
名称： 简单移动平均线  
简介：移动平均线，Moving Average，简称MA，原本的意思是移动平均，由于我们将其制作成线形，所以一般称之为移动平均线，简称均线。它是将某一段时间的收盘价之和除以该周期。 比如日线MA5指5天内的收盘价除以5 。  
[百度百科](https://baike.baidu.com/item/%E7%A7%BB%E5%8A%A8%E5%B9%B3%E5%9D%87%E7%BA%BF/217887?fromtitle=MA&fromid=1511750#viewPageContent) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/a04d723659318237?rid=96)   


```python
real = SMA(close, timeperiod=30)
```

Learn more about the Simple Moving Average at [tadoc.org](http://www.tadoc.org/indicator/SMA.htm).  
### T3 - Triple Exponential Moving Average (T3) 三重指数移动平均线

> 函数名：T3  
名称：三重指数移动平均线  
简介：TRIX长线操作时采用本指标的讯号，长时间按照本指标讯号交易，获利百分比大于损失百分比，利润相当可观。 比如日线MA5指5天内的收盘价除以5 。  
[百度百科](https://baike.baidu.com/item/%E4%B8%89%E9%87%8D%E6%8C%87%E6%95%B0%E5%B9%B3%E6%BB%91%E5%B9%B3%E5%9D%87%E7%BA%BF/15749345?fr=aladdin) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/6c22c15ccbf24e64?rid=80)   



NOTE: The ``T3`` function has an unstable period.  
```python
real = T3(close, timeperiod=5, vfactor=0)
```

Learn more about the Triple Exponential Moving Average (T3) at [tadoc.org](http://www.tadoc.org/indicator/T3.htm).  
### TEMA - Triple Exponential Moving Average

> 函数名：TEMA（T3 区别？）
名称：三重指数移动平均线  


```python
real = TEMA(close, timeperiod=30)
```

Learn more about the Triple Exponential Moving Average at [tadoc.org](http://www.tadoc.org/indicator/TEMA.htm).  
### TRIMA - Triangular Moving Average
```python
real = TRIMA(close, timeperiod=30)
```

Learn more about the Triangular Moving Average at [tadoc.org](http://www.tadoc.org/indicator/TRIMA.htm).  
### WMA - Weighted Moving Average 移动加权平均法

> 函数名：WMA  
名称：加权移动平均线  
简介：移动加权平均法是指以每次进货的成本加上原有库存存货的成本，除以每次进货数量与原有库存存货的数量之和，据以计算加权平均单位成本，以此为基础计算当月发出存货的成本和期末存货的成本的一种方法。  
[百度百科](https://baike.baidu.com/item/%E7%A7%BB%E5%8A%A8%E5%8A%A0%E6%9D%83%E5%B9%B3%E5%9D%87%E6%B3%95/10056490?fr=aladdin&fromid=16799870&fromtitle=%E5%8A%A0%E6%9D%83%E7%A7%BB%E5%8A%A8%E5%B9%B3%E5%9D%87) 
[同花顺学院](http://www.iwencai.com/yike/detail/auid/262b1dfd1c68ee30)   


```python
real = WMA(close, timeperiod=30)
```

Learn more about the Weighted Moving Average at [tadoc.org](http://www.tadoc.org/indicator/WMA.htm).  

[Documentation Index](../doc_index.md)
[FLOAT_RIGHTAll Function Groups](../funcs.md)
