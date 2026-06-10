# Hey, I'm Tharun!

I build internal tools and data pipelines for finance teams and spend my free time on personal projects in DeFi, trading infrastructure, and research. Outside of work I'm into traveling, collecting coins, drinking chocolate milk, and playing Risk and Bughouse Chess.

---

### Skills

| | |
|---|---|
| **Languages** | Python, Rust, Solidity, TypeScript, JavaScript, SQL, Go, HTML, CSS, Bash, Google Apps Script |
| **Blockchain & Web3** | Solana (on-chain architecture: PDAs, CPIs, BPF / Sealevel), Anchor, SPL Token, Solana Web3.js, Meteora, Helius, Foundry, Hardhat, EIP-712, EIP-3009, ERC-4626, ERC-721, ERC-8004, x402, Avalanche (C-Chain / Fuji), Wagmi, Viem, web3.py, Robinhood Chain |
| **Backend & APIs** | FastAPI, Flask, Express, SQLAlchemy, Supabase, Celery, Redis, REST APIs, WebSockets, OAuth 2.0, Webhooks, MCP, Polymarket (Gamma & CLOB), Google Workspace APIs, Slack Web API, Telegram Bot API, Reddit (PRAW), Jira API, Horizon API, LLM APIs (OpenAI, Anthropic, Google Gemini) |
| **Data & Analytics** | Pandas, NumPy, Copula Pricing, Monte Carlo Simulations, ARIMA, VADER Sentiment Analysis, Time Series Modeling, Statistical Testing, Streamlit, LightGBM, XGBoost |
| **Frontend** | React, Next.js, Vite, Three.js, CSS Modules |
| **Cloud & Infrastructure** | GCP, Terraform, Airflow, Docker, Prometheus, GitHub Actions, Cloud Functions, Cloud Composer, Akash Network, Service Accounts, IAM |
| **Integrations & Tools** | FloQast, NetSuite, n8n, Workday, Tableau, Git |

---

### Stats

| Projects | Hackathon Wins | Research Competition Wins | Competition Winnings | APIs Integrated | Automations Built |
|---|---|---|---|---|---|
| 13 | 5 | 3 | $60,800 | 19 | 28 |

---

### Independent Projects

**The KelpDAO rsETH Exploit & DeFi's Composability Trap (Artemis × DormDAO)** · `Long-form` · `May 2026`
> Long-form research with Michael Green on the April 2026 KelpDAO rsETH stress event across LayerZero and major lending venues, tracing how a single cross-chain approval moved a nine-figure rsETH balance out of Ethereum escrow without a matched burn, how that showed up as tighter backing for bridged holders than headline mainnet prices suggested, how supplier behavior flowed through to Aave WETH balances, and why the episode lines up with prior bridge governance failures (Ronin, Nomad, Wormhole, Resolv USR) more than a flaw in restaking math alone. The piece draws on primary on-chain timelines and public post-mortems to argue that bridge verifier setup and disclosure belong in collateral onboarding and ecosystem incentives, and it ends on the coalition-style DeFi United relief compared with a single backstop. **One of three winners of the Artemis × DormDAO Research Competition out of 60+ submissions.**

**Senthos (SCBC Hackathon)** · `42,825 lines` · `TypeScript, Rust` · `Apr 2026`
> Structured prediction-market protocol on Solana that wraps live Polymarket markets into Native Basket indices, senior/mezzanine/junior tranches, principal-protected notes that fund basket legs while preserving principal, and a USDC lending and repo market collateralized by basket and tranche inventory. Solana devnet runs Anchor programs senthos_vault and senthos_ppn for bundle vault deposits, leg resolution, finalization, and PPN minting. The Express and TypeScript backend exposes the Polymarket bridge, Supabase-backed bundle catalogs, a five-stage NLP filter before markets feed correlation sizing, and a trained correlation model integrated with basket and tranche pricing. Next.js 16 frontend ships the landing page and wallet-connected basket, tranche, PPN, lending, and portfolio flows against published devnet program IDs. **Won 1st place at the SCBC hackathon and Best Use of Solana.**

