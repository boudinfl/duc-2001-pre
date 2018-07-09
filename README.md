# Preprocessed DUC 2001 keyphrase extraction benchmark dataset

This dataset was introduced in:

 - **Single Document Keyphrase Extraction Using Neighborhood Knowledge.**
   Xiaojun Wan and Jianguo Xiao.
   *In Proceedings of AAAI 2008.*
   pp. 855-860.

The dataset is split into three directories:

  * `references`: reference keyphrases for evaluation
  * `test`: test set
  * `src`: scripts and archive from which the dataset is built

Each input file is processed using the Stanford CoreNLP suite v3.6.0.
We use the default parameters and perform tokenization, sentence splitting and
Part-Of-Speech (POS) tagging. Files are in XML format.

Reference keyphrases are in json format and named according to the following
rules:

    test.reader.[stem]?.json

reader-provided (stemmed or not) reference keyphrases for test.

Stemming (if applied), is performed with nltk Porter algorithm (English).

Below is a toy example of reference file:

    {
        "doc-1": [
            [
                "target detect"
            ],
            [
                "number of sensor",
                "sensor number"
            ]
        ],
        ...
    }