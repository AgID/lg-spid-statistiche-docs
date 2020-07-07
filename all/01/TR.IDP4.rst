.. _`TR.IDP4`:

TR.IDP4 - Tracciato “Indicatori di qualità”
===========================================

   ID tracciato: **IDP4**

   Descrizione statistica: **Indicatori di qualità** del servizio di
   autenticazione (Idp)

   Il tracciato consente di acquisire dati informativi relativi agli
   indici di qualità e ai livelli del servizio dei vari sotto-servizi
   già trasmesso trimestralmente/annualmente nell’ambito degli obblighi
   derivanti dalla Convenzione SPID sottoscritta dal Gestore Idp.

   Periodicità: **trimestrale** – data di invio acquisita
   automaticamente

======== ================== =================================================================================== =========== ==============
**#Id**  **Campo**          **Descrizione**                                                                     **formato** **Tipologica**
*IDP4.1* *IdentityProvider* Fornitore di Identità Digitale                                                      Numerico    T0
*IDP4.2* *Trimestre*        Trimestre                                                                           Numerico    -
                                                                                                                           
                            *(val. assoluto 1-4)*                                                                          
*IDP4.3* *Year*             Anno                                                                                Numerico    -
*IDP4.4* *IdcodeQ*          Codice univoco Indicatore Indice di qualità (IQ-xx)                                 *Numerico*  T9
                                                                                                                           
                            *(codice univoco tra 1 e 25)*                                                                  
*IDP4.5* *Value*            Valore rilevato *(calcolato secondo algoritmo e regole di arrotondamento previste)* *Numerico*  -
======== ================== =================================================================================== =========== ==============

Origine: informazioni statistiche fornite dai Gestori dell’identità
digitale SPID (IdP)

   *Tracciato di esempio*: IDP4

====== =========== ========== ========== ========== ==========
**ID** **IDP4.1**  **IDP4.2** **IDP4.3** **IDP4.4** **IDP4.5**
====== =========== ========== ========== ========== ==========
IDP4   Sample IDPn 1          2020       1          0,98 [7]_
IDP4   Sample IDPn 1          2020       2          10 [8]_
\      Sample IDPn 1          2020       8          3 [9]_
…      ….          …          ….         …          …
====== =========== ========== ========== ========== ==========



.. forum_italia::
   :topic_id: XXXXX
   :scope: document
