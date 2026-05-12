# PyRIT Red Teaming Hands-on

初心者向けに、PyRIT を使った生成 AI Red Teaming の基本を体験するためのスターター教材です。

この教材は参加者が Azure アカウントを持たない前提で作っています。講師が OpenAI 互換のモデルエンドポイント、API キー、モデル名またはデプロイ名を参加者へ一時的に共有し、参加者は GitHub Codespaces またはローカル Python 環境で Notebook を実行します。

## 目標

- AI Red Teaming の考え方を安全な題材で理解する
- PyRIT の Target、Converter、Attack、Scorer の役割を知る
- 簡単なプロンプト変換や拒否判定を試す
- 結果を人間がレビューする重要性を理解する

## 対象者

- 生成 AI セキュリティや Red Teaming が初めての方
- Python Notebook を少し触れる方
- Azure の操作やリソース作成は避けたいハンズオン参加者

## 参加者に必要なもの

- GitHub アカウント
- GitHub Codespaces、または Python 3.12 が動くローカル環境
- 講師から配布される一時的な `OPENAI_CHAT_*` 設定値

## はじめ方

迷ったら、まず Workshop Guide の `Begin Here` から進めてください。

[![Workshop Guide](https://img.shields.io/badge/Workshop_Guide-Begin_Here-0F6CBD?style=for-the-badge)](docs/index.md)
[![Fork this repository](https://img.shields.io/badge/Fork-this%20repository-181717?style=for-the-badge&logo=github)](https://github.com/mrmo-sandbox/pyrit-red-teaming-handson/fork)
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/mrmo-sandbox/pyrit-red-teaming-handson?quickstart=1)

おすすめの進め方は次の通りです。

1. [このリポジトリを Fork](https://github.com/mrmo-sandbox/pyrit-red-teaming-handson/fork) して、自分用のコピーを作ります。
2. Fork したリポジトリを GitHub Codespaces で開きます。
3. [Workshop Guide](docs/index.md) を開き、`Begin Here` のセットアップ手順に沿って進めます。

## ローカルで動かす場合

```bash
cp .env.sample .env
python -m pip install -r requirements.txt
mkdocs serve
```

`.env` には講師から共有された値を設定します。

```bash
OPENAI_CHAT_ENDPOINT="https://example.openai.azure.com/openai/v1"
OPENAI_CHAT_KEY="YOUR_TEMPORARY_KEY"
OPENAI_CHAT_MODEL="YOUR_MODEL_OR_DEPLOYMENT"
```

その後、ブラウザーで表示された Workshop Guide を開き、`Begin Here` から進めてください。詳細は [Setup](docs/begin-here/00-setup.md) を参照してください。

## Labs

| Lab | 内容 |
| --- | --- |
| Lab 0 | モデルエンドポイント接続確認 |
| Lab 1 | PyRIT の基本構成を体験 |
| Lab 2 | 安全なプロンプト注入シナリオと Converter |
| Lab 3 | 拒否判定と結果レビュー |

## 講師向けメモ

- 共有キーはイベント専用、短時間有効、低クォータにしてください。
- 終了後は必ずキーをローテーションまたは無効化してください。
- 本教材は安全な架空シナリオだけを扱います。実在システムや許可されていない対象へのテストには使わないでください。
