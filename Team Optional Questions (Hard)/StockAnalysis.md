# Stock Market Analysis

## Description
Create a stock market analysis tool that processes historical data and identifies patterns.

## Problem Statement
Develop a program that analyzes stock market data and implements common technical indicators.

### Requirements
- Moving averages calculation
- Volume analysis
- Trend identification
- Support/resistance levels
- Pattern recognition

### Constraints
1. Use only historical data
2. No external market APIs
3. Process data in CSV format
4. Include error handling

## Input Data Format
```csv
Date,Open,High,Low,Close,Volume
2024-01-01,150.25,152.75,149.50,151.30,1000000
2024-01-02,151.50,153.25,150.75,152.80,1200000
```

## Expected Outputs
```json
{
  "technical_indicators": {
    "sma_20": 151.45,
    "rsi_14": 63.5,
    "macd": {
      "line": 2.15,
      "signal": 1.95,
      "histogram": 0.20
    }
  },
  "support_levels": [148.50, 146.75],
  "resistance_levels": [153.25, 155.00],
  "trend": "BULLISH",
  "volume_analysis": "INCREASING",
  "recommendations": [
    {
      "type": "ENTRY",
      "price": 151.00,
      "confidence": 0.85
    }
  ]
}
```

## Required Indicators
1. Moving Averages (SMA, EMA)
2. RSI (Relative Strength Index)
3. MACD (Moving Average Convergence Divergence)
4. Bollinger Bands
5. Volume Profile

## Test Cases
1. Trend Detection:
   ```
   Input: 30 days of upward movement
   Expected: Strong bullish trend identification
   ```

2. Support/Resistance:
   ```
   Input: Multiple price bounces at 150.00
   Expected: Strong support level identification
   ```

3. Volume Analysis:
   ```
   Input: Sudden volume spike with price increase
   Expected: Breakout detection and alert
   ```
