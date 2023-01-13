# Aerial Drone Imageを用いたセグメンテーション
このレポジトリではオープンデータ「[Semantic Drone Dataset](https://www.kaggle.com/datasets/bulentsiyah/semantic-drone-dataset)」を用いたセマンティック・セグメンテーションのモデルを公開している。
かつ、そのモデルをベースにファインチューニングを行うソースコードや、モデルの推論を高速化するテクニックなども紹介している。
開発環境としてGoogle Colaboratoryを前提としている。
## 必要条件
- Google Colaboratoryが動作可能なマシン
- Googleアカウント
## 各ノートブックの内容
### TrainModel.ipynb
説明
### Test_PreTrainModel.ipynb
[事前学習済みのモデル](https://drive.google.com/file/d/14PtYuFZc-5sB2n9lLUDku8bgyEKSLZG5/view?usp=share_link)を用いて対象データに対してのセグメンテーションを実施する
### Fine-Tuning.ipynb
[事前学習済みのモデル](https://drive.google.com/file/d/14PtYuFZc-5sB2n9lLUDku8bgyEKSLZG5/view?usp=share_link)をベースとして、カスタム画像データを用いてFine-Tuning(転移学習)を行う
### Test_CustumModel.ipynb
[Fine-Tuningを行ったモデル](https://drive.google.com/file/d/1JXPHg4brau1T93z79VNr4VqLeCEx2CcW/view?usp=share_link)を用いて対象画像データに対してのセグメンテーションを実施する
### Model_Optimization_and_Quantization.ipynb
モデルの推論をCPU上で高速化するためのテクニック集
## 実行方法
ノートブックのパス設定を任意のパスに書き換えてノートブック上部から実行
- IMAGE_PATH, MASK_PATH セグメンテーション対象データの入力画像とアノテーション画像のファイルパス
- MODEL_PATH　事前学習済みのモデルを保存しているファイルパス
- SAVE_PATH　セグメンテーションの結果 or Fine-Tuningを行ったモデルを保存するフォルダパス
## Licence / ライセンス
このプロジェクトは Apache 2.0の元にライセンスされています
