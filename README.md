# rime-aurora-pinyin

 【极光拼音】输入方案

### 依赖

+   简化字八股文（℞ **essay-simp** ）

    >   提供词库

+   笔画輸入方案（℞ **stroke** ）

    >   用于反查不知道读音的字

### 安装

+    東風破

     [東風破](https://github.com/rime/plum) 安裝口令： `bash rime-install hosxy/rime-aurora-pinyin essay-simp`

+   手动安装

    下载本仓库内的`aurora_pinyin.dict.yaml`和`aurora_pinyin.schema.yaml`以及[简化字八股文](https://github.com/rime/rime-essay-simp)仓库内的`essay-zh-hans.txt`到 Rime 用户配置目录中。

### 特点

+ 专为简体中文用户设计

    >   【极光拼音】是一款专门为简体中文用户设计的拼音输入法方案，它与【朙月拼音】不同之处在于，【极光拼音】的码表是简体中文，不须要经过`opencc`转换，从而可以避免一些`opencc`转换带来的问题。

+ 码表

  >   【极光拼音】的码表由两部分组成，一部分是《通用规范汉字表》中的8105个汉字，另一部分是未收录进《通用规范汉字表》但是在网络中常用的字/字符。

+ 常用字和生僻字

  >   【极光拼音】带有两种模式：常用字和生僻字。常用字使用`GBK`字符集，应该能满足大部分用户日常使用，所以这是默认的。如果你发现无法输入某些汉字，请尝试切换到生僻字模式。不过【极光拼音】的生僻字比【朙月拼音】少很多(因为很多都是繁体，而且很复杂)，如果生僻字模式下依然无法输入，请切换到【朙月拼音】。

### 双拼
对于双拼用户，默认后端使用的是【朙月拼音】,如果想切换到【极光拼音】，以小鹤双拼为例，在`double_pinyin_flypy.custom.yaml`中加入以下内容：
```yaml
patch:
  translator/dictionary: aurora_pinyin
```
然后重新部署即可。

### 修订
+ 码表中可能会存在一些错误，比如错音，漏音之类的，如果发现有码表有错误欢迎指正，可以提 issue 或者 PR.
+ 如果你发现有什么较常用字/网络流行字没有收录的，也欢迎提 issue 或者 PR.
