## 在系统命令行中利用type合并我的小md文件

### step1：cd +路径名 导航到对应文件夹，如：
`cd C:\Users\WJL\Desktop\docsify\Docsify-Guide-main - 副本\Algebra\ch1`

### step2：先切换编码保证中文，命令行输入：
`chcp 65001`

### step3：利用type合并我的小md文件，echo类似于打字，type相当于复制。生成一二三章，命令行分别输入：
    (echo # 第一章 群 & type sec1.1.md sec1.2.md sec1.3.md sec1.4.md sec1.5.md sec1.6.md sec1.7.md sec1.8.md) > chapter1.md
    (echo # 第二章 环 & type sec2.1.md sec2.2.md sec2.3.md sec2.4.md sec2.5.md sec2.6.md ) > chapter2.md
    (echo # 第三章 域 & type sec3.1.md sec3.2.md sec3.3.md  ) > chapter3.md
    (echo # 知识库 & type ch1.md ch2.md   ) > chapter3.md


    <!-- 简化版 -->
    (echo # 第一章 群 & type sec1.*.md) > chapter1.md
    (echo # 第二章 环 & type sec2.*.md) > chapter2.md
    (echo # 第三章 域 & type sec3.*.md) > chapter3.md
    (echo # 知识库 & type ch*.md) > summary.md




