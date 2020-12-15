# Recommendation System


Two kinds of recommendations are commonly used:
- home page recommendations: personalized to a user based on their known interests.
- related item recommendations: recommendations similar to a particular item

## Terminology

Item: entities a system recommends

Query: input to recom system. contains user information such as the user id and previously interacted items, and additional context like time of day and user's device.

## architecture

candidate generation => scoring => re-ranking


### Candidate generation

Given a query, the system generates a set of relevant candidates. 

- content-based filtering: recommend items similar to what the user likes based on similarity between items.
    - pros: 1. don't need data from other users. easier to scale to large number of users. 2. can capture specific interests of a user thus recommend niche items that very few users are interested in.
    - cons: 1. include hand-engineered features thus requires domain knowledge. 2. can only make recommendations based on existing interests of a user, has limited ability to expand.

- collaborative filtering: recommend items based on similarities between queries and items simultaneously.
    auto learn embedding matrix for both users and items. often with matrix factorization.
    - user embedding matrix U (m,d), m=number of users, d is embedding dimension.
    - item embedding matrix V (n,d), n=number of items, d is embedding dimension.
    - UV(t) is feedback matrix A

    choosing the objective function:
    - Weighted Matrix Factorization decomposes the objective into the following two sums: A sum over observed entries.A sum over unobserved entries (treated as zeroes).

    minimiazing the objective function:
    - SGD or weighted alternating least squares

    - pros: no domain knowledge necessary and can help users discover new interests. only need feedback matrix to train.

    - cons: fail to handle fresh items. an item is not seen during training, the system can't create an embedding for it and can't query the model with this item. This issue is often called the cold-start problem. hard to include side features for query

Both method map each item and each query to an embedding vector in a common embedding space. 

- DNN

    address limitations of matrix factorization (must present in training set and popular items tend to be recommended for everyone)

    -DNN treats the problem as multiclass prediction problem: input = user query, output probability vector with size equal to the bnnumber of items in the corpus.

#### Similarity Measures

- cosine: cosine of the angle between the two vectors
- dot product: the cosine of the angle multiplied by the product of norms
- Euclidean distance: the usual distance in Euclidean space

Which Similarity Measure to Choose?

Compared to the cosine, the dot product similarity is sensitive to the norm of the embedding. That is, the larger the norm of an embedding, the higher the similarity (for items with an acute angle) and the more likely the item is to be recommended. This can affect recommendations as follows:

- Items that appear very frequently in the training set (for example, popular YouTube videos) tend to have embeddings with large norms. If capturing popularity information is desirable, then you should prefer dot product. However, if you're not careful, the popular items may end up dominating the recommendations. In practice, you can use other variants of similarity measures that put less emphasis on the norm of the item. 

- Items that appear very rarely may not be updated frequently during training. Consequently, if they are initialized with a large norm, the system may recommend rare items over more relevant items. To avoid this problem, be careful about embedding initialization, and use appropriate regularization. 

#### In summary:

Matrix factorization is usually the better choice for large corpora. It is easier to scale, cheaper to query, and less prone to folding.
DNN models can better capture personalized preferences, but are harder to train and more expensive to query. DNN models are preferable to matrix factorization for scoring because DNN models can use more features to better capture relevance. Also, it is usually acceptable for DNN models to fold, since you mostly care about ranking a pre-filtered set of candidates assumed to be relevant.

### Retrieval and scoring
Once you have the query embedding q, search for item embeddings Vj that are close to q in the embedding space. This is a nearest neighbor problem. For example, you can return the top k items according to the similarity score 

large-scale retrieval: To compute the nearest neighbors in the embedding space, the system can exhaustively score every potential candidate. to make it more efficient: If the query embedding is known statically, the system can perform exhaustive scoring offline, precomputing and storing a list of the top candidates for each query. This is a common practice for related-item recommendation. or use approximate nearest neighbors.

After candidate generation, another model scores and ranks the generated candidates to select the set of items to display. The recommendation system may have multiple candidate generators that use different sources, such as the following:

- Related items from a matrix factorization model.
- User features that account for personalization.
- "Local" vs "distant" items; that is, taking geographic information into account.
- Popular or trending items.
- A social graph; that is, items liked or recommended by friends.

Choose objective function for scoring:
- max click rate
- max watch time
- increase diversity and maximize session watch time

### Re-ranking

In the final stage of a recommendation system, the system can re-rank the candidates to consider additional criteria or constraints. One re-ranking approach is to use filters that remove some candidates. We can train a separate model to detect click-bai videos and remove them from the candidate pool, or add manual features such as promotions in.

Things to consider:
- Freshness: rerun new models with warm-starting, create average user to represent new users
- Diversity: include multiple candidate generators using different sources, re-rank items based on other metadata to ensure diversity.
- Fairness: model should treat all users fairly. try to eliminate bias when training.


