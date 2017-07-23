# 抽象API快速开始

如果您已经熟悉使用函数API，那么您就应该在精通使用抽象API。
每个函数有相同的输入，作为一个字典通过NumPy数组：

```python
import numpy as np
#请注意，所有的ndarrays必须是相同的长度！
inputs = {
    'open': np.random.random(100),
    'high': np.random.random(100),
    'low': np.random.random(100),
    'close': np.random.random(100),
    'volume': np.random.random(100)
}
```

函数可以直接导入，也可以用名称实例化：

```python
from talib import abstract
sma = abstract.SMA
sma = abstract.Function('sma')
```
调用函数基本上与函数API相同：

```python
from talib.abstract import *
output = SMA(input_arrays, timeperiod=25) # calculate on close prices by default
output = SMA(input_arrays, timeperiod=25, price='open') # calculate on opens
upper, middle, lower = BBANDS(input_arrays, 20, 2, 2)
slowk, slowd = STOCH(input_arrays, 5, 3, 0, 3, 0) # uses high, low, close by default
slowk, slowd = STOCH(input_arrays, 5, 3, 0, 3, 0, prices=['high', 'low', 'open'])
```

## 高级用法

For more advanced use cases of TA-Lib, the Abstract API also offers much more
flexibility. You can even subclass ``abstract.Function`` and override
``set_input_arrays`` to customize the type of input data Function accepts
(e.g. a pandas DataFrame).  
对于更高级的TA库用例，抽象API也提供了更大的灵活性。
你甚至可以子类``abstract.Function``和覆盖`` set_input_arrays``自定义类型的输入数据的函数接受
(e.g. a pandas DataFrame).

Details about every function can be accessed via the info property:   
有关每个功能的详细信息可以通过信息属性访问：

```python
print Function('stoch').info
{
  'name': 'STOCH',
  'display_name': 'Stochastic',
  'group': 'Momentum Indicators',
  'input_names': OrderedDict([
    ('prices', ['high', 'low', 'close']),
  ]),
  'parameters': OrderedDict([
    ('fastk_period', 5),
    ('slowk_period', 3),
    ('slowk_matype', 0),
    ('slowd_period', 3),
    ('slowd_matype', 0),
  ]),
  'output_names': ['slowk', 'slowd'],
}

```
或者是可读的格式：
```python
help(STOCH)
str(STOCH)
```

其他有用属性 ``Function``:

```python
Function('x').function_flags
Function('x').input_names
Function('x').input_arrays
Function('x').parameters
Function('x').lookback
Function('x').output_names
Function('x').output_flags
Function('x').outputs
```

Aside from calling the function directly, Functions maintain state and will
remember their parameters/input_arrays after they've been set. You can set
parameters and recalculate with new input data using run():   
除了直接调用函数，函数还可以保持状态，已经记住他们的 参数/数组
你可以设置参数，重新计算使用run()新输入数据
```python
SMA.parameters = {'timeperiod': 15}
result1 = SMA.run(input_arrays1)
result2 = SMA.run(input_arrays2)

# Or set input_arrays and change the parameters:
SMA.input_arrays = input_arrays1
ma10 = SMA(timeperiod=10)
ma20 = SMA(20)
```


欲了解更多详情，请看 [code](https://github.com/mrjbq7/ta-lib/blob/master/talib/abstract.pyx#L46).

[文档](doc_index.md)
