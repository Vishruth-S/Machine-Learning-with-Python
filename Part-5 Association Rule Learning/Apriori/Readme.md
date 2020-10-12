Association Rule Learning: Association rule learning is a machine learning method that uses a set of rules to discover interesting relations between variables in large databases i.e. the transaction database of a store. It identifies frequent associations among variables called association rules that consists of an antecedent  (if) and a consequent (then).



For example, if a person buys a burger, then there is a chance that he will buy some french fries too. This is because there is some relationship between french fries and burger (they are often taken together).



The task of associations rule learning is to discover this kind of relationships and identify the rules of their association.



Association rule learning algorithms are used extensively in data mining for market basket analysis, which is determining dependencies among various products purchased by the customers at different times analyzing the customer transaction databases.



There are two basic types of Association learning algorithms- Apriori and Eclat. In this article, we are going to implement the Apriori algorithm.





Apriori Intuition: This is a classic algorithm in data mining. It is used for analyzing frequent itemsets and relevant association rules. It can operate on databases containing a lot of transactions.
