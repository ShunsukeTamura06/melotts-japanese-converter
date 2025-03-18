# MeloTTS-Japanese テキスト→音声変換アプリ

[MeloTTS-Japanese](https://huggingface.co/myshell-ai/MeloTTS-Japanese) モデルを使用して、日本語のテキストファイルをアップロードすると、自然な音声に変換するJupyter Notebookアプリです。

## 機能

- 日本語テキストファイル(.txt)のアップロード
- 複数のエンコーディング形式に対応 (UTF-8, Shift-JIS, EUC-JP, ISO-2022-JP)
- テキストのプレビュー表示
- 発話速度の調整 (0.5倍～2.0倍)
- 音声のブラウザ内再生
- 変換した音声ファイルのダウンロード

## インストール方法

```bash
# リポジトリをクローン
git clone https://github.com/ShunsukeTamura06/melotts-japanese-converter.git
cd melotts-japanese-converter

# 必要なライブラリをインストール
pip install -r requirements.txt
```

## 使用方法

1. Jupyter Notebookを起動

```bash
jupyter notebook
```

2. `melotts_japanese_converter.ipynb` を開く

3. 最初のセルを実行して、MeloTTSとunidicをインストール

```python
!pip install git+https://github.com/myshell-ai/MeloTTS.git
!python -m unidic download
```

4. 次のセルを実行してアプリを起動

5. 「テキストファイルを選択」ボタンをクリックして日本語のテキストファイルをアップロード

6. 必要に応じて発話速度を調整

7. 変換された音声を再生、またはダウンロード

## 注意点

- 初回実行時はモデルのダウンロードに時間がかかることがあります
- 長いテキストの処理には時間がかかることがあります
- GPUがある環境では、`device='cuda:0'`に設定することで処理を高速化できます

## ライセンス

MIT License

## クレジット

このアプリは[MyShell.ai](https://myshell.ai)および[MIT](https://www.mit.edu/)によって開発された[MeloTTS](https://github.com/myshell-ai/MeloTTS)を使用しています。