# ADBench Leaderboard

A comprehensive benchmark for evaluating LLM-based agents on real-world advertising analytics tasks, with tiered difficulty and trajectory-based evaluation.

> 📊 100 Tasks · 🔧 11 Domain Tools · 🏷️ 3 Difficulty Levels · 🤖 10 Models Evaluated

## Leaderboard (Overall, Pass@3)

| Rank | Model | Type | Pass@1 | Pass@3 |
|:----:|-------|:----:|:------:|:------:|
| 1 | Gemini-3-Pro | Proprietary | 68.0% | 83.0% |
| 2 | o3 | Proprietary | 69.0% | 82.0% |
| 3 | GPT-5.1 | Proprietary | 64.7% | 82.0% |
| 4 | HY-2.0 | Proprietary | 65.7% | 82.0% |
| 5 | GLM-4.7 | Proprietary | 64.7% | 81.0% |
| 6 | DeepSeek-V3 | Proprietary | 68.3% | 80.0% |
| 7 | Kimi-K2 | Proprietary | 64.0% | 79.0% |
| 8 | Qwen3-235B | Open | 54.3% | 68.0% |
| 9 | Qwen3-32B | Open | 38.0% | 59.0% |
| 10 | Qwen3-8B | Open | 38.0% | 58.0% |

### By Difficulty Level

<details>
<summary><b>L1 (Easy) — 24 cases</b></summary>

| Rank | Model | Pass@1 | Pass@3 |
|:----:|-------|:------:|:------:|
| 1 | GPT-5.1 | 88.9% | 95.8% |
| 2 | Gemini-3-Pro | 77.8% | 91.7% |
| 3 | o3 | 86.1% | 91.7% |
| 4 | Kimi-K2 | 83.3% | 91.7% |
| 5 | HY-2.0 | 84.7% | 87.5% |
| 6 | GLM-4.7 | 72.2% | 87.5% |
| 7 | DeepSeek-V3 | 81.9% | 87.5% |
| 8 | Qwen3-235B | 79.2% | 87.5% |
| 9 | Qwen3-8B | 51.4% | 79.2% |
| 10 | Qwen3-32B | 50.0% | 70.8% |

</details>

<details>
<summary><b>L2 (Medium) — 47 cases</b></summary>

| Rank | Model | Pass@1 | Pass@3 |
|:----:|-------|:------:|:------:|
| 1 | o3 | 75.9% | 91.5% |
| 2 | Gemini-3-Pro | 74.5% | 91.5% |
| 3 | HY-2.0 | 70.2% | 91.5% |
| 4 | GLM-4.7 | 72.3% | 91.5% |
| 5 | DeepSeek-V3 | 74.5% | 87.2% |
| 6 | Kimi-K2 | 66.7% | 85.1% |
| 7 | GPT-5.1 | 66.7% | 83.0% |
| 8 | Qwen3-235B | 53.2% | 72.3% |
| 9 | Qwen3-32B | 41.8% | 63.8% |
| 10 | Qwen3-8B | 41.8% | 61.7% |

</details>

<details>
<summary><b>L3 (Hard) — 29 cases</b></summary>

| Rank | Model | Pass@1 | Pass@3 |
|:----:|-------|:------:|:------:|
| 1 | GPT-5.1 | 41.4% | 69.0% |
| 2 | Gemini-3-Pro | 49.4% | 62.1% |
| 3 | DeepSeek-V3 | 47.1% | 62.1% |
| 4 | HY-2.0 | 42.5% | 62.1% |
| 5 | o3 | 43.7% | 58.6% |
| 6 | GLM-4.7 | 46.0% | 58.6% |
| 7 | Kimi-K2 | 43.7% | 58.6% |
| 8 | Qwen3-235B | 35.6% | 44.8% |
| 9 | Qwen3-32B | 21.8% | 41.4% |
| 10 | Qwen3-8B | 20.7% | 34.5% |

</details>

## Example Cases

| Level | Query | Category |
|:-----:|-------|----------|
| L1 | What is the total spending across all accounts yesterday? | Single-step retrieval |
| L1 | How many total impressions did all accounts receive yesterday? | Single-step retrieval |
| L2 | What is the total spending on female audiences across all accounts in the past 30 days? | Filter + aggregation |
| L2 | What is the overall average cost-per-click across all accounts yesterday? | Multi-field computation |
| L3 | Based on the per-user billing cap rules, how many users have reached the spending cap given yesterday's impression data? | Knowledge + data fusion |
| L3 | Does the peak conversion-rate hour for ad #189****5704 during Double-11 match the industry-wide golden hours? | Parallel orchestration + reasoning |

## Submission Portal

Due to privacy-sensitive information in the benchmark queries, the dataset is **not publicly released**. We maintain and update the leaderboard through a centralized evaluation service.

**Target Audience**: Model providers, research institutions, and enterprise developers.

**Required Materials**:
1. Public model endpoint (API or HuggingFace repo)
2. Model card / technical spec (I/O format, context window, etc.)

**How to Submit**:
- Email: [lingxianghu@tencent.com](mailto:lingxianghu@tencent.com)
- Subject: `[ADBench Eval Request] <Institution / Model Name>`

**Turnaround**: We will schedule the evaluation and send a full report within **14 business days**.
