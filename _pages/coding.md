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

Catlow/faux towhee Input file:
======


<br/><img src='/images/zeolite.png'>


~~~
ensemble
'npt'
temperature
300.0d0
pressure
500.0d0
nmolty
3
nmolectyp
1 96 200
numboxes
2
stepstyle
'cycles'
nstep
1
printfreq
1   
blocksize
2000
moviefreq
100000
backupfreq
1000
runoutput
'full'
pdb_output_freq
1
pressure_virial_freq
20
trmaxdispfreq
1000
volmaxdispfreq
1000
linit   
.false. 
initboxtype
'dimensions'
initstyle
'coords' 'coords' 'none'
'none' 'none' 'full cbmc'
initlattice
'none' 'none' 'simple cubic'
'none' 'none' 'simple cubic'
initmol
1 96 0
0 0 200
inix iniy iniz
10   10   1
6    6    6
hmatrix
24.555d0 0.0d0 0.0d0 
0.0d0 24.555d0 0.0d0
0.0d0 0.0d0 24.555d0
70.0 0.0d0 0.0d0
0.0d0 70.0 0.0d0
0.0d0 0.0d0 70.0
pmvol     
0.005d0   
          pmvlpr
          0.0d0 1.0d0
          rmvol
          0.1d0
          tavol
          0.5d0
pm2boxcbswap
0.05d0
          pm2cbswmt
          0.0d0 0.0d0 1.0d0
          pm2cbswpr
          1.0d0
pm1boxcbswap
0.10d0
          pm1cbswmt
          0.0d0 0.0d0 1.0d0
pmcb
0.33d0
          pmcbmt
          0.0d0 0.0d0 1.0d0 
          pmall
          0.0d0 0.0d0 0.0d0
pmtraat
0.335d0
          pmtamt
          1.0d0 0.0d0 0.0d0
          rmtraa
          0.5d0 
          tatraa
          0.5d0
pmtracm
0.67d0
          pmtcmt
          0.0d0 0.0 1.0d0      	
          rmtrac
          0.5d0 
          tatrac
          0.5d0
pmrotate
1.0d0
          pmromt  
          0.0d0 0.0d0 1.0d0
          rmrot
          0.05d0
          tarot
          0.5d0
cbmc_formulation
'Martin and Siepmann 1999 + Martin and Thompson 2004'
cbmc_setting_style
'explicit'
cbmc_nb_one_generation
'uniform' 'uniform' 'uniform'
'uniform' 'uniform' 'uniform'
nch_nb_one
1 1 10
nch_nb
1 1 10
cbmc_dihedral_generation
'ideal'
nch_tor
1 1 100
nch_tor_connect
1 1 100
cbmc_bend_generation
'ideal'
nch_bend_a
1 1 1000
nch_bend_b
1 1 1000
cbmc_bond_generation
'r^2 with bounds'
vibrang
0.85 1.15	
nch_vib
1 1 1000
two_bond_fixed_endpoint_bias_style
'analytic Boltzmann dihedral energy sum'
three_bond_fixed_endpoint_bias_style
'analytic using max and min 2-4 distance'
ffnumber
1
ff_filename
/towheebase/ForceFields/towhee_ff_CatlowFaux
classical_potential
'Exponential-12-6'       
classical_mixrule
'Explicit'
lshift
.true.
ltailc
.false.
rmin  
0.5d0 
rcut  
12.0d0
rcutin 
6.0d0 
electrostatic_form
'coulomb'
coulombstyle
'ewald_fixed_kmax'
kalp 
5.6d0
kmax
5
dielect
1.0d0
input_style
'basic connectivity map'
nunit
576
nmaxcbmc
576
lpdbnames
F
forcefield
'CatlowFaux'
charge_assignment
'manual'
unit ntype qqatom
 1 'OZ    '  -1.86875
vibration
 2
 389 524
improper torsion
 0
unit ntype qqatom
 2 'OZ    '  -1.86875
vibration
 2
 421 494
improper torsion
 0
unit ntype qqatom
 3 'OZ    '  -1.86875
vibration
 2
 451 557
improper torsion
 0
unit ntype qqatom
 4 'OZ    '  -1.86875
vibration
 2
 454 556
improper torsion
 0
unit ntype qqatom
 5 'OZ    '  -1.86875
vibration
 2
 408 514
improper torsion
 0
unit ntype qqatom
 6 'OZ    '  -1.86875
vibration
 2
 410 513
improper torsion
 0
unit ntype qqatom
 7 'OZ    '  -1.86875
vibration
 2
 450 505
improper torsion
 0
unit ntype qqatom
 8 'OZ    '  -1.86875
vibration
 2
 402 554
improper torsion
 0
unit ntype qqatom
 9 'OZ    '  -1.86875
vibration
 2
 459 524
improper torsion
 0
unit ntype qqatom
 10 'OZ    '  -1.86875
vibration
 2
 421 563
improper torsion
 0
unit ntype qqatom
 11 'OZ    '  -1.86875
vibration
 2
 451 497
improper torsion
 0
unit ntype qqatom
 12 'OZ    '  -1.86875
vibration
 2
 394 556
improper torsion
 0
unit ntype qqatom
 13 'OZ    '  -1.86875
vibration
 2
 408 501
improper torsion
 0
unit ntype qqatom
 14 'OZ    '  -1.86875
vibration
 2
 398 513
improper torsion
 0
unit ntype qqatom
 15 'OZ    '  -1.86875
vibration
 2
 460 505
improper torsion
 0
unit ntype qqatom
 16 'OZ    '  -1.86875
vibration
 2
 402 565
improper torsion
 0
unit ntype qqatom
 17 'OZ    '  -1.86875
vibration
 2
 387 524
improper torsion
 0
unit ntype qqatom
 18 'OZ    '  -1.86875
vibration
 2
 421 492
improper torsion
 0
unit ntype qqatom
 19 'OZ    '  -1.86875
vibration
 2
 451 540
improper torsion
 0
unit ntype qqatom
 20 'OZ    '  -1.86875
vibration
 2
 436 556
improper torsion
 0
unit ntype qqatom
 21 'OZ    '  -1.86875
vibration
 2
 408 548
improper torsion
 0
unit ntype qqatom
 22 'OZ    '  -1.86875
vibration
 2
 445 513
improper torsion
 0
unit ntype qqatom
 23 'OZ    '  -1.86875
vibration
 2
 428 505
improper torsion
 0
unit ntype qqatom
 24 'OZ    '  -1.86875
vibration
 2
 402 533
improper torsion
 0
unit ntype qqatom
 25 'OZ    '  -1.86875
vibration
 2
 459 491
improper torsion
 0
unit ntype qqatom
 26 'OZ    '  -1.86875
vibration
 2
 388 563
improper torsion
 0
unit ntype qqatom
 27 'OZ    '  -1.86875
vibration
 2
 467 497
improper torsion
 0
unit ntype qqatom
 28 'OZ    '  -1.86875
vibration
 2
 394 572
improper torsion
 0
unit ntype qqatom
 29 'OZ    '  -1.86875
vibration
 2
 415 501
improper torsion
 0
unit ntype qqatom
 30 'OZ    '  -1.86875
vibration
 2
 398 520
improper torsion
 0
unit ntype qqatom
 31 'OZ    '  -1.86875
vibration
 2
 460 564
improper torsion
 0
unit ntype qqatom
 32 'OZ    '  -1.86875
vibration
 2
 461 565
improper torsion
 0
unit ntype qqatom
 33 'OZ    '  -1.86875
vibration
 2
 459 515
improper torsion
 0
unit ntype qqatom
 34 'OZ    '  -1.86875
vibration
 2
 412 563
improper torsion
 0
unit ntype qqatom
 35 'OZ    '  -1.86875
vibration
 2
 399 497
improper torsion
 0
unit ntype qqatom
 36 'OZ    '  -1.86875
vibration
 2
 394 504
improper torsion
 0
unit ntype qqatom
 37 'OZ    '  -1.86875
vibration
 2
 444 501
improper torsion
 0
unit ntype qqatom
 38 'OZ    '  -1.86875
vibration
 2
 398 549
improper torsion
 0
unit ntype qqatom
 39 'OZ    '  -1.86875
vibration
 2
 460 568
improper torsion
 0
unit ntype qqatom
 40 'OZ    '  -1.86875
vibration
 2
 465 565
improper torsion
 0
unit ntype qqatom
 41 'OZ    '  -1.86875
vibration
 2
 391 515
improper torsion
 0
unit ntype qqatom
 42 'OZ    '  -1.86875
vibration
 2
 412 496
improper torsion
 0
unit ntype qqatom
 43 'OZ    '  -1.86875
vibration
 2
 399 561
improper torsion
 0
unit ntype qqatom
 44 'OZ    '  -1.86875
vibration
 2
 458 504
improper torsion
 0
unit ntype qqatom
 45 'OZ    '  -1.86875
vibration
 2
 444 512
improper torsion
 0
unit ntype qqatom
 46 'OZ    '  -1.86875
vibration
 2
 409 549
improper torsion
 0
unit ntype qqatom
 47 'OZ    '  -1.86875
vibration
 2
 448 568
improper torsion
 0
unit ntype qqatom
 48 'OZ    '  -1.86875
vibration
 2
 465 553
improper torsion
 0
unit ntype qqatom
 49 'OZ    '  -1.86875
vibration
 2
 387 515
improper torsion
 0
unit ntype qqatom
 50 'OZ    '  -1.86875
vibration
 2
 412 492
improper torsion
 0
unit ntype qqatom
 51 'OZ    '  -1.86875
vibration
 2
 399 540
improper torsion
 0
unit ntype qqatom
 52 'OZ    '  -1.86875
vibration
 2
 436 504
improper torsion
 0
unit ntype qqatom
 53 'OZ    '  -1.86875
vibration
 2
 444 548
improper torsion
 0
unit ntype qqatom
 54 'OZ    '  -1.86875
vibration
 2
 445 549
improper torsion
 0
unit ntype qqatom
 55 'OZ    '  -1.86875
vibration
 2
 428 568
improper torsion
 0
unit ntype qqatom
 56 'OZ    '  -1.86875
vibration
 2
 465 533
improper torsion
 0
unit ntype qqatom
 57 'OZ    '  -1.86875
vibration
 2
 387 485
improper torsion
 0
