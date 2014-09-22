ik-analyzer
===========

基于ik分词器实现的同义词，maven管理

在ik-analyzer的基础上增加同义词filter，可以索引时将同义词索引。
新增的类IKSynonymAnalyzer
同义词库放在data/synonyms.txt

#### data/synonyms.txt 配置方法
##### 通过,分割的可拓展同义词
“采取,采用,采纳”代表着这三个词是同义词，并且任何一个词可以被扩展为其他三个。如果expand设为false的话，则这三个词都会被统一替换为第一个词，也就是“采取”。

##### 通过=>收缩的不可拓展同义词
比如“采用,采纳  => 采取”代表这三个词同义，并且无视expand参数，统一会被替换为“采取”
