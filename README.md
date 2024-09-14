# 上海交通大学2024本科毕业论文LaTeX模板（个人修订版）

该模板参考教务处给出的[2024届本科生毕业设计（论文）](https://www.jwc.sjtu.edu.cn/info/1041/111791.htm "https://www.jwc.sjtu.edu.cn/info/1041/111791.htm")附件中的Latex模板修订而成，请随意使用无需注明出处。
该教务处模板有一些小bug，似乎参考了早期版本的[https://github.com/sjtug/SJTUThesis](https://github.com/sjtug/SJTUThesis)

**如果你是LaTeX老手，建议下载原版教务处模板并自行修订和使用。**

笔者尽可能将模板制作为**新手友好型**，如果你恰好是LaTeX新手，请务必阅读本文档并积极在CSDN、知乎等平台搜索相关信息和使用技巧。

## 文件结构

* 《contents》-文章各个章节、附录等主要内容
* 《figures》-文章插图
* 《scans》-签字扫描页，即任务书及原创性申明
* 《texmf》-配置文件，切勿改动
* main.tex -论文主体，调用并整合各个子文件
* setup.tex -配置部分，用于设置如论文题目等基本信息，以及使用各种package
* refs.bib -文献库

## 使用本模板

### 软件推荐

#### LaTeX编辑器

笔者建议使用专门的LaTeX编辑器而非集成工具如VS Code，实测[TeXstudio](https://www.texstudio.org/ "https://www.texstudio.org/")有更快的编译速度，并且稳定性明显好于VS Code

使用TeXstudio时请在“选项-设置TeXstudio”中，进行配置：

* 构建：默认编译器改为Latexmk、默认文献工具为Biber
* 命令：修改Latexmk项为 ``latexmk -xelatex -silent -synctex=1 %``

或者，也可以在“选项-加载配置文件”中，加载《texmf》文件夹中笔者导出的自用配置文件configuration.txsprofile

#### 参考文献

笔者在refs.bib文献库中保留了尽可能多样的文献类型，以展示各种类型文献中field的填写方式。推荐下载使用[JabRef](https://www.jabref.org/ "https://www.jabref.org/")进行管理并不时备份（并不是文献阅读工具，前期建议使用[Endnote](https://endnote.com/zh/ "https://endnote.com/zh/")或[Zotero](https://www.zotero.org/ "https://www.zotero.org/")进行批量的文献阅读和标注，以上软件均可导出.bib格式的文献库）。本模板采用GB/T 7714相关规范，由于时间久远笔者已经有些遗忘相关debug过程，但方式方法均可在网络上搜索得到。

### 注意事项

1. 如果你不熟悉LaTeX相关操作，可以在附录中找到相关示例以供参考；
2. 有时编译操作并不能一次成功。如果文章格式出现问题（大多为参考文献格式问题）建议尝试多次编译、“工具-清理辅助文件”清理后再次编译；
3. 随着文章越来越长、图片越来越多，编译速度不免越来越慢。这是因为每次编译过程LaTeX都会重新加载整个文档而非有变动的部分。在使用时建议按需注释掉前置部分的任务书和原创性申明以及 `\input{}`的摘要、章节、附录，可以有效提升编译迭代速度；
4. 本模板四级标题采用1.1.1.1而非（1）的格式，如有需要请自行修改（不建议使用四级标题，如果用到建议先调整文章逻辑和展开方式）。

## 写在最后

诚然，不美观不合理的排版（不合理的图文比例、不对齐的排列、大片的留白……）是万万不可的，但笔者坚信无论如何内容始终大于版式。一味地苛求所谓的“标准化”、“一致性”毫无意义，也不必太过纠结。

最后，祝所有祝使用本模板的同学毕业顺利!
