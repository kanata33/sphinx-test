Series
========================================
Series ������һά�������ֵ�(map)���ݽṹ�Ľ�ϡ�
����һ�����ݺ�һ�����������Ӧ�����ݱ�ǩ������index����ɡ�
values: һ�����ݣ�ndarray���ͣ���
index: ��ص�����������ǩ��
�������ݺ�������ǩ�Ļ�������һ��һάndarray���顣

::

	import pandas as pd
	from pandas import Series
	import numpy as np

	nd = np.array([1, 2, 3])
	print(nd)    # [1 2 3]
	
	#���б��numpy����
	s = Series(nd)
	print(s)

	s.index = list("abc")
	print(s)

	s1 = Series(nd, index=["����", "����", "����"])
	print(s1)

	#���ֵ䴴��
	s2 = Series({"name": "��ѩ", "age": 18, "gender": True, "address": "�����人"})
	print(s2)

	nd = np.array([150, 150, 150, 300])
	s1 = Series(nd, index=["����", "��ѧ", "Ӣ��", "����"])
	print(s1��