unit ntype qqatom
 58 'OZ    '  -1.86875
vibration
 2
 478 492
improper torsion
 0
unit ntype qqatom
 59 'OZ    '  -1.86875
vibration
 2
 476 540
improper torsion
 0
unit ntype qqatom
 60 'OZ    '  -1.86875
vibration
 2
 436 483
improper torsion
 0
unit ntype qqatom
 61 'OZ    '  -1.86875
vibration
 2
 420 548
improper torsion
 0
unit ntype qqatom
 62 'OZ    '  -1.86875
vibration
 2
 445 525
improper torsion
 0
unit ntype qqatom
 63 'OZ    '  -1.86875
vibration
 2
 428 571
improper torsion
 0
unit ntype qqatom
 64 'OZ    '  -1.86875
vibration
 2
 468 533
improper torsion
 0
unit ntype qqatom
 65 'OZ    '  -1.86875
vibration
 2
 389 530
improper torsion
 0
unit ntype qqatom
 66 'OZ    '  -1.86875
vibration
 2
 427 494
improper torsion
 0
unit ntype qqatom
 67 'OZ    '  -1.86875
vibration
 2
 422 557
improper torsion
 0
unit ntype qqatom
 68 'OZ    '  -1.86875
vibration
 2
 454 527
improper torsion
 0
unit ntype qqatom
 69 'OZ    '  -1.86875
vibration
 2
 393 514
improper torsion
 0
unit ntype qqatom
 70 'OZ    '  -1.86875
vibration
 2
 410 498
improper torsion
 0
unit ntype qqatom
 71 'OZ    '  -1.86875
vibration
 2
 450 573
improper torsion
 0
unit ntype qqatom
 72 'OZ    '  -1.86875
vibration
 2
 470 554
improper torsion
 0
unit ntype qqatom
 73 'OZ    '  -1.86875
vibration
 2
 389 532
improper torsion
 0
unit ntype qqatom
 74 'OZ    '  -1.86875
vibration
 2
 429 494
improper torsion
 0
unit ntype qqatom
 75 'OZ    '  -1.86875
vibration
 2
 437 557
improper torsion
 0
unit ntype qqatom
 76 'OZ    '  -1.86875
vibration
 2
 454 542
improper torsion
 0
unit ntype qqatom
 77 'OZ    '  -1.86875
vibration
 2
 442 514
improper torsion
 0
unit ntype qqatom
 78 'OZ    '  -1.86875
vibration
 2
 410 547
improper torsion
 0
unit ntype qqatom
 79 'OZ    '  -1.86875
vibration
 2
 450 521
improper torsion
 0
unit ntype qqatom
 80 'OZ    '  -1.86875
vibration
 2
 418 554
improper torsion
 0
unit ntype qqatom
 81 'OZ    '  -1.86875
vibration
 2
 469 491
improper torsion
 0
unit ntype qqatom
 82 'OZ    '  -1.86875
vibration
 2
 388 574
improper torsion
 0
unit ntype qqatom
 83 'OZ    '  -1.86875
vibration
 2
 467 546
improper torsion
 0
unit ntype qqatom
 84 'OZ    '  -1.86875
vibration
 2
 443 572
improper torsion
 0
unit ntype qqatom
 85 'OZ    '  -1.86875
vibration
 2
 415 493
improper torsion
 0
unit ntype qqatom
 86 'OZ    '  -1.86875
vibration
 2
 390 520
improper torsion
 0
unit ntype qqatom
 87 'OZ    '  -1.86875
vibration
 2
 424 564
improper torsion
 0
unit ntype qqatom
 88 'OZ    '  -1.86875
vibration
 2
 461 529
improper torsion
 0
unit ntype qqatom
 89 'OZ    '  -1.86875
vibration
 2
 401 491
improper torsion
 0
unit ntype qqatom
 90 'OZ    '  -1.86875
vibration
 2
 388 506
improper torsion
 0
unit ntype qqatom
 91 'OZ    '  -1.86875
vibration
 2
 467 489
improper torsion
 0
unit ntype qqatom
 92 'OZ    '  -1.86875
vibration
 2
 386 572
improper torsion
 0
unit ntype qqatom
 93 'OZ    '  -1.86875
vibration
 2
 415 559
improper torsion
 0
unit ntype qqatom
 94 'OZ    '  -1.86875
vibration
 2
 456 520
improper torsion
 0
unit ntype qqatom
 95 'OZ    '  -1.86875
vibration
 2
 471 564
improper torsion
 0
unit ntype qqatom
 96 'OZ    '  -1.86875
vibration
 2
 461 576
improper torsion
 0
unit ntype qqatom
 97 'OZ    '  -1.86875
vibration
 2
 391 534
improper torsion
 0
unit ntype qqatom
 98 'OZ    '  -1.86875
vibration
 2
 431 496
improper torsion
 0
unit ntype qqatom
 99 'OZ    '  -1.86875
vibration
 2
 417 561
improper torsion
 0
unit ntype qqatom
 100 'OZ    '  -1.86875
vibration
 2
 458 522
improper torsion
 0
unit ntype qqatom
 101 'OZ    '  -1.86875
vibration
 2
 397 512
improper torsion
 0
unit ntype qqatom
 102 'OZ    '  -1.86875
vibration
 2
 409 502
improper torsion
 0
unit ntype qqatom
 103 'OZ    '  -1.86875
vibration
 2
 448 566
improper torsion
 0
unit ntype qqatom
 104 'OZ    '  -1.86875
vibration
 2
 463 553
improper torsion
 0
unit ntype qqatom
 105 'OZ    '  -1.86875
vibration
 2
 391 536
improper torsion
 0
unit ntype qqatom
 106 'OZ    '  -1.86875
vibration
 2
 433 496
improper torsion
 0
unit ntype qqatom
 107 'OZ    '  -1.86875
vibration
 2
 439 561
improper torsion
 0
unit ntype qqatom
 108 'OZ    '  -1.86875
vibration
 2
 458 543
improper torsion
 0
unit ntype qqatom
 109 'OZ    '  -1.86875
vibration
 2
 440 512
improper torsion
 0
unit ntype qqatom
 110 'OZ    '  -1.86875
vibration
 2
 409 545
improper torsion
 0
unit ntype qqatom
 111 'OZ    '  -1.86875
vibration
 2
 448 519
improper torsion
 0
unit ntype qqatom
 112 'OZ    '  -1.86875
vibration
 2
 416 553
improper torsion
 0
unit ntype qqatom
 113 'OZ    '  -1.86875
vibration
 2
 476 484
improper torsion
 0
unit ntype qqatom
 114 'OZ    '  -1.86875
vibration
 2
 479 483
improper torsion
 0
unit ntype qqatom
 115 'OZ    '  -1.86875
vibration
 2
 403 485
improper torsion
 0
unit ntype qqatom
 116 'OZ    '  -1.86875
vibration
 2
 478 508
improper torsion
 0
unit ntype qqatom
 117 'OZ    '  -1.86875
vibration
 2
 420 555
improper torsion
 0
unit ntype qqatom
 118 'OZ    '  -1.86875
vibration
 2
 452 525
improper torsion
 0
unit ntype qqatom
 119 'OZ    '  -1.86875
vibration
 2
 474 571
improper torsion
 0
unit ntype qqatom
 120 'OZ    '  -1.86875
vibration
 2
 468 481
improper torsion
 0
unit ntype qqatom
 121 'OZ    '  -1.86875
vibration
 2
 475 485
improper torsion
 0
unit ntype qqatom
 122 'OZ    '  -1.86875
vibration
 2
 478 488
improper torsion
 0
unit ntype qqatom
 123 'OZ    '  -1.86875
vibration
 2
 476 550
improper torsion
 0
unit ntype qqatom
 124 'OZ    '  -1.86875
vibration
 2
 447 483
improper torsion
 0
unit ntype qqatom
 125 'OZ    '  -1.86875
vibration
 2
 420 486
improper torsion
 0
unit ntype qqatom
 126 'OZ    '  -1.86875
vibration
 2
 480 525
improper torsion
 0
unit ntype qqatom
 127 'OZ    '  -1.86875
vibration
 2
 430 571
improper torsion
 0
unit ntype qqatom
 128 'OZ    '  -1.86875
vibration
 2
 468 535
improper torsion
 0
unit ntype qqatom
 129 'OZ    '  -1.86875
vibration
 2
 469 530
improper torsion
 0
unit ntype qqatom
 130 'OZ    '  -1.86875
vibration
 2
 427 574
improper torsion
 0
unit ntype qqatom
 131 'OZ    '  -1.86875
vibration
 2
 422 546
improper torsion
 0
unit ntype qqatom
 132 'OZ    '  -1.86875
vibration
 2
 443 527
improper torsion
 0
unit ntype qqatom
 133 'OZ    '  -1.86875
vibration
 2
 393 493
improper torsion
 0
unit ntype qqatom
 134 'OZ    '  -1.86875
vibration
 2
 390 498
improper torsion
 0
unit ntype qqatom
 135 'OZ    '  -1.86875
vibration
 2
 424 573
improper torsion
 0
unit ntype qqatom
 136 'OZ    '  -1.86875
vibration
 2
 470 529
improper torsion
 0
unit ntype qqatom
 137 'OZ    '  -1.86875
vibration
 2
 401 534
improper torsion
 0
unit ntype qqatom
 138 'OZ    '  -1.86875
vibration
 2
 431 506
improper torsion
 0
unit ntype qqatom
 139 'OZ    '  -1.86875
vibration
 2
 417 489
improper torsion
 0
unit ntype qqatom
 140 'OZ    '  -1.86875
vibration
 2
 386 522
improper torsion
 0
unit ntype qqatom
 141 'OZ    '  -1.86875
vibration
 2
 397 559
improper torsion
 0
unit ntype qqatom
 142 'OZ    '  -1.86875
vibration
 2
 456 502
improper torsion
 0
unit ntype qqatom
 143 'OZ    '  -1.86875
vibration
 2
 471 566
improper torsion
 0
unit ntype qqatom
 144 'OZ    '  -1.86875
vibration
 2
 463 576
improper torsion
 0
unit ntype qqatom
 145 'OZ    '  -1.86875
vibration
 2
 403 536
improper torsion
 0
unit ntype qqatom
 146 'OZ    '  -1.86875
vibration
 2
 433 508
