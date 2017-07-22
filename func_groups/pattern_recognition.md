# Pattern Recognition Functions 模式识别的功能
   
### CDL2CROWS - Two Crows
> 函数名：CDL2CROWS   
名称：Two Crows 两只乌鸦   
简介：三日K线模式，第一天长阳，第二天高开收阴，第三天再次高开继续收阴，
收盘比前一日收盘价低，预示股价下跌。

```python
integer = CDL2CROWS(open, high, low, close)
```

### CDL3BLACKCROWS - Three Black Crows
> 函数名：CDL3BLACKCROWS   
名称：Three Black Crows 三只乌鸦   
简介：三日K线模式，连续三根阴线，每日收盘价都下跌且接近最低价，
每日开盘价都在上根K线实体内，预示股价下跌。   

```python
integer = CDL3BLACKCROWS(open, high, low, close)
```

### CDL3INSIDE - Three Inside Up/Down
> 函数名：CDL3INSIDE   
名称： Three Inside Up/Down 三内部上涨和下跌   
简介：三日K线模式，母子信号+长K线，以三内部上涨为例，K线为阴阳阳，
第三天收盘价高于第一天开盘价，第二天K线在第一天K线内部，预示着股价上涨。
   
```python
integer = CDL3INSIDE(open, high, low, close)
```

### CDL3LINESTRIKE - Three-Line Strike 
> 函数名：CDL3LINESTRIKE   
名称： Three-Line Strike 三线打击   
简介：四日K线模式，前三根阳线，每日收盘价都比前一日高，
开盘价在前一日实体内，第四日市场高开，收盘价低于第一日开盘价，预示股价下跌。
   
```python
integer = CDL3LINESTRIKE(open, high, low, close)
```

### CDL3OUTSIDE - Three Outside Up/Down
> 函数名：CDL3OUTSIDE  
名称：Three Outside Up/Down 三外部上涨和下跌   
简介：三日K线模式，与三内部上涨和下跌类似，K线为阴阳阳，但第一日与第二日的K线形态相反，
以三外部上涨为例，第一日K线在第二日K线内部，预示着股价上涨。  

```python
integer = CDL3OUTSIDE(open, high, low, close)
```

### CDL3STARSINSOUTH - Three Stars In The South
> 函数名：CDL3STARSINSOUTH  
名称：Three Stars In The South 南方三星  
简介：三日K线模式，与大敌当前相反，三日K线皆阴，第一日有长下影线，
第二日与第一日类似，K线整体小于第一日，第三日无下影线实体信号，
成交价格都在第一日振幅之内，预示下跌趋势反转，股价上升。  

```python
integer = CDL3STARSINSOUTH(open, high, low, close)
```

### CDL3WHITESOLDIERS - Three Advancing White Soldiers
> 函数名：CDL3WHITESOLDIERS   
名称：Three Advancing White Soldiers 三个白兵  
简介：三日K线模式，三日K线皆阳，
每日收盘价变高且接近最高价，开盘价在前一日实体上半部，预示股价上升。

```python
integer = CDL3WHITESOLDIERS(open, high, low, close)
```

### CDLABANDONEDBABY - Abandoned Baby
> 函数名：CDLABANDONEDBABY  
名称：Abandoned Baby 弃婴  
简介：三日K线模式，第二日价格跳空且收十字星（开盘价与收盘价接近，
最高价最低价相差不大），预示趋势反转，发生在顶部下跌，底部上涨。  

```python
integer = CDLABANDONEDBABY(open, high, low, close, penetration=0)
```

### CDLADVANCEBLOCK - Advance Block
> 函数名：CDLADVANCEBLOCK   
名称：Advance Block 大敌当前   
简介：三日K线模式，三日都收阳，每日收盘价都比前一日高，
开盘价都在前一日实体以内，实体变短，上影线变长。   

```python
integer = CDLADVANCEBLOCK(open, high, low, close)
```

### CDLBELTHOLD - Belt-hold
> 函数名：CDLBELTHOLD   
名称：Belt-hold 捉腰带线   
简介：两日K线模式，下跌趋势中，第一日阴线，
第二日开盘价为最低价，阳线，收盘价接近最高价，预示价格上涨。   

```python
integer = CDLBELTHOLD(open, high, low, close)
```

