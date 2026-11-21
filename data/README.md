# Data

No raw data is stored in this repository. The notebook downloads everything it needs from the
**AIDev** dataset on Hugging Face ([`hao-li/AIDev`](https://huggingface.co/datasets/hao-li/AIDev)).

| Item | Value |
|---|---|
| Dataset | AIDev (Li, Zhang and Hassan, arXiv:2507.15003) |
| Version used | commit `b8dc67df93e7c11f6f20c84129db7232eb1ec253` |
| Snapshot date (latest timestamp) | 7 April 2026 |
| Tables used | `pull_request`, `issue`, `related_issue`, `pr_reviews`, `pr_comments`, `pr_timeline`, `repository` |

AIDev is published under its own licence; see the dataset card on Hugging Face before reusing or
redistributing it. Each source repository on GitHub keeps its own licence.

## Derived files

Step 1 of the notebook writes two files, which are not committed because they are re-created on every run:

| File | Content |
|---|---|
| `routing_main_v2.parquet` | Main dataset: 30,634 non-self-delegated issues with features and 14-day labels |
| `routing_all_v2.parquet` | All 45,032 issues with full follow-up, including self-delegated and leak-flagged ones |

If you want to share them, attach them to a GitHub Release rather than committing them.
