--- 
title: "Diagramma dei Casi d'Uso"
date: 2021-02-15T21:43:46+01:00 # aggiorna data !

draft: false # cambia con false quando viene approvata la versone definitiva !

languageName: "Italiano"
author: ["Giosuè", "Alessio", "Daniel", "Giacomo"] 

tags: ["Requisiti Software"]   
categories: ["Requisiti Software"]   
---  


---
Il diagramma dei casi d'uso è una rappresentazione dell'interazione di un utente con il sistema del software, che mostra la relazione tra l'utente e i diversi casi d'uso in cui esso è coinvolto.

Un diagramma dei casi d’uso può identificare i diversi tipi di utenti di un sistema e viene spesso accompagnato anche da altri tipi di diagrammi.

I casi d'uso specificano il comportamento previsto, ma non il metodo esatto per realizzarlo.

Il concetto chiave del diagramma è progettare un sistema dal punto di vista dell'utente finale.

&nbsp
![Use Case Diagram - Schema_iniziale](/images/UseCaseDiagram/Schema_iniziale.svg)

&nbsp
### Origini del Diagramma dei Casi d'Uso

- Nel 1986, Ivar Jacobson ha formulato per la prima volta tecniche di modellazione testuale e visiva per specificare i casi d'uso.
- Nel 1992 Jacobson pubblica “Object-Oriented Software Engineering - A Use Case Driven Approach”, che ha contribuito a rendere popolare la tecnica per l'acquisizione dei requisiti funzionali, soprattutto nello sviluppo software.

&nbsp
### Scopi e obiettivi del Diagramma dei Casi d'Uso

- Specificare il contesto del sistema in sviluppo
- Comprendere i requisiti del sistema
- Convalidare un'architettura di sistema
- Promuovere l'implementazione e generare casi di test

&nbsp
### Elementi in un diagramma di casi d’uso

- Attore: è qualcuno che interagisce con il caso d’uso ed è nominato da un sostantivo.

&nbsp
    ![Use Case Diagram - Attore](/images/UseCaseDiagram/Attore.svg)
&nbsp

- Caso d’uso: è una funzione del sistema, è rappresentato da verbo + sostantivo.

&nbsp
    ![Use Case Diagram - Caso_dUso](/images/UseCaseDiagram/Caso_dUso.svg)
&nbsp

- Collegamento di associazione: collega un attore a un caso d’uso.

&nbsp
    ![Use Case Diagram - Associazione](/images/UseCaseDiagram/Associazione.svg)
&nbsp

- Confine di sistema: è potenzialmente l’intero sistema, può costituire un confine di sistema per casi d’uso specifici.

&nbsp
### Relazione di generalizzazione

È una relazione padre-figlio tra casi d’uso. Il caso d’uso figlio è un miglioramento del caso d’uso padre.

È rappresentata da una freccia con punta triangolare. Il caso d’uso figlio è collegato alla base della freccia, mentre quello padre è collegato alla punta della freccia.

&nbsp
![Use Case Diagram - Generalizzazione1](/images/UseCaseDiagram/Generalizzazione1.svg)
&nbsp

I caso d’uso figli (Ricerca per numero di telefono/autore) ereditano il comportamento ed il significato del caso d’uso del padre (Ricerca).

Il figlio può aggiungere o sovrascrivere il comportamento del padre.

&nbsp
![Use Case Diagram - Generalizzazione](/images/UseCaseDiagram/Generalizzazione.svg)

&nbsp
### Relazione "include"

Quando un caso d’uso viene descritto come utilizzatore di un altro caso d’uso, la loro relazione si chiama "include".

Una relazione d’uso è rappresentata da una linea tratteggiata e una freccia. La punta indica il processo figlio, mentre alla base si trova il padre.

&nbsp
![Use Case Diagram - Include_3](/images/UseCaseDiagram/Include_3.svg)
&nbsp

La relazione "include" aggiunge funzionalità non specificate nel caso d’uso. Il caso incluso fa parte del comportamento di quello che lo include.

&nbsp
![Use Case Diagram - Include_1](/images/UseCaseDiagram/Include_1.svg)
&nbsp
![Use Case Diagram - Include_2](/images/UseCaseDiagram/Include_2.svg)

&nbsp
### Relazione "extend"

Si scrive "extend" per identificare una relazione di estensione tra due casi d’uso.

Viene raffigurata da una freccia tratteggiata. Alla punta della freccia troviamo il caso base e alla base viene indicato il caso d’uso figlio.

In questo caso il caso d’uso “Invalid password” può includere il comportamento specificato nel caso d'uso di base “Login Account”.

&nbsp
![Use Case Diagram - Extend_3](/images/UseCaseDiagram/Extend_3.svg)
&nbsp

La relazione "extend" mostra funzionalità opzionali, viene usata per includere il comportamento di un caso d’uso facoltativo (Ricerca) in quello base (Richiede un libro).

&nbsp
![Use Case Diagram - Extend_1](/images/UseCaseDiagram/Extend_1.svg)
&nbsp
![Use Case Diagram - Extend_2](/images/UseCaseDiagram/Extend_2.svg)
&nbsp

