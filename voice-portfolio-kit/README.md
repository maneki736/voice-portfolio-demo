# Voice Portfolio Template

音声活動者（声優・ナレーター）向けのポートフォリオサイトテンプレートです。
黒を基調としたクールで落ち着いたデザインで、あなたの声を魅力的に伝えます。
HTML/CSSのみ（一部FAQのみ軽量JS使用）で構成されており、サーバー契約不要でPC/スマホですぐに確認できます。

## 📁 フォルダ構成

```
voice-portfolio-kit/
├─ index.html       (HOME: トップページ)
├─ profile.html     (PROFILE: プロフィール)
├─ works.html       (WORKS: 音声サンプル一覧)
├─ request.html     (REQUEST: 依頼・料金)
├─ faq.html         (FAQ: よくある質問)
├─ assets/
│  ├─ css/          (デザイン設定)
│  ├─ img/          (画像フォルダ)
│  └─ audio/        (音声フォルダ)
└─ README.md        (このファイル)
```

## 🚀 30分で公開する手順

### 1. 自分の情報を入力する

各HTMLファイルをテキストエディタ（メモ帳やVSCodeなど）で開き、以下の部分を書き換えてください。

- `index.html` の `NAME HERE` → あなたの名前に変更
- `request.html` の `email@example.com` → あなたのメールアドレスに変更
- 各ページのテキスト（自己紹介、料金、実績など）

### 2. 画像・音声を差し替える

#### 画像
`assets/img/` フォルダの中に、以下の名前で画像を保存すると自動で反映されます。
- `avatar.png` : プロフィールアイコン（正方形推奨）
- その他必要な画像があれば追加し、HTMLの `<img src="...">` を書き換えてください。

#### 音声
`assets/audio/` フォルダに `sample_01.mp3` などの名前で音声ファイルを入れます。
各HTMLの `<audio src="assets/audio/〇〇.mp3">` のファイル名を、入れたファイル名に合わせて書き換えてください。

### 3. 色を変更する（任意）

`assets/css/style.css` の冒頭にある設定を変えるだけで、サイト全体の色が変わります。

```css
:root {
  --bg: #0b0d10;      /* 背景色 */
  --accent: #4da3ff;  /* アクセントカラー（ボタンやリンクの色） */
}
```

### 4. Googleフォームと連携する

`request.html` にある「Googleフォームで依頼する」ボタンのリンク先を修正します。

1. [Googleフォーム](https://www.google.com/intl/ja_jp/forms/about/) で問い合わせフォームを作成。
2. 「送信」ボタン → リンクアイコン → URLをコピー。
3. `request.html` の `<a href="https://docs.google.com/forms/..." target="_blank" class="btn-primary">` のURL部分を書き換える。

## 🌐 公開方法（GitHub Pages）

サーバーを借りなくても、GitHubアカウントがあれば無料で公開できます。

1. GitHubにリポジトリを作成（例: `my-portfolio`）。
2. このフォルダの中身（`index.html`などが直下にある状態）をアップロード。
3. リポジトリの [Settings] > [Pages] を開く。
4. [Source] を `Deploy from a branch` にし、Branch を `main` / `/(root)` に設定してSave。
5. 数分後に表示されるURL（例: `https://username.github.io/my-portfolio/`）にアクセスすれば公開完了です！

## ⚠️ よくあるエラー

**Q. 音声が再生されない**
A. ファイル名が合っているか確認してください（`Sample.mp3` と `sample.mp3` は区別されます）。また、PCのブラウザによってはローカルファイル（`file://`）での再生が一部制限されることがありますが、サーバーにアップロードすれば動作します。

**Q. 文字化けする**
A. ファイルを保存する際、文字コードが「UTF-8」になっているか確認してください。