improper torsion
 0
unit ntype qqatom
 147 'OZ    '  -1.86875
vibration
 2
 439 484
improper torsion
 0
unit ntype qqatom
 148 'OZ    '  -1.86875
vibration
 2
 479 543
improper torsion
 0
unit ntype qqatom
 149 'OZ    '  -1.86875
vibration
 2
 440 555
improper torsion
 0
unit ntype qqatom
 150 'OZ    '  -1.86875
vibration
 2
 452 545
improper torsion
 0
unit ntype qqatom
 151 'OZ    '  -1.86875
vibration
 2
 474 519
improper torsion
 0
unit ntype qqatom
 152 'OZ    '  -1.86875
vibration
 2
 416 481
improper torsion
 0
unit ntype qqatom
 153 'OZ    '  -1.86875
vibration
 2
 475 532
improper torsion
 0
unit ntype qqatom
 154 'OZ    '  -1.86875
vibration
 2
 429 488
improper torsion
 0
unit ntype qqatom
 155 'OZ    '  -1.86875
vibration
 2
 437 550
improper torsion
 0
unit ntype qqatom
 156 'OZ    '  -1.86875
vibration
 2
 447 542
improper torsion
 0
unit ntype qqatom
 157 'OZ    '  -1.86875
vibration
 2
 442 486
improper torsion
 0
unit ntype qqatom
 158 'OZ    '  -1.86875
vibration
 2
 480 547
improper torsion
 0
unit ntype qqatom
 159 'OZ    '  -1.86875
vibration
 2
 430 521
improper torsion
 0
unit ntype qqatom
 160 'OZ    '  -1.86875
vibration
 2
 418 535
improper torsion
 0
unit ntype qqatom
 161 'OZ    '  -1.86875
vibration
 2
 457 530
improper torsion
 0
unit ntype qqatom
 162 'OZ    '  -1.86875
vibration
 2
 427 562
improper torsion
 0
unit ntype qqatom
 163 'OZ    '  -1.86875
vibration
 2
 422 509
improper torsion
 0
unit ntype qqatom
 164 'OZ    '  -1.86875
vibration
 2
 405 527
improper torsion
 0
unit ntype qqatom
 165 'OZ    '  -1.86875
vibration
 2
 393 526
improper torsion
 0
unit ntype qqatom
 166 'OZ    '  -1.86875
vibration
 2
 423 498
improper torsion
 0
unit ntype qqatom
 167 'OZ    '  -1.86875
vibration
 2
 432 573
improper torsion
 0
unit ntype qqatom
 168 'OZ    '  -1.86875
vibration
 2
 470 537
improper torsion
 0
unit ntype qqatom
 169 'OZ    '  -1.86875
vibration
 2
 457 532
improper torsion
 0
unit ntype qqatom
 170 'OZ    '  -1.86875
vibration
 2
 429 562
improper torsion
 0
unit ntype qqatom
 171 'OZ    '  -1.86875
vibration
 2
 437 509
improper torsion
 0
unit ntype qqatom
 172 'OZ    '  -1.86875
vibration
 2
 405 542
improper torsion
 0
unit ntype qqatom
 173 'OZ    '  -1.86875
vibration
 2
 442 526
improper torsion
 0
unit ntype qqatom
 174 'OZ    '  -1.86875
vibration
 2
 423 547
improper torsion
 0
unit ntype qqatom
 175 'OZ    '  -1.86875
vibration
 2
 432 521
improper torsion
 0
unit ntype qqatom
 176 'OZ    '  -1.86875
vibration
 2
 418 537
improper torsion
 0
unit ntype qqatom
 177 'OZ    '  -1.86875
vibration
 2
 469 541
improper torsion
 0
unit ntype qqatom
 178 'OZ    '  -1.86875
vibration
 2
 438 574
improper torsion
 0
unit ntype qqatom
 179 'OZ    '  -1.86875
vibration
 2
 406 546
improper torsion
 0
unit ntype qqatom
 180 'OZ    '  -1.86875
vibration
 2
 443 511
improper torsion
 0
unit ntype qqatom
 181 'OZ    '  -1.86875
vibration
 2
 466 493
improper torsion
 0
unit ntype qqatom
 182 'OZ    '  -1.86875
vibration
 2
 390 570
improper torsion
 0
unit ntype qqatom
 183 'OZ    '  -1.86875
vibration
 2
 424 495
improper torsion
 0
unit ntype qqatom
 184 'OZ    '  -1.86875
vibration
 2
 392 529
improper torsion
 0
unit ntype qqatom
 185 'OZ    '  -1.86875
vibration
 2
 401 541
improper torsion
 0
unit ntype qqatom
 186 'OZ    '  -1.86875
vibration
 2
 438 506
improper torsion
 0
unit ntype qqatom
 187 'OZ    '  -1.86875
vibration
 2
 406 489
improper torsion
 0
unit ntype qqatom
 188 'OZ    '  -1.86875
vibration
 2
 386 511
improper torsion
 0
unit ntype qqatom
 189 'OZ    '  -1.86875
vibration
 2
 466 559
improper torsion
 0
unit ntype qqatom
 190 'OZ    '  -1.86875
vibration
 2
 456 570
improper torsion
 0
unit ntype qqatom
 191 'OZ    '  -1.86875
vibration
 2
 471 495
improper torsion
 0
unit ntype qqatom
 192 'OZ    '  -1.86875
vibration
 2
 392 576
improper torsion
 0
unit ntype qqatom
 193 'OZ    '  -1.86875
vibration
 2
 455 534
improper torsion
 0
unit ntype qqatom
 194 'OZ    '  -1.86875
vibration
 2
 431 560
improper torsion
 0
unit ntype qqatom
 195 'OZ    '  -1.86875
vibration
 2
 417 510
improper torsion
 0
unit ntype qqatom
 196 'OZ    '  -1.86875
vibration
 2
 407 522
improper torsion
 0
unit ntype qqatom
 197 'OZ    '  -1.86875
vibration
 2
 397 538
improper torsion
 0
unit ntype qqatom
 198 'OZ    '  -1.86875
vibration
 2
 435 502
improper torsion
 0
unit ntype qqatom
 199 'OZ    '  -1.86875
vibration
 2
 426 566
improper torsion
 0
unit ntype qqatom
 200 'OZ    '  -1.86875
vibration
 2
 463 531
improper torsion
 0
unit ntype qqatom
 201 'OZ    '  -1.86875
vibration
 2
 455 536
improper torsion
 0
unit ntype qqatom
 202 'OZ    '  -1.86875
vibration
 2
 433 560
improper torsion
 0
unit ntype qqatom
 203 'OZ    '  -1.86875
vibration
 2
 439 510
improper torsion
 0
unit ntype qqatom
 204 'OZ    '  -1.86875
vibration
 2
 407 543
improper torsion
 0
unit ntype qqatom
 205 'OZ    '  -1.86875
vibration
 2
 440 538
improper torsion
 0
unit ntype qqatom
 206 'OZ    '  -1.86875
vibration
 2
 435 545
improper torsion
 0
unit ntype qqatom
 207 'OZ    '  -1.86875
vibration
 2
 426 519
improper torsion
 0
unit ntype qqatom
 208 'OZ    '  -1.86875
vibration
 2
 416 531
improper torsion
 0
unit ntype qqatom
 209 'OZ    '  -1.86875
vibration
 2
 403 544
improper torsion
 0
unit ntype qqatom
 210 'OZ    '  -1.86875
vibration
 2
 441 508
improper torsion
 0
unit ntype qqatom
 211 'OZ    '  -1.86875
vibration
 2
 411 484
improper torsion
 0
unit ntype qqatom
 212 'OZ    '  -1.86875
vibration
 2
 479 516
improper torsion
 0
unit ntype qqatom
 213 'OZ    '  -1.86875
vibration
 2
 474 487
improper torsion
 0
unit ntype qqatom
 214 'OZ    '  -1.86875
vibration
 2
 473 481
improper torsion
 0
unit ntype qqatom
 215 'OZ    '  -1.86875
vibration
 2
 477 555
improper torsion
 0
unit ntype qqatom
 216 'OZ    '  -1.86875
vibration
 2
 452 482
improper torsion
 0
unit ntype qqatom
 217 'OZ    '  -1.86875
vibration
 2
 475 544
improper torsion
 0
unit ntype qqatom
 218 'OZ    '  -1.86875
vibration
 2
 441 488
improper torsion
 0
unit ntype qqatom
 219 'OZ    '  -1.86875
vibration
 2
 411 550
improper torsion
 0
unit ntype qqatom
 220 'OZ    '  -1.86875
vibration
 2
 447 516
improper torsion
 0
unit ntype qqatom
 221 'OZ    '  -1.86875
vibration
 2
 477 486
improper torsion
 0
unit ntype qqatom
 222 'OZ    '  -1.86875
vibration
 2
 480 482
improper torsion
 0
unit ntype qqatom
 223 'OZ    '  -1.86875
vibration
 2
 430 487
improper torsion
 0
unit ntype qqatom
 224 'OZ    '  -1.86875
vibration
 2
 473 535
improper torsion
 0
unit ntype qqatom
 225 'OZ    '  -1.86875
vibration
 2
 457 523
improper torsion
 0
unit ntype qqatom
 226 'OZ    '  -1.86875
vibration
 2
 419 562
improper torsion
 0
unit ntype qqatom
 227 'OZ    '  -1.86875
vibration
 2
 453 509
improper torsion
 0
unit ntype qqatom
 228 'OZ    '  -1.86875
vibration
 2
 405 558
improper torsion
 0
unit ntype qqatom
 229 'OZ    '  -1.86875
vibration
 2
 413 526
improper torsion
 0
unit ntype qqatom
 230 'OZ    '  -1.86875
vibration
 2
 423 518
improper torsion
 0
unit ntype qqatom
 231 'OZ    '  -1.86875
vibration
 2
 432 507
improper torsion
 0
unit ntype qqatom
 232 'OZ    '  -1.86875
vibration
 2
 404 537
improper torsion
 0
unit ntype qqatom
 233 'OZ    '  -1.86875
vibration
 2
 464 523
improper torsion
 0
unit ntype qqatom
 234 'OZ    '  -1.86875
vibration
 2
 419 569
improper torsion
 0
unit ntype qqatom
 235 'OZ    '  -1.86875
