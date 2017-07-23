# Math Operator Functions 
>数学运算符函数
### ADD - Vector Arithmetic Add
> 函数名：ADD   
名称：向量加法运算

```python
real = ADD(high, low)
```

### DIV - Vector Arithmetic Div
> 函数名：DIV   
名称：向量除法运算
```python
real = DIV(high, low)
```

### MAX - Highest value over a specified period
> 函数名：MAX   
名称：周期内最大值（未满足周期返回nan）
```python
real = MAX(close, timeperiod=30)
```

### MAXINDEX - Index of highest value over a specified period
> 函数名：MAXINDEX   
名称：周期内最大值的索引   
```python
integer = MAXINDEX(close, timeperiod=30)
```

### MIN - Lowest value over a specified period
> 函数名：MIN   
名称：周期内最小值 （未满足周期返回nan）
```python
real = MIN(close, timeperiod=30)
```

### MININDEX - Index of lowest value over a specified period
> 函数名：MININDEX   
名称：周期内最小值的索引 
```python
integer = MININDEX(close, timeperiod=30)
```

### MINMAX - Lowest and highest values over a specified period
> 函数名：MINMAX   
名称：周期内最小值和最大值(返回元组````元组（array【最小】，array【最大】）```)
```python
min, max = MINMAX(close, timeperiod=30)
```

### MINMAXINDEX - Indexes of lowest and highest values over a specified period
> 函数名：MINMAX   
名称：周期内最小值和最大值索引(返回元组````元组（array【最小】，array【最大】）```)
```python
minidx, maxidx = MINMAXINDEX(close, timeperiod=30)
```

### MULT - Vector Arithmetic Mult
> 函数名：MULT   
名称：向量乘法运算
```python
real = MULT(high, low)
```

### SUB - Vector Arithmetic Substraction
> 函数名：SUB   
名称：向量减法运算
```python
real = SUB(high, low)
```
### SUM - Summation
> 函数名：SUM   
名称：周期内求和
```python
real = SUM(close, timeperiod=30)
```


[文档](../doc_index.md)
[FLOAT_RIGHTAll Function Groups](../funcs.md)
