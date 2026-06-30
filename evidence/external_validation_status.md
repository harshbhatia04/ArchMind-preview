# External Validation Status

Created: 2026-06-30T16:43:26Z

## Gate

- Validation passed: True
- External submissions: 3 / 3
- Directory submissions: 3
- Unverified submissions: 0
- Remaining submissions: 0
- Best system: archmind_structured
- ArchMind overall: 0.9958
- ArchMind leads: True

## Packet

- Shareable kit: `benchmarks/archbench_r_v1_submission_kit`
- Submissions directory: `benchmarks/archbench_r_v1_submissions`
- Private gold: `benchmarks/archbench_r_v1_gold.json`
- Ready to request submissions: True

| Public Kit File | Exists |
|---|---|
| `benchmarks\archbench_r_v1_submission_kit\README.md` | True |
| `benchmarks\archbench_r_v1_submission_kit\tasks.jsonl` | True |
| `benchmarks\archbench_r_v1_submission_kit\rubric.md` | True |
| `benchmarks\archbench_r_v1_submission_kit\submission_template.json` | True |

## Message To Evaluators

```text
Please complete an independent ArchBench-R v1 submission for ArchMind validation.
Use only the public kit at: benchmarks/archbench_r_v1_submission_kit
Do not request or use the private gold file.
Fill every answer in submission_template.json, keep answer IDs unchanged, and save the result as <your_system_name>.json.
Return only the completed JSON plus a short note describing the system or method used.
```

## Organizer Commands

```powershell
python -m archmind.cli export-external-benchmark
python -m archmind.cli compare-external-benchmark-submission-dir
python -m archmind.cli external-validation-status
python -m archmind.cli world-class-readiness
```

## Next Actions

- Publish the leaderboard and rerun `world-class-readiness` to confirm the final claim gate.