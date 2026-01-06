MIASM is a abstract machine which have the same structure as the von neuman machine but it does have everything that a real machine would have . 
![[Pasted image 20251228225645.png]]
(von neuman machine architecture)

## The general structure of a MIASM
- memory capacity is : 2048 words(11 bit address bus)
- the size of a word is 16 bits (data bus of 16 bit)
- the size of the accumulator ,the RIM and RI is 16
- RAM size and CO size are 11 bits 
-  it has 4 flags: 
1- is put 1 if there is an overflow of capacity from one of the ops and 0 in the normal cases 
2- 1 if there is (ba9i) from the op or zero otherwise 
3- 1 if the content of the accumulator is zero and 0 if not 
4- 1 if the content of the accumulator is negative 0 otherwise


![[Pasted image 20251228233515.png]]
## the format of instructions : 
MIASM is a one address machine so the instructions ust be represented in one or more words (in bi ofc) , it has two types of instructions : 
- LONG : this type take 2 memory words : 
 the first has the code operation and the type of the address 
 the second has the address of the one that we are gonna op on 
 - SHORT (like you ) : it has one word which is the op code and the type of address , this format is used by the instructions that don't take adresses (input/output idk why )
 ![[Pasted image 20251228231035.png]]

#### the first word : 
its common in both fomrats : it's made out of 16 bits and divided into multiple fields : 
![[Pasted image 20251228231248.png]]



 the second word : 
 - only for the long format and it contains the adress of the instruction : 
 ![[Pasted image 20251228233138.png]]
### The cycle of execution of a short instruction 
ex : the development of a short instruction ACC in MIASM (input/output):
phase 1 : (search for the instruction for the treatment and decoding ) 
- put the content of CO to the register in the RAM 
- command of reading form the memory 
- transfer the content of the RIM in the register RI 
- analyse and decode 
phase 2 : (treatment)
- command of the execution of the op 
phase 3 :(go to the next instruction) 
- CO = CO + 1 
- ![[Pasted image 20251228234057.png]]
Ex 2 : 
![[Pasted image 20251228233801.png]]
EX 3: 
![[Pasted image 20251228233913.png]]


## assembly 
to make functional programs in  MIASM we need certain keywords which form the assembly language 
### A - switching instructions between the accumulator and the central memory : 
#### 1 - storing : 
MST (RANGEMNT) (Memory storage)
effect : writes what on the accumulator into memory with the given address (the content of the accumulator is not changed) 
format : long 
type of addressing : Direct or indirect : 
examples : MST A (direct mode )
 MST \* B (indirect more)
#### 2 - immediate loading 
ILO 
- effect : the address part of the instruction is changed in the accumulator and its past content is destroyed 
- Format : long 
- type of  addressing : immediate 
- the indicators 3 and 4 of the UAL are positioned depending on the change of the information
ex : ILO 25
ILO 0 
#### 3- memory word loading : 
- instruction : MLO 
- effect :
- the content of the word memory  referenced by the address part if the instruction is changed in the accumulator and  its past content is destroyed . 
- Format : direct 
- type of addressing : Direct or indirect 
- the indicators 3 and 4 in the UAL are positioned depending in the information changed
ex : MLO A (direct)
MLO \* B (indirect)
### B. instructions of arithmetic ops 
#### 1- immediate addition/subtraction 
- instruction : IADD / ISUB 
- effect : the address part of the instruction is either the addition/subtraction or the accumulator . the result is then saved in the accumulator 
- format : long 
- addressage(type of addressing): immediate 
- the indicators 1,2,3 and 4 in the UAL are positioned depending on the changed information 
Ex : IADD 40 
 ISUB 17 

#### 2- memory word addition / subtraction
- instruction : MADD /MSUB
  - effect  :the content of the memory word referenced by the address part of the instruction is addition/sub or the content of the acc(accumulator) , the result is saved in the acc 
  - format : long 
  - the indicators 1,2,3 and 4 in the UAL are positioned depending on the information changed 
  ex : 
  MADD A (direct)
  MSUB \* B (indirect)
#### 3- MUlti/div immediate  : 
- instruction : IMUL /IDIV
- effect : the addr part of the instruction  is either the multi/div or the content of the acc and the result is saved there 
- format : long 
- addressage : immediat 
- the indicators 1,2,3,4 of he UAL are pos according to the info changed 
- ex: IMUL 15 
IDIV 20 

