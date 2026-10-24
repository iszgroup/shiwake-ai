# ISZ™ 仕訳AI — AI経理・記帳自動化と、日本の税金・社会保険の計算ガイド（2026年版）

[![Website](https://img.shields.io/badge/公式サイト-shiwake.isz.ai-0b1f4d.svg)](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)
[![Free trial](https://img.shields.io/badge/無料で試す-証憑100枚まで無料-c9a227.svg)](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme)
[![Tools](https://img.shields.io/badge/無料計算ツール-shiwake.isz.ai%2Ftools-2e7d32.svg)](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE.md)

[日本語](README.md) ｜ [简体中文](README.zh-CN.md) ｜ [English](README.en.md)

**ISZ™ 仕訳AI** は、領収書・請求書・通帳などの証憑を撮って送るだけで、AI が読み取り、勘定科目・税区分・摘要を付けた**仕訳データ**を作る、税理士事務所と中小企業のための**AI経理（記帳自動化）サービス**です。弥生会計・freee・マネーフォワード クラウド・TKC などの会計ソフトにそのまま取り込める CSV と、電子帳簿保存法に対応した証憑データを同時に作ります。

このリポジトリは、ISZ™ 仕訳AI の開発で整理した**日本の税金・社会保険の計算方法と実務の知識**（消費税・インボイス・源泉徴収・社会保険料・所得税・年末調整・減価償却・法人税・電子帳簿保存法・申告期限）を、計算式・例・一次資料の出典付きでまとめた**知識ベース**です。

<p align="center">
  <a href="https://shiwake.isz.ai/?utm_source=github&utm_medium=referral"><b>▶ ISZ™ 仕訳AI の詳細</b></a>　｜　
  <a href="https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme"><b>▶ 無料で試す（証憑100枚まで・カード不要）</b></a>　｜　
  <a href="https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral"><b>▶ 無料計算ツール</b></a>　｜　
  <a href="https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral"><b>▶ 勘定科目・仕訳例検索</b></a>　｜　
  <a href="https://youtu.be/S9SmAAVw3MU"><b>▶ 紹介動画</b></a>
</p>

---

## 目次

- [ISZ™ 仕訳AI とは](#isz-仕訳ai-とは)
- [できること](#できること)
- [使い方（3ステップ）](#使い方3ステップ)
- [計算ガイドと無料ツール](#計算ガイドと無料ツール)
- [税理士のための無料計算ツール](#税理士のための無料計算ツール)
- [よくある質問](#よくある質問)
- [免責事項](#免責事項)
- [ISZ GROUP について](#isz-group-について)
- [ライセンス](#ライセンス)

---

## ISZ™ 仕訳AI とは

月末にまとめて届く領収書の束を、1枚ずつ会計ソフトに手入力する作業は、税理士事務所と経理担当者の大きな負担です。インボイス制度（登録番号の確認・8%と10%の区分・免税事業者からの仕入の経過措置）と電子帳簿保存法（スキャナ保存）への対応で、1枚あたりの確認の手間はさらに増えました。

ISZ™ 仕訳AI は、この**「打ち込み」と「税区分の判定」を AI が代わりに行う仕訳ドラフト作成AI**です。

| | 従来の手入力 | ISZ™ 仕訳AI |
| :--- | :--- | :--- |
| 証憑の集め方 | 紙の束を郵送・持参 | スキャナで一括ドロップ／顧問先がスマホで撮って送信 |
| 仕訳の入力 | 1枚ずつ画面に打ち込む | AI が日付・取引先・金額・税率・登録番号を読み取り、仕訳を作成 |
| 税区分 | 8%・10%・経過措置を人が判定 | 登録番号の有無と取引日から、経過措置（80%・70%控除など）まで自動判定 |
| 会計ソフトへの反映 | 転記 | 弥生・freee・MF・TKC 形式の CSV を一括インポート |
| 確認 | 紙と画面を見比べる | 仕訳と原本を左右に並べ、AI が「要確認」とした項目だけを確認 |

**AI は税務判断をしません。** AI が担うのは仕訳ドラフトの作成と、確認が必要な箇所の抽出（理由付き）までで、科目・税区分の判断と最終確定は税理士・経理担当者が行う設計です。税額などの**金額の計算は AI に任せず、公表された算式と料率で決定的に計算**しています（同じ入力なら必ず同じ結果）。

## できること

- **証憑の読み取りと仕訳の作成** — 領収書・レシート・請求書・カード明細・通帳（PDF・写真・ZIP）。「日付_取引先_金額」のファイル名を付け、電子帳簿保存法の解像度を満たすよう、1枚の写真に書類が何枚も写っていれば送る前にお知らせします
- **顧問先からのスマホ提出** — 提出用リンクを QR コード・メール・LINE で渡すだけ。アプリのインストールもログインも不要で、画質（電子帳簿保存法の解像度要件）をその場で確認します
- **インボイス制度** — 登録番号（T番号）の抽出と検算、軽減税率の区分、免税事業者からの仕入の経過措置（2026年10月から70%控除）
- **電子帳簿保存法** — 取引年月日・金額・取引先の検索、訂正削除の履歴、原本と仕訳の相互参照（証憑ID）、事務処理規程のひな形
- **銀行明細との照合** — 振込で支払った請求書と通帳の出金を突き合わせ、証憑のない出金・未払いの請求書を一覧に
- **決算前の要確認リスト** — 二重計上、源泉徴収の漏れ候補、1人1万円を超える飲食費、資産計上の候補、休日の支出など
- **給与計算・年末調整** — 源泉所得税・社会保険料の計算、源泉徴収票まで
- **試算表・決算書** — 合計残高試算表・損益計算書・貸借対照表・株主資本等変動計算書・個別注記表・消費税の区分集計、e-Tax 用の財務諸表 CSV
- **申告書の作成** — 法人税の別表・勘定科目内訳明細書・法人事業概況説明書、地方税（第六号・第二十号様式）、消費税の申告書を国税庁などの様式で作成。法人税・消費税は e-Tax 用の申告データ（.xtx）も出力し、税理士が確認・電子署名して送信
- **会計ソフト連携** — 弥生会計・freee会計・マネーフォワード クラウド会計・TKC（FX シリーズ）・JDL・勘定奉行

アップロードされた財務データは AI の学習には使いません。契約・サポート・データ管理はすべて日本国内です。

## 使い方（3ステップ）

1. **撮って送る** — 領収書をスマホかスキャナで撮影し、ドラッグ＆ドロップ。顧問先には提出用リンクを渡すだけ
2. **AI が仕訳にする** — 読み取り・科目の判定・摘要の作成・重複の検知・銀行明細との照合まで自動
3. **例外だけ確認する** — 「要確認」の項目を原本と見比べて確定し、会計ソフトへ CSV で取り込む

新規登録だけで**証憑100枚まで無料**（クレジットカード不要）で試せます → **[無料で試す](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme)**

料金・導入事例・機能の詳細は **[shiwake.isz.ai](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)** をご覧ください。

---

## 計算ガイドと無料ツール

計算の考え方を、計算式・例・一次資料（国税庁・日本年金機構・協会けんぽ・厚生労働省など）の出典付きで解説しています。数字を当てはめて計算したいときは、右の列の無料ツールをお使いください。

| ガイド | 内容 | 無料ツール |
| :--- | :--- | :--- |
| [AI経理とは](docs/ai-keiri.md)（[完全版](https://shiwake.isz.ai/guide/ai-jidou-shiwake/?utm_source=github&utm_medium=referral)） | 仕訳の自動化の仕組み、AI に任せること・人が確認すること、導入のポイント | [領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[通帳のAI読み取り](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)・[ツール一覧](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [記帳代行・記帳の自動化](docs/kicho-jidoka.md)（[完全版](https://shiwake.isz.ai/guide/kicho-jidoka/?utm_source=github&utm_medium=referral)） | 税理士事務所の入力業務を減らす方法、顧問先からの証憑回収、会計ソフトへの CSV 取込 | [領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[通帳のAI読み取り](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)・[ツール一覧](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [消費税の計算](docs/consumption-tax.md)（[完全版](https://shiwake.isz.ai/guide/shohizei/?utm_source=github&utm_medium=referral)） | 税込・税抜、インボイスの端数処理、一般課税・簡易課税・2割特例・3割特例、中間申告 | [消費税（税込・税抜・端数）](https://shiwake.isz.ai/tools/shohizei/?utm_source=github&utm_medium=referral)・[課税方式の比較](https://shiwake.isz.ai/tools/shohizei-hikaku/?utm_source=github&utm_medium=referral)・[中間申告](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [インボイスの登録番号（T番号）と経過措置](docs/invoice.md)（[完全版](https://shiwake.isz.ai/guide/invoice/?utm_source=github&utm_medium=referral)） | チェックディジットの計算、免税事業者からの仕入（80%→70%控除）、少額特例 | [登録番号チェック](https://shiwake.isz.ai/tools/invoice-number/?utm_source=github&utm_medium=referral)・[経過措置](https://shiwake.isz.ai/tools/keika-sochi/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral) |
| [源泉徴収税額の計算](docs/withholding-tax.md)（[完全版](https://shiwake.isz.ai/guide/gensen-choshu/?utm_source=github&utm_medium=referral)） | 給与の月額表（740,000円以上の算式・扶養7人超）、電算機計算の特例、賞与、報酬・料金（10.21%） | [給与](https://shiwake.isz.ai/tools/gensen-kyuyo/?utm_source=github&utm_medium=referral)・[賞与](https://shiwake.isz.ai/tools/gensen-shoyo/?utm_source=github&utm_medium=referral)・[報酬・料金](https://shiwake.isz.ai/tools/gensen-houshu/?utm_source=github&utm_medium=referral)・[退職金の税金](https://shiwake.isz.ai/tools/taishoku/?utm_source=github&utm_medium=referral) |
| [社会保険料の計算（令和8年度）](docs/social-insurance.md)（[完全版](https://shiwake.isz.ai/guide/shakai-hoken/?utm_source=github&utm_medium=referral)） | 標準報酬月額、健康保険・介護保険・子ども・子育て支援金・厚生年金・雇用保険 | [社会保険料](https://shiwake.isz.ai/tools/shakai-hoken/?utm_source=github&utm_medium=referral)・[給与の手取り](https://shiwake.isz.ai/tools/kyuyo-tedori/?utm_source=github&utm_medium=referral)・[年収の壁](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral) |
| [所得税と年末調整（令和8年分）](docs/income-tax.md)（[完全版](https://shiwake.isz.ai/guide/shotokuzei-nencho/?utm_source=github&utm_medium=referral)） | 速算表、給与所得控除、基礎控除、年末調整の流れ、年収の壁 | [年収の壁](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral)・[年末調整](https://shiwake.isz.ai/tools/nencho/?utm_source=github&utm_medium=referral)・[給与の手取り](https://shiwake.isz.ai/tools/kyuyo-tedori/?utm_source=github&utm_medium=referral) |
| [減価償却の計算](docs/depreciation.md)（[完全版](https://shiwake.isz.ai/guide/genka-shokyaku/?utm_source=github&utm_medium=referral)） | 定額法・200%定率法、少額減価償却資産（令和8年4月から40万円未満）、一括償却資産 | [減価償却](https://shiwake.isz.ai/tools/genka-shokyaku/?utm_source=github&utm_medium=referral) |
| [法人税等の計算（中小法人）](docs/corporate-tax.md)（[完全版](https://shiwake.isz.ai/guide/hojinzei/?utm_source=github&utm_medium=referral)） | 税率15%・23.2%、地方法人税、防衛特別法人税、住民税・事業税 | [法人税等](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral)・[申告・納付期限カレンダー](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral) |
| [法人税申告書の作り方](docs/hojinzei-shinkokusho.md)（[完全版](https://shiwake.isz.ai/guide/hojinzei-shinkokusho/?utm_source=github&utm_medium=referral)） | 別表の構成と作成の順番、別表四と五(一)の検算、勘定科目内訳明細書・概況書、e-Tax での提出 | [法人税等](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral)・[申告・納付期限カレンダー](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral) |
| [法人の申告・納付期限の一覧](docs/shinkoku-kigen.md)（[完全版](https://shiwake.isz.ai/guide/shinkoku-kigen/?utm_source=github&utm_medium=referral)） | 法人税・消費税・源泉所得税・法定調書・償却資産・算定基礎届・年度更新、延長の特例、延滞税 | [申告・納付期限カレンダー](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral)・[延滞税](https://shiwake.isz.ai/tools/entaizei/?utm_source=github&utm_medium=referral)・[中間申告](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [電子帳簿保存法のスキャナ保存](docs/denchoho.md)（[完全版](https://shiwake.isz.ai/guide/denchoho-scanner/?utm_source=github&utm_medium=referral)） | 解像度200dpi・入力期限・訂正削除の履歴・検索要件、スマホ撮影の注意点 | [領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral) |
| [電子取引データの保存](docs/denshi-torihiki.md)（[完全版](https://shiwake.isz.ai/guide/denshi-torihiki/?utm_source=github&utm_medium=referral)） | メールの PDF・Web 明細の保存義務、改ざん防止、検索要件、猶予措置 | [請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[領収書のAI読み取り](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral) |
| [勘定科目の一覧と仕訳の例](docs/accounts.md)（[完全版](https://shiwake.isz.ai/guide/kanjo-kamoku/?utm_source=github&utm_medium=referral)） | よく使う勘定科目、領収書の仕訳、会議費と交際費（1人1万円） | [勘定科目・仕訳例検索](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)・[会議費・交際費](https://shiwake.isz.ai/tools/kosaihi/?utm_source=github&utm_medium=referral)・[印紙税額の判定](https://shiwake.isz.ai/tools/inshi-zei/?utm_source=github&utm_medium=referral) |

## 税理士のための無料計算ツール

**[shiwake.isz.ai/tools](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)** では、税理士事務所・経理担当者がよく使う計算を無料で使えます。

- **AI読み取り（無料）**: [領収書・レシートのAI読み取り（登録で証憑100枚まで無料）](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)／[請求書のAI読み取り](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)／[通帳・銀行明細のAI読み取り](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)
- **勘定科目**: [勘定科目・仕訳例かんたん検索（155の取引）](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)
- **給与・社会保険**: [給与の源泉徴収税額](https://shiwake.isz.ai/tools/gensen-kyuyo/?utm_source=github&utm_medium=referral)／[社会保険料](https://shiwake.isz.ai/tools/shakai-hoken/?utm_source=github&utm_medium=referral)／[給与の手取り](https://shiwake.isz.ai/tools/kyuyo-tedori/?utm_source=github&utm_medium=referral)／[賞与の源泉徴収](https://shiwake.isz.ai/tools/gensen-shoyo/?utm_source=github&utm_medium=referral)／[年末調整](https://shiwake.isz.ai/tools/nencho/?utm_source=github&utm_medium=referral)
- **報酬**: [報酬・料金の源泉徴収（10.21%・グロスアップ）](https://shiwake.isz.ai/tools/gensen-houshu/?utm_source=github&utm_medium=referral)／[法定調書の提出要否（令和8年分）](https://shiwake.isz.ai/tools/hotei-yohi/?utm_source=github&utm_medium=referral)
- **退職金**: [退職金の税金（退職所得控除・源泉徴収・住民税）](https://shiwake.isz.ai/tools/taishoku/?utm_source=github&utm_medium=referral)
- **所得税・住民税（個人）**: [所得税・住民税の計算](https://shiwake.isz.ai/tools/shotokuzei-juminzei/?utm_source=github&utm_medium=referral)／[ふるさと納税の控除上限額（2026年）](https://shiwake.isz.ai/tools/furusato/?utm_source=github&utm_medium=referral)／[法人成りシミュレーション](https://shiwake.isz.ai/tools/hojinnari/?utm_source=github&utm_medium=referral)
- **年収の壁**: [年収の壁 判定（2026年: 住民税119万円・扶養136万円・所得税178万円・社会保険の扶養130万円／150万円）](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral)
- **消費税・インボイス**: [消費税（税込・税抜・インボイスの端数）](https://shiwake.isz.ai/tools/shohizei/?utm_source=github&utm_medium=referral)／[経過措置](https://shiwake.isz.ai/tools/keika-sochi/?utm_source=github&utm_medium=referral)／[登録番号チェック](https://shiwake.isz.ai/tools/invoice-number/?utm_source=github&utm_medium=referral)／[一般・簡易・2割・3割の比較](https://shiwake.isz.ai/tools/shohizei-hikaku/?utm_source=github&utm_medium=referral)／[中間申告](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral)
- **決算**: [減価償却](https://shiwake.isz.ai/tools/genka-shokyaku/?utm_source=github&utm_medium=referral)／[法人税等](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral)／[会議費・交際費](https://shiwake.isz.ai/tools/kosaihi/?utm_source=github&utm_medium=referral)／[役員報酬の最適額](https://shiwake.isz.ai/tools/yakuin-hoshu/?utm_source=github&utm_medium=referral)／[少額減価償却資産（年300万円）](https://shiwake.isz.ai/tools/shogaku-shisan/?utm_source=github&utm_medium=referral)／[償却資産の固定資産税（免税点180万円）](https://shiwake.isz.ai/tools/shokyaku-shisan/?utm_source=github&utm_medium=referral)
- **延滞税・期限・印紙税**: [延滞税（国税・2026年は2.8%／9.1%）](https://shiwake.isz.ai/tools/entaizei/?utm_source=github&utm_medium=referral)／[法人の申告・納付期限カレンダー（.ics 書き出し）](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral)／[印紙税額の判定](https://shiwake.isz.ai/tools/inshi-zei/?utm_source=github&utm_medium=referral)

ツールの計算は、**国税庁の源泉徴収税額表などの公表資料**と照らし合わせ、第三者の計算サイトの結果とも突き合わせて確認しています。料率・税額表は国税庁・日本年金機構・協会けんぽ・厚生労働省の公表資料から取り込んでいます。

## よくある質問

**Q. AI経理（仕訳AI）とは何ですか？**
A. 領収書や請求書の画像から AI が取引の内容を読み取り、勘定科目・税区分・摘要を付けた仕訳を自動で作る仕組みです。ISZ™ 仕訳AI は、作った仕訳を弥生・freee・マネーフォワード・TKC などの会計ソフトに CSV で取り込めます。

**Q. AI が税務判断まで行いますか？**
A. 行いません。AI は仕訳ドラフトの作成と、確認が必要な箇所の抽出までを担当し、判断と最終確定は税理士・経理担当者が行います。

**Q. 電子帳簿保存法やインボイス制度に対応していますか？**
A. はい。法定3項目（取引年月日・金額・取引先）での検索、訂正削除の履歴、原本と帳簿の相互参照、登録番号の抽出と経過措置の判定に対応しています。

**Q. 2026年10月以降、免税事業者からの仕入はいくら控除できますか？**
A. 2026年10月1日から2028年9月30日までの取引は、消費税相当額の70%です（令和8年度税制改正後）。詳しくは[インボイスと経過措置](docs/invoice.md)をご覧ください。

**Q. 月給が74万円を超えるときの源泉徴収税額は？**
A. 月額表の「740,000円以上」の算式で計算します。令和8年分・扶養0人・社会保険料等控除後 1,063,741円なら 121,820円 ＋（1,063,741円 − 960,000円）× 33.693% = 156,773円です（[源泉徴収税額の計算](docs/withholding-tax.md)）。

**Q. 無料で試せますか？**
A. 新規登録だけで証憑100枚まで無料です（クレジットカード不要）。[こちら](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme)からお試しください。計算ツールも無料です。

**Q. このリポジトリの文章を引用・転載してもよいですか？**
A. はい。CC BY 4.0 で公開しています。出典として「ISZ GROUP（ISZ™ 仕訳AI）」とこのリポジトリへのリンクを示してください。

## 免責事項

このリポジトリの解説は、一般的な計算方法を示すもので、個別の税務相談に代わるものではありません。料率・税額表は毎年改定されることがあり、特例・経過措置・自治体の超過税率などすべてのケースを網羅していません。実際の申告・納付・給与計算では、国税庁などの最新の公表資料を確認し、必要に応じて税理士・社会保険労務士にご相談ください。

## ISZ GROUP について

ISZ™ 仕訳AI は [ISZ.AI](https://isz.ai)（ISZ GROUP）が提供するサービスです。大阪産業局「大阪イノベーションハブ（OIH）」会員企業。

- 公式サイト: [shiwake.isz.ai](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)
- 無料トライアル: [acc.isz.ai](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme)
- 無料計算ツール: [shiwake.isz.ai/tools](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)
- 紹介動画: [YouTube](https://youtu.be/S9SmAAVw3MU)
- GitHub: [github.com/iszgroup](https://github.com/iszgroup)

## ライセンス

このリポジトリの文章・表は [クリエイティブ・コモンズ 表示 4.0 国際（CC BY 4.0）](LICENSE.md) で公開しています。引用・転載・改変するときは、「ISZ GROUP（ISZ™ 仕訳AI）」の表示とこのリポジトリへのリンクをお願いします。「ISZ」「仕訳AI」の名称・ロゴはこのライセンスの対象外です。
