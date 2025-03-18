# MeloTTS-Japanese テキスト→音声変換アプリ

[MeloTTS-Japanese](https://huggingface.co/myshell-ai/MeloTTS-Japanese) モデルを使用して、日本語のテキストファイルをアップロードすると、自然な音声に変換するJupyter Notebookアプリです。

## 機能

- 日本語テキストファイル(.txt)のアップロード
- 複数のエンコーディング形式に対応 (UTF-8, Shift-JIS, EUC-JP, ISO-2022-JP)
- テキストのプレビュー表示
- 発話速度の調整 (0.5倍～2.0倍)
- 音声のブラウザ内再生
- 変換した音声ファイルのダウンロード

## インストールと利用方法

このリポジトリには2つのバージョンのアプリケーションが含まれています：

### 1. GitHubリポジトリからのインストール（推奨）

```bash
# リポジトリをクローン
git clone https://github.com/ShunsukeTamura06/melotts-japanese-converter.git
cd melotts-japanese-converter

# 必要なライブラリをインストール
pip install -r requirements.txt
```

使用方法:

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

### 2. Hugging Faceからのモデル利用（実験的）

このバージョンでは、Hugging Faceから直接モデルファイルをダウンロードして利用します。

使用方法:

1. Jupyter Notebookを起動

```bash
jupyter notebook
```

2. `melotts_japanese_huggingface.ipynb` を開く

3. セルを順番に実行

注意: Hugging Face版は実験的な実装です。MeloTTSの内部実装へのアクセスが制限されているため、現時点では完全な機能を実現できない可能性があります。本格的な利用には、GitHubリポジトリからのインストール版を推奨します。

## 注意点

- 初回実行時はモデルのダウンロードに時間がかかることがあります
- 長いテキストの処理には時間がかかることがあります
- GPUがある環境では、`device='cuda:0'`に設定することで処理を高速化できます

## Hugging Faceモデルについて

MeloTTS-Japaneseは[Hugging Face](https://huggingface.co/myshell-ai/MeloTTS-Japanese)上でホストされていますが、モデルの利用には一般的にMeloTTSライブラリを使用することが推奨されています。これは、モデルの読み込みや推論処理が特殊なためです。

## ライセンス

MIT License

## クレジット

このアプリは[MyShell.ai](https://myshell.ai)および[MIT](https://www.mit.edu/)によって開発された[MeloTTS](https://github.com/myshell-ai/MeloTTS)を使用しています。