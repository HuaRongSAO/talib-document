#Volume Indicators 成交量指标

### AD - Chaikin A/D Line 量价指标
> 函数名：AD  
名称：Chaikin A/D Line 累积/派发线（Accumulation/Distribution Line）  
简介：Marc Chaikin提出的一种平衡交易量指标，以当日的收盘价位来估算成交流量，用于估定一段时间内该证券累积的资金流量。  
计算公式：   
``` A/D = 昨日A/D + 多空对比 * 今日成交量    
多空对比 = [（收盘价- 最低价） - （最高价 - 收盘价）] / （最高价 - 最低价)
 ```
若最高价等于最低价： 多空对比 = （收盘价 / 昨收盘） - 1  
研判：    
1、A/D测量资金流向，向上的A/D表明买方占优势，而向下的A/D表明卖方占优势   
2、A/D与价格的背离可视为买卖信号，即底背离考虑买入，顶背离考虑卖出   
3、应当注意A/D忽略了缺口的影响，事实上，跳空缺口的意义是不能轻易忽略的   
A/D指标无需设置参数，但在应用时，可结合指标的均线进行分析

```python
real = AD(high, low, close, volume)
```

### ADOSC - Chaikin A/D Oscillator
> 函数名：ADOSC   
名称：Chaikin A/D Oscillator Chaikin震荡指标   
简介：将资金流动情况与价格行为相对比，检测市场中资金流入和流出的情况   
计算公式：fastperiod A/D - slowperiod A/D   
研判：   
1、交易信号是背离：看涨背离做多，看跌背离做空   
2、股价与90天移动平均结合，与其他指标结合   
3、由正变负卖出，由负变正买进   

```python
real = ADOSC(high, low, close, volume, fastperiod=3, slowperiod=10)
```

### OBV - On Balance Volume

> 函数名：OBV   
名称：On Balance Volume 能量潮   
简介：Joe Granville提出，通过统计成交量变动的趋势推测股价趋势   
计算公式：以某日为基期，逐日累计每日上市股票总成交量，若隔日指数或股票上涨
，则基期OBV加上本日成交量为本日OBV。隔日指数或股票下跌，
则基期OBV减去本日成交量为本日OBV   
研判：   
1、以“N”字型为波动单位，一浪高于一浪称“上升潮”，下跌称“跌潮”；上升潮买进，跌潮卖出   
2、须配合K线图走势   
3、用多空比率净额法进行修正，但不知TA-Lib采用哪种方法   
```计算公式： 多空比率净额= [（收盘价－最低价）－（最高价-收盘价）] ÷（ 最高价－最低价）×成交量```  
```python
real = OBV(close, volume)
```

[文档](../doc_index.md)
[函数分组](../funcs.md)
