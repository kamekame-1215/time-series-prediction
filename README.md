# 株価予測モデル構築 README

## 目次
- [はじめに](#はじめに)
- [フォルダ構成](#フォルダ構成)
- [各ファイルについて](#各ファイルについて)
- [実行手順](#実行手順)

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
├── data
│    ├── data_submission_before.ipynb
│    ├── data_submission_feature_chose.ipynb
├── model
│    ├── model_lstm.ipynb
│    ├── model_xgboost.ipynb
```

## ファイルについて
#### 1. `data/data_creation.ipynb`
#### 概要
- 株価データ取得
- 取得したデータの理解
- 特徴量エンジニアリング(EDA)の実施
- モデル学習・テスト用データ生成(csvデータ)

#### 2. `data/data_submission_feature_chose.ipynb`
#### 概要 
- モデルに入力する特徴の選択

#### 3. `time_series/model_lstm.ipynb`
- LSTMを用いた株価予測

#### 4. `time_series/model_xgboost.ipynb`
- XGBoostを用いた株価予測
  - Optuna適用前
  - Optuna適用後

## 実行手順
1. `data/data_creation.ipynb`を上のセルから実行し、csvファイルを生成する。  
※ インポートされているライブラリは各自でインストールを行うこと  
2. `data/data_submission_feature_chose.ipynb`を上のセルから実行し、csvファイルを生成する。
3. 生成したcsvファイルを用いて、`model/model_letm.ipynb`または`model/model_xgboost.ipynb`を実行する。