### 测试

RainAir 数学大师竞赛题解

### 题目描述

求所有整数对 $(m,n)$ 使得
$$
\begin{cases}2m &\equiv -1 \pmod n\\n^2 &\equiv -2 \pmod m\end{cases}
$$

### 题解

由题意，只需要求所有的四元组 $(m,n,a,b)$：
$$
\begin{cases}an &= 2m+1\\bm&=n^2+2\end{cases}
$$
注意到显然 $2 \nmid a, 2 \nmid n$，因此 $2 \nmid n^2 + 2$，即 $2 \nmid b$。注意到：
$$
a^2 bm=(2m+1)^2 + 2a^2
$$
所以
$$
\begin{aligned}2a^2+1 &=a^2 bm-4m^2 - 4m\\		&= m(a^2b-4m-4)\end{aligned}
$$
当 $a = \pm1$ 时：
$$
3=m(b-4m-4)
$$
显然得到所有的四元组 $(m,n,a,b)$ 为：$(1,\pm 3, \pm 1,11), (-1, \pm 1, \mp 1, -3),(3,\pm 7, \pm 1 ,17),(-3, \pm 5, \mp 1 ,-9)$。同样可得 $a=\pm3$ 时四元组有 $(19, \pm 13, \pm 3, 9)$ 与 $(1, \pm 1, \pm 3, 3)$。

现假设 $|a| \geq 5$，注意到
$$
2n^2 + 4=abn-b\\(ab-2)n=b+4
$$
令 $\lambda = ab-2n$ 可知
$$
n=\frac{b+4}{\lambda}
$$
所以
$$
2 \cdot \frac{(b+4)^2}{\lambda^2} + 4 = \frac{ab(b+4)}{\lambda}-b
$$

$$
2(b+4)^2 + 4\lambda^2 =ab(b+4)\lambda-b\lambda^2\\ab(b+4)\lambda = (b+4)\lambda^2+2(b+4)^2\\a\lambda = \frac{\lambda^2}{b} + \frac{2(b+4)}{b} = \frac{\lambda^2+8}{b}+2
$$

所以
$$
b=\frac{\lambda^2 + 8}{a\lambda+2},n=\frac{b+4}{\lambda} = \frac{\lambda+4a}{a\lambda-2}
$$
取 $\lambda = \pm1$，有 $b \mid 9$，所以 $b \in \{-3, -1, 1, 3\}$，可得到符合条件的四元组有：$(17, \pm 7, \pm 5, 3), (27, \pm 5, \pm 1, 1), (-11, \pm 13, \mp 7, -1)$。

同理，$|\lambda| \leq 5$ 时，四元组有 $(-3, \pm 1, \mp 5, -1), (3, \pm 1, \pm 7, -1)$。

设函数 $f(x) = \displaystyle \frac{x+4|a|}{|a|x-2}$，则 $|n|=f(|\lambda|)$。

 由于我们已假设 $|a| \geq 5$，因此
$$
f'(x) = \frac{|a|x-2-(x+4|a|)|a|}{(|a|x-2)^2} = -\frac{4|a|^2+2}{(|a|x-2)^2} < 0
$$
由于 $|\lambda| \geq 7$，因此 $|n| \leq f(7) = \frac{4|a|+7}{7|a|-2} <1$，不存在这样的 $n$。







