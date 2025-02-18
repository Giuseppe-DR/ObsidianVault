= ricerca depth-first con limite di profondità l,
cioè i nodi alla profondità l non hanno successori.

## Recursive implementation

```Java
function Depth-Limited-Search( problem, limit) returns soln/fail/cutoff
Recursive-DLS(Make-Node(Initial-State[problem]), problem, limit)

function Recursive-DLS(node, problem, limit) returns soln/fail/cutoff
	cutoff-occurred? ← false
	if Goal-Test(problem, State[node]) then return node
	else if Depth[node] = limit then return cutoff
	else for each successor in Expand(node, problem) do
		result ← Recursive-DLS(successor, problem, limit)
		if result = cutoff then cutoff-occurred? ← true
		else if result " = failure then return result
if cutoff-occurred? then return cutoff else return failure

```
