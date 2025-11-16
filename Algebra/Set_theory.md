
there is a difference between $\in$ and  $\subset$ 
we talk about inclusion when we talk about an element in a set 
we talk about subsets when a set is in another set 

A$\subset$E :
lets say that we have the set E={1,2,3,4,5}
let A ={1,2} a subset of E  
we say that A is a subset of E if all the elements in A are included in E 
thus :
$$\forall x \in A => x\in B$$

### Complimentary of a set (Negation) 
Let A and B two sets in E 
where B includes all the elements in E that are not in A 
we note :B = $\bar{A} ,\space C(A)\space , C^E_A$ 
for example E = {1,2,3,4,5}
A ={1,2}
then B= {3,4,5}
thus: $$\begin{array}{1} \forall x \in A <=> x\notin C^E_A \\

\forall x \in \bar{A} <=> x \notin A 

\end{array}$$
for example if you are told to show that if A$\subset$B
then $\bar{B}\subset\bar{A}$ 
$$\begin{array}{1}
\forall x\in\bar{B} =>
x\notin B =>x\notin A => x \in \bar{A}


\end{array}$$
## Union 
$A\cup B$ the union of two sets is a set that includes all the elements in both sets
$$
\begin{array}{1}
x\in A\cup B <=> x\in A or x\in B


\end{array}
$$
(in an exercise we you have AuB A  and prove then use B  
but when yo only have one you can say since its in A then its in AuB
)
the cardinal of a set is the number of items included in that set let say $A = \{1, 2, 3,4 \}$ 
we say the cardinal of the set A is 4 and we note :
$|A| = 4$

### Intersection 
A$\cap$B is a set that contains all the common elements between A and B $$A\cap B <=> x \in A\space and\space x\in B$$         
### subtraction 
A\B , A-B which is the set that contains the elements of A but not the ones where A and B intersect 
$$x \in A -B <=> x \in A\space and \space x\notin \space B $$
### symmetric difference 
A$\Delta$B : which is the set that includes all the elements in A and B except the ones that are in both at the same time so  $$x \in A\Delta B <=> x \in A\cup B - A\cap B $$
or : $$B\space \not \space A \space \cup \space and \space A \space \not \space B  $$
\
### Power Set 
the power set is a set  that represents the collection of partitions of the set E

==example:== we have a set A = {1,2,3}
P(A) ={{$\emptyset$},{1},{2},{3},{1,2}, {1,3} ,{2,3},{1,2,3}}

generally the cardinal of the power set is 2 to the power of the cardinal of A  of the cardinal of the set it self so : 
$|p(A)| = $2^{|A|}$

in the example above we can say that {1,2} is included in P(A)
and we write : {1,2}$\in$ P(B)
but the set B={{1,2},{2,3}} is a subset of P(A)
B$\subset$P(A)

### The Partition of a set

let A the set of even numbers and B the set of odd numbers 
the union of the sets A$\cup$B  represents N 
and A$\cap$B = $\emptyset$ 
and  A and B  are not empty 
SO we can a partition of a set if these conditions are met : 
$$
\begin{cases}
A_i \neq \varnothing & \text{for every } i \\[6pt]
A_i \cap A_j = \varnothing & \text{if } i \neq j \\[6pt]
A_1 \cup A_2 \cup \cdots \cup A_n = A
\end{cases}
$$

 