**AgentHire (SCBC Hackathon)** · `28,970 lines` · `Python, JavaScript` · `Apr 2026`
> Agent marketplace on Avalanche Fuji that matches buyers and sellers of autonomous agents, with USDC routed through x402-style machine payments and gasless permits into escrow alongside ERC-8004 identity, on-chain reputation, slashable developer stake, and auction-based clearing when bids compete. Implemented in Flask and SQLAlchemy with Jinja2 templates and ethers.js wallet flows, using Python web3 to execute permit, deposit, and settle on Fuji without a standalone Node.js payment service. Integrated Akash-hosted inference (Qwen 2.5 Coder 7B), MCP tool discovery, Telegram streaming, Teleporter/ICM cross-subnet messaging, and a ChainTransaction-backed refresh path that keeps marketplace aggregates aligned to indexed Fuji activity between sparse blocks. Automated security gates are paired with structured human review before escrow completes payout. **Won 1st place at the SCBC hackathon for agentic payments on Avalanche.**

**Cronos On-Chain Research (Penn Blockchain Conference)** · `11,367 lines` · `Python` · `Mar 2026`
> Institutional-grade research pipeline for the Cronos (CRO) blockchain ecosystem built as a standalone investment thesis. Engineered an async distributed downloader with multi-endpoint RPC failover and checkpoint/retry across 29GB of raw block data. Ran 12 analytical modules covering the full ecosystem: behavioral bot classification using activity fingerprinting, wash-trading isolation via graph cycle enumeration and DEX direction-reversal detection, wallet clustering with Union-Find on funding-source and gas-price fingerprints, Gini coefficient holder concentration, Nakamoto coefficient validator tracking, DEX microstructure analysis, and staking emission sustainability modeling. Cross-chain peer benchmarking against BNB and OKB provided valuation context, feeding into a revenue-multiple model with bull/base/bear scenarios built on protocol fee projections and TVL trajectory assumptions. Layered in Reddit sentiment analysis across thousands of posts to capture community sentiment as a forward-looking signal alongside the on-chain fundamentals. Delivered as a 12-page interactive Streamlit dashboard covering every analytical layer from network health through valuation. **Won 1st place in the Penn Blockchain Conference research competition.**

**Laytus Protocol** · `53,431 lines` · `Python, Solidity, TypeScript` · `Jan 2026`
> Structured position protocol on Robinhood Chain that lets users take positions on correlated outcomes across multiple prediction markets in a single atomic transaction. The pricing engine uses a Gaussian copula to model joint outcome distributions across correlated markets, with dynamic vig that adjusts spread based on real-time liquidity and correlation confidence. Correlation estimates are produced by an ensemble ML model (LightGBM + XGBoost) trained on historical market outcome data, with features covering market category overlap, shared resolution authorities, and time-to-resolution alignment. The backend is split into 7 FastAPI microservices handling quoting, order management, correlation inference, position tracking, settlement orchestration, and user state, each deployable independently. Quote integrity is enforced through EIP-712 typed structured data signing verified end-to-end between the Python quoting service and the Solidity settlement contract, preventing quote manipulation between issuance and on-chain submission. The settlement state machine manages the full position lifecycle: open, partially resolved, fully resolved, and clawed back, with on-chain transaction submission handled by a keeper that monitors resolution oracle feeds. Frontend built in React with real-time market data streaming and position P&L tracking. **Won 2nd place ($40K) at the Arbitrum Open House in New York and reached the quarterfinals of the ADI bounty at ETHDenver.**

**Crypto Research (Midwest Blockchain Conference)** · `41,881 lines` · `Python` · `Nov 2025 - Jan 2026`
> Blockchain forensics research targeting Pi Network combining NLP, on-chain analytics, and statistical modeling into a unified fraud assessment framework. Applied Levenshtein similarity clustering to Play Store review data to surface coordinated fake review campaigns, and cross-referenced technical claims against independent third-party sources across multiple verification dimensions to produce a composite credibility index. On the on-chain side, used chi-squared validated random sampling via the Horizon API to test whether reported activity distributions were consistent with organic usage, fit ARIMA models to exchange inflow time series to identify structural breaks, and ran Granger causality tests to determine whether social sentiment shifts directionally predicted on-chain activity or were simply coincident. Generated log-normal synthetic baselines validated via Kolmogorov-Smirnov tests to benchmark observed metrics against organic growth expectations. Delivered a Streamlit dashboard with network topology visualization, whale wallet activity timelines, and a fraud scoring breakdown. **Won 1st place out of 57 teams in the Franklin Templeton Digital Assets research pitch competition.**

