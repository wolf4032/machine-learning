# machine-learning
機械学習の一連の処理を、**実務を想定**して、自分なりに行いました。

## 概要
以下の処理を行いました。
- 探索的データ分析
- 前処理
- モデルの作成
- モデルを使った予測

以下のボタンから、Google Colabでノートブックを見ることができます。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/wolf4032/machine-learning/blob/main/001.ipynb)

[使用したデータセット](https://www.kaggle.com/competitions/playground-series-s4e11/data)

## 実務を想定した実装

実務では主に、以下の３つが求められると考えました。
- 正確性
- 軽量な計算
- 高い汎化性能

これらのバランスを意識して、探索的データ分析、前処理、モデルの作成を行いました。

### 探索的データ分析
複数の特徴量間の関係から、目的変数だけでなく、他の説明変数にどう影響しているのか、仮設を立てて分析し、各特徴量の必要性を判断しました。

### 前処理
以下の4つを行いました。
- 異常値への対処
- 欠損値の補完
- 特徴量選択
- データの変換

欠損値の補完は、単純に中央値で補完するのではなく、各サンプルの特徴に配慮して補完する値を決めました。

データの変換では、カテゴリカル変数を数値へ変換したり、サンプル数の少ないカテゴリをまとめたりしました。

特に、数値への変換は、カテゴリの順序に配慮しました。

### モデルの作成
交差検証で、ハイパーパラメータをチューニングしたのち、データセット全体で学習しました。

