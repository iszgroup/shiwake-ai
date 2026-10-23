# ISZ™ Shiwake AI — AI bookkeeping automation and a guide to Japanese tax and social insurance calculations (2026)

[![Website](https://img.shields.io/badge/Website-shiwake.isz.ai-0b1f4d.svg)](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)
[![Free trial](https://img.shields.io/badge/Free%20trial-100%20documents%20free-c9a227.svg)](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme-en)
[![Tools](https://img.shields.io/badge/Free%20calculators-shiwake.isz.ai%2Ftools-2e7d32.svg)](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE.md)

[日本語](README.md) ｜ [简体中文](README.zh-CN.md) ｜ [English](README.en.md)

**ISZ™ Shiwake AI (ISZ™ 仕訳AI)** is an **AI bookkeeping service for Japanese tax accounting firms (税理士事務所) and small businesses**. Snap a photo of a receipt, invoice or bank passbook and upload it: the AI reads it and drafts a **journal entry (仕訳)** with the account title, consumption-tax category and description. It exports CSV files that import directly into Japanese accounting software — Yayoi, freee, Money Forward Cloud, TKC and others — and stores the source documents in a form that meets Japan's Electronic Books Preservation Act (電子帳簿保存法).

This repository is a **knowledge base**. It documents the Japanese tax and social insurance rules organized while building ISZ™ Shiwake AI — consumption tax, the qualified invoice system, withholding tax, social insurance premiums, income tax and year-end adjustment, depreciation, corporate tax, electronic record keeping and filing deadlines — with formulas, worked examples and links to primary sources. The guides are written in Japanese.

**[▶ Product details](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)**　｜　**[▶ Free trial (100 documents free, no credit card)](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme-en)**　｜　**[▶ Free calculators](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)**

## What ISZ™ Shiwake AI does

- **Reads source documents and drafts journal entries** — receipts, invoices, card statements and bank passbooks (PDF, photos, ZIP). Each file is named "date_counterparty_amount", and users are warned before sending if one photo contains several documents (to meet the scanner-storage resolution requirement)
- **Smartphone submission from clients** — send a submission link by QR code, email or LINE; no app install or login. Image quality (the resolution requirement of the Electronic Books Preservation Act) is checked on the spot
- **Qualified invoice system** — extracts and validates registration numbers (T + 13 digits), separates the 8% and 10% rates, and applies the transitional credit for purchases from unregistered suppliers (70% from October 2026)
- **Electronic Books Preservation Act** — search by date, amount and counterparty, correction/deletion history, cross-reference between originals and entries (document IDs), and a template for internal rules
- **Bank reconciliation** and a **pre-closing review list** (duplicates, possibly missed withholding, meals over ¥10,000 per person, possible fixed assets, and more)
- **Payroll and year-end adjustment**, **trial balance and financial statements**, and financial-statement CSV for e-Tax
- **Accounting software formats** — Yayoi, freee, Money Forward Cloud, TKC (FX series), JDL and Kanjo Bugyo

**The AI does not make tax judgments.** It drafts entries and flags items that need review (with reasons); accountants make and confirm the final decisions. Tax amounts are not left to generative AI — they are calculated deterministically from published formulas and rates. Uploaded financial data is not used for AI training, and contracts, support and data management are all in Japan.

## Guides (Japanese) and free calculators

| Guide | Topic | Free calculator |
| :--- | :--- | :--- |
| [AI経理とは](docs/ai-keiri.md) | How AI bookkeeping works; what the AI does and what people check | [All tools](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [記帳代行・記帳の自動化](docs/kicho-jidoka.md) | Cutting data entry in accounting firms, collecting documents, CSV import | [All tools](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [消費税の計算](docs/consumption-tax.md) | Tax-inclusive/exclusive conversion, invoice rounding, general/simplified/20%/30% methods | [Consumption tax](https://shiwake.isz.ai/tools/shohizei/?utm_source=github&utm_medium=referral) · [Method comparison](https://shiwake.isz.ai/tools/shohizei-hikaku/?utm_source=github&utm_medium=referral) · [Interim return](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [インボイスの登録番号と経過措置](docs/invoice.md) | Registration number check digit, 80%→70% transitional credit, small-amount relief | [Number check](https://shiwake.isz.ai/tools/invoice-number/?utm_source=github&utm_medium=referral) · [Transitional credit](https://shiwake.isz.ai/tools/keika-sochi/?utm_source=github&utm_medium=referral) |
| [源泉徴収税額の計算](docs/withholding-tax.md) | Monthly withholding table (formula for ¥740,000 and above), bonuses, fees at 10.21% | [Salary](https://shiwake.isz.ai/tools/gensen-kyuyo/?utm_source=github&utm_medium=referral) · [Bonus](https://shiwake.isz.ai/tools/gensen-shoyo/?utm_source=github&utm_medium=referral) · [Fees](https://shiwake.isz.ai/tools/gensen-houshu/?utm_source=github&utm_medium=referral) |
| [社会保険料の計算](docs/social-insurance.md) | Standard monthly remuneration; health, nursing care, child support levy, pension, employment insurance (FY2026) | [Social insurance](https://shiwake.isz.ai/tools/shakai-hoken/?utm_source=github&utm_medium=referral) · [Take-home pay](https://shiwake.isz.ai/tools/kyuyo-tedori/?utm_source=github&utm_medium=referral) |
| [所得税と年末調整](docs/income-tax.md) | Income tax brackets, employment income deduction, basic deduction (2026) | [Year-end adjustment](https://shiwake.isz.ai/tools/nencho/?utm_source=github&utm_medium=referral) |
| [減価償却の計算](docs/depreciation.md) | Straight-line and 200% declining balance; small assets under ¥400,000 | [Depreciation](https://shiwake.isz.ai/tools/genka-shokyaku/?utm_source=github&utm_medium=referral) |
| [法人税等の計算](docs/corporate-tax.md) | SME corporate tax 15%/23.2%, local corporate tax, defense surtax, inhabitant and enterprise taxes | [Corporate tax](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral) |
| [法人の申告・納付期限](docs/shinkoku-kigen.md) | Corporate filing and payment deadlines, extensions, withholding, annual information returns | [Interim return](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [電子帳簿保存法のスキャナ保存](docs/denchoho.md) | Scanning requirements: 200 dpi, input deadlines, history, search | — |
| [電子取引データの保存](docs/denshi-torihiki.md) | Keeping emailed PDFs and web statements electronically; search; grace measure | — |
| [勘定科目の一覧と仕訳の例](docs/accounts.md) | Common account titles, receipt entries, meeting vs. entertainment expenses (¥10,000 per person) | [Meeting/entertainment](https://shiwake.isz.ai/tools/kosaihi/?utm_source=github&utm_medium=referral) |

## FAQ

**Q. Which accounting software does it support?**
A. Import formats for Yayoi, freee, Money Forward Cloud, TKC (FX series), JDL and Kanjo Bugyo.

**Q. Is there a free trial?**
A. Yes — 100 documents free on sign-up, no credit card. [Sign up here](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme-en).

**Q. How much input tax can be credited on purchases from unregistered suppliers after October 2026?**
A. 70% of the tax-equivalent amount for transactions from 1 October 2026 to 30 September 2028.

**Q. How is withholding tax calculated on monthly pay of ¥740,000 or more?**
A. With the formula in the monthly table: the tax at the start of the bracket plus a percentage of the excess. For 2026 with no dependents and ¥1,063,741 after social insurance: ¥121,820 + (¥1,063,741 − ¥960,000) × 33.693% = ¥156,773.

## Disclaimer

These guides explain general calculation methods and are not individual tax advice. Rates and tables change; always check the latest publications of the National Tax Agency and other authorities, and consult a licensed tax accountant (税理士) or labor and social security attorney (社会保険労務士) where needed.

## About ISZ GROUP

ISZ™ Shiwake AI is provided by [ISZ.AI](https://isz.ai) (ISZ GROUP), a member of the Osaka Innovation Hub (OIH). Website: [shiwake.isz.ai](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral) ｜ [Intro video](https://youtu.be/S9SmAAVw3MU)

## License

Text and tables are licensed under [CC BY 4.0](LICENSE.md). When quoting, republishing or adapting, credit "ISZ GROUP (ISZ™ Shiwake AI)" and link to this repository. The names and logos "ISZ" and "仕訳AI" are not covered by this license.
