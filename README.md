# USD/TWD Election-Based Strategy Backtest

A backtestable strategy for USD/TWD exchange rate forecasting, modeled on U.S. presidential election events.  
Originally built as a spreadsheet-based logic map, this project transforms qualitative assumptions into a testable Python strategy with historical FX data.

---

## Motivation

- In the lead-up to the 2024 U.S. election, interest rate expectations surged.
- Historical FX movements around past election cycles revealed potential patterns.
- This project aims to verify entry/exit timing using event-driven assumptions and backtestable rules.

---

## Strategy Logic

- **Entry Condition**: USD/TWD drops below 30.5 (assumed support zone)
- **Exit Condition**: USD/TWD rebounds to 31.5 (target zone)
- **Stop-Loss**: Price dips below 30
- **Data Source**: Daily USD/TWD close price via [`yfinance`](https://pypi.org/project/yfinance/)

---

## Sample Output

![image](https://github.com/user-attachments/assets/59ffafeb-7f5a-4abe-9a93-58fb870632cf)

```python
# Example: Visualizing entry/exit zones
plt.plot(df['Close'], label='USD/TWD')
plt.axhline(30.5, color='green', linestyle='--', label='Entry Threshold')
plt.axhline(31.5, color='red', linestyle='--', label='Exit Threshold')
```

## Repository Structure

| Folder        | Description                                      | Link |
|---------------|--------------------------------------------------|------|
| `/data/`      | Original Excel assumptions and FX scenarios      | [Google Sheet](https://docs.google.com/spreadsheets/d/10DiAvFjMKqC1DRFANqVg_A8_3dPdnlSglUquVSOoeiU) |
| `/code/`      | Backtest implementation in Python / Notebook     | [Colab Notebook](https://colab.research.google.com/drive/1f6qG9ylhAXW93HMatvsUPBis_1k5Umj9?usp=sharing) |
| `/images/`    | Strategy output visualizations                   | –    |
| `README.md`   | Project description (you’re here)                | –    |

## Visualization Gallery

![Strategy Logic](https://github.com/user-attachments/assets/3a8b4931-5432-4d96-9e50-3229ec3e4c0b)
![USD/TWD Close](https://github.com/user-attachments/assets/2170d1dd-6240-4a3a-afa5-b4ac15fc7d45)
![Zone Indicators](https://github.com/user-attachments/assets/ffa79a0f-df39-4c6b-b163-09d395142031)
![Backtest Outcome](https://github.com/user-attachments/assets/21bb9189-1b38-4d4a-aba6-43de7a704081)
![Result Chart](https://github.com/user-attachments/assets/9d72c795-0d73-4f39-bc48-cf9ac6215505)

> Full output visualized: thresholds, backtest signals, and result metrics.



## Tech Stack
- Python (pandas, yfinance, matplotlib)
- Strategy testing via Jupyter Notebook
- Git-based version control

## Legacy Origin
This strategy was first drafted in Excel (2024 Q1) and included:
- Manual simulations of 2015–2017 election cycle FX behaviors
- 6-case scenario forecast with policy outcome assumptions
- Post-tax yield calculations and timing optimization
- The spreadsheet served as a sandbox to structure logic before converting it to Python.

## Future Enhancements
- Add FedWatch rate forecast or macro indicators as trigger filters
- Incorporate NLP-based news monitoring (NER + sentiment) to assess FX impact risk
- Refactor logic for multi-currency pairs (e.g., USD/JPY, EUR/USD)

---

## Tags

`#finance` `#exchange-rate` `#backtest` `#machine-learning` `#election-strategy` `#Python`

## License

MIT© Kailin
「此專案為學術用作品，請勿未經授權商業使用」
