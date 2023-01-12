# 01/09/2023
## set
* set is collection of objects
* check for containment
* $1 \in \{ 1, 2, 3\}$

### empty set
* write it as $\{\}$ or $\emptyset$
* $\subset$ = subset symbol
* $\{1, 2\} \subseteq \{1, 2, 3\}$
* $\{1, 4\} \nsubseteq \{1, 2, 3\}$

### iff
* $A = B$ iff $A \subseteq B$ and $B \subseteq A$

# 01/10/2023
### pop quiz
1. 6
2. 8
3. 6

### power set
* if $A = \{1, 2, 3\}$, power set is $\{\{\}, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\}\}$
* question: power set of $\{a, b\}$
	* $\{\{\}, \{a\}, \{b\}, \{a, b\}\}$
* POwer set of $A$ is $P(A)$

### cardinality
* number of elements in set
* only makes sense if elements if finite
* $A = \{2, 4, 5, 7\}, |A| = 4$ 
* if $A$ is finite, $|P(A)| = 2^{|A|}$

# 01/11/2023
### combining sets
* *union*: $A = \{1, 2, 6\}$, $B = \{1, 4, 7\}$, $A \cup B = \{1, 2, 4, 6, 7\}$
* *intersection*: $A = \{1, 2, 6\}$, $B = \{1, 4, 7\}$, $A \cap B = \{1\}$
* *disjoint*: no elements in common
* *set difference*: $A = \{1, 2, 5, 7, 8\}$, $B = \{1, 2, 3\}$
	* $A - B = \{5, 7, 8\}$
	* $= \{A \in B \mid A \notin B\}$
	 
###  Venn Diagrams
* ![[Venn Diagrams 2023-01-11 09.51.04.excalidraw]]

### Iterators
```cpp
cout << *iter;
iter++;
while (iter != list_set.end())
{
	cout << *iter;
	iter++;
}
```