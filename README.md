# Crypto exchange register data (Takame)

## What this is

What official financial registers say about crypto exchanges, as read by [Takame](https://takame.io), plus Takame's own mapping from the companies on those registers to the exchange brands people know. Updated daily; the git history is the version history.

## Sources, their terms, and how to credit them

Takame's own layer (exchange mapping, statuses, change log, file structure) is CC BY 4.0: credit "Takame (takame.io)". Data taken from a register keeps that register's terms. Only registers whose terms allow republishing are included; details in [SOURCES.md](SOURCES.md).

| Code | Register | Terms | Credit as |
|---|---|---|---|
| `ESMA_MICA` | ESMA interim MiCA register: authorised CASPs | [ESMA legal notice: reproduction authorised provided the source is acknowledged](https://esma.europa.eu/legal-notice) | Source: European Securities and Markets Authority (ESMA), interim MiCA register. |
| `ESMA_MICA_NCA` | ESMA interim MiCA register: non-compliant entities | [ESMA legal notice: reproduction authorised provided the source is acknowledged](https://esma.europa.eu/legal-notice) | Source: European Securities and Markets Authority (ESMA), interim MiCA register. |
| `AMF_FR` | AMF white list of digital asset service providers (France) | [Licence Ouverte / Open Licence 2.0 (Etalab)](https://www.data.gouv.fr/pages/legal/licences/etalab-2.0) | Source: Autorité des marchés financiers (AMF), data.gouv.fr, with the date of last update. |
| `FSA_JP` | Japan FSA list of registered crypto-asset exchange service providers | [Public Data License 1.0 (PDL1.0); edits must be disclosed](https://www.fsa.go.jp/rules/) | 出典：金融庁「暗号資産交換業者登録一覧」（Takame が加工して作成） |
| `FSA_JP_WARNING` | Japan FSA warnings to unregistered operators | [Public Data License 1.0 (PDL1.0); edits must be disclosed](https://www.fsa.go.jp/rules/) | 出典：金融庁「無登録で暗号資産交換業を行う者の名称等について」（Takame が加工して作成） |
| `FINCEN_US` | FinCEN MSB Registrant Search (crypto-related registrants read by Takame) | [CC0 on data.gov](https://catalog.data.gov/dataset/money-services-business-msb-registrant-search) | Source: Financial Crimes Enforcement Network (FinCEN), MSB Registrant Search. |
| `FSC_TW` | Taiwan FSC list of VASPs that completed AML registration | [Open Government Data License, version 1.0 (Taiwan)](https://data.gov.tw/license) | 資料來源：金融監督管理委員會證券期貨局「提供虛擬資產服務之事業或人員」名單 |
| `BSP_PH` | Bangko Sentral ng Pilipinas list of VASPs | [BSP Terms of Use: reuse with credit; commercial reuse must say the content is freely available on the BSP website and mark changes](https://www.bsp.gov.ph/Pages/AboutTheBank/Terms-of-Use.aspx) | Source: Bangko Sentral ng Pilipinas (BSP). This information is freely available on the BSP website; Takame reformatted it. |

Registers whose terms do not allow republishing (UK FCA, Singapore MAS, Hong Kong SFC, Dubai VARA, Malaysia SC) or are unclear (Canada FINTRAC, India FIU-IND, Indonesia OJK, Korea FIU) appear only as a register name and a link to their own page.

## Read this before using the data

- **This is not legal advice.** It reports what each register says, on the date Takame last read it.
- **Missing from this data does not mean unlicensed.** An exchange can be licensed under another company name, in a register Takame does not read, or in a country that does not require registration.
- **`name_match_unconfirmed`** means a company with a matching name is on the register, but Takame has not confirmed it is the same business.
- Natural persons are removed. Rankings on takame.io are never sold, and nothing here is a rating of safety.

## Files

| File | Rows | What it is |
|---|---|---|
| `exchanges.csv` | 1005 | One row per exchange × jurisdiction Takame reads: the status Takame shows (licensed, unconfirmed, flagged, self-filed, withdrawn, absent). |
| `exchange_records.csv` | 161 | Every register record Takame links to an exchange. Company name and number only where the register's terms allow it. |
| `changes.csv` | 1 | Changes Takame recorded in the registers, each with a permanent link. |
| `registers/<CODE>.csv` | 939 | Records from the registers listed above. |
| `register_reads.csv` | 8 | When Takame last read each register successfully. |
