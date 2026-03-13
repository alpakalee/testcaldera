---
layout: default
title: Installation
nav_order: 3
---

# Installation
{: .no_toc }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Prerequisites

| Component | Version | Notes |
|-----------|---------|-------|
| Python | 3.10.11 | Required |
| MITRE Caldera | 5.3.0 | Ubuntu 20.04 LTS recommended |
| VirtualBox | Any recent | For VM snapshot management |
| LLM API key | — | At least one (Anthropic, OpenAI, Google, or xAI) |

---

## 1. Clone the Repository

```bash
git clone https://github.com/alpakalee/caldera-attack-automation.git
cd caldera-attack-automation
```

---

## 2. Install Python Dependencies

```bash
pip install -r requirements.txt
```

Key dependencies:

| Package | Purpose |
|---------|---------|
| `anthropic>=0.40.0` | Claude API |
| `openai>=1.0.0` | GPT API |
| `google-generativeai>=0.3.0` | Gemini API |
| `pdfplumber==0.11.0` | PDF text extraction |
| `mitreattack-python==3.0.6` | MITRE ATT&CK data |
| `pyyaml==6.0.1` | YAML processing |
| `paramiko==3.4.0` | SSH for VirtualBox control |
| `python-dotenv==1.0.1` | Environment variable loading |

---

## 3. Configure Environment Variables

```bash
cp .env.example .env
```

Edit `.env` with your settings. See [Configuration]({{ site.baseurl }}/pages/configuration) for full details.

---

## 4. Set Up MITRE Caldera

Install Caldera on a Linux server (Ubuntu 20.04 LTS recommended):

```bash
git clone https://github.com/mitre/caldera.git --recursive
cd caldera
pip install -r requirements.txt
python server.py --insecure
```

{: .note }
Caldera runs on port 8888 by default. The system also uses port 34444 for payload delivery.

---

## 5. Set Up Target VMs

Each TTP scenario requires specific VM configurations. See `environment_ttps{1-11}.md` for per-scenario requirements.

**General requirements:**
- Windows 10 Pro (PC1, PC2): Caldera agent installed and running
- Windows Server 2019 (PC3, AD): Domain configured per scenario spec
- Clean snapshots saved in VirtualBox (restored between Self-Correcting retries)

{: .warning }
Disable Windows Defender real-time protection on target VMs before running experiments. This is a one-time manual step not covered by the pipeline.

---

## 6. Verify Installation

```bash
# Test LLM connection
python -c "from modules.ai.factory import LLMFactory; print('LLM OK')"

# Test Caldera connection
python -c "
import os, requests
from dotenv import load_dotenv
load_dotenv()
r = requests.get(os.getenv('CALDERA_URL') + '/api/v2/abilities',
                 headers={'KEY': os.getenv('CALDERA_API_KEY')})
print('Caldera OK:', r.status_code)
"
```
