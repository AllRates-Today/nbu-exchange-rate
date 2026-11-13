# National Bank of Ukraine Exchange Rates API — nbu-exchange-rate

[![npm version](https://img.shields.io/npm/v/nbu-exchange-rate.svg)](https://www.npmjs.com/package/nbu-exchange-rate)
[![license](https://img.shields.io/npm/l/nbu-exchange-rate.svg)](https://github.com/AllRates-Today/nbu-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/nbu-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![USD/UAH today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fnbu%3Fsource%3DUSD%26target%3DUAH&query=%24.rate&label=USD%2FUAH%20official%2C%20National%20Bank%20of%20Ukraine&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/nbu/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fnbu%3Fsource%3DUSD%26target%3DUAH&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/nbu/)

**Official National Bank of Ukraine (Ukraine) daily exchange rates for Node.js and TypeScript. The published central bank rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers National Bank of Ukraine itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official rates** — National Bank of Ukraine's own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 1996** — point-in-time tables and daily series for any past date
- 🔀 **Official vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number National Bank of Ukraine itself published, fixed once printed and carrying the central bank's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## 📈 Latest official table

[![Latest National Bank of Ukraine table](https://allratestoday.com/api/open/central-bank/nbu/table.svg)](https://allratestoday.com/central-bank-rates-api/nbu/)

The image is rendered live from the keyless endpoint, so it follows the central bank's publications on npm and on GitHub alike without a new release. The same table as text is folded below for search and copy-paste: on GitHub [a daily Action](.github/workflows/daily-table.yml) refreshes it whenever the central bank publishes a new table; on npm it is as of the package's publish date.

<!-- daily-table:start -->
<details>
<summary>Table as text: published 2026-11-13 by National Bank of Ukraine — 45 rates. Updated 2026-11-13.</summary>

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| AED | UAH | reference | 12.3563 |
| AUD | UAH | reference | 30.9829 |
| AZN | UAH | reference | 26.697 |
| BDT | UAH | reference | 0.3626 |
| CAD | UAH | reference | 31.8489 |
| CHF | UAH | reference | 54.5492 |
| CNY | UAH | reference | 6.8053 |
| CZK | UAH | reference | 2.0659 |
| DKK | UAH | reference | 6.7338 |
| DZD | UAH | reference | 0.33204 |
| EGP | UAH | reference | 0.8484 |
| EUR | UAH | reference | 50.3379 |
| GBP | UAH | reference | 60.2241 |
| GEL | UAH | reference | 17.4937 |
| HKD | UAH | reference | 5.7855 |
| HUF | UAH | reference | 0.138171 |
| IDR | UAH | reference | 0.0024885 |
| ILS | UAH | reference | 14.2688 |
| INR | UAH | reference | 0.48274 |
| JPY | UAH | reference | 0.28423 |
| KRW | UAH | reference | 0.034058 |
| KZT | UAH | reference | 0.102337 |
| LBP | UAH | reference | 0.000507 |
| MDL | UAH | reference | 2.4985 |
| MXN | UAH | reference | 2.439 |
| MYR | UAH | reference | 11.1268 |
| NOK | UAH | reference | 4.7512 |
| NZD | UAH | reference | 25.2371 |
| PLN | UAH | reference | 11.4334 |
| RON | UAH | reference | 9.4165 |
| RSD | UAH | reference | 0.42793 |
| SAR | UAH | reference | 12.0929 |
| SEK | UAH | reference | 4.5551 |
| SGD | UAH | reference | 35.3182 |
| THB | UAH | reference | 1.34342 |
| TND | UAH | reference | 14.9909 |
| TRY | UAH | reference | 0.903 |
| USD | UAH | reference | 45.3849 |
| VND | UAH | reference | 0.0017672 |
| XAG | UAH | reference | 2317.82 |
| XAU | UAH | reference | 178964.24 |
| XDR | UAH | reference | 61.229 |
| XPD | UAH | reference | 46437.46 |
| XPT | UAH | reference | 69452.14 |
| ZAR | UAH | reference | 2.7267 |

</details>

Source: [Official rates published by NBU, served by AllRatesToday](https://allratestoday.com/central-bank-rates-api/nbu/). Rates are as printed by the central bank; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 📦 Installation

```bash
npm install nbu-exchange-rate
```

```bash
yarn add nbu-exchange-rate
```

```bash
pnpm add nbu-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/nbu-exchange-rate`](https://www.npmjs.com/package/@allratestoday/nbu-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'nbu-exchange-rate';

const pair = await getRate('USD', 'UAH', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official National Bank of Ukraine rate, on the central bank's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest official table
- [Full official table](#full-official-table) — everything the central bank printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the central bank does not print directly are resolved from its table and flagged (see *Official vs derived rates* below).

```js
const pair = await getRate('USD', 'UAH', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'nbu',
  name: 'National Bank of Ukraine',
  rate_date: '2026-11-11',   // National Bank of Ukraine's own publication date
  source: 'USD',
  target: 'UAH',
  rate: 45.5013,
  rate_type: 'reference',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full official table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'nbu-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'nbu',
  name: 'National Bank of Ukraine',
  rate_date: '2026-11-11',
  rates: [
    { "base": "USD", "quote": "UAH", "type": "reference", "value": 45.5013 },
    // … the rest of the official table (45 currencies vs UAH)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 1996 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'nbu-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'USD', target: 'UAH' });
```

**Response:**

```javascript
{
  bank: 'nbu',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'nbu-exchange-rate';

const series = await getHistory(
  { source: 'USD', target: 'UAH', from: '2026-01-01', to: '2026-11-11' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'nbu',
  source: 'USD',
  target: 'UAH',
  from: '2026-01-01',
  to: '2026-11-11',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-11-11', rate: 45.5013, rate_type: 'reference', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'USD' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

National Bank of Ukraine currently publishes rates covering **45 currencies** against the UAH (as of the latest table):

🇦🇪 `AED` · 🇦🇺 `AUD` · 🇦🇿 `AZN` · 🇧🇩 `BDT` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇳 `CNY` · 🇨🇿 `CZK` · 🇩🇰 `DKK` · 🇩🇿 `DZD` · 🇪🇬 `EGP` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇬🇪 `GEL` · 🇭🇰 `HKD` · 🇭🇺 `HUF` · 🇮🇩 `IDR` · 🇮🇱 `ILS` · 🇮🇳 `INR` · 🇯🇵 `JPY` · 🇰🇷 `KRW` · 🇰🇿 `KZT` · 🇱🇧 `LBP` · 🇲🇩 `MDL` · 🇲🇽 `MXN` · 🇲🇾 `MYR` · 🇳🇴 `NOK` · 🇳🇿 `NZD` · 🇵🇱 `PLN` · 🇷🇴 `RON` · 🇷🇸 `RSD` · 🇸🇦 `SAR` · 🇸🇪 `SEK` · 🇸🇬 `SGD` · 🇹🇭 `THB` · 🇹🇳 `TND` · 🇹🇷 `TRY` · 🇺🇸 `USD` · 🇻🇳 `VND` · `XAG` · `XAU` · `XDR` · `XPD` · `XPT` · 🇿🇦 `ZAR`

## 🏛️ Source

The National Bank of Ukraine sets the hryvnia's official exchange rates for around 45 currencies each business day — published in the afternoon for the next working day, and the legally mandated reference for Ukrainian accounting and customs.

- Publisher's own page: [Official hryvnia exchange rates](https://bank.gov.ua/en/markets/exchangerates) · [bank.gov.ua/en](https://bank.gov.ua/en/)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [National Bank of Ukraine rates page](https://allratestoday.com/central-bank-rates-api/nbu/)
- In the API: usually by **13:25 UTC** (measured over the last 11 publications). Schedule a sync at or after that time and retry hourly until `rate_date` moves; every response carries the same figure as `available_by_utc` — see [when to poll](https://allratestoday.com/docs/#when-to-poll)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- National Bank of Ukraine quotes **UAH per 1 unit of foreign currency** (e.g. `base: "USD", quote: "UAH"` means UAH per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- Precious-metal codes (`XAU`, `XAG`, `XPT`, `XPD`) are quoted **per troy ounce**.
- `rate_type` tells you which of the central bank's series a row belongs to (`reference` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official National Bank of Ukraine rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/nbu/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('nbu')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate nbu ...` command
- Evaluating? Agents can self-issue a trial key with no signup: `POST https://allratestoday.com/api/agent/keys` (send `Content-Type: application/json`) returns a 100-call key valid 7 days that covers the free-plan methods (latest table, pairs); dated tables and history need a [paid plan](https://allratestoday.com/pricing/). The MCP servers expose it as `request_trial_key`
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Official vs derived rates

If National Bank of Ukraine does not print a pair directly, the API resolves it from the central bank's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The central bank printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via UAH from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('USD', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by National Bank of Ukraine |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'nbu-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('nbu-exchange-rate');

getRate('USD', 'UAH', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the official table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the official table |
| `getLatestRates({ apiKey })` | Free | The central bank's full latest official table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 1996 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same official tables are mirrored daily as open data:

- Hugging Face: [AllRatesToday/central-bank-exchange-rates](https://huggingface.co/datasets/AllRatesToday/central-bank-exchange-rates) — one CSV per institution (`rates/nbu.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- Raw JSON on GitHub: `https://raw.githubusercontent.com/AllRates-Today/central-bank-exchange-rates/main/data/nbu/latest.json`

## 🔗 Links

- **Website:** [allratestoday.com](https://allratestoday.com)
- [National Bank of Ukraine rates page](https://allratestoday.com/central-bank-rates-api/nbu/) — live table, publication cadence, FAQ
- [All central bank sources](https://allratestoday.com/central-bank-rates-api/) · [Full list of 130+ central banks and tax authorities](https://allratestoday.com/central-bank-rates-api/institutions/) — one API, the same response shape for every source
- [Download central bank rates](https://allratestoday.com/download-central-bank-rates/) — every bank's latest table and history as Excel, CSV or JSON
- [Package docs on the site](https://allratestoday.com/docs/sdk/nbu-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (Free)](https://allratestoday.com/register) · [Dashboard](https://allratestoday.com/profile) · [Pricing](https://allratestoday.com/pricing/)
- [Status](https://allratestoday.com/status)
- [Postman collection](https://allratestoday.com/postman/)
- [ChatGPT app](https://chatgpt.com/plugins/plugin_asdk_app_6ae1e76098f48191a285ac3f5ab7a83b) — ask ChatGPT for live and official central bank rates
- [OpenAPI reference on Bump.sh](https://bump.sh/allratestoday/doc/allratestoday-api) — also on [SwaggerHub](https://app.swaggerhub.com/apis-docs/allratestoday/allratestoday-exchange-rate-central-bank-rates-api/2.2.0)
- [GitHub](https://github.com/AllRates-Today/nbu-exchange-rate)

## 📜 License

MIT
