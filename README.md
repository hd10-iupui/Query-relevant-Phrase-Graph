# Query-relevant-Phrase-Graph
A query-relevant phrase graph generation model to reveal phrases relevancy and associations within the medical literature. Our method is robust to reveal hidden and important associations between medical terms. This query-relevant phrase graph can assist users in identifying the relevant content efficiently and effectively.

We investigate a BERT-based unsupervised information extraction model to extract noun phrases from the corpus. Then, we develop analgorithm to construct the phrase graph to help users visualize the associations between the various medicalterms in the search corpus and retrieve the supporting content in the documents. 

Our unsupervised information extraction model can also handle keyphrase extraction task by ranking the candidates scores. We evaluate the keyphrases extraction on a PubMed data set. There are 500 documents in this data set. The average length of the documents by words is 3888. Each document has a set of phrases as the ground truth keyphrases. Many ground truth keyphrases, however, do not exist in the corresponding original documents. The entire data set has 7120 keyphrases, and only 2891 of them can be accurately found in the corresponding original documents.
Considering our keyphrase extraction task, we excluded those keyphrases that could not be found.
In order to retain as many keyphrases as possible, we took the following two steps. First, after our investigation, some original keyphrases contained multiple similar but independent noun phrases, and we divided these into separate keyphrases. Second, since words have singular, plural and tense changes, if a keyphrase itself or its stemmed form can be found in the original document, we will keep it.
We retained 3587 keyphrases, of which 1-gram keyphrases accounted for 70.09%, 2-gram accounted for 24.76%, 3-gram accounted for 4.83%, and >3-gram accounted for 0.32%.

We released this keyphrase-cleaned data set on GitHub.