**GTO Poker Trainer** · `10,389 lines` · `JavaScript` · `Nov 2025`
> Fully client-side poker training engine with no server dependency. Implements a 3-pass Fisher-Yates shuffle, a 9-rank hand evaluation hierarchy, and Omaha's mandatory 2+3 rule via exhaustive combination enumeration. The GTO layer computes optimal bet frequencies using pot odds, equity, and position, with a bluffing engine based on the Minimum Defense Frequency formula and an ICM calculator for tournament stack pressure. Supports 5 game variants (Texas Hold'em, Omaha, PLO, Pineapple, Crazy Pineapple) with 2-10 players, double board variants, and a Player Profiler tracking VPIP and PFR stats across sessions.

**Plasma Donation Research** · `10,102 lines` · `Python` · `Oct - Nov 2025`
> Economic behavior research treating plasma donation as a behavioral signal for household financial distress. Collected 80,000+ Reddit posts from 75+ subreddits using PRAW and Pushshift, applied VADER sentiment scoring, and built a composite Financial Distress Index from 7 FRED indicators. Ran Granger causality tests, Transfer Entropy, and Pearson/Spearman rolling correlations to measure lagged relationships between economic stress and donation activity. Found 10 statistically significant relationships, including a peak correlation of r=0.81 at a 3-month lag between U6 unemployment and plasma donation post volume.

**Gappify Notification Bot** · `1,630 lines` · `Python` · `Oct 2025`
> Airflow DAG on GCP Composer that orchestrates monthly accrual cycle reminders across seven finance teams. Reminder schedules are defined in a YAML template with business day offsets relative to MEC. The DAG integrates with Google Calendar to resolve due dates dynamically, queries an internal database for Slack member ID resolution, and sends channel summaries and personalized DMs with exponential backoff retry on all Slack API calls. It reduced manual follow-up work by approximately 80%.

**FP&A Reminder Bot** · `1,238 lines` · `Python` · `Oct - Nov 2025`
> Slack notification system for FP&A task accountability. Reads a task completion matrix from Google Sheets via service account auth, resolves owner emails to Slack member IDs through the Google People API, and sends personalized DMs with batch rate limiting (batch size 10, 0.5-second delays). Includes dry-run mode for pre-MEC validation and structured logging throughout the delivery chain.

**Data Analysis Pipeline** · `1,107 lines` · `Python` · `Jan 2026`
> General ledger mapping and month-end reconciliation pipeline. A UnifiedGLMapper loads 4,029 account mapping patterns across 22 types and ranks candidates by priority and confidence when multiple patterns match, reaching 99.07% accuracy across historical backtests. The daily pipeline deduplicates source exports, flags accounts with variance beyond configurable thresholds, and generates formatted Excel reports with conditional formatting for finance reviewers.

**Terraform Config** · `473 lines` · `Python` · `Nov 2025`
> GCP infrastructure automation for the internal finance tool stack. Covers service account provisioning, IAM bindings, Cloud Function deployments, and API enablement. Includes a GoogleOAuthManager with an interactive setup wizard, predefined scope configs per bot, and a base64 export utility for storing credentials as Airflow Variables in GCP Composer without plaintext secrets in deployment configs.

**App Scripts** · `2,083 lines` · `Google Apps Script` · `Jun - Oct 2025`
> Seven Google Apps Script automations for internal finance workflows: a Sheets-to-Calendar sync with color mapping and duplicate prevention, a CCIL Fair Value Classifier, a FloQast MEC status updater, a Flux Analysis tool for period-over-period GL variance, a Google Drive Linker, and two Slack bots handling incident routing and internal workflow notifications.

---

![Profile Views](https://komarev.com/ghpvc/?username=tharune&color=0969da&style=flat-square)
