# 今日のビジュアル力チェック GitHub Pages サイト

App Store Connect のマーケティングURL、サポートURL、プライバシーポリシーURL、Google AdMob の `app-ads.txt` 確認に使うための静的Webサイトです。

## 生成ファイル

- `index.html`：マーケティングページ
- `support.html`：サポート・FAQページ
- `privacy-policy.html`：プライバシーポリシー
- `styles.css`：共通スタイル
- `app-ads.txt`：Google AdMob 確認用ファイル
- `favicon.ico`：favicon placeholder

## GitHub Pages 公開方法

1. このフォルダのファイルを GitHub リポジトリのルートに配置します。
2. GitHub のリポジトリ画面で `Settings` を開きます。
3. 左メニューの `Pages` を開きます。
4. `Build and deployment` の `Source` を `Deploy from a branch` にします。
5. `Branch` を `main`、フォルダを `/ (root)` にして保存します。
6. 数分後に GitHub Pages URL が発行されます。

## username.github.io 形式を推奨する理由

AdMob の `app-ads.txt` は、App Store Connect に登録するマーケティングURLのドメイン直下で確認されます。

リポジトリ名付き Pages の場合、公開URLは次のようになります。

```text
https://username.github.io/repository-name/
```

この場合でもページ自体は公開できますが、AdMob が確認する `app-ads.txt` はドメイン直下の次のURLになることがあります。

```text
https://username.github.io/app-ads.txt
```

そのため、AdMob 確認を安定させるには、可能であればリポジトリ名を `username.github.io` にして、サイトをドメイン直下で公開する構成を推奨します。

推奨公開URL例：

```text
https://username.github.io/
```

## App Store Connect 登録URL

`username.github.io` 形式で公開した場合：

- マーケティングURL：`https://username.github.io/`
- サポートURL：`https://username.github.io/support.html`
- プライバシーポリシーURL：`https://username.github.io/privacy-policy.html`

リポジトリ名付きで公開した場合：

- マーケティングURL：`https://username.github.io/repository-name/`
- サポートURL：`https://username.github.io/repository-name/support.html`
- プライバシーポリシーURL：`https://username.github.io/repository-name/privacy-policy.html`

## app-ads.txt 確認方法

公開後、ブラウザで以下を確認します。

```text
https://username.github.io/app-ads.txt
```

表示内容は次の1行のみである必要があります。

```text
google.com, pub-5840457424714744, DIRECT, f08c47fec0942fa0
```

余計な文字、空白行、HTML表示になっていないことを確認してください。

## AdMob 反映時間

`app-ads.txt` を公開してから AdMob 側に反映されるまで、数時間から数日かかる場合があります。
公開直後に未確認と表示されても、URLが正しく表示されていれば時間をおいて再確認してください。

## App Store 審査向けメモ

- 本サイトでは、アプリが医学的診断ではなく娯楽・参考目的であることを明記しています。
- 年齢や外見に関する表現は断定を避け、写真から受ける印象として説明しています。
- 画像利用、AI解析、外部AI利用可能性、AdMob、広告識別子、利用状況データ、第三者提供、安全管理、未成年利用、免責事項をプライバシーポリシーに記載しています。

## 次にやるべき作業

1. GitHub で `username.github.io` リポジトリを作成します。
2. 本ファイル一式をリポジトリのルートへ push します。
3. GitHub Pages を `main` / `/ (root)` で有効化します。
4. `https://username.github.io/` が表示されることを確認します。
5. `https://username.github.io/app-ads.txt` が指定の1行だけを表示することを確認します。
6. App Store Connect にマーケティングURL、サポートURL、プライバシーポリシーURLを登録します。
7. AdMob 管理画面で app-ads.txt の確認状態を確認します。
