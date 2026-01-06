## Voltage Divider : 
A voltage Divider is useful to divide voltage int o different voltage levels from common source voltage either negative or positive +5V ,  -12V.... etc
==this only works on series==

consider this circuit : 
there is only one current flowing around the loop is , we know that  : $V_2 = R_2 . i_s$
we also know that $i_s  = \frac{V_s}{R_{eq}}$ ,$R_{eq} = R_1 + R_2$from [[Alternating current]] on series and parallel resistors  

![[Pasted image 20260106230145.png]]
putting it all together : 
$V_2 = (\frac{R_2}{R_1+R_2})V_s$ 
so basically its the total voltage across all the resistors  times  the resistance itself over the sum of resistances 
## Current divider : 
==only works on parallel==
Current Divider Circuit have two or more parallel branches for currents to flow  through but the voltage is the same for all components in the parallel circuit 
![[Pasted image 20260106230923.png]]

A **current divider** is a parallel circuit in which the source (or supply) current splits among several parallel paths, known as **branches**. In a parallel circuit, all components are connected across the same two nodes, which creates multiple paths for current to flow. As a result, the current can take different paths through the circuit, and the amount of current in each branch may be different.

The key characteristic of a parallel circuit is that although the currents in the different branches can vary, the **voltage across all branches is the same**. This means that  
$$VR1=VR2=VR3=…$$

Because the voltage is common to all parallel components, there is no need to calculate individual resistor voltages. This makes it easier to find the current in each branch by applying **Kirchhoff’s Current Law (KCL)** along with **Ohm’s Law**.a
## Superposition Theorem : 
![[Drawing 2026-01-06 23.21.48.excalidraw]]
c is circuit and c1 and c2 are different configurations for how the flow of the current goes (it could be till n depending on how many generators are in the circuit)
*Superposition theorem* states that in any linear , active bilateral network having more than one source , the response across any element is that sum of the responses obtained from each source considered separately and  all other sources are replaced by their internal resistance , the superposition theorem is used to solve the network where two or more sources are present and connected 
==Ex:== 
![[Pasted image 20260106232054.png]]
the diagram shown below consists of two voltage sources V1 and V2 
![[Pasted image 20260106232509.png]]
![[Pasted image 20260106232614.png]]
$i_3'= i_1' - i_2'$ 
now the other way : 
![[Pasted image 20260106232725.png]]![[Pasted image 20260106232730.png]]
the sing here is dependent on the the direction of the branch chosen compared to the original circuit 
## Thevenin Theorem : 
 the basic idea is that we repalce are the elements that we are not studying with two  values the thevenin voltage and the thevenin resistance
 ![[Pasted image 20260106233045.png]]

   in this new circuit : 
   - $V_{th}$ is the open circuit voltage at the terminals between A and B 
   - $R_{th}$ is the input or equivalent resistance at the terminal when the sources are turned off , the eq resits of A and B 

*how to get the eq circuit ?*:
- Remove the load and lable the terminals to A and B 
- Solve for $V_{th}$(find the voltage at the terminals while supposing its an open circuit)
- solve for $R_{th}$(the eq resistance of the the circuit)
- draw the new circuit 
*detailed:*
![[Pasted image 20260106233728.png]]

![[Pasted image 20260106233747.png]]
![[Pasted image 20260106234023.png]]
![[Pasted image 20260106234135.png]]
## Norton Theorem : 
*Norton theorem* is used to change a complicated circuit into a simple equivalent circuit consisting of a single current source, referred to as Norton current In in parallel
with a single resistance (the same as Thevenin Resistance $R_{th}$ , explained below)
- the value of the norton current is one that flows from terminal A to B when the two terminals A to B when the two terminals are shorted together , this is in fact $I_{SC}$ that is short circuit current 
- The resistance represents the resistance looking back into the terminals when source is switched off . this is in fact Thevenin resistance 
![[Pasted image 20260106234625.png]]