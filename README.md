### MulitiLabel medical sentence classification

#### 本代码是针对公众健康问句多标签分类的一个简单开源版本的baseline,仅供参考学习
##### 数据集格式如下：
`QC0000000001,病情描述：病人是典型的“三高”，想吃拜阿司匹林做为预防用药，但是出现过敏症状。曾经治疗情况和效果：以前血压就高，三年前检查出糖尿病。长期服用二甲双胍和降压药。想得到怎样的帮助：病人是典型的“三高”，想吃拜阿司匹林做为预防用药，但是出现过敏症状。请问可以用血塞通分散片替代白阿司匹林做为预防性用药，长期服用吗？另外还有其他药推荐吗？,0,1,0,0,0,0
`
##### 基于BERT模型修改的baseline,可用于解决多标签文本分类问题
预训练模型采用Bert-base,大家可以自己去下载
https://github.com/ymcui/Chinese-BERT-wwm

##### 因为比赛组织方提供的训练集极其分布不均衡，因此没有做太多的数据增强(data augmentation)
|              | max_seq_length   |   epochs    | macro_f1  |
| ------------ | ------------------ | ------------------ | ------------------ |
| BERT+Base | 128     | 15     | 0.4736    |
| BERT+Base     | 300 | 15 | 0.6302 |

#### 代码提供出来仅供学习，此代码参考了kaggle的toxic comment classfication
