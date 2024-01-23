# BERT Question-Answering System
[VIDEO LINK](https://drive.google.com/file/d/12GcIImLBFkrcn3PV2JDgMhj7kQp9Vm1T/view?usp=sharing)

## Project Overview
This project aims to implement Section 3 of the paper, [A BERT Baseline for the Natural Questions](https://arxiv.org/pdf/1901.08634.pdf), focusing on finetuning BERT to create a Question-Answering (QA) system. The trained model will be capable of providing token spans for answers given a question and context. If no answer is found in the context, the system should return a span pointing to the [CLS] token.

## Dataset Notes
* The dataset only contains two annotated answer types: (1) no answer, and (2) short answer.
* Each dataset instance provides a context to extract an answer span directly for its corresponding question.
* The dataset uses character indices instead of token indices relative to the context.

## Implementation
Finetune DistilBERT (distilbert-base-cased) for the QA task. 
See `BERT_Question_Answering_System_Final.ipynb` for more details.

## Training the Model
Download `BERT_Question_Answering_System_Final.ipynb` and run it in Google Colab.

## Results
| Precision | Recall | F1    |
|-----------|--------|-------|
| 0.663     | 0.694  | 0.656 |