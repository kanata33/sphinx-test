常用操作
========================================
1. 文件读取

首先将用到的pandas和numpy加载进来再读取数据
::
	import pandas as pd
	import numpy as np
	df=pd.read_csv('D:\sphinx-test')

2. 查看数据

::
	df.head()

3. 查看数据类型

::
	df.dtypes

4. 查看基本统计量

::
	df.describe(include='all')