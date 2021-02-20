# TA-Lib
# 简介：
Talib一直缺乏有效的中文文档，自己又有空闲时间，且在研究量化对冲系统，就发点时间，做一下翻译。
原文地址： [TA-LIB document](https://mrjbq7.github.io/ta-lib/)
翻译地址：

这是一个Python 金融指数处理库[TA-LIB](http://ta-lib.org)，他是基于 Cython
而不是 SWIG。

> TA-Lib is widely used by trading software developers requiring to perform
> technical analysis of financial market data.  
> TA-Lib广泛应用与交易软件，和金融市场数据进行技术分析。

> * Includes 150+ indicators such as ADX, MACD, RSI, Stochastic, Bollinger
>   Bands, etc.
> * Candlestick pattern recognition
> * Open-source API for C/C++, Java, Perl, Python and 100% Managed .NET    
> * 包含了150多个指标,包括：ADX, MACD, RSI, Stochastic, Bollinger Bands, 等.
> * K线形态识别
> * 完全开源，支持 C/C++, Java, Perl, Python and 100% Managed .NET



#### 安装TA-Lib

## 案例（快速开始）

Similar to TA-Lib, the function interface provides a lightweight wrapper of
the exposed TA-Lib indicators.  
类似于TA-Lib，函数接口提供了一个暴露TA-Lib指标的轻量级封装。

Each function returns an output array and have default values for their
parameters, unless specified as keyword arguments. Typically, these functions
will have an initial "lookback" period (a required number of observations
before an output is generated) set to ``NaN``.   
每个函数都默认需要输入数组，并为它们提供默认值。
参数，除非指定为关键字参数。通常，这些函数
会有一个初步的“lookback”时期（观测所需数量
在生成一个输出之前），设置为“NaN”。

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

## Abstract API Quick Start 抽象 API 快速入门

If you're already familiar with using the function API, you should feel right
at home using the abstract API. Every function takes the same input, passed
as a dictionary of Numpy arrays:   
如果您已经熟悉使用函数API，那么您就应该精通使用抽象API。
每个函数有相同的输入，作为一个字典通过NumPy数组：

```python
import numpy as np
# note that all ndarrays must be the same length!
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
output = SMA(input_arrays, timeperiod=25) # SMA均线价格计算收盘价
output = SMA(input_arrays, timeperiod=25, price='open') # SMA均线价格计算收盘价
upper, middle, lower = BBANDS(input_arrays, 20, 2, 2)
slowk, slowd = STOCH(input_arrays, 5, 3, 0, 3, 0) # uses high, low, close by default
slowk, slowd = STOCH(input_arrays, 5, 3, 0, 3, 0, prices=['high', 'low', 'open'])
```

了解更多高级使用TA库 [here]().

## Supported Indicators 支持的指标

We can show all the TA functions supported by TA-Lib, either as a ``list`` or
as a ``dict`` sorted by group (e.g. "Overlap Studies", "Momentum Indicators",
etc):  
我们可以显示Ta lib的所有TA函数,返回一个 ``list`` 或者 ``dict`` 

```python
import talib

print talib.get_functions()
print talib.get_function_groups()
```

### Function Groups

* [Overlap Studies 重叠研究](func_groups/overlap_studies.md)
* [Momentum Indicators 动量指标](func_groups/momentum_indicators.md)
* [Volume Indicators 成交量指标](func_groups/volume_indicators.md)
* [Volatility Indicators 波动性指标](func_groups/volatility_indicators.md)
* [Price Transform 价格指标](func_groups/price_transform.md)
* [Cycle Indicators 周期指标](func_groups/cycle_indicators.md)
* [Pattern Recognition 形态识别](func_groups/pattern_recognition.md)
* [Statistic Functions 统计函数](func_groups/statistic_functions.md)
* [Math Transform 数学变换](func_groups/math_transform.md)
* [Math Operators 数学运算符](func_groups/math_operators.md)


#### [Overlap Studies](func_groups/overlap_studies.md)

```
BBANDS               Bollinger Bands #布林带
DEMA                 Double Exponential Moving Average #双指数移动平均线
EMA                  Exponential Moving Average #指数滑动平均
HT_TRENDLINE         Hilbert Transform - Instantaneous Trendline #希尔伯特变换瞬时趋势
KAMA                 Kaufman Adaptive Moving Average #卡玛考夫曼自适应移动平均
MA                   Moving average #均线
MAMA                 MESA Adaptive Moving Average #自适应移动平均 
MAVP                 Moving average with variable period #变周期移动平均
MIDPOINT             MidPoint over period #在周期的中点
MIDPRICE             Midpoint Price over period #中间时段价格
SAR                  Parabolic SAR #抛物线转向指标
SAREXT               Parabolic SAR - Extended #抛物线转向指标 - 扩展
SMA                  Simple Moving Average# 简单移动平均线
T3                   Triple Exponential Moving Average (T3)
TEMA                 Triple Exponential Moving Average#三次指数移动平均
TRIMA                Triangular Moving Average# 三角形移动平均
WMA                  Weighted Moving Average#加权移动平均线
```

#### [Momentum Indicators](func_groups/momentum_indicators.md)

```
ADX                  Average Directional Movement Index
ADXR                 Average Directional Movement Index Rating
APO                  Absolute Price Oscillator
AROON                Aroon
AROONOSC             Aroon Oscillator
BOP                  Balance Of Power
CCI                  Commodity Channel Index
CMO                  Chande Momentum Oscillator
DX                   Directional Movement Index
MACD                 Moving Average Convergence/Divergence
MACDEXT              MACD with controllable MA type
MACDFIX              Moving Average Convergence/Divergence Fix 12/26
MFI                  Money Flow Index
MINUS_DI             Minus Directional Indicator
MINUS_DM             Minus Directional Movement
MOM                  Momentum
PLUS_DI              Plus Directional Indicator
PLUS_DM              Plus Directional Movement
PPO                  Percentage Price Oscillator
ROC                  Rate of change : ((price/prevPrice)-1)*100
ROCP                 Rate of change Percentage: (price-prevPrice)/prevPrice
ROCR                 Rate of change ratio: (price/prevPrice)
ROCR100              Rate of change ratio 100 scale: (price/prevPrice)*100
RSI                  Relative Strength Index
STOCH                Stochastic
STOCHF               Stochastic Fast
STOCHRSI             Stochastic Relative Strength Index
TRIX                 1-day Rate-Of-Change (ROC) of a Triple Smooth EMA
ULTOSC               Ultimate Oscillator
WILLR                Williams' %R
```

#### [Volume Indicators](func_groups/volume_indicators.html)

```
AD                   Chaikin A/D Line
ADOSC                Chaikin A/D Oscillator
OBV                  On Balance Volume
```

#### [Volatility Indicators](func_groups/volatility_indicators.html)

```
ATR                  Average True Range
NATR                 Normalized Average True Range
TRANGE               True Range
```

#### [Price Transform](func_groups/price_transform.html)

```
AVGPRICE             Average Price
MEDPRICE             Median Price
TYPPRICE             Typical Price
WCLPRICE             Weighted Close Price
```

#### [Cycle Indicators](func_groups/cycle_indicators.html)

```
HT_DCPERIOD          Hilbert Transform - Dominant Cycle Period
HT_DCPHASE           Hilbert Transform - Dominant Cycle Phase
HT_PHASOR            Hilbert Transform - Phasor Components
HT_SINE              Hilbert Transform - SineWave
HT_TRENDMODE         Hilbert Transform - Trend vs Cycle Mode
```

#### [Pattern Recognition](func_groups/pattern_recognition.html)

```
CDL2CROWS            Two Crows
CDL3BLACKCROWS       Three Black Crows
CDL3INSIDE           Three Inside Up/Down
CDL3LINESTRIKE       Three-Line Strike
CDL3OUTSIDE          Three Outside Up/Down
CDL3STARSINSOUTH     Three Stars In The South
CDL3WHITESOLDIERS    Three Advancing White Soldiers
CDLABANDONEDBABY     Abandoned Baby
CDLADVANCEBLOCK      Advance Block
CDLBELTHOLD          Belt-hold
CDLBREAKAWAY         Breakaway
CDLCLOSINGMARUBOZU   Closing Marubozu
CDLCONCEALBABYSWALL  Concealing Baby Swallow
CDLCOUNTERATTACK     Counterattack
CDLDARKCLOUDCOVER    Dark Cloud Cover
CDLDOJI              Doji
CDLDOJISTAR          Doji Star
CDLDRAGONFLYDOJI     Dragonfly Doji
CDLENGULFING         Engulfing Pattern
CDLEVENINGDOJISTAR   Evening Doji Star
CDLEVENINGSTAR       Evening Star
CDLGAPSIDESIDEWHITE  Up/Down-gap side-by-side white lines
CDLGRAVESTONEDOJI    Gravestone Doji
CDLHAMMER            Hammer
CDLHANGINGMAN        Hanging Man
CDLHARAMI            Harami Pattern
CDLHARAMICROSS       Harami Cross Pattern
CDLHIGHWAVE          High-Wave Candle
CDLHIKKAKE           Hikkake Pattern
CDLHIKKAKEMOD        Modified Hikkake Pattern
CDLHOMINGPIGEON      Homing Pigeon
CDLIDENTICAL3CROWS   Identical Three Crows
CDLINNECK            In-Neck Pattern
CDLINVERTEDHAMMER    Inverted Hammer
CDLKICKING           Kicking
CDLKICKINGBYLENGTH   Kicking - bull/bear determined by the longer marubozu
CDLLADDERBOTTOM      Ladder Bottom
CDLLONGLEGGEDDOJI    Long Legged Doji
CDLLONGLINE          Long Line Candle
CDLMARUBOZU          Marubozu
CDLMATCHINGLOW       Matching Low
CDLMATHOLD           Mat Hold
CDLMORNINGDOJISTAR   Morning Doji Star
CDLMORNINGSTAR       Morning Star
CDLONNECK            On-Neck Pattern
CDLPIERCING          Piercing Pattern
CDLRICKSHAWMAN       Rickshaw Man
CDLRISEFALL3METHODS  Rising/Falling Three Methods
CDLSEPARATINGLINES   Separating Lines
CDLSHOOTINGSTAR      Shooting Star
CDLSHORTLINE         Short Line Candle
CDLSPINNINGTOP       Spinning Top
CDLSTALLEDPATTERN    Stalled Pattern
CDLSTICKSANDWICH     Stick Sandwich
CDLTAKURI            Takuri (Dragonfly Doji with very long lower shadow)
CDLTASUKIGAP         Tasuki Gap
CDLTHRUSTING         Thrusting Pattern
CDLTRISTAR           Tristar Pattern
CDLUNIQUE3RIVER      Unique 3 River
CDLUPSIDEGAP2CROWS   Upside Gap Two Crows
CDLXSIDEGAP3METHODS  Upside/Downside Gap Three Methods
```

#### [Statistic Functions](func_groups/statistic_functions.html)

```
BETA                 Beta
CORREL               Pearson's Correlation Coefficient (r)
LINEARREG            Linear Regression
LINEARREG_ANGLE      Linear Regression Angle
LINEARREG_INTERCEPT  Linear Regression Intercept
LINEARREG_SLOPE      Linear Regression Slope
STDDEV               Standard Deviation
TSF                  Time Series Forecast
VAR                  Variance
```

我想成为一名依靠乞讨的程序员。   

![164938069.png](https://upload-images.jianshu.io/upload_images/6167081-bd931bef186e212e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
