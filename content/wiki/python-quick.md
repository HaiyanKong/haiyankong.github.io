---
title: "Python 速查"
slug: "python-quick"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

---

```python
import os.path as op
import os
import sys
import pandas as pd
import numpy as np

import mne
```

## 获取代码路径

```python
import os
os.getcwd()
```

## 打印出分割线

```python
print('-' * 50)
```

## 绘图后端

### 将 Matplotlib 的后端设置为使用 Qt5Agg 后端

```python
# pip install matplotlib
import matplotlib
matplotlib.use('Qt5Agg')
```

### 将绘图后端设置为默认后端（Agg）

```python
# pip install matplotlib
import matplotlib
matplotlib.use('Agg')
```

### 画图说明：qt 代表画出来，inline 代表画在里面

```python
%matplotlib qt

%matplotlib inline
```

## 清除全局变量

```python
globals().clear()
```

## 查看函数

```python
mne.Epochs?
```

## 数据读取与预览代码

### 获取原始数据

```python
data = raw.get_data()
print(data)
```

### 行列

### 几行几列

```python
data.shape
```

### 前几行

```python
data.head(10)
```

### 最后几列

```python
data.tail(20)
```

### 每一列的内容是什么

```python
data.info
```

### 每一列的数据有什么特征

```python
# 数值类 numerical data 与 类别型数据(categorical data) 均适用

data.describe()

data.agg(np.mean)
data.agg([np.mean, min, max])
```
