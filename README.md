# Towards Explainable Food Hazard Detection: A Neuro-Symbolic Approach

Authors: Neelima Prasad, Advait Deshmukh and Karthik Sairam \
Class: CSCI 7000 - Topics in Neuro-symbolic NLP \
This is our neuro-symbolic approach for solving SemEval 2025's Task 9 : Food Hazard Detection\
Below is an overview of our repository \
### Datasets
The datasets folder contains a csv of the manually labeled English food recall titles. There are two different files, however we mainly work with incidents_train.csv. The other file is a sample of the data

### Data Analysis
The data analysis file sifts through the data and gathers all the product and hazard categories and filters duplicates. 

### Root
This folder is where our pipeline is stored
#### cocoex
This folder contains tsv files for all the following labels : products, hazards, product categories, hazard categories, and a file containing all the labels. These nodes were generated using cocoex, and are the inputs to the Llama model for filtering
#### data
This folder contains all the extracted keywords that Llama generated for each of keywords (json file). It also contains a csv of all of the food recall titles. 
#### notebooks
This folder contains three notebooks : LLAMA_Keyword_Extraction.ipynb,conceptnet_lite.ipynb, NLP__Final_Pipeline.ipynb, 
LLAMA_Keyword_Extraction is the code we use to extract the relevent keywords from the titles. \
conceptnet_lite is where we built our own sub-ConceptNet with limited relations and only the english language.
NLP__Final_Pipeline is the code we use to tie everything together and generate our results
