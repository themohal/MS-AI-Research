# MS-AI-Research NLP
This repository is about MS Thesis Research Title Saraiki Langange Word Prediction and Spell Correction Framework. Saraiki language is local language of Pakistan. To the best of our knowledge this is first research conducted on the language using Natural Language Processing with Deep Learning.


## Data Gathering

Data gathering is hectic task as there are no authentic resource or dataset available online. Data was collected from different sources like Saraiki news websites, wikipedia dumps etc.

## Data Cleaning and Preprocessing

Processing and tokenization steps are essential in NLP. There are no known tools that can process this language. Custom preprocessing and regex opertions are combined to clean and process the data.

## Training Word2Vec and Fasttext

Word2Vec and Fasttext are two models are trained to extract embeddings. Word2vec works on word level and Fasttext works on character level. Handling Unknown is not possible in Word2Vec we assign zero vector or random vector to unknown words. Fasttext can handle unknown words. Both the models are trained using different vector sizes and window sizes.

## Similarity Check

Wordsim353 is state of the art dataset to check similarity. It is translated to Saraiki and check the similarity of Word2Vec and Fasttext models. Results are compared to to know the best vector size and window size.

## Spell Correction
Edit distance is a matrix base technique that can be used to correct spell correction in strings. Hundered words are taken from Saraiki language randomly and delibratelty incorrected with different character sizes. Spell correction performed worst as we increased wrong characters.

## Training Roberta

RoBERTa ( Robustly Optimized Pretrained BERT Approach) is a transformer base model, It can be used to train on new dataset and get the results. RoBERTa model can be used for various tasks and missing word prediction is one of them. First the tokenizer is trained on new dataset and then RoBERTa is trained using famous platform Huggingface. RoBERTa Base and RoBERTa Distilled models are trained.

## Word Prediction

Over two hundered sentences are taken out randomly as test dataset, One word at random place is removed from sentences except first postion. These sentences are then provided as input to RoBERTa model to predict the missing words. Also the same dataset is provided as input to Word2Vec and Fasttext to predict the missing words. 

## Comparing Results

From the results it is concluded that RoBERTa performed well on prediction task as comapred to Word2Vec and Fasstext. Because RoBERTa can preserve context and it can predict more accurately.

## References

[Paper Reference](https://ieeexplore.ieee.org/document/9972938)
[HuggingFace Reference](https://huggingface.co/themohal/saraiki-roberta-base-small-finetuned3)
