# N-Gram Language Model
Modification of Python implementation of an N-gram language model with Laplace smoothing from [joshualoehr](https://github.com/joshualoehr/ngram-language-model/blob/master/preprocess.py) repository. 


Example output for a trigram model trained on classic Indonesian literature, Siti Nurbaya, as attached in `data/train.txt` and `data/test.txt`:
```
Vocabulary size: 5659
Generating sentences...
<s> <s>  Tetapi apa hendak dikata? Karena sekaliannya itu sekadar nama saja </s> (0.01265)
<s> <s> "  kata Nurbaya pula sambil </s> (0.02585)
<s> <s> , tak ada yang dapat dikailnya pada malam hari di sana, tiada terganggu oleh lalu-lintas </s> (0.00825)
<s> <s> yang pandai, gurunya telah </s> (0.03120)
<s> <s> di atas dunia ini tiada dapat lagi kita  *) Memberi uang tatkala kawin **) Ilmu supaya dikasihi atau </s> (0.00692)
<s> <s> tengah taman ini adalah sebuah rumah kayu, bercat putih dan celana pendek hitam, yang </s> (0.00913)
<s> <s> *) Tetapi bagi mereka yang tiada hendak menurut saja aturan baru ini </s> (0.00994)
<s> <s> rumah perhentian yang ada di sini, sebab aku amat lelah rasanya dan hari </s> (0.00999)
<s> <s> ini dimasukkannya beberapa butir berlian yang </s> (0.02068)
<s> <s> kepadamu </s> (0.11609)
Model perplexity: 132.334
```

```
Loading 4-gram model...
Vocabulary size: 5659
Generating sentences...
<s> <s> <s>  Tetapi apa hendak dikata? Karena sekaliannya itu telah takdir daripada </s> (0.01397)
<s> <s> <s> "  kata Samsu pula </s> (0.03083)
<s> <s> <s> , tak ada orang yang tahu akan perjalanan kita ini, sebab kalau </s> (0.01077)
<s> <s> <s> yang pandai, tentang kekuatannya </s> (0.03120)
<s> <s> <s> di atas bendinya, </s> (0.04080)
<s> <s> <s> tengah taman ini adalah sebuah pangkalan, yang menganjur sampai ke tepi laut kota Padang </s> (0.00834)
<s> <s> <s> *) Tetapi bagi mereka yang berkasih-kasihan tempat itu, pada waktu terang bulan, adalah sebagai dengan sengaja diperbuatnya </s> (0.00696)
<s> <s> <s> rumah perhentian ini, sambil berkata, "Marilah ikut aku, nanti kuberi tempat yang baik dan mengatur </s> (0.00839)
<s> <s> <s> ini dimasukkannya beberapa butir ke dalam sekerat kue </s> (0.01556)
<s> <s> <s> kepadamu </s> (0.11609)
Model perplexity: 276.102
```

---

Usage info:
```
usage: N-gram Language Model [-h] --data DATA --n N [--laplace LAPLACE] [--num NUM]

optional arguments:
  -h, --help         show this help message and exit
  --data DATA        Location of the data directory containing train.txt and test.txt
  --n N              Order of N-gram model to create (i.e. 1 for unigram, 2 for bigram, etc.)
  --laplace LAPLACE  Lambda parameter for Laplace smoothing (default is 0.01 -- use 1 for add-1 smoothing)
  --num NUM          Number of sentences to generate (default 10)
```
