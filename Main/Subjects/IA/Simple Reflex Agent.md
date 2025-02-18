Selezionare l'azione sulla base della sola percezione corrente
- ignora la storia percettiva
![[Simple Reflex Agent.png]]

Selezionare l'azione sulla base della sola percezione corrente
- ignora la cronologia dei percezioni;
Implementato attraverso regole di condizione-azione
Grande riduzione delle possibili situazioni di percezione/azione:
- da $$\sum_{t=1}^{T} \left| P^t \right|$$ a |P|;
Ma sarebbe un pessimo giocatore di scacchi:
- non guarda la scacchiera, ma solo l'ultima mossa dell'avversario (supponendo che l'input sensoriale sia solo l'ultima mossa, non visiva);

```java
function REFLEX-VACUUM-AGENT([location,status]) returns an action
	if satatus = Dirty then return Suck
	else if location = A then return Right
	else if location = B then return Left

```