vibration
 2
 453 499
improper torsion
 0
unit ntype qqatom
 236 'OZ    '  -1.86875
vibration
 2
 396 558
improper torsion
 0
unit ntype qqatom
 237 'OZ    '  -1.86875
vibration
 2
 413 503
improper torsion
 0
unit ntype qqatom
 238 'OZ    '  -1.86875
vibration
 2
 400 518
improper torsion
 0
unit ntype qqatom
 239 'OZ    '  -1.86875
vibration
 2
 462 507
improper torsion
 0
unit ntype qqatom
 240 'OZ    '  -1.86875
vibration
 2
 404 567
improper torsion
 0
unit ntype qqatom
 241 'OZ    '  -1.86875
vibration
 2
 385 523
improper torsion
 0
unit ntype qqatom
 242 'OZ    '  -1.86875
vibration
 2
 419 490
improper torsion
 0
unit ntype qqatom
 243 'OZ    '  -1.86875
vibration
 2
 453 528
improper torsion
 0
unit ntype qqatom
 244 'OZ    '  -1.86875
vibration
 2
 425 558
improper torsion
 0
unit ntype qqatom
 245 'OZ    '  -1.86875
vibration
 2
 413 552
improper torsion
 0
unit ntype qqatom
 246 'OZ    '  -1.86875
vibration
 2
 449 518
improper torsion
 0
unit ntype qqatom
 247 'OZ    '  -1.86875
vibration
 2
 434 507
improper torsion
 0
unit ntype qqatom
 248 'OZ    '  -1.86875
vibration
 2
 404 539
improper torsion
 0
unit ntype qqatom
 249 'OZ    '  -1.86875
vibration
 2
 464 541
improper torsion
 0
unit ntype qqatom
 250 'OZ    '  -1.86875
vibration
 2
 438 569
improper torsion
 0
unit ntype qqatom
 251 'OZ    '  -1.86875
vibration
 2
 406 499
improper torsion
 0
unit ntype qqatom
 252 'OZ    '  -1.86875
vibration
 2
 396 511
improper torsion
 0
unit ntype qqatom
 253 'OZ    '  -1.86875
vibration
 2
 466 503
improper torsion
 0
unit ntype qqatom
 254 'OZ    '  -1.86875
vibration
 2
 400 570
improper torsion
 0
unit ntype qqatom
 255 'OZ    '  -1.86875
vibration
 2
 462 495
improper torsion
 0
unit ntype qqatom
 256 'OZ    '  -1.86875
vibration
 2
 392 567
improper torsion
 0
unit ntype qqatom
 257 'OZ    '  -1.86875
vibration
 2
 464 517
improper torsion
 0
unit ntype qqatom
 258 'OZ    '  -1.86875
vibration
 2
 414 569
improper torsion
 0
unit ntype qqatom
 259 'OZ    '  -1.86875
vibration
 2
 395 499
improper torsion
 0
unit ntype qqatom
 260 'OZ    '  -1.86875
vibration
 2
 396 500
improper torsion
 0
unit ntype qqatom
 261 'OZ    '  -1.86875
vibration
 2
 446 503
improper torsion
 0
unit ntype qqatom
 262 'OZ    '  -1.86875
vibration
 2
 400 551
improper torsion
 0
unit ntype qqatom
 263 'OZ    '  -1.86875
vibration
 2
 462 575
improper torsion
 0
unit ntype qqatom
 264 'OZ    '  -1.86875
vibration
 2
 472 567
improper torsion
 0
unit ntype qqatom
 265 'OZ    '  -1.86875
vibration
 2
 455 517
improper torsion
 0
unit ntype qqatom
 266 'OZ    '  -1.86875
vibration
 2
 414 560
improper torsion
 0
unit ntype qqatom
 267 'OZ    '  -1.86875
vibration
 2
 395 510
improper torsion
 0
unit ntype qqatom
 268 'OZ    '  -1.86875
vibration
 2
 407 500
improper torsion
 0
unit ntype qqatom
 269 'OZ    '  -1.86875
vibration
 2
 446 538
improper torsion
 0
unit ntype qqatom
 270 'OZ    '  -1.86875
vibration
 2
 435 551
improper torsion
 0
unit ntype qqatom
 271 'OZ    '  -1.86875
vibration
 2
 426 575
improper torsion
 0
unit ntype qqatom
 272 'OZ    '  -1.86875
vibration
 2
 472 531
improper torsion
 0
unit ntype qqatom
 273 'OZ    '  -1.86875
vibration
 2
 385 517
improper torsion
 0
unit ntype qqatom
 274 'OZ    '  -1.86875
vibration
 2
 414 490
improper torsion
 0
unit ntype qqatom
 275 'OZ    '  -1.86875
vibration
 2
 395 528
improper torsion
 0
unit ntype qqatom
 276 'OZ    '  -1.86875
vibration
 2
 425 500
improper torsion
 0
unit ntype qqatom
 277 'OZ    '  -1.86875
vibration
 2
 446 552
improper torsion
 0
unit ntype qqatom
 278 'OZ    '  -1.86875
vibration
 2
 449 551
improper torsion
 0
unit ntype qqatom
 279 'OZ    '  -1.86875
vibration
 2
 434 575
improper torsion
 0
unit ntype qqatom
 280 'OZ    '  -1.86875
vibration
 2
 472 539
improper torsion
 0
unit ntype qqatom
 281 'OZ    '  -1.86875
vibration
 2
 385 544
improper torsion
 0
unit ntype qqatom
 282 'OZ    '  -1.86875
vibration
 2
 441 490
improper torsion
 0
unit ntype qqatom
 283 'OZ    '  -1.86875
vibration
 2
 411 528
improper torsion
 0
unit ntype qqatom
 284 'OZ    '  -1.86875
vibration
 2
 425 516
improper torsion
 0
unit ntype qqatom
 285 'OZ    '  -1.86875
vibration
 2
 477 552
improper torsion
 0
unit ntype qqatom
 286 'OZ    '  -1.86875
vibration
 2
 449 482
improper torsion
 0
unit ntype qqatom
 287 'OZ    '  -1.86875
vibration
 2
 434 487
improper torsion
 0
unit ntype qqatom
 288 'OZ    '  -1.86875
vibration
 2
 473 539
improper torsion
 0
unit ntype qqatom
 289 'OZ    '  -1.86875
vibration
 2
 443 546
improper torsion
 0
unit ntype qqatom
 290 'OZ    '  -1.86875
vibration
 2
 406 511
improper torsion
 0
unit ntype qqatom
 291 'OZ    '  -1.86875
vibration
 2
 386 489
improper torsion
 0
unit ntype qqatom
 292 'OZ    '  -1.86875
vibration
 2
 467 572
improper torsion
 0
unit ntype qqatom
 293 'OZ    '  -1.86875
vibration
 2
 417 530
improper torsion
 0
unit ntype qqatom
 294 'OZ    '  -1.86875
vibration
 2
 427 522
improper torsion
 0
unit ntype qqatom
 295 'OZ    '  -1.86875
vibration
 2
 389 561
improper torsion
 0
unit ntype qqatom
 296 'OZ    '  -1.86875
vibration
 2
 458 494
improper torsion
 0
unit ntype qqatom
 297 'OZ    '  -1.86875
vibration
 2
 439 532
improper torsion
 0
unit ntype qqatom
 298 'OZ    '  -1.86875
vibration
 2
 429 543
improper torsion
 0
unit ntype qqatom
 299 'OZ    '  -1.86875
vibration
 2
 457 510
improper torsion
 0
unit ntype qqatom
 300 'OZ    '  -1.86875
vibration
 2
 407 562
improper torsion
 0
unit ntype qqatom
 301 'OZ    '  -1.86875
vibration
 2
 469 574
improper torsion
 0
unit ntype qqatom
 302 'OZ    '  -1.86875
vibration
 2
 438 541
improper torsion
 0
unit ntype qqatom
 303 'OZ    '  -1.86875
vibration
 2
 401 506
improper torsion
 0
unit ntype qqatom
 304 'OZ    '  -1.86875
vibration
 2
 388 491
improper torsion
 0
unit ntype qqatom
 305 'OZ    '  -1.86875
vibration
 2
 415 520
improper torsion
 0
unit ntype qqatom
 306 'OZ    '  -1.86875
vibration
 2
 390 493
improper torsion
 0
unit ntype qqatom
 307 'OZ    '  -1.86875
vibration
 2
 466 570
improper torsion
 0
unit ntype qqatom
 308 'OZ    '  -1.86875
vibration
 2
 456 559
improper torsion
 0
unit ntype qqatom
 309 'OZ    '  -1.86875
vibration
 2
 464 501
improper torsion
 0
unit ntype qqatom
 310 'OZ    '  -1.86875
vibration
 2
 398 569
improper torsion
 0
unit ntype qqatom
 311 'OZ    '  -1.86875
vibration
 2
 408 523
improper torsion
 0
unit ntype qqatom
 312 'OZ    '  -1.86875
vibration
 2
 419 513
improper torsion
 0
unit ntype qqatom
 313 'OZ    '  -1.86875
vibration
 2
 385 548
improper torsion
 0
unit ntype qqatom
 314 'OZ    '  -1.86875
vibration
 2
 445 490
improper torsion
 0
unit ntype qqatom
 315 'OZ    '  -1.86875
vibration
 2
 444 517
improper torsion
 0
unit ntype qqatom
 316 'OZ    '  -1.86875
vibration
 2
 414 549
improper torsion
 0
unit ntype qqatom
 317 'OZ    '  -1.86875
vibration
 2
 393 566
improper torsion
 0
unit ntype qqatom
 318 'OZ    '  -1.86875
vibration
 2
 463 498
improper torsion
 0
unit ntype qqatom
 319 'OZ    '  -1.86875
vibration
 2
 448 514
improper torsion
 0
unit ntype qqatom
 320 'OZ    '  -1.86875
vibration
 2
 410 553
improper torsion
 0
unit ntype qqatom
 321 'OZ    '  -1.86875
vibration
 2
 442 519
improper torsion
 0
unit ntype qqatom
 322 'OZ    '  -1.86875
vibration
 2
 416 547
improper torsion
 0
unit ntype qqatom
 323 'OZ    '  -1.86875
vibration
 2
 426 526
improper torsion
 0
