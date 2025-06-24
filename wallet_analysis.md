# Wallet Behavior Analysis
This document presents an analysis of 5 high-scoring and 5 low-scoring wallets based on their behavioral features extracted from the Compound V2 protocol.

## High-Scoring Wallets
These wallets exhibit responsible and consistent interaction patterns:

| Wallet Address                               | Score     | Observations                                                                                          |
| -------------------------------------------- | --------- | ----------------------------------------------------------------------------------------------------- |
| `0x29fe7d60ddf151e5b52e5fab4f1325da6b2bd958` | **60.01** | Only one transaction, but likely large or important enough to score well under current normalization. |
| `0x0034ea9808e620a0ef79261c51af20614b742b24` | **31.42** | Moderate number of supplies, active for 1 day, no borrow/repay patterns.                              |
| `0x00000000001876eb1444c986fd502e618c587430` | **31.03** | Higher activity spread across multiple days. All actions are supplies.                                |
| `0x8f2d580c3cccd96c3541386daac0af71c5d1c0f9` | **29.77** | Slightly more active behavior, but no repayment or borrow behavior detected.                          |
| `0xa2b47e3d5c44877cca798226b7b8118f9bfb7a56` | **23.02** | Lower supply volume, but still among the top 5 in this dataset subset.                                |

Common Traits:

Regular supply behavior

Wide temporal activity spread

Minimal idle time between transactions

## Low-Scoring Wallets
These wallets likely show minimal or erratic participation:

| Wallet Address                               | Score   | Observations                                                         |
| -------------------------------------------- | ------- | -------------------------------------------------------------------- |
| `0x8d2150a54a2a25e0b966e15f9c6efc6397499044` | **0.0** | No activity detected, possible empty shell or failed transaction.    |
| `0x8dd90c29300f4e967c441a0753f19bf43fc39f34` | **0.0** | Identical inactivity; no supplies, borrows, or even timestamps.      |
| `0x8dd499ec0c328dfe2e035129197e964612310466` | **0.0** | No on-chain interaction or history detected.                         |
| `0x8dd466326a8761e28077cda4ebc85e9f89e60d8f` | **0.0** | Zero recorded behavioral indicators.                                 |
| `0x8dd391437c6ca1f9300f57431b75e975e6b56de5` | **0.0** | One of several likely bot-generated, inactive, or abandoned wallets. |

Observation: These wallets had no valid transactions parsed, which may indicate:

Junk data or unused accounts

Wallets initialized but never used

Errors or noise in the raw JSON

## Interpretation
High-scoring wallets generally represent loyal and stable participants in the protocol, with:

Time-consistent supply behavior

A history of returning engagement

Lower risk for liquidation or abandonment

Low-scoring wallets might be:

Short-term opportunists

Bots or abandoned addresses

Irregular in their usage of the protocol

