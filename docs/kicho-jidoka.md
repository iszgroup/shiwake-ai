# 記帳代行・記帳の自動化 — 税理士事務所の入力業務を AI で減らす方法

→ **完全版（計算例・よくある質問・出典付き）: [記帳代行・記帳の自動化 — 証憑の回収から領収書OCR・突合・CSV取込・電帳法まで](https://shiwake.isz.ai/guide/kicho-jidoka/?utm_source=github&utm_medium=referral)**

**要点**

- 記帳代行は、税理士が税理士業務に付随して行える業務です（税理士法第2条第2項）。記帳の代行そのものは独占業務ではありませんが、税務書類の作成・税務代理・税務相談は税理士業務です
- 時間がかかるのは **証憑の回収・手入力・税区分の判定・通帳やカード明細との突合**。記帳の遅れは入力より回収で起きることが多いです
- 自動化の基本は、**証憑を発生した日にデータで集め、AI で仕訳の下書きを作り、人は理由付きの「要確認」だけを見る**こと。ぼやけた写真・二重の取込・記載の足りない証憑は要確認に回します
- スキャナ保存の入力期間は、受領後おおむね7営業日以内（業務サイクル後なら最長2か月とおおむね7営業日以内）。A4 は約387万画素以上で読み取ります

## 工程ごとの自動化

| 工程 | これまで | 自動化したやり方 |
| :--- | :--- | :--- |
| 証憑の回収 | 月末・決算前に紙の束で受け取る | 顧問先が発生した日にスマホで撮って送る |
| 入力 | 1枚ずつ打ち込む | AI が勘定科目・税区分・摘要付きの仕訳の下書きを作る |
| 税区分 | 10%・8%・登録番号・経過措置を人が判定 | 登録番号と取引日から経過措置（80%・70%）まで判定し、迷うものは要確認 |
| 突合 | 通帳・カード明細と紙を見比べる | 入出金と証憑を突き合わせ、証憑のない出金・未払いを一覧に |
| 会計ソフトへ | 手入力・転記 | 取込形式の CSV で一括インポート（科目・補助科目・税区分の名前を合わせ、数件でテスト取込） |

## 領収書OCRで読む項目

| 項目 | 仕訳での使い道 |
| :--- | :--- |
| 取引年月日 | 仕訳の日付、経過措置の割合（2026年10月1日から70%） |
| 発行者・品目 | 勘定科目の推定、摘要 |
| 登録番号（T＋13桁） | インボイスかどうか → 税区分 |
| 税率ごとの対価の額・消費税額 | 仮払消費税等、10%と8%の仕訳の分け方 |
| 合計金額・支払方法 | 貸方の科目と金額、検算 |

電帳法の要件は[スキャナ保存](denchoho.md)・[電子取引データの保存](denshi-torihiki.md)、仕組みの全体は[AI経理とは](ai-keiri.md)にまとめています。

→ **完全版: [記帳代行・記帳の自動化](https://shiwake.isz.ai/guide/kicho-jidoka/?utm_source=github&utm_medium=referral)**（回収方法の比較、ぼやけ・重複・記載漏れへの対処、少額特例と経過措置の仕訳例、振込手数料差引の入金、CSV 取込の手順、導入の進め方）

---

## ISZ™ 仕訳AI を試す

- **[領収書・レシートのAI読み取り（登録で証憑100枚まで無料）](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)**
- **[請求書のAI読み取り（登録番号・税率別の金額から仕訳まで）](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)**
- **[通帳・銀行明細のAI読み取り（入出金を仕訳に・証憑と照合）](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)**
- **[勘定科目・仕訳例かんたん検索（155の取引）](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)**
- **[税理士のための無料計算ツール（源泉徴収・社会保険・消費税・減価償却・法人税など）](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)**

→ **[無料で試す（証憑100枚まで無料）](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=kicho-jidoka)**　｜　**[ISZ™ 仕訳AI の詳細](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)**
