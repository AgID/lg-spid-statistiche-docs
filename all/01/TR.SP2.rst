.. _`TR.SP2`:

TR.SP2 - Tracciato dati statistici: “Log utenti unici SP privati”
=================================================================

   ID tracciato: **SP2**

   Descrizione statistica: **Log utenti unici SP privati** (SP)

   Il tracciato record “Log utenti unici SP privati” consente di
   acquisire le informazioni statistiche relative al numero di utenti
   che hanno effettuato almeno un accesso al servizio nel corso
   dell’anno di riferimento (utenti unici). Qualora uno stesso utente
   abbia effettuato autenticazioni SPID su più livelli, va computato
   soltanto l’accesso di livello più elevato.

   Periodicità: **annuale** – data di invio acquisita automaticamente

Origine: informazioni statistiche fornite dai fornitori privati di
servizi SPID (SP)

======= ================== ==================================================================================== =========== ==============
**#Id** **Campo**          **Descrizione**                                                                      **formato** **Tipologica**
*SP2.1* *EntityId*\  [14]_ SP erogatore del servizio                                                            String      n/a
*SP2.2* *Year*             Anno                                                                                 String      -
*SP2.3* *NrProcAuth*       Nr. processi di autenticazione SPID                                                  numerico    n/a
                                                                                                                           
                           (utenti unici – lvl1 o 2)                                                                       
*SP2.4* *NrProcReg*        Nr. processi di registrazione SPID                                                   numerico    n/a
                                                                                                                           
                           (utenti unici – lvl 1 o 2)                                                                      
*SP2.5* *NrProcLvl3*       Nr. processi di autenticazione/registrazione SPID - livello 3 (utenti unici – Lvl 3) numerico    n/a
======= ================== ==================================================================================== =========== ==============

..

   *Tracciato di esempio*: SP2

====== ======================== ========= ========= ========= =========
**ID** **SP2.1**                **SP2.2** **SP2.3** **SP2.4** **SP2.5**
====== ======================== ========= ========= ========= =========
SP2    http://sampleSP          2020      845.750   1.450.000 300.000
SP2    http://sampleSPAggregato 2020      1.560.000 1.700.000 800.000
\      …                        ….                           
====== ======================== ========= ========= ========= =========


.. forum_italia::
   :topic_id: XXXXX
   :scope: document
