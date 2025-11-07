## types of circuits : 
there are two main types of circuits : 
- analogical circuits (electrical ): 
they have a variable amplitude which can take many values 
- digital circuits (numeric): 
they are designed to hold only too values which are 0 and 1 
this concept is the base of the boolean algebra 


## definition : 
we call boolean algebra a set E that uses two laws '.' and '+' this set respect these properties : 
- every one of these laws is associative and commutative 
- // // // // is distributive compared to the other 
- the '.' accept a unique neutral element noted $e_1$ :
 $$\forall{x} \in E , x . e_1 = x$$ - the '+'  accepts one neutral element $e_0$ :  $$\forall x \in E ,x+ e_0 = x $$
- all elements of E are idempotent for each law : 
$$\forall x \in E , x.x = x\space and \space x +x =x $$
- the complementary axioms : 
$$\forall x \in E , x . \bar{x} = e_0 and x + bar{x} = e_1 $$

## the duality principle : 
this principle allows the finding of properties that already exist : 
 ==> during the formula (axiom or theorem) already established , we can find another formula by replacing the first of the '+' law with a '. ' and inverting the neutral element from 0 to 1 

| Propriété       | Loi “+”                                     | Loi “·”                                                           |
| --------------- | ------------------------------------------- | ----------------------------------------------------------------- |
| Idempotence     | $$x + x = x$$                               | $$x \cdot x = x$$                                                 |
| Commutativité   | $$x + y = y + x$$                           | $$x \cdot y = y \cdot x$$                                         |
| Associativité   | $$x + y + z = x + (y + z) = (x + y) + z$$   | $$x \cdot y \cdot z = x \cdot (y \cdot z) = (x \cdot y) \cdot z$$ |
| Élément neutre  | $$x + 0 = x$$                               | $$x \cdot 1 = x$$                                                 |
| Distributivité  | $$x + (y \cdot z) = (x + y) \cdot (x + z)$$ | $$x \cdot (y + z) = (x \cdot y) + (x \cdot z)$$                   |
| Complémentarité | $$\overline{x} + x = 1$$                    | $$\overline{x} \cdot x = 0$$                                      |
## fundamental theorems : 
| theorem    | Loi “+”                              | Loi “·”                                      |
| ---------- | ------------------------------------ | -------------------------------------------- |
| inhibition | $$x + (\bar{x}y) = x+y$$             | $$x \cdot (\bar{x}+y) = x\cdot y$$           |
| absorption | $$x + 1 = 1$$  $$x + (x.y) = x$$     | $$x \cdot 0 = 0 \cdot 0$$ $$x.(x+y) =x$$     |
| De Morgan  | $$\overline{x+y} =\bar{x}.\bar{y} $$ | $$\overline{x \cdot y} = \bar{x} + \bar{y}$$ |
| Involution | $$\bar{\bar{x}}=x$$                  | //same thing                                 |
### proofs : 
the theorem of absorption 
$$x + 1 = 1$$
$$x+1 = x+(x+\bar{x}) = (x+x) +\bar{x} = x+\bar{x} = 1 $$
 the theorem of inhibition : 
 $$x + (\bar{x}.y) = x + y$$
 $$x+(\bar{x}.y) = (x+\bar{x}).(x+y) = 1.(x+y)= x+y$$
 $$x + (x+y) =x $$
 $$x + (x.y) = x.(y+1) = x.1=x $$

## Boolean variables : 
a boolean variable x is a mathematical element that reserves a value in the set {0,1} in reality this represents an electrical signal in an electronic system 
example : the interrupter K takes 2 states (opened and closed) thus we can describe these two states using boolean algebra (exactly the boolean variable x ) x=0 when closed and x=1 when opened  
## Boolean functions 
a boolean function is an association of a boolean variables linked using ops , it can take only two values (0,1)
Note : a boolean function can be used as a var for another function 
ex : 
f(x,y) = x +y
f(x,y) = x.y
z(x,y) = f(x,y) + g(x,y)
## Algebraic manipulation : 
in general they are written as truth tables and used to make logical circuits (which have to be expressed in an algebraic form)
the manipulation part here is about the simplification of the functions using the axioms and theorems . 
![[Pasted image 20251018212059.png]]
## Defining a boolean function : 
we can represent a boolean function using a truth table which takes all the cases for the given arguments and the output of their combinations ex![[Pasted image 20251018210321.png]]: 
![[Pasted image 20251018210321.png]]
we can also represent a boolean function using the algebraic form using the boolean ops : 
ex : $$f(x,y) = \bar{x}.y + \bar{y}.x $$
where the $\bar{x}.y\space{}and\space\bar{y}.x$ are algebraic terms 
## how to go from the algebraic form to the truth table : 
ex :
![[Pasted image 20251018211030.png]]

