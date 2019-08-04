# 离散数学
# 第一章
# 命题逻辑
# 重要术语
- 非：$\huge \neg$
- 合取$\huge \bigwedge$
- 析取$\huge \bigvee$
- 蕴含$\huge \to$
- 等价$\huge \leftrightarrow$
# 等值演算
- 等值式：如果$\huge A\leftrightarrow B$是重言式，则称A与B等值，记作$\huge A\Leftrightarrow B$
- 分配律： $\huge A\bigwedge(B\bigvee C)\Leftrightarrow (A\bigwedge B)\bigvee(A\bigwedge C)$
- 德摩根率：$\huge \neg(A\bigwedge B)\Leftrightarrow \neg A \bigvee \neg B$
- 蕴含等值式：$\huge A\to B \Leftrightarrow \neg A\bigvee B$
- 等价等值式：$\huge A\leftrightarrow B\Leftrightarrow(A\to B)\bigwedge(B\to A)$
- 假言易位：$\huge A\to B\Leftrightarrow \neg B\to \neg A$
- 等价否定等值式：$\huge A\leftrightarrow B\Leftrightarrow \neg A\leftrightarrow \neg B$
# 术语
- 命题常项：用p、q、r等等确定的简单命题，真值是确定不变的
- 命题变项：用p、q、r等等表示真值不确定的简单陈述句
- 变量：上面提到的p、q、r等等就是变量，它们的取值为0或1
- 合式公式：由有限个命题变项或者命题常项组成的公式
- 极小项：设有n个命题变项，若在简单合取式中每个命题变项以文字的形式出现且仅出现一次，则称这样的简单合取式为极小项
- 真值表：设公式A含有n个命题变项，将A在$2^n$种赋值下的情况列成表，称为A的真值表
- 赋值或解释：设A为一个公式，$\huge p_1,p_2,p_3,\cdots,p_n$是出现在A中的全部命题变项，给$\huge p_1,p_2,p_3,\cdots,p_n$各指定一个真值称为对A的一个赋值或者解释。
- 成真赋值：赋值或解释使A真值为1
- 成假赋值：赋值或解释使A真值为0
# 公式的分类
- 设A是一个公式
- 若A无成假赋值，那么称A为重言式或者永真式
- 若A无成真赋值，那么称A为矛盾式或者永假式
- 若A至少有一个成真赋值，那么A称为可满足式
- 若A至少有一个成真赋值，又至少有一个成假赋值，那么A称为非重言式的可满足式
# 公式的层次
- 设A是单个的命题变项，则称A为0层公式
- 称A是n+1层公式是指以下的请情况
1. $\huge A=\neg B$,B为n层公式
2. $\huge A=B\bigwedge C$或者$\huge A=B\bigvee C$或者$\huge A=B\to C$或者$\huge A=B\leftrightarrow C$，其中B、C分别为i，j层公式，其中n=max(i,j)
3. 若A的层次为k，那么称A为k层公式
# 范式
- 文字：命题变项及其否定统称为文字
- 简单析取式：由有限个文字组成的析取式
- 简单合取式：由有限个文字组成的合取式
- 极小项：设有n个命题变项，若在简单合取式中每一个变项以文字的形式出现且仅出现一次，则称这样的简单合取式为极小项。n个命题变项共可产生$2^n$个不同的极小项，分别记为$m_0,m_1,\cdots，m_{2^n-1}$，其中i ($0\leq i\leq 2^n-1$)的二进制表示即为$m_i$的成真赋值
- 极大项：设有n个命题变项，若在简单析取式中每一个变项以文字的形式出现且仅出现一次，则称这样的简单合取式为极大项。n个命题变项共可产生$2^n$个不同的极大项，分别记为$M_0,M_1,\cdots，M_{2^n-1}$，其中i ($0\leq i\leq 2^n-1$)的二进制表示即为$M_i$的成假赋值
- 在极小项和极大项中，文字通常按照下角标或字典顺序排列
- 析取范式：由有限个简单合取式组成的析取式
- 主析取范式：由有限个极小项组成的析取范式
- 合取范式：由有限个简单析取范式组成的合取范式
- 主合取范式：由有限个极大项组成的合取范式
# 主要定理
- 任何一个公式都存在与其等值的析取范式和合取范式
- 任何一个公式都存在唯一与其等值的主析取范式和主合取范式
# 联结词全功能集
- 真值函数：记$\huge \lbrace 0,1 \rbrace ^n= \lbrace 0\cdots00,0\cdots01,\cdots,1\cdots11 \rbrace $，即所有长为n的0、1的符号串的集合，称定义域为$\huge \lbrace 0,1 \rbrace ^n$，值域为$\huge  \lbrace 0,1 \rbrace $的函数为n元真值函数，有$\huge 2^{2^n}$个不同的n元真值函数
- 联结词全功能集：设S为一个联结词集合，若任意真值函数都可以用仅含S中的联结词的公式表示，则称S为联结词的全功能集
    - $\huge  \lbrace \neg,\bigwedge,\bigvee,\to,\leftrightarrow \rbrace , \lbrace \neg,\bigvee,\bigwedge \rbrace , \lbrace \neg,\bigvee \rbrace , \lbrace \neg,\bigwedge \rbrace , \lbrace \uparrow \rbrace , \lbrace \downarrow \rbrace , \lbrace \neg,\to \rbrace $这些都是联结词的全功能集
