# Content 1
## 如何加载数据
- import numpy as np 
- import pandas as pd
- ![image](https://github.com/gluorokana/Dataanalysis/blob/master/Loaddata.png)

## 如何加载表格
- 可以使用相对和绝对路径分别对表格加载，绝对。路径如下：
- df = pd.read_csv('/Users/wang_danni/Desktop/Data_analysis/Project1/titanic/train.csv')
- 查看命令：
- df.head(3)
- ![image](https://github.com/gluorokana/Dataanalysis/blob/master/Dataread.png)
- pd.read_csv()和pd.read_table()的不同：前者每一个字符串作为一列，后者每一行字符串为一列。

## 如何进行逐块读取
- chunker = pd.read_csv('/Users/wang_danni/Desktop/Data_analysis/Project1/titanic/train.csv', chunksize=1000)
- 上述命令可以逐块读取1000个行为。

## 如何将表头改为中文以方便阅读
- df = pd.read_csv('/Users/wang_danni/Desktop/Data_analysis/Project1/titanic/train.csv', names=['乘客ID','是否幸存','仓位等级','姓名','性别','年龄','兄弟姐 妹个数','父母子女个数','船票信息','票价','客舱','登船港口'],index_col='乘客ID',header=0) 
df.head()
- ![image](https://github.com/gluorokana/Dataanalysis/blob/master/Tableread.png)
