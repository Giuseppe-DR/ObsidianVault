
```Java
function TABLE-DRIVEN-AGENT(percept) returns an action
	static: percepts, a sequence initially empty
	table, a table of actions, indexed by percept sequence
append percept to the end of percepts
action ← LOOKUP(percepts, table)
return action
```

- ha una tabella di tutte le possibili storie percettive
- cerca la risposta giusta nella tabella

Chiaramente non è fattibile:
- se ci sono |P| percezioni e un tempo di vita di T passi temporali, abbiamo bisogno di una tabella di ricerca di dimensioni $$\sum_{t=1}^{T} \left| P^t \right|$$

Per esempio, gli scacchi:
- circa 36 mosse per posizione, lunghezza media della partita 40 mosse
→ 5105426007029058700898070779698222806522450657188621232590965