# Pandas-matplotlib-seabon
~~~
import pandas as pd
import matplotlib.pyplot as pt
import seaborn as sn

iris=pd.read_csv('iris.csv')
iris

iris.corr(numeric_only=True)
iris.describe()
iris.describe().T

iris.head(10)
iris.info()
~~~
# Scatter plot
pandas
~~~
iris.plot(kind='scatter', x='sepal.length', y='sepal.width')
~~~
seaborn
~~~
sn.scatterplot(x='sepal.length', y='sepal.width', data=iris, hue='variety')
pt.xlabel('SLength')
pt.ylabel('SWidth')
~~~
# Kdeplot
seaborn
~~~
sn.kdeplot(x='sepal.length', data=iris, hue='variety',color='r', fill=True)
~~~
# Box plot
pandas
~~~
iris.plot.box()
~~~
seaborn
~~~
sn.boxplot(x='variety', y='petal.length', data=iris, hue='variety', width=0.3)
~~~
# Histogram
pandas
~~~
pt.hist(iris["petal.length"], bins=40)
~~~
Seaborn
~~~
sn.histplot(data=iris, x='petal.length', bins=50, hue='variety', kde=True)
pt.grid(True)
~~~
# Piarplot
seaborn
~~~
sn.pairplot(data=iris,hue='variety')
~~~
# Bubble plot
seaborn
~~~
sn.scatterplot(data=iris, x='sepal.length', y='sepal.width', s=200, alpha=.6, hue='variety', style='variety', lw=3)
~~~
# Catplot
Seaborn
~~~
sn.catplot( x='petal.length', y='petal.width', hue='variety', data=iris)
~~~
# Parallel plot
seaborn
~~~
from pandas.plotting import parallel_coordinates as pc
pc(iris, 'variety', colormap=pt.get_cmap("Set2"))
~~~
# Heat Map
seaborn
~~~
sn.heatmap(iris.corr(numeric_only=True), annot=True)
~~~
# Andrew Curves
pandas
~~~
pd.plotting.andrews_curves(iris, 'variety')
~~~














