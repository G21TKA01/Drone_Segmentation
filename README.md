# Aerial Drone Imageを用いたセグメンテーション
Google Colaboratoryを用いて事前学習を行ったモデルをもとにFine-Tuningを行い、自身の適用したいデータセットに対してセグメンテーションを行う  
[事前学習に用いたデータセット](https://www.kaggle.com/datasets/bulentsiyah/semantic-drone-dataset)

## 必要条件
- Google Colaboratoryが動作可能なマシン  
- Googleアカウント

## 各ノートブックの内容
### Test_PreTrainModel.ipynb
事前学習済みのモデルを用いて対象データに対してのセグメンテーション
### Fine-Tuning.ipynb
事前学習済みのモデルを基に対象データでFine-Tuning(再度学習)を行う
### Test_FuehukiModel.ipynb
Fine-Tuningを行ったモデルを用いて対象データに対してのセグメンテーション

## 実行方法
ノートブックのパス設定を任意のパスに書き換えてノートブック上部から実行
- IMAGE_PATH, MASK_PATH セグメンテーション対象データの入力画像とアノテーション画像のファイルパス
- MODEL_PATH　事前学習済みのモデルを保存しているファイルパス
- SAVE_PATH　セグメンテーションの結果 or Fine-Tuningを行ったモデルを保存するフォルダパス

## Licence / ライセンス
このプロジェクトは Apache 2.0の元にライセンスされています
