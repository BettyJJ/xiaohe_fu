# 小鹤双拼 + 自然码辅助码方案
本方案的码表给 Rime 自带的明月拼音后面添加了自然码辅助码，自然码辅助码提取自	https://github.com/henices/rime	zrm2000	码表。

本方案优势：
- 因为码表是全拼+辅助码，双拼方案是在 schema.yaml 中定义，并且辅助码可不输入，所以任何双拼方案，只要辅助码相同或不使用辅助码，都可以使用这个码表。如果要使用不同的辅助码则需要修改码表
- Rime 会自动根据单字组词，码表里不存在的词也可以使用辅助码，输入一次之后下次不加辅助码也可以打出来。不需要简单粗暴地放巨大的词库到码表里！简单粗暴法不但占用内存爆炸，而且码表中不存在的词还是无法用辅助码打出来

处理方法参考了 https://tieba.baidu.com/p/6934018888 该楼主提到的“双拼要通过拼写运算间接产生，而不能直接编码”非常有启发。只是该楼主加的是笔画辅助码，所以我只好重新做码表，不然用他的就行了，哈哈

本方案默认是打分号 ; 后输入辅助码，如果希望双拼后直接输入辅助码，把 `xiaohe_fu.schema.yaml` 文件的 89 行 `- derive/^(\w+);(\w+)$/$1$2/` 前面的注释符号删掉即可。
