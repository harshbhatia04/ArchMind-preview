# ArchBench-R v2 Challenge Rubric

## Scope

Stress-test AI architecture-research agents on harder multi-paper design, critique, experiment, and prototype tasks.

## Submission Schema

Submit a JSON file with:

```json
{
  "system_name": "name",
  "system_type": "human_or_model_or_agent",
  "provenance": {
    "independent_external": true,
    "submitted_by": "person_or_model_runner",
    "method_note": "Model or human workflow used.",
    "private_gold_used": false
  },
  "answers": [
    {
      "id": "task id",
      "source_titles": [
        "paper titles used"
      ],
      "evidence_items": 1,
      "architecture_blocks": [
        "Transformer"
      ],
      "comparison_axes": [
        "backbone"
      ],
      "novelty_terms": [
        "hybrid"
      ],
      "weaknesses": [
        "failure mode"
      ],
      "experiments": [
        "ablation"
      ],
      "modules": [
        "module"
      ],
      "prototype": "code or pseudocode"
    }
  ]
}
```

## Metrics

- `paper_grounding`: uses the requested source titles and includes evidence.
- `architecture_correctness`: Jaccard overlap with expected architecture blocks.
- `comparison_quality`: recalls required comparison axes.
- `novelty`: covers required hybrid or mechanism novelty terms.
- `feasibility`: detects expected risks and weaknesses.
- `experiment_quality`: includes required baseline and ablation terms.
- `prototype_quality`: includes expected module boundaries and runnable-code signals.

## Tasks

| Task | Type | Sources |
|---|---|---|
| paper_deepseek_v3 | paper_to_architecture | DeepSeek-V3 Technical Report |
| paper_jamba | paper_to_architecture | Jamba: A Hybrid Transformer-Mamba Language Model |
| paper_memgpt | paper_to_architecture | MemGPT: Towards LLMs as Operating Systems |
| paper_command_r | paper_to_architecture | Command R: Retrieval-Augmented Generation at Production Scale |
| paper_self_rag | paper_to_architecture | Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection |
| paper_lfm2 | paper_to_architecture | LFM2 Technical Report: Efficient Mobile Foundation Models |
| paper_recurrent_gemma | paper_to_architecture | RecurrentGemma: Moving Past Transformers for Efficient Open Language Models |
| paper_voyager | paper_to_architecture | Voyager: An Open-Ended Embodied Agent with Large Language Models |
| compare_retrieval_memory | architecture_comparison | Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks, REALM: Retrieval-Augmented Language Model Pre-Training, Atlas: Few-shot Learning with Retrieval Augmented Language Models, MemGPT: Towards LLMs as Operating Systems, Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection |
| compare_hybrid_sequence_models | architecture_comparison | Mamba: Linear-Time Sequence Modeling with Selective State Spaces, Retentive Network: A Successor to Transformer for Large Language Models, RWKV: Reinventing RNNs for the Transformer Era, Gated Linear Attention Transformers with Hardware-Efficient Training, Jamba: A Hybrid Transformer-Mamba Language Model |
| compare_agent_tooling | architecture_comparison | ReAct: Synergizing Reasoning and Acting in Language Models, Toolformer: Language Models Can Teach Themselves to Use Tools, Gorilla: Large Language Model Connected with Massive APIs, AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation, The Fugu Framework: An Open-Ended and Adaptive Framework for Collaborative AI Agents |
| compare_edge_model_efficiency | architecture_comparison | LFM2 Technical Report: Efficient Mobile Foundation Models, Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone, MobileBERT: a Compact Task-Agnostic BERT for Resource-Limited Devices, DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter, Gemma 2: Improving Open Language Models at a Practical Size |
| hybrid_mla_moe_retrieval_agent | hybrid_architecture | DeepSeek-V3 Technical Report, Command R: Retrieval-Augmented Generation at Production Scale, MemGPT: Towards LLMs as Operating Systems, AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation |
| hybrid_jamba_jepa_retrieval | hybrid_architecture | Jamba: A Hybrid Transformer-Mamba Language Model, LLM-JEPA: Large Language Models Meet Joint Embedding Predictive Architectures, Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks, Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection |
| hybrid_edge_multimodal_adapter | hybrid_architecture | LFM2 Technical Report: Efficient Mobile Foundation Models, Qwen-VL: A Versatile Vision-Language Model for Understanding, Localization, Text Reading, and Beyond, LoRA: Low-Rank Adaptation of Large Language Models, Sigmoid Loss for Language Image Pre-Training |
| hybrid_tool_memory_research_agent | hybrid_architecture | ReAct: Synergizing Reasoning and Acting in Language Models, Toolformer: Language Models Can Teach Themselves to Use Tools, MemGPT: Towards LLMs as Operating Systems, The Fugu Framework: An Open-Ended and Adaptive Framework for Collaborative AI Agents |
| weakness_deepseek_v3 | weakness_detection | DeepSeek-V3 Technical Report |
| weakness_jamba | weakness_detection | Jamba: A Hybrid Transformer-Mamba Language Model |
| weakness_command_r | weakness_detection | Command R: Retrieval-Augmented Generation at Production Scale |
| weakness_memgpt | weakness_detection | MemGPT: Towards LLMs as Operating Systems |
| weakness_autogen | weakness_detection | AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation |
| experiment_mla_moe_retrieval_agent | experiment_design | DeepSeek-V3 Technical Report, Command R: Retrieval-Augmented Generation at Production Scale, MemGPT: Towards LLMs as Operating Systems |
| experiment_jamba_sequence_efficiency | experiment_design | Jamba: A Hybrid Transformer-Mamba Language Model, Mamba: Linear-Time Sequence Modeling with Selective State Spaces, Retentive Network: A Successor to Transformer for Large Language Models |
| experiment_agent_memory_safety | experiment_design | MemGPT: Towards LLMs as Operating Systems, Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection, ReAct: Synergizing Reasoning and Acting in Language Models |
| prototype_mla_retrieval_moe_agent | prototype_generation | DeepSeek-V3 Technical Report, Command R: Retrieval-Augmented Generation at Production Scale, Mixtral of Experts |
| prototype_jamba_jepa_agent | prototype_generation | Jamba: A Hybrid Transformer-Mamba Language Model, LLM-JEPA: Large Language Models Meet Joint Embedding Predictive Architectures, The Fugu Framework: An Open-Ended and Adaptive Framework for Collaborative AI Agents |
| prototype_edge_multimodal_adapter | prototype_generation | LFM2 Technical Report: Efficient Mobile Foundation Models, Qwen-VL: A Versatile Vision-Language Model for Understanding, Localization, Text Reading, and Beyond, LoRA: Low-Rank Adaptation of Large Language Models |

## Scoring Command

```powershell
python -m archmind.cli score-external-benchmark-submission --gold benchmarks/archbench_r_v2_gold.json --submission path/to/submission.json
```

## Leaderboard Command

```powershell
python -m archmind.cli compare-external-benchmark-submission-dir --submissions-dir benchmarks/archbench_r_v2_submissions --gold benchmarks/archbench_r_v2_gold.json --baseline-submission benchmarks/archbench_r_v2_single_prompt_baseline_submission.json --archmind-submission benchmarks/archbench_r_v2_archmind_structured_submission.json --out reports/archbench_r_v2_leaderboard.json --report reports/archbench_r_v2_leaderboard.md
```