# DarvasTrader

[![Python 3](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A Python and TradingView implementation of the Nicholas Darvas box-breakout method for screening and managing watchlist candidates.

## What is included

- A TradingView Pine Script indicator for visualizing Darvas boxes, breakout signals, and trailing stops in [pinescript/darvas_box_scanner.pine](pinescript/darvas_box_scanner.pine)
- A Python scanner in [scanner/darvas_scanner.py](scanner/darvas_scanner.py) that downloads daily OHLCV data, builds weekly boxes, and ranks symbols by breakout readiness
- Supporting documentation in [docs/darvas_method.md](docs/darvas_method.md)
- A lightweight order and reporting workflow under [scanner](scanner)

## Quick start

1. Create and activate a Python environment.
2. Install dependencies:
   ```bash
   pip install -r scanner/requirements.txt
   ```
3. Run the scanner with the built-in symbol list:
   ```bash
   python scanner/darvas_scanner.py
   ```
4. Or point it at a custom symbol list:
   ```bash
   python scanner/darvas_scanner.py --file scanner/symbols.txt
   ```

## Repository layout

```text
DarvasTrader/
├── agents/            # decision and portfolio helpers
├── config/            # configuration and universe files
├── docs/              # strategy notes and methodology
├── pinescript/        # TradingView Pine Script indicator
├── portfolio/         # portfolio management helpers
├── scanner/           # Python scanner, watchlist, reports, and orders
└── README.md          # project overview
```

## Strategy notes

The scanner follows the Darvas methodology using weekly box construction, breakout confirmation, and a tight stop based on the box ceiling. The full write-up is available in [docs/darvas_method.md](docs/darvas_method.md).

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