unit ntype qqatom
 324 'OZ    '  -1.86875
vibration
 2
 423 531
improper torsion
 0
unit ntype qqatom
 325 'OZ    '  -1.86875
vibration
 2
 471 576
improper torsion
 0
unit ntype qqatom
 326 'OZ    '  -1.86875
vibration
 2
 392 495
improper torsion
 0
unit ntype qqatom
 327 'OZ    '  -1.86875
vibration
 2
 424 529
improper torsion
 0
unit ntype qqatom
 328 'OZ    '  -1.86875
vibration
 2
 461 564
improper torsion
 0
unit ntype qqatom
 329 'OZ    '  -1.86875
vibration
 2
 460 499
improper torsion
 0
unit ntype qqatom
 330 'OZ    '  -1.86875
vibration
 2
 396 565
improper torsion
 0
unit ntype qqatom
 331 'OZ    '  -1.86875
vibration
 2
 395 568
improper torsion
 0
unit ntype qqatom
 332 'OZ    '  -1.86875
vibration
 2
 465 500
improper torsion
 0
unit ntype qqatom
 333 'OZ    '  -1.86875
vibration
 2
 428 528
improper torsion
 0
unit ntype qqatom
 334 'OZ    '  -1.86875
vibration
 2
 425 533
improper torsion
 0
unit ntype qqatom
 335 'OZ    '  -1.86875
vibration
 2
 453 505
improper torsion
 0
unit ntype qqatom
 336 'OZ    '  -1.86875
vibration
 2
 402 558
improper torsion
 0
unit ntype qqatom
 337 'OZ    '  -1.86875
vibration
 2
 422 534
improper torsion
 0
unit ntype qqatom
 338 'OZ    '  -1.86875
vibration
 2
 431 527
improper torsion
 0
unit ntype qqatom
 339 'OZ    '  -1.86875
vibration
 2
 455 509
improper torsion
 0
unit ntype qqatom
 340 'OZ    '  -1.86875
vibration
 2
 405 560
improper torsion
 0
unit ntype qqatom
 341 'OZ    '  -1.86875
vibration
 2
 437 536
improper torsion
 0
unit ntype qqatom
 342 'OZ    '  -1.86875
vibration
 2
 433 542
improper torsion
 0
unit ntype qqatom
 343 'OZ    '  -1.86875
vibration
 2
 391 557
improper torsion
 0
unit ntype qqatom
 344 'OZ    '  -1.86875
vibration
 2
 454 496
improper torsion
 0
unit ntype qqatom
 345 'OZ    '  -1.86875
vibration
 2
 397 573
improper torsion
 0
unit ntype qqatom
 346 'OZ    '  -1.86875
vibration
 2
 470 502
improper torsion
 0
unit ntype qqatom
 347 'OZ    '  -1.86875
vibration
 2
 432 538
improper torsion
 0
unit ntype qqatom
 348 'OZ    '  -1.86875
vibration
 2
 435 537
improper torsion
 0
unit ntype qqatom
 349 'OZ    '  -1.86875
vibration
 2
 440 521
improper torsion
 0
unit ntype qqatom
 350 'OZ    '  -1.86875
vibration
 2
 418 545
improper torsion
 0
unit ntype qqatom
 351 'OZ    '  -1.86875
vibration
 2
 450 512
improper torsion
 0
unit ntype qqatom
 352 'OZ    '  -1.86875
vibration
 2
 409 554
improper torsion
 0
unit ntype qqatom
 353 'OZ    '  -1.86875
vibration
 2
 413 524
improper torsion
 0
unit ntype qqatom
 354 'OZ    '  -1.86875
vibration
 2
 421 518
improper torsion
 0
unit ntype qqatom
 355 'OZ    '  -1.86875
vibration
 2
 459 503
improper torsion
 0
unit ntype qqatom
 356 'OZ    '  -1.86875
vibration
 2
 400 563
improper torsion
 0
unit ntype qqatom
 357 'OZ    '  -1.86875
vibration
 2
 446 515
improper torsion
 0
unit ntype qqatom
 358 'OZ    '  -1.86875
vibration
 2
 412 551
improper torsion
 0
unit ntype qqatom
 359 'OZ    '  -1.86875
vibration
 2
 387 552
improper torsion
 0
unit ntype qqatom
 360 'OZ    '  -1.86875
vibration
 2
 449 492
improper torsion
 0
unit ntype qqatom
 361 'OZ    '  -1.86875
vibration
 2
 451 507
improper torsion
 0
unit ntype qqatom
 362 'OZ    '  -1.86875
vibration
 2
 404 556
improper torsion
 0
unit ntype qqatom
 363 'OZ    '  -1.86875
vibration
 2
 462 497
improper torsion
 0
unit ntype qqatom
 364 'OZ    '  -1.86875
vibration
 2
 394 567
improper torsion
 0
unit ntype qqatom
 365 'OZ    '  -1.86875
vibration
 2
 399 575
improper torsion
 0
unit ntype qqatom
 366 'OZ    '  -1.86875
vibration
 2
 472 504
improper torsion
 0
unit ntype qqatom
 367 'OZ    '  -1.86875
vibration
 2
 434 540
improper torsion
 0
unit ntype qqatom
 368 'OZ    '  -1.86875
vibration
 2
 436 539
improper torsion
 0
unit ntype qqatom
 369 'OZ    '  -1.86875
vibration
 2
 476 483
improper torsion
 0
unit ntype qqatom
 370 'OZ    '  -1.86875
vibration
 2
 447 550
improper torsion
 0
unit ntype qqatom
 371 'OZ    '  -1.86875
vibration
 2
 479 484
improper torsion
 0
unit ntype qqatom
 372 'OZ    '  -1.86875
vibration
 2
 411 516
improper torsion
 0
unit ntype qqatom
 373 'OZ    '  -1.86875
vibration
 2
 478 485
improper torsion
 0
unit ntype qqatom
 374 'OZ    '  -1.86875
vibration
 2
 475 488
improper torsion
 0
unit ntype qqatom
 375 'OZ    '  -1.86875
vibration
 2
 403 508
improper torsion
 0
unit ntype qqatom
 376 'OZ    '  -1.86875
vibration
 2
 441 544
improper torsion
 0
unit ntype qqatom
 377 'OZ    '  -1.86875
vibration
 2
 468 571
improper torsion
 0
unit ntype qqatom
 378 'OZ    '  -1.86875
vibration
 2
 430 535
improper torsion
 0
unit ntype qqatom
 379 'OZ    '  -1.86875
vibration
 2
 474 481
improper torsion
 0
unit ntype qqatom
 380 'OZ    '  -1.86875
vibration
 2
 473 487
improper torsion
 0
unit ntype qqatom
 381 'OZ    '  -1.86875
vibration
 2
 420 525
improper torsion
 0
unit ntype qqatom
 382 'OZ    '  -1.86875
vibration
 2
 480 486
improper torsion
 0
unit ntype qqatom
 383 'OZ    '  -1.86875
vibration
 2
 452 555
improper torsion
 0
unit ntype qqatom
 384 'OZ    '  -1.86875
vibration
 2
 477 482
improper torsion
 0
unit ntype qqatom
 385 'Si    '   3.7
vibration
 4
 241 273 281 313
improper torsion
 0
unit ntype qqatom
 386 'Si    '   3.7
vibration
 4
 92 140 188 291
improper torsion
 0
unit ntype qqatom
 387 'Si    '   3.7
vibration
 4
 17 49 57 359
improper torsion
 0
unit ntype qqatom
 388 'Si    '   3.7
vibration
 4
 26 82 90 304
improper torsion
 0
unit ntype qqatom
 389 'Si    '   3.7
vibration
 4
 1 65 73 295
improper torsion
 0
unit ntype qqatom
 390 'Si    '   3.7
vibration
 4
 86 134 182 306
improper torsion
 0
unit ntype qqatom
 391 'Si    '   3.7
vibration
 4
 41 97 105 343
improper torsion
 0
unit ntype qqatom
 392 'Si    '   3.7
vibration
 4
 184 192 256 326
improper torsion
 0
unit ntype qqatom
 393 'Si    '   3.7
vibration
 4
 69 133 165 317
improper torsion
 0
unit ntype qqatom
 394 'Si    '   3.7
vibration
 4
 12 28 36 364
improper torsion
 0
unit ntype qqatom
 395 'Si    '   3.7
vibration
 4
 259 267 275 331
improper torsion
 0
unit ntype qqatom
 396 'Si    '   3.7
vibration
 4
 236 252 260 330
improper torsion
 0
unit ntype qqatom
 397 'Si    '   3.7
vibration
 4
 101 141 197 345
improper torsion
 0
unit ntype qqatom
 398 'Si    '   3.7
vibration
 4
 14 30 38 310
improper torsion
 0
unit ntype qqatom
 399 'Si    '   3.7
vibration
 4
 35 43 51 365
improper torsion
 0
unit ntype qqatom
 400 'Si    '   3.7
vibration
 4
 238 254 262 356
improper torsion
 0
unit ntype qqatom
 401 'Si    '   3.7
vibration
 4
 89 137 185 303
improper torsion
 0
unit ntype qqatom
 402 'Si    '   3.7
vibration
 4
 8 16 24 336
improper torsion
 0
unit ntype qqatom
 403 'Si    '   3.7
vibration
 4
 115 145 209 375
improper torsion
 0
unit ntype qqatom
 404 'Si    '   3.7
vibration
 4
 232 240 248 362
improper torsion
 0
unit ntype qqatom
 405 'Si    '   3.7
vibration
 4
 164 172 228 340
improper torsion
 0
unit ntype qqatom
 406 'Si    '   3.7
vibration
 4
 179 187 251 290
improper torsion
 0
unit ntype qqatom
 407 'Si    '   3.7
vibration
 4
 196 204 268 300
improper torsion
 0
unit ntype qqatom
 408 'Si    '   3.7
vibration
 4
 5 13 21 311
improper torsion
 0
unit ntype qqatom
 409 'Si    '   3.7
vibration
 4
 46 102 110 352
improper torsion
 0
unit ntype qqatom
 410 'Si    '   3.7
vibration
 4
 6 70 78 320
improper torsion
 0
unit ntype qqatom
 411 'Si    '   3.7
vibration
 4
 211 219 283 372
improper torsion
 0
unit ntype qqatom
 412 'Si    '   3.7
