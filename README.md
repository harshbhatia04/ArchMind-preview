# ArchMind Preview

ArchMind is an AI architecture-research agent that studies machine-learning research papers, extracts reusable architecture patterns, proposes hybrid model designs, and validates those designs through staged evidence gates.

This is a lightweight public preview. The full code, benchmark package, external submissions, and release evidence bundle are kept in a private repository and can be shared for serious review or collaboration.

## Current Result

ArchMind is world-best-claim ready under the ArchBench-R v1 validation suite. In the current validation, it ranked first against three independent external model submissions and passed all eight readiness gates.

| Rank | System | Type | Overall | Passed |
|---:|---|---|---:|---|
| 1 | archmind_structured | local_architecture_research_agent | 0.9958 | True |
| 2 | gpt_5_5_thinking_independent | model | 0.6076 | False |
| 3 | single_prompt_baseline | deterministic_keyword_baseline | 0.5819 | False |
| 4 | archbench_assistant_v1 | model | 0.5767 | False |
| 5 | Namazu | model | 0.5224 | False |

## What Is Included Here

- `one-page-project-summary.md`: short overview of ArchMind and its evidence
- `claim-card.md`: exact claim wording and what not to overclaim
- `collaboration-pitch.md`: outreach and collaboration framing
- `demo-script.md`: suggested review/demo flow
- `evidence/archbench_r_v1_leaderboard.md`: final public leaderboard report
- `evidence/world_class_readiness_report.md`: final 8/8 readiness report
- `evidence/external_validation_status.md`: external validation status
- `evidence/private_bundle_manifest.sha256`: checksum manifest from the private evidence bundle

## Honest Claim

ArchMind ranked first on ArchBench-R v1 against three independent external model submissions and passed all eight readiness gates.

This is not a universal proof that ArchMind is the best possible AI research system in the world. Broader public benchmarking, expert review, stronger baselines, and third-party blind evaluation are still needed.

## Collaboration Ask

I am looking for feedback on benchmark design, scoring fairness, stronger external baselines, and possible research collaboration.

If you want to inspect the full private repo, benchmark files, or external submissions, please contact me and I can share access.
