.. _`TR.SP3`:

TR.SP3 - Tracciato dati statistici: “Log utenti unici SP pubblici”
==================================================================

   ID tracciato: **SP3**

   Descrizione statistica: **Log utenti unici SP pubblici** (SP)

   Il tracciato record “Log utenti unici SP pubblici” consente di
   acquisire le informazioni statistiche relative al numero di utenti
   che hanno effettuato almeno un accesso al servizio nel corso
   dell’anno di riferimento (utenti unici).

   Periodicità: **annuale** – data di invio acquisita automaticamente

Origine: informazioni statistiche fornite dai SP pubblici di servizi
SPID (SP)

======= ================== ================================================================================ =========== ==============
**#Id** **Campo**          **Descrizione**                                                                  **formato** **Tipologica**
*SP3.1* *EntityId*\  [15]_ SP erogatore del servizio                                                        String      n/a
*SP3.2* *Year*             Anno                                                                             String      -
*SP3.3* *NrProcAuth*       Nr. processi di autenticazione SPID – indipendentemente dal livello di sicurezza numerico    n/a
                                                                                                                       
                           (utenti unici)                                                                              
======= ================== ================================================================================ =========== ==============

..

   *Tracciato di esempio*: SP3

====== ======================== ========= =========
**ID** **SP3.1**                **SP3.2** **SP3.3**
====== ======================== ========= =========
SP3    http://sampleSP          2020      845.750
SP3    http://sampleSPAggregato 2020      560.000
\      …                        ….       
====== ======================== ========= =========


.. forum_italia::
   :topic_id: XXXXX
   :scope: document
