# ISZ™ 仕訳AI — AI経理・記帳自動化と、日本の税金・社会保険の計算ガイド（2026年版）

**要点**

- **ISZ™ 仕訳AI** は、領収書・請求書・通帳を撮って送るだけで、AI が勘定科目・税区分・摘要の付いた仕訳データを作る、税理士事務所と中小企業のための **AI経理（記帳自動化）サービス**です
- 弥生会計・freee・マネーフォワード クラウド・TKC 形式の CSV と、電子帳簿保存法に対応した証憑データを同時に作ります
- このガイドでは、消費税・インボイス・源泉徴収・社会保険料・年末調整・減価償却・法人税・電子帳簿保存法・申告期限を、計算式・例・出典付きで解説しています

## ガイドの一覧

| ガイド | 内容 | 無料ツール |
| :--- | :--- | :--- |
| [AI経理とは](ai-keiri.md) | 仕訳の自動化の仕組み、AI に任せること・人が確認すること | [領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[通帳のAI読み取り](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)・[ツール一覧](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [記帳代行・記帳の自動化](kicho-jidoka.md) | 証憑の回収、入力・突合の自動化、会計ソフトへの CSV 取込 | [領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[通帳のAI読み取り](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)・[ツール一覧](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [消費税の計算](consumption-tax.md) | 税込・税抜、インボイスの端数処理、一般・簡易・2割特例・3割特例、中間申告 | [消費税](https://shiwake.isz.ai/tools/shohizei/?utm_source=github&utm_medium=referral)・[比較](https://shiwake.isz.ai/tools/shohizei-hikaku/?utm_source=github&utm_medium=referral)・[中間申告](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [インボイスの登録番号と経過措置](invoice.md) | T番号のチェックディジット、80%→70%控除、少額特例 | [登録番号チェック](https://shiwake.isz.ai/tools/invoice-number/?utm_source=github&utm_medium=referral)・[経過措置](https://shiwake.isz.ai/tools/keika-sochi/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral) |
| [源泉徴収税額の計算](withholding-tax.md) | 給与の月額表（740,000円以上の算式）、電算機計算の特例、賞与、報酬10.21% | [給与](https://shiwake.isz.ai/tools/gensen-kyuyo/?utm_source=github&utm_medium=referral)・[賞与](https://shiwake.isz.ai/tools/gensen-shoyo/?utm_source=github&utm_medium=referral)・[報酬](https://shiwake.isz.ai/tools/gensen-houshu/?utm_source=github&utm_medium=referral)・[退職金](https://shiwake.isz.ai/tools/taishoku/?utm_source=github&utm_medium=referral) |
| [社会保険料の計算](social-insurance.md) | 標準報酬月額、健康保険・介護・子ども・子育て支援金・厚生年金・雇用保険 | [社会保険料](https://shiwake.isz.ai/tools/shakai-hoken/?utm_source=github&utm_medium=referral)・[手取り](https://shiwake.isz.ai/tools/kyuyo-tedori/?utm_source=github&utm_medium=referral)・[年収の壁](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral) |
| [所得税と年末調整](income-tax.md) | 速算表、給与所得控除、基礎控除（令和8年分）、年収の壁 | [年収の壁](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral)・[年末調整](https://shiwake.isz.ai/tools/nencho/?utm_source=github&utm_medium=referral) |
| [減価償却の計算](depreciation.md) | 定額法・200%定率法、少額減価償却資産（40万円未満）、一括償却資産 | [減価償却](https://shiwake.isz.ai/tools/genka-shokyaku/?utm_source=github&utm_medium=referral) |
| [法人税等の計算](corporate-tax.md) | 中小法人の税率、地方法人税、防衛特別法人税、住民税・事業税 | [法人税等](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral)・[申告・納付期限カレンダー](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral) |
| [法人の申告・納付期限](shinkoku-kigen.md) | 法人税・消費税・源泉所得税・法定調書・償却資産・算定基礎届・年度更新、延滞税 | [申告・納付期限カレンダー](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral)・[延滞税](https://shiwake.isz.ai/tools/entaizei/?utm_source=github&utm_medium=referral)・[中間申告](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [電子帳簿保存法のスキャナ保存](denchoho.md) | 解像度200dpi、入力期限、訂正削除の履歴、検索要件、スマホ撮影 | [領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral) |
| [電子取引データの保存](denshi-torihiki.md) | メールの PDF・Web 明細の保存義務、検索要件、猶予措置 | [請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral) |
| [勘定科目の一覧と仕訳の例](accounts.md) | よく使う勘定科目、領収書の仕訳、会議費と交際費（1人1万円） | [勘定科目・仕訳例検索](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)・[会議費・交際費](https://shiwake.isz.ai/tools/kosaihi/?utm_source=github&utm_medium=referral)・[印紙税額](https://shiwake.isz.ai/tools/inshi-zei/?utm_source=github&utm_medium=referral) |

## ISZ™ 仕訳AI でできること

- 領収書・レシート・請求書・カード明細・通帳の読み取りと仕訳の作成
- 顧問先からのスマホ提出（リンクを渡すだけ・アプリ不要・画質をその場で確認）
- インボイスの登録番号の抽出、軽減税率・経過措置の税区分
- 電子帳簿保存法の検索・訂正削除の履歴・原本と仕訳の相互参照
- 銀行明細との照合、決算前の要確認リスト
- 給与計算・年末調整、試算表・決算書、e-Tax 用の財務諸表 CSV

AI は税務判断をしません。仕訳ドラフトの作成と要確認箇所の抽出までを担い、判断と確定は税理士・経理担当者が行う設計です。

---

→ **[無料で試す（証憑100枚まで無料・カード不要）](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=docs-index)**　｜　**[ISZ™ 仕訳AI の詳細](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)**　｜　**[無料計算ツール](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)**　｜　**[勘定科目・仕訳例検索](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)**

ISZ™ 仕訳AI は [ISZ.AI（ISZ GROUP）](https://isz.ai) が提供しています。
