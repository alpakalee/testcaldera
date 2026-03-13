---
layout: default
title: Results
nav_order: 7
---

# Experimental Results
{: .no_toc }

{: .note }
> This page will be updated with final numbers upon paper publication.

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Experimental Setup

- **Dataset**: 11 KISA CTI reports (2020–2024)
- **LLMs**: Claude Sonnet 4.5, GPT-4o, Gemini 2.5 Pro, Grok 4 Fast
- **Repetitions**: 5 runs per report-LLM pair
- **Total experiments**: 220 (11 × 4 × 5)
- **Target environment**: Windows 10 Pro (PC1), Windows 10 (PC2), Windows Server 2019 AD (PC3)
- **Caldera version**: 5.3.0

---

## RQ1: Generation Time and Cost

> How much time and cost does the pipeline require to generate an adversary emulation scenario from a CTI report?

### Claude Sonnet 4.5 — Per-Report Breakdown

| ID | Abilities | Total (s) | Generation (s) | Correction (s) | Execution (s) | Cost ($) |
|----|-----------|----------|---------------|---------------|-------------|---------|
| TTPs#1 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#2 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#3 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#4 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#5 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#6 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#7 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#8 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#9 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#10 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#11 | TBD | TBD | TBD | TBD | TBD | TBD |
| **Avg** | **TBD** | **TBD** | **TBD** | **TBD** | **TBD** | **TBD** |

### LLM Model Comparison

| Model | Avg. Abilities | Total (s) | Generation (s) | Cost ($) |
|-------|---------------|----------|---------------|---------|
| Claude Sonnet 4.5 | TBD | TBD | TBD | TBD |
| GPT-4o | TBD | TBD | TBD | TBD |
| Gemini 2.5 Pro | TBD | TBD | TBD | TBD |
| Grok 4 Fast | TBD | TBD | TBD | TBD |

<!-- ![RQ1 Figure]({{ site.baseurl }}/assets/images/results/rq1.png) -->

---

## RQ2: Execution Success Rate & Self-Correcting Effect

> What is the execution success rate of generated scenarios, and how much does Self-Correcting improve it?

### Per-Report Success Rate (Claude Sonnet 4.5)

| ID | Abilities | Initial SR (%) | Final SR (%) | Improvement (pp) | Corrections | Retries |
|----|-----------|--------------|------------|-----------------|------------|--------|
| TTPs#1 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#2 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#3 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#4 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#5 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#6 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#7 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#8 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#9 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#10 | TBD | TBD | TBD | TBD | TBD | TBD |
| TTPs#11 | TBD | TBD | TBD | TBD | TBD | TBD |
| **Avg** | **TBD** | **TBD** | **TBD** | **TBD** | **TBD** | **TBD** |

### Failure Type Distribution & Recovery Rate

| Failure Type | Count | % of Total | Recovery Rate (%) |
|-------------|-------|-----------|-----------------|
| `syntax_error` | TBD | TBD% | TBD% |
| `timeout` | TBD | TBD% | TBD% |
| `dependency_error` | TBD | TBD% | TBD% |
| `missing_env` | TBD | TBD% | TBD% |
| `unrecoverable` | TBD | TBD% | — |

<!-- ![RQ2 Figure]({{ site.baseurl }}/assets/images/results/rq2.png) -->

---

## RQ3: CTI Coverage & ATT&CK Validity

> How faithfully do generated scenarios reproduce the ATT&CK techniques from source CTI reports?

| Metric | Value |
|--------|-------|
| ATT&CK Validity (% of abilities with valid Technique ID) | TBD % |
| CTI Coverage (% of abilities matching report techniques) | TBD % |

<!-- ![RQ3 Figure]({{ site.baseurl }}/assets/images/results/rq3.png) -->

---

## RQ4: KISA Checklist vs. Attack Success Rate Correlation

> Does a correlation exist between KISA security checklist compliance and attack success rate?

| Environment | Checklist Compliance (%) | Attack Success Rate (%) |
|-------------|------------------------|----------------------|
| TTPs#1 | TBD | TBD |
| TTPs#2 | TBD | TBD |
| TTPs#3 | TBD | TBD |
| TTPs#4 | TBD | TBD |
| TTPs#5 | TBD | TBD |
| TTPs#6 | TBD | TBD |
| TTPs#7 | TBD | TBD |
| TTPs#8 | TBD | TBD |
| TTPs#9 | TBD | TBD |
| TTPs#10 | TBD | TBD |
| TTPs#11 | TBD | TBD |

**Correlation (r):** TBD

<!-- ![RQ4 Figure]({{ site.baseurl }}/assets/images/results/rq4.png) -->

---

## RQ5: LLM Model Performance Comparison

> Is there a significant performance difference between LLM models for end-to-end adversary emulation?

| Model | Avg. Abilities | Initial SR (%) | Final SR (%) | Improvement (pp) | Cost ($) |
|-------|---------------|--------------|------------|-----------------|---------|
| Claude Sonnet 4.5 | TBD | TBD | TBD | TBD | TBD |
| GPT-4o | TBD | TBD | TBD | TBD | TBD |
| Gemini 2.5 Pro | TBD | TBD | TBD | TBD | TBD |
| Grok 4 Fast | TBD | TBD | TBD | TBD | TBD |

<!-- ![RQ5 Figure]({{ site.baseurl }}/assets/images/results/rq5.png) -->