![[Pasted image 20251018213122.png]]

## Logical operators 
### 1. the "And" and "Or" Gates 
### **1. AND Gate**

- **Symbol:** `·` or multiplication (A · B)
    
- **Rule:** Output is **1 only if both** inputs are 1.
    
- **Explanation:** It’s like saying “A **and** B must both be true.”
    
- **Example:** 1 AND 1 → 1, otherwise 0.

![[Pasted image 20251107201501.png]]

The And Gate symbol 
![[Pasted image 20251107201754.png]]
### **2. OR Gate**

- **Symbol:** `+`
    
- **Rule:** Output is **1 if any** input is 1.
    
- **Explanation:** It’s like saying “A **or** B can be true.”
    
- **Example:** 1 OR 0 → 1.
![[Pasted image 20251107202237.png]]
### **3. NOT Gate**

- **Symbol:** `¯` (bar) or `’` (prime)
    
- **Rule:** **Inverts** the input.
    
- **Explanation:** If input is 1 → output is 0, and vice versa.
    
- **Example:** NOT(1) = 0. 
![[Pasted image 20251107202357.png]]
### **4. NAND Gate**

- **Symbol:** AND with a small circle (inversion)
    
- **Rule:** Output is **1 unless both** inputs are 1.
    
- **Explanation:** Opposite of AND.
    
- **Example:** 1 AND 1 → 0.
    

---
![[Pasted image 20251107202522.png]]

### **5. NOR Gate**

- **Symbol:** OR with a small circle
    
- **Rule:** Output is **1 only when all** inputs are 0.
    
- **Explanation:** Opposite of OR.
    
- **Example:** 0 OR 0 → 1.
    

---
![[Pasted image 20251107202601.png]]

### **6. XOR Gate** (Exclusive OR)

- **Symbol:** ⊕
    
- **Rule:** Output is **1 when inputs are different.**
    
- **Explanation:** It’s true for “either A or B, but not both.”
    
- **Example:** 1 XOR 0 → 1.
![[Pasted image 20251107202644.png]]![[Pasted image 20251107202714.png]]
### **7. XNOR Gate** (Exclusive NOR)

- **Symbol:** ⊙ or ⊕ with bar
    
- **Rule:** Output is **1 when inputs are the same.**
    
- **Explanation:** Opposite of XOR.
    
- **Example:** 1 XNOR 1 → 1
![[Pasted image 20251107202752.png]]
![[Pasted image 20251107202938.png]]
example : 
![[Pasted image 20251107203004.png]]


to evaluate a logical expression you have to : 
- evaluate the expressions in the parentheses
- do the complementation 
- do the product 
- do the addition 
## types of functions in boolean algebra: 

Canonical form :
which is represented by the existence of canonical terms which means the occurrence of every variable in the function (the occurrence of a var a is the existence of a and $\bar{a}$ )

there are two types of canonical terms : 
- ### Disjunctive form : 
in this form the equation is represented by the sum of products between the variables of the function , so from the truth table we take each row that returns 1 in the function column and we multiply its variables 
Examples:
![[Pasted image 20251107213947.png]]
2. 
![[Pasted image 20251107214126.png]]


- ### The conjunctive form : 
it is represented by the multiplication of the sum of  vars in the row which contains a 0 in its function column 
Examples : 
![[Pasted image 20251107214358.png]]
![[Pasted image 20251107214421.png]]
### conversion between the two forms : 
disjunctive  --> conjunctive  :
replace all the minterms of the function with maxterms that have different indexes than those minterms (and use the multiplication in between )
conjunctive  --> disjunctive :
same thing just the inverse(and use the addition in between )
example : 
![[Pasted image 20251107214830.png]]

### Simplifying the boolean functions : 
the objective of simplifying the boolean function is to reduce the number of logical ops and this the number of logical gates used , and the number of terms in the function 

There are two types of simplification methods : (3 in realty )
1. the algebraic simplification : using the rules and properties of algebraic variables
basically using the axioms and theorems of boolean algebra 
![[Pasted image 20251107220425.png]]
some tips that will help you here : 

![[Pasted image 20251107220632.png]]

![[Pasted image 20251107220649.png]]
2. graphical simplification using the Karnaugh table 
this works by writing all the the function return outputs in a table and then depending on the chosen form group all the 1s or 0s in a form of 2^n so it must be a group of (2 , 4 ,8 ....)
and then eliminate the vars that change in a group and keep what didn't change ![[Pasted image 20251107222910.png]]
![[Pasted image 20251107222918.png]]
![[Pasted image 20251107222927.png]]
![[Pasted image 20251107222939.png]]
step by seep usage : 
![[Pasted image 20251107223126.png]]
![[Pasted image 20251107223132.png]]

![[Pasted image 20251107223934.png]]
![[Pasted image 20251107223948.png]]