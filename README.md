# 木更津 民泊 清掃スタッフ募集 LP

看板QRコードからアクセスする、夏季限定 清掃スタッフ募集のランディングページです。

## 構成

- `index.html` — 募集LP本体（フライヤー内容＋お問い合わせフォーム）
- `thanks.html` — フォーム送信完了ページ（JavaScript無効時のリダイレクト先）

## お問い合わせフォーム

[FormSubmit](https://formsubmit.co/) を利用しています（無料・サーバー不要）。

- 送信先メール：`masaki0515opp@gmail.com`
- **初回のみ**：最初の送信時に FormSubmit から確認メールが届くので、本文のリンクをクリックして有効化してください（以降は自動でメール受信）。
- 送信は JavaScript による非同期送信。無効環境では通常POSTで `thanks.html` にリダイレクトします。

## 更新方法

`index.html` を編集後：

```bash
git add . && git commit -m "update: 内容修正"
git push
```

GitHub Pages に自動反映されます（反映まで1〜2分）。

## 公開URL

https://0515opp-arch.github.io/cleaning-staff-recruit/
