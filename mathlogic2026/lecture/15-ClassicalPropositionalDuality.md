---
title: 情報論理：古典命題論理の双対性
tags: mathematical-logic, slides, lecture
slideOptions:
  theme: white
  slideNumber: 'c/t'
  center: false
  transition: none
  controls: true
  progress: true
  history: true
  width: 1280
  height: 720
  margin: 0.08
---
<style>
body,
.markdown-body,
.reveal {
  font-family: "UD デジタル 教科書体 NP",
               "UD デジタル 教科書体 N",
               "UD デジタル 教科書体 NK",
               sans-serif !important;
}

/* 通常本文 */
.markdown-body :not(mjx-container):not(mjx-container *),
.reveal :not(mjx-container):not(mjx-container *) {
  font-family: "UD デジタル 教科書体 NP",
               "UD デジタル 教科書体 N",
               "UD デジタル 教科書体 NK",
               sans-serif !important;
}
.reveal h1,
.reveal h2,
.reveal h3,
.reveal h4,
.reveal h5,
.reveal h6 {
  text-transform: none !important;
}
/* コード部分は等幅フォント */
.markdown-body pre,
.markdown-body code,
.reveal pre,
.reveal code {
  font-family: "Cascadia Mono", "Consolas", monospace !important;
}

/* MathJax はデフォルトのまま */
mjx-container,
mjx-container * {
  font-family: inherit;
}

.reveal .math-proof { font-size: 85%; }
.reveal .math-proof mjx-container[display="true"] { text-align: left !important; }
.reveal { font-size: 36px; }
.reveal h1 { font-size: 2.2em; }
.reveal h2 { font-size: 1.5em; }
.reveal table { font-size: .85em; }
.reveal p, .reveal ul, .reveal ol { line-height: 1.35; }
.reveal .mermaid svg { max-height: 460px; }
.reveal section img { border: 0; box-shadow: none; }

/* Align slide content with the source PowerPoint. */
.reveal .slides section { text-align: left; }
.reveal .slides section mjx-container[display="true"], .reveal .slides section .MathJax_Display, .reveal .slides section .MathJax_SVG_Display { text-align: left !important; }
.reveal .slides section .mermaid { text-align: left; }
.reveal .slides section .mermaid svg { display: block; margin-left: 0 !important; margin-right: auto !important; }
.reveal .slides section table, .reveal .slides section img { margin-left: 0 !important; margin-right: auto !important; }
/* duality-left */

.reveal section.duality-detail h2 { font-size: 1.5em; margin-bottom: .4em; }
.reveal section.duality-detail p { margin: .4em 0; line-height: 1.3; }
.reveal section.duality-detail mjx-container[display="true"], .reveal section.duality-detail .MathJax_Display, .reveal section.duality-detail .MathJax_SVG_Display { margin: .4em 0 !important; }
</style>
---
# 情報論理

## 古典命題論理の双対性

西崎真也

Note:
本日は古典命題論理の双対性（duality）を扱います。射影幾何の例えから入り、写像 $d$ と双対性定理まで進めます。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 1 -->

---
<!-- .slide: class="duality-detail" style="font-size: 32px;" -->

## 双対性（duality）

Duality：二つの異なるものを組み合わせた状態（the state of combining two different things）。

数学の双対性：二つの役割を交換すると、対応する定理や法則が得られる。

Note:
双対性（duality）とは、点と直線、あるいは連言と選言のように、役割を入れ替えると対応する命題が得られる、という考え方です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 2 -->

---
<img src="assets/15-ClassicalPropositionalDuality/image1.png" alt="平面射影幾何に向けて" style="display:block; width:100%; height:600px; object-fit:contain; margin:0 auto;">

Note:
透視図の例です。平行線が遠くで一点に見える様子を確認してください。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 3 -->

---
## 平面射影幾何に向けて

ユークリッド幾何（普通の幾何）

平行線は交わらない。

長さや角度を測れる。比べられる。

三角形の相似比や面積などが意味をもつ。

透視図

平行線は遠くで一点で交わるように見える。

眺める位置が変わると長さも角度も変わる。

Note:
ユークリッド幾何では平行線は交わりませんが、透視図では平行線が一点で交わるように見えます。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 3 -->

---
<!-- .slide: class="duality-detail" style="font-size: 32px;" -->

