# mcan-vqa-thai

This repository is originally from https://github.com/MILVLG/mcan-vqa. You can read old README from original authors at https://github.com/suakow/mcan-vqa-thai/blob/master/old_README.md.

This repository is a part of term project of NLP course at Chulalongkorn University, semester 2021/2. This project is about VQA in Thai. We chosed the model https://github.com/MILVLG/mcan-vqa and modify language understanding part by replaced Embedding and LSTM layers with WangchanBERTa from VISTEC-AI(https://github.com/vistec-AI/thai2transformers , https://arxiv.org/abs/2101.09635)

We used VQA 2.0 as dataset by selected 8,000 question-answer pairs as training set and 2,000 pairs as test set from original VQA 2.0 validation set. All of selected 10,000 question-answer pairs were translated to Thai by Google Translate and manually verified by our group.

About the image feature, we used original extracted feature from original repository which able to download by this [link](https://awma1-my.sharepoint.com/personal/yuz_l0_tn/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fyuz%5Fl0%5Ftn%2FDocuments%2Fshare%2Fmscoco%5Fbottom%5Fup%5Ffeatures&originalPath=aHR0cHM6Ly9hd21hMS1teS5zaGFyZXBvaW50LmNvbS86ZjovZy9wZXJzb25hbC95dXpfbDBfdG4vRXNmQmxibUsxUVpGaENPRnByNGM1SFVCelVWMGFIMmgxTWNuUEcxaldBeHl0UT9ydGltZT1TWE1KZjE0WjJVZw)

## Trianing

You require Google Colaboratory-Pro with GPU enabled for training and inference. If you setup you own environment, you can download dependencies required by this project with `requirement.txt`

```
$ pip install -r requirements.txt
```

And you have to download image feature by this [link](https://awma1-my.sharepoint.com/personal/yuz_l0_tn/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fyuz%5Fl0%5Ftn%2FDocuments%2Fshare%2Fmscoco%5Fbottom%5Fup%5Ffeatures&originalPath=aHR0cHM6Ly9hd21hMS1teS5zaGFyZXBvaW50LmNvbS86ZjovZy9wZXJzb25hbC95dXpfbDBfdG4vRXNmQmxibUsxUVpGaENPRnByNGM1SFVCelVWMGFIMmgxTWNuUEcxaldBeHl0UT9ydGltZT1TWE1KZjE0WjJVZw)

The question-answer pairs for training and inference (test set) are included in this repository. You can find them at this [link](https://github.com/suakow/mcan-vqa-thai/tree/master/datasets/vqa).

If you have done above steps. you can fine-tune the model for Thai language by [link](https://github.com/suakow/mcan-vqa-thai/blob/master/run_training.ipynb) by Google Colab or your machine. You have to change the image feature path before running. You can click this [link](https://colab.research.google.com/github/suakow/mcan-vqa-thai/blob/master/run_training.ipynb) to open with Google Colab directly.
 
