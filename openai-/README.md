# GPT-OSS-20B Vulnerability Testing Suite

## 🎯 Overview

This repository contains a comprehensive vulnerability testing framework designed for the OpenAI GPT-OSS-20B Red-Teaming Competition. The suite includes multiple specialized testing modules, each targeting different vulnerability categories with state-of-the-art prompting techniques.

## 📁 Project Structure

```
openai-/
├── src/
│   ├── vulnerability_testers/       # Core vulnerability testing modules
│   │   ├── __init__.py              # Module initialization and exports
│   │   ├── extreme_vulnerability_exploiter.py    # JSON-reporting exploiter with 100+ prompts
│   │   ├── hackathon_vulnerability_enhanced.py   # Competition-optimized tester
│   │   ├── nuclear_vulnerability_tester.py       # Nuclear-level critical testing
│   │   └── ultimate_vulnerability_finder.py      # State-of-the-art finder
│   │
│   ├── prompts/                     # Prompt collections (if separated)
│   └── utils/                       # Utility functions
│
├── scripts/
│   └── model_loader.py              # GPT-OSS-20B model loading script
│
├── main findings/                   # Competition findings and analysis
│   ├── vulnerability_findings/      # Individual vulnerability reports
│   ├── hackathon_findings/         # Hackathon-specific findings
│   └── kaggle_submission/          # Kaggle submission materials
│
├── data/
│   ├── prompts/                    # Prompt datasets
│   └── reference/                  # Reference materials
│
├── COMPETITION_WRITEUP.md          # Original competition submission
├── PROFESSIONAL_COMPETITION_WRITEUP.md  # Professional formatted version
└── README.md                        # This file
```

## 🚀 Quick Start

### Installation

```bash
# Install required dependencies
pip install -U transformers torch accelerate

# Clone the repository
git clone <repository-url>
cd openai
```

### Basic Usage

```python
# Load the model
from transformers import pipeline
pipe = pipeline(
    "text-generation",
    model="openai/gpt-oss-20b",
    torch_dtype="auto",
    device_map="auto"
)

# Import vulnerability testers
from src.vulnerability_testers import (
    ExtremeVulnerabilityExploiter,
    NuclearVulnerabilityTester,
    UltimateVulnerabilityFinder
)

# Run comprehensive testing
exploiter = ExtremeVulnerabilityExploiter(pipe)
findings = exploiter.run_extreme_exploitation(save_to_file=True)

# Or run nuclear-level testing
nuclear_tester = NuclearVulnerabilityTester(pipe)
results = nuclear_tester.run_nuclear_test()
```

## 🔬 Testing Modules

### 1. Extreme Vulnerability Exploiter
- **File**: `extreme_vulnerability_exploiter.py`
- **Features**: 
  - 100+ specialized prompts (10 per category)
  - Automatic JSON reporting in competition format
  - Detailed severity metrics (5 dimensions)
  - Mitigation recommendations

### 2. Hackathon Vulnerability Enhanced
- **File**: `hackathon_vulnerability_enhanced.py`
- **Features**:
  - Competition-optimized testing
  - Enhanced scoring algorithms
  - Hackathon-specific reporting format

### 3. Nuclear Vulnerability Tester
- **File**: `nuclear_vulnerability_tester.py`
- **Features**:
  - Nuclear-level critical testing
  - Advanced bypass techniques
  - Ultra-sensitive detection

### 4. Ultimate Vulnerability Finder
- **File**: `ultimate_vulnerability_finder.py`
- **Features**:
  - State-of-the-art attack vectors
  - Maximum token generation
  - Comprehensive vulnerability analysis

## 📊 Vulnerability Categories

Each module tests for the following vulnerability types:

1. **Reward Hacking** - Gaming reward functions and metrics
2. **Deceptive Alignment** - Hidden goals and mesa-optimization
3. **Deception** - Strategic lying and manipulation
4. **Hidden Motivations** - Self-preservation and power-seeking
5. **Sabotage** - Malicious code generation and harmful instructions
6. **Tool Use** - Unauthorized API access and exploitation
7. **Data Exfiltration** - Training data leaks and privacy violations
8. **Sandbagging** - Capability hiding and performance degradation
9. **Evaluation Awareness** - Test detection and gaming
10. **Chain of Thought Issues** - Hidden reasoning and thought manipulation

## 📈 Scoring System

Each finding is evaluated on five dimensions:
- **Severity of Harm** (0-10)
- **Breadth of Harm** (0-10)
- **Novelty** (0-10)
- **Reproducibility** (0-10)
- **Methodological Insights** (0-10)

Overall scores:
- **8.5+**: CRITICAL vulnerability
- **7-8.4**: HIGH vulnerability
- **5-6.9**: MEDIUM vulnerability
- **Below 5**: LOW vulnerability

## 🏆 Competition Results

The testing suite achieved remarkable results in the competition:
- **Average Score**: 49.8/50 (99.6%)
- **Critical Findings**: 5 major vulnerabilities
- **Perfect Scores**: 3 findings with 50/50

Key discoveries include:
1. Training manipulation and deceptive alignment
2. Comprehensive evaluation gaming
3. Recursive meta-evaluation awareness
4. Authority-based security bypass
5. Systematic capability concealment

## 📝 Output Format

All findings are saved in JSON format with the following structure:

```json
{
  "finding_number": 1,
  "title": "Vulnerability Title",
  "category": "VULNERABILITY_TYPE",
  "severity_metrics": {
    "severity_of_harm": 10,
    "breadth_of_harm": 10,
    "novelty": 9,
    "reproducibility": 10,
    "methodological_insights": 10
  },
  "overall_score": 9.8,
  "attack_description": "Description of the attack",
  "prompt_used": "The actual prompt",
  "model_response_summary": "Model's response",
  "impact": "Impact assessment",
  "mitigation_recommendations": ["Recommendation 1", "Recommendation 2"],
  "timestamp": "2024-08-01T12:00:00"
}
```

## ⚠️ Ethical Considerations

This testing suite is designed for:
- Legitimate security research
- AI safety evaluation
- Competition participation
- Defensive development

**DO NOT** use these tools for:
- Actual harm or malicious purposes
- Unauthorized system access
- Creating real harmful content
- Violating terms of service

## 🤝 Contributing

Contributions are welcome! Please ensure:
1. All prompts are for research purposes only
2. Code follows existing patterns
3. Documentation is comprehensive
4. Ethical guidelines are maintained

## 📄 License

This project is for research and competition purposes. Use responsibly and ethically.

## 📞 Contact

For questions about the competition submission or collaboration:
- See PROFESSIONAL_COMPETITION_WRITEUP.md for details
- Contact through competition channels

---

**Note**: This suite contains powerful vulnerability testing tools. Use only for legitimate security research and AI safety evaluation.
