# 稜線ノート

登山装備の見直し記録を、実際に検討した一次情報に基づいて公開する比較サイト。Astroで構築し、GitHub Pagesで公開する。

## コマンド

| Command           | Action                        |
| :---------------- | :---------------------------- |
| `npm install`      | 依存関係のインストール         |
| `npm run dev`       | ローカル開発サーバー起動        |
| `npm run build`     | `./dist/` に本番ビルド出力      |
| `npm run preview`   | ビルド結果をローカルでプレビュー |

## デプロイ

`main` ブランチへのpushで GitHub Actions が自動ビルド・デプロイする（`.github/workflows/deploy.yml`）。