vibration
 4
 34 42 50 358
improper torsion
 0
unit ntype qqatom
 413 'Si    '   3.7
vibration
 4
 229 237 245 353
improper torsion
 0
unit ntype qqatom
 414 'Si    '   3.7
vibration
 4
 258 266 274 316
improper torsion
 0
unit ntype qqatom
 415 'Si    '   3.7
vibration
 4
 29 85 93 305
improper torsion
 0
unit ntype qqatom
 416 'Si    '   3.7
vibration
 4
 112 152 208 322
improper torsion
 0
unit ntype qqatom
 417 'Si    '   3.7
vibration
 4
 99 139 195 293
improper torsion
 0
unit ntype qqatom
 418 'Si    '   3.7
vibration
 4
 80 160 176 350
improper torsion
 0
unit ntype qqatom
 419 'Si    '   3.7
vibration
 4
 226 234 242 312
improper torsion
 0
unit ntype qqatom
 420 'Si    '   3.7
vibration
 4
 61 117 125 381
improper torsion
 0
unit ntype qqatom
 421 'Si    '   3.7
vibration
 4
 2 10 18 354
improper torsion
 0
unit ntype qqatom
 422 'Si    '   3.7
vibration
 4
 67 131 163 337
improper torsion
 0
unit ntype qqatom
 423 'Si    '   3.7
vibration
 4
 166 174 230 324
improper torsion
 0
unit ntype qqatom
 424 'Si    '   3.7
vibration
 4
 87 135 183 327
improper torsion
 0
unit ntype qqatom
 425 'Si    '   3.7
vibration
 4
 244 276 284 334
improper torsion
 0
unit ntype qqatom
 426 'Si    '   3.7
vibration
 4
 199 207 271 323
improper torsion
 0
unit ntype qqatom
 427 'Si    '   3.7
vibration
 4
 66 130 162 294
improper torsion
 0
unit ntype qqatom
 428 'Si    '   3.7
vibration
 4
 23 55 63 333
improper torsion
 0
unit ntype qqatom
 429 'Si    '   3.7
vibration
 4
 74 154 170 298
improper torsion
 0
unit ntype qqatom
 430 'Si    '   3.7
vibration
 4
 127 159 223 378
improper torsion
 0
unit ntype qqatom
 431 'Si    '   3.7
vibration
 4
 98 138 194 338
improper torsion
 0
unit ntype qqatom
 432 'Si    '   3.7
vibration
 4
 167 175 231 347
improper torsion
 0
unit ntype qqatom
 433 'Si    '   3.7
vibration
 4
 106 146 202 342
improper torsion
 0
unit ntype qqatom
 434 'Si    '   3.7
vibration
 4
 247 279 287 367
improper torsion
 0
unit ntype qqatom
 435 'Si    '   3.7
vibration
 4
 198 206 270 348
improper torsion
 0
unit ntype qqatom
 436 'Si    '   3.7
vibration
 4
 20 52 60 368
improper torsion
 0
unit ntype qqatom
 437 'Si    '   3.7
vibration
 4
 75 155 171 341
improper torsion
 0
unit ntype qqatom
 438 'Si    '   3.7
vibration
 4
 178 186 250 302
improper torsion
 0
unit ntype qqatom
 439 'Si    '   3.7
vibration
 4
 107 147 203 297
improper torsion
 0
unit ntype qqatom
 440 'Si    '   3.7
vibration
 4
 109 149 205 349
improper torsion
 0
unit ntype qqatom
 441 'Si    '   3.7
vibration
 4
 210 218 282 376
improper torsion
 0
unit ntype qqatom
 442 'Si    '   3.7
vibration
 4
 77 157 173 321
improper torsion
 0
unit ntype qqatom
 443 'Si    '   3.7
vibration
 4
 84 132 180 289
improper torsion
 0
unit ntype qqatom
 444 'Si    '   3.7
vibration
 4
 37 45 53 315
improper torsion
 0
unit ntype qqatom
 445 'Si    '   3.7
vibration
 4
 22 54 62 314
improper torsion
 0
unit ntype qqatom
 446 'Si    '   3.7
vibration
 4
 261 269 277 357
improper torsion
 0
unit ntype qqatom
 447 'Si    '   3.7
vibration
 4
 124 156 220 370
improper torsion
 0
unit ntype qqatom
 448 'Si    '   3.7
vibration
 4
 47 103 111 319
improper torsion
 0
unit ntype qqatom
 449 'Si    '   3.7
vibration
 4
 246 278 286 360
improper torsion
 0
unit ntype qqatom
 450 'Si    '   3.7
vibration
 4
 7 71 79 351
improper torsion
 0
unit ntype qqatom
 451 'Si    '   3.7
vibration
 4
 3 11 19 361
improper torsion
 0
unit ntype qqatom
 452 'Si    '   3.7
vibration
 4
 118 150 216 383
improper torsion
 0
unit ntype qqatom
 453 'Si    '   3.7
vibration
 4
 227 235 243 335
improper torsion
 0
unit ntype qqatom
 454 'Si    '   3.7
vibration
 4
 4 68 76 344
improper torsion
 0
unit ntype qqatom
 455 'Si    '   3.7
vibration
 4
 193 201 265 339
improper torsion
 0
unit ntype qqatom
 456 'Si    '   3.7
vibration
 4
 94 142 190 308
improper torsion
 0
unit ntype qqatom
 457 'Si    '   3.7
vibration
 4
 161 169 225 299
improper torsion
 0
unit ntype qqatom
 458 'Si    '   3.7
vibration
 4
 44 100 108 296
improper torsion
 0
unit ntype qqatom
 459 'Si    '   3.7
vibration
 4
 9 25 33 355
improper torsion
 0
unit ntype qqatom
 460 'Si    '   3.7
vibration
 4
 15 31 39 329
improper torsion
 0
unit ntype qqatom
 461 'Si    '   3.7
vibration
 4
 32 88 96 328
improper torsion
 0
unit ntype qqatom
 462 'Si    '   3.7
vibration
 4
 239 255 263 363
improper torsion
 0
unit ntype qqatom
 463 'Si    '   3.7
vibration
 4
 104 144 200 318
improper torsion
 0
unit ntype qqatom
 464 'Si    '   3.7
vibration
 4
 233 249 257 309
improper torsion
 0
unit ntype qqatom
 465 'Si    '   3.7
vibration
 4
 40 48 56 332
improper torsion
 0
unit ntype qqatom
 466 'Si    '   3.7
vibration
 4
 181 189 253 307
improper torsion
 0
unit ntype qqatom
 467 'Si    '   3.7
vibration
 4
 27 83 91 292
improper torsion
 0
unit ntype qqatom
 468 'Si    '   3.7
vibration
 4
 64 120 128 377
improper torsion
 0
unit ntype qqatom
 469 'Si    '   3.7
vibration
 4
 81 129 177 301
improper torsion
 0
unit ntype qqatom
 470 'Si    '   3.7
vibration
 4
 72 136 168 346
improper torsion
 0
unit ntype qqatom
 471 'Si    '   3.7
vibration
 4
 95 143 191 325
improper torsion
 0
unit ntype qqatom
 472 'Si    '   3.7
vibration
 4
 264 272 280 366
improper torsion
 0
unit ntype qqatom
 473 'Si    '   3.7
vibration
 4
 214 224 288 380
improper torsion
 0
unit ntype qqatom
 474 'Si    '   3.7
vibration
 4
 119 151 213 379
improper torsion
 0
unit ntype qqatom
 475 'Si    '   3.7
vibration
 4
 121 153 217 374
improper torsion
 0
unit ntype qqatom
 476 'Si    '   3.7
vibration
 4
 59 113 123 369
improper torsion
 0
unit ntype qqatom
 477 'Si    '   3.7
vibration
 4
 215 221 285 384
improper torsion
 0
unit ntype qqatom
 478 'Si    '   3.7
vibration
 4
 58 116 122 373
improper torsion
 0
unit ntype qqatom
 479 'Si    '   3.7
vibration
 4
 114 148 212 371
improper torsion
 0
unit ntype qqatom
 480 'Si    '   3.7
vibration
 4
 126 158 222 382
improper torsion
 0
unit ntype qqatom
 481 'Al    '   2.775
vibration
 4
 120 152 214 379
improper torsion
 0
unit ntype qqatom
 482 'Al    '   2.775
vibration
 4
 216 222 286 384
improper torsion
 0
unit ntype qqatom
 483 'Al    '   2.775
vibration
 4
 60 114 124 369
improper torsion
 0
unit ntype qqatom
 484 'Al    '   2.775
vibration
 4
 113 147 211 371
improper torsion
 0
unit ntype qqatom
 485 'Al    '   2.775
vibration
 4
 57 115 121 373
improper torsion
 0
unit ntype qqatom
 486 'Al    '   2.775
vibration
 4
 125 157 221 382
improper torsion
 0
unit ntype qqatom
 487 'Al    '   2.775
vibration
 4
 213 223 287 380
improper torsion
 0
unit ntype qqatom
 488 'Al    '   2.775
vibration
 4
 122 154 218 374
improper torsion
 0
unit ntype qqatom
 489 'Al    '   2.775
vibration
 4
 91 139 187 291
improper torsion
 0
unit ntype qqatom
 490 'Al    '   2.775
vibration
 4
 242 274 282 314
improper torsion
 0
unit ntype qqatom
 491 'Al    '   2.775
vibration
 4
 25 81 89 304
improper torsion
 0
unit ntype qqatom
 492 'Al    '   2.775
vibration
 4
 18 50 58 360
improper torsion
 0
unit ntype qqatom
 493 'Al    '   2.775
vibration
 4
 85 133 181 306
improper torsion
 0
unit ntype qqatom
 494 'Al    '   2.775
vibration
 4
 2 66 74 296
improper torsion
 0
unit ntype qqatom
 495 'Al    '   2.775
vibration
 4
 183 191 255 326
improper torsion
 0
unit ntype qqatom
 496 'Al    '   2.775
vibration
 4
 42 98 106 344
improper torsion
 0
unit ntype qqatom
 497 'Al    '   2.775
vibration
 4
 11 27 35 363
improper torsion
 0
unit ntype qqatom
 498 'Al    '   2.775
vibration
 4
 70 134 166 318
improper torsion
 0
