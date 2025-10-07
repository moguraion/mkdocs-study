# mkdocs-study

## このリポジトリの機能

- 文章校正

  - [Vale](https://vale.sh/)(英文用)

- ローカルマシンでの MkDocs 確認

  - VSCodeのデバッグ(F5)でChromeブラウザが起動し、ドキュメントのリアルタイム表示

  - 関連設定ファイル

    - [launch.json](.vscode/launch.json)

    - [tasks.json](.vscode/tasks.json)

- gh-pages

  - タグ付けバージョンドキュメントの発行[ワークフロー](.github/workflows/build-mkdocs.yaml)

  - 指定バージョンドキュメントの削除[ワークフロー](.github/workflows/delete-mkdocs.yaml)


## mkdocsに追加している機能

- [mkdocs-static-i18n](https://github.com/ultrabug/mkdocs-static-i18n)

  - ドキュメントの多言語対応

  - 画面上部に言語選択ボックス表示

- [mike](https://github.com/jimporter/mike)

  - ドキュメントのバージョン管理

  - 画面上部にバージョン選択ボックス表示

  - gh-pagesブランチでドキュメントを管理
