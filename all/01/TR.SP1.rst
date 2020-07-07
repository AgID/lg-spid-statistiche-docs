.. _`TR.SP1`:

TR.SP1 – Tracciato “Log accessi SP”
===================================

   ID tracciato: **SP1**

   Descrizione statistica: **Log accessi SP** (SP)

   La trasmissione del tracciato record corrispondente alla “Log accessi
   SP” consente di acquisire le informazioni statistiche per ogni evento
   corrispondente all’accesso al servizio inteso come nuova sessione.

   Periodicità: **settimanale**\  [10]_ – data di invio acquisita
   automaticamente

Origine: informazioni statistiche fornite dai fornitori di servizi SPID
(SP)

======= ================== =============================================================================================================================================== =========== =========================
**#Id** **Campo**          **Descrizione**                                                                                                                                 **formato** **Tipologica**
*SP1.1* *EntityId*\  [11]_ SP erogatore o SP aggregato (pubblico o privato)                                                                                                String      -
                                                                                                                                                                                      
                           Identifica sempre il Soggetto erogatore del servizio. Nel caso di Soggetto aggregato, il campo deve contenere l'EntityID del soggetto aggregato            
*SP1.2* *AuthId*\  [12]_   Identificativo sessione                                                                                                                         String      n/a
*SP1.3* *TimeStamp*        Data e ora relativa all’accesso:                                                                                                                Data        -
                                                                                                                                                                                      
                           formato UTC: *AAAA-MM-GGThhZ*                                                                                                                              
                                                                                                                                                                                      
                           *(granularità limitata all’ora: “hh”) ISO8601*                                                                                                             
*SP1.4* *ServiceCat*       *Categoria (ambito di applicazione del servizio erogato)                                                                                        String      T12
                           Rif. COFOG-2009*                                                                                                                                           
                                                                                                                                                                                      
                           afferisce al servizio per il quale si richiede l’autenticazione                                                                                            
*SP1.5* *MsgCode*\  [13]_  Codice di ritorno azione di identificazione espresso con Codice “ERROR CODE” da Tabella messaggi anomalia SPID                                  Numerico    Tabella messaggi anomalia
======= ================== =============================================================================================================================================== =========== =========================

..

   *Tracciato di esempio*: SP1

====== ======================== ========= ================ ========= =========
**ID** **SP1.1**                **SP1.2** **SP1.3**        **SP1.4** **SP1.5**
====== ======================== ========= ================ ========= =========
SP1    http://sampleSP          xxnnyy    *2019-11-29T08Z* 1         1
SP1    http://sampleSPAggregato nnffnn    *2019-11-29T09Z* 2         2
\      …                                                            
====== ======================== ========= ================ ========= =========



.. forum_italia::
   :topic_id: XXXXX
   :scope: document
