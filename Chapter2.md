# Content 2
## 缺失值观察。可以有如下两种方法：
- 方法一： df.info()
![image](https://github.com/gluorokana/Dataanalysis/blob/master/nullcheck.png)
- 方法二：df.isnull().sum()。相比于上一命令，该命令可以直接看到有多少个null值。
![image](https://github.com/gluorokana/Dataanalysis/blob/master/nullcheck1.png)

## 对缺失值进行处理
- 有两种方法可以对缺失值进行处理，即：将na数据行进行删除或者将缺失值进行填充。
- 将含有na的数据行进行删除，命令为： df.dropna()
![image](https://github.com/gluorokana/Dataanalysis/blob/master/dropna.png)
- fillna则是将null的值进行代替。fillna(0)则是将na值替代为0
- 如果需要对指定的列进行填充，那么可以输入： df[df['Age']==None]=0

## 对重复值进行观察及处理
- duplicated可以找到数据中是否有重复行
- df[df.duplicated()]可以显示出所有的重复值
![image](https://github.com/gluorokana/Dataanalysis/blob/master/dureplicate.png)
- 将重复值进行删除，如下：
- df.drop_duplicates().head()
- 将上述处理的数据进行保存
- df.to_csv('test_clear.csv')

## 数据的离散化处理
- 将年龄分成5个年龄段，使用cut函数
- df['AgeBand'] = pd.cut(df['Age'], 5,labels = ['1','2','3','4','5'])
![image](https://github.com/gluorokana/Dataanalysis/blob/master/cut.png)
- 将年龄按指定分段标准进行离散化ch
- df['AgeBand'] = pd.cut(df['Age'],[0,5,15,30,50,80],labels = ['1','2','3','4','5'])
- 按照百分比进行分段的离散化处理
- df['AgeBand'] = pd.qcut(df['Age'],[0,0.1,0.3,0.5,0.7,0.9],labels = ['1','2','3','4','5'])

## 对文本变量进行替换
- 观察各个条目的数据类型
- df['Sex'].value_counts()
- df['Cabin'].value_counts()
- df['Embarked'].value_counts()
![image](https://github.com/gluorokana/Dataanalysis/blob/master/value_counts.png)
- 使用replace函数来进行替换
- df['Sex_num'] = df['Sex'].replace(['male','female'],[1,2])
- 提取每个人的Title
- df['Title'] = df.Name.str.extract('([A-Za-z]+)\.', expand=False)
![image](https://github.com/gluorokana/Dataanalysis/blob/master/Title.png)
