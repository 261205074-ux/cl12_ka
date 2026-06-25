# 左右反転画像生成プログラム

## 1. 概要

引数で指定した画像の左右反転画像を作成する Python 3 で動作するプログラムです。

## 2. ソースコード

```python

*# このプログラムは python3 用です。*

*# あらかじめ pip install pillow で pillow をインストールしておきます。*



from PIL import Image

import sys



*# コマンドライン引数から入力画像と出力画像のファイル名を取得*

input\\\_image = sys.argv\\\[1]

output\\\_image = sys.argv\\\[2]



*# 画像の読み込み*

img = Image.open(input\\\_image)



*# 画像の左右反転*

img\\\_flip = img.transpose(Image.FLIP\\\_LEFT\\\_RIGHT)



*# 画像の保存*

img\\\_flip.save(output\\\_image)

```

## 3. 使い方

### 3.1 実行例

- コマンドラインフォーマット

```bash

python3 flip.py <input\\\_image\\\_path> <output\\\_image\\\_path>

```

- 利用例

```bash

python3 flip.py input.jpg output.jpg

```

### 3.2 出力結果

以下のように入力画像の左右反転画像が出力されます。

| 入力画像 (input.jpg) | 出力画像 (output.jpg) |
|----------------------|----------------------|
| ![元画像](./input.jpg) | ![左右反転画像](./output.jpg) |
