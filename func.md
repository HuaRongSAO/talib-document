# Function API Examples

Similar to TA-Lib, the function interface provides a lightweight wrapper of
the exposed TA-Lib indicators.   
类似于TA库，对函数接口进行了一个轻量级的封装，用于公开的ta-lib的指标。
 
Each function returns an output array and have default values for their
parameters, unless specified as keyword arguments. Typically, these functions
will have an initial "lookback" period (a required number of observations
before an output is generated) set to ``NaN``.   
每个函数都默认需要输入数组，并为它们提供默认值。 参数，除非指定为关键字参数。通常，这些函数 会有一个初步的“lookback”时期（观测所需数量 在生成一个输出之前），设置为“NaN”。


All of the following examples use the function API:  
所有的API函数的使用，都需引入库文件：

```python
import numpy
import talib

close = numpy.random.random(100)
```

计算收盘价的一个简单移动平均数SMA:

```python
output = talib.SMA(close)
```

计算布林线，三指数移动平均：

```python
from talib import MA_Type

upper, middle, lower = talib.BBANDS(close, matype=MA_Type.T3)
```

计算收盘价的动量，时间为5：

```python
output = talib.MOM(close, timeperiod=5)
```


方法类型分组:

* [Overlap Studies](func_groups/overlap_studies.md)
* [Momentum Indicators](func_groups/momentum_indicators.md)
* [Volume Indicators](func_groups/volume_indicators.md)
* [Volatility Indicators](func_groups/volatility_indicators.md)
* [Pattern Recognition](func_groups/pattern_recognition.md)
* [Cycle Indicators](func_groups/cycle_indicators.md)
* [Statistic Functions](func_groups/statistic_functions.md)
* [Price Transform](func_groups/price_transform.md)
* [Math Transform](func_groups/math_transform.md)
* [Math Operators](func_groups/math_operators.md)

[文档](doc_index.md)
[下一章: Using the Abstract API](abstract.md)
