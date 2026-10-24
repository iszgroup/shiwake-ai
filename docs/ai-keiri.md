# AI経理（AI自動仕訳）とは — 仕訳の自動化の仕組みと導入のポイント

→ **完全版（計算例・よくある質問・出典付き）: [AI自動仕訳（仕訳AI）とは？税理士事務所向けの仕組みと導入の進め方](https://shiwake.isz.ai/guide/ai-jidou-shiwake/?utm_source=github&utm_medium=referral)**

**要点**

- AI自動仕訳（AI経理）とは、領収書・請求書・通帳などの証憑から AI が取引を読み取り、**勘定科目・税区分・摘要を付けた仕訳の下書き**を作ることです
- 仕組みは **読み取り（OCR）→ 勘定科目の推定 → 税区分の判定 → 摘要 → 検算と要確認** の5段階。OCR は文字を読むだけで、科目・税区分の判断は別の工程です
- 人の確認は、AI が理由を付けた「要確認」に集中させます。判断と確定は税理士・経理担当者です（税理士法第2条）
- 導入は顧問先1社・1か月分から。今の会計ソフトに CSV で取り込み、入力と確認の時間を導入前と比べてから広げます

## OCR・科目分類・税区分判定の違い

| 工程 | 何をするか | よくある間違い |
| :--- | :--- | :--- |
| OCR・項目抽出 | 文字を読み、日付・金額・登録番号などの項目に分ける | ぼやけ・かすれでの読み違い、手書きの金額 |
| 科目分類 | 取引先・品目・過去の仕訳・記帳ルールから勘定科目を選ぶ | 用途が分からない支出（会議費か交際費か、私用か）、資産か費用か |
| 税区分判定 | 課税区分・税率（10%・8%）・経過措置の割合を決める | 税率の混在、登録番号の見落とし、経過措置の切り替え日（2026年10月1日から80%→70%） |

記帳代行の業務全体の見直し方は[記帳の自動化](kicho-jidoka.md)にまとめています。

→ **完全版: [AI自動仕訳（仕訳AI）とは？税理士事務所向けの仕組みと導入の進め方](https://shiwake.isz.ai/guide/ai-jidou-shiwake/?utm_source=github&utm_medium=referral)**（5段階の仕組みと例、確認の置き方、CSV 取込の注意点、作業量の比べ方、1社から始める手順、税理士法との関係）

---

## ISZ™ 仕訳AI を試す

- **[領収書・レシートのAI読み取り（登録で証憑100枚まで無料）](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)**
- **[請求書のAI読み取り（登録番号・税率別の金額から仕訳まで）](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)**
- **[通帳・銀行明細のAI読み取り（入出金を仕訳に・証憑と照合）](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)**
- **[勘定科目・仕訳例かんたん検索（155の取引）](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)**
- **[税理士のための無料計算ツール（源泉徴収・社会保険・消費税・減価償却・法人税など）](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)**

→ **[無料で試す（証憑100枚まで無料）](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=ai-keiri)**　｜　**[ISZ™ 仕訳AI の詳細](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)**
