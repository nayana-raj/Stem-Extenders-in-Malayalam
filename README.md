# Stem-Extenders-in-Malayalam
Mini-project for the course Natural Language Understanding, Fall 2020.

## Contents:
[1. Problem Statement](#problem-statement)\
[2. Rough Pipeline](#rough-pipeline)\
[3. Data and Tools](#data-and-tools)\
[4. Files in Repository](#files-in-repository)\
[5. References](references)


## Problem Statement:
Inflectional affixation for Malayalam verbs requires attaching a stem extender morpheme to the root form of the verb before the affix itself is attached. 
A seemingly consistent distribution for the kind of stem extenders that verbs take during affixation can be mapped out (based on Pillai (2000) and Nair(2020)). For example, given the root form of the verb ‘vil-’ (to sell), past, participial, adjectival and perfective forms seem to take one kind of extender, termed Type A, and present, future, infinitive, imperfective and gerund forms take another, termed Type B (Nair, 2020).  

![alt text](https://github.com/nayana-raj/Stem-Extenders-in-Malayalam/blob/main/extenders_example.png)
\
(Example from Nair, 2020)\
It is not yet clear whether these verbal stem extenders are morphogically conditioned or lexically listed, although preliminary analyses seem to hint at the former case. In an attempt to understand whether they are morphologically conditioned, we try to map out whether verbs with similar Type A extenders will also have the same Type B extender. 
If we find that there is a consistent mapping in a corpus, then we can predict that a word with one Type-A extender will consistently select one Type-B extender.

## Rough pipeline:
Implementation will involve
1. Grouping verbs from stemmed data
2. To arrive at the root of the verb, evaluating what forms existing stemmers and morphological analysers might give us
3. Based on the above, verbs with similar Type A stems grouped together
4. Words formed with Type B stem for these verbs checked against each other again with a stemmer and a morphanalyzer
5. Checking if the pattern/grouping holds 

## Data and Tools:
[IndicNLPSuite](https://indicnlp.ai4bharat.org/home/) has a Malayalam corpus consisting of 721 million tokens. We will also make use of their morphanalyzer. Additionally, we will use [IndicStemmer](https://github.com/libindic/indicstemmer).
[Here](https://docs.google.com/spreadsheets/d/1Rh4cWnMhCKupoYjap3n2KMygLbDTHFxkylKq2j7JAbs/edit#gid=0) are the results from the above tools.
 
## Files in Repository:
1. Data:  
a. raw_data: 800 sentences from IndicCorp's Malayalam data  
b. preprocessed_data: Preprocessed, tokenized and normalized data  
c. verbs_final: stemmed verbs from [IndicStemmer](https://github.com/libindic/indicstemmer)  
  
2. codeStringData: code to implement problem for a string of about only 12 verbs  
3. codeIndicData: code to implement problem on data from IndicCorp  


## References:
1. Kakwani, Divyanshu, et al. "iNLPSuite: Monolingual Corpora, Evaluation Benchmarks and Pre-trained Multilingual Language Models for Indian Languages." Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing: Findings. 2020.  
2. Kunchukuttan, Anoop. The IndicNLP Library. 2020. https://github.com/anoopkunchukuttan/indic_nlp_library/blob/master/docs/indicnlp.pdf  
3. Nair, Anjali. Binary Tense in Malayalam: Synchronic Evidence.  
4. Nair, Anjali. “Root of the Problem.” Zoomdemic Lecture Series, Apr. 2020.  
5. Pillai, Suranad. Malayalam Lexicon. University of Kerala, 2000.  
6. Thottingal, Santhosh. IndicStemmer. 2015. https://github.com/libindic/indicstemmer  