## 平面射影幾何に向けて（続き）

でも「線が一点で交わる」「点が一直線上にある」は変わらない。†

† 平面間の射影変換を考える場合。

Note:
射影変換で長さや角度は変わりますが、結合関係（incidence）は保たれます。参考画像：https://upload.wikimedia.org/wikipedia/commons/a/ae/Komehakubutsukan-passage.jpg
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 3 -->

---
<!-- .slide: class="duality-detail" style="font-size: 30px;" -->

## 無限遠点と射影平面

無限遠点(point at infinity)を加えて、「平行線は無限遠点で交わる」と考える。

そうすると「どんな異なる2直線もただ1点で交わる」ということになる。

ユークリッド幾何「平行線は交わらない」

球面幾何「直線に相当する大円は、異なるもの同士なら互いに対蹠な2点で交わる」

射影平面には、無限遠点を集めた「無限遠直線」というものもある。

Note:
無限遠点を加えると、異なる2直線は必ず1点で交わります。球面幾何では大円が互いに対蹠な2点で交わる点と対比してください。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 4 -->

---
<!-- .slide: class="duality-detail" style="font-size: 32px;" -->

## 平面射影幾何

平面射影幾何

点と直線の集合があって、任意の異なる2点は1つの直線上にあり、任意の異なる2直線は1つの点で交わる、という性質をもつ幾何学。

$$
\mathrm{RP}^{2}=\left\{ \left[ x:y:z\right]   \mid     \left( x,y,z\right) \ne \left( 0,0,0\right) \right\}
$$

ただし、$\left[ x:y:z\right] =\left[ cx:cy:cz\right]   (c\ne 0)$とみなす、すなわち、三つの座標が共通の非零定数倍で結ばれる。これを同次座標と呼ぶ。

Note:
実射影平面 $\mathrm{RP}^{2}$ は、原点を通る直線の集合として同次座標で表せます。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 5 -->

---
<!-- .slide: class="duality-detail" style="font-size: 32px;" -->

## 平面射影幾何（続き）

$(a,b,c)\ne(0,0,0)$ とする。直線は、原点を通る平面

$$
\left\{ \left( x,y,z\right) \in {\mathbb{R} }^{3}   \mid     ax+by+cz=0\right\}
$$

に対応する。$a,b,c$を定数倍にしても同じ平面を表すので、平面も同次座標

$$
\left[ a:b:c\right]
$$

で表すことができる。

Note:
点も直線も同次座標 $[a:b:c]$ で表せることが、あとで述べる点と直線の双対性の背景です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 5 -->

---
<!-- .slide: class="duality-detail" style="font-size: 30px;" -->

## 射影幾何の定理の例

デザルグの定理（実射影平面）

二つの三角形 $\triangle ABC$ と $\triangle A'B'C'$ があり，

対応する頂点を結ぶ三線 $AA'$, $BB'$, $CC'$ が一点 $O$ で交わるならば，

対応する辺 $AB,BC,CA$ と $A'B',B'C',C'A'$ の交点

$P=AB\cap A'B'$, $Q=BC\cap B'C'$, $R=CA\cap C'A'$

は同一直線上にある。

Note:
デザルグの定理は、対応頂点を結ぶ三線が一点で交わるとき、対応辺の交点が同一直線上にある、という主張です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 6 -->

---
## 射影幾何の定理の例（続き）

<img src="assets/15-ClassicalPropositionalDuality/image4.png" alt="射影幾何の定理の例" style="display:block; width:100%; height:600px; object-fit:contain; margin:0 auto;">

Note:
図で、三線の交点 $O$ と、辺の交点 $P,Q,R$ が同一直線上にある様子を追ってください。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 6 -->

---
<!-- .slide: class="duality-detail" style="font-size: 30px;" -->

## 射影幾何の双対性

「点」と「線」を入れ替えても成り立つ。「同一直線上にある」と「同一点を通る」を入れ替えても成り立つ。

デザルグの定理の双対

二つの三角形 $\triangle ABC$ と $\triangle A'B'C'$ があり，

$AB,BC,CA$ と $A'B',B'C',C'A'$ の交点

$P=AB\cap A'B'$, $Q=BC\cap B'C'$, $R=CA\cap C'A'$

は同一直線上にあるならば、

