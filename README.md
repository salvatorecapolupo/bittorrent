* Simulatore bittorrent online
https://salvatorecapolupo.github.io/bittorrent/


# Spiegazione della simulazione BitTorrent

Questa simulazione rappresenta il funzionamento del protocollo **BitTorrent**, un sistema di condivisione **peer-to-peer (P2P)**.

Ogni elemento grafico dell’animazione corrisponde a un concetto teorico studiato in **Sistemi e Reti / TPSIT**.

---

## Percentuale visualizzata nei peer

La percentuale mostrata all’interno di ogni peer indica:

(percentuale) = (numero di chunk posseduti / numero totale di chunk) × 100

- **0%** → il peer non possiede nessun pezzo del file  
- **50%** → il peer possiede metà dei pezzi  
- **100%** → il peer possiede il file completo

---

## Peer

Un **peer** è un computer collegato alla rete BitTorrent.

Caratteristiche:
- può **scaricare** chunk
- può **caricare** chunk
- svolge contemporaneamente il ruolo di *client* e *server*

---

## Seed

Un **seed** è un peer che:
- possiede **tutti i chunk** del file
- ha quindi il **100%** della percentuale

Nella simulazione:
- è rappresentato in **verde**
- serve per avviare la diffusione del file nello swarm

---

## Leecher

Un **leecher** è un peer che:
- non possiede ancora il file completo
- continua comunque a **condividere i chunk già scaricati**

Nella simulazione:
- è rappresentato in **giallo**
- la sua percentuale cresce nel tempo

---

## Chunk (pezzi di file)

Il file non viene trasferito interamente, ma diviso in **chunk**.

Vantaggi:
- download parallelo da più peer
- maggiore velocità
- maggiore tolleranza ai guasti

Ogni peer possiede un insieme diverso di chunk.

---

## Scambio di chunk

Le **linee blu** che compaiono tra due peer indicano:
- il trasferimento di un chunk
- un’operazione di upload + download simultanei

Questo mostra il principio fondamentale del P2P:
> chi scarica, condivide

---

## Swarm

Lo **swarm** è:
- l’insieme di tutti i peer che condividono lo stesso file
- una rete distribuita senza server centrale

Più grande è lo swarm:
- più veloce è il download
- più affidabile è la rete

---

## Affidabilità del sistema

La simulazione mostra che:
- se un peer si disconnette, gli altri continuano
- non esiste un punto singolo di fallimento

Questo rende BitTorrent:
- **scalabile**
- **resistente**
- **efficiente**

---

## Sintesi finale

- BitTorrent è un sistema **distribuito**
- ogni peer collabora allo scambio
- la percentuale rappresenta lo stato di avanzamento del download
- la rete migliora con l’aumentare dei peer
