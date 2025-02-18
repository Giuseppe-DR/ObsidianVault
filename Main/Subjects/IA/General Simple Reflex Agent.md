
```Java
function SIMPLE-REFLEX-AGENT(percept) returns an action
	static: rules, a set of condition-action rules
	state ← INTERPRET-INPUT(percept)
	rule ← RULE-MATCH(state, rule)
	action ← RULE-ACTION[rule]
	return action

```

Si noti che le regole sono utilizzate solo come concetto
- L'implementazione effettiva potrebbe essere, ad esempio, un circuito logico.
Funzionerà solo se l'ambiente è completamente osservabile
- Tutto ciò che è importante deve essere determinabile da input sensoriali attuali
- nel mondo del vuoto senza un sensore per la stanza, l'agente non sa se muoversi a destra o a sinistra
- possibile soluzione: randomizzazione
