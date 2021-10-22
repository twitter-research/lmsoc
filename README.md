# LMSOC: An Approach for Socially Sensitive Pretraining

[![Open All Collab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/twitter-research/lmsoc) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/twitter-research/lmsoc/HEAD)


![image](lmsoc.png)

Code for reproducing the paper **[LMSOC: An Approach for Socially Sensitive Pretraining](https://arxiv.org/abs/2110.10319)** to appear at [2021 Conference on Empirical Methods in Natural Language Processing: Findings](https://2021.emnlp.org/papers). 

## Abstract

> While large-scale pretrained language models have been shown to learn effective linguistic representations for many NLP tasks, there remain many real-world contextual aspects of language that current approaches do not capture. For instance, consider a cloze-test "I enjoyed the ____ game this weekend": the correct answer depends heavily on where the speaker is from, when the utterance occurred, and the speaker's broader social milieu and preferences. Although language depends heavily on the geographical, temporal, and other social contexts of the speaker, these elements have not been incorporated into modern transformer-based language models. We propose a simple but effective approach to incorporate speaker social context into the learned representations of large-scale language models. Our method first learns dense representations of social contexts using graph representation learning algorithms and then primes language model pretraining with these social context representations. We evaluate our approach on geographically-sensitive language-modeling tasks and show a substantial improvement (more than 100% relative lift on MRR) compared to baselines.

## Citation

Please cite as:

> Kulkarni, V., Mishra, S., & Haghighi, A. (2021). LMSOC: An Approach for Socially Sensitive Pretraining. Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing: Findings. [arXiv](https://arxiv.org/abs/2110.10319)


```bibtex
@inproceedings{kulkarni2021lmsoc,
  title={LMSOC: An Approach for Socially Sensitive Pretraining},
  author={Kulkarni, Vivek and Mishra, Shubhanshu and Haghighi, Aria},
  booktitle={Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing: Findings},
  year={2021}
  address={Online},
  publisher={Association for Computational Linguistics},
  pages={1--9},
  eprint={2110.10319},
  archivePrefix={arXiv},
  primaryClass={cs.CL}
}
```

## Reproducibility

NOTE: Dependencies are specified in the notebooks. But we have also encluded an `requirements.txt` and `environment.yml` files to install dependencies using pip or conda. 

* Create Social Context Embeddings via the example notebook `embed_time_toy_task.ipynb` which contains the implementation of how to embed time for Task 1 in the paper.
* Upload the files in `data/` to the location where you will run the next notebook. 
* The notebook `lmsoc_train_and_eval_toy_task.ipynb` contains the LMSOC training code. 
  * **NOTE:** This notebook assumes you have already trained social context embeddings for the data you have (for example, here the social context is time).
  * It is a runnable colab notebook which demonstrates the entire process of training and evaluating LMSOC as described in the paper. 
  * If run, it will reproduce the experimental setup for Task 1 and ultimately yield Figure 2. 
  * In order to run this notebook in colab, open this notebook in Google Colab and upload the files in "data" directory to your colab workspace. 


# Security Issues?

Please report sensitive security issues via Twitter's bug-bounty program (https://hackerone.com/twitter) rather than GitHub.
