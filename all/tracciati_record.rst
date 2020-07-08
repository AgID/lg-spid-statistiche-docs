.. _`TR.AA1`:

Tracciati record
================

.. _`TR.IDP1`:

TR.IDP1 - Tracciato “Identità digitali”
---------------------------------------

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

.. _`TR.IDP2`:

TR.IDP2 - Tracciato “Log accessi IdP”
-------------------------------------

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


.. _`TR.IDP3`:

TR.IDP3 - Tracciato “Richieste helpdesk IdP”
--------------------------------------------

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


.. _`TR.IDP4`:

TR.IDP4 - Tracciato “Indicatori di qualità”
-------------------------------------------

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


.. _`TR.SP1`:

TR.SP1 – Tracciato “Log accessi SP”
-----------------------------------

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


.. _`TR.SP2`:

TR.SP2 - Tracciato dati statistici: “Log utenti unici SP privati”
-----------------------------------------------------------------

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


.. _`TR.SP3`:

TR.SP3 - Tracciato dati statistici: “Log utenti unici SP pubblici”
------------------------------------------------------------------

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


TR.AA1 - Tracciato dati statistici: “Log accessi AA”
----------------------------------------------------

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


.. _`tipolTracc`:

Valori tipologici dei tracciati
-------------------------------

I valori tipologici, di seguito riportati, servono a normalizzare i dati
al fine di omogeneizzare le statistiche; Qualora le tipologie non
corrispondano, è opportuno effettuare un’operazione di *lookup* al fine
dell’estrazione dei dati in modo da non dover comportare una modifica
dei sistemi in uso;

-  **T0 – Denominazione Identity Provider**

-  **T1 – Stato delle identità**

-  **T2 – Modalità di riconoscimento**

-  **T3 – Comune/Stato estero**

-  **T4 – Tipologia utente**

-  **T5 – Protocollo**

-  **T6 - Canale helpdesk**

-  **T7- Stato richiesta di supporto**

-  **T8 - Categorie di supporto**

-  **T9 – Codice indicatore Indice di Qualità**

-  **T10 - Tipologia Accesso**

-  **T11 – Livello SPID**

-  **T12 – Categoria servizio erogato**

T0 - Identity Provider

*< IdentityProvider >*

stringa corrispondente alla “Denominazione” del “\ *Gestore
dell’identità*\ ” come presente sull’Elenco pubblico degli IdP
accreditati sul sito istituzionale AgID.

T1 – Stato delle identità

======== ==================================================================================
**Cod.** **Descrizione**
**1**    In lavorazione – identità in corso di completamento della procedura di attivazione
        
         *(comprese quelle richieste in periodi precedenti)*
**2**    Attive – identità attive non revocate e non in lavorazione
**3**    Revocate (identità disattivate nel periodo)
======== ==================================================================================

T2 - Modalità di riconoscimento (rilascio identità digitali)

======== =====================================================
**Cod.** **Canale di riconoscimento**
**1**    Online con identità pregresse - CIE
**2**    Online con identità pregresse - CNS
**3**    Online con Firma Elettronica Qualificata
**4**    Riconoscimento fisico via WebCam
**5**    Riconoscimento fisico via Sportello/operatore/ufficio
**6**    RAO pubblico
**7**    Altro
======== =====================================================

T3 – Comune/Stato estero

