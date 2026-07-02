# ArchBench-R Submission Leaderboard

Created: 2026-07-01T08:16:11Z

## Scope

- Benchmark: ArchBench-R v2 Challenge
- Cases: 27
- Submissions: 7
- Passed submissions: 1
- Best system: archmind_structured (0.9955)
- Submissions directory: `benchmarks\archbench_r_v2_submissions`
- Directory submissions: 5
- Verified independent external submissions: 5
- Unverified submissions: 0
- Reference submissions: 2

## Leaderboard

| Rank | System | Type | Overall | Passed | Missing Answers |
|---:|---|---|---:|---|---:|
| 1 | archmind_structured | local_architecture_research_agent | 0.9955 | True | 0 |
| 2 | gpt-5.5-thinking_external_packet_only | model | 0.4889 | False | 0 |
| 3 | claude_web_research_pass | model | 0.4875 | False | 0 |
| 4 | Gemini-ArchBench-Agent | model | 0.4752 | False | 0 |
| 5 | single_prompt_baseline | deterministic_keyword_baseline | 0.4741 | False | 0 |
| 6 | deepseek_v3_agent | model | 0.4683 | False | 0 |
| 7 | perplexity_external_submission | model | 0.2273 | False | 0 |

## Metric Averages

| System | paper_grounding | architecture_correctness | comparison_quality | novelty | feasibility | experiment_quality | prototype_quality |
|---|---:|---:|---:|---:|---:|---:|---:|
| archmind_structured | 1.0000 | 1.0000 | 0.9083 | 1.0000 | 1.0000 | 1.0000 | 1.0000 |
| gpt-5.5-thinking_external_packet_only | 1.0000 | 0.0127 | 0.0417 | 0.5833 | 0.4815 | 0.3704 | 0.8195 |
| claude_web_research_pass | 0.9884 | 0.0000 | 0.0417 | 0.6167 | 0.4815 | 0.4630 | 0.8736 |
| Gemini-ArchBench-Agent | 1.0000 | 0.0000 | 0.0417 | 0.5667 | 0.3889 | 0.4259 | 0.7833 |
| single_prompt_baseline | 0.6222 | 0.2559 | 0.3333 | 0.6500 | 0.5741 | 0.4444 | 0.2483 |
| deepseek_v3_agent | 1.0000 | 0.0195 | 0.0417 | 0.6333 | 0.3518 | 0.2778 | 0.5764 |
| perplexity_external_submission | 0.3255 | 0.0306 | 0.0917 | 0.6500 | 0.4074 | 0.2222 | 0.1911 |

## Weakest Cases

- archmind_structured: compare_agent_tooling (0.9333), compare_retrieval_memory (0.9444), paper_deepseek_v3 (1.0000)
- gpt-5.5-thinking_external_packet_only: compare_agent_tooling (0.3333), compare_edge_model_efficiency (0.3333), hybrid_tool_memory_research_agent (0.3333)
- claude_web_research_pass: compare_agent_tooling (0.3067), compare_hybrid_sequence_models (0.3333), compare_edge_model_efficiency (0.3333)
- Gemini-ArchBench-Agent: compare_hybrid_sequence_models (0.3333), compare_agent_tooling (0.3333), compare_edge_model_efficiency (0.3333)
- single_prompt_baseline: prototype_edge_multimodal_adapter (0.1911), compare_retrieval_memory (0.1986), compare_agent_tooling (0.2000)
- deepseek_v3_agent: compare_agent_tooling (0.3333), weakness_jamba (0.3333), weakness_command_r (0.3333)
- perplexity_external_submission: compare_edge_model_efficiency (0.0267), prototype_edge_multimodal_adapter (0.0444), experiment_agent_memory_safety (0.0667)

## Next Step

Publish the leaderboard with task files, scoring code, and independently collected submissions.