### CDLBREAKAWAY - Breakaway
> 函数名：CDLBREAKAWAY  
名称：Breakaway 脱离  
简介：五日K线模式，以看涨脱离为例，下跌趋势中，第一日长阴线，第二日跳空阴线，延续趋势开始震荡，
第五日长阳线，收盘价在第一天收盘价与第二天开盘价之间，预示价格上涨。   

```python
integer = CDLBREAKAWAY(open, high, low, close)
```

### CDLCLOSINGMARUBOZU - Closing Marubozu
> 函数名：CDLCLOSINGMARUBOZU   
名称：Closing Marubozu 收盘缺影线  
简介：一日K线模式，以阳线为例，最低价低于开盘价，收盘价等于最高价，
预示着趋势持续。

```python
integer = CDLCLOSINGMARUBOZU(open, high, low, close)
```

### CDLCONCEALBABYSWALL - Concealing Baby Swallow
> 函数名：CDLCONCEALBABYSWALL   
名称： Concealing Baby Swallow 藏婴吞没   
简介：四日K线模式，下跌趋势中，前两日阴线无影线
，第二日开盘、收盘价皆低于第二日，第三日倒锤头，
第四日开盘价高于前一日最高价，收盘价低于前一日最低价，预示着底部反转。   

```python
integer = CDLCONCEALBABYSWALL(open, high, low, close)
```

### CDLCOUNTERATTACK - Counterattack
> 函数名：CDLCOUNTERATTACK  
名称：Counterattack 反击线  
简介：二日K线模式，与分离线类似。  

```python
integer = CDLCOUNTERATTACK(open, high, low, close)
```

### CDLDARKCLOUDCOVER - Dark Cloud Cover
> 函数名：CDLDARKCLOUDCOVER  
名称：Dark Cloud Cover 乌云压顶  
简介：二日K线模式，第一日长阳，第二日开盘价高于前一日最高价，
收盘价处于前一日实体中部以下，预示着股价下跌。  

```python
integer = CDLDARKCLOUDCOVER(open, high, low, close, penetration=0)
```

### CDLDOJI - Doji
> 函数名：CDLDOJI  
名称：Doji 十字  
简介：一日K线模式，开盘价与收盘价基本相同。  

```python
integer = CDLDOJI(open, high, low, close)
```

### CDLDOJISTAR - Doji Star
> 函数名：CDLDOJISTAR  
名称：Doji Star 十字星  
简介：一日K线模式，开盘价与收盘价基本相同，上下影线不会很长，预示着当前趋势反转。  

```python
integer = CDLDOJISTAR(open, high, low, close)
```

### CDLDRAGONFLYDOJI - Dragonfly Doji
> 函数名：CDLDRAGONFLYDOJI  
名称：Dragonfly Doji 蜻蜓十字/T形十字  
简介：一日K线模式，开盘后价格一路走低，
之后收复，收盘价与开盘价相同，预示趋势反转。  

```python
integer = CDLDRAGONFLYDOJI(open, high, low, close)
```

### CDLENGULFING - Engulfing Pattern
> 函数名：CDLENGULFING  
名称：Engulfing Pattern 吞噬模式  
简介：两日K线模式，分多头吞噬和空头吞噬，以多头吞噬为例，第一日为阴线，
第二日阳线，第一日的开盘价和收盘价在第二日开盘价收盘价之内，但不能完全相同。  

```python
integer = CDLENGULFING(open, high, low, close)
```

### CDLEVENINGDOJISTAR - Evening Doji Star
> 函数名：CDLEVENINGDOJISTAR  
名称：Evening Doji Star 十字暮星  
简介：三日K线模式，基本模式为暮星，第二日收盘价和开盘价相同，预示顶部反转。  

```python
integer = CDLEVENINGDOJISTAR(open, high, low, close, penetration=0)
```

### CDLEVENINGSTAR - Evening Star
> 函数名：CDLEVENINGSTAR  
名称：Evening Star 暮星  
简介：三日K线模式，与晨星相反，上升趋势中,
第一日阳线，第二日价格振幅较小，第三日阴线，预示顶部反转。  

```python
integer = CDLEVENINGSTAR(open, high, low, close, penetration=0)
```

### CDLGAPSIDESIDEWHITE - Up/Down-gap side-by-side white lines
>函数名：CDLGAPSIDESIDEWHITE  
名称：Up/Down-gap side-by-side white lines 向上/下跳空并列阳线  
简介：二日K线模式，上升趋势向上跳空，下跌趋势向下跳空,
第一日与第二日有相同开盘价，实体长度差不多，则趋势持续。  

