# 离散数学

## 前言

我发现其实前两章当中都有着极为相似的定律形式，背后又藏着代数系统的影子，因此先把第三章提上来，图论就放最后了。

## Charpter 3 Algebraic System

### **Binary Operation :**

Defination:
$$
f:S \times S \rightarrow S
$$
Binary operation is a special kind of function.

Propertities(unary operation also meets the two laws):

$\forall x,y \in S$

1. $f(<x,y>)$ is unique
2. $f(<x,y>) \in S$  (viz closure) 运算的封闭性

(Unary operation is EZ so I ignored it)

运算可能满足的算律：

1. Associative operation		  结合律，比较基础
2. Commutative operation	  交换律
3. Idempotent operation		 幂等律，若一元运算$*$满足$x*x = x$
4. Distributive operation		分配律（对于两个二元运算来说）
5. Absorbtion law					 吸收律（对于两个二元运算来说）
6. Cancellation law 				 消去律

在给定运算的情况下集合可能包含的元素：

1. Identity Element幺元（单位元）

   可能只有左/右幺元，但如果左右都有的话必定是同一个

   若幺元存在则必定唯一

2. Zero Element 零元

   可能只有左/右零元，但如果左右都有的话必定是同一个

   若零元存在则必定唯一

3. Inverse Element逆元

   逆元基于幺元定义。逆元也有左右之分。

   如果左右逆元均存在则必定相等

   逆元唯一

运算表可以找幺元零元逆元

### **Algebraic System**

定义：由一个集合以及k个一元二元运算（首先运算必须封闭）组成。
$$
V = <S,f_1,f_2,\cdots,f_k>
$$
当然代数常数$e, \theta$也可以放进$V$里面

代数系统同类型满足：

1. 运算个数一样
2. $f_ig_i$的操作数目数一样
3. 同样数目的代数常数

### **同态映射**

有两个代数系统$V_1=<A,\circ>$和$V_2=<B,*>$，有一种映射$f:A\rightarrow B$，$\circ$和$*$都是二元运算。如果对$\forall x,y \in A$均有
$$
f(x\circ y) = f(x)*f(y)
$$
则称$f$为$A\rightarrow B$的同态映射。简称$AB$同态

我的理解是:
$$
x,y,\circ,x\circ y都是V_1的\\
f(x),f(y),*,f(x)*f(y)都是V_2的\\
x\rightarrow f(x)\\
y\rightarrow f(y)\\
x\circ y\rightarrow f(x\circ y)\\
\circ \rightarrow f()*f()\\
x\circ y\rightarrow f(x)*f(y)\\
$$
在$A$中做运算得到的东西通过$f$映射到$B$的结果，和先把$x$和$y$分别映射$B$再在$B$中做运算得到的结果是一样的。相当于是两条路到达了同一个结果。

同态的分类：

1. 单同态：$f$为单射
2. 满同态：$f$为满射
3. 同构：$f$为双射

意义：对一个代数系统研究得比较透彻，但是另外一个还尚不明朗，可以通过同态和同构来研究另外一个



### **群论（Group Theory）**

一个代数系统满足***含幺全可逆，二元可结合***，那么这个代数系统是群

$Algebraic System\rightarrow magma(二元)\rightarrow senigroup(二元可结合)\rightarrow monoid(含幺二元可结合)\rightarrow group$

除了只有一个元素的情况（也就是平凡群），一般群不能有零元，零元没有逆元，因此群天然满足消去律

两个比较有意思的四元群：克莱因四元群、$<Z_4,+_4>$

| 阶       | 含义                                                         | 性质         |
| -------- | ------------------------------------------------------------ | ------------ |
| 群的阶   | 基础集合$S$的大小，即基数Cardinlity                          |              |
| 元素的阶 | 对二元运算最少做$R$次幂运算可得到自己，则阶是$R$，若不存在则为无限阶 | 互逆元素同阶 |

一个比较有代表性的例子：$<Z_n,+_n>$，先加最后mod和边加边mod是一样的

补一个运算性质$(a*b)^{-1} = b^{-1}*a^{-1}$

有限群中阶$\geqslant2$的元素成对出现，总个数的偶数个

**子群**

非空子集对同一个二元运算也构成群。表示为$H\preccurlyeq G$，即$H$是$G$的子群

判定$H\preccurlyeq G（H非空）$：

1. 子群判定定理一：

   1. 对$\forall a,b \in H$，有$a*b^{-1}\in H$

2. 子群判定定理二：

   1. 运算对子集合封闭

   2. 满足对任意一个元素，它自己和它关于二元运算的逆元都在子集合中

      这样的话显然必定有幺元$e\in H$

3. 子群判定定理三：

   1. 运算对子集封闭
   2. $H$有限

生成子群：

取$g\in G$则$H=\{g^k|k\in Z\}$为元素$g$的生成子群，记为$<g>$

**陪集（Coset）**

我的理解是它是一种等价关系，是对群$G$的一种划分，两个陪集只可能有两种情况：完全不相交或者完全一样，这个和等价关系里面的等价类一样！或者说等价类和这个一样！

对于$a\in G$，记$aH=\{a*h|h\in H\}$为左陪集（类似可定义右陪集）$*$为了方便可以省略