対応する頂点を結ぶ三線 $AA'$, $BB'$, $CC'$ が一点 $O$ で交わる。

Note:
点と直線、および「同一直線上」「同一点を通る」を入れ替えると、デザルグの定理の双対が得られます。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 7 -->

---
## 古典論理

今紹介しているような論理を古典論理(classical logic)という。

直観主義論理(intuitionistic logic)という論理体系もある。

古典論理の特徴

真偽値による意味論。

背理法を認める。

双対性が成り立つ。

Note:
古典論理では真偽値意味論と背理法が使え、この授業で扱う双対性も古典論理の特徴です。直観主義論理では一般に双対性は成り立ちません。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 8 -->

---
## 双対性の事例

代表的な等式は、連言 $\land$ と選言 $\lor$（および略記の $\bot$ と $\top$）を入れ替えると対になります。

交換則

$$
\varphi\lor\psi\approx\psi\lor\varphi,\quad\varphi\land\psi\approx\psi\land\varphi
$$

分配則

$$
(\varphi\lor\psi)\land\sigma\approx(\varphi\land\sigma)\lor(\psi\land\sigma)
$$

Note:
交換則と分配則は、$\lor$ と $\land$ を入れ替えたものがそれぞれ対になっています。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 9 -->

---
## 双対性の事例（続き）

$$
(\varphi\land\psi)\lor\sigma\approx(\varphi\lor\sigma)\land(\psi\lor\sigma)
$$

恒等性

$$
\varphi\lor\bot\approx\varphi,\quad\varphi\land\top\approx\varphi
$$

零化（annihilator）

$$
\varphi\land\bot\approx\bot,\quad\varphi\lor\top\approx\top
$$

Note:
恒等性の対に加え、$\varphi\land\bot\approx\bot$ と $\varphi\lor\top\approx\top$ も双対の対です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 9 -->

---
## 双対性の事例（続き）

結合則

$$
(\varphi\land\psi)\land\sigma\approx\varphi\land(\psi\land\sigma)
$$

$$
(\varphi\lor\psi)\lor\sigma\approx\varphi\lor(\psi\lor\sigma)
$$

吸収則

$$
\varphi\land(\psi\lor\varphi)\approx\varphi,\quad\varphi\lor(\psi\land\varphi)\approx\varphi
$$

Note:
結合則と吸収則も、$\land$ と $\lor$ を入れ替えた式がそれぞれ対になります。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 9 -->

---
## 双対性の事例（続き）

べき等性

$$
\varphi\lor\varphi\approx\varphi,\quad\varphi\land\varphi\approx\varphi
$$

ド・モルガンの法則

$$
\neg(\varphi\land\psi)\approx\neg\varphi\lor\neg\psi
$$

Note:
べき等性とド・モルガンの法則も、$\land$ と $\lor$ の入替で対になる等式の例です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 9 -->

---
## 双対性の事例（続き）

$$
\neg(\varphi\lor\psi)\approx\neg\varphi\land\neg\psi
$$

Note:
ド・モルガンのもう一方です。前ページの式と合わせて、否定の内側で $\land$ と $\lor$ が入れ替わります。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 9 -->

---
<!-- .slide: class="duality-detail" style="font-size: 32px;" -->

## 双対性（ゆるふわ）

双対性

命題記号と $\land$ と $\lor$ と $\neg$ のみからなる命題の等式は、$\land$ を $\lor$ にして、$\lor$ を $\land$ にしても、等式は等式のまま。

略記の $\bot$ と $\top$ については、$\bot$ を $\top$ に、$\top$ を $\bot$ にする（これは $\bot\approx(\neg p\land p)$、$\top\approx(\neg p\lor p)$ という略記から従う）。

Note:
直感的には $\land$ と $\lor$ を入れ替えれば等式の対が得られます。$\bot$ と $\top$ の入替は、それらを連言・選言の略記とみなすことから従います。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 10 -->

---
<img src="assets/15-ClassicalPropositionalDuality/image9.png" alt="旭山動物園　空飛ぶペンギン" style="display:block; width:100%; height:600px; object-fit:contain; margin:0 auto;">

Note:
一息つきましょう。旭山動物園の「空飛ぶペンギン」の写真です。このあと形式的な写像 $d$ の定義に入ります。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 11 -->

