# trader-sentiment-analysis
Analysis of Hyperliquid trader behavior under Bitcoin Fear/Greed sentiment regimes.
<h1 align="center">Trader Behavior vs Market Sentiment Analysis</h1>

<p align="center">
Analysis of Hyperliquid trader performance under Bitcoin Fear/Greed market regimes
</p>

<hr>

<h2>Objective</h2>
<p>
This project analyzes how Bitcoin market sentiment (<b>Fear vs Greed</b>) influences 
trader behavior and profitability on Hyperliquid.
</p>

<hr>

<h2>Datasets</h2>
<ul>
<li><b>Bitcoin Fear/Greed Index</b> (Daily classification)</li>
<li><b>Hyperliquid Historical Trade Data</b></li>
</ul>

<hr>

<h2>Methodology</h2>
<ul>
<li>Converted timestamps to daily level</li>
<li>Merged trade data with sentiment classification</li>
<li>Engineered key performance metrics:
    <ul>
        <li>Daily total PnL</li>
        <li>Trade frequency</li>
        <li>Win rate</li>
        <li>Average trade size</li>
    </ul>
</li>
<li>Compared performance across sentiment regimes</li>
<li>Segmented traders by trading frequency</li>
</ul>

<hr>

<h2>Key Findings</h2>

<h3>1️Fear Regimes Drive Higher Activity</h3>
<p>
Trade frequency increases significantly during Fear periods, 
indicating volatility-driven participation.
</p>

<h3>Profitability is Regime-Dependent</h3>
<p>
Aggregate daily PnL is substantially higher during Fear compared to Greed phases.
</p>

<h3>Frequent Traders Outperform</h3>
<p>
High-frequency traders generate higher aggregate profitability, 
especially during volatile market conditions.
</p>

<hr>

<h2>Strategy Implications</h2>
<ul>
<li><b>Regime-Based Allocation:</b> Increase allocation to high-frequency traders during Fear regimes.</li>
<li><b>Risk Compression:</b> Reduce exposure and tighten risk controls during Greed regimes.</li>
<li><b>Volatility-Aware Capital Deployment:</b> Use dynamic exposure instead of static allocation.</li>
</ul>

<hr>

<h2>How to Run</h2>
<ol>
<li>Place the following files in the same directory:
    <ul>
        <li><code>fear_greed_index.csv</code></li>
        <li><code>historical_data.csv</code></li>
    </ul>
</li>
<li>Run the notebook from top to bottom.</li>
</ol>

<hr>

<p align="center">
Built as part of a data science analysis assignment.
</p>
