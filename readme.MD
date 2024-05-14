1、QAnchor：当通过某个query搜索出一批视频，并且点击了某个视频A，就把query称为这个视频A的QAnchor。<br> 
2、tf-idf：tf = （term 在该文档中出现的次数）/（该文档的总 term 数），df = （出现该 term 的 document 数量）/（总 document 数量），idf = log（总 document 数量 / 出现该 term 的 document 数量 + 1）
3、bm25：也可以理解为 tf-idf，但是 tf-idf 没有考虑文本长度，同样两篇文本，term = elephant 的 tf 和 idf 都一样，但是第二篇文本的长度是一万字，第一篇文本的长度是一万字，通过该算法无法体现差异。bm25 引入文档长度和平均文档长度作为分母，参数 b 控制文档长度分子的影响，参数 k1 限制了f(qi,D)过高时（大于 k1）分数太大，可以将 fieldLen = avgFieldLen 再化简绘图。https://www.elastic.co/cn/blog/practical-bm25-part-2-the-bm25-algorithm-and-its-variables<br>
