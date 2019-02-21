Convert winobias dataset to conll format

*Based on Berkeley Coref system*

python toSentences.py data/anti_stereotyped_type1.txt.dev wino_sentences/

Run Berkeleycoref preprocessh script
(*refer to "preprocessing" section [here](http://nlp.cs.berkeley.edu/downloads/berkeleycoref-readme.txt)*)

python addCoref.py data/winobias.txt data/wino_preprocess/ wino_berkeley/

python toWino.py wino_berkeley/ wino_conll/
