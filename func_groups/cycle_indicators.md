# Cycle Indicator Functions
> 不是很懂，欢迎指教
### HT_DCPERIOD - Hilbert Transform - Dominant Cycle Period
> 函数名：HT_DCPERIOD   
名称： 希尔伯特变换-主导周期   
简介：将价格作为信息信号，计算价格处在的周期的位置，作为择时的依据。   

[文库文档](https://wenku.baidu.com/view/0e35f6eead51f01dc281f18e.md)  

NOTE: The ``HT_DCPERIOD`` function has an unstable period.  
```python
real = HT_DCPERIOD(close)
```

Learn more about the Hilbert Transform - Dominant Cycle Period at [tadoc.org](http://www.tadoc.org/indicator/HT_DCPERIOD.htm).  
### HT_DCPHASE - Hilbert Transform - Dominant Cycle Phase

> 函数名：HT_DCPHASE   
名称： 希尔伯特变换-主导循环阶段 


NOTE: The ``HT_DCPHASE`` function has an unstable period.  
```python
real = HT_DCPHASE(close)
```

Learn more about the Hilbert Transform - Dominant Cycle Phase at [tadoc.org](http://www.tadoc.org/indicator/HT_DCPHASE.htm).  
### HT_PHASOR - Hilbert Transform - Phasor Components
> 函数名：HT_DCPHASE   
名称： 希尔伯特变换-希尔伯特变换相量分量 

NOTE: The ``HT_PHASOR`` function has an unstable period.  
```python
inphase, quadrature = HT_PHASOR(close)
```

Learn more about the Hilbert Transform - Phasor Components at [tadoc.org](http://www.tadoc.org/indicator/HT_PHASOR.htm).  
### HT_SINE - Hilbert Transform - SineWave

> 函数名：HT_DCPHASE   
名称： 希尔伯特变换-正弦波 
NOTE: The ``HT_SINE`` function has an unstable period.  
```python
sine, leadsine = HT_SINE(close)
```

Learn more about the Hilbert Transform - SineWave at [tadoc.org](http://www.tadoc.org/indicator/HT_SINE.htm).  

### HT_TRENDMODE - Hilbert Transform - Trend vs Cycle Mode

> 函数名：HT_DCPHASE   
名称： 希尔伯特变换-趋势与周期模式  
NOTE: The ``HT_TRENDMODE`` function has an unstable period. 

```python
integer = HT_TRENDMODE(close)
```

Learn more about the Hilbert Transform - Trend vs Cycle Mode at [tadoc.org](http://www.tadoc.org/indicator/HT_TRENDMODE.htm).  

[文档](../doc_index.md)
[FLOAT_RIGHTAll Function Groups](../funcs.md)
