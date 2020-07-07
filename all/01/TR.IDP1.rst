.. _`TR.IDP1`:

TR.IDP1 - Tracciato “Identità digitali”
==========

   ID tracciato: **IDP1**

   Descrizione statistica: **Identità digitali**

   La trasmissione con periodicità almeno settimanale [1]_ delle
   statistiche del tracciato record relativo alle “Identità digitali”
   mira ad acquisire le informazioni statistiche per ogni richiesta (o
   cambio stato) di “\ *Identità SPID”*.

   Frequenza: **settimanale** – data di invio acquisita automaticamente

   Origine: informazioni statistiche fornite dai Gestori dell’identità
   digitale SPID (IdP)

========= ====================== ===================================================================================== =========== ==============
**#Id**   **Campo**              **Descrizione**                                                                       **formato** **Tipologica**
*IDP1.1*  *IdentityProvider*     Fornitore di Identità Digitale                                                        String      T0
*IDP1.2*  *IdentityCode*\  [2]_  Codice associato all’identità (univoco per l’IdP)                                     String     
*IDP1.3*  *Day*                  giorno di riferimento evento registrato/cambio stato (valore assoluto: 1-366)         Num         -
*IDP1.4*  *Year*                 Anno (YYYY)                                                                           Num         -
*IDP1.5*  *IdStatus*             Stato dell’identità                                                                   Num         T1
*IDP1.6*  *RecogMethod*          Modalità di riconoscimento (per *IdStatus* =2)                                        Num         T2
*IDP1.7*  *placeOfBirth*         Luogo di nascita (per *IdStatus* =2)                                                  String      T3
*IDP1.8*  *countyOfBirth*\  [3]_ Provincia di nascita (per *IdStatus* =2)                                              String     
*IDP1.9*  *yearOfBirth*          Anno di nascita - (per *IdStatus* =2)                                                 Num        
                                                                                                                                  
                                 Sottostringa YYYY di DateOfBirth “YYYY-MM-DD”                                                    
*IDP1.10* *DomicilieCode*\  [4]_ Contiene il “Luogo” di domicilio fisico utente                                        String      T3
                                                                                                                                  
                                 (per *IdStatus* =2)                                                                              
                                                                                                                                  
                                 (sottostringa di ADDRESS nella forma codice catastale) – (valorizzato se disponibile)            
*IDP1.11* *Gender*               Sesso - (per *IdStatus* =2) (M o F)                                                   String      -
*IDP1.12* *UserType*             Tipologia utente                                                                      Num         T4
*IDP1.13* *ReleaseTime*          Tempo rilascio espresso in ore da momento richiesta a prima condizione *IdStatus=2*   Num         -
                                                                                                                                  
                                 (num. ore approssimato per eccesso)                                                              
========= ====================== ===================================================================================== =========== ==============

..

   *Tracciato di esempio*: IDP1

====== =========== ========== ========== ========== ========== ========== ========== ==========
**ID** **IDP1.1**  **IDP1.2** **IDP1.3** **IDP1.4** **IDP1.5** **IDP1.6** **IDP1.7** **IDP1.8**
====== =========== ========== ========== ========== ========== ========== ========== ==========
IDP1   Sample IDPn xxxxx      013        2020       3          5          IT-H501    RM        
IDP1   Sample IDPn …..        21         2020       2          5          IT-L701    VR        
IDP1   Sample IDPn xxxyy      nnn        2020       2          4          IT-A944    BO        
\      ……          ….                                                     -          EE        
====== =========== ========== ========== ========== ========== ========== ========== ==========

== ========== =========== =========== =========== ===========
\  **IDP1.9** **IDP1.10** **IDP1.11** **IDP1.12** **IDP1.13**
== ========== =========== =========== =========== ===========
\  1999       IT-M082     M           1           52
\  1961       IT-G224     F           1           25
\  1981       IT-A944     M           3           36
\  1975       US          M           3           32
== ========== =========== =========== =========== ===========


.. forum_italia::
   :topic_id: XXXXX
   :scope: document
