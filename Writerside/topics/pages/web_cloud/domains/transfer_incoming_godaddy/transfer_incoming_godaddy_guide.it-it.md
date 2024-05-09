---
title: 'Trasferire un dominio GoDaddy in OVHcloud'
excerpt: 'Questa guida ti mostra tutte le informazioni relative al trasferimento di un dominio GoDaddy in OVHcloud'
updated: 2024-04-10
---

> [!primary]
> Questa traduzione è stata generata automaticamente dal nostro partner SYSTRAN. I contenuti potrebbero presentare imprecisioni, ad esempio la nomenclatura dei pulsanti o alcuni dettagli tecnici. In caso di dubbi consigliamo di fare riferimento alla versione inglese o francese della guida. Per aiutarci a migliorare questa traduzione, utilizza il pulsante "Contribuisci" di questa pagina.
>

## Obiettivo

Il trasferimento di un dominio GoDaddy richiede una procedura specifica.

**Questa guida ti mostra come trasferire un dominio GoDaddy in OVHcloud**

> [!warning]
>
> Il [Registrar](domains-what-is-registrar.) di un dominio rappresenta l'organizzazione/provider accreditata presso la quale il dominio è registrato/sottoscritto da un privato, un'associazione o un'organizzazione. È presso lo stesso Registrar che rinnovi la sottoscrizione del tuo dominio (generalmente una volta all'anno).
>
> Se OVHcloud è già il Registrar del tuo dominio **prima** di avviare la procedura che seguirà, il trasferimento in entrata del dominio non è la procedura appropriata. La procedura trasferimento in entrata da un dominio si applica **solo** ai domini registrati in un altro Registrar di OVHcloud.
>
> Per trasferire la gestione del tuo dominio verso un altro account cliente OVHcloud, la modalità corretta è una modifica dei contatti. La procedura è descritta in [guida](managing_contacts1.).
>
> Se è necessario modificare il **proprietario** del dominio, è necessario farlo **prima** di modificare i contatti del dominio. Segui le istruzioni descritte nella nostra guida sul [cambiamento di proprietario dei domini](trade_domain1.).
>

## Prerequisiti

- il dominio è registrato presso il Registrar GoDaddy.
- il dominio esiste da più di 60 giorni.
- Il dominio non è stato trasferito o non ha cambiato proprietario nel corso degli ultimi 60 giorni.
- Lo stato del dominio è "OK" o "Trasferibile".
- il dominio non è scaduto e ha una data di scadenza che permette di completare il processo di trasferimento entro i termini (consigliato: oltre 60 giorni).

È inoltre necessario:

- Essere in grado di sbloccare il dominio.
- essere in possesso del codice di trasferimento o avere la possibilità di recuperarlo.
- essere abilitato a richiedere il trasferimento del dominio.
- Aver informato il proprietario del dominio e/o i suoi amministratori della richiesta di trasferimento.

> [!warning]
>
> OVHcloud mette a disposizione i servizi ma non si occupa della loro configurazione e gestione. garantirne il corretto funzionamento è quindi responsabilità dell’utente.
>
> Questa guida ti aiuta a eseguire le operazioni necessarie alla configurazione del tuo account. Tuttavia, in caso di difficoltà o dubbi, ti consigliamo di contattare un [provider specializzato](partner.) o il tuo attuale provider. OVH non sarà infatti in grado di fornirti assistenza. Per maggiori informazioni consulta la sezione [Per saperne di più](transfer_incoming_godaddy_#go-further.) di questa guida.
>

# Procedura

> [!primary]
>
> La zona DNS attiva di un dominio contiene la configurazione DNS applicata al dominio. che collega il dominio a servizi come gli indirizzi email o un sito Web.
>
> Se, oltre al dominio, disponi di una zona DNS attiva presso il tuo attuale Registrar, verifica che la zona DNS applicata non venga eliminata una volta effettuato il trasferimento.
>
> Alcuni Registrar eliminano la zona DNS in loro possesso al termine del trasferimento del dominio. In questo caso, ricrea la zona DNS in OVHcloud prima di avviare le azioni associate al trasferimento del dominio.
>
> Per farlo, consulta queste guide:
>
> - [Creare una zona DNS in OVHcloud](dns_zone_create1.)
> - [Modificare una zona DNS in OVHcloud](dns_zone_edit1.)
>
> Assicurati che il tuo attuale Registrar non chiuda altri servizi, ad esempio gli indirizzi email associati al dominio.
>

### Step 1 - Sblocca il dominio in GoDaddy

Il blocco di un dominio lo protegge contro i tentativi di trasferimento non autorizzati.
GoDaddy attiva questa protezione predefinita. Per trasferire il dominio in OVHcloud è necessario disattivarla.

Segui gli step descritti nella [documentazione dedicata di GoDaddy](https://it.godaddy.com/help/sblocca-o-blocca-il-mio-dominio-410){.external}.

### Step 2 - Ottieni il codice di autorizzazione 

OVHcloud chiederà il codice di autorizzazione o "Auth code" prima di avviare la procedura di trasferimento del dominio. Puoi ottenerlo aprendo la pagina del tuo portfolio di `Domini`{.action} in GoDaddy.

Segui gli step descritti nella [documentazione dedicata di GoDaddy](https://it.godaddy.com/help/trasferimento-del-dominio-da-godaddy-3560){.external}.

### Step 3 - Inizia il trasferimento di dominio in OVHcloud

Una volta ottenuto il codice di autorizzazione, è possibile procedere al trasferimento del dominio seguendo gli step indicati nella nostra guida "[Trasferire un dominio in OVHcloud](transfer_incoming_generic_domain1.)".

## Per saperne di più <a name="go-further"></a>

[Trasferire un dominio in OVHcloud](transfer_incoming_generic_domain1.)

[Migrare il proprio sito Web e le proprie email in OVHcloud](hosting_migrating_to_ovh1.)

Per prestazioni specializzate (referenziamento, sviluppo, ecc...), contatta i [partner OVHcloud](partner.).

Per usufruire di un supporto per l'utilizzo e la configurazione delle soluzioni OVHcloud, è possibile consultare le nostre soluzioni [offerte di supporto](support.).

Contatta la nostra Community di utenti all'indirizzo <https://community.ovh.com/en/>.