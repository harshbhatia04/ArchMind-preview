# ArchMind Demo Script

## Goal

Show ArchMind as a research-agent backend, not a chatbot demo.

## Demo Flow

1. Show the project summary.
   - Open `docs/one-page-project-summary.md`.
   - Explain that the system studies AI architecture papers and validates architecture-research outputs.

2. Show the evidence bundle.
   - Open `release/archmind_v1_evidence/README.md`.
   - Point to the leaderboard, readiness report, external submissions, and public packet manifest.

3. Show the final leaderboard.
   - Open `reports/archbench_r_v1_leaderboard.md`.
   - Highlight that ArchMind ranked first against three independent external model submissions.

4. Show the final readiness gate.
   - Open `reports/world_class_readiness_report.md`.
   - Highlight `8 / 8` gates passed and no blocking gates.

5. Show the honest claim wording.
   - Open `docs/claim-card.md`.
   - Emphasize that the claim is limited to ArchBench-R v1 and that broader external evaluation remains the next research step.

6. Show the harder v2 challenge.
   - Open `reports/archbench_r_v2_report.md`.
   - Highlight 27 harder cases, ArchMind 0.9955, baseline 0.4741, and the remaining comparison-quality cases to improve.

7. Show the v2 external validation status.
   - Open `reports/archbench_r_v2_external_validation_status.md`.
   - Emphasize that v2 has 5 / 5 external submissions collected and the validation gate passed.

## Commands To Reproduce

```powershell
python -m archmind.cli compare-external-benchmark-submission-dir
python -m archmind.cli external-validation-status
python -m archmind.cli world-class-readiness
python -m archmind.cli run-external-benchmark --benchmark .\benchmarks\archbench_r_v2.json --out .\reports\archbench_r_v2_results.json --report .\reports\archbench_r_v2_report.md
```

Expected result:

- External validation: 3 / 3 submissions, passed
- World-class readiness: 8 / 8 gates, no blockers
- ArchBench-R v2 Challenge: 5 / 5 external submissions collected; validation gate passed
