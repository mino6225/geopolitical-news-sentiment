# Geopolitical News Sentiment Tracker
A Python tool that pulls live international news headlines via the NewsAPI and runs 
NLP sentiment analysis to track geopolitical risk signals across high-risk countries 
and jurisdictions — with a focus on Eurasian and sanctioned states.

Built independently as a continuation of applied work in cross-border risk intelligence 
and Eurasian political economy.

## What It Does
- Pulls up to 50 live news headlines per country using the NewsAPI
- Runs VADER sentiment analysis on combined title and article description
- Classifies each headline as POSITIVE, NEGATIVE, or NEUTRAL
- Calculates composite sentiment scores by country
- Tracks sentiment trends over time
- Visualizes results in a four-panel dashboard
- Exports full results to CSV

## Target Countries (Configurable)
- Russia — war, sanctions, Ukraine coverage
- Iran — nuclear program, US-Israel tensions
- China — trade, Taiwan, geopolitical competition
- North Korea — missile and nuclear activity
- Belarus — Lukashenko, opposition, EU relations

## Sample Output (June 2026)

| Country | Articles | Avg Sentiment | % Negative |
|---|---|---|---|
| Iran | 48 | -0.276 | 62.5% |
| Belarus | 16 | -0.211 | 75.0% |
| Russia | 47 | -0.203 | 57.4% |
| North Korea | 45 | -0.130 | 55.6% |
| China | 49 | +0.062 | 38.8% |

## Key Findings
- Belarus had the highest percentage of negative coverage (75%) despite the lowest 
  article volume — indicating concentrated negative events rather than sustained conflict coverage
- Iran scored the most negative average sentiment driven by nuclear deal collapse 
  and Israeli threat escalation headlines
- China was the only country with a positive average sentiment, though recent 
  US-Philippines military exercises are driving scores negative

## Sentiment Scale
VADER compound scores range from -1.0 (most negative) to +1.0 (most positive):
- POSITIVE: score ≥ +0.05
- NEUTRAL: score between -0.05 and +0.05
- NEGATIVE: score ≤ -0.05

## Tech Stack
Python 3.14 · NewsAPI · VADER Sentiment · pandas · matplotlib · seaborn · python-dotenv

## Setup
1. Sign up for a free API key at newsapi.org
2. Create a file called `NewsAPI_Key` in the project folder containing:
   `NEWSAPI_KEY=your_key_here`
3. Run all cells in order

## Security
API key is loaded via dotenv and never hardcoded. A `.gitignore` excludes the key file from version control.

## Author
Mia Noll-Jones — International Affairs & Eurasian Risk Intelligence
github.com/mino6225 | Relocating to Washington D.C., July 2026
