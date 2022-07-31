$$\Huge{邪教·程序设计竞赛}$$

$$\huge{前言}$$

本书是邪教·程序设计竞赛系列书的第一本，当然也可能是最后一本，主要面向任何信仰 `#define int long long` 邪教的 OIer，大家阅读本书的目的可能有很多，有为了不被出题人卡的、有为了学到程序设计邪教的、还有知识单纯看看的，奔着这些愿望，本书就诞生了。

本书以 C++ 知识为主，邪教内容为辅，当然，本书会在每个邪教知识中详细的介绍，请不用担心。

当然，还是不要忘记多刷题，这里推荐一些刷题平台：

- 洛谷(www.luogu.com.cn)：始于 2013 年，是中国最有名的 Online Judge；
- Codeforces(codeforces.com)：俄罗斯题库，在全球出名，经常有高质量比赛，Codeforces 的题在洛谷上也都有，但要注意，它的比赛时间很阴间；
- AtCoder(atcode.jp)：日本题库，比赛比较有思维量。

**致谢**：

首先要感谢阮行止老师的模拟赛，是他的模拟赛成功卡掉了一堆学生的 `long long` 从而诞生了这个邪教。

感谢原著《深入浅出程序设计竞赛》，本书是在此书的基础上编写的。

感谢 [lzexmpoane](https://www.luogu.com.cn/user/318124) 为本书绘制的封面，也感谢 [zhouxiaoze](https://www.luogu.com.cn/user/558099) 绘制的初代封面。

参与本书编写的还有 （待补充）。

感谢团员 [oddy](https://www.luogu.com.cn/user/470348)、[only_matthew](https://www.luogu.com.cn/user/421080)、[初雪_matt](https://www.luogu.com.cn/user/360083)、[MilkAndTea](https://www.luogu.com.cn/user/141870) 等人。

感谢邪教吉祥物 [Breakingtdasc](https://www.luogu.com.cn/user/483824)，为邪教内容提供建议。

$\huge{第一部分：语言入门}$

# 第一章 - 简单程序



欢迎来到 `#define int long long` 邪教程序设计竞赛，千里之行始于足下，本书不同于洛谷教材深入浅出程序设计竞赛，此书为邪教专用版，您可以在里面学习到许多代码邪教技巧。

![](https://cdn.luogu.com.cn/upload/image_hosting/06xp56hf.png)

​															        图1-1      本章思维导图



## 邪教程序设计的目标和流程

促使大家阅读本书的目的有很多，有的人是希望学习到一些邪教代码知识、有的人是希望在今后的题目中不被卡、还有的只是纯粹的兴趣。

### 例题 1-1  

打开你的 IDE（Dev-C++、VS Code 等），输入下面的程序并编译运行：

```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
signed main(){
    puts("I Love #define int long long!");
    //return 0;
}
```

你能看到在屏幕中的画面是这样的：

```
I Love #define int long long
```

我们来对上面的代码进行深入分析：

- `#include<bits/stdc++.h>`，这句话在 C++ 叫做“头文件”，格式通常为 `#include< .. >`，在邪教中我们只使用万能头，即 `#include<bits/stdc++.h>`，该头文件包含了所有的头文件，让你不再因为少写头文件而编译错误；
- `#define int long long`，这句话是本书的核心，在现阶段的学习中，只需要记住在每个代码的头文件后加上这句话就可以了，使用这句话的注意事项会在更后的学习中提到；
- `using namespace std`，这句话是 C++ 程序中必加的，现阶段不需要知道是什么意思；
- `signed main(){`，这句话也是本书的第二精髓，代替了原有的 `int main(){`，邪教使用的是 `signed main(){`，原因会在后面的学习中提到。
- `puts("I Love #define int long long!");`，这句话是输出双引号里面的字符，你也可以更改里面的内容，注意，`puts("")` 会自动输出换行。
- `//return 0`，这句话分成两个部分，`//` 的意思是注释，意思就是之后的内容计算机是不会阅读到，还有一种注释方法是 `/* */`，这个注释可以多行注释，另一个部分是 `return 0`，意思是结束这个程序，这句话在程序中可以不加，但因为我们正在学习邪教，所以最好别加。

注意，编写程序时所有的标点符号均为半角而不是全角，不要忘记了行末的分号。

如果想借助计算机解决实际问题，就要设计计算机程序并让计算机执行。在这里举一个非常简单的例子来说明使用计算机解决问题的具体步骤。

## 简单数学计算

### 例题 1-2

`#define int long long` 邪教集团中的 3 个成员，$\texttt{ShanCreeper}$ 拿了 2 个金币，$\texttt{TimeComplexity}$ 拿了 4 个金币，吉祥物 $\texttt{Breakingtdasc}$ 拿了剩下的金币，问：

- $\texttt{ShanCreeper}$ 和 $\texttt{TimeComplexity}$ 一共拿了多少金币；
- $\texttt{Breakingtdasc}$ 拿了多少金币。

现在要编写一个程序输出 2 个答案，换行隔开。

![](https://cdn.luogu.com.cn/upload/image_hosting/9fqidohs.png)

我们可以按照上图方法解决这个问题。

（1）分析问题，理解题意

这是个很简单的小学数学题，这道题的目的非常明确，就是让你求前 2 个人拿到的金币总和和第 3 个人的金币数量。

但并不是所有的题目都是如此直白的，有的问题描述冗长复杂，后面会接触不少需要仔细理解题意得题目。

（2）建立模型，设计算法

接下来需要考虑这个程序“如何做”，也就是设计一个算法。本题得算法很简单，直接输出 $2+4$ 和 $10-2-4$，后面会设计很多较复杂得算法。

（3）编写程序

我们使用 C++ 来实现算法，根据题意可以写出以下程序：

```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
signed main(){
    printf("%lld\n",2+4);
    printf("%lld ",10-2-4);
    //return 0;
}
```

我们来讲解这个程序，其中多了一些新的东西：

- `printf("%lld\n",2+4);`，这句话的意思是输出 $2+4$ 的结果，`%lld` 的意思是计算机会输出一个 `lld` 类型，即 `long long` 类型的数字，而 `\n` 的意思是输出一个换行；
- `printf("%lld ",10-2-4);`，这句话的意识是输出 $10-2-4$ 的结果，在 `%lld` 的 的后面有一个空格，意思就是会输出一个空格，当然在本题也可以不加空格。

在原版教材中，使用了 `cout<<2+4<<' '<<10-2-4;` 这种写法，这种写法在邪教中是不支持的。

（4）调试编译运行测试

写完程序后，很可能会存在一些错误，常见的错误如下：

- 编译错误（CE）：可以被编译器发现，出现此错误时，计算机会拒绝运行程序并告诉你错误的地方，常见的比如少了分号，单词拼错了等等；
- 逻辑错误（WA）：返回了错误的值，这种错误程序不会告诉你错误在哪，需要自己发现错误。

还有其他更高级的错误将在今后谈到。

运行该程序，可以看到计算机的输出：
```
6
4
```

和期望的结果一致。

在 C++ 中，还能实现更多的数学计算：

- 减法：`x-y`，返回 x 减去 y 的差；
- 乘法：`x*y`，返回 x 乘上 y 的积，注意，在 C++ 程序中不能省略乘号；
- 除法：`x/y`，返回 x 除以 y 的商，注意，如果无法整除，得到的结果将会是向下取整的整数，但如果希望得到一个小数，可以在一个整数后加上 `.0`；
- 取余：`x%y`，返回 x 除以 y 的余数。

接下来我们将介绍一些数学函数：

### 例题 1-3

计算 $\sqrt{6^2 + 9^2}$。

我们先来看程序：

```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
signed main(){
    printf("%lld",sqrt(pow(6,2)+pow(9,2)));
}
```

这份程序中又多了新的内容：

- `sqrt()`，算出括号数字中的平方根，返回一个浮点数；
- `pow(x,y)`，计算 $x^y$。

除了这些数学函数，还有其他很多的数学函数如下：

|         函数原型         |     样例      |                说明                 |
| :----------------------: | :-----------: | :---------------------------------: |
|  `double sin(double x)`  | `sin(3.14/2)` |           三角函数的正弦            |
|  `double exp(double x)`  |   `exp(1)`    | 返回 $e^x$，其中 $e$ 是自然常数 |
|  `double log(double x)`  |   `log(10)`   |        返回 $x$ 的自然对数        |
| `double fabs(double x)`  |  `fabs(-10)`  |         返回 $x$ 的绝对值         |
| `double ceil(double x)`  |  `ceil(2.1)`  |       返回 $x$ 向上取整的值       |
| `double floor(double x)` | `floor(2.9)`  |       返回 $x$ 向下取整的值       |

当然不理解 `double` 也没关系，将在后面的章节提到。

## 变量和常量

可能你会以为计算机就是一个计算器，但 C++ 能够完成的任务有很多，有些问题需要多个表达式计算才能解决，因此需要有一个方法存储中间结果，可以使用**变量**来满足这个要求。

### 例题 1-4

$\texttt{ShanCreeper}$ 的邪教团里一开始有 $100$ 人，然后经过了以下操作：

- 来了 $10$ 个人；
- 走了 $20$ 个人；
- 群没了。

可以写出以下程序：
```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
int b=100; //初始人数
signed main(){
    b=b+10; //b+=10;
    printf("%lld\n",b);
    b=b-20; //b-=20;
    printf("%lld\n",b);
    b=0;
    printf("%lld\n",b);
    //return 0;
}
```

程序定义了一个 `long long` 类型的 $b$ 变量，注意不是 `int` 的原因在于我们邪教的专用语句 `#define int long long` 让所有程序中的 `int` 全部变为 `long long`，这也就是为什么 `int main()` 要改成 `signed main()`，使用 `long long` 可以防止一些题目的答案超过了 `int` 的范围却很难被做题者发现。

`int b=100` 说明 $b$ 一开始的值是 $100$，`b=b+10`，意思是给 $b$ 加上 10，"=" 的意思并不是两边相等，而是左边的变量得到的新的值是右边的内容，这句也可以写成注释中的 `b+=10`，叫做自赋值，意思是左边的值加上右边的值。

`b=b-20` 和上面是一样的。

`b=0` 是将 $b$ 的值赋为 $0$。

和 `int` 和 `long long` 一样的还有很多类型如下：

|       数据类型       | 占用空间 |                取值范围                 |
| :------------------: | :------: | :-------------------------------------: |
|        `char`        |  1 Byte  |            $-128 \sim 127$            |
|    `unsigned int`    |  4 Byte  |          $0 \sim 2^{32} -1$           |
| `unsigned long long` |  8 Byte  |          $$0 \sim 2^{64} -1$           |
|       `float`        |  4 Byte  |  大约指数绝对值不超过 $37$，$6$ 位有效数字  |
|       `double`       |  8 Byte  | 大约指数绝对值不超过 $307$，$15$ 位有效数字 |
|     `long long`      |  8 Byte  |       $-2^{63} \sim 2^{63} - 1$       |

所以，我们在开头讲的 `#define int long long`，就是将 `int` 的小范围变量改成了 `long long` 的大范围变量，用时间空间换取了比赛不会被卡 `long long` 的代价。

在原书中对 `char` 字符类型进行了详解，但因为作者很讨厌它，因此并不展开。

# 第二章：顺序结构

我们编写计算机程序，将一个任务分解成一条一条的语句，计算机会按照顺序一条一条的执行这些语句，这就是顺序结构程序设计。

到现在为止，我们的程序都没有输入，而大多的题目中都是要求根据输入的数字来解决问题，当然，在邪教中，对输入的要求也有些不同。

## 变量输入输出

### 例题 2-1

$\texttt{ShanCreeper}$ 有 $n$ 个部下，每个部下都想要 $x$ 枚金币，问总共要几枚金币？

我们可以编写如下程序：

```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
int n,x;
signed main(){
    scanf("%lld%lld",&n,&x)；
    int ans=n*x;
    printf("%lld\n",ans);
    //return 0;
}
```

我们运行该程序，发现没有任何输出，这是因为计算机在等待你的输入，我们输入题目中的 $n$ 和 $x$，比如 $3$ 和 $4$：

```
3 4
```

按下回车，得到了我们的输出：

```
12

```

我们来分析以下这个程序：

- 第四行 `int n,x` 在上节课讲过了，定义两个 `long long` 类型的变量 $n$ 和 $x$，注意是 `long long`，因为我们 `#define int long long`；
- 第六行 `scanf("%lld%lld",&n,&x);`，这句话的意思是输入两个 `long long` 类型的 $n$ 和 $x$，我们在上个章节学的 `printf` 中引号的内容讲过 `%lld` 是输入输出 `long long` 类型变量需要用到的东西，我们能发现，$n$ 和 $x$ 的左边有一个符号 `&`，这个符号现阶段不需要理解是什么意思，在今后的学习中会告诉大家什么时候需要用到它；

原版教材教的 `cin` 在邪教中已经被抛弃。



### 例2-2

$\texttt{ShanCreeper}$ 看小写英文字母不順眼，所以要求把字母的小写转换成大写,输入保证是小写字母（洛谷 P5704）

```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long 
int main(){
    char ch;
    scanf("%c", &ch);
    printf("%c", ch-'A'+'a'); 
}
```

​程序第 $6$ 行，ans 是经过计算得到的答案。 ch 是小写字符（实际上存储成对应 ASCII 数字，例如字母 q 对应数字 $113$），由于 ASCII 的小写字母和大写字母都是连续排列的，所以将 ch 的 ASCII 数字减去 `a`（也就是 $65$）就是 $0 \sim 25$ 的整数（也就是第几个字母，从 $0$ 开始计算，`q` 是第 $16$ 个）。最后加上 `A` 的 ASCII 数字（即 $65$）。就可以得到 `Q` 的 ASCII 数字。

​当然也可以理解为 (ch-(’a‘-’A‘) ，也就是 ch-32。根据 ASCII 表可以发现，每个大写字母和小写字母的 ASCII 之间刚好差 $32$。小写字母的 ASCII 比较大，大写字母的 ASCII 比较小，这样也可以完成字母转换。

​输出的时候，虽然 ans 实际上是存储为一个数字.但是毕竟是字符型变量，因此直接使用输出的时候还是会输出 ASCII 码对应的字符。

ASCII 码表如下：

![](https://img2.baidu.com/it/u=728517678,2518913466&fm=253&fmt=auto&app=138&f=PNG?w=843&h=493)



`double`、`char` 等类型的占位符如下，本篇不展开讨论：

|          占位符          |                          说明                          |
| :----------------------: | :----------------------------------------------------: |
|  `%nd` ($n$ 是正整数)  | 输出一个整数，如果不足 $n$ 位用空格补齐直到 $n$ 位 |
|          `%lld`          |                 用于 `long long` 类型                  |
|           `%f`           |    读入 `float` 类型，输出 `float` 或 `double` 类型    |
|          `%lf`           |                   读入 `double` 类型                   |
| `%.nf` ($n$ 是正整数)  |           输出一个固定 $n$ 位小数的浮点数            |
| `%0nd ` ($n$ 是正整数) | 输出一个整数，如果不足 $n$ 位用 0 补齐直到 $n$ 位  |
|           `%c`           |                 一个 `char` 类型的字符                 |
|           `%s`           |                       一个字符串                       |

原版教材中深入拓展了顺序结构程序设计，本书不详解。

## 更高效的读入输出

为什么要抛弃 `cin,cout` 而使用 `scanf,printf` 呢，下面我们来看一个例子：

### 例题 2-3

读入 $2 \times 10^6$ 个 $10^9$ 以内的随机数，我们用不同的方法读入：

```cpp
#include<bits/stdc++.h>
#define int long long
#define fore() for(int i=1;i<=2000000;i++)
using namespace std;
inline int read(){
    int ret=0,sgn=0,ch=getchar();
    while(!isdigit(ch)) sgn|=ch=='-',ch=getchar();
    while(isdigit(ch)) ret=ret*10+ch-'0',ch=getchar();
    return sgn>-ret:ret;
}
const int SIZE=1<<14;
inline char getc(){
    static char buf[SIZE],*begin=buf,*end=buf;
    if(begin==end){
        begin=buf;
        end=buf+fread(buf,1,SIZE,stdin);
    }
    return *in++;
}
inline int Fastread(){
    int ret=0,sgn=0,ch=getc();
    while(!isdigit(ch)) sgn|=ch=='-',ch=getc();
    while(isdigit(ch)) ret=ret*10+ch-'0',ch=getc();
    return sgn>-ret:ret;    
}
int tmp;
signed main(){
    fore() cin>>tmp;
    ios::sync_with_stdio(0);
    fore() cin>>tmp;
    ios::sync_with_stdio(1);
    fore() scanf("%lld",&tmp);
    fore() tmp=read();
    fore() tmp=Fastread():
}
```

因为我们不需要学习 `cin,cout`，所以只需要知道 `ios::sync_with_stdio(0);` 这句话是给 `cin` 加速的即可。

我们来测试一下这些读入的速度：

|    方法    | 时间（O2） |
| :--------: | :--------: |
|   `cin`    |   $440 \text{ ms}$   |
| `cin` 加速 |   $120 \text{ ms}$   |
|  `scanf`   |   $120 \text{ ms}$   |
|   `read`   |   $53 \text{ ms}$    |
|  `fread`   |   $37 \text{ ms}$    |

可以看到，在没加速前的 `cin` 慢的离谱，虽然加速后的 `cin` 和 `scanf` 一样快，但因为加速语句冗长难记，所以我们一般不适用 `cin`、`cout`。

但现在，我们要介绍一个比 `scanf` 还快的读入：快速读入，简称快读。

我们来看代码实现：

```cpp
inline int read(){
    int ret=0,sgn=0,ch=getchar();
    while(!isdigit(ch)) sgn|=ch=='-',ch=getchar();
    while(isdigit(ch)) ret=ret*10+ch-'0',ch=getchar();
    return sgn>-ret:ret;
}
```

这种读入既然叫做快速读入，那么必有过人之处，但使用时有以下几点要注意：

- 在输入到达文件结束时继续读入，`getchar` 会返回 `-1`，导致死循环，如果遇到输入不完整的情况，需要在第一个 `whil` 中判断 `EOF`;
- 读入均为正数时，可以删掉有关 `sgn` 的相关语句，会更快。

而更快速的 `fread` 虽然更快，但是单独实现 `getchar` 的步骤比较麻烦，所以目前使用 `read` 最合适。

那么，有快速读入，必然有快速输出，代码如下：

```cpp
inline void write(int x){
    if(x<0) putchar('-'),x=-x;
    if(x>9) write(x/10);
    putchar(x%10+'0');
}
inline void writesp(int x){
    write(x);
    putchar(' ');
}
inline void writeln(int x){
    write(x);
    putchar('\n');
}
```

上面的三个函数分别是普通快速输出，空格快速输出和换行快速输出。

虽然快速输出并不比 `printf` 快不少，但也时可以用的。

可能有的同学认为这些快速优化是没必要的，但笔者在参加的所有期末模拟考中，使用这些快读快写写出的程序总能比别人的快，少则 $440 \text{ ms}$，多则 $1 \text{ s}$，在你的总用时就能特别显优势，尽管笔者的代码都是 `#define int long long`，但是正是因为快读快写让 `long long` 的劣势——速度慢给覆盖了。

only_matthew 曾经在一场考试中使用快读用暴力拿到了1道题的满分

所以身为邪教成员，我们坚决不能使用 `cin`、`cout`，可以使用 `scanf`、`printf`，最好使用 `read`、`write`。

### 课后练习题（第一章-第二章）

#### 习题1：

读入 $10^6$ 个数字，要求在 $100 \text{ ms}$ 内完成。

#### 习题2：

输出 $1 \sim 10^6$，要求在 $100 \text{ ms}$ 内完成。

（待更新）
