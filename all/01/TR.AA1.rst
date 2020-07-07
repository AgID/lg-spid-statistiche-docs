.. _`TR.AA1`:

TR.AA1 - Tracciato dati statistici: “Log accessi AA”
====================================================

   ID tracciato: **AA1**

   Descrizione statistica: **Log accessi Attribute Authority** (AA)

   Il tracciato record “Log Accessi Attribute Authority” consente di
   acquisire le informazioni statistiche relative al numero di richieste
   di attributo utente pervenute al soggetto Attribute Authority dai
   rispettivi Service provider.

   Periodicità: **trimestrale** – data di invio acquisita
   automaticamente

Origine: informazioni statistiche fornite dai soggetti Attribute
Authority SPID (AA)

======= =========== ============================================== =========== ==============
**#Id** **Campo**   **Descrizione**                                **formato** **Tipologica**
*AA1.1* *AAid*      Attribute Authority                            String      n/a
*AA1.2* *Entityid*  Ente SP erogatore del servizio                 String      n/a
                                                                              
                    (Soggetto che richiede attributo)                         
*AA1.3* *Timestamp* Data issue instant “Request”                   Data        n/a
                                                                              
                    nel formato UTC: *AAAA-MM-GGThhZ*                         
                                                                              
                    *(granularità limitata all’ora: “hh”) ISO8601*            
*AA1.4* *AuthId*    Identificativo sessione                        String      n/a
======= =========== ============================================== =========== ==============

..

   *Tracciato di esempio*: AA1

====== ========================== =============== ============== =========
**ID** **AA1.1**                  **AA1.2**       **AA1.3**      **AA1.4**
====== ========================== =============== ============== =========
AA1    http://sampleAA            http://sampleSP 2020-01-15T15Z xxnnyy
AA1    http://sampleSPaggregatoAA http://sampleSP 2020-01-15T18Z nnffnn
\      …                          ….                             ….
====== ========================== =============== ============== =========



.. forum_italia::
   :topic_id: XXXXX
   :scope: document
