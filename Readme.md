Convert winobias dataset from .txt format to .conll format

*Based on Berkeley Coref system* (please check [their website](http://nlp.cs.berkeley.edu/projects/coref.shtml) for more info)

1. extract the senteces from winobias.txt (in our case, _winobias.txt_ means "anti_stereotyped_type1.txt.dev" etc.)
```
mkdir wino_sentences
python toSentences.py data/anti_stereotyped_type1.txt.dev wino_sentences/ 
```

2. Run Berkeleycoref preprocessh script
(*refer to "preprocessing" section [here](http://nlp.cs.berkeley.edu/downloads/berkeleycoref-readme.txt)*)

3. Add all the side info obtained by Berkeleycoref to our data: 
``` 
mkdir wino_berkeley
python addCoref.py data/winobias.txt data/wino_preprocess/ wino_berkeley/
```

4. 
```
mkdir wino_conll
python toWino.py wino_berkeley/ wino_conll/
```