- 与非式：设p、q为两命题，复合命题“p与q的否定”称为p与q的与非式，记作$\huge p\uparrow q$
    - $\huge p\uparrow q=\neg(p\bigwedge q)$，其中的$\huge \uparrow$称为与非联结词
    - $\huge p\uparrow q$为假当且仅当$\huge p、q$都为真
- 或非式：设$\huge p、q$为两命题复合命题“p或q的否定”称为p或q的或非式，记作$\huge p\downarrow q$
    - $\huge p\downarrow q=\neg(p\bigvee q)$，其中的$\huge \downarrow$称为或非联结词
    - $\huge p\downarrow q$为真当且仅当$\huge p、q$同时为假
# ~~组合电路~~
设计组合电路的一般步骤：
1. 写出问题的输入~输出表，也就是写出问题的真值函数
2. 根据真值函数写出它的主析取范式
3. 将主析取范式化简展开式，可采用奎因·莫克拉斯基方法化简
# 推理理论
- 推理的形式结构
    - 设$\huge A_1,A_2,\cdots,A_k,B$为命题公式称$\huge (A_1\bigwedge A_2\bigwedge\cdots\bigwedge A_k)\to B$为推理的形式结构
    - $\huge A_1,A_2,\cdots,A_k$为推理的前提，$\huge B$为推理的结论，如果$\huge (A_1,A_2,\cdots,A_k)\to B$为重言式，那么称为推理正确,这个时候称B是$\huge A_1,A_2,\cdots,A_k$的逻辑结论或有效结论，记为$\huge (A_1\bigwedge A_2\bigwedge \cdots\bigwedge A_k)\Rightarrow B$
