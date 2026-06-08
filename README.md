# 木更津 民泊 清掃スタッフ募集 LP

看板QRコードからアクセスする、夏季限定 清掃スタッフ募集のランディングページです。

## 構成

- `index.html` — 募集LP本体（フライヤー内容＋お問い合わせフォーム）
- `thanks.html` — フォーム送信完了ページ（JavaScript無効時のリダイレクト先）

## お問い合わせフォーム（Googleフォーム）

応募フォームは **Googleフォーム** を `index.html` に埋め込んでいます（安定・無料・回答が自動集計）。

- フォーム本体：Google Apps Script で生成（`../google-form-setup.gs` 参照）
- 回答用URL：`https://docs.google.com/forms/d/e/1FAIpQLScLlepclw91uGursXmQt8BC-npjWrAmyqGEGKwChUdraA_r1g/viewform`
- 回答は Google スプレッドシート「清掃スタッフ募集 応募一覧」に自動保存
- 応募が届くたびに `masaki0515opp@gmail.com` へ自動通知メール
- LP には埋め込み表示＋「別タブで開く」リンク＋電話フォールバックを併設

### フォームの内容を変えたいとき
Googleフォーム側（編集URL）で設問を編集すれば、LPの埋め込みにも即反映されます（HTML修正不要）。

## 更新方法

`index.html` を編集後：

```bash
git add . && git commit -m "update: 内容修正"
git push
```

GitHub Pages に自動反映されます（反映まで1〜2分）。

## 公開URL

https://0515opp-arch.github.io/cleaning-staff-recruit/
