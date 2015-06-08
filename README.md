
Overview
----------------
This is a list of entailment rules that are extracted from the RTE part of the SICK dataset (http://alt.qcri.org/semeval2014/task1/). 
Logical inference + perfect predictions for these rules give near perfect score in SICK RTE. 
For more details, check our paper: *Representing Meaning with a Combination of Logical Form and Vectors*. 


Download
----------------
The releases of this dataset can be downloaded from here: https://github.com/ibeltagy/rrr/releases


Cite
----------------
If you use this dataset in your work, please cite our paper: 

    @article{beltagy:arxiv15, 
    title = {Representing Meaning with a Combination of Logical Form and Vectors}, 
    author = {Islam Beltagy and Stephen Roller and Pengxiang Cheng and Katrin Erk and Raymond J. Mooney}, 
    journal={arXiv preprint arXiv:1505.06816 [cs.CL]},
    url="http://www.cs.utexas.edu/users/ai-lab/pub-view.php?PubID=127513",
    year={2015}
    }

License
----------------
This data set is released under a Creative Commons Attribution-NonCommercial-ShareAlike 3.0 
Unported License (http://creativecommons.org/licenses/by-nc-sa/3.0/deed.en_US)


Contents
----------------
The dataset has 12,508 rules, 10,211 are unique. Rules are split into training and testing, extracted from the training and testing parts of SICK respectively. Rules have three types, Entail, Neutral and Contradict. 


Files format
----------------
Each file has the following columns: 

- ruleID: an ID

- pairIndex: ID of the RTE pair where the rule is extracted from

- annotation: rule types: 1, 0 and -1 for Entail, Neutral and Contradict

- ruleLhs: the LHS of the rule. Each word is followed with **-i** where **i** is the index of the word in the source sentence

- ruleRhs: the RHS of the rule

- text: the Text where ruleLhs is extracted from

- hypothesis: the Hypothesis where ruleRhs is extracted from


Notes and Future Work 
----------------

- Some words are dropped from the rules, like {a, an, the, is, are, and}

- Words in a rule are not necessary consecutive in the sentence, but most porbably connected syntactically

- Few rules are wrong because of parsing errors and limitations in our Robinson Resolution algorithm

- Some rules are duplicated. Few rules (around 100) are duplicated with different rule types. This is because of inconsistencies in the annotations of the SICK dataset (remember that most of the rules are automatically annotated using the gold standard annotation for the pair where the rule is extracted from). For example, the relation between "flute" and "guitar" could be Entail but in most cases it is Neutral.

- Some rules are long and they can be split into multiple shorter and simpler rules. We leave that for future releases. 