---
<!-- .slide: class="duality-detail" style="font-size: 30px;" -->

## 写像$d$

双対性を述べるときは、命題は命題記号 ${p}_{i}$、否定 $\neg$、連言 $\land$、選言 $\lor$ のみから構成されると仮定する（van Dalen と同様）。

$\bot$ と $\top$ は原始記号ではなく、それぞれ $(\neg p\land p)$、$(\neg p\lor p)$（$p$ は任意の命題記号）の略記とする。

写像 $d$ は、命題に現れる連言 $\land$ と選言 $\lor$ を入れ替える写像である（定義域は $\land,\lor,\neg$ のみ）。

定義（写像 $d$）命題から命題への写像 $(-)^{d}$ は、次のように再帰的に定義される。

$$
{p}_{i}^{d}={p}_{i},
$$

Note:
ここからは形式的な定義です。言語は $\land,\lor,\neg$ に限り、$\bot$ と $\top$ は略記として扱います。原子の双対は自分自身です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 12 -->

---
## 写像$d$（続き）

$$
\left(\varphi\land\psi\right)^{d}=\left( {\varphi}^{d}\lor {\psi}^{d}\right) ,
$$

$$
\left(\varphi\lor\psi\right)^{d}=\left( {\varphi}^{d}\land {\psi}^{d}\right) ,
$$

$$
\left(\neg \varphi\right)^{d}=\neg \left( {\varphi}^{d}\right) .
$$

Note:
連言の双対は選言、選言の双対は連言、否定の双対は否定を外に残す、という再帰です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 12 -->

---
<!-- .slide: class="duality-detail" style="font-size: 32px;" -->

## 双対性定理

定理（双対性定理）

$$
\varphi\approx\psi\Longleftrightarrow{\varphi}^{d}\approx {\psi}^{d}
$$

$\varphi\approx\psi$ と ${\varphi}^{d}\approx {\psi}^{d}$ とは必要十分である。

注意）$\Longleftrightarrow$ は対象言語（命題論理）の結合子ではなく、二つの主張が同値であることを表すメタ言語（日本語）の記号。

Note:
双対性定理は、意味論的等価性が双対をとっても保たれる（かつ逆も成り立つ）ことを主張します。矢印 $\Longleftrightarrow$ はメタ言語の同値です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 13 -->

---
## 証明の準備　写像$*$

定義（写像$*$）命題から命題への写像

$$
(-)^{*}:PROP\to PROP
$$

は以下のように再帰的に定義される。

$$
{p}_{i}^{*}=\neg {p}_{i},
$$

Note:
証明のため、原子に否定を付けてから $\land$ と $\lor$ を入れ替える写像 $*$ を導入します。van Dalen の定義と同じです。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 14 -->

---
## 証明の準備　写像$*$（続き）

$$
\left(\varphi\land\psi\right)^{*}=\left( {\varphi}^{*}\lor {\psi}^{*}\right) ,
$$

$$
\left(\varphi\lor\psi\right)^{*}=\left( {\varphi}^{*}\land {\psi}^{*}\right) ,
$$

$$
\left(\neg \varphi\right)^{*}=\neg \left( {\varphi}^{*}\right) .
$$

Note:
$*$ は原子で否定を付け、結合子では $d$ と同様に $\land$ と $\lor$ を入れ替えます。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 14 -->

---
<!-- .slide: class="duality-detail" style="font-size: 28px;" -->

## 証明の準備　補題

補題.　${\varphi}^{*}\approx \neg \varphi$

証明. 命題 $\varphi$ の構造に関する帰納法により証明する。

$\varphi={p}_{i}$ のとき、${p}_{i}^{*}=\neg {p}_{i}$ であるから明らか。

$\varphi=\left( {\varphi}_{1}\land {\varphi}_{2}\right)$ のとき、定義より、

$$
\left( {\varphi}_{1}\land {\varphi}_{2}\right) ^{*}={{\varphi}_{1}}^{*}\lor {{\varphi}_{2}}^{*}
$$

帰納法の仮定 ${{\varphi}_{1}}^{*}\approx \left( \neg {\varphi}_{1}\right)$、 ${{\varphi}_{2}}^{*}\approx \left( \neg {\varphi}_{2}\right)$ と代入補題により、

