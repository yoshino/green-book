# データ解析のための統計モデリング入門
本で紹介されているRのコードをPythonで実装しました。

本の中で利用しているデータは[著者である久保拓弥先生のサイト](https://kuboweb.github.io/-kubo/ce/IwanamiBook.html)から取得しています。

![green-book](https://user-images.githubusercontent.com/17586662/216754540-faa10541-72ec-4b30-9856-a6b6be607a90.jpg)

## 統計モデリングの全体の流れ
最尤推定法からMCMCを利用したベイズモデルまでの考え方をわかりやすく紹介されていますが、ＭＣＭＣの理論的背景には深く説明がなされていないため、[ゼロからできるＭＣＭＣ](https://github.com/yoshino/mcmc-from-zero)などを参考にすると良いかもしれません。
- (1). 現象をグラフで表示する
- (2). この現象がどのような確率分布で説明されそうか？の仮定をおく
- (3). 現象のパラメータを求める(最尤推定)(~7章)
  - 説明変数で説明できる場合: 一般化線形モデル: GLM
    - ポアソン分布(4章)
    - 二項分布、ガンマ分布(6章)
  - 説明変数に加えて「個体差」を持ち込む場合: 一般化線形混合モデル(GLMM)
- (3'). 現象のパラメータの確率分布(p(Θ|Y)を求める: ベイズの世界(8~11章)
    - 階層ベイズモデル: GLMM(10章)
    - 個体差間で相関がある場合の階層ベイズモデル(11章)
- (4). 推定した確率分布を新しいデータに当てはめて予測して精度を観察する
