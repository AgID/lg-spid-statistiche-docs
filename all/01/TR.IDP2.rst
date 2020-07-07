.. _`TR.IDP2`:

TR.IDP2 - Tracciato “Log accessi IdP”
=====================================

   ID tracciato: **IDP2**

   Descrizione statistica: **Log accessi Idp**

   La trasmissione con periodicità almeno settimanale [5]_ delle
   statistiche del tracciato record corrispondente alla “Log accessi
   IdP” consente di acquisire le informazioni statistiche per ogni
   evento: “autenticazione utente”.

   Frequenza: **settimanale** – data di invio acquisita automaticamente

   Origine: informazioni statistiche fornite dai Gestori dell’identità
   digitale SPID (IdP)

======== ================== ============================================================================================================== =========== ==============================
**#Id**  **Campo**          **Descrizione**                                                                                                **formato** **Tipologica**
*IDP2.1* *IdentityProvider* Fornitore di identità Digitale                                                                                 String      T0
*IDP2.2* *EntityId*         Service Provider / Aggregatore                                                                                 String      -
*IDP2.3* *IdentityCode*     Codice associato all’identità                                                                                  String      -
                                                                                                                                                      
                            (univoco per l’IdP [6]_)                                                                                                  
*IDP2.4* *TimeStamp*        Data e ora relativa all’accesso:                                                                               Data        -
                                                                                                                                                      
                            formato UTC: *AAAA-MM-GGThhZ*                                                                                             
                                                                                                                                                      
                            *(granularità limitata all’ora: “hh”) ISO8601*                                                                            
*IDP2.5* *SPIDLevel*        Livello autenticazione SPID                                                                                    Numerico    T11
*IDP2.6* *UserAgent*        Dispositivo richiesta autenticazione                                                                           String      -
*IDP2.7* *AccessType*       Tipo Accesso                                                                                                   Numerico    T10
*IDP2.8* *MsgCode*          codice di ritorno azione di identificazione espresso con Codice “ERROR CODE” da Tabella messaggi anomalia SPID Numerico    Tabella messaggi anomalia SPID
*IDP2.9* *Protocol*         Protocollo utilizzato                                                                                          Numerico    T5
======== ================== ============================================================================================================== =========== ==============================

..

   *Tracciato di esempio*: IDP2

====== ========== ================ ========== ============== ========== ========== ========== ========== ==========
**ID** **IDP2.1** **IDP2.2**       **IDP2.3** **IDP2.4**     **IDP2.5** **IDP2.6** **IDP2.7** **IDP2.8** **IDP2.9**
====== ========== ================ ========== ============== ========== ========== ========== ========== ==========
IDP2   SampleIDPn http://sampleSP  xxxxx      2020-01-15T18Z 21         Chrome     1          1          1
IDP2   IDPn       http://sampleAgg nnyy       2020-01-15T19Z 22         IOS        1          2          1
====== ========== ================ ========== ============== ========== ========== ========== ========== ==========



.. forum_italia::
   :topic_id: XXXXX
   :scope: document
