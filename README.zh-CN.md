# ISZ™ 仕訳AI — AI 记账自动化，以及日本税务・社会保险计算指南（2026 年版）

[![Website](https://img.shields.io/badge/官网-shiwake.isz.ai-0b1f4d.svg)](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)
[![Free trial](https://img.shields.io/badge/免费试用-凭证100张免费-c9a227.svg)](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme-zh)
[![Tools](https://img.shields.io/badge/免费计算工具-shiwake.isz.ai%2Ftools-2e7d32.svg)](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE.md)

[日本語](README.md) ｜ [简体中文](README.zh-CN.md) ｜ [English](README.en.md)

**ISZ™ 仕訳AI（Shiwake AI）** 是面向日本税理士事务所和中小企业的 **AI 记账（仕訳自动生成）服务**。拍下收据、发票、存折等凭证并上传，AI 会读取内容，生成带有会计科目、税区分和摘要的**会计分录**，并输出可直接导入弥生会计・freee・Money Forward Cloud・TKC 等日本会计软件的 CSV，同时保存符合《电子账簿保存法》的凭证数据。

本仓库是一个**知识库**：把开发 ISZ™ 仕訳AI 过程中整理的日本税务与社会保险的计算方法和实务知识（消费税・发票制度・源泉征收・社会保险费・所得税・年末调整・折旧・法人税・电子账簿保存法・申报期限），附上计算公式、算例和一次资料出处。正文为日语。

**[▶ 产品详情](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral)**　｜　**[▶ 免费试用（凭证 100 张免费，无需信用卡）](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme-zh)**　｜　**[▶ 免费计算工具](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)**　｜　**[▶ 会计科目・分录示例检索](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)**

## ISZ™ 仕訳AI 能做什么

- **读取凭证并生成分录** — 收据・小票・请求书・信用卡明细・存折（PDF・照片・ZIP），并按「日期_交易方_金额」命名文件；为满足电子账簿保存法的分辨率要求，一张照片里拍了多张单据时会在发送前提示
- **客户用手机提交** — 只需把提交链接通过二维码・邮件・LINE 发给客户，无需安装 App、无需登录，拍照时当场检查画质（电子账簿保存法的分辨率要求）
- **发票制度（インボイス）** — 提取并校验登记号码（T 号码）、区分 8%/10% 税率、判定从免税事业者采购的过渡措置（2026 年 10 月起可抵扣 70%）
- **电子账簿保存法** — 按交易日期・金额・交易方检索，保留修改删除履历，原件与分录互相对应（凭证 ID），提供事务处理规程模板
- **与银行明细核对**、**决算前待确认清单**（重复计账、源泉征收遗漏候选、人均超过 1 万日元的餐饮费、应资本化的候选等）
- **工资计算・年末调整**、**试算表・决算书**、e-Tax 用财务报表 CSV
- **申报书**：法人税别表・科目明细书（内訳書）・法人事业概况说明书、地方税（第六号・第二十号样式）、消费税申报书，按国税厅等官方样式生成；法人税・消费税另可输出 e-Tax 申报数据（.xtx），由税理士确认、电子签名后提交
- **会计软件对接** — 弥生会计・freee 会计・Money Forward Cloud 会计・TKC（FX 系列）・JDL・勘定奉行

**AI 不做税务判断。** AI 只负责生成分录草稿并列出需要确认的地方（附理由），科目与税区分的最终判断由税理士或会计人员完成。税额等金额不交给生成式 AI，而是按公开的公式和费率确定性地计算。上传的财务数据不会用于 AI 训练，合同・支持・数据管理均在日本国内。

## 指南与免费工具

| 指南（日语） | 内容 | 免费工具 |
| :--- | :--- | :--- |
| [AI経理とは](docs/ai-keiri.md)（[完整版](https://shiwake.isz.ai/guide/ai-jidou-shiwake/?utm_source=github&utm_medium=referral)） | AI 记账的原理，AI 负责什么、人负责什么 | [收据 AI 识别](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[请求书 AI 识别](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[存折 AI 识别](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)・[工具一览](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [記帳代行・記帳の自動化](docs/kicho-jidoka.md)（[完整版](https://shiwake.isz.ai/guide/kicho-jidoka/?utm_source=github&utm_medium=referral)） | 税理士事务所如何减少录入工作、凭证回收、会计软件 CSV 导入 | [收据 AI 识别](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[请求书 AI 识别](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[存折 AI 识别](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)・[工具一览](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral) |
| [消費税の計算](docs/consumption-tax.md)（[完整版](https://shiwake.isz.ai/guide/shohizei/?utm_source=github&utm_medium=referral)） | 含税・不含税换算、发票的尾数处理、一般・简易课税・2 成特例・3 成特例 | [消费税](https://shiwake.isz.ai/tools/shohizei/?utm_source=github&utm_medium=referral)・[方式比较](https://shiwake.isz.ai/tools/shohizei-hikaku/?utm_source=github&utm_medium=referral)・[中间申报](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [インボイスの登録番号と経過措置](docs/invoice.md)（[完整版](https://shiwake.isz.ai/guide/invoice/?utm_source=github&utm_medium=referral)） | T 号码校验位、80%→70% 抵扣、小额特例 | [登记号码校验](https://shiwake.isz.ai/tools/invoice-number/?utm_source=github&utm_medium=referral)・[过渡措置](https://shiwake.isz.ai/tools/keika-sochi/?utm_source=github&utm_medium=referral)・[请求书 AI 识别](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral) |
| [源泉徴収税額の計算](docs/withholding-tax.md)（[完整版](https://shiwake.isz.ai/guide/gensen-choshu/?utm_source=github&utm_medium=referral)） | 工资月额表（74 万日元以上的算式）、电算机计算特例、奖金、报酬 10.21% | [工资](https://shiwake.isz.ai/tools/gensen-kyuyo/?utm_source=github&utm_medium=referral)・[奖金](https://shiwake.isz.ai/tools/gensen-shoyo/?utm_source=github&utm_medium=referral)・[报酬](https://shiwake.isz.ai/tools/gensen-houshu/?utm_source=github&utm_medium=referral)・[退职金的税金](https://shiwake.isz.ai/tools/taishoku/?utm_source=github&utm_medium=referral) |
| [社会保険料の計算](docs/social-insurance.md)（[完整版](https://shiwake.isz.ai/guide/shakai-hoken/?utm_source=github&utm_medium=referral)） | 标准报酬月额、健康保险・护理保险・育儿支援金・厚生年金・雇用保险（令和 8 年度） | [社会保险费](https://shiwake.isz.ai/tools/shakai-hoken/?utm_source=github&utm_medium=referral)・[到手工资](https://shiwake.isz.ai/tools/kyuyo-tedori/?utm_source=github&utm_medium=referral)・[年收之壁（年収の壁）](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral) |
| [所得税と年末調整](docs/income-tax.md)（[完整版](https://shiwake.isz.ai/guide/shotokuzei-nencho/?utm_source=github&utm_medium=referral)） | 速算表、工资所得扣除、基础扣除、年收之壁（令和 8 年分） | [年收之壁（年収の壁）](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral)・[年末调整](https://shiwake.isz.ai/tools/nencho/?utm_source=github&utm_medium=referral) |
| [減価償却の計算](docs/depreciation.md)（[完整版](https://shiwake.isz.ai/guide/genka-shokyaku/?utm_source=github&utm_medium=referral)） | 定额法・200% 定率法、少额折旧资产（40 万日元未满） | [折旧](https://shiwake.isz.ai/tools/genka-shokyaku/?utm_source=github&utm_medium=referral) |
| [法人税等の計算](docs/corporate-tax.md)（[完整版](https://shiwake.isz.ai/guide/hojinzei/?utm_source=github&utm_medium=referral)） | 中小法人税率 15%・23.2%、地方法人税、防卫特别法人税、住民税・事业税 | [法人税等](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral)・[申报・缴纳期限日历](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral) |
| [法人税申告書の作り方](docs/hojinzei-shinkokusho.md)（[完整版](https://shiwake.isz.ai/guide/hojinzei-shinkokusho/?utm_source=github&utm_medium=referral)） | 别表的构成与填写顺序、别表四与五(一)的核对、科目明细书・概况书、e-Tax 提交 | [法人税等](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral)・[申报・缴纳期限日历](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral) |
| [法人の申告・納付期限](docs/shinkoku-kigen.md)（[完整版](https://shiwake.isz.ai/guide/shinkoku-kigen/?utm_source=github&utm_medium=referral)） | 法人税・消费税・源泉所得税・法定调书・偿却资产申报・算定基础届・年度更新、延滞税 | [申报・缴纳期限日历（.ics）](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral)・[延滞税](https://shiwake.isz.ai/tools/entaizei/?utm_source=github&utm_medium=referral)・[中间申报](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral) |
| [電子帳簿保存法のスキャナ保存](docs/denchoho.md)（[完整版](https://shiwake.isz.ai/guide/denchoho-scanner/?utm_source=github&utm_medium=referral)） | 200dpi、录入期限、修改删除履历、检索要求、手机拍摄要点 | [收据 AI 识别](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)・[请求书 AI 识别](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral) |
| [電子取引データの保存](docs/denshi-torihiki.md)（[完整版](https://shiwake.isz.ai/guide/denshi-torihiki/?utm_source=github&utm_medium=referral)） | 邮件 PDF・网页明细的电子保存义务、检索要求、宽限措置 | [请求书 AI 识别](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)・[收据 AI 识别](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral) |
| [勘定科目の一覧と仕訳の例](docs/accounts.md)（[完整版](https://shiwake.isz.ai/guide/kanjo-kamoku/?utm_source=github&utm_medium=referral)） | 常用会计科目、收据分录、会议费与交际费（人均 1 万日元） | [会计科目・分录示例检索](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)・[会议费・交际费](https://shiwake.isz.ai/tools/kosaihi/?utm_source=github&utm_medium=referral)・[印花税额判定](https://shiwake.isz.ai/tools/inshi-zei/?utm_source=github&utm_medium=referral) |

## 面向税理士的免费工具

**[shiwake.isz.ai/tools](https://shiwake.isz.ai/tools/?utm_source=github&utm_medium=referral)** 上的工具全部免费（页面为日语）。

- **AI 识别（免费）**：[收据・小票 AI 识别（注册即可免费 100 张）](https://shiwake.isz.ai/tools/receipt-ocr/?utm_source=github&utm_medium=referral)／[请求书 AI 识别](https://shiwake.isz.ai/tools/invoice-ocr/?utm_source=github&utm_medium=referral)／[存折・银行明细 AI 识别](https://shiwake.isz.ai/tools/tsucho-ocr/?utm_source=github&utm_medium=referral)
- **会计科目**：[会计科目・分录示例检索（155 种交易）](https://shiwake.isz.ai/tools/kanjo-kamoku/?utm_source=github&utm_medium=referral)
- **工资・社会保险**：[工资源泉征收税额](https://shiwake.isz.ai/tools/gensen-kyuyo/?utm_source=github&utm_medium=referral)／[社会保险费](https://shiwake.isz.ai/tools/shakai-hoken/?utm_source=github&utm_medium=referral)／[到手工资](https://shiwake.isz.ai/tools/kyuyo-tedori/?utm_source=github&utm_medium=referral)／[奖金源泉征收](https://shiwake.isz.ai/tools/gensen-shoyo/?utm_source=github&utm_medium=referral)／[年末调整](https://shiwake.isz.ai/tools/nencho/?utm_source=github&utm_medium=referral)
- **报酬**：[报酬・费用的源泉征收（10.21%・含税倒算）](https://shiwake.isz.ai/tools/gensen-houshu/?utm_source=github&utm_medium=referral)／[法定调书是否需要提交（令和8年分）](https://shiwake.isz.ai/tools/hotei-yohi/?utm_source=github&utm_medium=referral)
- **退职金**：[退职金的税金（退职所得扣除・源泉征收・住民税）](https://shiwake.isz.ai/tools/taishoku/?utm_source=github&utm_medium=referral)
- **个人所得税・住民税**：[所得税・住民税计算](https://shiwake.isz.ai/tools/shotokuzei-juminzei/?utm_source=github&utm_medium=referral)／[故乡纳税（ふるさと納税）扣除上限（2026 年）](https://shiwake.isz.ai/tools/furusato/?utm_source=github&utm_medium=referral)／[个体户转法人（法人成り）模拟](https://shiwake.isz.ai/tools/hojinnari/?utm_source=github&utm_medium=referral)
- **年收之壁**：[年收之壁判定（2026 年：住民税 119 万・扶养 136 万・所得税 178 万・社保扶养 130 万／150 万日元）](https://shiwake.isz.ai/tools/nenshu-kabe/?utm_source=github&utm_medium=referral)
- **消费税・发票**：[消费税（含税・不含税・尾数）](https://shiwake.isz.ai/tools/shohizei/?utm_source=github&utm_medium=referral)／[过渡措置](https://shiwake.isz.ai/tools/keika-sochi/?utm_source=github&utm_medium=referral)／[登记号码校验](https://shiwake.isz.ai/tools/invoice-number/?utm_source=github&utm_medium=referral)／[一般・简易・2 成・3 成比较](https://shiwake.isz.ai/tools/shohizei-hikaku/?utm_source=github&utm_medium=referral)／[中间申报](https://shiwake.isz.ai/tools/chukan-shinkoku/?utm_source=github&utm_medium=referral)
- **决算**：[折旧](https://shiwake.isz.ai/tools/genka-shokyaku/?utm_source=github&utm_medium=referral)／[法人税等](https://shiwake.isz.ai/tools/hojinzei/?utm_source=github&utm_medium=referral)／[会议费・交际费](https://shiwake.isz.ai/tools/kosaihi/?utm_source=github&utm_medium=referral)／[董事报酬最优额](https://shiwake.isz.ai/tools/yakuin-hoshu/?utm_source=github&utm_medium=referral)／[少额折旧资产（年 300 万上限）](https://shiwake.isz.ai/tools/shogaku-shisan/?utm_source=github&utm_medium=referral)／[折旧资产固定资产税（免税点 180 万）](https://shiwake.isz.ai/tools/shokyaku-shisan/?utm_source=github&utm_medium=referral)
- **延滞税・期限・印花税**：[延滞税（国税・2026 年为 2.8%／9.1%）](https://shiwake.isz.ai/tools/entaizei/?utm_source=github&utm_medium=referral)／[法人申报・缴纳期限日历（可导出 .ics）](https://shiwake.isz.ai/tools/shinkoku-kigen/?utm_source=github&utm_medium=referral)／[印花税额判定](https://shiwake.isz.ai/tools/inshi-zei/?utm_source=github&utm_medium=referral)

## 常见问题

**Q. ISZ™ 仕訳AI 支持哪些会计软件？**
A. 弥生会计・freee 会计・Money Forward Cloud 会计・TKC（FX 系列）・JDL・勘定奉行的导入格式。

**Q. 可以免费试用吗？**
A. 注册即可免费处理 100 张凭证，无需信用卡。[点此注册](https://acc.isz.ai/login?tab=register&utm_source=github&utm_medium=referral&utm_campaign=readme-zh)。

**Q. 2026 年 10 月以后，从没有登记号码的事业者采购，能抵扣多少消费税？**
A. 2026 年 10 月 1 日至 2028 年 9 月 30 日的交易，可抵扣消费税相当额的 70%。

**Q. 工资超过 74 万日元时源泉征收税额怎么算？**
A. 使用月额表「740,000 円以上」栏的算式：区间起点的税额 ＋ 超出部分 × 税率。例如令和 8 年分、扶养 0 人、扣除社保后 1,063,741 日元 → 121,820 ＋（1,063,741 − 960,000）× 33.693% ＝ 156,773 日元。

## 免责声明

本仓库内容仅说明一般计算方法，不能替代个别税务咨询。费率与税额表每年可能修订。实际申报与工资计算请以国税厅等机构的最新公开资料为准，必要时请咨询税理士或社会保险劳务士。

## 关于 ISZ GROUP

ISZ™ 仕訳AI 由 [ISZ.AI](https://isz.ai)（ISZ GROUP）提供，大阪产业局「大阪创新中心（OIH）」会员企业。官网 [shiwake.isz.ai](https://shiwake.isz.ai/?utm_source=github&utm_medium=referral) ｜ [介绍视频](https://youtu.be/S9SmAAVw3MU)

## 许可

文字与表格以 [CC BY 4.0](LICENSE.md) 公开。引用・转载・改编时请注明「ISZ GROUP（ISZ™ 仕訳AI）」并附上本仓库链接。「ISZ」「仕訳AI」名称与标志不在许可范围内。
