Convert winobias dataset to conll format

*Based on Berkeley Coref system*

python toSentences.py data/winobias.txt wino_sentences/

Run Berkeleycoref preprocessh script
e.g sh scripts/preprocess.sh wino_sentences/ data/wino_preprocess/

python addCoref.py data/winobias.txt data/wino_preprocess/ wino_berkeley/

python toWino.py wino_berkeley/ wino_conll/
