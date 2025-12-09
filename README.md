# GitHub Pages Deployment Guide

このプロジェクトは、GitHub Pagesを使用して簡単に公開できるシンプルなウェブサイトのテンプレートです。

## ファイル構成

- `index.html`: ウェブサイトのメインページ
- `style.css`: デザインを定義するスタイルシート
- `README.md`: この説明書

## デプロイ手順 (GitHub Pages)

以下の手順で、このウェブサイトをインターネット上に公開できます。

### 1. GitHubリポジトリの作成

1. [GitHub](https://github.com/)にログインします。
2. 画面右上の「+」アイコンをクリックし、「New repository」を選択します。
3. **Repository name** に好きな名前（例: `my-simple-site`）を入力します。
4. "Public" が選択されていることを確認します（無料プランでのPages利用のため）。
5. 「Create repository」をクリックします。

### 2. コードのアップロード

ご自身のPCで以下のコマンドを実行し、ファイルをGitHubにアップロードします。
※ ターミナル（PowerShellやCommand Prompt）を使用します。

```bash
# Gitの初期化（まだ行っていない場合）
git init

# ファイルをステージング
git add .

# コミット
git commit -m "Initial commit"

# リモートリポジトリを追加 (URLは作成したリポジトリのものに置き換えてください)
git remote add origin https://github.com/<あなたのユーザー名>/<リポジトリ名>.git

# メインブランチにプッシュ
git branch -M main
git push -u origin main
```

### 3. GitHub Pagesの設定

1. GitHubのリポジトリページを開きます。
2. 上部タブの **Settings** をクリックします。
3. 左サイドバーの **Pages** をクリックします。
4. **Build and deployment** セクションの **Source** で "Deploy from a branch" を選択します。
5. **Branch** のドロップダウンで `main` を選択し、その隣のフォルダ設定は `/(root)` のままにして「Save」をクリックします。

数分待つと、ページ上部に公開URL（`https://<ユーザー名>.github.io/<リポジトリ名>/`）が表示されます。そのリンクをクリックして、サイトが正しく表示されるか確認してください。

---

## ローカルでの確認方法

`index.html` ファイルをブラウザ（Chrome, Edgeなど）にドラッグ＆ドロップするだけで、デザインを確認できます。
