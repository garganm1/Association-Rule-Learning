# Association-Rule-Learning

Association Rule is meant to uncover associations between items in a set of transactions (ex. a grocery/retail store)

Consider a retail store which has products ranging from grocery items, household items and several other products to sell. It has employed a market analyst who is given the task to improve sales. 

One of the strategies that the market analyst can use is Association rule learning. This can tell the analyst that which products are related to each other. By finding this out, the related products (such as eggs, bread, milk, cereal) can be placed in proximity to each other or use promotional pricing to attract more customers without sacrificing much revenue.

Essentially, association rule discovers interesting relations between items in large databases containing transactions of items as 'datapoints'. The measure of relation is jointly given by Support, Confidence and Lift.

1. Support - tells how frequent an item appears in all transactions
2. Confidence - tells measure of transactions where the related items appear together
3. Lift - indicates whether there is an actual relationship between items or the items appear together randomly

Several algortihms have been devised for ML to find these related items. One of the algorithm is the "Apriori Algorithm". In this, the analyst fixes a minimum support (minsup) and confidence (minconf) value. For n unique items, there is a possibility of (2^^n - 1) combinations. 

But, with apriori algorithm and the user-defined minimum values of support and confidence, subsets of frequent itemset are considered and supersets of infrequent itemsets are eliminated from algorithm process.

With these two steps, we have identified a set of association rules which satisfy both the minimum support and minimum confidence condition. The number of such rules obtained will vary with the values of minsup and minconf. Now, this subset of rules thus generated can be searched for highest values of lift to make business/market decisions.

Here is the full process summary - 

- Association rule mining: (a) Itemset generation, (b) Rule generation
- Apriori principle: All subsets of a frequent itemset must also be frequent & All supersets of infrequent itemset must also be infrequent
- Apriori algorithm: Pruning to efficiently get all the frequent itemsets
