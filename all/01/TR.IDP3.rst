.. _`TR.IDP3`:

TR.IDP3 - Tracciato “Richieste helpdesk IdP”
============================================

   ID tracciato: **IDP3**

   Descrizione statistica: **Richieste helpdesk Idp**

   Il tracciato consente di acquisire i dati informativi sulle richieste
   di assistenza/supporto pervenute al Gestore IdP tramite il canale
   helpdesk.

   Il numero delle richieste di supporto è aggregato per periodi
   settimanali (intervallo Lun ore 00:00-Dom 23:59) e differenziati
   attraverso le tipologiche: T10, T11 e T12.

   Periodicità: **settimanale** - Il numero degli eventi è riferito al
   periodo settimanale rilevato.

   Origine: informazioni statistiche fornite dai Gestori dell’identità
   digitale SPID (IdP)

======== ================== ================================================================================================================== =========== ==============
**#Id**  **Campo**          **Descrizione**                                                                                                    **formato** **Tipologica**
*IDP3.1* *IdentityProvider* Fornitore di Identità Digitale                                                                                     Numerico    T0
*IDP3.2* *Week*             Settimana di riferimento (val. assoluto 1-52)                                                                      Numerico    -
*IDP3.3* *Year*             Anno                                                                                                               Numerico    -
*IDP3.4* *Channel*          Canale HelpDesk                                                                                                    Numerico    T6
*IDP3.5* *RequestStatus*    Stato Richieste supporto                                                                                           Numerico    T7
*IDP3.6* *SupportCat*       Categoria del supporto                                                                                             Numerico    T8
*IDP3.7* *NumOfReq*         | Numero richieste supporto nel periodo                                                                            Numerico    -
                            | Valore a fine periodo:                                                                                                      
                                                                                                                                                          
                            Es. n. Richieste di supporto registrate nell’intervallo: Lun. ore 00:00 - Dom. ore 23:59 per il rispettivo Status)            
======== ================== ================================================================================================================== =========== ==============

..

   *Tracciato di esempio*: IDP3

====== =========== ========== ========== ========== ========== ========== ==========
**ID** **IDP3.1**  **IDP3.2** **IDP3.3** **IDP3.4** **IDP3.5** **IDP3.6** **IDP3.7**
====== =========== ========== ========== ========== ========== ========== ==========
IDP3   Sample IDPn 52         2020       1          1          1          50
IDP3   Sample IDPn 52         2020       1          2          1          45
\      …           ….                                                    
====== =========== ========== ========== ========== ========== ========== ==========



.. forum_italia::
   :topic_id: XXXXX
   :scope: document
