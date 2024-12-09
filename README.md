# Towards Explainable Food Hazard Detection: A Neuro-Symbolic Approach

Authors: Neelima Prasad, Advait Deshmukh and Karthik Sairam \
Class: CSCI 7000 - Topics in Neuro-symbolic NLP \
This is our neuro-symbolic approach for solving SemEval 2025's Task 9 : Food Hazard Detection\
Below is an overview of our repository 

### [Datasets](https://github.com/karthiksairam01/SemEval-Task9/tree/main/Dataset)
The datasets folder contains a csv of the manually labeled English food recall titles. There are two different files, however we mainly work with [incidents_train.csv](https://github.com/karthiksairam01/SemEval-Task9/blob/main/Dataset/incidents_train.csv). The other file is a sample of the data

### [Data Analysis](https://github.com/karthiksairam01/SemEval-Task9/tree/main/Data%20Analysis)
The data analysis file sifts through the data and gathers all the product and hazard categories and filters duplicates. 

### [Root](https://github.com/karthiksairam01/SemEval-Task9/tree/main/root)
This folder is where intermediate files for our pipeline are stored.
#### [CoCo-Ex](https://github.com/karthiksairam01/SemEval-Task9/tree/main/root/cocoex)
This folder contains tsv files for all of the following (obtained by processing titles/labels through CoCo-Ex): [input titles](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/cocoex/outputfile_all.tsv) [products](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/cocoex/products.tsv), [hazards](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/cocoex/hazards.tsv), [product categories](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/cocoex/product_categories.tsv), [hazard categories](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/cocoex/hazard_categories.tsv). These files are fed into LLaMA in the pipeline.
#### [Data](https://github.com/karthiksairam01/SemEval-Task9/tree/main/root/data)
This folder contains all the extracted keywords that Llama generated for each of file output by COCO-Ex (json file): [input titles](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/data/extracted_keywords_incidents_train.json), [products](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/data/extracted_keywords_products.json), [hazards](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/data/extracted_keywords_hazards.json), [product categories](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/data/extracted_keywords_product_category.json), [hazard categories](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/data/extracted_keywords_hazard_category.json).
#### [Notebooks](https://github.com/karthiksairam01/SemEval-Task9/tree/main/root/notebooks)
This folder contains three notebooks : [LLAMA_Keyword_Extraction.ipynb](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/notebooks/LLAMA_Keyword_Extraction.ipynb), [conceptnet_lite.ipynb](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/notebooks/conceptnet_lite.ipynb) , [NLP__Final_Pipeline.ipynb](https://github.com/karthiksairam01/SemEval-Task9/blob/main/root/notebooks/NLP__Final_Pipeline.ipynb). \
&emsp; LLAMA_Keyword_Extraction is the code we use to extract the relevent keywords from the titles. \
&emsp; conceptnet_lite is where we built our own sub-ConceptNet with limited relations and only the english language. \
&emsp; NLP__Final_Pipeline is the code we use to tie everything together and generate our results
