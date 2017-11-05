# DialogueClassifier
通过分析客户和客服对话，对客户的问题进行一些分类。

## 实验方法
1. 基于SVM的分类方法
2. 基于Naive Bayes的分类方法
3. 基于LSTM循环神经网络的分类方法

## 数据集
约7200个对话文本，每个文本包含三级分类标签，其中一级分类有5类，二级分类有80类。

不同实验中，数据集的划分如下表所示：

|实验编号|训练集|验证集|测试集|
|:----:|:----:|:----:|:----:|
|1|80%|0|20%|
|2|80%|0|20%|
|3|60%|20%|20%|

## 实验结果

1.一级分类（5类）准确率（每个模型训练10次取平均值）

||SVM|Bayes|LSTM|
|:----:|:----:|:----:|:----:|
|分类准确率（%）|71.42|63.41|66.16|

2.二级分类（80类）准确率（每个模型训练10次取平均值）

||SVM|Bayes|LSTM|
|:----:|:----:|:----:|:----:|
|分类准确率（%）|60.15|33.63|待测|

注：一级分类和二级分类彼此独立，即进行二级分类时没有引入上一级分类信息。



