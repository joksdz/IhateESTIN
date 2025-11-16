[Link](https://www.electronics-tutorials.ws/combination/comb_8.html) (better course)
# types of logical circuits
all computers are composed of logical circuits that have special functions(ALU , memory , decoder)
their role is to execute operations on logical variables(binary)
logical circuits are made through combining electronic components
## circuit logique combinatior (CLC)

is a numerical circuit which the outputs of are only dependent on the inputs 
![[Pasted image 20251108212103.png]]

### Analysis pf a CLC
 - determine the output equations 
 - try to understand the functionality of the circuit 


![[Pasted image 20251108213222.png]]

![[Pasted image 20251108213344.png]]
![[Pasted image 20251108213430.png]]

![[Pasted image 20251108213828.png]]
![[Pasted image 20251108213931.png]]
## Semi addition-er
which allows the arithmetic addition of two numbers A and B of one bit  the output has the sum and that remainder ![[Pasted image 20251108214430.png]]
the truth table looks like this : 
![[Pasted image 20251108214508.png]]
the boolean expression looks like this : 

![[Pasted image 20251108214515.png]]

![[Pasted image 20251108214538.png]]
### Full addition-er 
does the addition between two numbers in n bit 
![[Pasted image 20251108214825.png]]
![[Pasted image 20251108214836.png]]


there are two ways of making this either making it from scratch or combining multiple semi-additioners (which is the case for our course)

a full additioner has 3 inputs and two outputs 
inputs : 
Ai : is the first number in bit form 
Bi : is the second number in bit form 
$r_{i-1}$ : is the rest of the previous semi additioner 

outputs: 
Si : is the sum 
Ri : is the reset
![[Pasted image 20251108215721.png]]

the truth table of 1 bit : 


| Ai  | Bi  | $r_{i-1}$ |     | $r_i$ | Si  |
| --- | --- | --------- | --- | ----- | --- |
| 0   | 0   | 0         |     | 0     | 0   |
| 0   | 0   | 1         |     | 0     | 1   |
| 0   | 1   | 0         |     | 0     | 1   |
| 0   | 1   | 1         |     | 1     | 0   |
| 1   | 0   | 0         |     | 0     | 1   |
| 1   | 0   | 1         |     | 1     | 0   |
| 1   | 1   | 0         |     | 1     | 0   |
| 1   | 1   | 1         |     | 1     | 1   |
we can write the expressions as : 

$$Si = m_1 + m_2 + m_4 + m_7$$
$$r_i = m_3 + m_5 + m_6 + m_7$$
Si = 
![[Pasted image 20251108220426.png]]
Ri = 
![[Pasted image 20251108220446.png]]
![[Pasted image 20251108220636.png]]

a Full diagram 
![[Pasted image 20251108220848.png]]
![[Pasted image 20251108220900.png]]

### comparateur 1 bit : 
its  a circuit that compares between two binary numbers A and B and has 2 entries and 3 outputs 
Entries : 
A : 1 bit 
B : 1 bit 
OUTs : 
$F_e$ : equal (A= B)
$F_i$ : less(A< B)
$F_s$ : bigger (A >B)
design : 

![[Pasted image 20251115194537.png]]
truth table : 

algebraic expression : 

![[Pasted image 20251115194603.png]]
the logical gram (what ever this thing is called)
![[Pasted image 20251115194609.png]]
### Decoder  
its a circuit that converts binary information form n info to 2^n unique  outs 
which has n entries 
2^n outs 
one validation input : E (enable)

#### how it works
for example you have 3 inputs e0 e1 e2 you can represent all the numbers form 0 to 8 while E is 1 so S0 being 000 s1 001 and so on thats from 3 single bit inputs 
![[Pasted image 20251115200140.png]]
![[Pasted image 20251115200206.png]]
this is the logigramme of this decoder as you can see you take 3 inputs e0 e1 e2 and you "and" each one of them according the binary number order

### Coder(Encoder): 
its literally the inverse of a decoder its takes 2^n inputs and return n outs while E is enabled ofc 


Example : 
a 8 to # encoder looks like this : 
![[Pasted image 20251115200527.png]]

truth table looks like this : 
![[Pasted image 20251115200558.png]]
which mean we can get 3 expressions s1 s2 s3:  ![[Pasted image 20251115200746.png]]
the loligramme
![[Pasted image 20251115200834.png]]
### Demultiplexer
its a circuit (ofc) that takes D(data) n entries and E(enable)
and outputs 2^n outputs 
fit check 
![[Pasted image 20251115201159.png]]
(ugly)
#### how it works ? 
(who knows ) 
basically guides the data to one out based on the entries of control which can be the address 
$$S_i = E.D.m_i$$
Example : 
a 1 to 4 Demultiplexer will guide the date to s if the command entries are both at 0
![[Pasted image 20251115201749.png]]
looks like this 
![[Pasted image 20251115201803.png]]
loligramme : 
![[Pasted image 20251115201824.png]]

### Multiplexer 
this literally the inverse of a Demultiplexer it takes 2^n entries and outputs 1 out and ofc n entries of control with the E 
#### how it works : 
it redirects one entree from 2^n and guides the data to the single(and ready to mingle) output according to the entries of control 
$$S= E.\sum_{n=0}^{2^n-1}.ei.mi $$
example : 
![[Pasted image 20251115204012.png]]

### (insert 7 segment shit)
bye bye ;) 
