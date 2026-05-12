# Setup

## 1. リポジトリを Fork する

自分用のコピーを作るため、まずリポジトリを Fork します。

[このリポジトリを Fork](https://github.com/mrmo-sandbox/pyrit-red-teaming-handson/fork){ .md-button .md-button--primary }

Fork が作成されたら、Fork 先のリポジトリ画面を開きます。

## 2. Codespaces を開く

Fork 先の GitHub リポジトリ画面で **Code** → **Codespaces** → **Create codespace** を選びます。

[Codespaces で開く](https://codespaces.new/mrmo-sandbox/pyrit-red-teaming-handson?quickstart=1){ .md-button .md-button--primary }

!!! note "Fork 先で開く場合"
    上のボタンはこのリポジトリを直接 Codespaces で開きます。Fork したリポジトリで作業する場合は、Fork 先のリポジトリ画面から **Code** → **Codespaces** → **Create codespace** を選んでください。

ローカルで実行する場合は Python 3.12 の仮想環境を作成してください。

## 3. 依存関係をインストールする

Codespaces では自動インストールされます。手動で実行する場合は次のコマンドを使います。

```bash
python -m pip install -r requirements.txt
```

## 4. `.env` を作成する

```bash
cp .env.sample .env
```

`.env` を開き、講師から共有された値を設定します。

```bash
OPENAI_CHAT_ENDPOINT="https://YOUR_RESOURCE.openai.azure.com/openai/v1"
OPENAI_CHAT_KEY="YOUR_TEMPORARY_KEY"
OPENAI_CHAT_MODEL="YOUR_MODEL_OR_DEPLOYMENT"
```

## 5. Workshop Guide を起動する

```bash
mkdocs serve
```

ブラウザーで表示された URL を開きます。

## 6. Notebook を開く

VS Code の Explorer から `labs/` フォルダーを開き、`0-validate-endpoint.ipynb` から順番に実行します。

!!! tip "Notebook の実行"
    Kernel は `Python (PyRIT Hands-on)` または Python 3.12 の環境を選択します。
