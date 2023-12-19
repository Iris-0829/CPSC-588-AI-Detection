# CPSC-588-AI-Detection

## Instruction for Running the Experiments
### Computing Infrastructure
The experiments should be run on Google Colab, using V100 GPU
All dependencies should already be satisfied or installed by simply running the notebooks

### Upload Datasets to Drive
First, please download the PubMedQA dataset (`ori_pqaa.json` and `ori_pqal.json`):
- `ori_pqaa.json` ([Google Drive](https://drive.google.com/file/d/15v1x6aQDlZymaHGP7cZJZZYFfeJt2NdS/view))
- `ori_pqal.json` ([Github](https://github.com/pubmedqa/pubmedqa/blob/master/data/ori_pqal.json))
Then, upload them to Google Drive, at the specific path:
```
/content/gdrive/MyDrive/CPSC_588_dataset/
```
(i.e. upload `ori_pqaa.json` and `ori_pqal.json` into a folder named `CPSC_588_dataset`, please make sure this is correctly performed!)

For the Wiki Intro dataset, the downloading code is already included in the notebooks so you don't have to worry about it

### Miscellaneous / Random Settings
Some more settings before running the notebooks:
1. First, for each notebook, replace the current `openai.api_key` with your api key
2. If you wish, you could add a line:
```
random.seed(0)
```
as the first line of the `downsample_data` function under the `Dataset` tab of the code.

This step is not necessary since we've tested that our model is robust with different data samples

### Experiments: Baseline Model
Then, to run the baseline experiments, simply run
`CPSC_588_Statistical_AI_Detection_Baseline.ipynb`
anywhere in the drive

If you wish to run the experiment on different datasets, please change this line in the second cell under the Model Training block
```
dataset = "Wiki" # "PMQA"
```
To the corresponding dataset

### Experiments: Model with Statistical Embeddings Only
To run the Statistical Embedding Experiments:

## Dataset

### Wiki Intro
This is available on [HuggingFace](https://huggingface.co/datasets/aadityaubhat/GPT-wiki-intro)

### PubMedQA
- `ori_pqaa.json` ([Google Drive](https://drive.google.com/file/d/15v1x6aQDlZymaHGP7cZJZZYFfeJt2NdS/view))
- `ori_pqal.json` ([Github](https://github.com/pubmedqa/pubmedqa/blob/master/data/ori_pqal.json))
