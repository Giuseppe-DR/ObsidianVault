---
tags:
  - IA
links: "[[IA MOC]]"
---

## Problem-solving agents


```Java
function Simple-Problem-Solving-Agent( percept) returns an action
	static: seq, an action sequence, initially empty
			state, some description of the current world state
			goal, a goal, initially null
			problem, a problem formulation
	state ← Update-State(state, percept)
	if seq is empty then
		goal ← Formulate-Goal(state)
		problem ← Formulate-Problem(state, goal)
		seq ← Search( problem)
	action ← Recommendation(seq, state)
	seq ← Remainder(seq, state)
	return action
```

## Esempio: Romania

In vacanza in Romania, attualmente ad Arad.
Il volo parte domani da Bucarest
Formulare l'obiettivo:
	-essere a Bucarest
Formulare il problema:
	-stati: varie città
	-azioni: guidare tra le città
Trovare la soluzione:
	-sequenza di città, ad esempio, Arad, Sibiu, Fagaras, Bucarest
	
![[Romania.png]]
## Single-State problem formulation

A problem is defined by four items:

==initial state== e.g., “at Arad”
==successor function== S(x) = set of action–state pairs
e.g., S(Arad) = {〈Arad → Zerind, Zerind〉, . . .}
==goal test==, can be
explicit, e.g., x = “at Bucharest”
implicit, e.g., NoDirt(x)
==path cost== (additive)
e.g., sum of distances, number of actions executed, etc.
c(x, a, y) is the step cost, assumed to be ≥ 0

A solution is a sequence of actions
leading from the initial state to a goal state

## Selecting a state space
Il mondo reale è molto complesso.
 => lo state space deve essere astratta per il problem solving
(Abstract) state = set degli stati reali
(Abstract) action = combinazione complesse di azioni reali, “Arad→Zerind” rappresenta un set complesso di percorsi, deviazioni, soste.
Per garantire la realizzabilità, qualsiasi stato reale “in Arad”
deve raggiungere uno stato reale “a Zerind”.
(Abstract) solution = insieme di percorsi reali che sono soluzioni nel mondo reale

Ogni azione stratta dovrebbe essere più facile dell problema originale.

![[Vacuum world state space graph.png]]

## Three search algorithms

Basic idea:
	offline, simulazione dell’esplorazione dello spazio di stati, generando successori di stati già esplorati (a.k.a. expanding states)

```java
function Tree-Search( problem, strategy) returns a solution, or failure
	initialize the search tree using the initial state of problem
	loop do
		if there are no candidates for expansion then return failure
	choose a leaf node for expansion according to strategy
	if the node contains a goal state then return the corresponding solution
	else expand the node and add the resulting nodes to the search tree
end

```

![[Tree Search Example.png]]

## Implementation: states vs. nodes

![[States]]

![[Nodes]]


![[States vs nodes.png]]

La funzione EXPAND function create a new [[Nodes]], riempiendo i vari campi e usando successorFn del problema per creare lo [[States]] corrispondente.

## Implementation: general tree search

```Java
function Tree-Search( problem, fringe) returns a solution, or failure
fringe ← Insert(Make-Node(Initial-State[problem]), fringe)
	loop do
		if fringe is empty then return failure
		node ← Remove-Front(fringe)
		if Goal-Test(problem, State(node)) then return node
		fringe ← InsertAll(Expand(node, problem), fringe)

```


```Java
function Expand( node, problem) returns a set of nodes
	successors ← the empty set
	for each action, result in Successor-Fn(problem, State[node]) do
		s ← a new Node
		Parent-Node[s] ← node; Action[s] ← action; State[s] ← result
		Path-Cost[s] ← Path-Cost[node] + Step-Cost(node, action, s)
		Depth[s] ← Depth[node] + 1
		add s to successors
return successors

```


![[Search Strategies]]

## Uniformed search strategies
Uninformed strategies usano solo le informazioni disponibile nella definizione del problema.

[[Breadth-first search]]
[[Uniform-cost search]]
[[Depth-first search]]
[[Depth-limited search]]
[[Iterative deepening search]]
[[Summary of Algorithms]]