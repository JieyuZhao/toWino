Convert winobias dataset to conll format

*Based on Berkeley Coref system*

1. python toSentences.py data/anti_stereotyped_type1.txt.dev wino_sentences/

2. Run Berkeleycoref preprocessh script
(*refer to "preprocessing" section [here](http://nlp.cs.berkeley.edu/downloads/berkeleycoref-readme.txt)*)

3. python addCoref.py data/winobias.txt data/wino_preprocess/ wino_berkeley/

4. python toWino.py wino_berkeley/ wino_conll/
