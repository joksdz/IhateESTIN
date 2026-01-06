### How does it move ? 
certain materials like metals (aluminum ,copper ) because they have electrons that they can be liberated from the attraction of the core to participate in the electrical conduction  where as there are other materials that are can insulators where electrical chargers cant move .

### What is electrokinetic  ? 
it is the study of the movement of electrical charges and its phenomenons,when can do so because the movement of charges in a conductor isn't instant but close to the speed of light $$c= 3*10^8 m/s$$
#### receptors
are devices that transform electrical energy to different forms of energies 
#### The role of a generator
is not to manufacture charges but to move the free charges that are already in the conductive material and the movement of these electrical charges is what we call the current (I)  

### Electrical charges and Electrical current 
the elementary charge "-q" is the one of an electron which is represented by the unit Coulomb (C) which take the value : 
$$ -q =-1.6*10^{-19} C$$
the charges that move can be positive (positive ions) but the majority that contributes to electrical conduction are electrons 

Electric current is the movement of charge carriers in a conductor under the influence of an external electric field. The direction of electric current (represented by an arrow) is
conventionally considered to be the direction in which positive charges would move (hence, opposite to the direction of electrons). It is generally measured as positive from
the + terminal of the generator to the terminal in the external circuit.
The intensity of a current (denoted as I) is a flow of charges (quantity of charges per unit of time).
### How does it work ? 
In a conductor with cross-section 1 cm^2 , the mobile charges (electrons) move randomly due to collisions, and since there is no electric field and them moving in every direction at once, their average contribution to current is zero.(the last part basically means that because they are moving in multiple directions and not in one direction making the amount of charge that is moving in the one direction the same as any other which the sum of is 0  ) (and this is why there is no electricity in a random wire not because there are no charges but their movement is so random that they can't make a current, they need an electrical field )

their speed is represented by : 
$$ \vec{V} = \mu*\vec{E}$$
where V : is the speed vector 
E : is the electrical field vector 
$\mu$: is the mobility of the charges which uses the unit $m^2 /(v*s)$

![[Pasted image 20260106185339.png]]
now in the span of 1 second the number of charges that passes through the surface $\vec{dS}$ is : 
$$N = \vec{v}.n.\vec{dS}.dt=\vec{v}.n.1cm^2.1s$$
where n is the density of the charges which means the number of mobile charges per unite volume of the conductor 

which makes the the electric charge the passes through the section in 1 second : 
$$dQ = qN=q.\vec{v}.n.\vec{dS}.dt$$

==.== The flux of electrons (i.e., the flow of mobile charge carriers through the cross-section of a conductor) is what we call the electric current I.which is represented by the unite ampére or amps (A)

$$I = \frac{dQ}{dt} = \vec{J}.\vec{dS}$$

![[yay.jpg]]

$\vec{J}$  is the density of the current which has the unite of $A.m^{-2}$ 
which is tied to the speed of the mobile charges and the volumetric density of the local charges : 
$$\vec{J}=p.\vec{V}$$
which can be expressed as : 
$$\vec{J}= p.\mu.\vec{E} = \sigma\vec{E} $$
$\sigma$: is the electrical conductivity of the conductor uses simens per meters (S/m)
![[Pasted image 20260106185501.png]]
##  Relationship between the electric field and electric current density:
![[Pasted image 20260106185657.png]]
![[Pasted image 20260106185735.png]]
## the Joule effect : 
According to the definition of electric potential, the work 𝑑𝑊 done by the elemental
charge 𝑑𝑞 moving between two points where there is an electric potential difference (or
voltage) 𝑈 is:
𝑑𝑊 = 𝑈. 𝑑𝑞 
n general, we define power in both electricity and mechanics as the work done per unit
of time, which can be expressed as: P = dW/dt =$u.dq/dt$ = U . I 

According to the definition of energy, we can deduce that the energy E produced by a
source or the energy consumed by a resistor during the time interval Δt is given by : $$E=U.I.t = R.I^2.t = \frac{U^2}{R}.t$$
with the unit of joule (j)
## The laws of electric circuits : 
Consider the circuit depicted in the figure, consisting of a generator (with
electromotive force e and internal resistance), an external resistor 𝑅, and a
motor (with electromotive force 𝑒′ and resistance 𝑟′).
The generator produces electrical power: 𝑃 = 𝑒. 𝐼
The ohmic resistor (R) converts electrical energy into heat energy, with a value
of 𝑅𝐼2. The internal resistance of the generator also consumes a portion of this
energy(there is an internal resistance missing )
![[Pasted image 20260106192357.png]]

According to the principle of conservation of energy, the energy produced is
equal to the energy consumed.
𝑒𝐼 = 𝑒’𝐼 + 𝑅𝐼2 + 𝑟𝐼2 + 𝑟′𝐼2
Hence, the current intensity that flows through the circuit is determined by this energy conservation principle : $$I = \frac{e-e'}{R+r+r'}$$
so its gonna be : (equation of the electric circuit)$$I = \frac{\sum e}{\sum r + \sum R}$$
### generator grouping
a/ Case of voltage generators: Each generator is characterized by an electromotive force 𝑒𝑖 and an internal resistance 𝑟
![[Pasted image 20260106193011.png]]
![[Pasted image 20260106193104.png]]
We consider the receiver (for example, a motor) as a generator connected in opposition to the effective generator, and the generator connected in opposition serves as the receiver (or motor). The generator with the higher electromotive force (EMF) takes precedence as the generator.
Hence:
![[Pasted image 20260106193202.png]]
Series system In this case, the electromotive force (EMF) of the equivalent generator is equal to the EMF of a single generator in the group, and the inverse of the equivalent resistance is equal to the sum of the inverses of the internal resistances.
$$I = nI_1 ; e= e1 ; 1/r = \sum 1/r_i = n/r_i$$
## kirchoff's laws : 
### a.Node law :
At a node in a circuit, the sum of the entering currents is equal to the sum of the exiting currents: $$\sum I_s = \sum I_e$$
this means that the charges do not accumulate ,they flow in and out 
### b.conservation of energy of loop law : 
in an electrical circuit loop k , the algebraic sum of the products of resistance by current $\sum^{n}_{k=1}= e_k$ $$\sum^n_{k=1} = \sum^n_{k=1} R_k .I_k$$
### kirchhoff's laws:

kirchhoff laws known as k current law(KCL)  and k voltage law (KVL) are based respectively  on the conservation of charge and of energy. 
#### kirchhoff's current law
it states that the current flowing out of any node in a circuit must be equal to the current flowing into the node it is expressed mathematically as : $\sum^N_{n=1}i_n=0$ 
where N is the number of branches  that are connected to the node by adopting sign convention that current flowing into a  node is positive + and current flowing out of the node is negative - application of KCL gives 
 i1 + i2 = i3 + i4 
 ![[Pasted image 20260106204302.png]]
 ![[Pasted image 20260106204350.png]]

![[Pasted image 20260106204452.png]]
i3 = Is + i1 


#### kirchhoff's voltage law
states that hte algebraic sum of voltage around a closed loop is zero it is expressed mathematically as : $$\sum^N_{n=1} V_n= 0$$
where N is the number of voltages in the loop then number of voltages is equal to the number of elements encountered as we go around the loop . 
![[Pasted image 20260106205111.png]]
