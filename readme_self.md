#### 1. Get similar words for the words out of vocabulary:
```python
from gensim.models import FastText as fText
'''
 There are two files in directory "/home/jack/dev1.8t/models/vecs/":
      
      zhwiki15-100_200dim.vec
      zhwiki15-100_200dim.bin
'''
fastText_wv = fText.load_fasttext_format("/home/jack/dev1.8t/models/vecs/zhwiki15-100_200dim") 
fastText_wv.wv.most_similar("哈哈国")
```

#### 2. Get similar words for the words within vocabulary for normal usage:
```python
from gensim.models.keyedvectors import KeyedVectors
zh_vec_model = KeyedVectors.load_word2vec_format('/home/jack/dev1.8t/models/vecs/zhwiki15-100_200dim.vec',binary=False)
zh_vec_model.most_similar("相似")
```
