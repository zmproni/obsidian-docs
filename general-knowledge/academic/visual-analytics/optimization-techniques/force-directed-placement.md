# Force-directed placement

<img src="https://repository-images.githubusercontent.com/140739735/d9f6bc80-ae30-11e9-86e4-f8bd1b99a4aa" height=300 width="auto">

This refers to the optimisation technique force directed placement. 
For the idiom [force directed placement graph](academic/visual-analytics/visual-idioms/networks/force-directed-placement.md). 
More on [networks](obsidian://open?vault=general-knowledge&file=academic%2Fvisual-analytics%2Fdata-types%2Fnetworks) the data type. 

## Physics model 
- links -> springs pull together
- nodes -> magnets repulse apart

## Algorithm 
- place vertices in random locations
- while not in equilibrium 
	- calculate force on vertex
		- sum of
			- pairwise repulsion of all sides
			- attraction between connected nodes 
	- move vertex by c* vertex_force

Note:
Iterative approach

### Pros:
- Good layout for small, sparse graphs
- Clusters typically visible
- Edge length uniformity

### Cons
- Nondeterministic
 - Computationally expensive: $O(n^3)$
 - Naive FD doesn't scale well beyond IK nodes
 - Iterative progress is engaging but distracting 
