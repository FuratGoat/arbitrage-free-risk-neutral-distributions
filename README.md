# Arbitrage-free risk-neutral distributions

A single Jupyter notebook that recovers the risk-neutral distribution of an index ETF's return from noisy end-of-day option quotes.

It fits the closest arbitrage-free call price curve inside the bid-ask spreads (a small non-negative least squares problem), moves it to a constant five-session horizon, and reads off quantiles and Bakshi-Kapadia-Madan moments. Everything is tested on a synthetic Merton jump-diffusion market where the true distribution is known. The notebook then shows a measurement trap: option-implied skewness and kurtosis from a truncated strike range mostly measure how far the strikes reach, which is also visible on fifteen years of SPY, QQQ and IWM chains.

Open `arbitrage_free_rnd.ipynb` on GitHub to read it with all outputs, or run it top to bottom with Python 3, NumPy, SciPy and Matplotlib. It runs in under a minute.
