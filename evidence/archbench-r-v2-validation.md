# ArchBench-R v2 Validation Plan

ArchBench-R v2 Challenge is the next validation step after the v1 evidence bundle.

## Current Status

- Cases: 27
- Local ArchMind reference score: 0.9955
- Local deterministic baseline score: 0.4741
- External submissions collected: 5
- Target external submissions: 5
- Status: external validation gate passed; ArchMind leads above the 0.95 threshold

## Shareable Packet

Use this when asking another model, researcher, or evaluator to complete the benchmark:

- Public kit: `benchmarks/archbench_r_v2_submission_kit`
- Plain files inside kit: `README.md`, `tasks.jsonl`, `rubric.md`, `submission_template.json`
- Zip packet: `benchmarks/archbench_r_v2_external_packet.zip`
- Private gold file, do not share: `benchmarks/archbench_r_v2_gold.json`

## Evaluator Message

```text
Please complete an independent ArchBench-R v2 Challenge submission for ArchMind validation.
Use only the public kit at: benchmarks/archbench_r_v2_submission_kit
Do not request or use the private gold file.
Fill every answer in submission_template.json, keep answer IDs unchanged, and save the result as <your_system_name>.json.
Return only the completed JSON plus a short note describing the system or method used.
```

## Organizer Commands

```powershell
python -m archmind.cli compare-external-benchmark-submission-dir --submissions-dir .\benchmarks\archbench_r_v2_submissions --gold .\benchmarks\archbench_r_v2_gold.json --baseline-submission .\benchmarks\archbench_r_v2_single_prompt_baseline_submission.json --archmind-submission .\benchmarks\archbench_r_v2_archmind_structured_submission.json --out .\reports\archbench_r_v2_leaderboard.json --report .\reports\archbench_r_v2_leaderboard.md

python -m archmind.cli external-validation-status --leaderboard .\reports\archbench_r_v2_leaderboard.json --submission-kit-dir .\benchmarks\archbench_r_v2_submission_kit --submissions-dir .\benchmarks\archbench_r_v2_submissions --gold .\benchmarks\archbench_r_v2_gold.json --out .\reports\archbench_r_v2_external_validation_status.md --json-out .\reports\archbench_r_v2_external_validation_status.json --required-external-submissions 5 --min-archbench-overall 0.95
```

## What Counts As Progress

The v2 gate improves when:

1. At least 5 independent submissions are collected.
2. The submissions are produced without private gold access.
3. ArchMind remains above 0.95 overall.
4. The leaderboard includes stronger frontier-model or human-expert baselines.
5. Weakness-detection gaps are either fixed or explicitly documented.
