# Momentum Indicator Functions
### ADX - Average Directional Movement Index
> 函数名：ADX  
名称：平均趋向指数  
简介：使用ADX指标，指标判断盘整、振荡和单边趋势。
#### 公式：
一、先决定股价趋势（Directional Movement，DM）是上涨或下跌：   
“所谓DM值，今日股价波动幅度大于昨日股价波动幅部分的最大值，可能是创高价的部分或创低价的部分；如果今日股价波动幅度较前一日小，则DM = 0。”   
若股价高点持续走高，为上涨趋势，记作 +DM。   
若为下跌趋势，记作 -DM。-DM的负号（–）是表示反向趋势（下跌），并非数值为负数。   
其他状况：DM = 0。   
二、寻找股价的真实波幅（True Range，TR）：   
所谓真实波幅（TR）是以最高价，最低价，及前一日收盘价三个价格做比较，求出当日股价波动的最大幅度。   
三、趋势方向需经由一段时间来观察，研判上才有意义。一般以14天为指标的观察周期：   
先计算出 +DM、–DM及TR的14日算术平均数，得到 +DM14、–DM14及TR14三组数据作为起始值，再计算各自的移动平均值（EMA）。   
```
    +DI14 = +DM/TR14*100
    -DI14 = +DM/TR14*100
    
    DX = |(+DI14)-(-DI14)| / |(+DI14)+(-DI14)|
    
    DX运算结果取其绝对值，再将DX作移动平均，得到ADX。
```

#### 特点：  
* ADX无法告诉你趋势的发展方向。
* 如果趋势存在，ADX可以衡量趋势的强度。不论上升趋势或下降趋势，ADX看起来都一样。
* ADX的读数越大，趋势越明显。衡量趋势强度时，需要比较几天的ADX 读数，观察ADX究竟是上升或下降。ADX读数上升，代表趋势转强；如果ADX读数下降，意味着趋势转弱。
* 当ADX曲线向上攀升，趋势越来越强，应该会持续发展。如果ADX曲线下滑，代表趋势开始转弱，反转的可能性增加。
* 单就ADX本身来说，由于指标落后价格走势，所以算不上是很好的指标，不适合单就ADX进行操作。可是，如果与其他指标配合运用，ADX可以确认市场是否存在趋势，并衡量趋势的强度。

#### 指标应用：
* +DI与–DI表示多空相反的二个动向，当据此绘出的两条曲线彼此纠结相缠时，代表上涨力道与下跌力道相当，多空势均力敌。当 +DI与–DI彼此穿越时，由下往上的一方其力道开始压过由上往下的另一方，此时出现买卖讯号。
* ADX可作为趋势行情的判断依据，当行情明显朝多空任一方向进行时，ADX数值都会显著上升，趋势走强。若行情呈现盘整格局时，ADX会低于 +DI与–DI二条线。若ADX数值低于20，则不论DI表现如何，均显示市场没有明显趋势。
* ADX持续偏高时，代表“超买”（Overbought）或“超卖”（Oversold）的现象，行情反转的机会将增加，此时则不适宜顺势操作。当ADX数值从上升趋势转为下跌时，则代表行情即将反转；若ADX数值由下跌趋势转为上升时，行情将止跌回升。
* 总言之，DMI指标包含4条线：+DI、-DI、ADX和ADXR。+DI代表买盘的强度、-DI代表卖盘的强度；ADX代表趋势的强度、ADXR则为ADX的移动平均。

NOTE: The ``ADX`` function has an unstable period.  
```python
real = ADX(high, low, close, timeperiod=14)
```

