---
tags:
  - IA
links: "[[IA MOC]]"
---

## Cosa sono gli Agenti
Un ==agente== è un'entità che percepisce e agisce.

Questo corso riguarda la progettazione di ==agenti razionali==.

Astrattamente, un agente è una funzione che va dalla storia delle percezioni alle azioni:

$$ f : \mathcal{P}^{*} \to \mathcal{A}$$

Gli ==Agenti== includono umani, robots, softbots, termostati, etc.
Il programma Agente gira sull’architettura fisica to produce $$ f $$

Per una data classe di ambienti e compiti, cerchiamo l'agente (o la classe di agenti) con le migliori prestazioni.

> [!warning]
> Le limitazioni computazionali rendono la perfetta razionalità non raggiungibile.
> Progettare il miglior programma date le risorse della macchina.

![[Agents.png]]


### Razionalità
Un ==agente razionale== sceglie l'azione che massimizza il ==valore atteso== della performance, ==data la sequenza di percezioni fino a quel momento==.

### PEAS
Per progettare un agente razionale, dobbiamo specificare l'ambiente del compito.
Consideriamo, ad esempio, il compito di progettare un taxi automatizzato:
Performance measure: sicurezza, destinazione, profitti, legalità, comfort.
Environment: strade/strade americane, traffico, pedoni, tempo atmosferico.
Actuators: sterzo, acceleratore, freno, clacson, altoparlante/display.
Sensors: video, accelerometri, indicatori, sensori del motore, tastiera, GPS.

### Riassumendo
Gli Agenti interagiscono con l’ ambiente attraverso attuatori e sensori.
La Agent Function descrive cosa l Agente fa in tutte le circostanze.
La Performance Measure valuta la sequenza ambientale.
Agent program implementano alcune funzioni degli agenti.
PEAS definiscono i task ambientali.
Gli ambienti sono categorizzati in diverse dimensioni: Osservabili, deterministici, episodico, statico, discreto, a singolo agente.
Esistono diverse architetture di agenti: reflex, reflex with state, goal-based, utility-based

[[A Simple General Agent]]
[[Simple Reflex Agent]]
[[General Simple Reflex Agent]]
[[Model-Based Reflex Agent]]
[[General Model-Based Reflex Agent]]
[[Goal-Based Agent]]
[[Utility-Based Agent]]

[[Learning]]
[[Learning Agent]]
