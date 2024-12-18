

# Nonlinear Causal Learning Algorithm

Code repository for a causal discovery method focused on learning non-linear relations from data


## Summary:

- Highlights: 

	- A likelihood-ratio based statistical test to compare and determine the true causal direction of an undirected edge;
	- A framework for ranking undirected edges for orientation based on an independence measure derived from the Additive Noise Model assumption;
	- Faster computation times and greater interpretability of results during the learning process compared to competing non-linear learning methods;
	- Theoretical guarantees for structural learning in both the population and finite sample settings.
	

- Algorithm Structure:

	1. Initial structural learning: performs modified version of PC algorithm to learn a denser CPDAG containing extraneous edges but v-structures/edge orientations detected under a strigent threshold
	2. Edge orientation: employs likelihood-ratio based statistical test to determine the true orientation of undirected edges in the graph
	3. Edge deletion: utilizes significance test results of covariates to delete superfluous edges from the graph, yielding the final DAG structure
	4. (For practical purposes) Graph refinement: converts previous output from PDAG to DAG by applying the likelihood test to undirected edges, if there exists any
