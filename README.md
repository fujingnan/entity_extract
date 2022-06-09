# 基于指针网络的三元组抽取baseline

## 使用方法

+ 下载预训练模型，放到bert目录下，下载训练数据放到data目录下
+ 安装`transformers`,`pip install transformers`
+ 执行train.py文件

## 数据格式
使用自己的训练数据，请至少生成三个文件：train.json、relation.json、vocab.json
+ train.json：存放训练数据，格式为：

`[{"text": text, "spo_list": [[实体1, 关系, 实体2], ...}, ...]`
+ relations.json：存放关系类别，一共有几种关系，就为几个类别，在objectModel阶段需要用到，格式为：

`[{id: relation, ...}]`
+ vocab.json: 常用词词表，由于网络结构最后是对token级别进行预测，所以在最终输出时需要将每个token转回文字，格式为：

`[{id: word, ...}]`

    您也可以根据自己数据的实际情况，更改数据处理代码

预训练模型下载地址

https://huggingface.co/bert-base-chinese/tree/main


训练数据下载地址

链接: https://pan.baidu.com/s/1h-1qgtnfohQDFoV6AZfC7g
密码:7uw4