unit ntype qqatom
 499 'Al    '   2.775
vibration
 4
 235 251 259 329
improper torsion
 0
unit ntype qqatom
 500 'Al    '   2.775
vibration
 4
 260 268 276 332
improper torsion
 0
unit ntype qqatom
 501 'Al    '   2.775
vibration
 4
 13 29 37 309
improper torsion
 0
unit ntype qqatom
 502 'Al    '   2.775
vibration
 4
 102 142 198 346
improper torsion
 0
unit ntype qqatom
 503 'Al    '   2.775
vibration
 4
 237 253 261 355
improper torsion
 0
unit ntype qqatom
 504 'Al    '   2.775
vibration
 4
 36 44 52 366
improper torsion
 0
unit ntype qqatom
 505 'Al    '   2.775
vibration
 4
 7 15 23 335
improper torsion
 0
unit ntype qqatom
 506 'Al    '   2.775
vibration
 4
 90 138 186 303
improper torsion
 0
unit ntype qqatom
 507 'Al    '   2.775
vibration
 4
 231 239 247 361
improper torsion
 0
unit ntype qqatom
 508 'Al    '   2.775
vibration
 4
 116 146 210 375
improper torsion
 0
unit ntype qqatom
 509 'Al    '   2.775
vibration
 4
 163 171 227 339
improper torsion
 0
unit ntype qqatom
 510 'Al    '   2.775
vibration
 4
 195 203 267 299
improper torsion
 0
unit ntype qqatom
 511 'Al    '   2.775
vibration
 4
 180 188 252 290
improper torsion
 0
unit ntype qqatom
 512 'Al    '   2.775
vibration
 4
 45 101 109 351
improper torsion
 0
unit ntype qqatom
 513 'Al    '   2.775
vibration
 4
 6 14 22 312
improper torsion
 0
unit ntype qqatom
 514 'Al    '   2.775
vibration
 4
 5 69 77 319
improper torsion
 0
unit ntype qqatom
 515 'Al    '   2.775
vibration
 4
 33 41 49 357
improper torsion
 0
unit ntype qqatom
 516 'Al    '   2.775
vibration
 4
 212 220 284 372
improper torsion
 0
unit ntype qqatom
 517 'Al    '   2.775
vibration
 4
 257 265 273 315
improper torsion
 0
unit ntype qqatom
 518 'Al    '   2.775
vibration
 4
 230 238 246 354
improper torsion
 0
unit ntype qqatom
 519 'Al    '   2.775
vibration
 4
 111 151 207 321
improper torsion
 0
unit ntype qqatom
 520 'Al    '   2.775
vibration
 4
 30 86 94 305
improper torsion
 0
unit ntype qqatom
 521 'Al    '   2.775
vibration
 4
 79 159 175 349
improper torsion
 0
unit ntype qqatom
 522 'Al    '   2.775
vibration
 4
 100 140 196 294
improper torsion
 0
unit ntype qqatom
 523 'Al    '   2.775
vibration
 4
 225 233 241 311
improper torsion
 0
unit ntype qqatom
 524 'Al    '   2.775
vibration
 4
 1 9 17 353
improper torsion
 0
unit ntype qqatom
 525 'Al    '   2.775
vibration
 4
 62 118 126 381
improper torsion
 0
unit ntype qqatom
 526 'Al    '   2.775
vibration
 4
 165 173 229 323
improper torsion
 0
unit ntype qqatom
 527 'Al    '   2.775
vibration
 4
 68 132 164 338
improper torsion
 0
unit ntype qqatom
 528 'Al    '   2.775
vibration
 4
 243 275 283 333
improper torsion
 0
unit ntype qqatom
 529 'Al    '   2.775
vibration
 4
 88 136 184 327
improper torsion
 0
unit ntype qqatom
 530 'Al    '   2.775
vibration
 4
 65 129 161 293
improper torsion
 0
unit ntype qqatom
 531 'Al    '   2.775
vibration
 4
 200 208 272 324
improper torsion
 0
unit ntype qqatom
 532 'Al    '   2.775
vibration
 4
 73 153 169 297
improper torsion
 0
unit ntype qqatom
 533 'Al    '   2.775
vibration
 4
 24 56 64 334
improper torsion
 0
unit ntype qqatom
 534 'Al    '   2.775
vibration
 4
 97 137 193 337
improper torsion
 0
unit ntype qqatom
 535 'Al    '   2.775
vibration
 4
 128 160 224 378
improper torsion
 0
unit ntype qqatom
 536 'Al    '   2.775
vibration
 4
 105 145 201 341
improper torsion
 0
unit ntype qqatom
 537 'Al    '   2.775
vibration
 4
 168 176 232 348
improper torsion
 0
unit ntype qqatom
 538 'Al    '   2.775
vibration
 4
 197 205 269 347
improper torsion
 0
unit ntype qqatom
 539 'Al    '   2.775
vibration
 4
 248 280 288 368
improper torsion
 0
unit ntype qqatom
 540 'Al    '   2.775
vibration
 4
 19 51 59 367
improper torsion
 0
unit ntype qqatom
 541 'Al    '   2.775
vibration
 4
 177 185 249 302
improper torsion
 0
unit ntype qqatom
 542 'Al    '   2.775
vibration
 4
 76 156 172 342
improper torsion
 0
unit ntype qqatom
 543 'Al    '   2.775
vibration
 4
 108 148 204 298
improper torsion
 0
unit ntype qqatom
 544 'Al    '   2.775
vibration
 4
 209 217 281 376
improper torsion
 0
unit ntype qqatom
 545 'Al    '   2.775
vibration
 4
 110 150 206 350
improper torsion
 0
unit ntype qqatom
 546 'Al    '   2.775
vibration
 4
 83 131 179 289
improper torsion
 0
unit ntype qqatom
 547 'Al    '   2.775
vibration
 4
 78 158 174 322
improper torsion
 0
unit ntype qqatom
 548 'Al    '   2.775
vibration
 4
 21 53 61 313
improper torsion
 0
unit ntype qqatom
 549 'Al    '   2.775
vibration
 4
 38 46 54 316
improper torsion
 0
unit ntype qqatom
 550 'Al    '   2.775
vibration
 4
 123 155 219 370
improper torsion
 0
unit ntype qqatom
 551 'Al    '   2.775
vibration
 4
 262 270 278 358
improper torsion
 0
unit ntype qqatom
 552 'Al    '   2.775
vibration
 4
 245 277 285 359
improper torsion
 0
unit ntype qqatom
 553 'Al    '   2.775
vibration
 4
 48 104 112 320
improper torsion
 0
unit ntype qqatom
 554 'Al    '   2.775
vibration
 4
 8 72 80 352
improper torsion
 0
unit ntype qqatom
 555 'Al    '   2.775
vibration
 4
 117 149 215 383
improper torsion
 0
unit ntype qqatom
 556 'Al    '   2.775
vibration
 4
 4 12 20 362
improper torsion
 0
unit ntype qqatom
 557 'Al    '   2.775
vibration
 4
 3 67 75 343
improper torsion
 0
unit ntype qqatom
 558 'Al    '   2.775
vibration
 4
 228 236 244 336
improper torsion
 0
unit ntype qqatom
 559 'Al    '   2.775
vibration
 4
 93 141 189 308
improper torsion
 0
unit ntype qqatom
 560 'Al    '   2.775
vibration
 4
 194 202 266 340
improper torsion
 0
unit ntype qqatom
 561 'Al    '   2.775
vibration
 4
 43 99 107 295
improper torsion
 0
unit ntype qqatom
 562 'Al    '   2.775
vibration
 4
 162 170 226 300
improper torsion
 0
unit ntype qqatom
 563 'Al    '   2.775
vibration
 4
 10 26 34 356
improper torsion
 0
unit ntype qqatom
 564 'Al    '   2.775
vibration
 4
 31 87 95 328
improper torsion
 0
unit ntype qqatom
 565 'Al    '   2.775
vibration
 4
 16 32 40 330
improper torsion
 0
unit ntype qqatom
 566 'Al    '   2.775
vibration
 4
 103 143 199 317
improper torsion
 0
unit ntype qqatom
 567 'Al    '   2.775
vibration
 4
 240 256 264 364
improper torsion
 0
unit ntype qqatom
 568 'Al    '   2.775
vibration
 4
 39 47 55 331
improper torsion
 0
unit ntype qqatom
 569 'Al    '   2.775
vibration
 4
 234 250 258 310
improper torsion
 0
unit ntype qqatom
 570 'Al    '   2.775
vibration
 4
 182 190 254 307
improper torsion
 0
unit ntype qqatom
 571 'Al    '   2.775
vibration
 4
 63 119 127 377
improper torsion
 0
unit ntype qqatom
 572 'Al    '   2.775
vibration
 4
 28 84 92 292
improper torsion
 0
unit ntype qqatom
 573 'Al    '   2.775
vibration
 4
 71 135 167 345
improper torsion
 0
unit ntype qqatom
 574 'Al    '   2.775
vibration
 4
 82 130 178 301
improper torsion
 0
unit ntype qqatom
 575 'Al    '   2.775
vibration
 4
 263 271 279 365
improper torsion
 0
unit ntype qqatom
 576 'Al    '   2.775
vibration
 4
 96 144 192 325
improper torsion
 0
# Faux Na +1 ions
input_style
'basic connectivity map'
nunit
1
nmaxcbmc
1
lpdbnames
F
forcefield
'CatlowFaux'
charge_assignment
'manual'
unit ntype qqatom
1 'Na    '   1.
vibration
0
improper torsion
0
#Catlow methane
input_style
'basic connectivity map'
nunit
5
nmaxcbmc
5
lpdbnames
F
forcefield
'CatlowFaux'
charge_assignment
'manual'
unit ntype qqatom
1    'Cc'    -0.4
vibration
4
2 3 4 5
improper torsion
0
unit ntype qqatom
2    'Hc'    0.1
vibration
1
1
improper torsion
0
unit ntype qqatom
3    'Hc'    0.1
vibration
1
1
improper torsion
0
unit ntype qqatom
4    'Hc'    0.1
vibration
1
1
improper torsion
0
unit ntype qqatom
5    'Hc'    0.1
vibration
1
1
improper torsion
0
~~~


Grand Cannonical Ensemble Energy Biasing.
======

<br/><img src='/images/energybiasing.png'>

