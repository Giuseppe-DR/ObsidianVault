Espandere il nodo meno costoso non espanso
## Implementation
fringe = coda ordinata in base al costo del percorso, prima il più basso.
Equivalente a breadth-first se i costi dei passi sono tutti uguali.

Complete?? Si se il costo dei passi è ≥ e
Tempo?? # dei nodi con g≤ costo della soluzione ottiamle, O(b^[C*/e]) dove C* è il costo della soluzione ottimale
Spazio?? # dei nodi con g≤ costo della soluzione ottimale, O(b^[C*/e])
Optiaml?? Sì-nodi espansi in ordine crescente di g(n)