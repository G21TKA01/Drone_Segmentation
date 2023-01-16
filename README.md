# Aerial Drone Imageを用いたセグメンテーション
このレポジトリではオープンデータ「[Semantic Drone Dataset](https://www.kaggle.com/datasets/bulentsiyah/semantic-drone-dataset)」を用いたセマンティック・セグメンテーションのモデルを公開している。
かつ、そのモデルをベースにファインチューニングを行うソースコードや、モデルの推論を高速化するテクニックなども紹介している。
開発環境としてGoogle Colaboratoryを前提としている。
## オープンデータのクラス
オープンデータ「Semantic Drone Dataset」は24Classから構成されるデータセットでアノテーションとクラスの対応は以下のとおりである。
|id|クラス名|RGB値|
|-|-|-|
|0|ラベルなし|0, 0, 0|
|1|道路|128, 64, 128|
|2|土壌|130, 76, 0|
|3|草原|0, 102, 0|
|4|砂利|112, 103, 87|
|5|水|28, 42, 168|
|6|岩|48, 41, 30|
|7|プール|0, 50, 89|
|8|草木|107, 142, 35|
|9|屋根|70, 70, 70|
|10|壁|102, 102, 156|
|11|窓|254, 228, 12|
|12|ドア|254, 148, 12|
|13|フェンス|190, 153, 153|
|14|フェンス支柱|153, 153, 153|
|15|人|255, 22, 96|
|16|犬|102, 51, 0|
|17|車|9, 143, 150|
|18|自転車|119, 11, 32|
|19|木|51, 51, 0|
|20|枯れ木|190, 250, 190|
|21|arマーカー|112, 150, 146|
|22|障害|2, 135, 115|
|23|衝突|255, 0, 0|

## 必要条件
- Google Colaboratoryが動作可能なマシン
- Googleアカウント
## 各ノートブックの内容
### TrainModel.ipynb
[Semantic Drone Dataset](https://www.kaggle.com/datasets/bulentsiyah/semantic-drone-dataset)」を用いた学習
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