性质：

1. $He=H$

2. $\forall a\in H,a\in Ha,for\ that\ e\in H$

3. $$
   for \forall a,b\in G,a\in Hb\\\Leftrightarrow \exist h\in H,a=hb\\\Leftrightarrow h=ab^{-1}\in H\\\Leftrightarrow Ha=Hb
   $$

4. only can:$Ha=Hb$,or$Ha\bigcap Hb=\phi$

5. $a$取遍群$G$中所有元素，则$\bigcup Ha=G$

6. 对同一个代表元素$a$，有$|Ha|=|aH|$

通常群不一定可交换，$aH$和$Ha$不一定一样。

如果对$\forall a \in G $均有$aH=Ha$那么称$H$为正规子群。$\{e\}和G$是两个特殊的正规子群，对阿贝尔交换群来说任何子群都是正规子群

**群的Largrange's Theorem :**

$G$是有限群，$H\preccurlyeq G$，那么必定有$|G|=|H|\cdot[G:H]$，或者说$|H|||G|$

**循环群 :**

还记得生成子群吗？若群$G$中存在一个元素$g$，使得$<g>=G$（不仅仅是$<g>=H\preccurlyeq G$），那么称$G$为循环群，$g$为generator

1. 若$|G|=n$，则$G=\{e,g,g^2,\cdots,g^{n-1}\}$
2. 若$G$为无限群，则$G=\{e,g^1,g^{-1},g^2,g^{-2},\cdots,g^k,g^{-k},\cdots\}$

**一个特殊的子群：中心C**
$$
C=\{a|a\in G \bigwedge \forall x\in G,ax=xa\}
$$
群$C$称为$G$的中心。对阿贝尔交换群来说$C=G$，对某些非交换群来说可能$C=\{e\}$。

### **格论(Lattice)  和群是完全不同的两个代数系统，不要往群上靠**

**子群格 ：**

群$G$所有的子群$H_!,H_2,\cdots ,H_n$构成一个集合$S$，定义集合$S$上的偏序关系$H_a\preccurlyeq H_b$为$\forall H_a,H_b\in S,\Leftrightarrow H_a\subseteqq H_b$，则$<S,\preccurlyeq>$构成格，称为群$G$的子群格。

也就是子群上的包含关系构成格。

**格的第一定义：（通过偏序定义）**

已知一个偏序集（poset）$<S,\preccurlyeq>$，如果对$\forall a,b \in S $，$\{a,b\}(不要求可比)$均有最小上界($lcm\ \ \bigvee$)和最大下界($gcd\ \ \bigwedge$)，那么称集合$S$关于偏序$\preccurlyeq$构成格$L$。

$Hasse$图是很有用的东西

$S_n$是n所有正因子构成的集合，$D$为整除关系，那么$<S_n,D>$构成格

**格的第二定义：（通过代数系统定义）**

$<S,\circ,*>$是具有两个二元运算的代数系统，两个二元运算满足交换律、结合律、吸收律（幂等律可以被导出），则可以适当定义$\preccurlyeq$，使得$<S,\preccurlyeq>$构成格$L$

**格的性质：**

1. 对偶原理

   如果命题$f$含有格中的元素以及符号$\preccurlyeq,\succcurlyeq,\bigvee,\bigwedge$，那么将$\preccurlyeq和\succcurlyeq,\bigvee和\bigwedge$相互调换之后得到对偶命题$f^*$。若$f$对一切格中元素均为真，那么$f^*$也对一切格中元素为真

   且有$(f^*)^*=f,(f)^*=f^*$

2. 四大算律（对于二元运算$lcm\ \ gcd$）

   交换律，结合律，幂等律，吸收律

**序与运算关系：**

$L$为格，对$\forall a,b,c,d\in L,a\preccurlyeq b,c\preccurlyeq d$，有
$$
a\bigwedge c\preccurlyeq b\bigwedge d\\
a\bigvee c\preccurlyeq b\bigvee d
$$
$L$为格，对$\forall a,b,c\in L$，有
$$
a\bigvee(b\bigwedge c)\preccurlyeq(a\bigvee b)\bigwedge(a\bigvee c)
$$
由对偶原理可得另外一条。格一般是$\preccurlyeq和\succcurlyeq$而不是$=$，一般不满足分配律

**子格**  类似子群，可以通过哈斯图求

**分配格：**

格$L$上的运算$\bigvee\ \bigwedge$满足分配律

充要条件：格$L$为分配格$\Leftrightarrow$$L$不含与钻石格或者五角格同构的子格

推论：小于5元的的格都是分配格，单链都是分配格

**-----------------------------------To Be Continue----------------------------------**

**有界格：**

全下界0，全上界1

有限格必定有界

有界格的补元：$a,b\in L,a\bigvee b=1,a\bigwedge b=0$，那么$ab$互补

可以没有补，可以有多个补

有界分配格如果存在补元则必唯一

**有补格：**

有界格的情况下每个元素都存在补元，全有补

**布尔代数：**

有补分配格，有界分配格+全有补，补元唯一

求补运算和lcn gcd构成摩根定律

幂集的包含关系可以代表布尔代数