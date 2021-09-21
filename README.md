# Open-CyKG
## Open-CyKG: An Open Cyber Threat Intelligence Knowledge Graph

[![Journal](https://img.shields.io/badge/Journal-Knowledge--Based%20Systems-blue)](https://www.journals.elsevier.com/knowledge-based-systems)
[![Paper](https://img.shields.io/badge/Paper-Open--CyKG-red)](ADD link)
[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-Injy%20Sarhan-yellow)](https://scholar.google.nl/citations?user=Otq5vX0AAAAJ&hl=nl)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Injy%20Sarhan-brightgreen)](https://linkedin.com/in/injy-sarhan-03294295)


### Model Description

Open-CyKG is a framework that is constructed using an attention-based neural Open Information Extraction (OIE) model to extract valuable cyber threat information from unstructured Advanced
Persistent Threat (APT) reports. More specifically, we first identify relevant entities by developing a neural cybersecurity Named Entity Recognizer (NER) that aids in labeling relation triples generated by the OIE model. Afterwards, the extracted structured data is canonicalized to build the KG by employing fusion techniques using word embeddings.

<p align="center">
 
  <img src="https://github.com/IS5882/Open-CyKG/blob/main/Open%20CyKg%20images-Framework.png" width="550" title="Open-CyKG Framework">


</p>



### Datasets

* OIE dataset: [Malware DB](https://justhalf.github.io/publication/2017-07-01-malwaretextdb) 
* NER dataset: Microsoft Security Bulletins ([MSB](https://arxiv.org/abs/1308.4941)) and Cyber Threat Intelligence reports ([CTI](https://koreauniv.pure.elsevier.com/en/publications/automatic-extraction-of-named-entities-of-cyber-threats-using-a-d))

For dataset files please refer to the appropiate refrence in the paper.

### Code:

#### Dependencies

* Compatible with Python 3.x
* Dependencies can be installed as specified in Block 1 in the respective notebooks. 
* All the code was implemented on Google Colab using GPU. Please ensure that you are using the version as specified in the "Ïnstallion and Drives" block.
* Make sure to adapt the code based on your dataset and choice of word embeddings.
* To utlize CRF in NER model using Keras; plase make sure to:
	
	-- Use tensorFlow version and Keras version:
	
	-- In tensorflow_backend.py and Optimizer.py write down those 2 liness ---> then restart runtime
	
		```
		import tensorflow.compat.v1 as tf
		tf.disable_v2_behavior()
		```
		
**For more details on the how the exact process was carried out and the final hyper-parameters used; please refer to Open-CyKG paper.**

### Citing:
Please cite Open-CyKG if you use any of this material in your work.

`I. Sarhan and M. Spruit, Open-CyKG: An Open Cyber Threat Intelligence Knowledge Graph, Knowledge-Based Systems (2021), doi: https://doi.org/10.1016/j.knosys.2021.107524.`

```bibtex

```

#### Implementation Refrences:
* Contextualized word embediings: [link to Flairs word embedding documentation](https://github.com/flairNLP/flair/blob/master/resources/docs/embeddings/TRANSFORMER_EMBEDDINGS.md), Hugging face link of all pretrained models https://huggingface.co/transformers/v2.3.0/pretrained_models.html 
* Functions in block 3&9 are originally refrenced from the work of Stanvosky et al. Please refer/cite his work, with exception of some modification in the functions `Stanovsky, Gabriel, et al. "Supervised open information extraction." Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long Papers). 2018.`
* OIE implements Bahdanau attention (https://arxiv.org/pdf/1409.0473.pdf). Towards Data Science [Blog](https://towardsdatascience.com/light-on-math-ml-attention-with-keras-dc8dbc1fad39)
* NER refrence [blog](https://medium.com/@utkarsh.kumar2407/named-entity-recognition-using-bidirectional-lstm-crf-9f4942746b3c)  
* Knowledge Graph fusion motivated by the work of CESI `Vashishth, Shikhar, Prince Jain, and Partha Talukdar. "Cesi: Canonicalizing open knowledge bases using embeddings and side information." Proceedings of the 2018 World Wide Web Conference. 2018.`.
* [Neo4J](https://neo4j.com/) was used for Knowledge Graph visualization.


*Please cite the appropriate reference(s) in your work*

