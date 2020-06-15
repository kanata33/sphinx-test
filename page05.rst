可视化
========================================
Python中有许多可视化模块，我们通常使用matpalotlib库，再使用pandas模块中集成的R的ggplot主题来美化图表。
::
	import matplotlib.pyplot as plt
	
	pd.options.display.mpl_style = 'default' # Sets the plotting display theme to ggplot2
	
	df.plot(kind = 'box')


