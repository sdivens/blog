# NLP实战高手课

## 极客时间课程

* 预测性建模
  * 预测性建模:只关注模型的预测准确性
  * 统计学模型:主要关注模型的可解释性
* 优化问题
  * 增强学习  
    如何在动态环境下做出正确的决定

## 另一种分类

* 结构化数据
* 文本数据
  常见的中文分词器：
    Hanlp 

      1.维特比(viterbi)：效率和效果的最佳平衡。也是最短路分词，HanLP最短路求解采用Viterbi算法
      2.双数组trie树 (dat)：极速词典分词，千万字符每秒（可能无法获取词性，此处取决于你的词典）
      3.条件随机场(crf)：分词、词性标注与命名实体识别精度都较高，适合要求较高的NLP任务
      4.感知机(perceptron)：分词、词性标注与命名实体识别，支持在线学习
      5.N最短路 (nshort)：命名实体识别稍微好一些，牺牲了速度
    Stanford 分词
    ansj 分词器
    哈工大 LTP
    KCWS分词器
    jieba
    IK
    清华大学THULAC
    ICTCLAS
  常见的英文分词工具：
    Keras
    Spacy
    Gensim
    NLTK

* 图像、视频数据
* 语音数据

## How

* 钻
* 快
* 深 夯实基础、数学与编程
* 广 广泛涉猎、抓住本质

## 损失函数


**损失函数**
* 连续数据：
  L2 Loss:  
  $L_2(\widehat{y}, y) = (\widehat{y} - y)^2$  
  L2 Loss:  
  $L_2(\widehat{y}, y) = |\widehat{y} - y|$
* 离散数据  
  $p(y, \theta) = \left\{\begin{aligned} \theta, y = 1 = \theta^y(1-\theta)^{1-y} \\ 1-\theta y=0 \end{aligned}\right.$

**全连接**
* softmax 转换  
  
**激活函数**
  $$sigmoid(x) = \frac{e^x}{1+e^x}$$
  $$ f(x) = tanh(x) $$
  $$ f(x) = Relu(x)$$

**Dropout**

**Batch Normalization**

## 编码
  * one-hot 方式

## Embedding 
  * Embedding 是一个将离散变量转为连续向量表示的一个方式

## RNN
* 马尔科夫过程
  * 
* 隐马尔科夫过程
  * HMM

* RNN (Recurrent Neural Networks)

* LSTM
  * 