# 4. The renormalization group and scaling
$$
\begin{aligned}
\end{aligned}
$$

## 4.1 Scale invariance

凝縮体の問題を解く際には

- ハミルトニアン

    $H=H^*+H'$

- 作用

    $S=S^*+S'$

の形で書くことが多く, またこれらを場$\phi(x)$およびその微分を用いて表すことが可能である.

この場$\phi$は大概はFermi統計またはBose統計に従い, それに応じて

- Fermi: グラスマン
- Bose:  スカラー(またはベクトル)

といった代数系にそれぞれ従うことになる.

以上のことをもちいて, 次のような経路積分の文脈で問題を解くことを題材としていく.

$$
\begin{aligned}
    \mathcal{Z} = \int \mathcal{D}\phi e^{-S(\phi)}
\end{aligned}
$$

#### 繰り込み群の流れ

1. 異なる大きさや異なる組み合わせを
2. 新たなパラメータを定義する("renormalized")ことで
3. 変化前と同様の系を保ちながら
4. システムを(短距離 or 高エネルギーでの)カットオフを施した状態に写像する

といった流れを取る.

#### カットオフ

場$\phi(x,t)\equiv \phi(x)$ は($D$次元として)多くのフーリエ成分を持つ.

$$
\begin{aligned}
    \phi(x)=\int\frac{d^Dk}{(2\pi)^D}e^{ik\cdot x}\phi(k)
\end{aligned}
$$

もし高い($k,\omega$)の成分($\phi_{>}(x)$と表すこととする)を積分で消去することができれば, 残った部分は低い($k,\omega$)を持った成分($\phi_{<}(x)$)が有効作用(または有効ハミルトニアン)として扱うことができるようになる.


$$
\begin{aligned}
    &\downarrow \\
    &\mathcal{Z}=\int\mathcal{D}\phi e^{-S(\phi)}=\int\mathcal{D}\phi_{<}\mathcal{D}\phi_{>} e^{-S(\phi_{<}+\phi_{>})}
\end{aligned}
$$

ここでもし

$$
\begin{aligned}
    e^{-S_{\rm eff}(\phi_{<})}\equiv \int\mathcal{D}\phi_{>} e^{-S(\phi_{<}+\phi_{>})}
\end{aligned}
$$

が成立するならば,

$$
\begin{aligned}
    \mathcal{Z}=\int\mathcal{D}\phi_{<} e^{-S_{\rm eff}(\phi_{<})}
\end{aligned}
$$

として有効作用を用いた同系へと変形された.

#### 固定点

作用$S^*$が次のような関係が成立するようなとき

$$
\begin{aligned}
    S^*_{\rm eff}(\phi_{<})=S^*(\phi)
\end{aligned}
$$

この作用は繰り込み群(RG)の ___固定点___ であるという.

固定点においては, 対称性として ___スケール不変性___ が生まれることとなる.

$\to$ もはやスケールが問題外となる!

また極限の性質を得ることもできるようになる.

1. 相関長が消え($\xi\to0$), エネルギーギャップが発散する($E_{\rm G}\to\infty$)
2. 相関長が発散して($\xi\to\infty$), エネルギーギャップが消える($E_{\rm G}\to0$)