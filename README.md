# Cebuano Natural Language Toolkit Beta version 1.1

* This toolkit is still in its beta version and is still undergoing further testings 

## In this README :point_down:

- [Sample Usage](#sample-usage)
  - [Initial setup](#initial-setup)
- [Modules](#sample-usage)
  - [Cebuano corpus](#cebuano-corpus)
  - [Preprocessing](#preprocessing)
  - [Vocabulary](#vocabulary)
  - [POS TAGGER MODEL](#pos-tagger-model)
  - [NER TAGGER MODEL](#ner-tagger-model)
  - [POS NER tags](#pos-ner-tags)
  - [POS test](#pos-test)
  - [NER test](#ner-test)
    
    

## Sample Usage

### Initial setup

1. [Create a new Google Colab notebook](https://colab.research.google.com) from this link create with the desired name of your notebook.

    *any project name but do not change the file type .ipynb*

    ```
    python 3.10.8 
    ```

2. Install necessary libraries.

    *Google colab is very flexible in installing libraries with older versions*

    ```
    !pip install tensorflow==2.2 
    !pip install keras==2.3.1
    !pip install plot-keras-history
    !pip install git+https://www.github.com/keras-team/keras-contrib.git
    !pip install tensorflow_addons
    !pip install keras-self-attention
    !pip install attention
    !pip install nltk
    ```

    *or you could just do*
    ```
    !pip install git+https://www.github.com/keras-team/keras-contrib.git
    !pip install keras-self-attention
    !pip install attention
    ```
    *Then you are ready to install CNLTK latest version*

2. Install CNLTK library.

    *Google colab is very flexible in installing libraries with older versions*

    ```
    pip install CNLTK-Beta-version==1.1.0
    ```

## Modules

### Cebuano corpus

*access the annotated corpus used for training the model*

```
from CNLTK import ceb_corpus

your_variable = ceb_corpus.cebuano_corpus()
```

#### Preprocessing

*access the preprocessing modules used for the dataset*

```
from CNLTK import preprocessing

your_variable = preprocessing._POS(your_sentence)
your_variable = preprocessing._NER(your_sentence)
```


#### Vocabulary

*access the indexed vocabulary from the corpus*

```
from CNLTK import vocabulary

your_variable = vocabulary.get_VOCAB_model()
```


#### POS TAGGER MODEL

*access the trained model for POS Tagger*

```
from CNLTK import POS_TAGGER_MODEL

your_variable = POS_TAGGER_MODEL.get_POS_TAGGER_model()
```

#### NER TAGGER MODEL

*access the trained model for NER Tagger*

```
from CNLTK import NER_TAGGER_MODEL

your_variable = NER_TAGGER_MODEL.get_NER_TAGGER_model()
```

#### POS NER tags

*access the indexed annotated tags for POS and NER*

```
from CNLTK import POS_NER_tags

your_variable = POS_NER_tags.get_POS_TAGS()
your_variable = POS_NER_tags.get_NER_TAGS()
```


#### POS test

*Test how the trained model tags sample input sentences*
*This module will return two variable the preprocessed sentence & predicted tags*

```
from CNLTK import POS_test

sentence_variable, tag_variable = POS_test.predict_POS_model()
```

#### NER test

*Test how the trained model tags sample input sentences*
*This module will return two variable the preprocessed sentence & predicted tags*

```
from CNLTK import NER_test

sentence_variable, tag_variable = NER_test.predict_NER_model()
```

## FAQ

#### Can i reuse the model for another corpus?

Unfortunately the CNLTK library is still in its beta version and is still undergoing further testings and improvements.
