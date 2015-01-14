# tropicalCommutingVariety
This repository contains computational outputs, supplement the paper Tropical Commuting Variety with Ralph Morrison

List of files:
Gfan input files:
- input2: the ideal for n = 2
- input3: the ideal for n = 3
- symmetry3: generators of the symmetry group for n = 3
- symmetricInput3: the ideal for the symmetric variety for n = 3, with generators of the symmetry group appended

Gfan output files:
- prevariety2: the tropical commuting prevariety for n = 2
- prevariety3: the tropical commuting prevariety for n = 3
- variety2: the tropical commuting variety for n = 2
- variety3: the tropical commuting variety for n = 3, with cones
listed up to symmetry only
- symmetricPrevariety3: the symmetric tropical commuting prevariety for n = 3
- symmetricVariety3: the symmetric tropical commuting variety for n = 3

Gfan commands used to generate the output files:
- prevariety2: gfan_tropicalintersection < input2
- prevariety3: gfan_tropicalintersection < input3
- variety2: gfan_buchberger < input2 | gfan_tropicalbruteforce 
- variety3: 
gfan_tropicalstartingcone < input3 > tconestart3
cat tconestart3 symmetry3 | tmp
gfan_tropicaltraverse --symmetry < tmp
- symmetricPrevariety3: gfan_tropicalintersection < symmetricInput3
- symmetricVariety3: 
gfan_tropicalstartingcone < symmetricInput3 > symtconestart3
cat symtconestart3 symmetricInput3 | tmp
gfan_tropicaltraverse --symmetry < tmp

- 
=======
Computational outputs, supplement the paper Tropical Commuting Variety with Ralph Morrison