Learn more about the Average Directional Movement Index at [tadoc.org](http://www.tadoc.org/indicator/ADX.htm).  
###  ADXR- Average Directional Movement Index Rating
> 函数名：ADXR  
名称：平均趋向指数的趋向指数  
简介：使用ADXR指标，指标判断ADX趋势。
NOTE: The ``ADXR`` function has an unstable period.  
```python
real = ADXR(high, low, close, timeperiod=14)
```

Learn more about the Average Directional Movement Index Rating at [tadoc.org](http://www.tadoc.org/indicator/ADXR.htm).  
### APO - Absolute Price Oscillator
```python
real = APO(close, fastperiod=12, slowperiod=26, matype=0)
```

Learn more about the Absolute Price Oscillator at [tadoc.org](http://www.tadoc.org/indicator/APO.htm).  
### AROON - Aroon
> 函数名：AROON  
名称：阿隆指标  
简介：该指标是通过计算自价格达到近期最高值和最低值以来所经过的期间数，阿隆指标帮助你预测价格趋势到趋势区域（或者反过来，从趋势区域到趋势）的变化。  
#### 计算公式：
``` 
Aroon(上升)=[(计算期天数-最高价后的天数)/计算期天数]*100
Aroon(下降)=[(计算期天数-最低价后的天数)/计算期天数]*100
```
#### 指数应用
1、极值0和100  
当UP线达到100时，市场处于强势；如果维持在70~100之间，表示一个上升趋势。同样，如果Down线达到0，表示处于弱势，如果维持在0~30之间，表示处于下跌趋势。如果两条线同处于极值水平，则表明一个更强的趋势。  
2、平行运动  
如果两条线平行运动时，表明市场趋势被打破。可以预期该状况将持续下去，只到由极值水平或交叉穿行西安市出方向性运动为止。  
3、交叉穿行  
当下行线上穿上行线时，表明潜在弱势，预期价格开始趋于下跌。反之，表明潜在强势，预期价格趋于走高。  

```python
aroondown, aroonup = AROON(high, low, timeperiod=14)
```

Learn more about the Aroon at [tadoc.org](http://www.tadoc.org/indicator/AROON.htm).  
### AROONOSC - Aroon Oscillator
> 函数名：AROONOSC  
名称：阿隆振荡  
简介：
```python
real = AROONOSC(high, low, timeperiod=14)
```

Learn more about the Aroon Oscillator at [tadoc.org](http://www.tadoc.org/indicator/AROONOSC.htm).  
### BOP - Balance Of Power 均势
> 函数名：BOP  
名称：均势指标  
简介
```python
real = BOP(open, high, low, close)
```

Learn more about the Balance Of Power at [tadoc.org](http://www.tadoc.org/indicator/BOP.htm).  
### CCI - Commodity Channel Index
> 函数名：CCI  
名称：顺势指标  
简介：CCI指标专门测量股价是否已超出常态分布范围

#### 指标应用
* 1.当CCI指标曲线在+100线～-100线的常态区间里运行时,CCI指标参考意义不大，可以用KDJ等其它技术指标进行研判。
* 2.当CCI指标曲线从上向下突破+100线而重新进入常态区间时，表明市场价格的上涨阶段可能结束，将进入一个比较长时间的震荡整理阶段，应及时平多做空。
* 3.当CCI指标曲线从上向下突破-100线而进入另一个非常态区间（超卖区）时，表明市场价格的弱势状态已经形成，将进入一个比较长的寻底过程，可以持有空单等待更高利润。如果CCI指标曲线在超卖区运行了相当长的一段时间后开始掉头向上，表明价格的短期底部初步探明，可以少量建仓。CCI指标曲线在超卖区运行的时间越长，确认短期的底部的准确度越高。
* 4.CCI指标曲线从下向上突破-100线而重新进入常态区间时，表明市场价格的探底阶段可能结束，有可能进入一个盘整阶段，可以逢低少量做多。
* 5.CCI指标曲线从下向上突破+100线而进入非常态区间(超买区)时，表明市场价格已经脱离常态而进入强势状态，如果伴随较大的市场交投，应及时介入成功率将很大。
* 6.CCI指标曲线从下向上突破+100线而进入非常态区间(超买区)后，只要CCI指标曲线一直朝上运行，表明价格依然保持强势可以继续持有待涨。但是，如果在远离+100线的地方开始掉头向下时，则表明市场价格的强势状态将可能难以维持，涨势可能转弱，应考虑卖出。如果前期的短期涨幅过高同时价格回落时交投活跃，则应该果断逢高卖出或做空。
* CCI主要是在超买和超卖区域发生作用，对急涨急跌的行情检测性相对准确。非常适用于股票、外汇、贵金属等市场的短期操作。[1] 
```python
real = CCI(high, low, close, timeperiod=14)
```

Learn more about the Commodity Channel Index at [tadoc.org](http://www.tadoc.org/indicator/CCI.htm).  
### CMO - Chande Momentum Oscillator
NOTE: The ``CMO`` function has an unstable period.  
```python
real = CMO(close, timeperiod=14)
```

Learn more about the Chande Momentum Oscillator at [tadoc.org](http://www.tadoc.org/indicator/CMO.htm).  
### DX - Directional Movement Index
NOTE: The ``DX`` function has an unstable period.  
```python
real = DX(high, low, close, timeperiod=14)
```

Learn more about the Directional Movement Index at [tadoc.org](http://www.tadoc.org/indicator/DX.htm).  
### MACD - Moving Average Convergence/Divergence
```python
macd, macdsignal, macdhist = MACD(close, fastperiod=12, slowperiod=26, signalperiod=9)
```

Learn more about the Moving Average Convergence/Divergence at [tadoc.org](http://www.tadoc.org/indicator/MACD.htm).  
### MACDEXT - MACD with controllable MA type
```python
macd, macdsignal, macdhist = MACDEXT(close, fastperiod=12, fastmatype=0, slowperiod=26, slowmatype=0, signalperiod=9, signalmatype=0)
```

### MACDFIX - Moving Average Convergence/Divergence Fix 12/26
```python
macd, macdsignal, macdhist = MACDFIX(close, signalperiod=9)
```

### MFI - Money Flow Index
NOTE: The ``MFI`` function has an unstable period.  
```python
real = MFI(high, low, close, volume, timeperiod=14)
```

Learn more about the Money Flow Index at [tadoc.org](http://www.tadoc.org/indicator/MFI.htm).  
### MINUS_DI - Minus Directional Indicator
NOTE: The ``MINUS_DI`` function has an unstable period.  
```python
real = MINUS_DI(high, low, close, timeperiod=14)
```

Learn more about the Minus Directional Indicator at [tadoc.org](http://www.tadoc.org/indicator/MINUS_DI.htm).  
### MINUS_DM - Minus Directional Movement
NOTE: The ``MINUS_DM`` function has an unstable period.  
```python
real = MINUS_DM(high, low, timeperiod=14)
```

Learn more about the Minus Directional Movement at [tadoc.org](http://www.tadoc.org/indicator/MINUS_DM.htm).  
### MOM - Momentum
```python
real = MOM(close, timeperiod=10)
```

Learn more about the Momentum at [tadoc.org](http://www.tadoc.org/indicator/MOM.htm).  
### PLUS_DI - Plus Directional Indicator
NOTE: The ``PLUS_DI`` function has an unstable period.  
```python
real = PLUS_DI(high, low, close, timeperiod=14)
```

Learn more about the Plus Directional Indicator at [tadoc.org](http://www.tadoc.org/indicator/PLUS_DI.htm).  
### PLUS_DM - Plus Directional Movement
NOTE: The ``PLUS_DM`` function has an unstable period.  
```python
real = PLUS_DM(high, low, timeperiod=14)
```

Learn more about the Plus Directional Movement at [tadoc.org](http://www.tadoc.org/indicator/PLUS_DM.htm).  
### PPO - Percentage Price Oscillator
```python
real = PPO(close, fastperiod=12, slowperiod=26, matype=0)
```

Learn more about the Percentage Price Oscillator at [tadoc.org](http://www.tadoc.org/indicator/PPO.htm).  
### ROC - Rate of change : ((price/prevPrice)-1)*100
```python
real = ROC(close, timeperiod=10)
```

Learn more about the Rate of change : ((price/prevPrice)-1)*100 at [tadoc.org](http://www.tadoc.org/indicator/ROC.htm).  
### ROCP - Rate of change Percentage: (price-prevPrice)/prevPrice
```python
real = ROCP(close, timeperiod=10)
```

Learn more about the Rate of change Percentage: (price-prevPrice)/prevPrice at [tadoc.org](http://www.tadoc.org/indicator/ROCP.htm).  
### ROCR - Rate of change ratio: (price/prevPrice)
```python
real = ROCR(close, timeperiod=10)
```

Learn more about the Rate of change ratio: (price/prevPrice) at [tadoc.org](http://www.tadoc.org/indicator/ROCR.htm).  
### ROCR100 - Rate of change ratio 100 scale: (price/prevPrice)*100
```python
real = ROCR100(close, timeperiod=10)
```

Learn more about the Rate of change ratio 100 scale: (price/prevPrice)*100 at [tadoc.org](http://www.tadoc.org/indicator/ROCR100.htm).  
### RSI - Relative Strength Index
NOTE: The ``RSI`` function has an unstable period.  
```python
real = RSI(close, timeperiod=14)
```

Learn more about the Relative Strength Index at [tadoc.org](http://www.tadoc.org/indicator/RSI.htm).  
### STOCH - Stochastic
```python
slowk, slowd = STOCH(high, low, close, fastk_period=5, slowk_period=3, slowk_matype=0, slowd_period=3, slowd_matype=0)
```

Learn more about the Stochastic at [tadoc.org](http://www.tadoc.org/indicator/STOCH.htm).  
### STOCHF - Stochastic Fast
```python
fastk, fastd = STOCHF(high, low, close, fastk_period=5, fastd_period=3, fastd_matype=0)
```

Learn more about the Stochastic Fast at [tadoc.org](http://www.tadoc.org/indicator/STOCHF.htm).  
### STOCHRSI - Stochastic Relative Strength Index
NOTE: The ``STOCHRSI`` function has an unstable period.  
```python
fastk, fastd = STOCHRSI(close, timeperiod=14, fastk_period=5, fastd_period=3, fastd_matype=0)
```

Learn more about the Stochastic Relative Strength Index at [tadoc.org](http://www.tadoc.org/indicator/STOCHRSI.htm).  
### TRIX - 1-day Rate-Of-Change (ROC) of a Triple Smooth EMA
```python
real = TRIX(close, timeperiod=30)
```

Learn more about the 1-day Rate-Of-Change (ROC) of a Triple Smooth EMA at [tadoc.org](http://www.tadoc.org/indicator/TRIX.htm).  
### ULTOSC - Ultimate Oscillator
```python
real = ULTOSC(high, low, close, timeperiod1=7, timeperiod2=14, timeperiod3=28)
```

Learn more about the Ultimate Oscillator at [tadoc.org](http://www.tadoc.org/indicator/ULTOSC.htm).  
### WILLR - Williams' %R
```python
real = WILLR(high, low, close, timeperiod=14)
```

Learn more about the Williams' %R at [tadoc.org](http://www.tadoc.org/indicator/WILLR.htm).  

[Documentation Index](../doc_index.md)
[FLOAT_RIGHTAll Function Groups](../funcs.md)
