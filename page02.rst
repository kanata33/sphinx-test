Series
========================================
Series 类似于一维数组与字典(map)数据结构的结合。
它由一组数据和一组与数据相对应的数据标签（索引index）组成。
values: 一组数据（ndarray类型）。
index: 相关的数据索引标签。
这组数据和索引标签的基础都是一个一维ndarray数组。

::

	import pandas as pd
	from pandas import Series
	import numpy as np

	nd = np.array([1, 2, 3])
	print(nd)    # [1 2 3]
	
	#由列表或numpy创建
	s = Series(nd)
	print(s)

	s.index = list("abc")
	print(s)

	s1 = Series(nd, index=["张三", "李四", "王五"])
	print(s1)

	#由字典创建
	s2 = Series({"name": "林雪", "age": 18, "gender": True, "address": "湖北武汉"})
	print(s2)

	nd = np.array([150, 150, 150, 300])
	s1 = Series(nd, index=["语文", "数学", "英语", "理综"])
	print(s1）