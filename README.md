# python_gemini_sample

本リポジトリはシンプルな GeminiをPythonで使うためのリポジトリ鳥です
devcontainer の設定をしていますので、VS Code と Docker、Git さえあれば各種開発用設定が行われた Python の開発環境が構築され、即時開発が可能です

## 内容

- [devcontainer](https://code.visualstudio.com/docs/remote/containers)
- [uv](https://docs.astral.sh/uv/)
  - [ruff](https://beta.ruff.rs/docs/)
- [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance), [pyright](https://github.com/microsoft/pyright)
- [hadolint](https://github.com/hadolint/hadolint)
- [pytest](https://docs.pytest.org/en/stable/)
- [GitHub Actions](https://github.co.jp/features/actions)
- [logging](https://docs.python.org/ja/3/howto/logging.html)

## 環境詳細

- Python : 3.12

### 開発手順

1. VS Code 起動
2. プロジェクト直下に `.env` ファイルを空ファイルで作成
3. 左下のアイコンクリック
4. 「Dev Containers: Reopen in Container」クリック
5. しばらく待つ
   - 初回の場合コンテナー image の取得や作成が行われる
6. 起動したら開発可能
   - 初回起動時は `uv sync` を実行してください

## NOTE

- 実行
  - `uv run main.py`
- ユニットテスト
  - `uv run python -m pytest`
    - `uvx pytest` の設定もしているが、uv環境で実装されないため、上記コマンドで実行する
- lint
  - `uvx ruff check`
- format
  - `uvx ruff format`
  - `uvx ruff format --check`
