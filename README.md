# India-Stocks-2581-2610-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 2581 to 2610)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-2581-2610-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (2581 to 2610)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 2581 | `WANBURY` | Wanbury Limited | `WANBURY.NS` |
| 2582 | `WARDINMOBI` | Wardwizard Innovations & Mobility Limited | `WARDINMOBI.NS` |
| 2583 | `WATERBASE` | Waterbase Limited | `WATERBASE.NS` |
| 2584 | `WCIL` | Western Carriers (India) Limited | `WCIL.NS` |
| 2585 | `WEALTH` | Wealth First Portfolio Managers Limited | `WEALTH.NS` |
| 2586 | `WEBELSOLAR` | Websol Energy System Limited | `WEBELSOLAR.NS` |
| 2587 | `WEIZMANIND` | Weizmann Limited | `WEIZMANIND.NS` |
| 2588 | `WEL` | Wonder Electricals Limited | `WEL.NS` |
| 2589 | `WELENT` | Welspun Enterprises Limited | `WELENT.NS` |
| 2590 | `WELINV` | Welspun Investments and Commercials Limited | `WELINV.NS` |
| 2591 | `WELSPLSOL` | Welspun Specialty Solutions Limited | `WELSPLSOL.NS` |
| 2592 | `WENDT` | Wendt (India) Limited | `WENDT.NS` |
| 2593 | `WESTLIFE` | WESTLIFE FOODWORLD LIMITED | `WESTLIFE.NS` |
| 2594 | `WEWIN` | WE WIN LIMITED | `WEWIN.NS` |
| 2595 | `WEWORK` | WeWork India Management Limited | `WEWORK.NS` |
| 2596 | `WHBRADY` | WH Brady & Company Limited | `WHBRADY.NS` |
| 2597 | `WHEELS` | Wheels India Limited | `WHEELS.NS` |
| 2598 | `WILLAMAGOR` | Williamson Magor & Company Limited | `WILLAMAGOR.NS` |
| 2599 | `WINDLAS` | Windlas Biotech Limited | `WINDLAS.NS` |
| 2600 | `WINDMACHIN` | Windsor Machines Limited | `WINDMACHIN.NS` |
| 2601 | `WIPL` | The Western India Plywoods Limited | `WIPL.NS` |
| 2602 | `WONDERLA` | Wonderla Holidays Limited | `WONDERLA.NS` |
| 2603 | `WORTHPERI` | Worth Peripherals Limited | `WORTHPERI.NS` |
| 2604 | `WPIL` | WPIL Limited | `WPIL.NS` |
| 2605 | `WSI` | W S Industries (I) Limited | `WSI.NS` |
| 2606 | `WSTCSTPAPR` | West Coast Paper Mills Limited | `WSTCSTPAPR.NS` |
| 2607 | `XCHANGING` | Xchanging Solutions Limited | `XCHANGING.NS` |
| 2608 | `XELPMOC` | Xelpmoc Design And Tech Limited | `XELPMOC.NS` |
| 2609 | `XPROINDIA` | Xpro India Limited | `XPROINDIA.NS` |
| 2610 | `XTGLOBAL` | Xtglobal Infotech Limited | `XTGLOBAL.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream WANBURY 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-2581-2610-Historical-Data/main/WANBURY/1m/2026/10/WANBURY_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
