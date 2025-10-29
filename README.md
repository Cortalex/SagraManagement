# SagraManagement

##  **Progetto: Applicazione desktop per la gestione ordini di una sagra**

###  **Obiettivo**

Creare un’applicazione desktop completa per la gestione degli ordini durante una sagra o evento gastronomico.
Il sistema dovrà consentire la creazione, la stampa e la visualizzazione degli ordini in tempo reale, oltre a offrire funzionalità di magazzino, statistiche e gestione multi postazione (server-client).

---

###  **Schermata principale**

* Creazione rapida di un **nuovo ordine**.
* Possibilità di selezionare **articoli, quantità, e note aggiuntive**.
* Visualizzazione immediata del **totale** e gestione del **pagamento (contanti, POS, ecc.)**.
* Opzione per associare l’ordine a un **tavolo o numero cliente**, se richiesto.
* Bottone per l’invio dell’ordine in stampa nei vari reparti.

---

###  **Sottosezioni principali**

1. **Articoli e tipologie**

   * Inserimento e modifica degli articoli.
   * Categorie.
   * Prezzo, reparto di stampa associato, disponibilità.

2. **Magazzino**

   * Gestione scorte e aggiornamento automatico dopo ogni ordine.
   * Alert automatico in caso di scorte basse.
   * Possibilità di import/export da file CSV o Excel.

3. **Reparti e stampanti**

   * Configurazione dei reparti.
   * Associazione di **una stampante diversa per ogni reparto**.
   * Test stampa e impostazioni di layout (opzionale anteprima di stampa).

4. **Resoconti e statistiche**

   * Visualizzazione degli ordini giornalieri o per intervallo di date.
   * Statistiche per articolo, reparto o fascia oraria.
   * Esportazione dei dati in PDF o Excel.

---

###  **Configurazioni**

* Tutte le configurazioni (articoli, reparti, stampanti, rete, ecc.) vengono salvate in un **file locale** (es. JSON o XML) per essere facilmente trasferibili e modificabili.
* Opzione per **backup automatico** del database locale.

---

### **Gestione stampa automatica**

* Ogni ordine, al momento della conferma, viene **smistato automaticamente** alle stampanti dei vari reparti in base agli articoli selezionati.
* Possibilità di definire se l’ordine deve essere stampato subito o solo dopo conferma.

---

###  **Web Server integrato**

* Possibilità di attivare un **server web locale** (basato su Node.js o Python Flask integrato).
* Accesso via browser (`http://ipserver:porta`) per visualizzare:

  * Lista ordini in preparazione.
  * Stato degli ordini (in coda, in preparazione, completato).
  * Filtro per reparto o tavolo.
* Modalità “solo visualizzazione” per schermi o tablet nei reparti.

---

### **Modalità multi-client**

* L’app può funzionare sia in **modalità stand alone** che in **rete locale**:

  * Un PC principale funge da **server** (gestione database, stampa, web server).
  * Gli altri PC (postazioni cassa) si collegano come **client**.
* Connessione tramite **indirizzo IP locale** e **porta configurabile**.
* Riconnessione automatica in caso di disconnessione.

---

###  **Gestione da dispositivi mobili **

* Tramite interfaccia tramite mini app dedicata:

  * Possibilità di **associare un numero ordine a un tavolo** o di **inserire ordini** da smartphone o palmare.
  * L’ordine viene inviato in stampa solo dopo conferma.

---

###  **Funzionalità secondarie**

* **Log attività**: registro di modifiche, ordini stampati, errori di rete o stampante.

---

###  **Tecnologie usate**

* **Linguaggio:** C# (.NET 8)
* **Database:** PostgreSQL o SQLite (per versione stand-alone)
* **Backend web integrato:** Kestrel (nativo .NET) o Node.js
* **Comunicazione client-server:** API REST o TCP
* **File configurazione:** JSON
* **Interfaccia mobile:**  mini app Flutter


