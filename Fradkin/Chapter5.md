# 5. One-Dimensional Quantum Antiferromagnets

## 5.1 The Spin-One-Half Heisenberg Chain

サイト数$N$の1次元Heisenberg模型を考えてみる.
ハミルトニアンは次の通り.

$$
\begin{aligned}
    H = J \sum_{n=1}^{N} \vec{S}(n) \cdot \vec{S}(n+1)
\end{aligned}
$$

ここで$J>0$とする. 
また便利のためにサイト数$N$は偶数とし, 周期境界条件がかかっていると仮定する.

この系から得られる特徴の多くは, 次の4つから由来している.
1. 基底状態におけるベーゼ仮説(Bethe-Ansatz)の解およびその励起スペクトル([Yang 69]())
2. サインゴルドン(Sine-Gordon)理論の射影([Luther 75]())
3. 非可換ボゾン化([Affleck 85]())
4. シグマ模型の射影([Hldane 83]())


ベーゼ仮説の厳密解は1次元可積分系に特有に現れるもので, 一般的には導出不可能である.
(他の系でも同様であるが, 高次元の場合に適用できることもあり, 現在さかんに研究が進んでいる)

### 5.1.1 The Bethe-Ansatz Solution

スピン$\frac{1}{2}$が$N$個連なった純粋状態の波動関数を出発点とする.
$n$番目のサイトにある電子のスピン状態を知るためのスピン演算子を$\vec{S}(n)$と表記すると, 励起状態$\Psi(s(1),\dots,s(n))$のスピン状態を次のように導ける.

$$
\begin{aligned}
    S_z \Psi(s(1),\dots,s(N))
    =& \left(\sum_{n=1}^{N}s(n)\right)\Psi(s(1),\dots,s(N))
\end{aligned}
$$

下向きのスピンの総数を$M$を記述すれば,

$$
\begin{aligned}
    \left(\sum_{n=1}^{N}s(N)\right)
    =& \frac{N}{2}-M
\end{aligned}
$$

波動関数を便利のために表記を変えてみる.

$$
\begin{aligned}
    \Psi(s(1),\dots,s(N))
    \equiv& \phi(x_1,\dots,x_M)
\end{aligned}
$$
(正確には$\phi$は係数のような役割?)


$x_j$はスピンが逆を向いているサイトを示している.
例えば, $n=1,4$の2箇所が下を向いていた場合は,$\phi(1,4)$と書ける.
また強秩序状態は$\Psi_0=\left|\uparrow\dots\uparrow\right>$と表記することとする.

下向きスピンが$M$この場合の一般的な状態は次のように書くことができる.


$$
\begin{aligned}
    \Psi
    =& \sum_{\{x_j\}}\phi(x_1,\dots,x_M)S^-(x_1)\dots S^-(x_M)\Psi_0
\end{aligned}
$$
ここで$S^-(n)$は$n$番目のサイトのスピンを下に向ける演算子である.

### 5.1.2 The Basis Function

ベーゼの手法は, まずスピンの位置を入れ替える演算子$P{n,m}$を用いることから考える.

$$
\begin{aligned}
    P_{n,m}&\Psi(s(1),\dots,s(n),\dots,s(m),\dots,s(N))\\
    = & \Psi(s(1),\dots,s(m),\dots,s(n),\dots,s(N))
\end{aligned}
$$

<!-- 
すると境界条件のある下ではハミルトニアンは次のように書き下すことが可能.

$$
\begin{aligned}
    H 
    =& J \sum_{n=1}^{N} \vec{S}(n) \cdot \vec{S}(n+1)\\
    =& J \sum_{n=1}^{N} \left(P_{n,n+1}-1\right)\tag{?}\\
\end{aligned}
$$ 
-->

全体のスピンを一つ平行移動させる演算子を$\tilde{P}$とすると

$$
\begin{aligned}
    \tilde{P}\Psi(s(1),\dots,s(N))
    =& \Psi(s(N),s(1),\dots,s(N-1))
\end{aligned}
$$ 

一つだけ下向きスピンを持つ状態

$$
\begin{aligned}
    \Psi(s_1,\dots,s_N)
    =& \sum_{p=1}^N \psi(p)\left|\uparrow\dots \downarrow \dots \uparrow\right>
\end{aligned}
$$ 

に$\tilde{P}$を作用させると$\tilde{P}\Psi=\mu \Psi$を書けることから,

$$
\begin{aligned}
    \tilde{P}\phi(p) = \phi(p+1) = \mu \phi(p)\quad \text{for}\quad p=1,\dots,N
\end{aligned}
$$ 

となることがわかる.
つまり, $\phi(1)=1$と仮定すれば

$$
\begin{aligned}
    \phi(p)
    =& \mu^{p-1}
\end{aligned}
$$ 

となる. (もちろん周期境界条件から$1=\mu^N$である)


