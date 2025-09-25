# Quaderno di Sistemi e reti - 4I1
In questo quaderno condiviso raccoglieremo gli appunti del laboratorio. Ognuno di voi avrà anche un proprio quaderno personale, dove scriverà i suoi appunti. Nel quaderno condiviso, invece, riporteremo soltanto il riepilogo della lezione precedente e i concetti fondamentali, che da soli non saranno comunque sufficienti.

Il quaderno utilizza un linguaggio di markdown simile a HTML, che ci permette di mantenere una buona formattazione senza doverci concentrare troppo sull'aspetto grafico, così da poterci dedicare principalmente ai contenuti.

## Introduzione alle reti
- Abbiamo capito che per studiare una rete, devo prima dividerla per livelli
- Ogni livello ha una funzionalità particolare e specifica (es. livello fisico si occupa dei collegamenti fisici tra gli host)
- Nello specifico, ci siamo riferiti allo stack protocollare ISO / OSI, ovvero una pila di 7 livelli (standard per lo studio delle reti, insieme all'architettura TCP / IP)
- I livelli (_layer_) che abbiamo visto sono:
    1. Fisico
    2. Collegamento (data link)
    3. Rete
    4. Trasporto
    5. Sessione
    6. Presentazione
    7. Applicazione
- Nello specifico, abbiamo cercato di capire cosa succede fino al livello 3 (compreso). Lo abbiamo fatto usando degli apparati di rete fisici, collegandoli e simulando il traffico (messaggi inviati da un host all'altro)
- Abbiamo quindi definito che per comunicare (nelle reti così come in situazioni sociali), è necessario definire delle regole
- Queste regole si chiamano protocolli, ciascun livello si occupa di alcuni protocolli

## Livello applicativo
