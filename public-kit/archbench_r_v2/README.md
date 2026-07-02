# ArchBench-R v2 Challenge Submission Kit

This folder is safe to share with human evaluators, model runners, or external agents.
It intentionally does not include the private gold file used for scoring.

## Files

- `tasks.jsonl`: public benchmark tasks and source summaries.
- `rubric.md`: output schema, metrics, task list, and scoring command.
- `submission_template.json`: fill-in JSON template with all required answer IDs.

## Submission Rules

1. Fill every answer in `submission_template.json`.
2. Keep each answer `id` unchanged.
3. Put paper titles used in `source_titles`.
4. Count concrete evidence in `evidence_items`.
5. Save the completed file as `<system_name>.json`.
6. Set `provenance.independent_external` to `true` only if the submission was produced outside ArchMind.
7. Keep `provenance.private_gold_used` as `false`; do not use the private gold file.

## Organizer Scoring

The organizer keeps `benchmarks/archbench_r_v2_gold.json` private and runs:

```powershell
python -m archmind.cli compare-external-benchmark-submission-dir --submissions-dir benchmarks/archbench_r_v2_submissions --gold benchmarks/archbench_r_v2_gold.json --baseline-submission benchmarks/archbench_r_v2_single_prompt_baseline_submission.json --archmind-submission benchmarks/archbench_r_v2_archmind_structured_submission.json --out reports/archbench_r_v2_leaderboard.json --report reports/archbench_r_v2_leaderboard.md
```