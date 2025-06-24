# Compound-wallet-Credit-Scoring
This project implements a custom machine learning pipeline to assign a credit score (0–100) to each wallet interacting with the Compound V2 protocol, based solely on historical transaction behavior.

## Objective
Assign higher scores to wallets that show responsible, long-term engagement (e.g., consistent supply, repay behavior), and lower scores to risky or exploitative wallets.

## Dataset
Source: Raw Compound V2 JSON files from the provided Google Drive

We selected the top 3 largest JSON files to ensure high transaction volume

## Methodology
1. Data Extraction
Parsed malformed JSON using custom flattening logic

Extracted the following per-wallet fields:

wallet_address

timestamp

amount and amountUSD

Action type (supply only)

2. Feature Engineering
We engineered the following behavioral features per wallet:

Number of transactions (tx_count)

Number of active days

Repay-to-borrow ratio (0 for supply-only data)

Number of supply events

Average time between transactions (wallet consistency)

3. Scoring Logic
Each feature was normalized via MinMaxScaler, then a weighted scoring formula was applied:

Feature	Weight
Transaction Count	0.2
Active Days	0.2
Repay/Borrow Ratio	0.3
Supply Count	0.2
Avg Time Between Tx	0.1

Scores are scaled to a range of 0 to 100.

## Results
We generated:

📄 wallet_scores.csv: Full list of wallet scores

📄 top_1000_wallet_scores.csv: Top 1,000 wallets (sorted)
https://docs.google.com/spreadsheets/d/1bo1tt2XmLADdMKZLiuBTHYZbr2o7z9GE4rsWKUXail8/edit?usp=sharing


📊 A histogram showing the distribution of credit scores

