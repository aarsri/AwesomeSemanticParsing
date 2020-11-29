# AWESOME Bibliography: Semantic Parsing

Papers and Resources for Semantic Parsing in NLP

Aarohi Srivastava


## Datasets
-	[ATIS (1990)](https://www.kaggle.com/siddhadev/atis-dataset-from-ms-cntk/)
-	[Geoquery (1996)](https://www.cs.utexas.edu/users/ml/geo.html/)
-	[WebQuestions (2013)](https://worksheets.codalab.org/worksheets/0xba659fe363cb46e7a505c5b6a774dc8a/)
-	[Free917 (2013)](https://www.aclweb.org/anthology/P13-1042.pdf)
-	[Overnight (2015)](https://worksheets.codalab.org/worksheets/0x269ef752f8c344a28383240f7bb2be9c/)
-	[WikiSQL (2017)](https://github.com/salesforce/WikiSQL/)
-	[Spider (2018)](https://yale-lily.github.io/spider/)


## Survey of Semantic Parsing

[**Learning to Parse Database Queries Using Inductive Logic Programming**](https://www.cs.utexas.edu/~ml/papers/chill-aaai-96.pdf)

In this seminal paper, Zelle & Mooney (1996) adapt their CHILL parser (Zelle & Mooney, 1993) to the task of natural language querying on a database.  They develop the famous Geoquery corpus of 880 question-answer pairs expressed in the Prolog programming format.


[**Grounded Unsupervised Semantic Parsing**](https://www.aclweb.org/anthology/P13-1092.pdf)

Poon (2013) conceives the first unsupervised method of semantic parsing that performs competively well compared to supervised semantic parsers. Their model annotates a dependency tree with latent states and learns a probabilistic grammar, making use of the knowledge-base for indirect supervision. 


[**Compositional Semantic Parsing on Semi-Structured Tables**](https://ppasupat.github.io/WikiTableQuestions/)

Pasupat & Liang (2015) devise a parsing algorithm guided by semantic type constraints to answer questions about semi-structured tables.


[**Data Recombination for Neural Semantic Parsing**](https://www.aclweb.org/anthology/P16-1002.pdf)

Jia & Liang (2016) introduce a novel framework of data recombination to inject task- or domain- specific knowledge into a semantic parsing model.  They develop a seq2seq RNN and find an improvement in semantic parsing performance when employing data recombination.


[**Transforming Dependency Structures to Logical Forms for Semantic Parsing**](https://www.aclweb.org/anthology/Q16-1010/)

Reddy et al. (2016) design DepLambda to map from natural language to an ungrounded lambda calculus logical representation using the dependency parse of the sentence.  In addition, they implement an algorithm to ground the logical reprentation of the sentence in a knowledge base.


[**Universal Semantic Parsing**](https://www.aclweb.org/anthology/D17-1009.pdf)

Reddy et al. (2017) create UDepLambda, a semantic interface for Universal Dependencies that maps natural language to logical forms and processes dependency graphs.


[**TRANX: A Transition-based Neural Abstract Syntax Parser for Semantic
Parsing and Code Generation**](https://github.com/pcyin/tranX/)

Yin et al. (2018) develop an abstract syntax parser that can map natural language queries to machine-executable code and logical form.  Their model generalizes well and adapts to new meaning representations.


## Cross-Domain Semantic Parsing

**Language to Logical Form with Neural Attention** [[paper](https://www.aclweb.org/anthology/P16-1004.pdf)] [[code](https://github.com/donglixp/lang2logic)]

Dong & Lapata (2016) construct an encoder-decoder model with attention that generates logical forms.  Their model is easy to adapt across domains and meaning representations.


**Decoupling Structure and Lexicon for Zero-Shot Semantic Parsing** [[paper](https://www.aclweb.org/anthology/D18-1190/)] [[code](https://github.com/jonathanherzig/zero-shot-semantic-parsing)]

Herzig & Berant (2018) devise a method of zero-shot learning for semantic parsing in which they first map an utterance to an abstract logical form with slots (resembling lambda calculus) before replacing the slots with knowledge-base constants.


**Coarse-to-Fine Decoding for Neural Semantic Parsing** [[paper](https://www.aclweb.org/anthology/P18-1068.pdf)]

Dong & Lapata (2018) design a structure-aware neural architecture in which they first generate a rough sketch of the meaning of an input sequence and later fill in missing details.


**Zero-Shot Semantic Parsing for Instructions** [[paper](https://www.aclweb.org/anthology/P19-1438.pdf)] [[code](https://github.com/givoli/TechnionNLI/)]

Givoli & Reichart (2019) implement a semantic parser that takes instructions as inputs and outputs the corresponding compositional logical form. They obtain good performance even in domains not seen during training.


**Semantic Parsing with Dual Learning** [[paper](https://arxiv.org/abs/1907.05343/)] [[code](https://github.com/rhythmcao/semantic-parsing-dual)]

Cao et al. (2019) illustrate a method of dual learning for semantic parsing in which two models, one mapping from query to logical form, and the other mapping from logical form to query, regularize each other and provide feedback symbols of prior-knowledge. This way, the model can be trained in a semi-supervised setting utilizing unlabeled data. 


**Bootstrapping a Crosslingual Semantic Parser** [[paper](https://arxiv.org/abs/2004.02585)]

Sherborne, Xu, and Lapata (2020) bootstrap a transformer-based parser with various techniques, including paraphrasing, machine translation, and multilingual-BERT, in order to do semantic parsing on unseen domains and languages.


**Exploring Unexplored Generalization Challenges for Cross-Database Semantic Parsing** [[paper](https://www.aclweb.org/anthology/2020.acl-main.742.pdf)] [[code](https://github.com/google-research/language/tree/master/language/xsp/)]

In formulating their own cross-domain semantic parser, Suhr et al. 2020 identify three key challenges faced by contemporary, SOTA semantic parsers when tested on unseen domains: 1) linguistic variation across domains, 2) differing database and query structures, and 3) dataset conventions.


## Semantic Parsing with TAG and CCG

-	Synchronous Tree-Adjoining Grammars (Shieber & Schabes, 1991) [[paper](https://pdfs.semanticscholar.org/8d1d/72ad7b26824b9036be5e95f4eecb6425b77a.pdf)]
-	Pied-piping in Relative Clauses: Syntax and Compositional Semantics using Synchronous Tree Adjoining Grammar (Han, 2007) [[paper](https://www.aclweb.org/anthology/W06-1506.pdf)]
-	Online Learning of Relaxed CCG Grammars for Parsing to Logical Form (Zettlemoyer & Collins, 2007) [[paper](https://www.aclweb.org/anthology/D07-1071.pdf)]
-	Inducing Probabilistic CCG Grammars from Logical Form with Higher-Order Unification (Kwiatkowski et al., 2010) [[paper](https://www.aclweb.org/anthology/D10-1119.pdf)]
-	Lexical Generalization in CCG Grammar Induction for Semantic Parsing (Kwiatkowski et al., 2011) [[paper](https://www.aclweb.org/anthology/D11-1140.pdf)]
-	Learning to Map Sentences to Logical Form: Structured Classification with Probabilistic Categorial Grammars (Zettlemoyer & Collins, 2012) [[paper](https://arxiv.org/abs/1207.1420)]
-	Scaling Semantic Parsers with On-the-fly Ontology Matching (Kwiatkowski et al., 2013) [[paper](https://www.aclweb.org/anthology/D13-1161.pdf)]
-	ccg2lambda: A Compositional Semantics System (Gomez et al., 2016) [[paper](https://www.aclweb.org/anthology/P16-4015.pdf)] [[code](https://github.com/mynlp/ccg2lambda/)]
-	Reflexives and Reciprocals in Synchronous Tree Adjoining Grammar (Aggazzotti & Shieber, 2017) [[paper](https://www.aclweb.org/anthology/W17-6204.pdf)]
-	A CCG-based Compositional Semantics and Inference System for Comparatives (Haruta et al., 2019) [[paper](https://arxiv.org/abs/1910.00930/)] [[code](https://github.com/izumi-h/fracas-comparatives_adjectives)]
-	Cross-lingual CCG Induction (Evang, 2019) [[paper](https://www.aclweb.org/anthology/N19-1160.pdf)] [[code](https://github.com/texttheater/xlci/)]


## Semantic Parsing PhD Theses and Dissertations

-	[Learning for Semantic Parsing and Natural Language Generation Using Statistical Machine Translation Techniques (Wong, 2007)](https://www.cs.utexas.edu/users/ml/papers/john-dissertation.pdf)
-	[Cross-Lingual Semantic Parsing with Categorial Grammars (Evang, 2016)](https://kilian.evang.name/phdthesis.pdf)
-	[Learning Natural Language Interfaces with Neural Models (Dong, 2018)](https://era.ed.ac.uk/bitstream/handle/1842/35587/Dong2019.pdf?sequence=1&isAllowed=y)
-	[The Lifecycle of Neural Semantic Parsing (Cheng, 2019)](https://era.ed.ac.uk/bitstream/handle/1842/35554/Cheng2019.pdf?sequence=1&isAllowed=y)


## Additional Resources

-	Semantics for Semantic Parsing [[slides](https://yoavartzi.com/sp14/slides/steedman.sp14.pdf)]
-	Theories of Semantic Representation [[slides](https://www.clsp.jhu.edu/wp-content/uploads/2018/06/2018-06-21-Ellie-Pavlick-JSALT-Summer-School.pdf)]
-	SQL-Based Semantic Parsing [[website](https://medium.com/@tao.yu/awesome-sequence-to-sql-and-semantic-parsing-1d7656861679/)]
-	AllenAI Semantic Parsing Tutorial (ACL 2018) [[website](https://github.com/allenai/acl2018-semantic-parsing-tutorial)]
-	SEMPRE [[website](https://nlp.stanford.edu/software/sempre/)]
-	NLP Progress for Semantic Parsing [[website](https://nlpprogress.com/english/semantic_parsing.html/)]