```python
integer = CDLGAPSIDESIDEWHITE(open, high, low, close)
```

### CDLGRAVESTONEDOJI - Gravestone Doji
> 函数名：CDLGRAVESTONEDOJI  
名称：Gravestone Doji 墓碑十字/倒T十字  
简介：一日K线模式，开盘价与收盘价相同，上影线长，无下影线，预示底部反转。  

```python
integer = CDLGRAVESTONEDOJI(open, high, low, close)
```

### CDLHAMMER - Hammer
> 函数名：CDLHAMMER  
名称：Hammer 锤头  
简介：一日K线模式，实体较短，无上影线，
下影线大于实体长度两倍，处于下跌趋势底部，预示反转。  

```python
integer = CDLHAMMER(open, high, low, close)
```

### CDLHANGINGMAN - Hanging Man
> 函数名：CDLHANGINGMAN  
名称：Hanging Man 上吊线  
简介：一日K线模式，形状与锤子类似，处于上升趋势的顶部，预示着趋势反转。  

```python
integer = CDLHANGINGMAN(open, high, low, close)
```

### CDLHARAMI - Harami Pattern
> 函数名：CDLHARAMI  
名称：Harami Pattern 母子线  
简介：二日K线模式，分多头母子与空头母子，两者相反，以多头母子为例，在下跌趋势中，第一日K线长阴，
第二日开盘价收盘价在第一日价格振幅之内，为阳线，预示趋势反转，股价上升。  

```python
integer = CDLHARAMI(open, high, low, close)
```

### CDLHARAMICROSS - Harami Cross Pattern
> 函数名：CDLHARAMICROSS  
名称：Harami Cross Pattern 十字孕线  
简介：二日K线模式，与母子县类似，若第二日K线是十字线，
便称为十字孕线，预示着趋势反转。  

```python
integer = CDLHARAMICROSS(open, high, low, close)
```

### CDLHIGHWAVE - High-Wave Candle
> 函数名：CDLHIGHWAVE  
名称：High-Wave Candle 风高浪大线  
简介：三日K线模式，具有极长的上/下影线与短的实体，预示着趋势反转。  

```python
integer = CDLHIGHWAVE(open, high, low, close)
```

### CDLHIKKAKE - Hikkake Pattern
> 函数名：CDLHIKKAKE  
名称：Hikkake Pattern 陷阱  
简介：三日K线模式，与母子类似，第二日价格在前一日实体范围内,
第三日收盘价高于前两日，反转失败，趋势继续。  
```python
integer = CDLHIKKAKE(open, high, low, close)
```

### CDLHIKKAKEMOD - Modified Hikkake Pattern
> 函数名：CDLHIKKAKEMOD  
名称：Modified Hikkake Pattern 修正陷阱  
简介：三日K线模式，与陷阱类似，上升趋势中，第三日跳空高开；
下跌趋势中，第三日跳空低开，反转失败，趋势继续。
```python
integer = CDLHIKKAKEMOD(open, high, low, close)
```

### CDLHOMINGPIGEON - Homing Pigeon
> 函数名：CDLHOMINGPIGEON  
名称：Homing Pigeon 家鸽  
简介：二日K线模式，与母子线类似，不同的的是二日K线颜色相同，
第二日最高价、最低价都在第一日实体之内，预示着趋势反转。  

```python
integer = CDLHOMINGPIGEON(open, high, low, close)
```

### CDLIDENTICAL3CROWS - Identical Three Crows
> 函数名：CDLIDENTICAL3CROWS  
名称：Identical Three Crows 三胞胎乌鸦  
简介：三日K线模式，上涨趋势中，三日都为阴线，长度大致相等，
每日开盘价等于前一日收盘价，收盘价接近当日最低价，预示价格下跌。  

```python
integer = CDLIDENTICAL3CROWS(open, high, low, close)
```

### CDLINNECK - In-Neck Pattern
>函数名：CDLINNECK  
名称：In-Neck Pattern 颈内线  
简介：二日K线模式，下跌趋势中，第一日长阴线，
第二日开盘价较低，收盘价略高于第一日收盘价，阳线，实体较短，预示着下跌继续。  

```python
integer = CDLINNECK(open, high, low, close)
```

