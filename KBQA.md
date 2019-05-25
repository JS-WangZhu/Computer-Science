##KBQA

####评价标准：召回率，准确率，F1-Score

方法:自然语言查询-->意图识别(Intention Recognition)-->实体链指(Entity Linking)+关系识别(Relation Detection) -->查询语句拼装(Query Construction)-->返回结果选择(Answering Selection)

KBQA除了 **基于模板的方法** 之外，还有 **基于语义解析** 和 **基于深度学习** 等方法

* 三元组表示 
  “奥巴马出生在火奴鲁鲁。” 可以用三元组表示为 (BarackObama, PlaceOfBirth, Honolulu)
  (实体entity,实体关系relation,实体entity)

###技术基础

####一、词语的向量化表示
* 离散表示 One-Hot模型（维度高造成很大开销，词与词关系隔离）
* 分布式表示 思想：词的语义可以通过上下文信息确认，通过无监督学习，将文本信息映射到定长的向量表示
* Word2Vec两种模型  
  CBOW模型(Continous Bags-of-Words Model) 利用上下文预测目标词语  
  Skip-Gram模型(Contin-uous Skip-Gram Model) 利用当前词语预测上下文  
  CBOW复杂度公式 N*D+D*log(v) 其中N是上下文窗口大小，D是词向量维度，V是词典大小
 
