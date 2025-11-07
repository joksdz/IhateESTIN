

Encoding is the process of converting data into a specific format for processing, storage, or transmission, primarily by transforming it into binary code that a computer can understand and execute. This includes instructions for the processor, text characters (like ASCII), and multimedia data.

## Data representation : 
To represent a number in n bits the largest number we can represent is $2^n -1$  while the number of combinations is $2^n$ 


![[Pasted image 20251012172507.png]]

### representation of an unsigned int : 
an unsigned int is a number that is natural (no signs)
![[Pasted image 20251012172648.png]]
this means that we can represent all the numbers in $[0 , 2^n -1 ]$
### representing a signed int : 
to represent a signed int we have 3 methods //(for now)
### A.Representation by sign + absolute value (S + AV):

to represent a number in S+av you have to use the binary representation of said number and just put a 1 for minus sign(-) or 0 for the plus sign (+) at the left most position of the number according to the specified number of bits n 
so if your told to represent the number -3 in 5 bit you would write : 
(-3)$10$  = (10011)$s+va$ 
the number you can represent with n bits are the numbers that are included in this interval : 
$[-(2^{n-1} -1) ,+(2^{n-1}-1)]$ 
![[Pasted image 20251012175848.png]]
### B.Representation by restricted complement 

RC(0)=1 / RC(1)=1 
meaning you flip everything except the sign 
==Note:== this is only true for the is negative numbers positive numbers are represented the same way as the s+av
with this method we can represent all the numbers in n bits in the interval : $[-(2^{n-1} -1 ), 2^{n-1} -1 ]$ 
![[Pasted image 20251012181653.png]]
### C.Representation by True complement : 
TC(A)= RC(A) +1 

to represent a number in n bits in tc you have to convert it to Rc and add 1 to it or !! read from left to right and in the s+AV and keep numbers as they are until you reach a 1 when that happens keep it and flip everything after it except the sign which is the leftmost digit 
using this method allows us represent all the numbers in between the interval : $[-(2^{n-1} ), 2^{n-1} -1 ]$
## Applying arithmetical operations on different types of representations : 
### 1.On restricted complement : 
we keep the positive numbers as they are in the binary form then change the negative numbers to the RC then we do normal addition if we get a new 1 that exceeds the number of bits given (n) we must add it as a 1 in the rightmost (before the decimal (maybe))
![[Pasted image 20251012201239.png]]
![[Pasted image 20251012201447.png]]

### 2.On truth complement : 
its the same thing with the RC but if there is a carry at the end we just ignore the fuck of it .
![[Pasted image 20251012201650.png]]


### Some problems that you can face : 
![[Pasted image 20251012201733.png]]

## Representation of real numbers : 
Floating points :
a floating point number is defined by : $$\pm m . b^e$$
![[Pasted image 20251012202007.png]]

### IEEE754 standard : 
in this standard we represent the sign with 1 bit at the left most part of the number 1 for - , 0 for + 
there are two types in this standard
single precision (32 bit representation): the exponent is represented in 8 bits and the mantissa 23 bits 
for the double precision (64 bit representation) : the exponent is represented in 11 bits while the mantissa is represented in 52 bits 

![[Pasted image 20251012205352.png]]

### 1.single precision : 
![[Pasted image 20251012205849.png]]

### 2.Double precision : 

![[Pasted image 20251012205917.png]]
### BCD(binary codded decimal): 
![[Pasted image 20251012210001.png]]
### Gray code : 
![[Pasted image 20251012210023.png]]