Nel caso di comuni italiani, il campo sarà costituito dal prefisso
**IT-** seguito dal codice catastale del comune, come indicato
all'archivio storico dei comuni presente sul sito ANPR
(https://www.anpr.interno.it). Es.: **IT-H501**

Nel caso di città estere, il campo sarà costituito dal codice ISO 3166-1
alpha-2 dello stato estero. Esempio: **US**

T4 –Tipologia utente

======== ===============================================
**Cod.** **Descrizione**
**1**    Persona fisica
**2**    Persona giuridica
**3**    Uso professionale
**4**    Uso professionale associato a Persona Giuridica
======== ===============================================

T5 – Protocollo

======== ===============
**Cod.** **Descrizione**
**1**    SAML
**2**    OpenIDConnect
======== ===============

T6 - Canale helpdesk

======== ===========================================================
**Cod.** **Descrizione**
**1**    Telefono
**2**    Online asincrono (ticket, PEC, mail, ecc.)
**3**    Online sincrono (chat testuale/webcam, altri canali online)
**4**    Presso ufficio / sportello
======== ===========================================================

T7 - Stato richieste di supporto

======== ====================================
**Cod.** **Descrizione**
**1**    Aperte (nel periodo)
**2**    Chiuse (lavorate/chiuse nel periodo)
**3**    Pendenti (nel periodo)
======== ====================================

T8 - Categorie di supporto

======== ========================
**Cod.** **Descrizione**
**1**    Assistenza informativa
**2**    Rilascio identità
**3**    Utilizzo identità
**4**    Sospensione identità
**5**    Revoca identità
**6**    Gestione degli attributi
**7**    Errori e malfunzioni
**8**    Altro
======== ========================

T9 – Codice indicatore *Indici di Qualità*\  [16]_

======== ============ ============================================================================ ========================== ==============================================
**Cod.** **ID All.3** **Indicatore di qualità**                                                    **Modalità funzionamento** **Tipologia Limite**
*1*      *IQ01*       Disponibilità del sotto-servizio di registrazione identità                   Erogazione Automatica      Tempo totale di disponibilità
*2*      *IQ01*       Disponibilità del sotto-servizio di registrazione identità                   Erogazione Automatica      Durata massimo evento di indisponibilità
*3*      *IQ01*       Disponibilità del sotto-servizio di registrazione identità                   Erogazione in Presenza     Tempo totale di disponibilità
*4*      *IQ02*       Tempo di risposta del sotto-servizio di registrazione identità               Null                       Null
*5*      *IQ03*       Disponibilità del sotto-servizio di gestione rilascio credenziali            Erogazione Automatica      Tempo Totale di disponibilità
*6*      *IQ03*       Disponibilità del sotto-servizio di gestione rilascio credenziali            Erogazione Automatica      Durata massimo evento di indisponibilità (ore)
*7*      *IQ03*       Disponibilità del sotto-servizio di gestione rilascio credenziali            Erogazione in Presenza     Tempo Totale di disponibilità
*8*      *IQ04*       Tempo di rilascio credenziali                                                Null                       Null
*9*      *IQ05*       Tempo riattivazione delle credenziali                                        Null                       Null
*10*     *IQ06*       Disponibilità del sotto-servizio di sospensione e revoca delle credenziali   Null                       Tempo totale di disponibilità
*11*     *IQ06*       Disponibilità del sotto-servizio di sospensione e revoca delle credenziali   Null                       Durata massimo evento di indisponibilità
*12*     *IQ07*       Tempo di sospensione delle credenziali                                       Null                       Null
*13*     *IQ8*        Tempo di revoca delle credenziali                                                                      
*14*     *IQ9*        Disponibilità del sotto-servizio di rinnovo e sostituzione delle credenziali Erogazione automatica      Null
*15*     *IQ9*        Disponibilità del sotto-servizio di rinnovo e sostituzione delle credenziali Erogazione in presenza     Null
*16*     *IQ10*       Tempo di rinnovo e sostituzione delle credenziali                            Null                       Null
*17*     *IQ11*       Disponibilità del sotto-servizio di autenticazione                           Null                       Tempo totale di disponibilità
*18*     *IQ11*       Disponibilità del sotto-servizio di autenticazione                           Null                       Durata massimo evento di indisponibilità
*19*     *IQ12*       Tempo di risposta del sotto-servizio di autenticazione                       Null                       Null
*20*     *IQ13*       RPO sotto-servizio registrazione e rilascio delle identità                   Null                       Null
*21*     *IQ14*       RTO sotto-servizio registrazione e rilascio delle identità                   Null                       Null
*22*     *IQ15*       RPO sotto-servizio di sospensione e revoca delle credenziali                 Null                       Null
*23*     *IQ16*       RTO sotto-servizio di sospensione e revoca delle credenziali                 Null                       Null
*24*     *IQ17*       RPO sotto-servizio di Autenticazione                                         Null                       Null
*25*     *IQ18*       RTO sotto-servizio di Autenticazione                                         Null                       Null
======== ============ ============================================================================ ========================== ==============================================

T10 - Tipologia accesso

======== ===========================
**Cod.** **Descrizione**
**1**    Autenticazione
**2**    Ex Art.20 comma 1 bis (CAD)
**3**    Autenticazione minori
**4**    Altro
======== ===========================

T11 – Livello SPID

======== ============================
**Cod.** **Descrizione**
**10**   Livello 1
**21**   Livello 2 con SMS
**22**   Livello 2 con App
**23**   Livello 2 con altro
**31**   Livello 3 con CIE
**32**   Livello 3 con CNS
**33**   Livello 3 con Firma digitale
**34**   Livello 3 con Firma remota
**35**   Livello 3 con altro
======== ============================

T12 – Categoria servizio erogato

======== ================================================
**Cod.** **Descrizione ambito del servizio**
**1**    SERVIZI GENERALI DELLE PUBBLICHE AMMINISTRAZIONI
**2**    DIFESA
**3**    ORDINE PUBBLICO E SICUREZZA
**4**    AFFARI ECONOMICI
**5**    PROTEZIONE DELL'AMBIENTE
**6**    ABITAZIONI E ASSETTO TERRITORIALE
**7**    SANITà
**8**    ATTIVITA' RICREATIVE, CULTURALI E DI CULTO
**9**    ISTRUZIONE
**10**   PROTEZIONE SOCIALE
**11**   SERVIZI DA SP PRIVATI
**12**   ALTRO
======== ================================================

.. [1]
   La periodicità indicata corrisponde all’intervallo minimo di
   trasmissione. Tuttavia il soggetto incaricato di trasmettere i dati
   statistici, può stabilire – p.es. sulla base di proprie esigenze
   tecnico-organizzative - intervalli ridotti di trasmissione fino alla
   trasmissione in modalità giornaliera o continua (se consentita dal
   canale).

.. [2]
   **IdentityCode**\ \ \ *:* Codice univoco in ambito IdP, creato
   autonomamente dall’IdP e associato a ciascuna identità digitale
   rilasciata dal medesimo IdP. AgID non dispone di alcuna modalità per
   poter risalire all’identità dell’utente. Non può essere utilizzato lo
   *SPIDCode* poiché consentirebbe di risalire all’identità digitale.

.. [3]
   Se *PlaceOfBirth* (Luogo di nascita) corrisponde a luogo estero,
   questo viene valorizzato con Nazione estera di nascita (v.Tabella
   attributi) e il campo **CountyOfBirth** viene valorizzato con
   “\ \ **EE**\ \ ” (v.Avviso SPID n.26)

.. [4]
   Ai fini statistici il dato che si vuole acquisire con
   **DomicilieCode** corrisponde al LUOGO di domicilio fisico. Nelle
   more dell’adozione delle indicazioni ai Gestori IDP emanate da AgID
   con l’Avviso SPID n.25, il luogo di domicilio fisico nella forma
   indicata dalla relativa tipologica, sarà estratto dalla stringa
   **address**\ \ \ *che* è composta da una sequenza di sottostringhe
   non vuote intervallate da uno (solo) spazio (v.Tabella attributi).
   Con l’adozione dell’Avviso SPID n.25, **DomicilieCode** corrisponderà
   al contenuto dell’attributo *DomicilieMunicipality* espresso nella
   forma del Codice catastale preceduto da identificativo Nazione (v.
   codice ISO 3166-1 alpha-2) Es. IT-H501. Per domicilio estero viene
   valorizzato solo con l’identificativo Nazione secondo codice ISO
   3166-1 alpha-2.

.. [5]
   La periodicità indicata corrisponde all’intervallo minimo di
   trasmissione. Tuttavia il soggetto incaricato di trasmettere i dati
   statistici, può stabilire – p.es. sulla base di proprie esigenze
   tecnico-organizzative - intervalli ridotti di trasmissione fino alla
   trasmissione in modalità giornaliera o continua (se consentita dal
   canale).

.. [6]
   **IdentityCode**: Codice univoco in ambito IdP, creato autonomamente
   dall’IdP e associato a ciascuna identità digitale rilasciata dal
   medesimo IdP. AgID non dispone di alcuna modalità per poter risalire
   all’identità dell’utente. Non può essere utilizzato lo *SPIDCode*
   poiché consentirebbe di risalire all’identità digitale

.. [7]
   Valore percentuale relativo al tempo totale di disponibilità del
   sotto-servizio di registrazione identità (indicatore IQ-01
   dell’Allegato 3 della Convenzione SPID);

.. [8]
   Valore in ore che esprime la “Durata massima dell’evento di
   indisponibilità del sotto-servizio di registrazione identità.” (v.
   indicatore IQ-01 dell’Allegato 3 Convenzione SPID);

.. [9]
   Valore espresso in giorni relativo al tempo di rilascio credenziali
   (IQ-04)

.. [10]
   La periodicità indicata corrisponde all’intervallo minimo di
   trasmissione. Tuttavia il soggetto incaricato di trasmettere i dati
   statistici, può stabilire – ad es. sulla base di proprie esigenze
   tecnico-organizzative - intervalli ridotti di trasmissione fino alla
   trasmissione in modalità giornaliera o continua (se consentita dal
   canale).

.. [11]
   Identifica sempre il Soggetto erogatore del servizio. Nel caso di
   Soggetto aggregato, il campo deve contenere l'\ \ *EntityID* del
   soggetto aggregato in accordo con quanto definito dall'avviso n.19
   **(**\ \ \ *\ *\ \ \ https://www.agid.gov.it/sites/default/files/repository_files/spid-avviso-n19-_metadata_soggetti_aggregati.pdf)

.. [12]
   In alcuni casi il campo *AuthID* può non essere valorizzato (es.
   quando sul SP non viene aperta alcuna sessione)

.. [13]
   Si faccia sempre riferimento all’ultima versione della “\ \ **Tabella
   messaggi di anomalia SPID**\ \ ” (V. `Regole
   Tecniche <https://www.agid.gov.it/sites/default/files/repository_files/tabella-messaggi-spid-v1.3_0.pdf>`__)

.. [14]
   EntityID identifica sempre il Soggetto erogatore del servizio. Nel
   caso di Soggetto aggregato, il campo deve contenere l'\ \ *EntityID*
   del soggetto aggregato in accordo con quanto definito dall'Avviso
   SPID n.19
   **(**\ \ \ *\ *\ \ \ https://www.agid.gov.it/sites/default/files/repository_files/spid-avviso-n19-_metadata_soggetti_aggregati.pdf)

.. [15]
   Il campo EntityID dentifica sempre il Soggetto erogatore del
   servizio. Nel caso di Soggetto aggregato, il campo deve contenere
   l'\ \ *EntityID* del soggetto aggregato in accordo con quanto
   definito dall'Avviso SPID n.19
   **(**\ \ \ *\ *\ \ \ https://www.agid.gov.it/sites/default/files/repository_files/spid-avviso-n19-_metadata_soggetti_aggregati.pdf\ \ \ *\ *\ \ \ **)**

.. [16]
   *Sostituisce Report Livelli di servizio di cui Allegato 3 convenzione
   Gestori Identità digitale- SP privati*


.. forum_italia::
   :topic_id: 15546
   :scope: document
