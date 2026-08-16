## コマンド一覧

| コマンド | 説明 |
| --- | --- |
| `npx qiita init` | `.gitignore` / ワークフローファイル / `qiita.config.json` を生成 |
| `npx qiita login` | トークンを登録して Qiita アカウントと紐付け |
| `npx qiita preview` | ブラウザでプレビュー（http://localhost:8888）。実行時に投稿済み記事をDL |
| `npx qiita new ベース名` | 新規記事作成（ベース名がファイル名になる） |
| `npx qiita publish ベース名` | 指定した記事を投稿・更新 |
| `npx qiita publish --all` | 全記事をまとめて投稿・更新 |
| `npx qiita publish ベース名 --force` | 強制的にファイル内容を反映（`-f` も可） |
| `npx qiita pull` | Qiita 側の更新を手元に同期（手元未変更の記事のみ） |
| `npx qiita pull --force` | 強制的に Qiita の内容をファイルへ反映（`-f` も可） |
| `npx qiita posting-campaigns` | 開催中の投稿キャンペーン一覧（最大100件） |
| `npx qiita version` | バージョン確認 |
| `npx qiita help` | ヘルプ表示 |

※ 記事の**削除コマンドはなし**。`public/` から `.md` を消しても Qiita 上では消えない。削除は Qiita 上で行う。

## 共通オプション

| オプション | 説明 |
| --- | --- |
| `--credential <dir>` | 認証情報 `credentials.json` の置き場所。デフォルト `$HOME/.config/qiita-cli` |
| `--config <dir>` | `qiita.config.json` の置き場所。デフォルトはカレントディレクトリ |
| `--root <dir>` | 記事ファイルのDL先。デフォルトはカレントディレクトリ |
| `--verbose` | 詳細ログを出力 |

## frontmatter（記事冒頭の設定）

| 項目 | 説明 |
| --- | --- |
| `title` | 記事タイトル |
| `tags` | タグ。**最低1つ必須**（空だと投稿時にエラー） |
| `private` | `true`: 限定共有記事 / `false`: 公開記事 |
| `updated_at` | 投稿時に自動で更新日時が入る |
| `id` | 投稿時に自動で記事のUUIDが入る |
| `organization_url_name` | 関連付ける Organization の URL 名 |
| `slide` | `true`: スライドモードON / `false`: OFF |
| `ignorePublish` | `true`: publish で無視され投稿されない / `false`: 投稿される |
| `posting_campaign_uuid` | 紐付けるキャンペーンのUUID |
| `agreed_posting_campaign_term` | `true`: キャンペーン規約に同意（UUID指定時は必須） |

## qiita.config.json の設定

| 項目 | 説明 | デフォルト |
| --- | --- | --- |
| `includePrivate` | DL する記事に限定共有記事を含めるか | `false` |
| `host` | preview で使うホスト | `localhost` |
| `port` | preview で使うポート | `8888` |