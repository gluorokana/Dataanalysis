# 数据可视化
## 使用柱状图来显示男女比例
- sex = text.groupby('Sex')['Survived'].sum()
- sex.plot.bar()
- plt.title('survived_count')
- plt.show()
![image](https://github.com/gluorokana/Pictures/blob/master/Figure_1.png)
## 可视化各性别生存比例
- text.groupby(['Sex','Survived'])
- ['Survived'].count().unstack().plot(kind='bar',stacked='True')
- plt.title('survived_count')
- plt.ylabel('count')
- Text(0, 0.5, 'count')
![image](https://github.com/gluorokana/Pictures/blob/master/Figure_2.png)
## 排序后的折线图
- fig = plt.figure(figsize=(20, 18))
- fare_sur.plot(grid=True)
- plt.legend()
- plt.show()
![image](https://github.com/gluorokana/Pictures/blob/master/Figure_3.png)

## 组直方图
- pclass_sur = text.groupby(['Pclass'])['Survived'].value_counts()
- import seaborn as sns
- sns.countplot(x="Pclass", hue="Survived", data=text)
![image](https://github.com/gluorokana/Pictures/blob/master/Figure_4.png)

## 不同年龄段的分布
- facet = sns.FacetGrid(text, hue="Survived",aspect=3)
- facet.map(sns.kdeplot,'Age',shade= True)
- facet.set(xlim=(0, text['Age'].max()))
- facet.add_legend()
![image](https://github.com/gluorokana/Pictures/blob/master/Figure_5.png)
