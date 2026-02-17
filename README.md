<h1 align="center">Trader Behavior vs Market Sentiment Analysis</h1>

<p align="center">
Comprehensive analysis of Hyperliquid trader performance under Bitcoin Fear/Greed sentiment regimes
</p>

<hr>

<h2>1. Objective</h2>

<p>
This project analyzes how Bitcoin market sentiment (Fear vs Greed) relates to trader behavior and performance on Hyperliquid. The primary objective is to identify regime-dependent behavioral patterns that can inform systematic trading strategies and capital allocation decisions.
</p>

<p>
Specifically, the analysis evaluates whether market sentiment influences:
</p>

<ul>
<li>Aggregate profitability (PnL)</li>
<li>Trade frequency</li>
<li>Win rate</li>
<li>Position sizing behavior</li>
<li>Performance differences across trader segments</li>
</ul>

<hr>

<h2>2. Data Sources</h2>

<ul>
<li>
<b>Bitcoin Fear/Greed Index</b><br>
Daily market sentiment classification.
</li>
<li>
<b>Hyperliquid Historical Trade Data</b><br>
Trade-level dataset containing account identifiers, execution price, trade size, timestamps, and realized PnL.
</li>
</ul>

<hr>

<h2>3. Data Preparation</h2>

<h3>3.1 Initial Inspection</h3>

<ul>
<li>Verified row and column counts for both datasets</li>
<li>Checked for missing values and data integrity issues</li>
<li>Ensured correct timestamp formats</li>
</ul>

<h3>3.2 Timestamp Alignment</h3>

<ul>
<li>Converted trade timestamps from epoch milliseconds to datetime</li>
<li>Extracted daily-level keys</li>
<li>Aligned trade data with sentiment classification by date</li>
<li>Performed inner join to ensure regime consistency</li>
</ul>

<h3>3.3 Feature Engineering</h3>

The following core metrics were engineered:

<ul>
<li><b>Daily Total PnL</b> – Sum of closed PnL per day</li>
<li><b>Trade Frequency</b> – Number of trades executed per day</li>
<li><b>Win Rate</b> – Percentage of profitable trades</li>
<li><b>Average Trade Size</b> – Mean USD size per trade</li>
</ul>

Trader-level aggregation was also computed to enable behavioral segmentation.

<hr>

<h2>4. Sentiment Regime Analysis</h2>

The dataset was segmented into Fear and Greed regimes for direct comparison.

<h3>4.1 Performance Comparison</h3>

Key metrics compared:

<ul>
<li>Mean Daily PnL</li>
<li>Mean Trades per Day</li>
<li>Mean Win Rate</li>
<li>Mean Average Trade Size</li>
</ul>

<h3>4.2 Observations</h3>

<ul>
<li>Trade frequency increases significantly during Fear periods.</li>
<li>Aggregate daily PnL is materially higher under Fear compared to Greed.</li>
<li>Win rates show regime-dependent variation.</li>
<li>Position sizes adjust moderately across sentiment conditions.</li>
</ul>

These results suggest that volatility-driven environments (Fear regimes) create more trading opportunity.

<hr>

<h2>5. Behavioral Segmentation</h2>

To analyze heterogeneity in performance, traders were segmented based on trading frequency.

<h3>5.1 Segmentation Logic</h3>

<ul>
<li>Computed total trades per account</li>
<li>Used median trade count as threshold</li>
<li>Defined two groups:
    <ul>
        <li><b>Frequent Traders</b></li>
        <li><b>Infrequent Traders</b></li>
    </ul>
</li>
</ul>

<h3>5.2 Segment-Level Performance</h3>

For each segment:

<ul>
<li>Mean Total PnL</li>
<li>Mean Trade Count</li>
<li>Mean Trade Size</li>
</ul>

<h3>5.3 Key Insight</h3>

Frequent traders demonstrate materially higher aggregate profitability compared to infrequent participants, particularly during high-volatility sentiment regimes.

This suggests that trading style and participation intensity play a critical role in profitability.

<hr>

<h2>6. Visual Analysis</h2>

The notebook includes structured visualizations to support findings:

<ul>
<li>Mean Daily PnL by Sentiment</li>
<li>Win Rate by Sentiment</li>
<li>Trade Frequency Comparison</li>
<li>PnL Distribution Boxplots</li>
<li>Segment-Level PnL Comparison</li>
<li>Daily PnL Time Series</li>
</ul>

Each visualization is designed to directly support a behavioral or regime-dependent inference.

<hr>

<h2>7. Strategic Implications</h2>

Based on the empirical findings:

<ul>
<li>
<b>Regime-Based Allocation:</b><br>
Increase capital allocation during Fear regimes, where volatility-driven opportunities are higher.
</li>

<li>
<b>Selective Participation:</b><br>
Prioritize allocation toward high-frequency trader segments, which demonstrate stronger aggregate performance.
</li>

<li>
<b>Risk Adjustment During Greed:</b><br>
Reduce exposure and tighten risk parameters during Greed regimes where aggregate profitability compresses.
</li>
</ul>

These recommendations translate sentiment classification into actionable trading logic.

<hr>

<h2>8. Repository Structure</h2>

<ul>
<li><b>Trader_Main_Assignment_Enhanced_With_Visuals.ipynb</b> – Core required analysis</li>
<li><b>Trader_Bonus_Extra_Plots.ipynb</b> – Extended modeling and exploratory analysis</li>
<li><b>Trader_Results_All_In_One.md</b> – Results-only summary</li>
</ul>

<hr>

<h2>9. Reproducibility</h2>

To reproduce results:

<ol>
<li>Place <code>fear_greed_index.csv</code> and <code>historical_data.csv</code> in the project directory.</li>
<li>Open the notebook in Jupyter.</li>
<li>Run cells sequentially from top to bottom.</li>
</ol>

All preprocessing, feature engineering, aggregation, and visualization steps are fully documented within the notebook.

<hr>

<p align="center">
Prepared as part of a Data Science / Analytics internship evaluation assignment.
</p>