Include: l’azione viene sempre eseguita durante l’esecuzione del caso d’uso alla base della freccia.

Extend: l’azione può essere eseguita in determinate circostanze del caso d’uso alla punta della freccia.

&nbsp
### Come costruire un modello dei Casi d'Uso

Le informazioni possono essere ricavate dalle interviste con gli utenti. Si identificano gli obiettivi, ovvero quello che il sistema dovrebbe fare secondo gli utenti, e le interazioni, cioè cosa vorrebbero o potrebbero fare i diversi utenti.

I passi principali per la costruzione di un modello dei Casi d'Uso sono:

1. Identificare gli attori
2. Identificare i casi d’uso
3. Definire le associazioni fra attori e casi d’uso
4. Descrivere i casi d’uso
5. Strutturare i casi d’uso

&nbsp
### Identificazione degli attori

Domande utili:

- Chi usa il sistema?
- Chi installa il sistema?
- Chi avvia il sistema?
- Chi mantiene il sistema?
- Chi arresta il sistema?
- Quali altri sistemi utilizzano questo sistema?
- Chi riceve le informazioni da questo sistema?
- Chi fornisce le informazioni al sistema?
- Succede qualcosa automaticamente in questo momento?

Un errore tipico che si commette nell’individuazione degli attori è quello di utilizzare nomi diversi per identificare lo stesso ruolo e quindi lo stesso attore (es. banconista, addetto allo sportello, sportellista).

Questo problema è particolarmente frequente quando uno stesso modello dei casi sia realizzato da diversi team.

Per risolverlo è sufficiente stilare una lista degli attori condivisa che viene aggiornata ogni qualvolta si voglia aggiungere un nuovo attore.

&nbsp
### Identificazione dei casi d’uso

Domande utili:

- Quali funzioni esigerà l'attore dal sistema?
- Il sistema memorizza delle informazioni? Quali attori creeranno, leggeranno, aggiorneranno o cancelleranno queste informazioni?
- Il sistema deve notificare a un attore i cambiamenti nello stato interno?
- Ci sono eventi esterni di cui il sistema deve essere a conoscenza? Quale attore informa il sistema di quegli eventi?

Per ogni attore:

- Identificare i compiti o le funzioni che esso deve essere in grado di eseguire
- Identificare i compiti che il sistema richiede che esso esegua

In seguito è necessario raggruppare i compiti e le funzioni in casi d’uso che:

- Devono corrispondere ad un obiettivo specifico per l’attore o per il sistema
- Devono raggruppare le funzioni che sono eseguite in sequenza o che sono innescate dallo stesso evento
- Non devono essere troppo specifici se non necessario

Infine bisogna assegnare a ogni caso d’uso un nome significativo che sintetizzi le funzionalità svolte.

&nbsp
### Definizione delle associazioni

- Ogni attore deve partecipare in almeno un caso d’uso
- Ogni caso d’uso deve avere almeno un attore con cui comunica
- Se due attori partecipano agli stessi casi d’uso è si può considerare la possibilità di combinarli in un unico attore

&nbsp
### Descrizione dei casi d’uso

- È utile considerare sia lo scenario principale che scenari alternativi ed eccezionali
- Per ogni scenario bisogna specificare:
    - come e quando il caso d’uso inizia
    - chi avvia il caso d’uso
    - l’interazione che c’è tra attore e caso d’uso e cosa viene scambiato
    - come e quando c’è bisogno di memorizzare dati
    - come e quando il caso d’uso termina
- Se sono presenti due casi d’uso che hanno comportamenti leggermente differenti ma hanno gli stessi attori, si può considerare la possibilità di avere un unico caso d’uso con scenari alternativi.

&nbsp
### Strutturazione dei casi d’uso

Identificare le relazioni di generalizzazione e di estensione:

- specializzare i casi d’uso che hanno molti scenari alternativi
- collegare i nuovi casi d’uso a quelli di partenza mediante relazioni di generalizzazione o di "extend"

Identificare le relazioni di inclusione:

- individuare parti comuni in casi d’uso diversi
- collegare i casi d’uso che condividono una parte comune al nuovo caso d’uso (rappresentante il comportamento condiviso) mediante l’associazione "include"

&nbsp
### Esempi di Diagrammi Di Casi d'Uso

#### 1. Servizio passeggeri

&nbsp
![Use Case Diagram - Servizio_passeggeri](/images/UseCaseDiagram/Servizio_passeggeri.svg)
&nbsp

#### 2. Servizio broadcasting

&nbsp
![Use Case Diagram - Sistema_broadcasting](/images/UseCaseDiagram/Sistema_broadcasting.svg)
&nbsp

#### 3. Ristorante

&nbsp
![Use Case Diagram - Ristorante](/images/UseCaseDiagram/Ristorante.svg)
&nbsp

#### 4. Vendita di veicoli

&nbsp
![Use Case Diagram - Sistema_di_vendita_di_veicoli](/images/UseCaseDiagram/Sistema_di_vendita_di_veicoli.svg)
&nbsp 