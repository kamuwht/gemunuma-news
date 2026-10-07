# げむぬまニュース投稿システム 公開ページ

GitHubアカウント: kamuwht
新規リポジトリ名: gemunuma-news

このフォルダのファイルは公開用です。GoogleのClient SecretやOAuthトークン、VPSの設定、動画ファイルは含みません。
Googleへの審査通過や公開ボタンの有効化を保証するものではありません。

## 1. 新規リポジトリを作成

https://github.com/new

- Owner: kamuwht
- Repository name: gemunuma-news
- Visibility: Public
- Add README: On
- Create repository

既存の同名リポジトリがある場合、その内容を上書きせず、作業を止めて確認してください。

## 2. ファイルをアップロード

ZIPを展開し、次の6ファイルをリポジトリの最上位にアップロードしてください。
フォルダごとではなく、ファイルを選択します。

- index.html
- privacy.html
- terms.html
- styles.css
- icon.png
- README.md

アップロード画面:
https://github.com/kamuwht/gemunuma-news/upload/main

Commit changesを押します。

## 3. GitHub Pagesを有効化

https://github.com/kamuwht/gemunuma-news/settings/pages

- Source: Deploy from a branch
- Branch: main
- Folder: /(root)
- Save

GitHubの初回公開には最大10分程度かかる場合があります。
公開完了後、以下のURLが実際に表示されることを確認してください。

- ホーム: https://kamuwht.github.io/gemunuma-news/
- プライバシー: https://kamuwht.github.io/gemunuma-news/privacy.html
- 利用規約: https://kamuwht.github.io/gemunuma-news/terms.html

上記は予定URLです。作成・設定完了前には表示されません。

## 4. Google Auth Platformへ登録

Game Shortsプロジェクトのブランディング画面で、先に承認済みドメインへ次を追加します。

kamuwht.github.io

次に:

- アプリケーションのホームページ: https://kamuwht.github.io/gemunuma-news/
- アプリケーション プライバシーポリシー リンク: https://kamuwht.github.io/gemunuma-news/privacy.html
- アプリケーション利用規約リンク: https://kamuwht.github.io/gemunuma-news/terms.html
- アプリ名: げむぬまニュース投稿システム
- ロゴ: 現時点では未設定

保存してから「対象」へ戻り、「アプリを公開」が押せるか確認します。
所有権確認やブランド確認が求められた場合は、その具体的なメッセージを確認して追加対応します。
Google Search Console用の確認コード・HTMLファイルは発行された実物を使用し、架空のコードは入れません。

公開ステータスを本番環境へ変更できた後、既存のn8nのYouTube認証を再接続し、接続確認フローを実行してください。
これはOAuthアプリのステータス変更です。投稿済み動画の公開設定は変更しません。
YouTube API経由の公開投稿に関するプロジェクト監査は別の手続きです。

## ページ内容

このページは個人用の投稿アプリを説明しています。一般向けのOAuthログインサービスではありません。
現在の実装に合わせ、認証情報の暗号化保存、投稿履歴の保管、APIへの送信、アクセス権の取り消し、手動削除について記載しています。
運用やデータの扱いが変わる場合はポリシーの内容も更新してください。

## 参考資料

- https://support.google.com/cloud/answer/15549049
- https://developers.google.com/identity/protocols/oauth2/production-readiness/brand-verification
- https://developers.google.com/terms/api-services-user-data-policy
- https://developers.google.com/youtube/terms/developer-policies
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
