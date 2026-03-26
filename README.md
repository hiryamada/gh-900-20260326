# gh-900-20260326

FastAPI を使用した Hello World API のサンプルプロジェクトです。
テスト書き換え.

#1 の作業が必要。

## 概要

`GET /` エンドポイントにアクセスすると `{"message": "Hello World"}` を返す REST API です。

## ディレクトリ構成

```
.
├── src/
│   └── main.py        # FastAPI アプリケーション本体
├── tests/
│   └── test_main.py   # pytest 単体テスト
├── requirements.txt   # 依存ライブラリ
└── README.md
```

## セットアップ

```bash
pip install -r requirements.txt
```

## サーバーの起動

```bash
uvicorn src.main:app --reload
```

起動後、ブラウザで `http://localhost:8000/` にアクセスするか、以下のコマンドで動作確認できます。

```bash
curl http://localhost:8000/
# -> {"message":"Hello World"}
```

## テストの実行

```bash
pytest tests/ -v
```
