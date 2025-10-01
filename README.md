# cwt-2025

セミナープレゼンテーションスライドシステム

## デモ

プレゼンテーションは GitHub Pages で公開されています：
**https://hgw.github.io/cwt-2025/**

main ブランチへの push で自動的にデプロイされます。

## 技術スタック

- **Markdown**: 原稿管理
- **HTML**: 表示出力
- **Reveal.js**: プレゼンテーションフレームワーク
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

1. `slides.md` でプレゼンテーションの内容を編集
2. `npm run build:css` でスタイルをビルド
3. ブラウザで `index.html` を開いてプレゼンテーションを表示

### ライブリロード（開発時）

```bash
# CSSの変更を監視
npm run watch:css

# 別のターミナルでローカルサーバーを起動
npm run serve
```

## ファイル構成

```
cwt-2025/
├── index.html           # HTMLプレゼンテーション
├── slides.md            # Markdown原稿
├── package.json         # 依存関係管理
├── tailwind.config.js   # Tailwind設定
├── src/
│   └── input.css        # Tailwindスタイルソース
└── dist/
    └── output.css       # コンパイル済みCSS
```

## プレゼンテーション操作

- **→ / Space**: 次のスライド
- **← / Backspace**: 前のスライド
- **ESC / O**: スライド一覧表示
- **F**: フルスクリーンモード
- **S**: スピーカーノート表示

## デプロイ

main ブランチへの push で GitHub Actions が自動的に：
1. npm 依存関係をインストール
2. Tailwind CSS をビルド
3. GitHub Pages にデプロイ

デプロイ状況は [Actions タブ](../../actions) で確認できます。