### CDLINVERTEDHAMMER - Inverted Hammer
> 函数名：CDLINVERTEDHAMMER  
名称：Inverted Hammer 倒锤头  
简介：一日K线模式，上影线较长，长度为实体2倍以上，
无下影线，在下跌趋势底部，预示着趋势反转。  

```python
integer = CDLINVERTEDHAMMER(open, high, low, close)
```

### CDLKICKING - Kicking
> 函数名：CDLKICKING  
名称：Kicking 反冲形态  
简介：二日K线模式，与分离线类似，两日K线为秃线，颜色相反，存在跳空缺口。  

```python
integer = CDLKICKING(open, high, low, close)
```

### CDLKICKINGBYLENGTH - Kicking - bull/bear determined by the longer marubozu
```python
integer = CDLKICKINGBYLENGTH(open, high, low, close)
```

### CDLLADDERBOTTOM - Ladder Bottom
```python
integer = CDLLADDERBOTTOM(open, high, low, close)
```

### CDLLONGLEGGEDDOJI - Long Legged Doji
```python
integer = CDLLONGLEGGEDDOJI(open, high, low, close)
```

### CDLLONGLINE - Long Line Candle
```python
integer = CDLLONGLINE(open, high, low, close)
```

### CDLMARUBOZU - Marubozu
```python
integer = CDLMARUBOZU(open, high, low, close)
```

### CDLMATCHINGLOW - Matching Low
```python
integer = CDLMATCHINGLOW(open, high, low, close)
```

### CDLMATHOLD - Mat Hold
```python
integer = CDLMATHOLD(open, high, low, close, penetration=0)
```

### CDLMORNINGDOJISTAR - Morning Doji Star
```python
integer = CDLMORNINGDOJISTAR(open, high, low, close, penetration=0)
```

### CDLMORNINGSTAR - Morning Star
```python
integer = CDLMORNINGSTAR(open, high, low, close, penetration=0)
```

### CDLONNECK - On-Neck Pattern
```python
integer = CDLONNECK(open, high, low, close)
```

### CDLPIERCING - Piercing Pattern
```python
integer = CDLPIERCING(open, high, low, close)
```

### CDLRICKSHAWMAN - Rickshaw Man
```python
integer = CDLRICKSHAWMAN(open, high, low, close)
```

### CDLRISEFALL3METHODS - Rising/Falling Three Methods
```python
integer = CDLRISEFALL3METHODS(open, high, low, close)
```

### CDLSEPARATINGLINES - Separating Lines
```python
integer = CDLSEPARATINGLINES(open, high, low, close)
```

### CDLSHOOTINGSTAR - Shooting Star
```python
integer = CDLSHOOTINGSTAR(open, high, low, close)
```

### CDLSHORTLINE - Short Line Candle
```python
integer = CDLSHORTLINE(open, high, low, close)
```

### CDLSPINNINGTOP - Spinning Top
```python
integer = CDLSPINNINGTOP(open, high, low, close)
```

### CDLSTALLEDPATTERN - Stalled Pattern
```python
integer = CDLSTALLEDPATTERN(open, high, low, close)
```

### CDLSTICKSANDWICH - Stick Sandwich
```python
integer = CDLSTICKSANDWICH(open, high, low, close)
```

### CDLTAKURI - Takuri (Dragonfly Doji with very long lower shadow)
```python
integer = CDLTAKURI(open, high, low, close)
```

### CDLTASUKIGAP - Tasuki Gap
```python
integer = CDLTASUKIGAP(open, high, low, close)
```

### CDLTHRUSTING - Thrusting Pattern
```python
integer = CDLTHRUSTING(open, high, low, close)
```

### CDLTRISTAR - Tristar Pattern
```python
integer = CDLTRISTAR(open, high, low, close)
```

### CDLUNIQUE3RIVER - Unique 3 River
```python
integer = CDLUNIQUE3RIVER(open, high, low, close)
```

### CDLUPSIDEGAP2CROWS - Upside Gap Two Crows
```python
integer = CDLUPSIDEGAP2CROWS(open, high, low, close)
```

### CDLXSIDEGAP3METHODS - Upside/Downside Gap Three Methods
```python
integer = CDLXSIDEGAP3METHODS(open, high, low, close)
```


[Documentation Index](../doc_index.html)
[FLOAT_RIGHTAll Function Groups](../funcs.html)
