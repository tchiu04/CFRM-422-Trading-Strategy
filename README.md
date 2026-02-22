# CFRM-422-Trading-Strategy
Final Project: Create your own strategy

- Core idea: Build a multi-factor crypto portfolio that combines cross-sectional signals—momentum, funding/basis carry, liquidity, volatility, and attention metrics from search-trend forecasting—with regime-aware allocation.
- Hypotheses
    - (1) Momentum and attention shocks predict short-term returns due to slow information diffusion.
    - (2) Funding rates and futures basis predict reversals when positioning is crowded.
    - (3) Liquidity and volatility factors explain cross-sectional risk premia.
    - (4) Regime switching using volatility, BTC dominance, and liquidity states improves drawdown control and Sharpe ratio. Signals are standardized and combined via regularized regression or PCA into a composite score. Portfolios are beta-neutral to BTC/ETH, with allocations tilting toward momentum in trending regimes and defensive factors in high-volatility regimes.
- Testing, constraints, and objectives
    - Testing: Walk-forward backtests on spot/futures/order-book and attention data. Evaluate IC, Sharpe, turnover, and robustness across coins, rebalance frequencies, and stress periods. Include transaction-cost modeling.
    - Constraints: Leverage caps, liquidity filters, position limits, funding exposure limits, and volatility targeting. Benchmarks include BTC buy-and-hold, ETH buy-and-hold, and a market-cap crypto index.
    - Risk management: Beta neutrality, CVaR and drawdown limits, regime-based de-risking, and execution controls (ADV limits, TWAP/VWAP slicing). Objective: achieve stable Sharpe > 1–1.5, controlled drawdowns, and low correlation to major crypto assets.

Literature review: Crypto factor models

- Liu et al. (2022) document momentum, size, and volatility factors in cryptocurrency markets, finding that momentum is the strongest predictor of returns.
- Borri & Shakhnov (2020) show that liquidity is priced in crypto cross-sections, with illiquid tokens earning higher returns.
- Kozhan & Viswanath-Natraj (2021) find that funding rates contain information about future returns and can predict basis reversals.
- Shen et al. (2020) demonstrate that attention metrics from social media and search trends correlate with short-term price movements.

Literature review: Risk management in cryptots.

- Hu et al. (2019) propose volatility-based regime switching for crypto portfolios, showing improved risk-adjusted returns during high-volatility periods.
- Alexander & Dakos (2020) recommend beta-neutral construction to isolate alpha from market exposure in crypto strategies.
- Grobys & Sapkota (2019) emphasize the importance of transaction cost modeling in crypto backtests due to high spreads and slippage.
- Trimborn & Härdle (2018) advocate for CVaR-based position sizing to manage tail risk in cryptocurrency portfolios.