#### 4- memory word MUlti/div  : 
- instruction : MMUL /MDIV
- effect : the content of the memory referenced by the addr part in hte instruction is multi/div by content of the acc and the result is saved there 
- format : long 
- addressage : direct or indirect 
- the indicators 1,2,3,4 of he UAL are pos according to the info changed 
- ex: MMUL A 
MDIV \*B 
### C.Logical instructions : 
#### 1- AND memory word : 
- instruction : AND 
- effect : the AND if executed between the content of the accumulator and the content of the word address of the address part in the instruction , the result is saved in acc 
- format : long 
- addressage : direct or indirect 
- the indicators 3,4 of he UAL are pos according to the found result 
- ex: AND A 
AND \*B (indirect) 
#### 2- OR/XOR memory word : 
- instruction : OR / XOR word  
- effect : the OR/XOR if executed between the content of the accumulator and the content of the word address of the address part in the instruction , the result is saved in acc 
- format : long 
- addressage : direct or indirect 
- the indicators 3,4 of he UAL are pos according to the found result 
- ex: OR A (direct)
XOR \*B (indirect) 
### D. input/ output instructions : 
#### 1- Input : 

- instruction : IN
- effect : the data is entered using a device in the acc 
- format : short
- the field C1 isn't used 
- C2 is the number of the device used (1 is the keyboard)

- ex: IN 01 
 MST A 

#### 1- Output : 

- instruction : out 
- effect : outputs whats on the acc to the device  
- format : short
- the field C1 isn't used 
- C2 is the number of the device used (02 is the display)
- ex: 
 MLO A 
 OUT 02 
 ### E. STOP instruction : 
 - instruction : STOP 
 - Effect : provoke the program to stop 
 - format : short 
 - ex : stop (gg)
### F. Branching instructions?? : 
- in the program the instructions are executed in order generally sequential 
- in some cases the instructions are executed after the verification of some condition 
- if the conditions is not met then a jump will happen , so it jumps to the next instruction (after all whats on  the condition)
- the second word of the  instruction contains the address of the jump (address of the the instruction to execute of the condition is not met ) 
- to test the condition we use the indicators : 
#### 1- (TCB,flag) to check if the condition is true : 
- instruction : (TCB,flag) addr 
- effect :the 3 bits of the c1 field give a number between 0 and 4 for testing : 
- if the number of the condition is 0 : this executes a  branching on the effective address AE ?
- if the number of the condition is 1,2,3or 4 : the corresponding indicator and exe the branching on AE , of the indicator if its  1 , if its 0- no branching - 
- ex : (TCB,4) addr  :branch if the indicator 4 is 1 ( the result is negative )
- (TCB, 3) addr : branch if hte indicator 3 is at 1 (the result is null=0 )
#### 2- (FCB,flag) to check if the condition is false : 
- instruction : (FCB,flag) addr 
- effect :the 3 bits of the c1 field give a number between 0 and 4 for testing : 
- if the number of the condition is 0 : this executes a  branching on the effective address AE ?
- if the number of the condition is 1,2,3 or 4 : the corresponding indicator and exe the branching on AE , of the indicator if its  0 , if its 1 - no branching - 
- ex : (FCB,4) addr  :branch if the indicator 4 is 0 ( the result is not negative )
- (FCB, 3) addr : branch if hte indicator 3 is at 0 (the result is not null $\not=$ 0  )

some ex :
MAX <- A here not B 
![[Pasted image 20251229004241.png]]
![[Pasted image 20251229004249.png]]
![[Pasted image 20251229004255.png]]

### the general structure of a miasm program : 
a miasm program is composed of two parts : 
- data part 
- instructions part
EX : 
- data part : 
-ORG X'100' (the beginning address of the program in the memory ) 
-W MR 1 (reservation of word memory )
-Y IR 10 (reserve a word memory and init  it with 10)


- instruction part : 
-IN 01 
-MADD Y 
-MST W
-OUT 02 
-STOP 
#### 1.The data part : 
for the data we use the two directives : MR and IR 
- MR permits us to reserve a zone in the memory with N word memories 
- IR permits us to reserve a memory zone with initialization 
EX: 
ORG X '100'
W MR 1 (reserves one word)
Y IR 40 (reserves a word an init it with the value 40)
z MR 2 (reserves 2 words)
T IR X'AD' X'12' (reserves 2 word memories and inited with the hex values of 'AD' and '12')


#### 2.The instruction part: 
the instruction part contains the set of  instructions  in order that determine the logic of the program : 
in this part we can find these types of instructions : 
- arithmetic 
- logic 
- input / output 
- branching ......

![[Pasted image 20251229171815.png]]![[Pasted image 20251229172139.png]]![[Pasted image 20251229172201.png]]