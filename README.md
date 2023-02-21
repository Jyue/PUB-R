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

## Data Preprocessing
The original data files are put under data/multi-woz, which includes:

data.json: The orignal MultiWOZ 2.0 data released by researchers in University of Cambridge available here
annotated_user_da_with_span_full.json: A preprocessed and fully annotated version of MultiWOZ 2.0 data released by developers of Convlab available here
We mainly show the implementation process on MultiWOZ 2.0. If you want to implement later versions you'll have to get the dataset yourself and change the corresponding paths in the scripts or use the scripts postfixed with "21".

Get ready for preprocessng:

python data_analysis.py
python preprocess.py
