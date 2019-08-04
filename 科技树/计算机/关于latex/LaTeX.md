# 使用La TeX的心路历程
- 指数和下标可以用^和_后加相应字符来实现。比如：
 $a^{2}$ $a^2$ $a_2$  
  ${a^2}^2$
  $a^2_3$

  //在这边我发现使用多个空格和一个空格的效果是一样的。

  //如果在编辑页面使用回车键在浏览界面是不会显示出换行的

 //使用$\qquad$可以在现实中作为一个制表符
  //在使用^和_写出数学公式的上下标的时候是需要写在$$里面的

  //但是在编辑文档里面多敲击几个回车键是能够增加行间距的

  //但是使用两个回车键是可以在显示界面显示出换行的样子的
- 平方根（square root）的输入命令为：\sqrt，n 次方根相应地为: \sqrt[n]。方根符号的大小由LATEX自动加以调整。也可用\surd 仅给出
符号。比如：

 $\sqrt{x}$
 $\surd$
 $\sqrt[3]{x}$
 $\sqrt[3]{x^{2}}+1$
 $\sqrt[3]{x+1}$
 $\Huge\sqrt[6]{x^2_3+y^2}$
 $\surd[a+b]$

//在letax编写出公式的时候可以使用\huge\Huge\tiny\small等等进行字体大小变化

 - 命令\overline 和\underline 在表达式的上、下方画出水平线。比如：
 $\overline{a}$
 $\overline{a^2_4\sqrt[3]{y^2}}$
 $\underline{a}$

 - 命令\overbrace 和\underbrace 在表达式的上、下方给出一水平的大括号。
 $\overbrace{a}$
 $\underbrace{a}$
 $\underbrace{a+b+\cdots+z}_{26}$
 $\cdots$
 - 向量（Vectors）通常用上方有小箭头（arrow symbols）的变量表示。这可由\vec 得到。另两个命令\overrightarrow 和\overleftarrow在定义从A 到B 的向量时非常有用。

 $\vec{1}$
 $\vec{aaaaa}$
 $\overrightarrow{aaa}$
 $\overleftarrow{aaa}$

 - 分数（fraction）使用\frac{...}{...} 排版。一般来说，1/2 这种形式更受欢迎，因为对于少量的分式，它看起来更好些。

 $\frac{1}{22}$ $\qquad$
 $\frac{1}{x^2}$

 - 积分运算符（integral operator）用\int 来生成。求和运算符（sum operator）由\sum 生成。乘积运算符（product operator）由\prod 生成。上限和下限用^ 和_来生成，类似于上标和下标。
 
 $\int_0^{\frac{1}{2}}ada$
 $\qquad$
 $\sum_{i=1}^{n}$
 $\qquad$$\prod_a^b$

  - 常用符号的表示方法
  \\以下是小写希腊字母
  $\alpha$$\qquad$
  $\beta$$\qquad$
  $\theta$$\qquad$
  $\vartheta$$\qquad$
  $\pi$$\qquad$
  $o$ $\qquad$
  $\hat{a}$ $\phi$ $\upsilon$ $\varphi$ $\psi$
  $\omega$
  $\xi$
  $\eta$
  $\tau$
  $\zeta$
  $\varepsilon$
  $\epsilon$
  $\mu$
  $\nu$


//以下是大写希腊字母
$\Gamma$$\qquad$$\Lambda$$\qquad$$\Sigma$$\qquad$$\Psi$$\qquad$$\Delta$$\qquad$$\Xi$$\qquad$$\Upsilon$$\qquad$$\Omega$$\qquad$$\Theta$$\qquad$$\Pi$$\qquad$$\Phi$

- 二元关系符
> 可以在下述命令之前加上\not得到他们的否定形式
$\huge <$
$\huge \not<$ $\qquad$ $\huge >$ $\qquad$ $\huge =$ $\qquad$ $\huge \leq$ $\qquad$ $\huge \le$ $\qquad$ $\huge \geq$ $\qquad$ $\huge \ge$ $\qquad$ $\huge \equiv$ $\qquad$ $\huge \ll$ $\qquad$ $\huge \gg$ $\qquad$ $\huge \doteq$
$\qquad$
$\huge \prec$ $\qquad$ $\huge \sim$ $\qquad$ $\huge \preceq$ $\qquad$
$\huge \succeq$
$\qquad$
$\huge \simeq$
$\qquad$ $\huge \subset$ $\qquad$ $\huge supset$ $\qquad$ $\huge \approx$ $\qquad$ $\huge \subseteq$
$\qquad$ $\huge \cong$ $\qquad$ $\huge \sqsubset$ $\qquad$ $\huge \sqsupset$ $\qquad$ $\huge \Join$ $\qquad$ $\huge \sqsubseteq$ $\qquad$ $\huge \sqsupseteq$ $\qquad$ $\huge \bowtie$ $\qquad$ $\huge \in$ $\qquad$ $\huge \ni \owns$ $\qquad$ $\huge \propto$
$\qquad$ $\huge \vdash$ $\qquad$ $\huge \dashv$ $\qquad$
$\huge \models$ $\qquad$ $\huge \mid$ $\qquad$ $\huge \parallel$ $\qquad$ $\huge \perp$ $\qquad$ $\huge \smile$ $\qquad$ $\huge \frown$ $\qquad$ $\huge \asymp$
$\qquad$ $\huge :$ $\qquad$ $\huge \not \in$ $\qquad$ $\huge \neq \ne$


