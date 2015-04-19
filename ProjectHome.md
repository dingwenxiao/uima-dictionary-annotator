UIMA AE which recognizes CSV dictionary entries stored as a prefix tree in any annotation feature path

**Overview**

The UIMA dictionary annotator aims at **recognizing in an annotation feature path text entries defined in CSV dictionaries**.
The dictionary can be declared as a resource or locally via a parameter.
It is stored in memory as a **prefix tree** to parse it quickly.
The **columns of the CSV dictionary can be associated on fly to a feature structure** either independently to feature of a specified annotation or as a whole for a string array annotation feature.
Depending on your objective you can specify constraints such as an **exact match** with a feature path value (3) (instead of a **substring match** (4)) or **annotating the annotation** of the specified feature path (1) (instead of **the occurrence itself** of the dictionary entry (2)).

These constraints allow to search and annotate text forms defined as dictionary entries within the uima.tcas.DocumentAnnotation:coveredText (case 2 and 4); as well as searching the token annotations for some exact forms (3 and 1) ; as well as search the lemmas of token annotations for exact or substring forms ((3 or 4) and 1).


**Where to start ?**

Check the various parameters and resource declarations of the [desc/dictionaryAnnotator/dictionaryAnnotatorAE.xml descriptor](https://code.google.com/p/uima-dictionary-annotator/source/browse/trunk/desc/dictionaryAnnotator/dictionaryAnnotatorAE.xml).