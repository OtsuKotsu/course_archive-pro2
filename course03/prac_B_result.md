## Q.3-7
### explanation
```stdout
(1) x = 1
(2) x = 1
(3) x = 3
(4) p = (0, 0)
(5) p = (2, 0)
(6) p = (2, 0)
(7) a[0] = 4
    a[1] = 3
```
- 1行目は基本型であるint型の変数がそのまま出力される。
- 2行目は`change1()`に`x`を渡してその中でインクリメ
  ントしているが、この変数は基本型なのでコピーが渡さ
  れており、`change1()`内部での変更はコピーされた変
  数に対してのみ行われ、その変更は`main`内部の`x`には
  影響をあたえない。よって`1`が出力される。
- 3行目は`main`内の`x`に、`change2()`の返り値が代入
  されるので`1+2`の結果`3`が出力される。
- 4行目はpのインスタンス変数が0に初期化されて出力されている。
- 5行目は`MyPoint`が参照型なので、`changePoint1()`には
  参照のコピーが渡される。よって、関数内部での変更は`main`内の
  `p`が参照しているMyPointオブジェクトへ反映される。よって
  `changePoint1()`での変更を反映した`(2, 0)`が出力される。
- 6行目は`changePoint2()`に渡されたpへの参照のコピーに
  新しいオブジェクトを割り当ててそこに対して変更を行っている。
  そのため、`main`内部の`p`が参照しているオブジェクトへの
  変更は行われず、そのまま`(2, 0)`が出力される。
- 7行目は参照型である配列の要素に対して変更を加えている。
  `changeArray1()`には参照のコピーが渡されるので
  `changeArray1()`での代入は`main`内の`a`が参照している
  配列のオブジェクトへ反映される。よって上記のように出力される。


## Q.3-8
### result
```stdout
16.1245154965971
```


## Q.3-10
### result
```stdout
count = 0
a: false
e: true
i: true
o: false
count = 3
a: false
e: false
i: true
o: false
count = 2
k: false
e: false
i: true
a: true
l: true
m: true
count = 4
```
