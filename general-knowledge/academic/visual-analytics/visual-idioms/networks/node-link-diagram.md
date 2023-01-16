# Node Link Diagrams

<img src="https://www.researchgate.net/profile/Jean-Daniel-Fekete/publication/5852578/figure/fig2/AS:277672610549762@1443213717100/Node-Link-diagram-from-Indiana-University-Wei04.png" height=300 width="auto">
source: https://www.researchgate.net/figure/Node-Link-diagram-from-Indiana-University-Wei04_fig2_5852578

## Criteria
Properties to make node link diagrams good:  

### Minimise
- edge crossing  
- node overlaps
- drawing area
- edge bends 

### Maximise
* aspect ratio disparity 
* angular distance

### Emphasise symmetry
- symmetrical designs 

### Limitations  
Node link diagrams are hard to make because:
- most criteria is NP-hard individually 
- many criteria directly conflicts

#### Criteria conflicts
- minimise white space vs. symmetrical designs

## How to get over limitations 
Deciding which criteria should take precedence we need to look at the task and decide ourselves. Depending on the type of problems faced and the ideal solution the use of certain optimisation techniques can help find a minimal cost layout. 

The use of cost functions to determine the importance of a metric over another:
$$ F(layout) = w_1[C_1] + w_2[C_2] + ... + w_n[C_n]$$
or:
$$ F(layout) = \sum_{i=1}^n{w_i[C_i]} $$
Where: 
- $F(layout)$ : the score of your layout
- $C_i$ : is a given metric (crossing counts, drawing space used, etc...)
- $w_i$ : is the weight given to the metric to symbolise its importance 

The optimisation techniques:
- energy-based physics model
- [force-directed placement](academic/visual-analytics/visual-idioms/networks/force-directed-placement.md)
- spring embedders
