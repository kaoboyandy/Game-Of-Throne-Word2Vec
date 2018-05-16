
# Word2Vec with Game of Throne

## Can we represent the 5 Game of Thrones books with word vectors reflecting the relationship between various words and characters?

## Outline
#### 1. Generating Word Embedding with IMDB movie comment using Keras
We'll use the imdb dataset to create word embeddings. This dataset contains 25,000 movie reviews from IMDB, labeled with sentiment (positive or negative). For convenience, the words are indexed by their frequency in the dataset, meaning the for that has index 1 is the most frequent word. We will only use the first 20 words from each review to speed up training, use a max vocab size of 10,000.

#### 2. Game of Thrones Word2Vec with Gensim
We'll input all 5 books of Game of Throne and output the word vector, this time using Gensim.

#### 3. Visualisation with T-SNE using Bokeh
We will map the multi-dimension vector down to 2 dimension using a technique called T-SNE. We will then visualize them using Bokeh. You will likely find words that are more related closer to each other closer. See example below.


### What is Word2Vec

Word2vec is a group of related models that are used to produce word embeddings. These models are neural networks that are trained to reconstruct linguistic contexts of words. Word2vec takes as its input a large corpus of text and produces a vector space, typically of several hundred dimensions, with each unique word in the corpus being assigned a corresponding vector in the space. Word vectors are positioned in the vector space such that words that share common contexts in the corpus are located in close proximity to one another in the space.

### Game of Thrones Examples

A simple formula of __"king" + "He" - "She"__ gives us the following

[('cersei', 0.6207334995269775), <br>
 ('queen', 0.6201149225234985),<br>
 ('sansa', 0.5549461841583252),<br>
 ('catelyn', 0.535677969455719), <br>
 ('dany', 0.5277178287506104),<br>
 ('margaery', 0.5257571339607239),<br>
 ('joffrey', 0.4984680414199829),<br>
 ('daenerys', 0.4920499324798584),<br>
 ('viserys', 0.4814302921295166),<br>
 ('arya', 0.4803134799003601)]<br>

### A cluster of word embeddings

![image.png](attachment:image.png)

### Another cluster of embeddings

![image.png](attachment:image.png)

### And another one on various locations

![image.png](attachment:image.png)
