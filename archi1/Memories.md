[src](https://elearn.estin.dz/pluginfile.php/12757/mod_resource/content/1/Overview%20of%20the%20computer.pdf) , [src2](https://drive.google.com/drive/folders/1xCN4KvhhUCH5S9abf3zoG5x-c4vpWREN)

with 1 flip flop we can memories 1 bit , with a register we can do n bits , so if we need to memories smth with a big 
## material Architecture of a machine (von neuman) : 
 its composed of : 
 - central memory 
 - central unit or a CPU 
 - this a archi is the base of the computers 
 ![[Pasted image 20251229173727.png]]
### Central Unit (UC)
 the central unit also called the processor takes the role of executing the programs 
 the UC is composed of an arithmetic and a logical unit (UAL) and a unit of Control 
- the UAL can do elementary ops like add sub multi and is processed each top of the clock 
- the command unit(control) controls the ops on the memory (read and write ) and the ops made by the UAL according to the instruction that are being executed 
 to do some ops on the data and execute the programs UC has to dispose a space of work this space is the central memory 

### What is a memory ? 
a memory is a device capable of : 
- save info 
- store the info 
- give the ability to read that info 
Examples on memories : 
- central memory 
-  a hard disk 
- a floppy disk  
- a flash disk 

the memory could be integrated into the processor (registers) , internal (central memory or principal) or external (secondary memory  )
#### the characteristics of memories : 
##### the capacity : 
its the number of information that we can store in this memory 
we use the these units to quantify it : 
Bit : is the base element of the information represents either a 0 or a 1 
Octet (bytes): 1 octet = 8 bits  
![[Pasted image 20251229194453.png]]
#### volatility: 
if a memory loses its cotent when the source of the info is cut then the memory is called a volatile memory 
if a memory doesn't loose the info when the source is cut off then its non volatile (permanent or stable memory) 

##### READ and write-ability : 
in a memory we can do ops like : 
- read : retrieve or restore the information from the memory 
- write : save the new information or modify the existing info in the memory 
there are memories that offer both modes we call them live memories , and there a re that offer only the possibility of reading (you cant modify) we call them dead memories 

#### Classification of the memories : 
we can class memories into 3 categories based on the tech used : 
- semi conductive memories : (central memory , rom , PROM...): really fast with a small size 
- magnetic memories : (hard disk , floppy...) : less speed but with high capacity  
- optical memories (DVD,CDROM)
 ![[Pasted image 20251229202317.png]]

#### Semi-conductive memories : 
![[Pasted image 20251229195611.png]]
The central memory is called RAM : random access memory
![[Pasted image 20251229202306.png]]

#### what is the central memory : 
the central memory represents the working space of the computer 
its the principal organ for arranging the information used by the processor 
in a machine (pc) to execute smth you need to load it into the RAM first (like copying it ) 
the time of access in the central memory and its capacity are two elements that influence the time of execution of the program (the performance) 
##### characteristics of the central memory 
- its based on a semi conductor 
- its a live memory 
- its random access (RAM) which means that the time of access to the information is independent from the place in the memory 
- its volatile : the conservation of the content needs permanent power supply 
- the speed of access to it is mid but faster that the rest of memories outside of the internals 
- the capacity of the central memory is limited but always has the possibility of extending 
- to communicate with other devices in the pc it uses buses (address buses or data busses )
##### the types of central memories : 
there are two types of memories SRAM and DRAM : S for static and D is for dynamic 
 SRAM : are based on the flip flop of type D and the have a bad integration ability but a fast access time (used for cache memories )
 DRAM : based on the condensers these memories have a really big integration ability and they are simpler than the static memories but slower 
![[Pasted image 20251230130943.png]]
#### logical overview of the central memory : 
- it can be seen as a large vector (table) of words or octets(bytes)
- a word memory stores info in n bits 
- a word memory contains many memory cells
- a memory cell can stock up to 1 bit 
- each word has its own address 
- an address is a unique number that permits us to access a  word memory
- the addresses are sequential (consecutive) 
- the size of the address (the number of bits) deprend on the capacity of the memory 
 ![[Pasted image 20251229202143.png]]
![[Pasted image 20251229202457.png]]
### The physical structure of the central memory : 
- **RAM** (memory address Register ): is a register that holds the address of the word memory for reading or writing 
- **RIM** (memory information Register) : saves info read from the memory or the information in the memory 
- **Decoder**: permits us to select a word memory 
- **R/$\bar{W}$** : is the command of the reading/writing this command permits us to read or write to the memory (if R/$\bar{W}$ = 1 then its on reading mode else it's on writing ) 
- addresses bus with a size of k bits 
- the data bus has a size of  n bits 
![[Pasted image 20251229203245.png]]

![[Pasted image 20251229203437.png]]

![[Pasted image 20251229203430.png]]

### How to select a word memory : 
when the address is changed in the register RAM , the decoder has to receive the same info as the one in the RAM 
for the output of the decoder we are gonna have one ouput which is active => permits the selection of the one word memory 
![[Pasted image 20251229203747.png]]
### How to calculate the capacity of a central memory : 
- given k size of the address bus (the size of the register RAM ) 
- and n the size of the bus of the data (the size of the register RIM r the size of the word memory) : 
- we can write the capacity of the central memory either iin number of word memories or in bits (octets , KO) :
-  the capacity =$2^k$ word memories 
-  the capacity = $2^k$ x n bits 
Example : 
in a memory with an address bus of k =14 and the size of the data is n=4 calculate the capacity of this memory ?
![[Pasted image 20251229204418.png]]
#### HOW to read info? 
to read info in the ram we need to do these ops : 
- load the address of the word memory we want to read into the -
RAM register 
- put R/$\bar{W}$ =1 
- then the info will be stored in the RIM register for a duration (access time )
#### HOW to write info ? 
to write into an MC do these ops : 
- load the address where we want to save the info in the RAM register 
- put the info in the RIM register 
-  put R/$\bar{W}$= 0 so that the info is transferred from the RIM to the memory 
### Making a central memory : 
if we want to make a memory of size C but we have only boxes (circuits ) of a lesser size 
![[Pasted image 20251229205630.png]]
![[Pasted image 20251229204514.png]]
![[Pasted image 20251229210132.png]]
![[Pasted image 20251229210207.png]]
#### the structure of the modules : 
a module has the same structure as the memory (RAM , RIM ) + a command $\bar{CS}$ (the bar is over both) (chip select) : 
its a command that has the negative logic that permits us to select or activate the module  
$\bar{CS}$ = 0 then the module is selected else no ![[Pasted image 20251229210032.png]]
some examples : 
![[Pasted image 20251229210409.png]]![[Pasted image 20251229210419.png]]![[Pasted image 20251229210424.png]]![[Pasted image 20251229210432.png]]![[Pasted image 20251229210437.png]]![[Pasted image 20251229210444.png]]![[Pasted image 20251229210450.png]]

#### some other types of memories : 
![[Pasted image 20251229224814.png]]
![[Pasted image 20251229224836.png]]btw cache stores instructions or info that is repeatedly accessed from ram to save time . 
## Execution function : 
The CPU central processing unit is the core component of a computer that executes instructions , it preforms basic ops and input/output processing . 
characteristics : Frequency(GHZ) , instruction set,...
### the functional units of the cpu :
 ![[Pasted image 20251229225139.png]]
 ALU (UAL) is arithmetic and logic unit 
 the data is in genral-purpose registers 
 the result is placed in the accumulator (we call it acc for short) 
 ![[Pasted image 20251229225411.png]]
### ALU Registers : 
- general-purpose registers 
- accumulator register (ACC)
- status register : has these flags C S O Z 
![[Pasted image 20251229225518.png]]
![[Pasted image 20251230130727.png]]

- pointer register (SP stack pointer )
-  Index register 
- base register 
### CCU(control ad command units) Registers : 
- program counter (PC)
- instruction register 
![[Pasted image 20251229225633.png]]
note : an operand can be either data or and address 
- decoder 
- sequencer 
- clock 
![[Pasted image 20251229225733.png]]
### Machine instruction structure : 
A machine with 4 addresses : 
- a field for op code 
- four address fields : 
- 1 : 1st operand
- 2: 2nd operand
- result addr 
- next instruction addr 
![[Pasted image 20251229230017.png]]
![[Pasted image 20251229230111.png]]
![[Pasted image 20251229230426.png]]
![[Pasted image 20251229230444.png]]
content of the PC : 191

![[Pasted image 20251229230600.png]]

#### Access modes : 
this defines how the operand is gonna be accessed , the op code contains a set of bits that indicate the address mode 
- Immediate 
- direct 
- indirect 

- indexed 
- relative 

#### Immediate addressing : 
Load #15
this means it loads the value : 15 directly into the acc 
![[Pasted image 20251229230815.png]]
#### Direct :
Load 15 : 
![[Pasted image 20251229230915.png]]
loads the content of the memory address 15 

#### Indirect : 
Load (15) : 
![[Pasted image 20251229231009.png]]
 basically its using pointers , like we have are looking what does the address 15 points to , it holds the real address as its content 

#### index addressing : 
Effective address = addr + Index 
![[Pasted image 20251229231527.png]]
ig its like relative to where the x is (its not really relative more like absolute cuz x is always 100 from what ive seen here idk if thats true )

#### Relative addressing effective : 
![[Pasted image 20251229231741.png]]
goes backwards or forwards relative to where the current program is at 
### instruction cycle : 
![[Pasted image 20251229232823.png]]
![[Pasted image 20251229232830.png]]
the same thing is in [[MIASM]]
##  Communication function 
basic functions of a computer : 
![[Pasted image 20251230002056.png]]
peripherals : 
![[Pasted image 20251230002111.png]]

### Exchange units :(input/output)
enables communications between the components of the machine 
they consist of buses input/output interfaces , and peripheral controllers 
#### Bus 
they are carriers of information exchanged between the various components of the computer 
 - data lines 
 - address lines 
 - control lines 
 characteristics : 
 - number of address lines in the bus 
 - number of data line in the bus (serial or parallel connections)
 - Direction of data transfer in the bus (unidirectional , bidirectional) 
 - transmission mode 
 ![[Pasted image 20251230125437.png]]
 ![[Pasted image 20251230125442.png]]


bus :
parallel 
takes multiple lines fast but not good when its too close of a distance (interference )

serial :
transmits bit by bit

PCI express 
slower but better for security 


the direction of communication : 
uni directional: take one way like display , keyboard  
bi directional : takes and returns  like the bus from the cpu to ram 
: 
sync: send the info in the same time like second 
async : send the info not at the same time like you send now some then 4 sec later you send the rest , like when the sending to a device that is busy like the printer 
