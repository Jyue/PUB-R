# PUB-R
This is the code and data of six expeiments mentioned in the paper "PUB-R: End-to-End TOD System via Turn-Based Positioning". 

## Description

| Setting | Description | Action Span Used | Positioning Representation |
| :----: | :----: | :----: |
| 1 | Original method used in the 2021 AAAI paper UBAR | Y | - | 
| 2 | - | N | - | 
| 3 |  Our final method | Y | ATP | 
| 4 |  - | N | ATP | 
| 5 | - | Y | RTP-F | 
| 6 | - | Y | RTP-P | 

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
