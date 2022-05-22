

## DIANA

![Drag Racing](diana_overview.png)


### What is DIANA?

DIANA is a large-scale dialogue-narrative parallel corpus. 
It contains 243K (DIAlogue, NArrative) pairs derived from subtitles and synopses of 47,050 English movies and TV episodes.

To facilitate the training of current NLP models, we first split subtitles and synopses into smaller segments. 
Then we align the related segments from each part to shorter (dialogue, narrative) pairs using the dynamic time warping method. 

### Why use DIANA?

Comprehending a dialogue requires a model having diverse capabilities such as paraphrasing, summarizing, narrating, and reasoning. 
(Dialogue, narrative) pairs in DIANA naturally bridge the format and style gaps 
between the dialogues (from multiple speakers) and narratives (from a narrator). 

Besides that, narratives in DIANA reveal varying knowledge types such as summarizing, visual/audial knowledge, 
paraphrasing, text matching, implicit knowledge, causal relationships, and interpersonal relationships. 
The diverse knowledge types in DIANA will benefit dialogue-related downstream tasks such as conversational MRC and dialogue summarization.


### How to use DIANA?

As an example, we provide a "learning-by-narrating" strategy to further pre-train a seq-2-seq model on DIANA before applying it to downstream tasks. 
We show that our model outperforms strong baselines on varying downstream tasks under a zero-shot setting. 
We also observe that DIANA can outperform the vanilla pre-trained models when finetuned on downstream tasks.

We hope that DIANA will promote future research in various ways.


### Download

We provide a sampled dataset in this repository that contains 1k (dialogue, narrative) pairs. 
To download the entire dataset, please fill in this Google form 
and we'll send the link to your email address within a week.


### Citation 

```bibtex
@inproceedings{zhao-etal-2022-learning,
    title = "Learning-by-Narrating: Narrative Pre-Training for Zero-Shot Dialogue Comprehension",
    author = "Zhao, Chao  and
      Yao, Wenlin  and
      Yu, Dian  and
      Song, Kaiqiang  and
      Yu, Dong  and
      Chen, Jianshu",
    booktitle = "Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers)",
    month = may,
    year = "2022",
    address = "Dublin, Ireland",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.acl-short.23",
    pages = "212--218",
    abstract = "Comprehending a dialogue requires a model to capture diverse kinds of key information in the utterances, which are either scattered around or implicitly implied in different turns of conversations. Therefore, dialogue comprehension requires diverse capabilities such as paraphrasing, summarizing, and commonsense reasoning. Towards the objective of pre-training a zero-shot dialogue comprehension model, we develop a novel narrative-guided pre-training strategy that learns by narrating the key information from a dialogue input. However, the dialogue-narrative parallel corpus for such a pre-training strategy is currently unavailable. For this reason, we first construct a dialogue-narrative parallel corpus by automatically aligning movie subtitles and their synopses. We then pre-train a BART model on the data and evaluate its performance on four dialogue-based tasks that require comprehension. Experimental results show that our model not only achieves superior zero-shot performance but also exhibits stronger fine-grained dialogue comprehension capabilities. The data and code are available at https://github.com/zhaochaocs/DIANA.",
}
```


