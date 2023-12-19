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
Then, to run the baseline experiments, simply run the notebook
`CPSC_588_Statistical_AI_Detection_Baseline.ipynb`
anywhere in the drive

#### Change Dataset:
If you wish to run the experiment on different datasets, please change this line in the second cell under the Model Training block
```
dataset = "Wiki" # "PMQA"
```
To the corresponding dataset

### Experiments: Model with Statistical Embeddings Only
To run the Statistical Embedding Experiments, simply run the notebook
`CPSC_588_Statistical_AI_Detection_StatEmbs.ipynb`
anywhere in the drive

Changing dataset is the same as above

If you need to change the type of Statistical Embeddings or the fusion type, a few things needs to be changed:
#### Change Statistical Embedding Type
All changes happen in the second cell under the Model Training block (the same cell where you change datasets)

There are two variables that you need to change:
```
stat_emb_dim =
stat_fn =
```
1. Use PoS Tag Distribution Embedding Only:
```
stat_emb_dim = 36
stat_fn = calculate_statistical_features_pos
```
2. Use Readability Metrics Embedding Only
```
stat_emb_dim = 8
stat_fn = calculate_statistical_features_readability
```
3. Use both Embeddings at the Same Time
```
stat_emb_dim = 44
stat_fn = calculate_statistical_features
```

#### Change Fusion Type
In the same cell, simply set
```
fusion_type = "early"
or
fusion_type = "late"
```
accordingly

### Experiments: Model with Everything
To run the Experiments with Model that has all modules (i.e. including the Attacker), simply run the notebook
`CPSC_588_Statistical_AI_Detection_Combined.ipynb`
anywhere in the drive

Changing any experiment settings is the same as above (Change Dataset; Change Statistical Embedding Type; Change Fusion Type)

## Dataset

### Wiki Intro
This is available on [HuggingFace](https://huggingface.co/datasets/aadityaubhat/GPT-wiki-intro)

### PubMedQA
- `ori_pqaa.json` ([Google Drive](https://drive.google.com/file/d/15v1x6aQDlZymaHGP7cZJZZYFfeJt2NdS/view))
- `ori_pqal.json` ([Github](https://github.com/pubmedqa/pubmedqa/blob/master/data/ori_pqal.json))
