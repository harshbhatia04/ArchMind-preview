# ArchBench-R Submission Leaderboard

Created: 2026-06-30T16:43:26Z

## Scope

- Benchmark: ArchBench-R v1
- Cases: 16
- Submissions: 5
- Passed submissions: 1
- Best system: archmind_structured (0.9958)
- Submissions directory: `benchmarks/archbench_r_v1_submissions`
- Directory submissions: 3
- Verified independent external submissions: 3
- Unverified submissions: 0
- Reference submissions: 2

## Leaderboard

| Rank | System | Type | Overall | Passed | Missing Answers |
|---:|---|---|---:|---|---:|
| 1 | archmind_structured | local_architecture_research_agent | 0.9958 | True | 0 |
| 2 | gpt_5_5_thinking_independent | model | 0.6076 | False | 0 |
| 3 | single_prompt_baseline | deterministic_keyword_baseline | 0.5819 | False | 0 |
| 4 | archbench_assistant_v1 | model | 0.5767 | False | 0 |
| 5 | Namazu | model | 0.5224 | False | 0 |

## Metric Averages

| System | paper_grounding | architecture_correctness | comparison_quality | novelty | feasibility | experiment_quality | prototype_quality |
|---|---:|---:|---:|---:|---:|---:|---:|
| archmind_structured | 1.0000 | 1.0000 | 0.9333 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| gpt_5_5_thinking_independent | 1.0000 | 0.0226 | 0.7667 | 0.9167 | 0.9028 | 0.7000 | 1.0000 |
| single_prompt_baseline | 0.6146 | 0.5950 | 0.3000 | 0.6667 | 0.4445 | 0.4000 | 0.4000 |
| archbench_assistant_v1 | 0.8458 | 0.1603 | 0.6333 | 0.7500 | 0.8472 | 0.4000 | 0.8700 |
| Namazu | 1.0000 | 0.0399 | 0.5500 | 0.6667 | 0.5000 | 0.3000 | 0.7400 |

## Weakest Cases

- archmind_structured: compare_sparse_experts (0.9333), paper_transformer (1.0000), paper_mixtral (1.0000)
- gpt_5_5_thinking_independent: paper_transformer (0.5000), paper_mixtral (0.5000), paper_flashattention (0.5000)
- single_prompt_baseline: compare_sparse_experts (0.2833), prototype_jepa_moe_research_agent (0.4111), compare_long_context (0.4278)
- archbench_assistant_v1: compare_sparse_experts (0.4000), experiment_design_archmind_hybrid (0.4254), experiment_design_jepa_retrieval (0.4254)
- Namazu: experiment_design_archmind_hybrid (0.4000), compare_multimodal_latent (0.4167), weakness_longnet (0.4167)

## Next Step

Publish the leaderboard with task files, scoring code, and independently collected submissions.