
# Assignment 4: CubeSat Risk Quick-Assessor  
**Course:** [Your Course Name]  
**Author:** [Your Name]  
**Date:** June 6, 2025  

## 1. Introduction  
The **CubeSat Risk Quick-Assessor** is a CLI application designed to streamline Failure Mode and Effects Analysis (FMEA) for CubeSat subsystems. It calculates Risk Priority Numbers (RPN) and generates actionable reports, supporting rapid risk assessment in aerospace engineering projects.

## 2. Software Description  
### Key Features  
- **Input:**  
  - Subsystem name (e.g., "Power", "Communication")  
  - Custom failure modes or default values  
- **Analysis:**  
  - Auto-calculates RPN (Severity × Occurrence × Detection)  
  - Prioritizes risks (RPN range: 1-100)  
- **Output:**  
  - Generates `.txt` reports with ranked failures  
  - Optional LLM-generated risk descriptions (Ollama integration)  

### Technical Stack  
| Component       | Choice               | Version  |
|-----------------|----------------------|----------|
| Language        | Python               | 3.10+    |
| Compiler        | PyInstaller          | 6.0      |
| LLM Integration | Ollama (LLAMA 3)    | (Optional)|

## 3. AI-Assisted Development  
### LLM Prompts Used  
1. Code Generation:  
   ```plaintext
   "Generate Python code to calculate RPN with random S/O/D values between 1-10."

> Written with [StackEdit](https://stackedit.io/).
