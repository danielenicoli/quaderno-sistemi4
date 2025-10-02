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
- L'application layer ci permette di utilizzare le applicazioni della rete
- Di conseguenza avremo uno o più protocolli L7 per ciascuna applicazione della rete
    - HTTP per lo scambio di documenti (pagine) web
    - SMTP per l'invio di messaggi di posta elettronica
    - DNS per la risoluzione di nomi a dominio
    - FTP per il trasferimento di file
    - SNMP (Simple Network Management Protocol), serve per il monitoraggio e la configurazione di dispositivi di rete
    - ...

### HTTP
Iniziamo a studiare il protocollo HTTP, perchè è quello che usiamo più di frequente:
- È un procollo di tipo client-server
    - Il client (l'utente, normalmente attraverso il browser) richiede una risorsa a un server web (pagina web, un documento, un'immagine, ...)
    - Il server (web server o server http), fornisce una risposta al client
        - Normalmente la risposta è un documento HTML
- Abbiamo quindi disegnato lo schema di funzionamento, in cui troviamo
    - HTTP request
    - HTTP response
- HTTPS aggiunge al protocollo HTTP un livello di sicurezza, questa sicurezza consiste nel rendere illeggibile a terzi il contenuto del pacchetto
    - Di conseguenza non va bene per il nostro scopo (ovvero quello di studiare il funzionamento dei protocolli)
- Stiamo quindi analizzando un pacchetto HTTP, che è composto da queste parti
    - Header (intestazione)
        - Method
            - GET per la richiesta di una risorsa
            - POST per l'invio di una risorsa
            - PUT / PUSH per la modifica di una risorsa
            - DELETE per la cancellazione di una risorsa
            - OPTION per visualizzare i metodi accettati da quell'URL
            - HEAD per ottenere come risposta una intestazione dal server (senza payload)
    - Payload (corpo), che è opzionale
- Le risposte HTTP producono uno status code numerico, che può essere di 5 categorie
    - 1xx - Informazione
    - 2xx - Successo
    - 3xx - Redirect
    - 4xx - Problema lato client
    - 5xx - Problema lato server