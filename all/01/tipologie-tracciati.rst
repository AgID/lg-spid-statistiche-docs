.. _`tipolTracc`:

Valori tipologici dei tracciati
===============================

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
   :topic_id: XXXXX
   :scope: document
