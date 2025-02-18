
```java
function REFLEX-AGENT-WITH-STATE(percept) returns an action
	static: state, a description of the current world state
		rules, a set of condition-action rules
		action, the most recent action, initially none
	state ← UPDATE-STATE(state, action, percept)
	rule ← RULE-MATCH(state, rule)
	action ← RULE-ACTION[rule]
	return action

```

L'input non viene solo interpretato, ma mappato in una descrizione interna dello stato (un modello del mondo).
descrizione (un modello del mondo)
- un agente scacchistico potrebbe tenere traccia della situazione attuale della scacchiera situazione della scacchiera quando le sue percezioni sono solo le mosse

Lo stato interno viene utilizzato anche per interpretare le percezioni successive.
Il modello del mondo può includere gli effetti delle proprie azioni!