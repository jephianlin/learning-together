---
description: notes, 2020F, math203, discrete math, jephian, nsysu, 離散數學一, 林晉宏
tags: learning-together
---

# 離散數學（一）課程筆記 2020FMath203

![](https://i.imgur.com/EYydzth.png)


----

## 1: 關於這門課 (2020/09/06~2020/09/12)
- [課程網頁](http://www.math.nsysu.edu.tw/~chlin/2020FMath203/2020FMath203.html)：課程資訊、大綱、評分方式、各種規範。
- [課程筆記](https://hackmd.io/@jlch3554/2020FMath203-notes)：這個頁面，記錄上課內容、作業。
- [討論版](https://hackmd.io/@jlch3554/2020FMath203-forum)：問問題，搶 AL 分數。
- [網路大學](https://cu.nsysu.edu.tw/)：查分數。
- 課本：[_Applied Combinatorics_](https://appliedcombinatorics.org/) by Mitchel T. Keller and William T. Trotter [ [html](https://rellek.net/book/app-comb.html) [pdf](https://www.rellek.net/book-2017/app-comb-2017.pdf) ]

---

### 暖身一下

如果你的生日是 20yy 年 X 月 dd 日  
請計算  yy + (yy % 4) + mm + dd 並除 7 取餘數  
如果是 19yy 出生的，再額外加 1

mm = 

| Jan | Feb | Mar | Apr |
|-----|-----|-----|-----|
| 6 | 2 | 2 | 5 |

| May | Jun | Jul | Aug |
|-----|-----|-----|-----|
| 0 | 3 | 5 | 1 |

| Sept | Oct | Nov | Dec |
|-----|-----|-----|-----|
| 4 | 6 | 2 | 4 |

- 互相認識一下，年級、科系、為什麼會修這門課？
- 高中最喜歡的科目？如果是數學的話、哪個部份？
- 你覺得離散數學跟高中哪個部份有關？

---

### 課前準備
- Kahoot:  [Get ready for 2020FMath203](https://create.kahoot.it/share/2020fmath203-get-ready-for-the-course/0804aab5-ede0-4d72-a012-81d4fc0e6baf)
- HW0: [Tell me your email](https://docs.google.com/forms/d/e/1FAIpQLSf_Qiclf_dFje3ESWjJjjRwPIuZ1UJn8e1kPB94lhXW2103PQ/viewform) 

[//]: # (
something about syllabus
how much are you willing to do preview
which email address do you use
how often do you check it
do you use Google Calendar or any calendar app?
how often do you check FB/Discord
)

---

### 這週要做的事

#### 影片（每週二上課前完成）
- [video 1](https://youtu.be/waMdCn2Cqv4): Topics in discrete mathematics  (to be watched in class) 
- reading assignment: [1.1 Introduction](https://rellek.net/book/s_intro_intro.html)
- [questions 1](https://docs.google.com/forms/d/e/1FAIpQLSfRCkbpDi6c-jKF3-Nepkh9MfYqBpzq8OMugajdilGrpdzoNA/viewform?usp=sf_link)

```
AL 分數 += Question 分數 * 0.01
```

[//]: # (
...
finite, doable
get your hand dirty: try, example, observe, programming
three categories
how to read text book
)

#### HW1（下週二 5:00 pm 前交給助教）
請註名姓名學號以及第幾次作業
1. 把 $00000111$ 八個數字排成一列，有幾種排法是最左邊的 $1$ 和中間的 $1$ 間隔至少兩個 $0$、中間的 $1$ 和最右邊的 $1$ 間隔至少一個 $0$？列出所有這樣的字串。
2. 在下方的圖中，把邊上的數字當作距離，若要從 $A$ 點走到 $B$ 點，最短的路徑是哪條？怎麼確認它是最短的？  
![](https://github.com/jephianlin/TikZStudio/raw/master/gallery/figures/shortestAB.png)


---

### 如何使用討論版

[討論版](https://hackmd.io/@jlch3554/2020FMath203-forum)

[//]: # (
我要怎麼打 C n 取 k？
reply
有個句子看不懂
reply
)

---

### 離散數學考慮的問題
1. 把正整數 $n$ 寫成幾個正整數的合（不計較順序）叫作 $n$ 的分解。比如說  
$\begin{aligned}
4 &= 4 \\
  &= 3+1 \\
  &= 2+2 \\
  &= 2+1+1 \\
  &= 1+1+1+1
\end{aligned}$  
有 $5$ 種分解。算算看 $8$ 有幾種分解？有幾個分解是奇數項？有幾個分解每項數字都不同？
2. 看著下方的圖，利用以下的敘述猜測各個專有名詞的意思。  
![Figure 1.2 of the textbook](https://rellek.net/book/images/3012-fig15.svg "Figure 1.2 of the textbook")   

    + $G$ has $9$ **vertices** and $10$ **edges**.
    + $\{2,6\}$ is an **edge**.
    + $\{5,4\}$ is not an edge.
    + Vertices $5$ and $9$ are **adjacent**.
    + Vertices $3$ and $7$ are not adjacent.
    + $P=(4,3,1,7,9,5)$ is a **path** of length $5$ from vertex $4$ to vertex $5$.
    + $C=(5,9,7,1)$ is **cycle** of length $4$.
    + $G$ is **disconnected** and has two **components**. One of the components has vertex set $\{2,6,8\}$.
    + $\{1,5,7\}$ is a **triangle**.
    + $\{1,7,5,9\}$ is a **clique** of size $4$.
    + $\{4,2,8,5\}$ is an **independent set** of size $4$.
    
3. 看著下方的圖，回答以下問題。  
![Figure 1.4 of the textbook](https://rellek.net/book/images/3012-fig17.svg "Figure 1.4 of the textbook")
    + 圖中最長的 path 有幾條邊？
    + 圖中最長的 cycle 有幾條邊？
    + 圖中最大的 clique 有幾個點？
    + 圖中最大的 independent set 有幾個點？
    + 從點 $7$ 到點 $6$ 最短的 path 有幾條邊？
4. 有沒有辦法把 $K_{3,3}$ 放在平面上使得邊都沒交叉？

----

## 2: 字串、集合、二項式係數 (2020/09/13~2020/09/19)

---

### 這週要做的事

#### 影片（每週二上課前完成）
- [video 2](https://youtu.be/c-ppdqNDe6U): Strings
- reading assignment: [2.1 Strings: A First Look](https://rellek.net/book/s_strings_intro.html) before Example 2.1
- [questions 2](https://docs.google.com/forms/d/e/1FAIpQLScfWZLCCt6GTIgzFzBj1glQztW0KeeyfriYVyOZGC1D3LHOhA/viewform?usp=sf_link)

```
AL 分數 += Question 分數 * 0.01
```

[//]: # (
string, def, notation
binary, ternary strings
cartesian
|X x Y| = |X| x |Y|
letter words, etc
)

#### HW2（下週二 5:00 pm 前交給助教）
請註名姓名學號以及第幾次作業
1. 令 $\mathbb{Z}$ 為所有整數、$\mathbb{Z}^+$ 為所有正整數，找一個函數 $f: \mathbb{Z} \rightarrow \mathbb{Z}^+$ 使得 $f$ 是一個 bijection。證明你給的 $f$ 確實是一個 bijection。
2. 令 $a_0 = a_1 = 1$ 且 $a_n = a_{n-1} + a_{n-2}$。用組合證明來證明 $a_0^2 + a_1^2 + \cdots + a_n^2 = a_n\times a_{n+1}$。提示：[The magic of Fibonacci numbers](https://www.ted.com/talks/arthur_benjamin_the_magic_of_fibonacci_numbers)。

---

### 證明數量一樣 Bijection
- 列出所有長度是 5 且恰有兩個 1 的 binary string；同時列出所有 $\{1,2,3,4,5\}$ 裡面大小是 2 的子集。它們個數一樣多嗎？它們彼此有沒有什麼對應關係？
- $[4]$ 的子集中，大小為奇數的子集（**奇子集**）有幾個？大小為偶數的子集（**偶子集**）有幾個？
- 證明對任意正整數 $n$，集合 $[n]$ 的奇子集和偶子集個數一樣多。
- 證明正奇數和正偶數一樣多。

--- 

### 符號

| 名稱 | 高中 | 公式 | 大學 |
| -------- | -------- | -------- | -------- |
| 組合 combination | $C^n_k$ | $\frac{n!}{k!(n-k)!}$ | $\binom{n}{k}$ |
| 排列 permutation | $P^n_k$ | $\frac{n!}{(n-k)!}$ | $k!\binom{n}{k}$ |
| 重覆排列 combination with repetition | $H^n_k$ | $\frac{(n+k-1)!}{k!(n-1)!}$ | $\binom{n+k-1}{k}$ |

$\binom{n}{k}$ 讀作 "n choose k"，$\LaTeX$ 的打法為 `$\binom{n}{k}$`。

- 要如何說明 $P^n_k = \frac{n!}{(n-k)!}$？
- 要如何說明 $C^n_k = \frac{n!}{k!(n-k)!}$？

---

### 組合證明（Combinatorial proof）
- 下圖為 $(n+1)\times (n+1)$ 格點的示意圖，問對角線的右上（不包含對角線）有幾個點？  
    ![Figure 2.14 of the textbook](https://rellek.net/book/images/3012-fig25.svg "Figure 2.14 of the textbook" =400x)
    :::spoiler
    $$1 + 2 + \cdots + n = \frac{n(n+1)}{2}$$
    :::
- 求 $1 + 3 + 5 + \cdots + (2n-1)$ 的公式（用 $n$ 表示）。
    :::spoiler 
    ![Figure 2.15 of the textbook](https://rellek.net/book/images/3012-fig21.svg "Figure 2.15 of the textbook" =400x)
    :::
- 長度是 $n$ 的 binary string 有幾個？它們可以用 $1$ 的個數分為 $n+1$ 類，每類各有幾個？
    :::spoiler
    $$\binom{n}{0} + \binom{n}{1} + \cdots + \binom{n}{n} = 2^n$$

    這個方法叫 **double counting**，用兩種不同方法來計算同一個集合的個數，因而得到恆等式。
    :::
- 利用 double counting 的方法來證明  
    $$\binom{n}{0}2^n + \binom{n}{1}2^{n-1} + \cdots + \binom{n}{n}2^0 = 3^n $$
- 利用 double counting 的方法來證明  
    $$\binom{n}{k+1} = \binom{n-1}{k} + \binom{n-2}{k} + \cdots + \binom{k}{k}$$
- 利用 double counting 的方法來證明  
    $$\binom{2n}{n} = \binom{n}{0}^2 + \binom{n}{1}^2 + \cdots + \binom{n}{n}^2$$

--- 

### 二項式係數

- $x_1 + x_2 + x_3 = 5$ 有幾組正整數解？
- $x_1 + x_2 + x_3 = 5$ 有幾組非負整數解？
- $x_1 + x_2 + x_3 \leq 5$ 有幾組正整數解？
- $x_1 + x_2 + x_3 \leq 5$ 有幾組非負整數解？

---

### Catalan number

$\rightarrow: (1,0)$  
$\uparrow: (0,1)$

- 利用 $\rightarrow$ 及 $\uparrow$ 從 $(0,0)$ 走到 $(m,n)$ 有幾種不同的走法？
    ![Figure 2.26 in the textbook](https://rellek.net/book/images/3012-fig22.svg "Figure 2.26 in the textbook" =400x) 
- 利用 $\rightarrow$ 及 $\uparrow$ 從 $(0,0)$ 走到 $(4,4)$ 且沒有超過 $x=y$ 有幾種不同的走法？如果把 $(4,4)$ 改成 $(n,n)$？
- 利用 $\rightarrow$ 及 $\uparrow$ 從 $(0,0)$ 走到 $(4,4)$ 且有超過 $x=y$ 有幾種不同的走法？如果把 $(4,4)$ 改成 $(n,n)$？
:::spoiler
目標：從 $(0,0)$ 走到 $(4,4)$  
條件：$\rightarrow$ 及 $\uparrow$；有超過 $x=y$  
令 $D_n$ 為符合條件的走法數。  
列出 $D_1$, $D_2$, $D_3$, $D_4$ 並猜測 $D_n$。 
:::

:::spoiler
$D_1 = 1$,  
$D_2 = 4$,  
$D_3 = 15$,  
$D_4 = 56$,  
$D_5 = 210$,  
找一個巴斯卡三角形，猜測 $D_n = \binom{2n}{n-1}$。 

這個答案是正確的，但是為什麼？（[Example 2.28 of the textbook](https://rellek.net/book/s_strings_bin-coeff.html)）
:::

利用 $\rightarrow$ 及 $\uparrow$ 從 $(0,0)$ 走到 $(n,n)$ 且沒有超過 $x=y$ 的走法數有稱作 **Catalan number**，記作 $C_n$。  
    $$C_n = \binom{2n}{n} - D_n = \frac{1}{n+1}\binom{2n}{n}$$
    
---

### 二項式定理 & 多項式定理

- 把 $(1+x)^4$ 展開的（升冪）係數為多少？
- 把 $(1+x)(2+x)(3+x)(4+x)$ 展開的（升冪）係數為多少？

**二項式係數**（binomial coefficient）  
    $$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$

##### Theorem 2.30 (Binomial Theorem)
若 $n$ 為一個非負整數，則  
    $$ (x+y)^n = \sum_{k=0}^n \binom{n}{k} x^{n-k}y^k $$

**多項式係數**（multinomial coefficient）  
    $$\binom{n}{k_1,k_2,\ldots, k_r} = \frac{n!}{k_1!k_2!\cdots k_r!}$$

##### Theorem 2.33 (Multinomial Theorem)
若 $n$ 為一個非負整數，則  
    $$ (x_1+x_2+\cdots+x_r)^n = \sum_{k_1+k_2+\cdots+k_r=n} \binom{n}{k_1,k_2,\ldots,k_r} x_1^{k_1}x_2^{k_2}\cdots x_r^{k_r}$$
    
- 計算 $(3x+2y)^5$ 中 $xy^4$ 的係數。
- 計算 $(3x+2y+5z)^6$ 中 $xy^2z^3$ 的係數。
    
----

## 3: 數學歸納法 (2020/09/20~2020/09/26)
週六補課

---

### 這週要做的事

#### 影片（每週二上課前完成）
- [video 3](): Well-ordering principle :construction:
- reading assignment: [3.1 Introduction](https://rellek.net/book/s_induction_intro.html) and [3.2 The Positive Integers are Well Ordered](https://rellek.net/book/s_induction_posintsord.html)
- [questions 3]() :construction:

```
AL 分數 += Question 分數 * 0.01
```

[//]: # (
minimum
three sets Z, R, Z+
Peano Postulates
two ways to think about induction
)

#### HW2（下週二 5:00 pm 前交給助教）
請註名姓名學號以及第幾次作業
1. 證明 Theorem 3.9。
2. 令 $a_0 = a_1 = 1$ 且 $a_n = a_{n-1} + a_{n-2}$。用（強）數學歸納法來證明 $a_0^2 + a_1^2 + \cdots + a_n^2 = a_n\times a_{n+1}$。

---

### 理所當然？遞迴定義

- 找一下下方數列的規律，或猜測下一項。
    $1, 2, 3, 4, 1, 2, 3, 4, 5, 1, 2, 3, 4, 5, 2, 3, 4, 5, 6, 2, 3, 4, 5, 6, \ldots$
- 當有人寫 $1+2+3+\cdots +6$ 或是 $\sum_{k=1}^6 k$ 的時候他的意思是哪個？
    1. $1+2+3+4+5+6$
    2. $1+2+3+4+1+2+3+4+5+1+2+3+4+5+2+3+4+5+6+2+3+4+5+6$
    :::spoiler
    我們用遞迴的方法明確地定義 $\sum_{i=1}^n f(i)$ 的意思。
    - $\sum_{i=1}^1 = f(1)$
    - $\sum_{i=1}^{n} = f(n) +\sum_{i=1}^{n-1} f(i)$ for any $n > 1$
    :::
- 平常我們會寫 $n! = n\times (n-1)\times \cdots\times  1$，試著遞迴的方法來寫 $n!$ 的定義。
    :::spoiler
    - $1! = 1$
    - $n! = n\times (n-1)!$ for any $n > 1$
    :::
- 執行課本 3.3 中的[程式](https://rellek.net/book/s_induction_statements.html#sage-4)，猜測 `sumrecursive(5)` 並看看你的答案是否正確。
- 改寫剛剛的程式，讓它可以計算 $n!$。
- 如何利用遞迴定義來定義二項式係數？
    :::spoiler
    方法一：
    - $$\binom{n}{0} = \binom{n}{n} = 1 \text{ for any } n$$
    - $$\binom{n}{k} = \binom{n-1}{k-1} + \binom{n-1}{k} \text{ for any } k\neq 0,n$$

    方法二：
    - $$\binom{n}{0} = 1 \text{ for any } n$$
    - $$\binom{n}{k} = \frac{n-k+1}{k}\binom{n}{k-1}$$

    哪一個方法寫的程式比較快？
    :::

---

### 除法原理

- 證明對於任何的正整數 $n$，$n$ 和 $n+1$ 一定互質。
- 證明對於任何的正奇數 $n$，$n$ 和 $n+2$ 一定互質。

##### Theorem 3.7 (Division Theorem)
若 $m$ 和 $n$ 為正整數。則存在唯一的整數 $q$ 和唯一的整數 $r$ 使得
    $$ m = q\cdot n + r \text{ and } 0\leq r< n.$$
    
這裡的 $q$ 被稱作**商**（quotient）  
而 $r$ 被稱作**餘數**（remainder）

- 證明唯一性。（假設有 $q_1,r_1$ 及 $q_2,r_2$ 同時滿足除法原理的式子，說明 $q_1=q_2$，$r_1=r_2$。）

- 證明存在性：在以下情況下，怎麼找到 $q$ 和 $r$？
    - $m = 1$ 時？
    - $n = 1$ 時？
    - $m = 100$, $n = 7$ 時？
    - 任意的 $m$ 和 $n$？ 
    :::spoiler
    參考[課本證明](https://rellek.net/book/s_induction_recursion.html#s_induction_gcd)。
    :::
    
### 輾轉相除法

**最大公因數**（greatest common divisor）  
記作 $\gcd(m,n)$


##### Theorem 3.8 (Euclidean Algorithm)
若 $m$ 和 $n$ 為正整數且 $m>n$。令 $q$ 和 $r$ 為滿足
    $$ m = q\cdot n + r \text{ and } 0\leq r< n$$
的商和餘數。  
- 若 $r>0$，則 $\gcd(m,n) = \gcd(n,r)$；
- 若 $r=0$，則 $\gcd(m,n) = n$。

對於以下的 $m,n,c$ 找一組整數 $a,b$，使得 $am+bn = c$，或說明這樣的 $a,b$ 不存在。
- $m = 7$, $n=13$, $c=1$。
- $m = 4$, $n=2$, $c=1$。
- $m = 99$, $n=121$, $c=5$。
- $m = 99$, $n=121$, $c=5$。
    
##### Theorem 3.9
若 $m$ 和 $n$ 為正整數。以下 $a,b$ 的整數方程（又叫丟番圖方程）
    $$ am + bn = c$$
有解若且唯若 $c$ 是 $\gcd(m,n)$ 的倍數。 

:::spoiler
證明必要性：  
說明若 $c$ 不為 $\gcd(m,n)$ 的倍數，則方程式無解。

證明充分性：  
令 $x_0 = \max\{m,n\}$, $y_0 = \min\{m,n\}$。  
若 $x_0 = q_0y_0+r_0$，先說明 $r_0$ 可以寫成 $a_0x_0 + b_0y_0$。  
令 $x_0 = y_0$, $y_0 = r_0$，則 $\gcd(x_0,y_0) = \gcd(y_0, r_0)$。  
$\cdots$
:::

--- 

### 排序

如何將一堆數字  
```
[13, 19, 94, 77, 51, 73, 67, 57, 89, 76, 
 44, 27, 56, 41, 58, 81, 31, 6, 16, 87, 
 46, 19, 5, 24, 77, 46, 27, 89, 32, 25, 
 96, 100, 19, 96, 38, 39, 42, 51, 46, 25, 
 6, 57, 47, 41, 17, 43, 100, 87, 47, 70, 
 86, 56, 64, 15, 20, 100, 94, 40, 80, 99, 
 30, 17, 76, 62, 32, 43, 43, 53, 97, 59, 
 12, 14, 44, 32, 100, 51, 89, 18, 38, 30, 
 36, 98, 63, 62, 85, 90, 21, 40, 67, 38, 
 15, 73, 5, 41, 74, 30, 42, 81, 79, 9, 
 80, 54, 5, 2, 80, 29, 24, 30, 89, 85, 
 97, 97, 78, 61, 31, 74, 26, 96, 71, 87, 
 82, 59, 19, 12, 15, 92, 12, 69]

```
從小到大排好？

:::spoiler
- 不斷把最小的挑出來放在最前面（selection sort） $\sim n^2$
- 不斷比較連續兩個數字並調整順序（bubble sort） $\sim n^2$
- 分工合作？（Merge sort） $\sim n\log n$
:::

**Selection sort**
1. 在紙條上找出數字最小的數，把這個數畫掉然後記錄在你自己的紙上。

**Mergesort**  
1. 一位同學拿起紙條，用剪刀把數字大約均分成兩份，把兩份紙條交給兩位有空的同學。
2. 每位拿到紙條的同學：
    - 如果你覺得紙條上數字夠少可以排序了（可能少於 4 個數字？），請把你手上的數字排好寫在紙上，交回給交給你紙條的同學
    - 如果你覺得紙條上數字還太多，用剪刀把數字大約均分成兩份，把兩段紙條交給兩位有空的同學。

比較兩個方法的優缺點？

---

### 數學歸納法

對於以下的式子，判斷對所有正整數 $n$ 是否都正確，還是取決於 $n$？
1. $2n + 7 = 13$
2. $3n − 5 = 9$
3. $n^2 − 5n + 9 = 3$
4. $8n − 3 < 48$
5. $8n − 3 > 0$ 
6. $(n + 3)(n + 2) = n^2 + 5n + 6$ 
7. $n^2 − 6n + 13 \geq 0$
:::spoiler
這樣的敘述叫作 **open statement**  
它可以是一個方程式、一個不等式、或是任何敘述。  

比如說：  
1. $$\sum_{k=1}^n k= \frac{n(n+1)}{2}$$
2. $$\sum_{k=1}^n 2k-1 = n^2$$
3. $n^n \geq n! + 4000000000n2^n$ when $n\geq 14$
:::

##### Principle 3.11 (Principle of Mathematical Induction)  
若 $S_n$ 是一個跟 $n$ 有關的 open statement。如果  

1. $S_1$ 是正確的，且  
2. $S_k$ 是正確的 $\implies$ $S_{k+1}$ 是正確的  

則 $S_n$ 對於任何正整數 $n$ 都是正確的。 

- 證明
    $$\sum_{k=1}^n k= \frac{n(n+1)}{2}$$
    :::spoiler
    令 $S_n$ 為上述的 open statement。  
    $S_1$ 的左式為 $\sum_{k=1}^1 k= 1$，右式為 $\frac{1(1+1)}{2} = 1$，左式等於右式，所以 $S_1$ 是正確的。
    
    假設 $S_n$ 的敘述是正確的，也就是對這個特定的 $n$   
    $$\sum_{k=1}^n k= \frac{n(n+1)}{2}$$  
    則我們可以驗證 $S_{n+1}$ 的敘述也是正確的：
    $$\begin{aligned}
    \sum_{k=1}^{n+1} k &= (n+1) + \sum_{k=1}^n k \\
    &= (n+1) + \frac{n(n+1)}{2} \qquad \text{ by }S_n \\
    &= \frac{(n+1)(n+2)}{2}
    \end{aligned}$$
    
    由數學歸納法得知， $S_n$ 對任意正整數 $n$ 都是正確的。
    :::
    
數學歸納法的證明包含幾個關鍵：
+ basis step
+ inductive step
+ inductive hypothesis（歸納法的假設）

用數學歸納法完成以下練習
- 證明
    $$\sum_{k=1}^n 2k-1 = n^2$$
- 框出 basis step, inductive step, 還有 inductive hypothesis

### 強數學歸納法

- 令 $f(1) = 3$, $f(2) = 5$ 且  
    $$f(n) = 2f(n-1) - f(n-2)$$
    猜測 $f(n)$ 的一般式。
- 如果只用數學歸納法來證明，會遇到什麼問題？

##### Principle (Strong Principle of Mathematical Induction)  
若 $S_n$ 是一個跟 $n$ 有關的 open statement。如果  

1. $S_1$ 是正確的，且  
2. $S_1$ 到 $S_k$ 都是正確的 $\implies$ $S_{k+1}$ 是正確的  

則 $S_n$ 對於任何正整數 $n$ 都是正確的。 

- 令 $f(1) = 1$, $f(2) = 2$ 且  
    $$f(n) = 2f(n-1) - f(n-2)$$
    猜測 $f(n)$ 的一般式。
- 用（強）數學歸納法來證明。

### 最小反例（Minimal counterexample）

數學歸納法 $\sim$ well-ordering principle  

另一種證明寫法：

- 證明
    $$\sum_{k=1}^n k= \frac{n(n+1)}{2}$$


令 $S_n$ 為上述的 open statement。  
$S_1$ 的左式為 $\sum_{k=1}^1 k= 1$，右式為 $\frac{1(1+1)}{2} = 1$，左式等於右式，所以 $S_1$ 是正確的。  

**假設**對某個 $n_0$，敘述 $S_{n_0}$ 是錯的。  
因此存在一個**最小**的正整數 $n$ 使得 $S_n$ 是錯的。  
我們還知道這個 $n>1$，因為 $S_1$ 是正確的。

因為 $n$ 已經是最小的，我們知道 $S_{n-1}$ 是對的，  
也就是說  
    $$\sum_{k=1}^{n-1} k= \frac{(n-1)(n)}{2}$$  


如果是這樣的話，我們就可以驗證 $S_{n}$ 的敘述也是正確的：
    $$\begin{aligned}
\sum_{k=1}^{n} k &= (n) + \sum_{k=1}^{n-1} k \\
&= (n) + \frac{(n-1)(n)}{2} \qquad \text{ by }S_{n-1} \\
&= \frac{n(n+1)}{2}
\end{aligned}$$  
但這和我們的假設矛盾，所以假設不成立。

----

## 4: (2020/09/27~2020/10/03)
週五中秋節彈性放假

----

## 5: (2020/10/04~2020/10/10)
週五國慶日補假

----

## 6: 期中考 (2020/10/11~2020/10/17)
週二期中考

----

## 7: (2020/10/18~2020/10/24)

----

## 8: (2020/10/25~2020/10/31)

----

## 9: (2020/11/01~2020/11/07)

----

## 10: (2020/11/08~2020/11/14)

----

## 11: (2020/11/15~2020/11/21)

----

## 12: 期中考 (2020/11/22~2020/11/28)
週二期中考

----

## 13: (2020/11/29~2020/12/05)

----

## 14: (2020/12/06~2020/12/12)

----

## 15: (2020/12/13~2020/12/19)

----

## 16: (2020/12/20~2020/12/26)

----

## 17: (2020/12/27~2021/01/02)

----

## 18: 期末考 (2021/01/03~2021/01/09)
週二期末考


