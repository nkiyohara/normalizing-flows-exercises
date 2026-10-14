# 正規化フローによる変分推論：演習

距離センサーの観測から物体の位置を推定し、事後分布を**対角ガウス・全共分散ガウス・カップリングフロー**で近似して比較する、日本語の演習ノートブックです。

## Google Colabで開く

| ノートブック | 内容 | Colab |
| --- | --- | --- |
| [exercise.ipynb](exercise.ipynb) | `TODO` を埋めて取り組む演習 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nkiyohara/normalizing-flows-exercises/blob/main/exercise.ipynb) |
| [exercise_solution.ipynb](exercise_solution.ipynb) | 解答を記入済みのノートブック | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nkiyohara/normalizing-flows-exercises/blob/main/exercise_solution.ipynb) |

## 使い方

1. 上の **Open in Colab** ボタンを押して、Googleアカウントでログインします。
2. 編集内容を保存する場合は、Colabの **「ファイル」→「ドライブにコピーを保存」** で自分のGoogle Driveにコピーします。
3. Python 3のCPUランタイムに接続し、上から順にセルを実行します。GPUは不要です。このコードはCPUで計算します。
4. 演習版では、該当するセルを実行する前に `TODO 1`〜`TODO 4` の `...` を埋めてください。未記入のまま実行するとエラーになります。
5. 解答版は上から順に実行できます。学習には時間がかかります。

外部データのダウンロードやGoogle Driveのマウントは不要です。各自のコピーで編集・実行するため、配布元のノートブックは変更されません。

使用ライブラリは PyTorch・Matplotlib・tqdm です。インポート時に `ModuleNotFoundError` が出た場合は、先頭にコードセルを追加して次を実行してください。

```python
%pip install torch matplotlib tqdm
```

## 演習の内容

- **TODO 1**：アフィンカップリング層の変換と対数ヤコビアン行列式
- **TODO 2**：複数の層を合成したときの対数ヤコビアン行列式
- **TODO 3**：順写像を使った変分分布の対数密度とELBO
- **TODO 4**：逆写像を使った密度の評価

センサーが1つの場合の曲がった事後分布と、2つの場合の二峰性の事後分布を扱います。最後に `init_mu` と `init_sigma` を変え、初期値によって近似や学習結果がどう変わるかを観察します。
