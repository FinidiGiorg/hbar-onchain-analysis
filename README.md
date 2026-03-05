# HBAR On-Chain Analysis — 2020 vs 2026

Comparative analysis of the **Hedera (HBAR) network** between its first February 1st (2020) and February 1st 2026 — tracking 6 years of adoption, transaction patterns and wallet behaviour.

---

## What it covers

- **Transaction volume** — total, average and max per period
- **Active wallet count** — via Hedera Mirror Node (more accurate than BitQuery for HBAR)
- **Top 30 wallet classification** — Institutional, Market Maker/Bot, Mixed/Gateway
- **Transaction size distribution** — micro (< 0.01 HBAR) through whale (> 10,000 HBAR)
- **6-year adoption trajectory** — how the network evolved from early 2020 to early 2026

---

## Key findings

| Metric | Feb 2020 | Feb 2026 |
|---|---|---|
| Total Volume | — | 1,906,266,052 units |
| Active Wallets | — | tracked via Mirror Node |
| Tx Distribution | early adopters | institutional + bot dominated |
| Top-10 Wallet Supply | — | 99.81% |

---

## Stack

| Layer | Technology |
|---|---|
| On-chain data | BitQuery GraphQL API |
| Wallet activity | Hedera Mirror Node REST API |
| Data processing | Python · pandas · numpy |
| Visualisation | matplotlib · gridspec |
| Environment | Jupyter Notebook |

---

## Data sources

- **BitQuery GraphQL API** — volume, wallet classification, transaction size distribution
- **Hedera Mirror Node** (`https://mainnet-public.mirrornode.hedera.com`) — active wallet counts (used instead of BitQuery due to accuracy issues with Hedera uniq counts)

---

## Quickstart

### 1. Install dependencies

```bash
pip install requests pandas numpy matplotlib jupyter
```

### 2. Configure API key

Create a `.env` file:

```
BITQUERY_API_KEY=your_key_here
```

Get a free key at [bitquery.io](https://bitquery.io).

### 3. Run

```bash
jupyter notebook hbar_analysis_2020_2026.ipynb
```

Run cells sequentially. Each cell is independent and labelled.

---

## Notebook structure

| Cell | What it does |
|---|---|
| 1 | Setup — imports, API config |
| 2 | Helper functions — GraphQL query runner |
| 3 | Volume, median, max, concentration (BitQuery) |
| 4 | Active wallets (Mirror Node) |
| 5 | Top 30 wallets + classification |
| 6 | Transaction size distribution (micro → whale) |
| 7 | Final summary table |
| 8 | Wallet profile chart (bubble + activity + volume) |
| 9 | Micropayments & whales + key metrics summary |

---

## Why Hedera

Hedera is one of the few enterprise-grade distributed ledgers with real institutional adoption — used by Google, Boeing, IBM and others. Its low, predictable fees make it a strong candidate for **AI agent micropayments** and **RWA tokenisation** at scale.

This analysis was built as part of a broader research into blockchain infrastructure suitable for autonomous AI agent payment systems.

---

## Related projects

- [XRPL RWA Intelligence Pipeline](https://github.com/FinidiGiorg/rwa-token-analyzer) — autonomous on-chain analytics pipeline for XRPL RWA activity, using local LLM inference and Streamlit dashboard

---

## Author

**Daniel Ávila** · Data Analyst | AI Agents | Blockchain & RWA  
[LinkedIn](https://linkedin.com/in/danielavilahrdataanalyst-scientist) · [GitHub](https://github.com/FinidiGiorg)
