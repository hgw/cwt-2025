# cwt-2025

セミナープレゼンテーションスライドシステム

## デモ

プレゼンテーションは GitHub Pages で公開されています：
**https://hgw.github.io/cwt-2025/**

main ブランチへの push で自動的にデプロイされます。

## 技術スタック

- **HTML**: プレゼンテーション原稿
- **Tailwind CSS**: スタイリング
- **GitHub Actions**: 自動デプロイ
- **GitHub Pages**: ホスティング

## セットアップ

### 推奨環境

- Node.js 22 (最新安定版)
- nvm を使用している場合、`.nvmrc` ファイルで自動的にバージョンが設定されます

```bash
# nvm ユーザーの場合
nvm use

# 依存関係のインストール
npm install

# Tailwind CSSのビルド
npm run build:css
```

## 使い方

1. `public/index.html` でプレゼンテーションの内容を編集
2. `npm run build:css` でスタイルをビルド
3. ブラウザで `public/index.html` を開いてプレゼンテーションを表示

### 開発サーバー（ライブリロード）

```bash
# 開発サーバーを起動（推奨）
npm run dev
# http://localhost:8000 で起動
# CSS、HTMLファイルの変更を自動リロード
```

## ファイル構成

```
cwt-2025/
├── public/              # 公開用ディレクトリ
│   ├── index.html       # プレゼンテーション原稿（ここを編集）
│   └── assets/
│       └── css/
│           └── index.css # ビルド済みCSS
├── src/
│   └── css/
│       └── index.css    # Tailwindスタイルソース
├── package.json         # 依存関係管理
└── tailwind.config.js   # Tailwind設定
```

## プレゼンテーション操作

- **↑↓ / Space**: スライド移動
- **マウスホイール**: スクロール

## デプロイ

main ブランチへの push で GitHub Actions が自動的に：
1. npm 依存関係をインストール
2. Tailwind CSS をビルド
3. GitHub Pages にデプロイ

デプロイ状況は [Actions タブ](../../actions) で確認できます。