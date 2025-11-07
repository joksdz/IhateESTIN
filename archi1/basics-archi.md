

## Intro  : 
A computer processes data, making it essential to encode and represent it in various forms, such as: nums , text,images... 
and this representation is in binary form meaning 1s and 0s 
## Numerical systems : 
A numeration system describes how numbers are represented and it has 3 properties : 
- the base 
- a set of digits 
- rules for representing numbers 
## Common numerical systems in archi : 
### Decimal system (base 10):
$A = {a0,a1,a2,....,a9}$ with 0 <= ai < 10 
to represent a number in decimal from another numerical system we use multiplication with the base to the power of the position and we sum them up : 
example : to represent (1010100)(base 2) in base 10 we do : 
$$0*2^0 + 0*2^1 + 1*2^2 + 0*2^3 +1*2^4 +0*2^5+1*2^6 = (84)base 10$$
we can represent it with this sum : 
$$ (N)_B=\sum_{i=-p}^{n-1} a_i b^i$$
 where : 
 N: number 
 B:base 
 $a_i$= digits($a_i$<B)
 $B^i$ = weight 
 i= rank
 (note : to represent the numbers after the decimal point we take the $b^{-1}$ and continue...  ) 

  ![[Pasted image 20251005104915.png]]
  now to represent a number from base 10 to any other base we have to do successive division then we take the rest from the last division to the first (so that the last remainder is the first number in the new base)
  ![[Pasted image 20251005105327.png]] to represent the numbers after the decimal point we have to do successive multiplication 
  ![[Pasted image 20251005105550.png]]  to go form any base to another we need base 10 to be an intermediate meaning we convert base1 to base 10 then we convert 10 to base 10 
  Note: there are ways to convert from base 2 to base 8 and base 2 to base 16 directly we will talk about that later...
  ![[Pasted image 20251005105829.png]]

## hexadecimal system(base 16) 

$A = {a0,a1,a2,....,a9,A,B,C,D,E,F}$ with 0 <= $a_i$ < 16 (0<=i<10)
to convert base 16 to base 10 we use the rule mentioned above 
to convert base 16 to base to base 2 we follow this rule : 
![[Pasted image 20251005110341.png]]
you take the numbers from right to left after the decimal point and represent each one in 4 bits and if we have less than 4 in the last digit we add 0s to the front , to represent the number before the decimal point we go from the right of it to the left and if we have less than 4 digits we add 0s to the back of it

to convert from base 2 to base 16 we do the inverse : 
![[Pasted image 20251005110522.png]]we split the number into 4 bits and we convert each one into hex
we follow this table for conversion : 
![[Pasted image 20251005110640.png]]

## Octal system (base 8)
$A = {a0,a1,a2,....,a7}$ with 0 <= $a_i$ <8 (0<=i<8)

to convert base 8 to 10 or 10 to 8 we use the rules mentioned above 
to convert base 8 to base 2 we do : 
![[Pasted image 20251005110924.png]]
you take the numbers from right to left after the decimal point and represent each one in 3 bits and if we have less than 3 in the last digit we add 0s to the front , to represent the number before the decimal point we go from the right of it to the left and if we have less than 3 digits we add 0s to the back of it
to convert from base 2 to base 8 : 
![[Pasted image 20251005111237.png]]


## Addition in binary 
you only have to do normal addition just using this table : 
![[Pasted image 20251005111416.png]]


ex : 
~~~
 (10)1(1)0(10)1(1)01
+11111
-------
= 110100
~~~
Note : the numbers in the () are the new numbers after we added the carried 1 
![[Pasted image 20251005111741.png]]
![[Pasted image 20251005112553.png]]
## Multiplication 
its easy really just normal multi + addition 
![[Pasted image 20251005112903.png]]

## Subtraction : 
for subtraction you need to do normal things when its 0-0 , 1-0 , 1-1 but when you have 0-1 you need to make it so that the zero is 10 (2) then you return the 1 that you take to the next power on the lower part of the subtraction(the sub-tractor )
which means 0-1 = 1(and you carry the one to the next sub-tractor )

![[Pasted image 20251012142207.png]]

## Division :
to divided something in binary you have to check if it fits inside(its less than) the number with the same number of digits in the leftmost position of the number being divided if that's true then put a 0 and subtract the divisor from the divided if not put a one and pick a number of digits that is bigger than the number of digits of the divisor , now if there are no more numbers just put the decimal point there and add 0s to the divided from the right  
![[Pasted image 20251012142747.png]]
