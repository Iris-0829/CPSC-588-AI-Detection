# CPSC-588-AI-Detection

## Instruction for Running the Experiments
The experiments should be run on Google Colab, using V100 GPU
All dependencies should already be satisfied or installed by simply running the notebooks

First, please download the PubMedQA dataset (`ori_pqaa.json` and `ori_pqal.json`):
- `ori_pqaa.json` ([Google Drive](https://drive.google.com/file/d/15v1x6aQDlZymaHGP7cZJZZYFfeJt2NdS/view))
- `ori_pqal.json` ([Github](https://github.com/pubmedqa/pubmedqa/blob/master/data/ori_pqal.json))
Then, upload them to Google Drive, at the specific path:
```
/content/gdrive/MyDrive/CPSC_588_dataset/
```
(i.e. upload `ori_pqaa.json` and `ori_pqal.json` into a folder named `CPSC_588_dataset`, please make sure this is correctly performed!)
For the Wiki Intro dataset, the downloading code is already included in the notebooks so you don't have to worry about it

Some settings before running the notebooks:
First, for each notebook, replace the `openai.api_key` with your api key

## Dataset

### Wiki Intro
This is available on [HuggingFace](https://huggingface.co/datasets/aadityaubhat/GPT-wiki-intro)

### PubMedQA
- `ori_pqaa.json` ([Google Drive](https://drive.google.com/file/d/15v1x6aQDlZymaHGP7cZJZZYFfeJt2NdS/view))
- `ori_pqal.json` ([Github](https://github.com/pubmedqa/pubmedqa/blob/master/data/ori_pqal.json))
