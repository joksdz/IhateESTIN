[Link](https://www.electronics-tutorials.ws/combination/comb_8.html) (better course)
# types of logical circuits
all computers are composed of logical circuits that have special functions(ALU , memory , decoder)
their role is to execute operations on logical variables(binary)
logical circuits are made through combining electronic components
## circuit logique combinatior (CLC)

is a numerical circuit which the outputs of are only dependent on the inputs 
![[Pasted image 20251108213222.png]]
![[Pasted image 20251108213344.png]]
![[Pasted image 20251108213430.png]]
![[Pasted image 20251108213828.png]]
![[Pasted image 20251108213931.png]]
![[Pasted image 20251108214508.png]]
![[Pasted image 20251108214515.png]]
![[Pasted image 20251108214538.png]]
![[Pasted image 20251108214825.png]]
![[Pasted image 20251108214836.png]]
![[Pasted image 20251108215721.png]]

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


GOOOOOOOOODDDDD MORNING VITANME!!!!!!!!
## Sequential shit 
a sequential circuit is a logical circuit where the output depends on the input and the state of the memory as well 
so it memorizes the past state this is generally how it looks 
![[Pasted image 20251122234025.png]]
(pretty like you bro ;))
### types 
there are two types of sequential circuits 
- synchronous: the output depends on the change in the external entries ***And*** the current state ***And*** the signal from the clock  

- asynchronous : the output is based on the change of the external entries ***OR*** the internal state

The clock : 
is an electrical signal that oscillate that controls the rhythm of the circuit , the period is called a cycle 

there are 4 types of clocks which depend on the sensitivity of the clock  : 
- low level sensitive :
![[Pasted image 20251122235148.png]]
- rising edge sensitive :
![[Pasted image 20251122235230.png]]
- high level sensitive : 
![[Pasted image 20251122235259.png]]
- falling edge sensitive : 
![[Pasted image 20251122235331.png]]
![[Pasted image 20251123001503.png]]
the cycle us represented as the delta time between two points at the same (y) from different (x)s 
T is in seconds 
![[Pasted image 20251122235502.png]]
the frequency is the inverse of the period T thus : 
$f=\frac{1}{T}$ which is represented in hz (hertz(those germans))   

### flip flops (cool name btw)

a flip flop is a circuit that can memories 1 bit of information , which with creating counters(or down counters its 2025 bro )
and we can have complex memorization like registers or memory cells 
#### types 
there are two types based on the sequential circuit used (sync or async) 
and 4+ types based on entries : 
- RS(reset/set)
- JK(j=S/k=R)(just a bit diff)
- D(direct info)
- T(the flip flop(bro literally just flip flops all day))
etc ++(idk thats what she wrote)

==Note:== all the flip flops based on entries are based on RS 


### RS flip flops  :
##### async : 
they have two inputs : 
R for rest to 0  
and S for set to 1  (wow)
and they return two outputs : Q and $\bar{Q}$ 
![[Pasted image 20251123001400.png]]

![[Pasted image 20251123001343.png]]



tarns table : 
![[Pasted image 20251123003646.png]]
we can also write it as : 



![[Pasted image 20251123003709.png]]
karghnau + resualt 
![[Pasted image 20251123003744.png]]
==Note:== the output Q represent the current state of the flip flop and $Q^+$ is the future state
 ##### sync: 
this one has 3 inputs  R S and H or CLK 
![[Pasted image 20251123003100.png]]