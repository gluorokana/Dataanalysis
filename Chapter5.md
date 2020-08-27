## 模型搭建
# 使用预测模型来预测哪些乘客会存活。
- 使用填充函数（fillna）来填充缺失值。
- 对分类变量和连续变量的缺失值进行填充
![image](https://github.com/gluorokana/Pictures/blob/master/fillna.png)
- 对输入模型的特征（如：性别、年龄、票价等）进行编码
![image](https://github.com/gluorokana/Pictures/blob/master/classify.png)
- 从数据集中切割出测试集和训练集
![image](https://github.com/gluorokana/Pictures/blob/master/cut.png)
- 这个问题是一个分类模型，我们可以使用逻辑回归来进行模型的搭建，逻辑回归虽然是一个线性模型，但是由于他的优化函数不同，所以它可以进行分类问题的探索。
![image](https://github.com/gluorokana/Pictures/blob/master/LR.png)
- 同样，我们也可以使用随机森林模型来进行分类
![image](https://github.com/gluorokana/Pictures/blob/master/RF.png)
- 输出不同feature的预测概率
![image](https://github.com/gluorokana/Pictures/blob/master/OP.png)

## 模型评估
# 交叉验证、混淆矩阵以及ROC曲线都可以作为分类评估的重要方法。
- 使用混淆矩阵
![image](https://github.com/gluorokana/Pictures/blob/master/matrix.png)
- 使用ROC曲线
![image](https://github.com/gluorokana/Pictures/blob/master/Figure_ROC.png)
