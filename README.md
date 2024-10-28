# slidev-theme-kstm-su
[Slidev](https://sli.dev/) theme for kstm

## デザイン

作者の好みとkstmらしさでバランスを取り、以下のフォントを使用しています。

- 全般: 欧文 Roboto, 日本語 Noto Sans
- 等幅: 欧文 Inconsolata, 日本語 Noto Sans
- 数学: Times New Roman
    - 注: Times New Romanがインストールされていない場合のフォールバック未指定

文字は標準24ptで、20pt、18ptのレイアウトを収録しています（`layout: intro20`, `layout: intro18`で利用できます）。

ソースコードの文字は標準13ptです。v0.2.0の時点では、小さすぎる場合に`pre, pre > code`に対してfont-sizeを適切に指定してください（うまくいかない場合は`!important`を使って逃げてもよいです）。

## 使用方法

1. GitHubのSettings > Developer settings > Personal access tokensより、「read:packages」を持つ「GitHubのPersonal Access Token(Classic)」を作成して控えておきます
    - 取得したトークンの値をこの後述べる`.npmrc`にべた書きすると公開事故をする可能性があるので、環境変数を使って書くことを推奨します
2. `npm init slidev`などでSlidevのプロジェクトを作成します
3. `.npmrc`ファイルに以下の2行を追加します
```
@kstm-su:registry=https://npm.pkg.github.com/
//npm.pkg.github.com/:=_autToken=<トークン値>
```
4. `npm i @kstm-su/slidev-theme-kstm` でインストールできます。ユーザ名とパスワードを尋ねられた場合は、ユーザ名にGitHubのIDを、パスワードに先ほど取得した**トークン値**を入力します
5. 以降の使い方は普通のSlidevと変わりません
