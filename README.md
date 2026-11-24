# A/B testing with non-compliance

How to measure the impact of a campaign when not everyone assigned to it actually receives it.

This notebook simulates a call campaign across 12 sites, where customers are randomly assigned to a call or a control group, but the call centre only reaches part of the call group. Reachable customers are also more engaged, so the people you manage to call would have returned more often anyway.

## What the notebook covers

- **Why the naive comparison is biased.** Comparing called customers against control overstates the effect.
- **ITT vs CACE.** The intention-to-treat effect measures the policy; the complier average causal effect uses random assignment as an instrument to estimate the effect of actually receiving a call.
- **Power and minimum detectable effect per site.** Low contact rates dilute the effect and can multiply the sample size needed.
- **From uplift to a decision.** Turning the estimated effect into value per call to decide where calling pays off.

## Why this matters

I have worked on a real experiment with this exact problem: a call campaign where limited call-centre capacity meant many assigned customers were never reached. This repository reproduces the method on simulated data, with no company data or code.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook ab_test_noncompliance.ipynb
```

All data is simulated and all numbers are illustrative.
