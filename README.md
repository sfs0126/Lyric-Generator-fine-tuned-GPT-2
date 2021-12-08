# Lyric Generation for Different Music Genres
## Fine-Tuning GPT-2 and Evaluating with Perplexity

### This project uses Huggingface GPT-2 transformer to fine-tune text generation models based on lyric data to specific music genres.



Using lyric data for a given genre of music, can we fine-tune a model to genreate lyrics? Yes, we can! This project takes you through the data preprocessing, model training and evaluation with perplexity, and test generation for lyric data. 



Dataset: Song lyrics from 6 musical genres (Data scraped from the website vagalume.com.br)

https://www.kaggle.com/neisse/scrapped-lyrics-from-6-genres

Data used for this project can be downloaded from Kaggle at the link above. The data preprocessing requires both the lyrics-data.csv and the artists-data.csv



With the data preprocessing notebook, we take the datasets and split them by genre to give us our genre specific datasets. Here, we use rock, pop, and hip hop genres. Then, we can obtain our train, test, validation datasets to fine-tune our models. 



The model train and evaluation notebook takes us through the fine-tuning steps. Here, we fully trained and evaluated our hip hop model, but code is included for rock and pop genres as well. We trained using the run_clm.py file, origionally from the Huggingface, but updated with some modifications (to account for adding BOS and EOS tokens in our preprocessing). Then, we evaluate our fine-tuned and baseline GPT-2 models with out test dataset. Here, we can evaluate and compare perplexity scores. In the notebook, we can see just how well our fine-tuned model preforms vs. the baseline GPT-2. 



The lyric generation notebook shows how to generate lyrics from our models - you can see how much the lyric outputs vary! We generated text by using the run_generation.py file, origionally from the Huggingface, but again with minor updates. Not only do we quantitatively show that our fine-tuned model outpreforms the baseline GPT-2 with perplexity, we can see and compare the results qualitatively! 



Try it out and see what lyrics you can generate! 





Resources:

https://github.com/huggingface/transformers/tree/master/examples/pytorch

https://towardsdatascience.com/fine-tuning-gpt2-for-text-generation-using-pytorch-2ee61a4f1ba7
