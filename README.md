# Project summary
News Summarizer and Translator from English to Arabic, that can scrape news articles from almost any international news website.

# Motivation
Facilitate access to international news to Arabic readers. Inspired by millions of Arabs who can't read English and want to be aware of international politics, events, etc...

# Dataset
We used large pre-trained models already fine tuned using huge datasets, so we didn't need to further train them.

# Architecture
The project's architecture consists of:

### 1.  Scraping news website
[Newspaper3k library](https://github.com/codelucas/newspaper) is a simple and very powerful library for scraping almost any news website without the need to explicitly provide any HTML tags.

### 2. Summarize latest news articles
Was done using [BART-large model](https://huggingface.co/facebook/bart-large-cnn) which is pre-trained on English language, and fine-tuned on [CNN Daily Mail dataset](https://huggingface.co/datasets/cnn_dailymail) which was introduced in a 2019 paper by Lewis et al. (you can read more about it [here](https://arxiv.org/abs/1910.13461)) with the code released in this [repository](https://github.com/pytorch/fairseq/tree/master/examples/bart)

### 3. Translate articles summary
Was done using [mBART-50 many to many multilingual machine translation model](https://huggingface.co/facebook/mbart-large-50-many-to-many-mmt). Knowing that this model is a fine-tuned checkpoint specifically for Machine Translation of [mBART-large-50](https://huggingface.co/facebook/mbart-large-50) which is a general purpose multilingual Sequence-to-Sequence model.

# Conclusion
You can use our **Article Scraper-Summerizer-Translator** to get a glimpse of recent international news in Arabic for any non-English speaker with ease.
