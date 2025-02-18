![[Pasted image 20250218221318.png]]

## Repeated States
Il mancato rilevamento di stati ripetuti può trasformare un problema lineare in uno esponenziale!

![[Pasted image 20250218221402.png]]

## Graph Search

![[Pasted image 20250218221553.png]]

## Problem Types

Deterministic, fully observable => single-state problem
L’agente sa lo stato preciso in cui sarà, la soluzione è una sequenza

Non-observable => conformant problem
L'agente potrebbe non avere alcuna idea di dove si trovi; la soluzione (se esiste) è una sequenza.

**Nondeterministico e/o parzialmente osservabile** ⟶ **problema di contingenza**  
Le percezioni forniscono **nuove** informazioni sullo stato attuale.  
La soluzione è un **piano contingente** o una **politica**.  
Spesso **interlaciano** ricerca ed esecuzione.

**Spazio degli stati sconosciuto** ⟶ **problema di esplorazione** ("online")

## Summary
La formulazione di un problema richiede solitamente l'astrazione dei dettagli del mondo reale per
definire uno spazio di stati che possa essere esplorato in modo fattibile
Varietà di strategie di ricerca non informate
La ricerca iterativa di approfondimento utilizza solo uno spazio lineare
e non molto più tempo di altri algoritmi disinformati
La ricerca a grafo può essere esponenzialmente più efficiente della ricerca ad albero