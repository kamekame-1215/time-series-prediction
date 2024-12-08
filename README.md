# 株価予測モデル構築 README

## 目次
- [はじめに](#はじめに)
- [フォルダ構成](#フォルダ構成)
- [ファイルについて](#ファイルについて)

## はじめに
本リポジトリでは、**長期投資**を想定した株価予測モデル構築を行う。  
株価データは、任天堂のデータを用いる。  
任天堂のデータは、Pythonを用いて、stooqから抽出する。  
本リポジトリの詳細は、下記やコードを参照すること。

**注意**  
本リポジトリは、自己学習を目的として作成したものであるため、内容の信頼性はないことに注意する。

## フォルダ構成
```
time-series-prediction
├── letm.ipynb
```

## ファイルについて
#### 1. `time_series/lstm.ipynb`
- 株価データの取得
- データの可視化
- データの正規化
- LSTMを用いた株価予測
- 予測結果の可視化