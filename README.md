# Ow1nomic's DataNest- 11 Bangladesh Listed Banks (August/26) — Financial Dataset (2015–2025)

⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣀⣀⣄⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀               Contact: kmmiadhassanornob@gmail.com
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⣶⣾⣿⣿⣿⣿⣿⣶⡆⠀⠀⠀⠀⠀⠀               ------------------- 
⠀⠀⠀⠀⠀⠀⠀⠀⠀⢰⡏⢤⡎⣿⣿⢡⣶⢹⣧⠀⠀⠀⠀⠀⠀               Banks: 11 
⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⣿⣶⣶⣇⣸⣷⣶⣾⣿⠀⠀⠀⠀⠀⠀               Last Date Updated: August 3rd,2026
⠀⠀⠀⠀⠀⠀⠀⠀⠀⢨⣿⣿⣿⢟⣿⣿⣿⣿⣿⣧⡀⠀⠀⠀⠀               Data Type: MD , CSV , ODE
⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⣿⣿⡏⣿⣿⣿⣿⣿⣿⣿⣿⡄⠀⠀⠀               Revision No.: 29
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠘⣿⣿⣿⣜⠿⣿⣿⣿⣿⣿⣿⣿⡄⠀⠀               Total Packages: 16 
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠐⣷⣿⡿⣷⣮⣙⠿⣿⣿⣿⣿⣿⡄⠀               Open source : Yes 
⠀⠀⠠⢄⣀⡀⠀⠀⠀⠀⠀⠈⠫⡯⢿⣿⣿⣿⣶⣯⣿⣻⣿⣿⠀               Copyright: CC0 
⠀⠀⠤⢆⠆⠈⠉⠳⠤⣄⡀⠀⠀⠀⠙⢻⣿⣿⠿⠿⠿⢻⣿⠙⠇               
⠠⠤⠀⣉⣁⣢⣄⣀⣀⣤⣿⠷⠦⠤⣠⡶⠿⣟⠀⠀⠀⠀⠻⡀⠀               
⠀⠀⠔⠋⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠃⠃⠉⠉⠛⠛⠿⢷⡶⠀⠀               
   ___         _     _  _        _      
  / _ \__ __ _/ |___| \| |___ __| |_    G
 | (_) \ V  V / |___| .` / -_|_-<  _|   
  \___/ \_/\_/|_|   |_|\_\___/__/\__|
                                                                
                                                                
Annual financial and performance data for **11 publicly listed commercial banks in Bangladesh**, covering fiscal years **2015 through 2025**. The dataset combines core balance sheet and income statement figures, per-share and profitability ratios, asset quality and capital metrics, plus a set of derived/statistical indicators (growth rates, drawdowns, risk-adjusted return ratios) calculated per bank.

## Banks covered

1. City Bank PLC
2. IFIC Bank PLC
3. Bank Asia PLC
4. BRAC Bank PLC
5. Dutch-Bangla Bank PLC
6. Eastern Bank PLC
7. Mutual Trust Bank PLC (MTB)
8. Prime Bank PLC
9. Mercantile Bank PLC
10. Southeast Bank PLC
11. Pubali Bank PLC

## Repository structure

```
data/
├── raw/
│   └── DATASET_11_BANKS_2025-2015_.xlsx     # Original workbook, one sheet per bank
└── csv/
    ├── all_banks_long.csv                   # Tidy/long format — every metric, every bank, every year, one row each
    ├── all_banks_summary_stats.csv          # Pre-computed summary statistics per bank (see below)
    └── per_bank/
        ├── City_Bank.csv
        ├── IFIC_Bank.csv
        ├── Bank_Asia_Ltd.csv
        ├── BRAC_Bank_Ltd.csv
        ├── Dutch-Bangla_Bank_PLC.csv
        ├── Eastern_Bank_Ltd.csv
        ├── Mutual_Trust_Bank.csv
        ├── Prime_Bank_PLC.csv
        ├── Mercantile_Bank_Ltd.csv
        ├── Southeast_Bank_PLC.csv
        └── Pubali_Bank_PLC.csv