~~~
random_number_generator
'RANLUX'
random_luxlevel
3
random_seed
1302552
random_allow_restart
T
ensemble 
'uvt'
temperature
298.15d0
nmolty
2
nmolectyp
1 50
chempot
0 -500.0d0
numboxes
1 
stepstyle
'moves'
nstep
1000
printfreq
100
blocksize
200
moviefreq
10000000
backupfreq
100000
runoutput
'blocks'
pdb_output_freq
1000000
trmaxdispfreq
1
volmaxdispfreq
10000000
linit   
T
initboxtype
'dimensions'
initstyle
'coords' 'full cbmc'
initlattice
'none' 'center'
initmol
1 0
inix iniy iniz
1    1    1
hmatrix
20.0511d0 0.0d0 0.0d0
0.0d0   19.87570d0  0.0d0
0.0d0 0.0d0  26.73640d0
pmuvtcbswap
1.0d0
          pmuvtcbmt
          0.0d0 1.0d0
pm1boxcbswap
0.0d0
          pm1cbswmt
          0.0d0 1.0d0
pmavb1    
0.0d0     
          pmavb1in
          0.5d0
          pmavb1mt
          0.2d0 1.0d0
          pmavb1ct
          0.33d0 1.0d0
          0.33d0 1.0d0
          avb1rad
          5.0d0
pmavb2
0.0d0     
          pmavb2in
          0.5d0
          pmavb2mt
          0.2d0 1.0d0
          pmavb2ct
          0.33d0 1.0d0
          0.33d0 1.0d0
          avb2rad
          5.0d0
pmavb3
0.0d0     
          pmavb3mt
          0.2d0  1.0d0
          pmavb3ct
          0.33d0 1.0d0
          0.33d0 1.0d0
          avb3rad
          5.0d0
pmcb
0.35d0
          pmcbmt
          0.0d0 1.0d0 
          pmall
          0.0d0 0.5d0
pmback
0.0d0
          pmbkmt
          0.0d0 1.0d0
pmpivot
0.0d0
          pmpivmt
          0.0d0 1.0d0
pmconrot
0.0d0
          pmcrmt
          0.0d0 1.0d0
pmcrback
0.0d0
          pmcrbmt
          0.0d0 1.0d0
pmplane
0.0d0
          pmplanebox
          1.0d0
          planewidth
          3.0d0
pmrow
0.0d0
          pmrowbox
          1.0d0
          rowwidth
          3.0d0
pmtraat
0.00d0
          pmtamt
          0.0d0 1.0d0 
          rmtraa
          0.5d0 
          tatraa
          0.5d0
pmtracm
0.00d0
          pmtcmt
          0.0d0 1.0d0      	
          rmtrac
          0.5d0 
          tatrac
          0.5d0
pmrotate
1.0d0
          pmromt  
          0.0d0 1.0d0
          rmrot
          0.05d0
          tarot
          0.5d0
cbmc_formulation
'Martin and Siepmann 1999 + Martin and Thompson 2004'
cbmc_setting_style
'explicit'
cbmc_nb_one_generation
'uniform' 'energy bias'
mapmolty
2  
lcreatemap
T                      
cubex cubey cubez
10 10 10  
nch_nb_one
1 1
nch_nb
1 1
cbmc_dihedral_generation
'ideal'
nch_tor
1 360
nch_tor_connect
1 360
cbmc_bend_generation
'ideal'
nch_bend_a
1 1000
nch_bend_b
1 1000
cbmc_bond_generation
'r^2 with bounds'
vibrang
0.85 1.15	
nch_vib
1 1
two_bond_fixed_endpoint_bias_style
'none'
three_bond_fixed_endpoint_bias_style
'none'
ffnumber
1
ff_filename
/towheebase/ForceFields/towhee_ff_Dubb2004
classical_potential
'Lennard-Jones'               
classical_mixrule
'Explicit'
lshift
.false.
ltailc
.true.
rmin  
1.0d0 
rcut  
9.5d0
rcutin 
9.5d0
electrostatic_form
'none'
#silicalite
input_style
'basic connectivity map'
nunit
576
nmaxcbmc
576
lpdbnames
F
forcefield
'Dubb2004'
charge_assignment
'none
unit ntype 
   1 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   2 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   3 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   4 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   5 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   6 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   7 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   8 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
   9 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  10 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  11 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  12 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  13 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  14 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  15 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  16 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  17 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  18 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  19 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  20 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  21 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  22 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  23 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  24 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  25 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  26 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  27 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  28 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  29 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  30 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  31 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  32 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  33 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  34 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  35 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  36 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  37 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  38 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  39 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  40 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  41 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  42 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  43 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  44 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  45 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  46 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  47 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  48 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  49 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  50 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  51 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  52 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  53 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  54 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  55 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  56 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  57 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  58 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  59 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  60 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  61 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  62 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  63 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  64 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  65 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  66 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  67 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  68 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  69 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  70 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  71 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  72 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  73 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  74 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  75 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  76 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  77 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  78 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  79 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  80 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  81 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  82 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  83 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  84 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  85 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  86 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  87 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  88 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  89 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  90 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  91 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  92 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  93 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  94 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  95 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  96 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
  97 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
  98 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
  99 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 100 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 101 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 102 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 103 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 104 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 105 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 106 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 107 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 108 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 109 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 110 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 111 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 112 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 113 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 114 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 115 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 116 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 117 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 118 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 119 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 120 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 121 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 122 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 123 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 124 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 125 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 126 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 127 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 128 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 129 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 130 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 131 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 132 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 133 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 134 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 135 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 136 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 137 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 138 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 139 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 140 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 141 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 142 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 143 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 144 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 145 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 146 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 147 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 148 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 149 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 150 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 151 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 152 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 153 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 154 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 155 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 156 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 157 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 158 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 159 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 160 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 161 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 162 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 163 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 164 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 165 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 166 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 167 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 168 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 169 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 170 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 171 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 172 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 173 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 174 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 175 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 176 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 177 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 178 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 179 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 180 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 181 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 182 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 183 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 184 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 185 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 186 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 187 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 188 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 189 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 190 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 191 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 192 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 193 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 194 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 195 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 196 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 197 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 198 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 199 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 200 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 201 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 202 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 203 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 204 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 205 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 206 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 207 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 208 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 209 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 210 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 211 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 212 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 213 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 214 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 215 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 216 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 217 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 218 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 219 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 220 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 221 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 222 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 223 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 224 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 225 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 226 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 227 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 228 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 229 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 230 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 231 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 232 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 233 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 234 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 235 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 236 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 237 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 238 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 239 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 240 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 241 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 242 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 243 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 244 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 245 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 246 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 247 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 248 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 249 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 250 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 251 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 252 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 253 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 254 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 255 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 256 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 257 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 258 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 259 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 260 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 261 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 262 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 263 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 264 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 265 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 266 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 267 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 268 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 269 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 270 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 271 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 272 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 273 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 274 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 275 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 276 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 277 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 278 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 279 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 280 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 281 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 282 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 283 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 284 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 285 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 286 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 287 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 288 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 289 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 290 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 291 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 292 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 293 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 294 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 295 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 296 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 297 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 298 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 299 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 300 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 301 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 302 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 303 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 304 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 305 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 306 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 307 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 308 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 309 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 310 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 311 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 312 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 313 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 314 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 315 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 316 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 317 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 318 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 319 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 320 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 321 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 322 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 323 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 324 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 325 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 326 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 327 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 328 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 329 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 330 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 331 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 332 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 333 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 334 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 335 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 336 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 337 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 338 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 339 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 340 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 341 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 342 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 343 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 344 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 345 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 346 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 347 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 348 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 349 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 350 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 351 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 352 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 353 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 354 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 355 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 356 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 357 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 358 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 359 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 360 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 361 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 362 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 363 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 364 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 365 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 366 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 367 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 368 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 369 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 370 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 371 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 372 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 373 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 374 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 375 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 376 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 377 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 378 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 379 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 380 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 381 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 382 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 383 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 384 'Si    '   
vibration
 0
improper torsion
 0
unit ntype 
 385 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 386 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 387 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 388 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 389 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 390 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 391 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 392 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 393 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 394 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 395 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 396 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 397 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 398 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 399 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 400 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 401 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 402 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 403 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 404 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 405 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 406 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 407 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 408 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 409 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 410 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 411 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 412 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 413 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 414 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 415 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 416 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 417 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 418 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 419 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 420 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 421 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 422 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 423 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 424 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 425 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 426 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 427 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 428 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 429 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 430 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 431 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 432 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 433 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 434 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 435 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 436 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 437 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 438 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 439 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 440 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 441 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 442 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 443 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 444 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 445 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 446 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 447 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 448 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 449 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 450 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 451 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 452 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 453 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 454 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 455 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 456 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 457 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 458 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 459 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 460 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 461 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 462 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 463 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 464 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 465 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 466 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 467 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 468 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 469 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 470 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 471 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 472 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 473 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 474 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 475 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 476 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 477 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 478 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 479 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 480 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 481 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 482 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 483 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 484 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 485 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 486 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 487 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 488 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 489 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 490 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 491 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 492 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 493 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 494 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 495 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 496 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 497 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 498 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 499 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 500 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 501 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 502 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 503 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 504 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 505 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 506 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 507 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 508 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 509 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 510 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 511 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 512 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 513 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 514 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 515 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 516 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 517 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 518 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 519 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 520 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 521 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 522 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 523 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 524 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 525 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 526 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 527 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 528 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 529 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 530 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 531 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 532 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 533 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 534 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 535 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 536 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 537 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 538 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 539 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 540 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 541 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 542 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 543 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 544 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 545 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 546 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 547 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 548 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 549 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 550 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 551 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 552 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 553 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 554 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 555 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 556 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 557 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 558 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 559 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 560 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 561 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 562 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 563 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 564 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 565 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 566 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 567 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 568 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 569 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 570 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 571 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 572 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 573 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 574 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 575 'O     '  
vibration
 0
improper torsion
 0
unit ntype 
 576 'O     '  
vibration
 0
improper torsion
 0
#Methane
input_style
'basic connectivity map'
nunit
1
nmaxcbmc
1
lpdbnames
F
forcefield
'Dubb2004'
charge_assignment
'none
unit ntype    
1    'CH4'
vibration
0
improper torsion
0 
~~~