- 二元运算符

$\huge +$ $\qquad$ $\huge -$ $\qquad$ $\huge \pm$ $\qquad$ $\huge \mp$ $\qquad$ $\huge \triangleleft \qquad\triangleright$ $\qquad$ $\huge \times$ $\qquad$ $\huge \setminus$ $\qquad$ $\huge \star$ $\qquad$ $\huge \cup$ $\qquad$ $\huge \cap$ $\qquad$ $\huge \ast$ $\qquad$ $\huge \sqcup$ $\qquad$ $\huge \sqcap$ $\qquad$ $\huge \circ$ $\qquad$ $\huge \vee\qquad\lor$ $\qquad$ $\huge \wedge\qquad \land$ $\qquad$ $\huge \bullet$ $\qquad$ $\huge \oplus$ $\qquad$ $\huge \ominus$ $\qquad$ $\huge \diamond$ $\qquad$ $\huge \odot$ $\qquad$ $\huge \oslash$ $\qquad$ $\huge \uplus$ $\qquad$ $\huge \otimes$ $\qquad$ $\huge \bigcirc$ $\qquad$ $\huge \bigtriangledown\qquad\bigtriangleup$ $\qquad$ $\huge \dagger$ $\qquad$ $\huge \lhd$ $\qquad$ $\huge \rhd$ $\qquad$ $\huge \ddagger$ $\qquad$ $\huge \unlhd$ $\qquad$ $\huge \wr$ 

- 大尺寸的运算符等待补充
  - $\huge \sum$ $\qquad$ $\huge \bigcup$ $\qquad$ $\huge \bigvee$ $\qquad$ $\huge \bigoplus$ $\qquad$ $\huge \bigotimes$ $\qquad$ $\huge \bigodot$ $\qquad$ $\huge \biguplus$ $\qquad$ $\huge \prod$ $\qquad$ $\huge \bigcap$ $\qquad$ $\huge \bigwedge$ $\qquad$ 
  $\huge \coprod$ $\qquad$ $\huge \bigsqcup$ $\qquad$ $\huge \int$ $\qquad$ $\huge \oint$

- 箭头
  - $\huge \leftarrow\qquad\gets$ $\qquad$ $\huge \rightarrow\qquad\to$ $\qquad$ $\huge\longleftarrow$ $\qquad$ $\huge \uparrow$ $\qquad$ $\huge \downarrow$ $\qquad$ $\huge \longrightarrow$ $\qquad$ $\huge \leftrightarrow$ $\qquad$ $\huge \longleftrightarrow$ $\qquad$ $\huge\Leftarrow$ $\qquad$ $\huge \longleftarrow$ $\qquad$ $\huge \Rightarrow$ $\qquad$ $\huge \Longrightarrow$ $\qquad$ $\huge \updownarrow$ $\qquad$ $\huge\Uparrow$ $\qquad$ $\huge \Downarrow$ $\qquad$ $\huge\Updownarrow$ $\qquad$ $\huge\mapsto$ $\qquad$ $\huge\longmapsto$ $\qquad$ $\huge\nearrow$ $\qquad$ $\huge\searrow$ $\qquad$ $\huge\hookleftarrow$ $\qquad$ $\huge \hookrightarrow$ $\qquad$ $\huge \leftharpoonup$ $\qquad$ $\huge \swarrow$ $\qquad$ $\huge\nwarrow$ $\qquad$ $\huge \leadsto$ $\qquad$ $\huge\rightharpoonup$ $\qquad$ $\huge \rightleftharpoons$ $\qquad$ $\huge\leftrightharpoons$ $\qquad$ $\huge \iff$


- 定界符
  - $\huge ($ $\qquad$ $\huge\)$ $\qquad$ $\huge\uparrow$ $\qquad$ $\huge \Uparrow$ $\qquad$ $\huge [ \lbrace]\rbrace$ $\qquad$ $\huge\downarrow$ $\qquad$ $\huge \Downarrow$ $\qquad$ $\huge \updownarrow$ $\qquad$ $\huge\Updownarrow$ $\qquad$ $\huge \langle$ $\qquad$ $\huge\rangle$ $\qquad$ $\huge | \qquad\vert$ $\qquad$ $\huge\\|\Vert$ $\qquad$ $\huge\lfloor$ $\qquad$ $\huge\rfloor$ $\qquad$ $\huge \lceil$ $\qquad$ $\huge\rceil$ $\qquad$ $\huge /$ $\qquad$ $\huge \backslash$ $\qquad$ $\huge .$

- 大尺寸定界符等待补充
  - $\huge$


//其他符号等待补充
//非数学符号等待补充
//AMS定界符等待补充
//AMS希腊和希伯来字母等待补充
//AMS二元关系符等待补充
//AMS箭头等待补充
//AMS二元否定关系符和箭头等待补充
//数学字母等待补充


需要的链接：
http://www.mohu.org/info/symbols/symbols.htm?tdsourcetag=s_pcqq_aiomsg


https://liam.page/2014/09/08/latex-introduction/




























|a|b|c
|---|---|---|
|1|2|3|
|4|5|6|











$\Huge \in^2_2$

$\tiny a^2$

$\small a_2$