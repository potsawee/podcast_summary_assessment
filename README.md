Podcast Summary Assessment Data
===================================
Data resource in the paper **"Podcast Summary Assessment: A Resource for Evaluating Summary Assessment Methods"** | https://arxiv.org/abs/2208.13265

## Overview
- This dataset is a collection of podcast summaries that were evaluated by humsn experts at the Podcast Challenge at TREC2020.
- The entire podcast dataset for summarization (without summary evaluation annotation) can be found at [this link](https://podcastsdataset.byspotify.com/).
- This dataset has 3580 examples, where each example is a trascript-summary pair with the associated human score. 

## Usage

### Option1: HuggingFace
[update 20/03/2023] the dataset is available on [HuggingFace](https://huggingface.co/datasets/potsawee/podcast_summary_assessment)

```python
from datasets import load_dataset
dataset = load_dataset("potsawee/podcast_summary_assessment")
```


### Option2: Manual Download
Download link**: <https://drive.google.com/file/d/1HtFj27LvV_KlsjhflrGclLb3w0QiR4tW/>, which consists of one data file in JSON format ```podcast_summary_assessment.json``` about 100MB. Example usage:

```python
import json
with open(podcast_summary_assessment.json, 'r') as f:
	content = f.read()
data = json.loads(content)
```

- ```data``` is a list of size 3580.  
- ```data[i]``` is a dictionary containing:
	- ```transcript```: podcast trascript, i.e. document
	- ```summary```: summary
	- ```score```: human score
	- ```attributes```: human annotation for 8 attributes
	- ```episode_id```: podcast episode ID
	- ```system_id```: (anonymized) system ID

## Citation
```
@article{manakul2022podcast,
  title={Podcast Summary Assessment: A Resource for Evaluating Summary Assessment Methods},
  author={Manakul, Potsawee and Gales, Mark JF},
  journal={arXiv preprint arXiv:2208.13265},
  year={2022}
}
```