$$
\left( {\varphi}_{1}\land {\varphi}_{2}\right) ^{*}\approx \left( \neg {\varphi}_{1}\right) \lor \left( \neg {\varphi}_{2}\right) \approx \neg \left( {\varphi}_{1}\land {\varphi}_{2}\right)
$$

Note:
補題 ${\varphi}^{*}\approx\neg\varphi$ を構造帰納法で示します。原子と連言の場合です。ド・モルガンの法則を使います。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 15 -->

---
<!-- .slide: class="duality-detail" style="font-size: 28px;" -->

## 証明の準備　補題（続き）

$\varphi=\left( {\varphi}_{1}\lor {\varphi}_{2}\right)$ のとき、定義より、

$$
\left( {\varphi}_{1}\lor {\varphi}_{2}\right) ^{*}={{\varphi}_{1}}^{*}\land {{\varphi}_{2}}^{*}
$$

帰納法の仮定と代入補題により、

$$
\left( {\varphi}_{1}\lor {\varphi}_{2}\right) ^{*}\approx \left( \neg {\varphi}_{1}\right) \land \left( \neg {\varphi}_{2}\right) \approx \neg \left( {\varphi}_{1}\lor {\varphi}_{2}\right)
$$

Note:
選言の場合も、帰納法の仮定とド・モルガンの法則で $\neg\varphi$ に帰着できます。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 16 -->

---
<!-- .slide: class="duality-detail" style="font-size: 28px;" -->

## 証明の準備　補題（続き）

$\varphi = \neg \varphi'$ のとき、定義より $\left( \neg {\varphi}'\right) ^{*}=\neg\left( ({\varphi}')^{*}\right)$ である。

帰納法の仮定 $({\varphi}')^{*}\approx \neg {\varphi}'$ より

$$
{\varphi}^{*}\approx \left( \neg \varphi'\right) ^{*}\approx \neg\left( ({\varphi}')^{*}\right) \approx \neg(\neg \varphi')\approx \neg \varphi.
$$

証明終

Note:
否定の場合は、帰納法の仮定に外側の否定を付け、二重否定を外して終わります。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 17 -->

---
<!-- .slide: class="duality-detail" style="font-size: 32px;" -->

## 補題

補題.　${\sigma}_{1}$ と ${\sigma}_{2}$ を命題とする。

${\sigma}_{1}$ において、現れる命題記号の前に否定 $\neg$ を付けたものを ${\sigma}_{1}'$ とし、

${\sigma}_{2}$ において、現れる命題記号の前に否定 $\neg$ を付けたものを ${\sigma}_{2}'$ とする。

このとき、${\sigma}_{1}\approx {\sigma}_{2}$ と ${\sigma}_{1}'\approx {\sigma}_{2}'$ とは必要十分である。

付値 $v$ に対し、原子を反転した付値 $\overline{v}$（$\overline{v}(p_i)=1-v(p_i)$）を考えると、この対応は付値全体の上で全単射です（講義10の付値の記法を参照）。

Note:
各原子の前に否定を付けた命題の等価性は、付値の真偽を反転する操作が全単射であることから従います。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 18 -->

---
<!-- .slide: class="duality-detail" style="font-size: 30px;" -->

## 双対性定理の証明

${\varphi}^{*}$ に現れるすべての命題記号の前に否定 $\neg$ を付けたものを $({\varphi}^{*})'$ と書くと、

$$
({\varphi}^{*})'\approx {\varphi}^{d}
$$

（同様に $({\psi}^{*})'\approx {\psi}^{d}$）。

よって次の鎖が成り立つ。

$$
\varphi\approx\psi
\Longrightarrow {\varphi}^{*}\approx {\psi}^{*}
\Longrightarrow ({\varphi}^{*})'\approx({\psi}^{*})'
\Longrightarrow {\varphi}^{d}\approx {\psi}^{d}
$$

逆方向も同様である。したがって前の二つの補題により、$\varphi \approx  \psi$ と ${\varphi}^{d}\approx {\psi}^{d}$ とは必要十分である。

証明終

Note:
まず $({\varphi}^{*})'\approx{\varphi}^{d}$ に注意し、補題1（$*$）と補題2（原子への否定）をつなげると双対性定理が得られます。逆も同じ議論です。
<!-- 原資料: 15-古典命題論理の双対性.pptx / スライド 19 -->
