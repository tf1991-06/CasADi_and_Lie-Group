# PythonとCasADiで学ぶLie群上の最適化

ロボットやドローンの姿勢（回転）を変数とする最適化問題を、Python と [CasADi](https://web.casadi.org/) で解くためのチュートリアル・ノートブックです。Lie群・Lie代数の基本から、自動微分、数値積分、最適化までを、実行できるコードと図で順に学びます。

**[casadi_lie_group_optimization.ipynb](casadi_lie_group_optimization.ipynb)**（GitHub 上でそのまま閲覧できます。実行結果と図も保存されています）

## 内容

| 章 | テーマ | 主な内容 |
| --- | --- | --- |
| 0 | Lie群とは何か | 群、Lie群、Lie代数、指数写像と対数写像 |
| 1 | SO(2) | 円周としてのLie群、指数写像のイメージ |
| 2 | SO(3) | hat / vee、Rodrigues の公式、対数写像の CasADi 実装 |
| 3 | Lie括弧と非可換性 | 回転の順序、BCH 公式 |
| 4 | 自動微分 | 摂動による「Lie群上の微分」、右ヤコビアン |
| 5 | 数値積分 | オイラー法・RK4 と Lie群積分の比較 |
| 6 | SE(2)・SE(3) | 位置と姿勢の指数写像・対数写像、姿勢の補間 |
| 7 | Lie群上の最適化 | 回転の推定（Gauss–Newton法）、SE(2) 上の軌道最適化（`Opti`） |

## 動かし方

### ローカル環境

```bash
pip install -r requirements.txt
jupyter lab casadi_lie_group_optimization.ipynb
```

動作確認は Python 3.11 / CasADi 3.7.0 / NumPy 2.2 / Matplotlib 3.10 で行いました。

### Google Colab

Colab には CasADi が入っていないため、ノートブック冒頭のセルにある `# !pip install casadi` の `#` を外してから実行してください。
