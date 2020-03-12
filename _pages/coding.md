---
layout: archive
title: "GCMC Simulations"
permalink: /coding/
author_profile: true
redirect_from: 
  - /md/
  - /markdown.html
---

For this project, Grand Canonical Monte Carlo Simulation (GCMC) will be adopted for calculating adsorption isotherms based on the Catlow and Faux force field provided by [MCCCS Towhee](http://towhee.sourceforge.net/forcefields/catlow_faux.html). This page will be updated with relevant files, instructions, graphs and data relevant to the simulation work I am doing. 

Catlow/faux Force field
======

~~~
towhee_ff Version
          15
Number of Nonbonded Types
           9
Potential Type
Exponential-12-6              
Classical Mixrule
Explicit                      
Atom Type Number
           1
Nonbond Coefficients
   -0.2465945413E+06
    0.0000000000E+00
    0.2641636770E+09
   -0.6711409396E+01
Nonbond Coefficients
   -0.5802224500E+06
    0.1334511635E+08
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.1508578370E+08
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.6773331210E+08
   -0.4189359028E+01
Nonbond Coefficients
   -0.2718806356E+06
    0.6550911057E+08
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.6281488244E+05
    0.7667964601E+07
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.2048649426E+06
    0.1276489390E+09
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.6465650849E+05
    0.1806116442E+08
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1599900000E+02
Element
 O
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
OZ        
OZ        
OZ        
OZ        
Atom Type Number
           2
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.6800207114E+04
    0.1235177552E+06
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.1032795961E+04
    0.6405655848E+04
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.2808600000E+02
Element
Si
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
Si        
Si        
Si        
Si        
Atom Type Number
           3
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.5802224500E+04
    0.1364451113E+06
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.8703336750E+03
    0.7264385074E+04
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.2698200000E+02
Element
Al
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
Al        
Al        
Al        
Al        
Atom Type Number
           4
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.6773331210E+08
   -0.4189359028E+01
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.3991930456E+05
    0.2432039069E+08
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.1413421888E+05
    0.3360532386E+07
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.2299000000E+02
Element
Na
Bond Pattern
null 
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
Na        
Na        
Na        
Na        
Atom Type Number
           5
Nonbond Coefficients
   -0.3147397506E+06
    0.3167037521E+09
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1599900000E+02
Element
 O
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
OW        
OW        
OW        
OW        
Atom Type Number
           6
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1007900000E+01
Element
 H
Bond Pattern
s    
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
HW        
HW        
HW        
HW        
Atom Type Number
           7
Nonbond Coefficients
   -0.2099627771E+06
    0.2285148097E+09
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.6778738883E+05
    0.3249245720E+08
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.6781639996E+05
    0.3312572359E+08
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1201100000E+02
Element
 C
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
Cc        
Cc        
Cc        
Cc        
Atom Type Number
           8
Nonbond Coefficients
   -0.2305455883E+05
    0.4465856153E+07
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
   -0.1276489390E+04
    0.4123060730E+05
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1007900000E+01
Element
 H
Bond Pattern
s    
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
Hc        
Hc        
Hc        
Hc        
Atom Type Number
           9
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1007900000E+01
Element
 H
Bond Pattern
s    
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
CatlowFaux
Atom Names
HZ        
HZ        
HZ        
HZ        
Number of Bonded Terms
           4
Bond Type Number
           1
Bond Style
           1
Bond Coefficients
    0.1000000000E+01
Vibration Order
wild      
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           1
Atom Names
OW         HW        
Bond Type Number
           2
Bond Style
           7
Bond Coefficients
Vibration Order
wild      
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           2
Atom Names
OZ         Al        
OZ         Si        
Bond Type Number
           3
Bond Style
           2
Bond Coefficients
    0.1405700000E+01
    0.3481334700E+06
Vibration Order
wild      
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           1
Atom Names
Cc         Cc        
Bond Type Number
           4
Bond Style
           2
Bond Coefficients
    0.1054000000E+01
    0.1798689595E+06
Vibration Order
wild      
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           1
Atom Names
Cc         Hc        
Number of Angle Terms
           4
Angle Type Number
           1
Angle Style
           6
Angle Coefficients
Angle Order
wild           
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           3
Atom Names
Al         OZ         Al        
Al         OZ         Si        
Si         OZ         Si        
Angle Type Number
           2
Angle Style
           7
Angle Coefficients
    0.1094700000E+03
    0.2658289186E+05
Angle Order
wild           
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           2
Atom Names
OZ         Al         OZ        
OZ         Si         OZ        
Angle Type Number
           3
Angle Style
           1
Angle Coefficients
    0.1094700000E+03
    0.1966954106E+05
Angle Order
wild           
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           3
Atom Names
Cc         Cc         Cc        
Hc         Cc         Cc        
Hc         Cc         Hc        
Angle Type Number
           4
Angle Style
           0
Angle Coefficients
    0.1094700000E+03
    0.1000000000E-04
Angle Order
wild           
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           1
Atom Names
HW         OW         HW        
Number of Torsion Terms
           2
Torsion Type Number
           1
Torsion Style
           8
One-Four Nonbond Logical
 T
One-Four Coulombic Scaling
    0.0000000000E+00
Torsion Coefficients
Torsion Order
wild           
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           1
Atom Names
wild       Cc         Cc         wild      
Torsion Type Number
           2
Torsion Style
           8
One-Four Nonbond Logical
 T
One-Four Coulombic Scaling
    0.1000000000E+01
Torsion Coefficients
Torsion Order
wild           
Force Field Name
CatlowFaux
Number of Atoms with Same Parameters  
           2
Atom Names
wild       OZ         Al         wild      
wild       OZ         Si         wild      
Number of Improper Terms
           0
Number of Angle-Angle Terms
           0
Number of One-Five Types
           0
Number of Bond Increments
           0
~~~

Dubb2004 Force Field
======

~~~
towhee_ff Version
          15
Number of Nonbonded Types
           9
Potential Type
Lennard-Jones                 
Classical Mixrule
Explicit                      
Atom Type Number
           1
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3470000000E+01
    0.1150000000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3480000000E+01
    0.9300000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3580000000E+01
    0.6050000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3920000000E+01
    0.4000000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.4560000000E+01
    0.1000000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3400000000E+01
    0.2300000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1599900000E+02
Element
 O
Bond Pattern
ion  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
O         
O         
O         
O         
Atom Type Number
           2
Nonbond Coefficients
    0.3720000000E+01
    0.1585000000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3740000000E+01
    0.1308400000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3840000000E+01
    0.9421000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.4170000000E+01
    0.5191000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.4870000000E+01
    0.1126000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.2720000000E+01
    0.5821700000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1603260000E+02
Element
 C
Bond Pattern
ion  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
CH4       
CH4       
CH4       
CH4       
Atom Type Number
           3
Nonbond Coefficients
    0.3760000000E+01
    0.1080000000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.3860000000E+01
    0.7777000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.4190000000E+01
    0.4285000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.4900000000E+01
    0.9300000000E+01
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.2650000000E+01
    0.4437300000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1502470000E+02
Element
 C
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
CH3       
Csp3      
Csp3      
CH3       
Atom Type Number
           4
Nonbond Coefficients
    0.3960000000E+01
    0.5600000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.4300000000E+01
    0.3085000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.5030000000E+01
    0.6690000000E+01
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.2950000000E+01
    0.3100000000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1401680000E+02
Element
 C
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
CH2       
Csp3      
Csp3      
CH2       
Atom Type Number
           5
Nonbond Coefficients
    0.4670000000E+01
    0.1700000000E+02
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.5460000000E+01
    0.3690000000E+01
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1300890000E+02
Element
 C
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
CH        
Csp3      
Csp3      
CH        
Atom Type Number
           6
Nonbond Coefficients
    0.6380000000E+01
    0.8000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.1200100000E+02
Element
 C
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
C         
Csp3      
Csp3      
C         
Atom Type Number
           7
Nonbond Coefficients
    0.2160000000E+01
    0.1244000000E+03
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.2299000000E+02
Element
Na
Bond Pattern
ion  
Base Charge 
    0.1000000000E+01
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
Na        
Na        
Na        
Na        
Atom Type Number
           8
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.2698200000E+02
Element
Al
Bond Pattern
sp3  
Base Charge 
   -0.1000000000E+01
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
Al        
Al        
Al        
Al        
Atom Type Number
           9
Nonbond Coefficients
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
    0.0000000000E+00
Mass
    0.2808600000E+02
Element
Si
Bond Pattern
sp3  
Base Charge 
    0.0000000000E+00
Polarizability
    0.1000000000E+01
Force Field Name
Dubb2004  
Atom Names
Si        
Si        
Si        
Si        
Number of Bonded Terms
           2
Bond Type Number
           1
Bond Style
           2
Bond Coefficients
    0.1540000000E+01
    0.4825000000E+05
Vibration Order
wild      
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           1
Atom Names
Csp3       Csp3      
Bond Type Number
           2
Bond Style
           8
Bond Coefficients
Vibration Order
wild      
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           2
Atom Names
Al         O         
Si         O         
Number of Angle Terms
           2
Angle Type Number
           1
Angle Style
           3
Angle Coefficients
    0.1140000000E+03
    0.3125000000E+05
Angle Order
wild           
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           1
Atom Names
Csp3       Csp3       Csp3      
Angle Type Number
           2
Angle Style
          11
Angle Coefficients
Angle Order
wild           
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           4
Atom Names
Si         O          Si        
Si         O          Al        
O          Si         O         
O          Al         O         
Number of Torsion Terms
           5
Torsion Type Number
           1
Torsion Style
          10
One-Four Nonbond Logical
 F
Number of Torsion Loops
           5
Torsion Coefficients
    0.1204654000E+04
    0.1947740000E+04
   -0.3578450000E+03
   -0.1944666000E+04
    0.7156900000E+03
   -0.1565572000E+04
Torsion Order
wild           
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           1
Atom Names
Cwild      CH2        CH2        Cwild     
Torsion Type Number
           2
Torsion Style
          10
One-Four Nonbond Logical
 F
Number of Torsion Loops
           3
Torsion Coefficients
    0.1293324000E+04
    0.3879849000E+04
    0.0000000000E+00
   -0.5173163000E+04
Torsion Order
wild           
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           1
Atom Names
Cwild      C          CH2        Cwild     
Torsion Type Number
           3
Torsion Style
          10
One-Four Nonbond Logical
 F
Number of Torsion Loops
           3
Torsion Coefficients
    0.2045657000E+04
    0.6136797000E+04
    0.0000000000E+00
   -0.8182447000E+04
Torsion Order
wild           
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           1
Atom Names
Cwild      C          C          Cwild     
Torsion Type Number
           4
Torsion Style
          11
One-Four Nonbond Logical
 T
One-Four Coulombic Scaling
    0.5000000000E+00
Torsion Coefficients
   -0.2510600000E+03
    0.4287300000E+03
   -0.1118500000E+03
    0.4412700000E+03
Torsion Order
wild           
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           2
Atom Names
Cwild      CH         CH2        Cwild     
Cwild      CH         CH         Cwild     
Torsion Type Number
           5
Torsion Style
           8
One-Four Nonbond Logical
 F
Torsion Coefficients
Torsion Order
wild           
Force Field Name
Dubb2004  
Number of Atoms with Same Parameters  
           2
Atom Names
wild       Al         O          wild      
wild       Si         O          wild      
Number of Improper Terms
           0
Number of Angle-Angle Terms
           0
Number of One-Five Types
           0
Number of Bond Increments
           3
Bond Increment Type Number
           1
Bond Increment Value
    0.5125000000E+00
Bond Increment Order
wild      
Force Field Name
Dubb2004  
Atom Names
Si         O         
Bond Increment Type Number
           2
Bond Increment Value
    0.6875000000E+00
Bond Increment Order
wild      
Force Field Name
Dubb2004  
Atom Names
Al         O         
Bond Increment Type Number
           3
Bond Increment Value
    0.0000000000E+00
Bond Increment Order
wild      
Force Field Name
Dubb2004  
Atom Names
Csp3       Csp3      
~~~
