# PUB-R
This is the code and data for the paper "PUB-R: End-to-End TOD System via Turn-Based Positioning". 

## Abstract
In high demand across countless industries, Task-Oriented Dialog (TOD) systems [11][22] may greatly reduce the overhead costs of customer service personnel and simplify human resource processes. The GPT-2 model is used across a variety of TOD systems, but these systems do not take into account the turn number, a critical consideration for multi-turn dialogs. Our paper PUB-R introduces a new embedding input method for recent end-to-end task dialog models [23] [6]: the “Turn-Based Positioning Embedding Method” (TPEM). Our results show that (1) PUB-R can obtain better training performance in a shorter training time compared with previous SOTA models and (2) rapid model convergence can be achieved by reducing the number of epochs required without compromising performance. Our implementation successfully improves upon previous end-to-end dialog systems in evaluation score of the model [39] with the "turn-based positioning" with shorter training times and without requiring additional manual annotation.

## Requirements
- CUDA 10.1
- Python 3.6
- PyTorch 1.5
- spaCy
- transformers 2.11

We use the tokenization tool in SpaCy which can be installed through:

```python -m spacy download en_core_web_sm```
