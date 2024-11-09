# 株価予測モデル構築 README

## 目次
- [フォルダ構成](#フォルダ構成)
- [ファイルについて](各ファイルについて)
- [実行手順](#実行手順)

## フォルダ構成
```
time_series
├── data
│    ├── data_submission_before.ipynb
│    ├── data_submission_feature_chose.ipynb
├── model
│    ├── model_lstm.ipynb
│    ├── model_xgboost.ipynb
```

## ファイルについて
#### 1. `time_series/data.ipynb`
#### 概要
- データ理解
  - データの型確認
  - トレンド性・季節性の確認
  - 異常値の確認
- 特徴量エンジニアリング(EDA)の実施
- モデル学習・テスト用データ生成

#### 2. `time_series/model_lightgbm.ipynb`
#### 概要
- LightGBMを用いた株価予測
  - Optuna適用前
  - Optuna適用後

#### 3. `time_series/model_lstm.ipynb`
- LSTMを用いた株価予測

#### 4. `time_series/model_xgboost.ipynb`
- XGBoostを用いた株価予測
  - Optuna適用前
  - Optuna適用後

## 実行手順
1. `data/data_submission_before.ipynb`を上のセルから実行し、csvファイルを生成する。
※ インポートされているライブラリは各自でインストールを行うこと
2. `data/data_submission_feature_chose.ipynb`を上のセルから実行し、csvファイルを生成する。
3. 1. 2. で生成したcsvファイルを`model/model_letm.ipynb`、または`model/model_xgboost.ipynb`を実行する。