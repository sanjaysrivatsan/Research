1. how do i use the MadGraph5_aMC@NLO framework to allow for loop level processes?
	1. The UFO dir needs UV and R2 counterterms 
2. which files exactly need to include the UV and R2 counterterms?  
	1. in CT_vertices.py and R2_vertices.py
3. What is feynrules and how do i generate the terms from it?
	1. Feynrules is a mathematica package that translates a $\mathcal{L}$, Lagrangian into Feynman rules and exports models to UFO format
4. how do i check if the ALRM_general UFO model includes these loop and counterterm implementations
	1. Open these files and check for definitions of UV counterterms and R2 vertices
	2. Search for keywords “UV,” “R2,” “counterterm” within the files. If absent, counterterms must be generated and added using FeynRules+NLOCT.
5. modifying this model so that i can make loop calculations
	1. Use FeynRules + NLOCT to add UV and R2 terms, then export new UFO files
	2. Replace the existing UFO folder in MadGraph with these updated files
	3. Test your setup by generating a known loop process and checking outputs.
6. A **loop-induced process** lacks tree-level diagrams and arises exclusively from loop amplitudes; the lowest order for such a process is one-loop, not tree-level.