# 推理理论
- 称重言蕴含式为推理定律，主要的推理定理：
    - 附加：$\huge A\Rightarrow (A\bigvee B)$
    - 化简：$\huge (A\bigwedge B)\Rightarrow A$
    - 假言推理：$\huge ((A\to B)\bigwedge A)\Rightarrow B$
    - 拒取式：$\huge ((A\to B)\bigwedge \neg B\Rightarrow \neg A$
    - 析取三段论：$\huge ((A\bigvee B)\bigwedge \neg A)\Rightarrow B$
    - 假言三段论：$\huge ((A\to B)\bigwedge(B\to C))\Rightarrow (A\to C)$
    - 等价三段论：$\huge ((A\leftrightarrow B)\bigwedge(B\leftrightarrow C))\Rightarrow(A\leftrightarrow B)$
    - 构造性二难：$\huge (A\to B)\bigwedge (C\to D)\bigwedge (A\bigvee C)\Rightarrow(B\bigvee D)$
# 判断推理是否正确
- 即判断推理的形式结构是否为重言式，主要方法：
1. 真值表法
2. 等值演算法
3. 主析取、主合取范式法
# 推理规则
1. 前提引入规则
2. 结论引入规则
3. 置换规则
> 接下来的部分上面是前提，下面是结论
4. 假言推理规则：

$\huge A\to B$

$\huge \qquad A$

$\huge \overline{\therefore B\qquad \qquad    }$

5. 附加规则：

$\huge \qquad A$

$\huge \overline{\therefore A\bigvee B}$

6. 化简规则

$\huge A\bigwedge B$

$\huge \overline{\therefore A\qquad}$

7. 拒取式规则：

$\huge A\to B$

$\huge \qquad \neg B$

$\huge \overline{\therefore \qquad\neg A}$

8. 假言三段论规则：

$\huge A\to B$

$\huge B\to C$

$\huge \overline{\therefore A\to C}$

9. 析取三段论规则：

$\huge A\bigvee B$

$\huge \neg A$

$\huge \overline{\therefore B\qquad}$

10. 合取引入规则

$\huge A$

$\huge B$

$\huge \overline {\therefore A\bigwedge B}$

11. 构造性二难规则

$\huge A\to B$

$\huge C\to D$

$\huge A\bigvee C$

$\huge \overline{\therefore B\bigvee D}$

# 其他的一些证明方法
1. 构造证明法
    - 证明是一个描述推理过程的命题公式序列，其中的每个命题公式或者为已知的前提，或者是由前面的公式应用推理规则得到的结论（中间结论） 
2. 附加前提证明法
    - 设推理的结论是蕴含式$\huge A\to B$,把结论中的前件A作为前提，称为附加前提，证明结论中的后件B为有效结论
3. 归谬法
    - 把推理的结论B的否定$\huge \neg B$作为前提，推出矛盾，即证明0为有效结论

## 第一章节小结
- 命题都是陈述句，但是陈述句不都是命题。只有当陈述句所表达的判断结果是唯一的时候（正确或者错误的），它才是命题
- 基本等值式一共有24个

# 第二章
# 一阶逻辑
## 基本概念
- 个体词
    - 在一阶逻辑中，简单命题被分解成主语和谓语两个部分，表示主语的词称为个体词
    - 具体或者特定的词称为个体常项，抽象或者泛指的词称为个体变项，个体变项的取值范围称为个体域。
    - 宇宙中一切事物组成的个体域称为全总个体域
- 谓词
    - 用于刻画个体词的性质或者描述个体词之间的关系
    - 谓词分为个体常项和个体变项
    - 为了讨论个体域中有共同性质的个体的其他性质，首先要引进表示其共同性质的谓词，这叫做特性谓词
- 量词
    - 表示数量的词。表示存在的量词称为存在量词，符号为$\exist$。表示所有的量词称为全称量词,符号为$\forall$
## 一阶逻辑的公式及其解释
- 字母表
    - 个体常项：a,b,c,···,$a_i$
    - 个体变项：x，y，z，···，$x_i$
    - 函数符号：$f,g,h,···,f_i$
    - 谓词符号：F,G,H,···
    - 量词符号：$\exist\qquad \forall$
    - 联结词：上一章讲到的
    - 括号与逗号
- 项
    - 个体常项和个体变项都是项
    - 由有限个项组成的项也是项
- 原子公式
    - 由谓词连接项
- 合式公式
    - 原子公式和由联结词构成的公式是合式公式
- 指导变元，辖域
    - 在公式$\forall xA$和$\exist xA$中，称x为指导变元，称A为相应量词的辖域。当x为指导变元时，A中x的所有出现都称为是约束出现，A中不是约束出现的个体变项称为自由出现。若在$\forall xA$和$\exist xA$中，无自由出现的个体变项，则称它们为闭式。
- 解释
    - 一个解释由4个部分组成
    - 非空个体域D
    - 给涉及的每一个个体常项符号指定一个D中的元素
    - 给涉及的每一个函数，谓词变项符号指定一个D上的函数，谓词
- 赋值
    - 在给定的解释下，对公式中每一个自由出现的个体变项指定个体域中的一个元素
    - 具体实操：在给定的解释I和赋值$\sigma$下，采用指定的个体域D，并将公式A中的所有个体常项符号，函数变项符号及谓词变项符号分别替换成I中指定的元素、函数及谓词，将A中所有自由出现的个体变项符号替换成$\sigma$指定的元素
#公式的分类
- 若A在任何解释和该解释下的任何赋值下均为真，则称A为逻辑有效式或永真式
- 若A在任何解释和该解释下的任何赋值下均为假，则称A为矛盾式
- 若A至少存在一个成真的解释和该解释下的一个赋值，则称A为可满足式
- 代换实例：设$A_0$是含n个命题变项$p_1,p_2,\cdots,p_n$的公式，用一阶逻辑公式$A_i(1\leq i\leq n)$处取代$A_0$中的$p_i$，所得公式A称为$A_0$的代换实例
# 主要定理
- 命题逻辑中的重言式的代换实例都是逻辑有效式，命题逻辑中的矛盾式的代换实例都是罗i就矛盾式
- 一阶逻辑等值式：
    - 等值式：设A、B为一阶逻辑公式，若$A\leftrightarrow B$为逻辑有效式，则称A与B等值，记作$A\Leftrightarrow B$
    - 前束范式：若一阶逻辑公式A具有如下的形式：$Q_1x_1Q_2x_2\cdots Q_kx_kB$，则称A为前束范式，其中$Q_i(1\leq i\leq k)$为$\forall或\exist$，且B中不含量词
- 任何一阶逻辑公式都存在与之等值的前束范式（形式无不唯一）
- 换名规则
    - 将一个指导变项及其在辖域中所有约束出现替换公式中没有出现的个体变项符号
    - 通过使用换名规则得到的公式与原公式等值
- 量词否定等值式：
    - $\neg\forall xA(x)\Leftrightarrow \exist x\neg A(x)$
    - $\neg \exist xA(x)\Leftrightarrow\forall x\neg A(x)$
- 量词辖域收缩与扩张等值式
    - 设公式B中不含x的自由出现
    - $\forall x(A(x)\bigvee B)\Leftrightarrow \forall A(x)\bigvee B$(这个可以使用$\exist$替换)
    - $\forall x(A(x)\bigwedge B)\Leftrightarrow \forall A(x)\bigwedge B$(这个可以使用$\exist$替换)
    - $\forall x(A(x)\to B)\Leftrightarrow \forall xA(x)\to B$
    - $\forall x(B\to A(x))\Leftrightarrow B\to \forall xA(x)$(这个可以使用$\exist$替换)
    - $\exist x(A(x)\to B)\Leftrightarrow \forall xA(x)\to B$
- 量词分配等值式
    - $\forall x(A(x)\bigwedge B(x))\Leftrightarrow \forall xA(x)\bigwedge \forall xB(x)$
    - $\exist x(A(x)\bigvee B(x))\Leftrightarrow \exist xA(x)\bigvee \exist xB(x)$
- 消去量词
    - 设个体域为有穷集合D=$ \lbrace a_1,a_2,\cdots,a_n \rbrace $,则
        - $\forall xA(x)$可以写成$A(a_1)\bigwedge A(a_2)\bigwedge\cdots\bigwedge A(a_n)$
        - $\exist xA(x)$可以写成$A(a_1)\bigvee A(a_2)\bigvee\cdots\bigvee A(a_n)$
# 小结
- 同一个命题在不同个体域内可能有不同的符号化形式，也可能有不同的真值，因而在一个命题符号化之前，必须弄清个体域。若没有指定个体域，应采用全总个体域
- 在一阶逻辑命题符号化的时候，经常使用到如下的两条公式：
    - $\forall x(F(x)\to G(x))$对于任意的x，如果具有性质F(x)，那么一定具有性质G(x)
    - $\exist x(F(x)\bigwedge G(x))$存在个体x，既具有性质F(x),也具有性质G(x)或者存在具有性质F(x)的x，具有性质G(x)
    - 其中F(x)和G(x)为任意两个一元谓词，其中F(x)是特性谓词
- 相似的公式：
    - $\forall x(F(x)\bigwedge G(x))$所有个体，具有性质F(x)也具有性质G(x)
    - $\exist x(F(x)\to G(x))$存在个体x，如果具有性质F(x)，那么具有性质G(x)
- 一阶逻辑公式共分3种类型：逻辑有效式(永真式)，矛盾式和可满足式。公式在人格解释和赋值下都是命题。对于闭式，只需要给定解释
- 记住主要的等值式，包括量词否定等值式、量词辖域收缩与扩张等值式、量词分配等值式、在有限个体域内翘曲量词等值式。使用换名规则，会求给定公式的前束范式
# 第三章
# 集合的基本概念和运算
- 集合与元素
    - 集合与元素是集合论的基本概念，联系元素和集合的是隶属关系，如果元素x术语集合A，则记作$x\in A$，否则记作$x\notin A$
- 集合与集合
    - 集合与集合之间的关系有包含$\subseteq$,相等$=$,不包含$\not=$,真包含$\subset$，不真包含$\not\subset$，具体定义如下：
        - $B\subseteq A\Leftrightarrow \forall x(x\in B\to x\in A)$
        - $B=A\Leftrightarrow B\subseteq A\bigwedge A\subseteq B$
        - $B\not\subseteq A\Leftrightarrow \exist x(x\in B\bigwedge x\not\subseteq A)$
        - $B\not=A\Leftrightarrow A\not\subseteq B\bigvee B\not\subseteq A$
        - $B\subset A\Leftrightarrow B\subseteq A\bigwedge A\not= B$
        - $B\not\subset A\Leftrightarrow B\not\subseteq A\bigvee B=A$
- 空集$\emptyset$,全集E与幂集
    - 不含任何元素的集合叫做空集，记作$\emptyset$，空集是唯一存在的，而且是任意集合的子集
    - 在一个具体问题中，如果涉及的集合都是某个集合的子集，则称这个集合为全集，记作E
    - 设A为集合，A的所有子集构成的集合称为A的幂集，记作P(A),即：
        - P(A)={$x|x\subseteq A$}令|S|表示集合S中的元素个数，那么若|A|=n，则|P(A)|=$2^n$
- 集合的基本运算和算律
    - 集合的基本运算是并$\cup$，交$\cap$,相对补$-$,绝对补~，对称差$\bigoplus$。定义是：
        - $A\bigcup B= \lbrace x|x\in A\bigvee x\in B \rbrace$
        - $A\bigcap B= \lbrace x|x\in A\bigwedge x\in B \rbrace$
        - $A-B= \lbrace x|x\in A\bigwedge x\in B \rbrace$
        - ~$A=E-A= \lbrace x\in E\bigwedge x\not\in A \rbrace = \lbrace x\not\in A \rbrace$
        - $A\bigoplus B=(A-B)\bigcup (B-A)=(A\bigcup B)-(A\bigcap B)$
    - 集合的基本运算遵从的算律：
        - 等幂律：$A\bigcup A=A\qquad A\bigcap A=A$
        - 结合律：$(A\bigcup B)\bigcup C=A\bigcup (B\bigcup C)\qquad (A\bigcap B)\bigcap C=A\bigcap (B\bigcap C)$
        - 交换律：$A\bigcup B=B\bigcup A\qquad A\bigcap B=B\bigcap A$
        - 分配律：$A\bigcup (B\bigcap C)=(A\bigcup B)\bigcap (A\bigcup C)\qquad A\bigcap(B\bigcup C)=(A\bigcup B)\bigcap(A\bigcup C)$
        - 同一律：$A\bigcup =A\qquad A\bigcup  E=A$
        - 零律：$A\bigcup E=E\qquad A\bigcap\emptyset=\emptyset$
        - 排中律：$A\bigcup$~$A=E$
        - 矛盾律：$A\bigcap$~$A=\emptyset$
        - 吸收率：$A\bigcup(A\bigcap B)=A\qquad A\bigcap(A\bigcup B)=A$
        - 德·摩根律：$A-(B\bigcup C)=(A-B)\bigcap(A-C)\qquad A-(B\bigcap C)=(A-B)\bigcup(A-C)$
            - ~$(B\bigcup C)=$~$B\bigcap$~$C$
            - ~$(B\bigcap C)=$~$B\bigcup$~$C$
        - 双重否定率：~(~$A$)=A
    - 有穷集合的记数
        - 解决有穷集合的记数问题有两种方法：文氏图和包含排斥原理
        - 设S为有穷集，$p_1,p_2,\cdots,p_m$是m条性质，S中的任何元素x对于性质$p_i$(i=1,2,···,m)具有或者不具有，两种情况肯定有一种。令$\overline{A_i}$表示S中不具有性质$p_i$的元素构成的集合，那么包含排斥原理可以表述为下面两个公式：
            - $|\overline{A_1}\bigcap\overline{A_2}\bigcap\cdots\bigcap\overline{A_m}=|S|-\sum_{i=1}^m|A_i|+\sum_{1\leq i\leq j\leq m}|A_i\bigcap A_j|-\sum_{1\leq i\leq j\leq m}|A_i\bigcap A_j\bigcap A_k|+\cdots+(-)^m|A_1\bigcap A_2\bigcap\cdots\bigcap A_m|$
            - $|A_1\bigcup A_2\bigcup\cdots\bigcup A_m|=\sum_{i=1}^m|A_i|-\sum_{1\leq i\leq j\leq m}|A_i\bigcap A_j|+\sum_{1\leq i\leq j\leq m}|A_i+A_j+A_k|-\cdots+(-1)^{m+1}|A_1\bigcap A_2\bigcap\cdots\bigcap A_m|$
# 小结
- 好好练题
# 第四章
# 二元关系和函数
- 有序对与笛卡尔积
    - 由两个元素x和y（允许x=y）按照一定的顺序排列成的二元组叫做一个有序对（也称为序偶），记作<x,y>。其中x是它的第一元素，y是它的第二元素，两个有序对<x,y>与<u,v>相等的充分必要条件是x=u且y=v
    - 设A，B为集合，A与B的笛卡尔积记作A$\times$B,其中$A\times B= \lbrace <x,y>|x\in A\wedge y\in B \rbrace $
    - 笛卡尔积运算具有下述性质：
        - $\emptyset \times B=A\times\emptyset=\emptyset$
        - $A\times B\not= B\times A$(A,B不等于空集)
        - $(A\times B)\times C\not=A\times(B\times C)$(A,B不等于空集)
        - $A\times(B\bigcup C)=(A\times B)\bigcup(A\times C)$
        - $(B\bigcup C)\times A=(B\times A)\bigcup(C\times A)$
        - $A\times (B\bigcap C)=(A\times B)\bigcap(A\times C)$
        - $(B\bigcap C)\times A=(B\times A)\bigcap(C\times A)$
    - 关系，从A到B的关系和A上的关系
        - 如果一个集合为空集或者它的元素都是有序对，则称这个集合是一个二元关系，记作R。对于二元关系R，如果<x,y>$\in$R，则记作xRy；如果<x,y>$\notin R$，则记作$x\not{R}Y$
        - 设A,B为集合，$A\times B$的任何子集所定义的二元关系称作从A到B的二元关系，特别当$A=B$时，则叫做A上的二元关系。当A含有n个元素，即|A|=n时，A上有$2^{2^n}$个不同的二元关系，其中最常用的A上的二元关系有以下5种：
            - 恒等关系：$I_A= \lbrace <x,x>|x\in A \rbrace $
            - 全域关系：$E_A=A\times A$
            - 小于等于关系：$L_A= \lbrace <x,y>|x,y\in A\wedge x\leq y \rbrace $,这里的A是实数集R的某个子集
            - 整除关系：$D_A= \lbrace <x,y>|x,y\in A\wedge x|y \rbrace $这里的A是整数集$Z^+$的某个子集，x|y表示x是y的因子，或者说x整除y
            - 包含关系：$R= \lbrace <x,y>|x,y\in P(B)\wedge x\subseteq y \rbrace $,这里A=P(B)
- 关系表示法
    - 表示关系的方法有3种，集合表达式，关系矩阵和关系图，其中关系图只能表示有穷集A上的关系，关系矩阵可以表示有穷集A到B的关系与A上的关系
- 关系的性质
    - 对于集合A上的关系R可以定义5种性质，自反性，反自反性，对称性，反对称性和传递性
        - R在A上自反$\Leftrightarrow \forall x(x\in A \to xRx)$
        - R在A上反自反$\Leftrightarrow \forall x(x\in A\to x\not Rx)$
        - R在A上对称$\Leftrightarrow \forall x \forall y(x,y\in A\wedge xRy\to yRx)$
        - R在A上反对称$\Leftrightarrow\forall x\forall y(x,y\in A\wedge xRy\wedge yRx\to x=y)$
        - R在A上传递$\Leftrightarrow\forall x\forall y\forall z(x,y,z\in A\wedge xRy\wedge yRz\to xRz)$
    - 判别关系性质的方法如下表

    |充要条件|自反|反自反|对称|反对称|传递|
    |---|---|---|---|---|---|
    |集合表示$R$|$I_A\subseteq R$|$I_A\cap R=\emptyset$|$R=R^{-1}$|$R\cap R^{-1}=\emptyset$|$R\circ R\subseteq R$|
    |关系矩阵M|主对角线元素全是1|主对角线元素全是0|对称矩阵|若$r_{ij}=1,且i\not= j,则r_{ji}=0$|$M-M^2中不含负数$|
    |关系图G|每个结点都有环|每个结点都没有环|如果两个结点之间有边，必是一对方向相反的边|如果两个结点之间有边，必是一条单方向的边|若结点$x_i到x_j有边，x_j到x_k有边，那么从x_i到x_k有边$|
- 等价关系和划分
    - 设R为非空集合A上的关系，如果R是自反的，对称的和传递的，则称R为A上的等价关系。对任何$x,y\in A$,如果<x,y>$\in$等价关系R，则记作x~y。对于A的任何元素x，A中与x等价的元素构成了x的等价类，记作$[x]_R=\lbrace y|y\in A\wedge xRy\rbrace$A中与x等价的元素构成了x的等价类，记作$[x]_R$,简记作A/R，即$A/R=\lbrace [x]_R|x\in A\rbrace$
    - 设A是非空集合，如果存在一个A的子集族$\pi(\pi \subseteq P(A))$,满足以下条件：
        1. $\emptyset\not\in \pi$
        2. $\pi$中任意两个元素不交
        3. $\pi$中所有元素的并集等于A
    - 则称$\pi$为A的一个划分，且称$\pi$中元素为划分块
    - 可以证明A关于等价关系R的商集A/R就是A的划分；反之，给定A的划分$\pi$，将$\pi$中划分快作为等价类也可以导出A上的等价关系。A上的等价关系与A的划分是一一对应的。
- 偏序关系和偏序集
    - 设R为非空集合A上的关系，如果R是自反的、反对称的和传递的，则称R为A上的偏序关系，简称偏序，记作$\preccurlyeq$。集合A和A上的偏序关系$\preccurlyeq$一起叫做偏序集，记作$<A,\preccurlyeq>$。其中$\forall x,y\in A$,x与y之间只能保证以下四种情况之一：$x=y,x\prec y,y\prec x,x与y不可比。这里的x\prec y,y\prec x以及x与y不可比的含义是$
        - $x\prec y\Leftrightarrow x\preccurlyeq y\wedge x\not=y$
        - $y\prec x\Leftrightarrow y\preccurlyeq x\wedge y\not=x$
        - x与y不可比$\Leftrightarrow x\not\preccurlyeq y\wedge y\not\preccurlyeq x$
    - 当$x\prec y$且不存在其他的元素z使得$x\prec z\prec y$成立时，称y盖住x。$x\prec y$意味着在序关系上y排在x的后面；而y盖住x则意味着在序关系上y紧跟在x的后边。
    - 有穷集上的偏序可以用哈斯图来表示，在哈斯图中的元素是分层排列的。最底层是所有的极小元。相邻两层之间较高一层的元素至少盖住较低一层的一个元素，每条路径的最高层元素都是极大元。如果偏序集只有唯一的极小元，它就是该偏序集的最小元。类似的，如果偏序集只有唯一的极大元，它就是该偏序集的最大元，给定偏序集$<A,\preccurlyeq>$的子集B，如果存在元素$x\in A$大于等于B中的所有元素，那么x就是b的上界。所有上界中的最小元就是B的最小上界。类似的，可以定义B的最大下界。B的最大下界或者最小上界如果存在那么一定是唯一的。
# 关系运算
- 和关系有关的运算有以下这些：
    - 定义域：domR={$x|\exist y(<x,y>\in R)$}
    - 值域：ranR={$y\exist x(<x,y>\in R)$}
    - 域：$fldR=domR\cup ranR$
    - 逆：$R^{-1}=\lbrace<x,y>|yRx\rbrace$
    - 合成：$F\circ G=\lbrace<x,y>|\exist z(xGz\wedge zFy)\rbrace$
    - 限制：$F\upharpoonright A=\lbrace <x,y>|xFy\wedge x\in A\rbrace$
    - 像：$F[A]=ran(F\upharpoonright A)$
- 一下运算仅适合A上的关系R：
    - 幂：$R^0=I_A$
        - $R^{n+1}=R^n\circ R$n为自然数
    - 自反闭包：$r(R)=R\cup R^0$
    - 对称闭包：$s(R)R\cup R^{-1}$
    - 传递闭包：$t(R)=R\cup R^2···$
# 函数
- 函数也称作映射，他是一种特殊的二元关系。函数的定义是：设F为二元关系，若对于任意的$x\in domF$都存在唯一的$y\in ranF$使得xFy成立，则称F为函数。若$<x,y>\in$函数F，则记作$y=F(x)$,称y是F在x上的函数值。
- 给定集合A,B和函数f，若f满足以下条件：
    - 若dom$f=A$
    - ran$f\subseteq B$
则称f是从A到B的函数，记作$f:A\to B$。所有从A到B的函数的集合$\lbrace f|f:A\to B\rbrace$记作$B^A$。读作“B上A”。如果|A|=m，|B|=n，且m、n不全为0，则$|B^A|=n^m$
- 函数的性质
    某些函数$f:A\to B$具有单射、满射或双射的性质。这些性质分别定义如下：
    - 设$f:A\to B$
        1. 若ran$f=B$,则称$f:A\to B$是满射的
        2. 若对任意的$x,y\in A,x\not= y,都有f(x)\not= f(y),则称f:A\to B是单射的$
        3. 若$f:A\to B$既是满射的，又是单射的，则称$f:A\to B是双射的$
- 函数的复合和反函数
    - 给定函数f和g，f与g的合成也是函数，称作f与g的复合函数，并且满足：
        1. dom$(f\circ g)=\lbrace x|x\in domg\wedge g(x)\in domf\rbrace$;
        2. $f\circ g(x)=f(g(x)),\forall x\in dom(f\circ g)$
    - 特别的，若$f:B\to C,g:A\to B,那么f\circ g:A\to C$
    - 函数的逆不一定构成函数，但对于双射函数$f:A\to B$,它的逆$f^{-1}"B\to A$也是 双射函数称为f的反函数
# 图论
- 多重集合：元素可以重复出现的集合
- 无序积：A&B={(x,y)|x$\in A\wedge y\in B$}
- 定义：无向图G=<V,E>,其中
    1. 顶点集V是非空有穷集合，其元素称为顶点
    2. 边集E为V&V的多重子集，其元素称为无向边，简称边
        - 例如：G=<V,E>,其中$\huge V=\lbrace v_1,v_2,\cdots,v_5\rbrace ,\qquad E=\lbrace (v_1,v_1),(v_1,v_2),(v_2,v_3),(v_2,v_3),(v_2,v_5),(v_1,v_5),(v_4,v_5)$
- 有向图：
    - 定义：有向图D=<V,E>，其中
        1. 顶点集V是非空有穷集合，其元素称为顶点
        2. 边集E为$V\times V$的多重子集，其元素称为有向边，简称边
    - D的基图：