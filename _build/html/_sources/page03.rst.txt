DataFrame
========================================
DataFrame是一个类似表格的数据结构，索引包括列索引和行索引，包含有一组有序的列，每列可以是不同的值类型（数值、字符串、布尔值等）。
如下：

index：行索引。

columns：列索引。

values：值的二维数组。

name：名字。


构建方法，DataFrame(sequence)，通过序列构建，序列中的每个元素是一个字典。

frame=DateFrame构建完之后，假设frame中有’name’,’age’,’addr’三个属性，可以使用fame[‘name’]查看属性列内容，也可以fame.name这样直接查看。

frame按照’属性提取出来的每个列是一个Series类。

DataFrame类可以使用布尔型索引。

groupby(str|array…)函数：可以使用frame中对应属性的str或者和frame行数相同的array作为参数还可以使用一个会返回和frame长度相同list的函数作为参数，如果使用函数做分组参数，这个用做分组的函数传入的参数将会是fame的index，参数个数任意。使用了groupby函数之后配合,size()函数就可以对groupby结果进行统计。

groupby后可以使用：

size()：就是count

sum()：分组求和

apply(func，axis=0)：在分组上单独使用函数func返回frame，不groupby用在DataFrame会默认将func用在每个列上，如果axis=1表示将func用在行上。


reindex(index,column,method)：用来重新命名索引，和插值。

size()：会返回一个frame，这个frame是groupby后的结果。

sum(n).argsort()：如果frame中的值是数字，可以使用sum函数计算frame中摸个属性，各个因子分别求和，并返回一个Series，这个Series可以做为frame.take的参数，拿到frame中对应的行。

pivot_table(操作str1,index=str2,columns=str3,aggfunc=str4)透视图函数：

str1：是给函数str4作为参数的部分。

str2：是返回frame的行名。

str3：是返回frame的列名。

str4：是集合函数名，有’mean’,’sum’这些，按照str2，str3分组。

使用透视图函数之后，可以使用.sum()这类型函数，使用后会按照index和columns的分组求和。

order_index(by,ascending):
返回一个根据by排序，asceding=True表示升序，False表示降序的frame

concat(list)：将一个列表的frame行数加起来。

ix[index]：就是行索引，DataFrame的普通下标是列索引。

take(index)：作用和ix差不多，都是查询行，但是ix传入行号，take传入行索引。

unstack()：将行信息变成列信息。

apply(func，axis=0)和applymap(func)：apply用在DataFrame会默认将func用在每个列上，如果axis=1表示将func用在行上。applymap表示func用在每个元素上。

combine_first(frame2)：combine_first会把frame中的空值用frame1中对应位置的数据进行填充。Series方法也有相同的方法。

stack()函数，可以将DataFrame的列转化成行，原来的列索引成为行的层次索引。（stack和unstack方法是两个互逆的方法，可以用来进行Series和DataFrame之间的转换）

duplicated()：返回一个布尔型Series，表示各行是否重复。
drop_duplicates()：返回一个移除了重复行后的DataFrame.
pct_change()：Series也有这个函数，这个函数用来计算同colnums两个相邻的数字之间的变化率。

corr()：计算相关系数矩阵。

cov()：计算协方差系数矩阵。

corrwith(Series|list,axis=0)：axis=0时计算frame的每列和参数的相关系数。
