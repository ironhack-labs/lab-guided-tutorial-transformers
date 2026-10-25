![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Transformers


## Introduction

A digital bank wants to route every customer message to the right team before any person reads it. In this lab you compare three ways of doing that on the ten intents that support agents mix up most often: a zero-shot transformer that needs no labelled examples, a DistilBERT model that you fine-tune on 1,185 labelled messages, and the semantic search you built yesterday. You look at the messages as tokens, route them with zero-shot, fine-tune, compare the three methods on 400 new messages, study the mistakes, and write a recommendation for the bank. In the extra task, you measure how many labelled messages fine-tuning needs to beat the semantic search.

The lab follows the **Transformers and Hugging Face** lesson step by step.


## Getting Started

Open the `main.ipynb` file in the `your-code` directory. Follow the instructions, add your code, and answer the questions in the markdown cells. Each challenge ends with a checkpoint that tells you what you should see. The data is in the `data` folder: `banking_train.csv` has the past messages and `banking_test.csv` the new ones, both with the columns `text` and `category`. The notebook keeps only the ten intents of the lab.

The lab needs `pip install transformers torch datasets accelerate sentence-transformers`. The first run downloads three models, about 500 MB, so you need an internet connection. Everything runs on your own computer, with no account and no API key. Fine-tuning takes one to four minutes on a laptop CPU. If your computer is slow, open the notebook in [Google Colab](https://colab.research.google.com), choose **Runtime → Change runtime type → T4 GPU**, and upload the two CSV files.

## Deliverables

- `main.ipynb` with your code, its outputs, and your answers.

## Submission

Upon completion, add your deliverables to git. Then commit git and push your branch to the remote.

## Resources

- [Hugging Face LLM course, chapter 3: Fine-tuning a pretrained model](https://huggingface.co/learn/llm-course/chapter3/1)
- [Transformers documentation: Pipelines](https://huggingface.co/docs/transformers/main_classes/pipelines)
- [Transformers documentation: Trainer](https://huggingface.co/docs/transformers/main_classes/trainer)
- [Model card of the zero-shot model](https://huggingface.co/MoritzLaurer/deberta-v3-xsmall-zeroshot-v1.1-all-33)

## Data

The Banking77 dataset was created by PolyAI and published in [Efficient Intent Detection with Dual Sentence Encoders](https://arxiv.org/abs/2003.04807) (Casanueva et al., 2020). It is available at [PolyAI-LDN/task-specific-datasets](https://github.com/PolyAI-LDN/task-specific-datasets) under the [Creative Commons Attribution 4.0 licence](https://creativecommons.org/licenses/by/4.0/). The files in `data` are the original `train.csv` and `test.csv`, renamed, with no other change.
