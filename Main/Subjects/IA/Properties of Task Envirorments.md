## Osservabilità
Completamente osservabile
- è possibile rilevare l'intero stato dell'ambiente;
- almeno le parti rilevanti;
- non è necessario tenere traccia degli stati interni;

Parzialmente osservabile
- parti dell'ambiente non possono essere rilevate;

## Deterministic vs Stochastic
Deterministic
- lo stato successivo dell'ambiente è completamente determinato dallo stato attuale e dall'azione eseguita;

## Episodic vs Sequential
Episodico:
- l'esperienza dell'agente può essere suddivisa in fasi atomiche;
- l'agente percepisce e poi compie una singola azione;
- la scelta dell'azione dipende solo dall'episodio stesso;

Sequenziale:
- la decisione corrente può influenzare tutte le decisioni future

## Dynamic vs Static
Dynamic:
- l'ambiente può cambiare mentre l'agente delibera;
Static:
- l'ambiente non cambia;
Semidynamic:
- l'ambiente non cambia, ma il punteggio di performance viene

## Discrete vs. Continuous
Discrete:
- numero finito di azioni / stati ambientali / percezioni;
Continuo:
- azioni, stati, percezioni sono su scala continua;

## Single-Agent vs Multi-Agent
Single-Agent:
- Nessun altro agente (altri agenti possono essere parte dell’ambiente);
Multi-Agent:
- L'ambiente contiene altri agenti le cui prestazioni misura che dipende dalle mie azioni?;
- altri agenti possono essere cooperativi o competitivi;