```

- **`raw/`** keeps the original `.xlsx` exactly as provided, for anyone who wants the source formatting/formulas.
- **`csv/per_bank/`** has one clean wide-format CSV per bank (`Category, Metric, Unit, 2025 … 2015`) — easiest for opening a single bank in Excel/Sheets.
- **`csv/all_banks_long.csv`** is the recommended file for analysis (pandas, R, SQL, Power BI, etc.) — every observation is a single row: `Bank, Category, Metric, Unit, Year, Value`.
- **`csv/all_banks_summary_stats.csv`** contains the pre-computed, per-bank statistics described below.

## Metrics included (per bank, per year, 2015–2025)

**Balance Sheet** (Tk mn)
- Total Assets
- Loans & Advances, gross
- Total Deposits
- Shareholders' Equity

**Income Statement** (Tk mn)
- Net Interest Income
- Non-Interest Income
- Net Profit After Tax (NPAT)

**Per-Share & Profitability**
- EPS (BDT)
- ROA % (Return on Assets)
- ROE % (Return on Equity)

**Asset Quality**
- NPL % (gross)
- NPL amount (Tk mn)
- Provision Coverage %
- Loan-Deposit Ratio %

**Capital & Efficiency**
- Capital Adequacy Ratio %
- Cost-to-Income Ratio %

**Derived Metrics** (calculated in the source workbook)
- NPL / Total Assets %
- YoY NPAT growth %
- YoY Total Assets growth %

## Summary statistics (per bank)

Each bank sheet also includes pre-computed summary statistics, carried into `all_banks_summary_stats.csv`:

- Mean ROE % (2015–2025)
- Std Dev ROE % (2015–2025)
- Sharpe-like ratio (risk-free rate = 3%, full period)
- Rolling mean ROE % (2019–2024 window)
- Rolling std dev ROE % (2019–2024)
- Rolling Sharpe-like ratio (2019–2024)
- Equity CAGR % (2015–2025)
- Max drawdown in NPAT %, 2015–2025 (peak-to-trough) *(most banks)*
- Newey-West (HAC) trend regression: NPL% vs. year, slope *(most banks)*

> Note: not every summary statistic is present for every bank — a small number of sheets omit one or two of the items above.

## Data quality notes

- Figures are sourced/compiled from published annual reports and financial statements of each bank; always cross-check against the bank's official disclosures before using this data for investment or research decisions.
- 2025 figures may reflect the latest available reporting period at time of compilation and could be provisional/unaudited for some banks.
- "Tk mn" = Bangladeshi Taka, in millions.
- Some derived/ratio fields in the raw workbook are stored as decimals rather than percentages (e.g. `0.113` for an 11.3% CAGR) — check the `Unit` column and scale accordingly before charting.

## Suggested uses

- Time-series analysis of bank profitability, asset quality, and capital adequacy trends in Bangladesh's banking sector
- Cross-bank comparison / peer benchmarking
- Academic research, teaching material for finance/economics courses
- Dashboards and visualizations (Power BI, Tableau, Python/R notebooks)

## Quick start (Python)

```python
import pandas as pd

df = pd.read_csv("data/csv/all_banks_long.csv")

# ROE trend for one bank
roe = df[(df.Bank == "City Bank") & (df.Metric == "ROE %")]
print(roe[["Year", "Value"]].sort_values("Year"))

# Compare Total Assets across all banks for 2025
assets_2025 = df[(df.Metric == "Total Assets") & (df.Year == 2025)]
print(assets_2025[["Bank", "Value"]].sort_values("Value", ascending=False))
```

## License

Released under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — free to use, share, and adapt for any purpose, including commercial use, with no attribution required. Attribution to this repository is appreciated but not mandatory. See [`LICENSE`](LICENSE).

## Disclaimer

This dataset is provided for informational and research purposes only. It is **not** financial advice. While care has been taken in compiling and cleaning the data, no guarantee is made as to its completeness or accuracy. Always verify against primary sources (annual reports, Dhaka Stock Exchange filings, Bangladesh Bank disclosures) before making financial decisions.

## Contributing

Corrections, additional years, or additional banks are welcome — open an issue or submit a pull request.
