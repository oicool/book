$\Huge{邪教·程序设计竞赛}$

$\huge{前言}$

本书是邪教·程序设计竞赛系列书的第一本，当然也可能是最后一本，主要面向任何信仰 `#define int long long` 邪教的 OIer。大家阅读本书的目的可能有很多，有为了不被出题人卡的，有为了学到程序设计邪教的，还有知识单纯看看的。由于这些原因，本书就诞生了。

本书以 C++ 知识为主，邪教内容为辅，当然，本书会在每个邪教知识中详细的介绍，请不用担心。

当然，还是不要忘记多刷题，这里推荐一些刷题平台：

- 洛谷(<www.luogu.com.cn>)：始于 2013 年，是中国最有名的 Online Judge；
- Codeforces(codeforces.com)：俄罗斯题库，在全球出名，经常有高质量比赛，Codeforces 的题在洛谷上也都有，但要注意，它的比赛时间很阴间；
- AtCoder(atcoder.jp)：日本题库，比赛比较有思维量。

**致谢**：

首先要感谢阮行止老师的模拟赛，是他的模拟赛成功卡掉了一堆学生的 `long long` 从而诞生了这个邪教。

感谢原著《深入浅出程序设计竞赛》，本书是在此书的基础上编写的。

感谢 [lzexmpoane](https://www.luogu.com.cn/user/318124) 为本书绘制的封面，也感谢 [zhouxiaoze](https://www.luogu.com.cn/user/558099) 绘制的初代封面。

参与本书编写的还有 （待补充）。

感谢团员 [oddy](https://www.luogu.com.cn/user/470348)、[only_matthew](https://www.luogu.com.cn/user/421080)、[初雪_matt](https://www.luogu.com.cn/user/360083)、[MilkAndTea](https://www.luogu.com.cn/user/141870) 等人。

感谢可爱的邪教吉祥物 [Breakingtdasc](https://www.luogu.com.cn/user/483824)，为邪教内容提供建议。

感谢世界上最可爱的阿时 [Time_Complexity](https://www.luogu.com.cn/user/553776)，担任了邪教团队的管理员。

$\huge{目录}$

## 第一部分：邪教语言入门

### 第一章-简单程序

- 邪教程序设计的目标和流程；
- 简单数学计算；
- 变量和常量。

### 第二章-顺序结构

- 变量输入输出；
- 更高效的输入输出。

### 第三章-邪教错误

- 邪教程序中常见的错误及解决方法；
- 提高查错能力。

## 第二部分：邪教语言精通

### 第四章 - 邪教函数

- `inline` 函数。

### 第五章 - 宏定义

- 数组大小定义；
- 让你的代码更简洁；
- 工程化代码。

## 第三部分：C++ 黑科技

### 第六章 - C++ STL

- `valarray`；
- 函数。

### 第七章 - 面向对象编程

***

$\huge{第一部分：邪教语言入门}$

# 第一章 - 简单程序



欢迎来到 `#define int long long` 邪教程序设计竞赛。千里之行始于足下。本书不同于洛谷教材深入浅出程序设计竞赛，此书为邪教专用版，您可以在里面学习到许多代码邪教技巧。

注意，本书不会太详细讲解 C++ 的学习内容，而是学习在 `#define int long long` 邪教中写 C++ 程序的要点。

## 邪教程序设计的目标和流程

促使大家阅读本书的目的有很多，有的人是希望学习到一些邪教代码知识，有的人是希望在今后的题目中不被卡，还有的只是纯粹的兴趣。

### 例题 1-1  

打开你的 IDE 或编辑器（Dev-C++、Visual Studio Code 等），输入下面的程序并编译运行：

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

- `#include<bits/stdc++.h>`，这句话在 C++ 中叫做“引入头文件”，格式通常为 `#include< .. >`，在邪教中我们只使用万能头，即 `#include<bits/stdc++.h>`，该头文件包含了所有的头文件，让你不再因为少写头文件而编译错误。（**oddy 注：如果要使用 `pb_ds`，还要加上 `#include<bits/extc++.h>`，这叫“扩展万能头”**）（**oddy 又注：C++20 引入了模块（module），可以用 `import` 关键字引入，但我们现在用不到就是了**）
- `#define int long long`，这句话是本书的核心。在现阶段的学习中，只需要记住在每个代码的头文件后加上这句话就可以了，使用这句话的注意事项会在更后的学习中提到。
- `using namespace std;`，这句话是 C++ 程序中必加的，现阶段不需要知道是什么意思。
- `signed main(){`，这句话是本书的第二精髓，代替了原有的 `int main(){`。邪教使用的是 `signed main(){`，原因会在后面的学习中提到。
- `puts("I Love #define int long long!");`，这句话是输出双引号里面的字符，你也可以更改里面的内容。注意，`puts("")` 会自动输出换行。
- `//return 0;`，这句话分成两个部分，`//` 的意思是注释，意思就是该处到行尾的内容计算机是不会阅读到，还有一种注释方法是 `/* */`，这种注释可以有多行。另一个部分是 `return 0`，意思是结束这个程序，这句话在程序中可以不加，但因为我们正在学习邪教，所以最好别加。

注意，编写程序时所有的标点符号均为半角而不是全角，不要忘记了行末的分号。

如果想借助计算机解决实际问题，就要设计计算机程序并让计算机执行。在这里举一个非常简单的例子来说明使用计算机解决问题的具体步骤。

## 简单数学计算

### 例题 1-2

`#define int long long` 邪教集团中的 3 个成员，$\texttt{ShanCreeper}$ 拿了 2 个金币，$\texttt{TimeComplexity}$ 拿了 4 个金币，吉祥物 $\texttt{Breakingtdasc}$ 拿了剩下的金币，已知一共有 10 个金币，问：

- $\texttt{ShanCreeper}$ 和 $\texttt{TimeComplexity}$ 一共拿了多少金币；
- $\texttt{Breakingtdasc}$ 拿了多少金币。

现在要编写一个程序输出 2 个答案，换行隔开。

![](https://cdn.luogu.com.cn/upload/image_hosting/9fqidohs.png)

即使是邪教，我们依旧要按照普通设计程序的流程来进行编程，我们可以按照上图方法解决这个问题。

（1）分析问题，理解题意

这是个很简单的小学数学题，这道题的目的非常明确，就是让你求前 2 个人拿到的金币总和和第 3 个人的金币数量。

但并不是所有的题目都是如此直白的。有的问题描述冗长复杂，后面会接触不少需要仔细理解题意得题目。

（2）建立模型，设计算法

接下来需要考虑这个程序“如何做”，也就是设计一个算法。本题的算法很简单，直接输出 $2+4$ 和 $10-2-4$。后面会设计很多较复杂得算法。

（3）编写程序

我们使用 C++ 来实现算法，根据题意可以写出以下程序：

```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
signed main(){
    printf("%lld\n",2+4);
    printf("%lld",10-2-4);
    //return 0;
}
```

我们来看这个程序，其中多了一些新的东西：

- `printf("%lld\n",2+4);`，这句话的意思是输出 $2+4$ 的结果，`%lld` 的意思是计算机会输出一个 `long long` 类型的十进制整数，而 `\n` 的意思是输出一个换行；
- `printf("%lld ",10-2-4);`，这句话的意识是输出 $10-2-4$ 的结果，在 `%lld` 的 的后面有一个空格，意思就是会输出一个空格，当然在本题也可以不加空格。

在原版教材中，使用了 `cout<<2+4<<' '<<10-2-4;` 这种写法，这种写法在邪教中是不支持的。

（4）调试：编译，运行，测试

写完程序后，很可能会存在一些错误，常见的错误如下：

- 编译错误（CE）：可以被编译器发现，出现此错误时，计算机会拒绝运行程序并告诉你错误的地方，常见的比如少了分号，单词拼错了等等；
- 答案错误（WA）：返回了错误的值，这种错误程序不会告诉你错误在哪，需要自己发现错误。

还有其他更高级的错误将在今后谈到（**oddy 注：然而并没有谈**）。

运行该程序，可以看到计算机的输出：
```
6
4
```

和期望的结果一致。

在 C++ 中，还能实现更多的数学计算：

- 减法：`x-y`，返回 x 与 y 的差；
- 乘法：`x*y`，返回 x 与 y 的积，注意在 C++ 程序中不能省略乘号；
- 除法：`x/y`，返回 x 与 y 的商，注意如果无法整除，得到的结果将会是向下取整的整数，但如果希望得到一个小数，可以在一个整数后加上 `.0`；
- 取余：`x%y`，返回 x 除以 y 的余数。

接下来我们将介绍一些数学函数：

### 例题 1-3

计算 $\sqrt{3^2 + 5^2}$。

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

在邪教中，我们尽量不要手写书写函数，而是直接使用这些函数。

除了这些数学函数，还有其他很多的数学函数如下：

|         函数原型         |     样例      |              说明               |
| :----------------------: | :-----------: | :-----------------------------: |
|  `double sin(double x)`  | `sin(3.14/2)` |         三角函数的正弦          |
|  `double exp(double x)`  |   `exp(1)`    | 返回 $e^x$，其中 $e$ 是自然常数 |
|  `double log(double x)`  |   `log(10)`   |       返回 $x$ 的自然对数       |
| `double fabs(double x)`  |  `fabs(-10)`  |        返回 $x$ 的绝对值        |
| `double ceil(double x)`  |  `ceil(2.1)`  |      返回 $x$ 向上取整的值      |
| `double floor(double x)` | `floor(2.9)`  |      返回 $x$ 向下取整的值      |

当然不理解 `double` 也没关系，将在后面的章节提到。

（**oddy 注：OI 程序里应当尽量避免浮点数运算。但是毕竟是邪教，也就算了罢。**）

## 变量和常量

可能你会以为计算机就是一个计算器，但 C++ 能够完成的任务有很多，有些问题需要多个表达式计算才能解决，因此需要有一个方法存储中间结果，可以使用**变量**来满足这个要求。

### 例题 1-4

$\texttt{ShanCreeper}$ 的邪教团里一开始有 100 人，然后经过了以下过程：

- 来了 10 个人；
- 走了 20 个人；
- 群没了。

可以写出以下程序：
```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
int b=100; //初始金额
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

程序定义了一个 `long long` 类型的变量 $b$，注意不是 `int` 的原因在于我们邪教的专用语句 `#define int long long` 让所有程序中的 `int` 全部变为 `long long`，这也就是为什么 `int main()` 要改成 `signed main()`，使用 `long long` 可以防止一些题目的答案超过了 `int` 的范围却很难被做题者发现。

`int b=100` 说明 $b$ 一开始的值是 $100$，`b=b+10`，意思是给 $b$ 加上 10，"=" 的意思并不是两边相等，而是左边的变量得到的新的值是右边的内容，这句也可以写成注释中的 `b+=10`，叫做复合赋值，意思是左边的值加上右边的值。

`b=b-20` 和上面是一样的。

`b=0` 是将 $b$ 的值赋为 $0$。

作为一名邪教成员，因为我们使用了 `#define int long long`，导致有的时候在空间方面会有风险，因此，你需要记住这些变量的占用空间，从而合理估计内存：

|       数据类型       |      占用空间      |         取值范围（均为闭区间）          |
| :------------------: | :----------------: | :-------------------------------------: |
|        `char`        | $1\operatorname B$ |             $-128 \sim 127$             |
|    `unsigned int`    | $4\operatorname B$ |           $0 \sim 2^{32} -1$            |
| `unsigned long long` | $8\operatorname B$ |           $0 \sim 2^{64} -1$            |
|       `float`        | $4\operatorname B$ |  大约指数绝对值不超过 37，6 位有效数字  |
|       `double`       | $8\operatorname B$ | 大约指数绝对值不超过 307，15 位有效数字 |
|     `long long`      | $8\operatorname B$ |        $-2^{63} \sim 2^{63} - 1$        |

（**oddy 注：这只是在 ~~CCF 评测机~~常见架构下的空间和取值，真正的空间和取值都是实现定义的。**）

所以，我们在开头讲的 `#define int long long`，就是将 `int` 的小范围变量改成了 `long long` 的大范围变量，用时间空间换取了比赛不会被卡 `long long` 的代价。

在原书中对 `char` 字符类型进行了详解，但作者很讨厌它，因此并不展开。

# 第二章：顺序结构

到现在为止，我们的程序都没有输入，而大多的题目中都是要求根据输入的数字来解决问题。当然，在邪教中，对输入的要求也有些不同。

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

我们运行该程序，发现没有任何输出，这是因为计算机在等待你的输入，我们输入题目中的 $n$ 和 $x$，比如 3 和 4：

```
3 4
```

按下回车，得到了我们的输出：

```
12
```

我们来分析以下这个程序：

- 第四行 `int n,x` 在上节讲过了，定义两个 `long long` 类型的变量 $n$ 和 $x$，注意是 `long long`，因为我们 `#define int long long`；
- 第六行 `scanf("%lld%lld",&n,&x);`，这句话的意思是输入两个 `long long` 类型的 $n$ 和 $x$，我们在上个章节学的 `printf` 中引号的内容讲过 `%lld` 是输入输出 `long long` 类型变量需要用到的东西，我们能发现，$n$ 和 $x$ 的左边有一个符号 `&`，这个符号现阶段不需要理解是什么意思，在今后的学习中会告诉大家什么时候需要用到它；

原版教材教的 `cin` 在邪教中已经被抛弃。

如果你现在还不知道快速读入和快速输出的方法，那么作为邪教成员必须要熟记占位符，特别是 `%lld`，否则你连程序都运行不了：

|         占位符         |                        说明                        |
| :--------------------: | :------------------------------------------------: |
|  `%nd` ($n$ 是正整数)  | 输出一个整数，如果不足 $n$ 位用空格补齐直到 $n$ 位 |
|         `%lld`         |               用于 `long long` 类型                |
|          `%f`          |  读入 `float` 类型，输出 `float` 或 `double` 类型  |
|         `%lf`          |                 读入 `double` 类型                 |
| `%.nf` ($n$ 是正整数)  |          输出一个固定 $n$ 位小数的浮点数           |
| `%0nd ` ($n$ 是正整数) | 输出一个整数，如果不足 $n$ 位用 0 补齐直到 $n$ 位  |
|          `%c`          |               一个 `char` 类型的字符               |
|          `%s`          |                     一个字符串                     |

原版教材中深入研究了顺序结构程序设计，本书不详解。

## 更高效的读入输出

为什么要抛弃 `cin`、`cout` 而使用 `scanf`、`printf` 呢？下面我们来看一个例子：

### 例题 2-2

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

因为我们不需要学习 `cin`、`cout`，所以只需要知道 `ios::sync_with_stdio(0);` 这句话是给 `cin` 加速的即可。

我们来测试一下这些读入的速度：

|    方法    | 时间（O2） |
| :--------: | :--------: |
|   `cin`    |   440 ms   |
| `cin` 加速 |   120 ms   |
|  `scanf`   |   120 ms   |
|   `read`   |   53 ms    |
|  `fread`   |   37 ms    |

可以看到，在没加速前的 `cin` 慢的离谱，虽然加速后的 `cin` 和 `scanf` 一样快，但因为加速语句冗长难记，所以我们一般不适用 `cin,cout`。

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
- 读入均为正数时，可以删掉有关 `sgn` 的相关语句，速度会更快。

而 `fread` 虽然更快，但是单独实现 `getchar` 的步骤比较麻烦，所以目前使用 `read` 最合适。

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

虽然快速输出并不比 `printf` 快不少，但也是可以用的。

可能有的同学认为这些快速优化是没必要的，但笔者在参加的所有模拟比赛中，使用这些快读、快写写出的程序总比别人的快，少则 $100\operatorname{ms}$，多则 $1\operatorname s$，在你的总用时中能显出优势来。尽管笔者的代码都是 `#define int long long`，但是正是因为快读快写让 `long long` 的劣势——速度慢给覆盖了。

（**oddy 注：由于现在用的都是 64 位机器，`long long` 正好是它的一次基本数据传输大小，所以反而快，不存在慢的这一说。`rxz` 老师替我们测试 `int` 和 `long long` 的速度后，发现速度一样，气愤地拍了桌子。**）

所以身为邪教成员，我们坚决不能使用 `cin`、`cout`，可以使用 `scanf`、`printf`，最好使用 `read`、`write`。

## 邪教错误

### 邪教程序中常见的错误及解决方法

由于我们的邪教代码风格特异，所以还是有必要介绍一下容易出现的错误：

- TLE：在保证你算法正确的情况下 TLE，可能是因为 `long long` 的原因，在这种情况下可以尝试将 `#define int long long` 注释；（**oddy 注：见上一条注解。**）
- MLE：`long long` 占的内存比 `int` 大，可能开不到 `int` 能开的最大数量，可以将大数组换成 `int` 类型；
- Warning：可能是把占位符 `%lld` 写出 `%d` 了，这点要注意。

接下来，我们通过几个查错例题来锻炼自己差错能力。

### 提高差错能力

阅读以下代码，回答问题：

```cpp
#include<bits/stdc++.h>
#define int long long
using namespace std;
signed main(){
    int n,s;
    int sum=0;
    scanf("%d",&n);
    for(int i=1;i<=n;i++){
        int tmp;
        scanf("%d",&tmp);
        sum+=tmp;
    }
    printf("%d",sum);
    return 0;
}
```

（1）这个代码运行后报警了，请问问题在哪？

有警告，说明编译器替我们查出了一些问题。我们可以发现，$n$ 和 $\text{tmp}$ 和 $\text{sum}$ 都是 `long long` 类型的（因为我们 `#define int long long` 了），所以使用 `scanf` 和 `printf` 时占位符要写成 `%lld`。

（2）如果时间要求很严格，我要怎么办？

我们可以尝试使用快读快写增加效率，如果使用快读快写后还是超时，我们只能注释 `#define int long long`，来增加效率。

（3）将 `tmp` 换成数组，如果限制程序可用的 RAM 不能超过 $512\operatorname{MB}$，我最大能开多大？

我们通过计算可得大约能开 $1.5 \times 10^7$。

***

至此，基本上所有的邪教普通语法都介绍完了，更多高阶邪教代码将会在后面的学习中深入体会。

$\huge{邪教语言精通}$

# 第四章-邪教函数

现在你的代码已经有邪教风了，但是在这里，你还能学习到更多邪教代码技巧！

### `inline` 函数

作为邪教成员，知道在哪些函数前加上 `inline` 是很重要的。

在 C++ 中，为了解决一些频繁调用的小函数大量消耗栈空间，我们可以使用 `inline` 表示为内联函数。

比如这个代码：

```cpp
#include<bits/stdc++.h>
#define int long long
using namespaces std;
inline const char *num(int v){
    return (v%2>0)?"%2!=0":"%2=0";
}
signed main(){
    for(int i=0;i<=100;i++){
        printf("%lld",num(i));
    }
    //return 0;
}
```

这个代码是 `inline` 使用的典中典，在内部工作时通过了一系列的操作避免了频繁调用函数对栈内存重复开辟所带来的消耗。

但是 `inline` 的使用是有限的，在一些情况下会消耗内存来换时间，但是我们是邪教风，所以我们在每个函数前加上 `inline`，以空间的代价来换时间。

在普通题目中，内存一般都够用，并且在比赛中排行榜上分数相同时排行的是时间。

注意，`inline` 不要这么用：

```cpp
inline void Find(int x,int y);
some code...
void Find(int x,int y){}
```

应该是这样：

```cpp
void Find(int x,int y);
some code...
inline void Find(int x,int y)
```

换句话说，`inline` 要加在函数的**定义**而非声明前面。

那么，`inline` 的优点有哪些呢：

- 内联函数同宏函数一样将在被调用处进行代码展开，省去了参数压栈、栈帧开辟与回收，结果返回等，从而提高程序运行速度；
- 内联函数相比宏函数来说，在代码展开时，会做安全检查或自动类型转换（同普通函数一样），而宏定义则不会：

```cpp
#define MAX(a,b) ((a)>(b)?(a):(b))
inline int MAX(int a,int b){
    return a>b?a:b;
}

```

使用宏函数时，其书写语法也较为苛刻。如果对宏函数出现如下错误的调用 `MAX(a,"Hello");`，宏函数会错误地比较 `long long` 和字符串，没有参数类型检查，但是使用内联函数的时候，会出现类型不匹配的编译错误。

- 在类中声明同时定义的成员函数，自动转化为内联函数。因此内联函数可以访问类的成员变量，宏定义则不能。
- 内联函数在运行时可调试（**oddy 注：有时也不能**），而宏定义不可以。

虽然我们是邪教成员，但我们还是有必要了解 `inline` 的缺点：

- 在上文我们说了 `inline` 是用空间换时间的做法，内联是以代码膨胀（复制）为代价，消除函数调用带来的开销。如果执行函数体内代码的时间，相比于函数调用的开销较大，那么效率的收获会很少。另一方面，每一处内联函数的调用都要复制代码，将使程序的总代码量增大，消耗更多的内存空间。

当然，在你的函数数量不多的情况下，这点空间可以忽略不计。

# 第五章 - 宏定义

本章主要讲解宏定义，即 `#define` 的多种用法，也是邪教之一的精髓，请务必学习完前面的知识在来阅读本章。

## 数组大小定义

一般大家的数组大小都是这么定义的：

```cpp
int a[10005];
bool vis[10000005];
double k[1];
```

这样不仅输入数字很麻烦，而且可能你还会少写多写一些东西。

这时候，我们就要介绍一个很神奇的东西了——`#define`。

`#define` 用法如下：

```cpp
#define 代替符 原有符
```

比如说我们邪教的精髓 `#define int long long`，其中我们使用 `int` 来代替 `long long`，这样我们就可以节省打 `long long` 的时间并且不用顾虑哪些变量要开 `long long`。

需要注意的是，代替符只能是一个单词，但是原有符可以是多个单词，比如 `#define long long int` 在电脑的眼中就是将 `long` 代替成 `long int`。

`#define` 的替代符和原有符甚至可以是数字，所以我们可以通过宏定义来定义数组的大小：

```cpp
#define MAXN 10005
int a[MAXN],b[MAXN];
bool v[MAXN];
```

这样做的好处是，可以省去打数字的时间；修改方便，将宏定义的数字修改后其他数组的大小会随之修改；也不会因为打太多数字而发生看错等问题。

同样的，我们在写代码中会遇到找最大值最小值的情况，这是我们需要用一个很大的数或很小的数来为答案赋初值，我们便可以使用 `#define` 来定义：

```cpp
#define MAXX=0x3f3f3f3f
#define MINN=-0x3f3f3f3f
...
int big=MINN,sma=MAXX;
for(int i=1;i<=n;i++){
    big=max(big,a[i]);
    sma=min(sma,a[i]);
}
```

***

在定义变量或数组时，还可以更方便：

```cpp
#define IntSZ(name,long) int name[long]
#define IntTwo(name1,name2) int name1,name2
#define IntFive(n1,n2,n3,n4,n5) int n1,n2,n3,n4,n5
#define MAXX 100005
IntSZ(a,MAXX);
signed main(){
    IntFive(a,b,c,d,e);
    IntTwo(j,k);
}
```

在某些情况下这么使用非常方便。

（**oddy 注：这么使用大多数时候很复杂，而且 rxz 老师说过“你就正常写也不会少块肉”，所以最好别这样写。但是毕竟这是邪教集团的教材，那就没有什么关系了。**）

## 让你的代码更简洁

讲完了定义，接下来我们来介绍怎么让你的代码通过 `#define` 更简洁。

**有参宏定义**是比较常见的定义方法，具体使用如下：

```cpp
#define 宏名(形参表) 字符串
```

比如我们用宏定义两数相加：

```cpp
#define Add(a,b) a+b
#define IntTwo(a,b) int a,b
...
IntTwo(a,b);
printf("%lld",Add(a,b));
```

这样，我们就利用宏来实现了加法。

注意，如果你这样使用：

```cpp
#define Add(a,b) a+b
#define IntTwo(a,b) int a,b
...
IntTwo(a,b);
printf("%lld",Add(a,b)*a);
```

我们知道 `#define` 是粗暴替换字符，那么在编译器的眼中他是这样的：

```cpp
printf("%lld",a+b*a);
```

根据运算优先级，它会先计算 `b*a`，然后再做加法，因此我们需要这么做：

```cpp
printf("%lld",(Add(a,b))*a);
```

所以，使用 `#define` 要记得勤加括号！

***

`#define` 不仅可以代替数学计算，还可以代替我们常见的 C++ 关键字，比如 `for`：

```cpp
#define For(i,x,n) for(int i=x;i<=n;i++)
#define Rof(i,x,n) for(int i=x;i>=n;i--)
...
For(i,1,n) a[i]=read():
Rof(i,n,1) writesp(a[i]);
```

在这里，`For(i,1,n)` 就等同于 `for(int i=1;i<=n;i++)`，十分方便。

我们知道邪教输入输出 `scanf` 和 `printf` 打字太麻烦，有些人可能会这么写：

```cpp
#define sc(s,a) scanf("s",&a)
#define pr(s,a) printf("s",a)
```

遗憾的是，不能这么写，你应该要这么写：

```cpp
#define sc(s,a) scanf("#s",&a)
#define pr(s,a) printf("#s",a)
```

我们看到，在字符串部分出现了一个 `#`，假如希望在字符串中包含宏参数，`#` 符号用作一个预处理运算符，它可以把语言符号转化程字符串。

例如，如果 `s` 是一个宏参量，那么 `#x` 可以把参数名转化成相应的字符串。该过程称为字符串化。

类似的，我们可以用宏实现简介 `freopen`：

```cpp
#define FREIN(name) freopen("#name.in","r",stdin)
#define FREOUT(name) freopen("#name.out",“w",stdout)
```

***

在大规模模拟题中，要定义很多名字相似的变量，例如：

```cpp
int a1,a2,a3;
int t1,t2,t3;
int sum1,sum2;
queue<int> q1;
queue<int> q2;
```

我们就可以使用宏来定义：

````cpp
#define SameName(n) x##n
#define For(i,x,n) for(int i=x;i<=n;i++)
...
For(i,1,n) SameName(i)=0x3f;
````

在上面的代码中，`SameName(i)=0x3f` 等同于 `int xi=0x3f`，其中 $i$ 是数字。

`##` 运算符可以用于有参宏的替换部分，还可以用于类对象宏的替换部分。这个运算符把两个语言标识符组合成单个语言标识符。

比如定义一个类：

```cpp
#define Int(LX,long,name1,name2) #LX<long> #name1##name2
...
Int(stack,int,s,1);
Int(queue,int,q,1);
```

***

可能你觉得在上面宏定义 `printf` 的方法还是太麻烦，那这时候我们就要引入一个高科技：

```cpp
#define PR(...) printf(__VA_ARGS__)
...
PR("I Love #define int long long Forever");
PR("%lld are vert NB!",a+b);
```

`__VA_ARGS__` 是一个可变参数的宏，很少人知道这个宏，这个可变参数的宏是新的 C99 规范中新增的，目前似乎只有 gcc 支持。（**oddy 注：此条未加考证，还请仔细甄别**）

实现思想就是宏定义中参数列表的最后一个参数为省略号。这样预定义宏 `__VA_ARGS__` 就可以被用在替换部分中，替换省略号所代表的字符串。

还有其他的高科技宏如下，不做展开：

- `__FILE__`  宏在预编译时会替换成当前的源文件名；

- `__LINE__` 宏在预编译时会替换成当前的行号；

- `__FUNCTION__` 宏在预编译时会替换成当前的函数名称。

***

如果是多行宏定义：

```cpp
#define MACRO(arg1,arg2) do{ /
/* declarations */ /
stmt1; /
stmt2; /
/* ... */ /
}while(0) /* (no trailing ; ) */
```

切记，每行后面要加个 `/`。

***

我们知道在不同的操作系统中有不同的规则，我们就可以这么做：

```cpp
#ifdef WINDOWS
......
(#else)
......
#endif
#ifdef LINUX
......
(#else)
......
#endif
```

这句话的意思是，如果是 `WINDOWS` 系统执行第二行，如果是 `LINUX` 系统执行第七行。

## 工程化代码

此章为整活。

我们可以利用 `#define` 让代码看起来特别高大上：

```cpp
#include<bits/stdc++.h>
#define __int__s int
#define __int__l long long
#define __Scanf__Read(s,a) scanf("#s",a)
#define __Print__Write(s,a) printf("#s",a)
#define _For_Low_High(i,x,n) for(int i=x;i<=n;i++)
#define _FOr_High_Low(i,x,n) for(int i=x;i>=n;i--)
#define __&opta__*(name,num) name[num]
#define __^opta__*(num) num
#define _Using__Np_std&__ using namespace std
#define _Signed@Main signed main
#define LOW_HIGH_SORT sort

__int__l __&opta__*(f,10005);
_Using__Pn_std&__;
_Signed@Main(){
    __int__l __^opta__*(a);
    __int__l __^opta__*(b);
    __Scanf__Read(%lld,__^opta__*(a));
    __Scanf__Read(%lld,__^opta__*(a));
    __int__l __^opta__*(ans);
    _For_Low_High(__^opta__*(i),1,__^opta__*(a)) __^opta__*(ans)++;
    _For_High_Low(__^opta__*(i),__^opta__*(b),1) __^opta__*(ans)--;
    _For_Low_High(__^opta__*(i),1,__^opta__*(ans)){
        __Scanf__Read(%lld,__&opta__*(f,i));
	}
    LOW_HIGH_SORT(__^opta__*(f)+1,__^opta__*+1+__^opta__*(ans));
    _For_Low_High(__^opta__*(i),1,__^opta__*(ans)){
        __Print__Write(%lld,__&opta__*(f,i));
    }
}
```


$\huge{第三部分：C++ 黑科技}$

# 第六章 - C++ STL

本章节将会介绍许多原著内从来没介绍过的黑科技。

## `valarray` 

`valarray` 类是由头文件 `#include<valarray>` 支持的。他和 `stack` 和 `queue` 十分相似，定义方法如下：

```cpp
using namespace std;

valarray<int> va;
valarray<double> va_d;
```

那么 `valarray` 有哪些作用呢：

- `operator[]()`：访问元素；
- `size()`：顾名思义，返回元素个数。

这些都是基本数据结构都有的东西，那么它的特别之处就在于能够得到所有元素的总和、最大值和最小值：

- `sum()`：返回元素总和；
- `max()`：返回最大元素；
- `min()`：返回最小元素。

（**oddy 注：注意！！注意！！这三个方法的时间复杂度在不同的库中不一致，因此，慎用。**）

接下来我们以一道例题来了解 `valarray`。

### 例题 6-1

给定 $n$ 个元素 $a_i$，求出他们的总和、最大值以及最小值。

可以写出以下代码：

```cpp
#include<bits/stdc++.h>
#define int long long
#define fore(i,x,n) for(int i=x;i<=n;i++)
using namespace std;
const int MAXX=100005;
const int mod=1;
inline int read(){ ... }
inline void write(){ ... }
inline void writesp(){ ... }
int a[MAXX];
inline void input(){
    n=read();
    fore(i,0,n-1) a[i]=read();
}
valarray<int> va(a,sizeof(a));
inline void work(){
    int Big=va.max();
    int Sma=va.min();
    int Sum=va.sum();
    writesp(Big);
    writesp(Sma);
    writesp(Sum);
}
signed main(){
    input();
    work();
}
```

小技巧：`valarray<int> va(..)` 可以指定 va 的大小。

## 函数

有一些特别实用的函数将会在这里介绍给大家。

一个大家都不陌生的函数：`next_permutation`，是全排列函数。

***

### `reverse`

使用方法：`reverse(begin,end)`，`begin` 指的是数组起始位置，`end` 指的是数组的终止位置，将 $a_{begin}$ 到 $a_{end}$ 的左闭右开区间所有数字反转过来。

例如：

```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long 
#define fore(i,x,n) for(int i=x;i<=n;i++)
int a[100005],n;
signed main(){
    scanf("%lld",&n);
    fore(i,1,n) scanf("%lld",&a[i]);
    reverse(a+1,a+1+n);
    fore(i,1,n) scanf("%lld",&a[i]);
}
```

便可以将数组 $a$ 的所有元素反转。

***

### `max/min_element`

`max_element`：求一个数组中的最大值

使用方法和 `sort`、`reverse` 相同。


# 面向对象编程

## 注意！

本文章写的所有代码均属于“举例说明”，非正规写法，即将所有东西写在 `public` 中，而正规写法为：所有方法写在 `public` 中，而属性写在 `private` 中，反正被外部随意篡改数据。 

## Part 1 类和对象

比如一个例子：`int a=114514`。

在这句话中，`int` 表示整数**类**，是个**系统自带的类**，而 $a$ 则是这个类的**对象**。由类定义出一个对象的过程叫**实例化**，也说一个对象是它所属的类的一个**实例**。**对象是类实例化的结果，类是对对象的抽象**。

所以，`double`、`char` 这些都是系统自带的**类**。

那么，面向对象编程指的就是创建**自己的类**和**自己的对象**，比如创建类 `student`，对象是同学 A 和 B，好比 `int a,b`。

那么创建自己的类的方法如下：

```cpp
class Student
{
	string Name;
    int Age;
};
```

其中，`Name` 和 `Age` 叫做这个类的**成员变量**，也叫这个类的**属性**。

到这里为止，`class` 和 `struct` 看起来还是一模一样的。

那么类还有个更高科技的东西：

```cpp
class Student
{
public:
	string Name;
private:
	int Age;
};
```

其中，$\text{Name}$ 是公有，类的外部可以读写它的值，而 $\text{Age}$ 私有，类的外部外面看不到。当没有声明一个属性的 `public` 或 `private` 时，默认为 `private`。

但是，可以有只有 `public`，没有 `private` 的类。这种类在 C++ 中相当于结构体，但跟 C 的结构体有区别。

`private` 体现了类的**封装性**。

当一个类被定义后，就可以创建类的对象，形如 `int a` 一样：

```cpp
Student Stu1;
Stu1.Age=20;
```

上方代码创建了一个 `Student` 类的对象 `Stu1`，而 `Stu1.Age=20` 则是给它的属性**赋值**。

***

接下来是**成员函数**，也叫**方法**。

例如下面的代码：

```cpp
class Student
{
public:
	int Age;
    string Name;
    bool Set(int a);
    bool Set(string a);
};
```

`Student` 类中有 2 个方法。并且我们发现，方法的名称可以相同，通过不同的输入参数来识别：


```cpp
Student ShanCreeper

ShanCreeper.Set(10);
ShanCreeper.Set("#define int long long");
```


至此，我们把所有的概念全部讲完，接下来通过一道题来实战一下：

### 例题1 [Score](https://www.luogu.com.cn/problem/U237641)

我们可以用 `class` 来完成这道题。

首先定义类的部分要这么写：

```cpp
class Student
{
public:
    int Id;
    int Ch,Ma,Eg,GN;
    int sum;
    int Output_ID(int ID);
    int Output_Score(int S);
    int Output_GorN(int All,int G);
};
```

- 第 4 行到第 6 行，定义了类的属性：ID、语文数学英语成绩、评分和总成绩；
- 第 7 行到第 9 行，定义了 3 个成员函数：输出 ID、输出分数、输出好或普通。

那么，如何写函数部分呢？

```cpp
inline int Student::Output_ID(int __ID){
    std::cout<<"Student ID: ";
    std::cout<<__ID;
    puts("");
}

inline int Student::Output_Score(int __S){
    std::cout<<"Total score: ";
    std::cout<<__S;
    puts("");
}

inline int Student::Output_GorN(int __ALL,int __G){
    puts((__ALL>280&&__G>5)?"Good":"Normal");
    puts("");
}
```

具体格式为：`type ClassName::FunctionName(...)`。

接下来就可以愉快的写主函数啦：

```cpp
Student Stu;

std::cin>>Stu.Id;
std::cin>>Stu.Ch>>Stu.Ma>>Stu.Eg;
std::cin>>Stu.GN;

Stu.sum=Stu.Ch+Stu.Ma+Stu.Eg;
        
Stu.Output_ID(Stu.Id);
Stu.Output_Score(Stu.sum);
Stu.Output_GorN(Stu.sum,Stu.GN);
```

***

## Part 2 其他函数

- 定义一个 `Student S`，请问 $S$ 有默认值吗？

如果有**构造函数**，那就有默认值。

构造函数是将对象**初始化**的函数。

使用方法如下：

```cpp
class Student
{
public:
	int Age;
    string Name;
    Student();
};

Student::Student(){
	Age=14;
    Name="ShanCreeper";
}

Student S;
```

构造函数定义的特点是冒号两边都是一样的，并且这个构造函数没有参数。

但在绝大部分情况下类的属性值会不同，所以我们要写**带参数的构造函数**：

```cpp
class Student
{
public:
	int Age;
    string Name;
    Student();
    Student(int a,string b);
};

Student::Student(){
	Age=14;
    Name="ShanCreeper";
}

Student::Student(int a,string b){
	Age=a;
    Name=b;
}

Student A;
Student B(14,"ycy");
```

带参数的构造函数可以更方便的动态输入名字年龄。

***

讲了构造函数，我们再来讲讲**析构函数**。

想象一个场景：一个对象 $S$ 被创建后，这个数据的内存就一直在内存中了，如果我们想要释放这个内存，就必须使用构造函数。

使用方法如下：

```cpp
class Student{ ... };
Student *p=new Student(14,"Time_Complexity");

Student::~Student(){
	printf("She is so cute!");
}

delete p;
```

- 定义指针 $p$ 指向临时的对象，当使用 `deltet p` 时调用函数并释放内存。

和构造函数不同的是，析构函数的第二个 Class Name 前有个 `~`。

***

接下来介绍**常方法**。

如果一个函数不修改属性，就是**常方法**，代码如下：

```cpp
class Student
{
public:
	int Age;
    string Name;
    bool Set(int i);
    bool Output() const;
};

inline bool Student::Output() const
{
	printf("%d %d",Age,Name);
    return true;
}

Student S;
S.Output();
```

使用方法：在 `public` 声明时在后面加个 `const` 修饰符，然后在 `class` 外定义的函数后也加个 `const`。

写常方法时，大括号一般换行。

使用 `S.Output()` 就可以调用了。

- 虽然可以不使用 `const`，使用 `const` 是为了安全起见，防止意外修改数据。
- 虽然能直接访问 `S.Age`，但在正规程序中还是会使用 `const`。

***

最后讲一讲**静态成员**：`static`。

举个例子，一个类可以创建多个对象：`int a,b,c,d;`。我们可以定义一个变量 $n$ 来表示程序已经创建了 $n$ 个对象，但是，$n$ 这个数和这个类有关，但又不属于这个类的对象。

这种描述全局，又和某个对象属性无关的，叫做**静态成员数据**，读取静态成员数据的方法叫做**静态成员函数**。

使用方法如下：

```cpp
class Student
{
public:
	int Age;
    string Name;
    Student();
    static int cnt;
    static int count();
};

Student::Student(){
	Age=14;
    Name="ShanCreeper";
    cnt+=1;
}

int Student::count(){
	return cnt;
}
```

在 `public` 中，定义了 1 个静态成员数据和静态成员函数。

注意：`static` 加在前面，而 `const` 加在后面。

在 `Student()` 中，`cnt+=1` 表示定义的对象多了一个，而在 `count()` 中，返回了对象个数。

上面的代码等同于下面的代码：

```cpp
struct student{
	int age;
    string name;
}a[10005];

int cnt;

inline void Student(){
	a.age=14;
    a.name="ShanCreeper";
    cnt+=1;
}

inline int count(){
	return cnt;
}
```

这个 `cnt` 是在这个类之外的关于这个类的变量。

值得一提的是：

```cpp
Student a;
Student b;
a.count();
b.count();
Student::count();
```

我们知道，`cnt` 表示的是 `Student` 创建的对象的个数，所以 `a.count` 和 `b.count` 的返回值是一样的。

而 `Student::count()` 的写法和 `a.count()` 效果完全一样，但只有**不依赖于对象** 的静态函数才能这么写，而且有的时候会莫名其妙编译错误~~所以还是别用了~~。


## Part 3 高级类和对象

我们再来讲讲 `public` 和 `private`。

`private` 的目的是对类的外部隐藏了类内部的工作机制。

通俗的讲，`public` 的内容主函数能看到，但 `private` 的内容只能在类的内部看到。

举个例子：

```cpp
class Student
{
public:
	void Output_Name();
private:
	void Output_Age();
};

void Student::Output_Name(){
	puts("ShanCreeper");
}

void Student::Output_Age(){
	puts("14");
}

Student S;
S.Output_Name();
S.Output_Age();
```

**本程序省略了属性和构造函数。**

根据刚刚讲的，你认为那句话有问题？

没错，是 `S.Output_Age()`，因为 `Output_Age` 是 `private` 里面定义的函数，只能在类的内部看到，而它在外部使用，所以会编译错误。

那既然私有方法外部无法使用，那么有何作用呢？

当然有用，但有条件：需要通过公有方法的外壳调用私有方法：

```cpp
class Student
{
public:
	void Output_public();
private:
	void Output_private();
};

void Student::Output_public(){
	Output_private();
}

void Student::Output_private(){
	printf("I like you.");
}

Student S;
S.Output_public();
S.Output_private();
```

**本程序省略了属性和构造函数。**

其中，`S.Output_public()` 通过套用公有函数外壳调用私有，输出字符，而 `S.Output_private()` 会报错，原因上面已经讲过了。

