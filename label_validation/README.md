# Manual validation of the outcome label

The outcome treats every agent PR not merged within 14 days as a failure. PRs are also closed for reasons
that have nothing to do with the agent, so a sample of failures is coded by hand.

`label_validation_sample.csv` holds 200 failed PRs drawn by step 7 of the notebook (stratified by agent,
at least 10 per agent, seed 0). Open each `html_url`, read the conversation and the final state, and fill
in `closure_reason` with one of:

| Code | Meaning |
|---|---|
| `AGENT_FAILURE` | Closed because the change was wrong, incomplete, broke tests or CI, or was rejected on review |
| `DUPLICATE_OR_SUPERSEDED` | The same problem was fixed by another PR, by a human or by another agent |
| `ABANDONED_OR_STALE` | Closed or left open without substantive review |
| `NOT_WANTED_OR_OUT_OF_SCOPE` | Maintainers decided the change or feature was not needed |
| `STILL_OPEN_OR_LATE_MERGE` | Merged more than 14 days after the PR was opened, or still open at the snapshot |
| `OTHER` | None of the above, or unclear |

Use `notes` for a short quote or reason. A second coder should independently code a random subset so that
agreement (Cohen's kappa) can be reported.
