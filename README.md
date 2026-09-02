# やまかなた

登山装備の見直し記録を、実際に検討した一次情報に基づいて公開する比較サイト。

「最軽量だから良い」ではなく、山での信頼性とのバランスを考えながら実際に検討した装備選びの過程を、カテゴリごとに公開しています。

**公開URL**: https://kanata3180.github.io/

## 技術構成

- [Astro](https://astro.build/) — 静的サイトジェネレーター
- GitHub Pages — ホスティング
- GitHub Actions — `main` ブランチへのpushで自動ビルド・デプロイ（[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)）

## プロジェクト構成

```text
src/
├── data/
│   ├── articles.js     # 記事のメタ情報（タイトル・カテゴリ・抜粋等）一覧
│   └── categories.js   # カテゴリ名とURLスラッグの対応
├── layouts/
│   └── BaseLayout.astro  # ヘッダー・フッター・カテゴリナビ等、全ページ共通のシェル
├── styles/
│   └── global.css        # デザイントークン・共通コンポーネントのスタイル
└── pages/
    ├── index.astro           # トップページ（検索・記事一覧・今後のトピックス）
    ├── category/[slug].astro # カテゴリ別の記事一覧（ビルド時に自動生成）
    └── *.astro               # 個別記事ページ
```

## 記事の追加方法

1. `src/pages/` に新しい記事ページ（`.astro`）を追加する。既存記事（`backpack-comparison.astro` 等）と同じ構成（`BaseLayout` に `title` / `description` / `currentCategory` を渡す形）に揃える
2. `src/data/articles.js` に記事のメタ情報を1件追加する（トップページの記事一覧・検索・該当カテゴリページに自動的に反映される）
3. 新しいカテゴリを扱う場合のみ、`src/data/categories.js` にも追加する（ヘッダーナビ・フッターに自動反映される）

## コマンド

| Command             | Action                           |
| :------------------ | :------------------------------- |
| `npm install`        | 依存関係のインストール             |
| `npm run dev`         | ローカル開発サーバー起動           |
| `npm run build`       | `./dist/` に本番ビルド出力          |
| `npm run preview`     | ビルド結果をローカルでプレビュー     |

## 免責

本サイトはプロモーション（アフィリエイトリンク）を含みます。掲載内容は実際に検討した一次情報に基づいていますが、価格・在庫・仕様は変更されている場合があります。
