# MED: Monotonicity Entailment Dataset (Ver.1.0)

## Overview
MED is a new evaluation dataset that covers a wide range of monotonicity reasoning that was created by crowdsourcing and collected from linguistics publications.
Compared with manual or automatic construction like [HELP](https://github.com/verypluming/HELP), we collected naturally-occurring examples by crowdsourcing and well-designed ones from linguistics publications.

## Data
The file ``MED.tsv`` is formatted similarly to the MNLI release, so if your system is trained on MNLI you may be able to feed this file directly into your system. Otherwise, you may need to reformat the data to fit your system's input format. 

The fields in this file are:
- ``gold_label``: The correct label for this sentence pair (either ``entailment`` or ``neutral``)
- ``sentence1``: The premise
- ``sentence2``: The hypothesis
- ``pairID``: A unique identifier for this sentence pair
- ``genre``: Multiple annotation tags joined by a colon. The tags are: 
 - (i) the type of the example (``crowd``: naturally-occuring inferences collected through crowdsourcing, or ``paper``: well-designed ones collected from previous NLI datasets and linguistics publications)
 - (ii) the type of monotonicity reasoning (``upward_monotone``, ``downward_monotone``, and ``non_monotone``) 
 - (iii) the linguistic phenomena related to monotonicity reasoning (``lexical_knowledge``, ``reverse``, ``conjunction``, ``disjunction``, ``conditionals``, and ``npi``)
 - (iv) original NLI datasets (optional)

## Citation
If you use this dataset in any published research, please cite the following:
* Hitomi Yanaka, Koji Mineshima, Daisuke Bekki, Kentaro Inui, Satoshi Sekine, Lasha Abzianidze, and Johan Bos. [Can neural networks understand monotonicity reasoning?](https://www.aclweb.org/anthology/W19-4804) Proceedings of ACL2019 Workshop BlackboxNLP: Analyzing and interpreting neural networks for NLP, Florence, Italy, 2019. [arXiv](https://arxiv.org/pdf/1906.06448.pdf)

```
@inproceedings{yanaka-etal-2019-neural,
    title = "Can Neural Networks Understand Monotonicity Reasoning?",
    author = "Yanaka, Hitomi  and
      Mineshima, Koji  and
      Bekki, Daisuke  and
      Inui, Kentaro  and
      Sekine, Satoshi  and
      Abzianidze, Lasha  and
      Bos, Johan",
    booktitle = "Proceedings of the 2019 ACL Workshop BlackboxNLP: Analyzing and Interpreting Neural Networks for NLP",
    year = "2019",
    pages = "31--40",
    }
```

A part of the MED dataset comes from [the FraCaS test suite (Generalized Quantifier section)](https://nlp.stanford.edu/~wcmac/downloads/fracas.xml) and [the GLUE diagnostic set](https://gluebenchmark.com/diagnostics).

## Contact
For questions and usage issues, please contact hitomi.yanaka@riken.jp .

## License
Apache License

## Acknowledgement
This work is conducted in collaboration with RIKEN AIP, Ochanomizu University, and University of Groningen.

## Disclaimer
A part of the MED dataset is collected from the published works referred to in our paper, and copyright (where applicable) remains with the original authors or publishers.
