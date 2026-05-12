# Setup

## 1. Codespaces を開く

GitHub のリポジトリ画面で **Code** → **Codespaces** → **Create codespace** を選びます。

ローカルで実行する場合は Python 3.12 の仮想環境を作成してください。

## 2. 依存関係をインストールする

Codespaces では自動インストールされます。手動で実行する場合は次のコマンドを使います。

```bash
python -m pip install -r requirements.txt
```

## 3. `.env` を作成する

```bash
cp .env.sample .env
```

`.env` を開き、講師から共有された値を設定します。

```bash
OPENAI_CHAT_ENDPOINT="https://YOUR_RESOURCE.openai.azure.com/openai/v1"
OPENAI_CHAT_KEY="YOUR_TEMPORARY_KEY"
OPENAI_CHAT_MODEL="YOUR_MODEL_OR_DEPLOYMENT"
```

## 4. Workshop Guide を起動する

```bash
mkdocs serve
```

ブラウザーで表示された URL を開きます。

## 5. Notebook を開く

VS Code の Explorer から `labs/` フォルダーを開き、`0-validate-endpoint.ipynb` から順番に実行します。

!!! tip "Notebook の実行"
    Kernel は `Python (PyRIT Hands-on)` または Python 3.12 の環境を選択します。

