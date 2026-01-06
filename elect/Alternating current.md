### Magnetic induction & flux  
![[Pasted image 20260106205850.png]]
 ![[Pasted image 20260106205950.png]]

==magnetic flux :==
is any area that has a magnetic field passing through it 
the area vector as one that is perpendicular to the surface of the material 
![[Pasted image 20260106210200.png]]
B being the flux and A being the area vector 
$\phi_B = \vec{B} . \vec{A} =BAcos(\theta)$  with the unit being Tm^2 or Weber (Wb)
![[Pasted image 20260106210524.png]]
## Faraday's Law : 
basically if you change any pat of the flux overtime and you will get current by induction in a conductor and thus create a source of EMF (Voltage, potential difference ) we can represent that over time with a rate of change of flux which is in itself faraday's law : 
![[Pasted image 20260106211118.png]]
![[Pasted image 20260106211124.png]]
(looks interesting ;) ) 
#### applications : 
==AC generators== use rotation to turn kinetic energy to electric one 
![[Pasted image 20260106211323.png]]
==Transformers==
AC current moves in the coil very quick back and forth (thus the idea of change ) across the secondary coil , the moving magnetic field caused by the changing field (flux) induces a current in the secondary coil 
==Microphones== : a mic works when sound waves enter the filter of a microphone , inside the filter , diaphragm (like a net) is vibrated bu sound waves which in turn moves a coil of wire wrapped around a magnet which makes current 


## Alternating current : 
if the surface is bounded by a coiled circuit with N turn the total surface is N times the surface of a single turn and : 
$\phi = N\vec{B}.\vec{S} = NBScos(\alpha)$ 
( $\vec{S}$ is always the surface vector of a single turn ! )
The phenomenon of electromagnetic induction occurs in an electrical circuit if the magnetic flux changes . 
If the circuit is open, the phenomenon is manifested by an electromotive force (EMF) appearing
at the circuit's terminals. If the circuit is closed, it is manifested by an induced current flowing in
the circuit. It can be noted that the EMF produced by an alternator is expressed as: $NBS\omega.sin(\omega.t) = E.sin(\omega.t)$ 
![[Pasted image 20260106212859.png]]
A current is alternating if it changes direction over time t. Furthermore, it
is periodic if its intensity i repeats the same value at intervals of time
equal to T. We then have:
i = f(t) = f(t+nT) 
![[Pasted image 20260106213237.png]]
frequency : f =1/T (Hz) T being the period of one full alternating wave in seconds (s) 

An alternating current is sinusoidal when its current intensity is a sinusoidal function of
time : 
𝑖 = 𝐼ₘ sin(𝜔𝑡 + 𝜑) 𝑜𝑟 𝑖 = 𝐼ₘ cos(𝜔𝑡 + 𝜑)
where  : 
i is the instantaneous value of the current 
Im is the maximum value of the current 
$\omega$ = is the angular frequency . 𝜔 = 2𝜋𝑓 = 2𝜋/𝑇
$\phi$ = is the phase angle 
Note: You can also use a cosine function instead of a sine function to represent an
electrical signal. For example, for voltage:
𝑢(𝑡) = 𝑈ₘ sin(𝜔𝑡 + 𝜑ᵤ) = 𝑈ₘ cos(𝜔𝑡 + 𝜑ᵤ − 𝜋/2)
Here, Uₘ is the maximum voltage value or amplitude, and φᵤ is the phase angle.
![[Pasted image 20260106214204.png]]
A voltmeter indicates the root mean square electromotive force
$$E_{eff} =E/\sqrt2$$ the square root of the average of e^2 over time )
Ex : 
![[Pasted image 20260106214346.png]]
## Complex concept of electrical quantities : 
### module and argument 
![[Pasted image 20260106214537.png]]
![[Pasted image 20260106214545.png]]

#### props of complex numbers : 
##### addition : 
z1 = a +bj 
z2 = c +dj 
z = z1 +z2 = (a+c) + j(b+d) 
##### Multi: 
z =z1 . z2 = z1 . z2 . $e^{j(\phi_1 +\phi_2 )}$
![[Pasted image 20260106214934.png]]
##### Div : 
Z = Z1/Z2 
 Z = (z1 /z2 ) . $e^{j(\phi_1 - \phi_2)}$ 
 ![[Pasted image 20260106215154.png]]
![[Pasted image 20260106215223.png]]
#### representations : 

voltage : 

$$u(t) = U_m sin(\omega t+\phi_u) => U = U_me^{j\phi_u} = U < \phi_u$$
current : 
$$i(t) = I_m sin(\omega t+\phi_i) => I = I_me^{j\phi_i} = i < \phi_i$$
Representation of the impedance : 
complex impedance is represented by Z = z$e^{j\phi}$

z is the impedance in ohm($\ohm$)
$\phi$ is the phase difference between the current and the voltage  
$\phi=\Delta\phi =\phi_u -\phi_i$  
#### applications :
![[Pasted image 20260106220108.png]]
z in ohm z = U/I
the cartesian form of Z : 
![[Pasted image 20260106220314.png]]
![[Pasted image 20260106220348.png]]
Ohms law for a restive conductor : 
$Ur = Zr$ 
$Ue^{j\phi_u}=RIe^{j\phi_i}$  
U =RI , $\phi_u = \phi_i$
![[Pasted image 20260106221722.png]]
![[Pasted image 20260106221727.png]]
###### the impedance for an inductive conductor :
==uwu:==
z= $L\omega$ (w = 2.pi. f )
$phi_z=\pi/2$ 
==\uwu==
![[Pasted image 20260106222823.png]]
###### capacity : 
==uwu:==
z= $1/(C\omega)$   (w = 2.pi. f )
$phi_z=-\pi/2$  
==\uwu==
![[Pasted image 20260106223011.png]]


### Equivalent impedance of dipole association : 
impedance works like resistance so on series the eq is  the sum and on parallel its the inverse of the sum of the inverses of each imedance
#### series Association : 
According to kirchhoff's Voltage Law : 
![[Pasted image 20260106223247.png]]
U = U1 + U2 
with U1 = Z1 . i , U2 = Z2 . i 
U = (Z1 + Z2) . i = Z . i , Z = $Z_{eq}$   
![[Pasted image 20260106223423.png]]
$Z_eq= \sum^n_{i=1}Z_i$ 
#### parallel : 
![[Pasted image 20260106223748.png]]
 I = I1 + I2 + I3 and $I_i =\frac{U}{Z_i}$   (am using I instead of I cuz I is a complex number not just one real var )
 ![[Pasted image 20260106223939.png]]
 ![[Pasted image 20260106223947.png]]
$$Zn = (\space\sum^n_{i=1} \frac{1}{Z_i} \space)$$
### Applications : 
#### Dipole R,L in series (real coil) :
![[Pasted image 20260106224144.png]]
![[Pasted image 20260106224151.png]]

R,L,C : 
![[Pasted image 20260106224230.png]]
R,L,C Parallel :
![[Pasted image 20260106224257.png]]
![[Pasted image 20260106224307.png]]