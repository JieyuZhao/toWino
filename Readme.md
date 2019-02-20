Convert winobias dataset to conll format

*Based on Berkeley Coref system*
python2 toSentences.py data/winobias.txt wino_sentences/

Run Berkeleycoref preprocessh script
e.g sh scripts/preprocess.sh wino_sentences/ data/wino_preprocess/

python2 addCoref.py data/winobias.txt data/wino_preprocess/ wino_berkeley/

python2 toWino.py wino_berkeley/ wino_conll/
