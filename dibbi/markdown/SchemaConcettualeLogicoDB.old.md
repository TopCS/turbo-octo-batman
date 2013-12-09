###Schema Concettuale DB

<a name="legenda-simboli"></a>
* __[Legenda Simboli ♣](#legenda)__:
    * __[Links ⚓](#legenda-simboli-links)__:
        * __[⚒](#strutture)__ : _link alla struttura_
        * __[☢](#vincoli)__ : _link ai vincoli_
        * __[✎](#diagrammi-er)__ : _link allo sketch_
        * __[☝](#indice)__ : _link all'indice_
    * __[Vincoli Attributo ☢](#legenda-simboli-vincoli-attributo-tabella)__:
        * __[♔](#legenda-simboli)__ : _vincolo di chiave primaria_
        * __[♕](#legenda-simboli)__ : _vincolo di chiave esterna_
        * __[♖](#legenda-simboli)__ : _vincolo di chiave esterna ridondante_
        * __[⚠](#legenda-simboli)__ : _vincolo unique su attributo singolo_
        * __[⚛](#legenda-simboli)__ : _vincolo unique su attributo multiplo_
        * __[✓](#legenda-simboli)__ : _vincolo di attributo obbligatorio_
        * __[⚡](#legenda-simboli)__ : _vincolo di dominio_
    * __[Regole Aziendali - Business Rules ☆](#regole-aziendali)__
        * __[V](#vincolo-integrità)__ : `♔` `♕` `⚠` `⚛` _vincolo d'integrità referenziale_
        * __[VR](#vincolo-integrità-ridondante)__ : ` ♖` _vincolo d'integrità referenziale ridondante_
        * __[D](#vincolo-dominio)__ : `⚡` _vincolo di dominio_
        * __[✍](#descrizione)__ : _descrizione_

<a name="indice"></a>
* __[Indice ☝](#indice)__
    1. __[⚒](#utente) [☢](#vincoli-utente) [✎](#diagramma-credenziali-utente)__ `Utente`
    2. __[⚒](#bee) [☢](#vincoli-bee) [✎](#diagramma-relazioni-utente)__ `Bee`
    3. __[⚒](#beekeeper) [☢](#vincoli-beekeeper) [✎](#diagramma-relazioni-utente)__ `Beekeeper`
    4. __[⚒](#anagrafica-bee) [☢](#vincoli-anagrafica-bee) [✎](#diagramma-credenziali-utente)__ `AnagraficaBee`
    5. __[⚒](#anagrafica-beekeeper) [☢](#vincoli-anagrafica-beekeeper) [✎](#diagramma-credenziali-utente)__ `AnagraficaBeekeeper`
    6. __[⚒](#preferiti-bee) [☢](#vincoli-preferiti-bee) [✎](#diagramma-relazioni-utente)__ `PreferitiBee`
    7. __[⚒](#preferiti-beekeeper) [☢](#vincoli-preferiti-beekeeper) [✎](#diagramma-relazioni-utente)__ `PreferitiBeekeeper`
    8. __[⚒](#prelievo-bee) [☢](#vincoli-prelievo-bee) [✎](#diagramma-transazioni-utente)__ `PrelievoBee`
    9. __[⚒](#versamento-beekeeper) [☢](#vincoli-versamento-beekeeper) [✎](#diagramma-transazioni-utente)__ `VersamentoBeekeeper`
    10. __[⚒](#documento-fiscale-bee) [☢](#vincoli-documento-fiscale-bee) [✎](#diagramma-transazioni-utente)__ `DocumentoFiscaleBee`
    11. __[⚒](#documento-fiscale-beekeeper) [☢](#vincoli-documento-fiscale-beekeeper) [✎](#diagramma-transazioni-utente)__ `DocumentoFiscaleBeekeeper`
    12. __[⚒](#feedback-bee-to-beekeeper) [☢](#vincoli-feedback-bee-to-beekeeper) [✎](#diagramma-feedbacks)__ `FeedbackBeeToBeekeeper`
    13. __[⚒](#feedback-beekeeper-to-bee) [☢](#vincoli-feedback-beekeeper-to-bee) [✎](#diagramma-feedbacks)__ `FeedbackBeekeeperToBee`
    14. __[⚒](#chat-room) [☢](#vincoli-chat-room) [✎](#diagramma-messaggi-e-notifiche)__ `ChatRoom`
    15. __[⚒](#messaggio-chat) [☢](#vincoli-messaggio-chat) [✎](#diagramma-messaggi-e-notifiche)__ `MessaggioChat`
    16. __[⚒](#notifica-bee) [☢](#vincoli-notifica-bee) [✎](#diagramma-messaggi-e-notifiche)__ `NotificaBee`
    17. __[⚒](#notifica-beekeeper) [☢](#vincoli-notifica-beekeeper) [✎](#diagramma-messaggi-e-notifiche)__ `NotificaBeekeeper`
    18. __[⚒](#candidatura-task) [☢](#vincoli-candidatura-task) [✎](#diagramma-assegnazioni-e-candidature-task)__ `CandidaturaTask`
    19. __[⚒](#assegnazione-task) [☢](#vincoli-assegnazione-task) [✎](#diagramma-assegnazioni-e-candidature-task)__ `AssegnazioneTask`
    20. __[⚒](#accredito) [☢](#vincoli-accredito) [✎](#diagramma-assegnazioni-e-candidature-task)__ `Accredito`
    21. __[⚒](#job) [☢](#vincoli-job) [✎](#diagramma-azioni-job-e-task)__ `Job`
    22. __[⚒](#task) [☢](#vincoli-task) [✎](#diagramma-azioni-job-e-task)__ `Task`
    23. __[⚒](#sequenza-predefinita-azioni-job) [☢](#vincoli-sequenza-predefinita-azioni-job) [✎](#diagramma-azioni-job-e-task)__ `SequenzaPredefinitaAzioniJob`
    24. __[⚒](#sequenza-richiesta-azioni-task) [☢](#vincoli-sequenza-richiesta-azioni-task) [✎](#diagramma-azioni-job-e-task)__ `SequenzaRichiestaAzioniTask`
    25. __[⚒](#azione-predefinita-job) [☢](#vincoli-azione-predefinita-job) [✎](#diagramma-azioni-job-e-task)__ `AzionePredefinitaJob`
    26. __[⚒](#azione-richiesta-task) [☢](#vincoli-azione-richiesta-task) [✎](#diagramma-azioni-job-e-task)__ `AzioneRichiestaTask`
    27. __[⚒](#immagine-ricevuta-task) [☢](#vincoli-immagine-ricevuta-task) [✎](#diagramma-azioni-job-e-task)__ `ImmagineRicevutaTask`
    28. __[⚒](#filmato-ricevuto-task) [☢](#vincoli-filmato-ricevuto-task) [✎](#diagramma-azioni-job-e-task)__ `FilmatoRicevutoTask`
    29. __[⚒](#immagine-esempio-azione-predefinita-job) [☢](#vincoli-immagine-esempio-azione-predefinita-job) [✎](#diagramma-azioni-job-e-task)__ `ImmagineEsempioAzionePredefinitaJob`
    30. __[⚒](#domanda-questionario-predefinito-job) [☢](#vincoli-domanda-questionario-predefinito-job) [✎](#diagramma-azioni-job-e-task)__ `DomandaQuestionarioPredefinitoJob`
    31. __[⚒](#opzione-risposta-questionario-predefinito-job) [☢](#vincoli-opzione-risposta-questionario-predefinito-job) [✎](#diagramma-azioni-job-e-task)__ `OpzioneRispostaQuestionarioPredefinitoJob`
    32. __[⚒](#domanda-richiesta-questionario-task) [☢](#vincoli-domanda-richiesta-questionario-task) [✎](#diagramma-azioni-job-e-task)__ `DomandaRichiestaQuestionarioTask`
    33. __[⚒](#opzione-risposta-questionario-task) [☢](#vincoli-opzione-risposta-questionario-task) [✎](#diagramma-azioni-job-e-task)__ `OpzioneRispostaQuestionarioTask`
    34. __[⚒](#area-presidio-bee) [☢](#vincoli-area-presidio-bee) [✎](#diagramma-presidio-bee)__ `AreaPresidioBee`
    35. __[⚒](#luogo-task) [☢](#vincoli-luogo-task) [✎](#diagramma-presidio-bee)__ `LuogoTask`
    36. __[⚒](#svolgimento-sequenza-azioni-task) [☢](#vincoli-svolgimento-sequenza-azioni-task) [✎](#diagramma-svolgimento-task)__ `SvolgimentoSequenzaAzioniTask`
    37. __[⚒](#azione-svolta-task) [☢](#vincoli-azione-svolta-task) [✎](#diagramma-svolgimento-task)__ `AzioneSvoltaTask`
    38. __[⚒](#questionario-svolto-task) [☢](#vincoli-questionario-svolto-task) [✎](#diagramma-svolgimento-task)__ `QuestionarioSvoltoTask`
    39. __[⚒](#risposta-ricevuta-questionario-task) [☢](#vincoli-risposta-ricevuta-questionario-task) [✎](#diagramma-svolgimento-task)__ `RispostaRicevutaQuestionarioTask`

--------------------------------------------------------------------------------

<a name="strutture"></a>
###Strutture ⚒

<a name="utente"></a>
####[1. Utente](#utente) __[☢](#vincoli-utente) [✎](#diagramma-credenziali-utente) [☝](#indice)__

> `♔ referenced by` : [`Bee`](#bee) [`Beekeeper`](#beekeeper)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idUtente__                      |  ♔  |     |      | _String_ |                |
| 2   | username                          |     |  ✓  |  ⚠   | _String_ |                | __[`RA 2`](#RA2)__ |
| 3   | email                             |     |  ✓  |  ⚠   | _String_ |                | __[`RA 3`](#RA3)__ |
| 4   | auth                              |     |  ✓  |      | _String_ |                |        |
| 5   | dataCreazione                     |     |  ✓  |      | _Date_   |                |
| 6   | statoAccount                      |     |  ✓  |      | _String_ | __`attivo`<br/>`disabilitato`__ |
| 7   | statoVerificaCredenziali          |     |  ✓  |      | _String_ | __`pendente`<br/>`completata`__ | __[`RA 41`](#RA41)__<br/>__[`RA 65`](#RA65)__ |
| 8   | tipoUtente                        |     |  ✓  |      | _String_ | __[`Bee`](#bee)<br/>[`Beekeeper`](#beekeeper)__ | __[`RA 53`](#RA53)__ |
| 9   | dataUltimoAccesso                 |     |     |      | _Date_   |                |        |
| 10  | dataUltimaModifica                |     |     |      | _Date_   |                |        |
| 11  | twitterId                         |     |     |      | _String_ |                | __[`RA 4`](#RA4)__ |
| 12  | facebookId                        |     |     |      | _String_ |                | __[`RA 4`](#RA4)__ |
| 13  | linkedinId                        |     |     |      | _String_ |                | __[`RA 4`](#RA4)__ |
| 14  | avatarURL                         |     |     |      | _String_ |                |        |

---------------------------------------------------------------------------------------------------


<a name="bee"></a>
####[2. Bee](#bee) [☢](#vincoli-bee) [✎](#diagramma-relazioni-utente) [☝](#indice)

> `♔ referenced by` : [`AnagraficaBee`](#anagrafica-bee) [`PreferitiBee`](#preferiti-bee) [`PreferitiBeekeeper`](#preferiti-beekeeper) [`PrelievoBee`](#prelievo-bee) [`MessaggioChat`](#messaggio-chat) [`NotificaBee`](#notifica-bee) _[`AssegnazioneTask`](#assegnazione-task)_ [`CandidaturaTask`](#candidatura-task) [`AreaPresidioBee`](#area-presidio-bee) [_`FeedbackBeeToBeekeeper`_](#feedback-bee-to-beekeeper) [_`FeedbackBeekeeperToBee`_](#feedback-beekeeper-to-bee) [_`Accredito`_](#accredito)

|  #  |                     Attribute Name                           | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|:------------------------------------------------------------:|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idBee`__                                                  |  ♔  |     |      | _String_ |                |        |
| 2   | [`idCredenzialiAccessoUtente`](#credenziali-accesso-utente)  |  ♕  |  ✓  |  ⚠   | _String_ |                | __[`RA 1`](#RA1)__ |
| 3   | bankrollCrediti                                              |     |  ✓  |      | _Number_ | __[`⚡ attributo calcolato`](#1.3)__ | __[`RA 63`](#RA63)__ |
| 4   | statoAccount                                                 |     |  ✓  |      | _String_ | __`attivo`<br/>`disabilitato`__ | __[`RA 40`](#RA40)__<br/>__[`RA 65`](#RA65)__ |
| 5   | dataCreazione                                                |     |  ✓  |      | _Date_   |                |        |
| 6   | avatarURL                                                    |     |     |      | _String_ |                |        |
| 7   | mediaVotazioniRicevute                                       |     |     |      | _Number_ | __[`⚡ attributo calcolato`](#1.7)__ |        |

<a name="attributi-calcolati-bee"></a>
#####[Attributi Calcolati Bee ⚡](#attributi-calcolati-bee)

<a name="1.3"></a>
* `bankrollCrediti` : Rappresenta il totale dei crediti attualmente
  in possesso del Bee. E' calcolato come la differenza tra il totale degli importi
  di [`Accredito`](#accredito) ricevuti e il totale degli importi di
  [`Prelievo`](#prelievo-bee) effettuati.
<a name="1.7"></a>
* `mediaVotazioniRicevute` : rappresenta la media dei voti ricevuti dai Beekeeper
  per ogni [`AssegnazioneTask`](#assegnazione-task). E' calcolato come la media di
  tutti i __votoBeekeeper__ maggiori o uguali a 0 presenti nei [`FeedbackBeekeeperToBee`](#Feedback-beekeeper-to-bee).

------------------------------------------------------------------------------------------------------------------------------------------

<a name="beekeeper"></a>
####[3. Beekeeper](#beekeeper) __[☢](#vincoli-beekeeper) [✎](#diagramma-relazioni-utente) [☝](#indice)__

> `♔ referenced by` : [`AnagraficaBeekeeper`](#anagrafica-beekeeper) [`PreferitiBee`](#preferiti-bee) [`PreferitiBeekeeper`](#preferiti-beekeeper) [`VersamentoBeekeeper`](#prelievo-bee) [`MessaggioChat`](#messaggio-chat) [`NotificaBeekeeper`](#notifica-beekeeper) [`Job`](#job) _[`AssegnazioneTask`](#assegnazione-task)_ [_`FeedbackBeeToBeekeeper`_](#feedback-bee-to-beekeeper) [_`FeedbackBeekeeperToBee`_](#feedback-beekeeper-to-bee) [_`Accredito`_](#accredito)

|  #  |                        Attribute Name                        | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|:------------------------------------------------------------:|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idBeekeeper`__                                            |  ♔  |     |      | _String_ |                |        |
| 2   | [`idCredenzialiAccessoUtente`](#credenziali-accesso-utente)  |  ♕  |  ✓  |  ⚠   | _String_ |                | __[`RA 1`](#RA1)__ |
| 3   | bankrollCrediti                                              |     |  ✓  |      | _Number_ |  __[`⚡ attributo calcolato`](#2.3)__  |        |
| 4   | creditiDisponibili                                           |     |  ✓  |      | _Number_ |  __[`⚡ attributo calcolato`](#2.4)__  | __[`RA 64`](#RA64)__ |
| 5   | statoAccount                                                 |     |  ✓  |      | _String_ | __`attivo`<br/>`disabilitato`__ | __[`RA 40`](#RA40)__<br/>__[`RA 65`](#RA65)__ |
| 6   | dataCreazione                                                |     |  ✓  |      | _Date_   |                |        |
| 7   | avatarURL                                                    |     |     |      | _String_ |                |        |
| 8   | mediaVotazioniRiceute                                        |     |     |      | _Number_ | __[`⚡ attributo calcolato`](#2.8)__ |        |

<a name="attributi-calcolati-bee"></a>
#####[Attributi Calcolati Beekeeper ⚡](#attributi-calcolati-beekeeper)

<a name="2.3"></a>
* `bankrollCrediti` : Rappresenta il totale dei crediti attualmente in possesso del
   Beekeeper. E' calcolato come la differenza tra il totale degli importi di
   [`VersamentoBeekeeper`](#versamento-beekeeper) effettuati con successo e il
   totale degli importi di [`Accredito`](#accredito).
<a name="2.4"></a>
* `creditiDisponibili` : rappresentano il limite dei crediti
   investibili da un Beekeeper; sono calcolati come la differenza tra il suo
   `bankrollCrediti` attuale e la quota totale dei crediti investiti
   per ognuno dei suoi [`Task`](#task) attualmente pubblicati / disponibili.
<a name="2.8"></a>
* `mediaVotazioniRicevute` : rappresenta la media dei voti ricevuti dai Bee per
   ogni [`AssegnazioneTask`](#assegnazione-task). E' calcolato come la media di
   tutti i __votoBee__ maggiori o uguali a 0 presenti nei [`FeedbackBeetoBeekeeper`](#Feedback-bee-to-beekeeper).

---------------------------------------------------------------------------------------------------------------------


<a name="anagrafica-bee"></a>
####[4. AnagraficaBee](#anagrafica-bee) __[☢](#vincoli-anagrafica-bee) [✎](#diagramma-credenziali-utente) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |    Attribute Name     | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idAnagraficaBee`__ |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBee`](#bee)       |  ♕  |  ✓  |  ⚠   | _String_ |                |  __[`RA 5`](#RA5)__  |
| 3   | nome                  |     |  ✓  |      | _String_ |                |        |
| 4   | cognome               |     |  ✓  |      | _String_ |                |        |
| 5   | codiceFiscale         |     |  ✓  |  ⚠   | _String_ |                |  __[`RA 6`](#RA6)__ __[`RA 61`](#RA61)__ |
| 6   | ragioneSociale        |     |     |      | _String_ |                |        |
| 7   | partitaIVA            |     |     |      | _String_ |                |   __[`RA 8`](#RA8)__ __[`RA 62`](#RA62)__ |
| 8   | tipologiaFiscale      |     |  ✓  |      | _String_ | __`privato`<br/>`libero professionista`<br/>`ditta individuale`<br/>`azienda`__ |  __[`RA 43`](#RA43)__ __[`RA 8`](#RA8)__ |
| 9   | fax                   |     |     |      | _String_ |                |        |
| 10  | cellulare             |     |     |      | _String_ |                |        |
| 11  | telefono              |     |     |      | _String_ |                |        |
| 12  | via                   |     |     |      | _String_ |                |        |
| 13  | civico                |     |     |      | _String_ |                |        |
| 14  | codicePostale         |     |     |      | _String_ |                |        |
| 15  | località              |     |     |      | _String_ |                |        |
| 16  | comune                |     |     |      | _String_ |                |        |
| 17  | provincia             |     |     |      | _String_ |                |        |
| 18  | dataNascita           |     |  ✓  |      |  _Date_  |                |        |
| 19  | sesso                 |     |  ✓  |      | _String_ |                |        |

---------------------------------------------------------------------------------------

<a name="anagrafica-beekeeper"></a>
####[5. AnagraficaBeekeeper](#anagrafica-beekeeper) __[☢](#vincoli-anagrafica-beekeeper) [✎](#diagramma-credenziali-utente) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |         Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idAnagraficaBeekeeper`__   |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBeeKeeeper`](#beekeeper)  |  ♕  |  ✓  |  ⚠   | _String_ |                |  __[`RA 5`](#RA5)__  |
| 3   | nome                          |     |  ✓  |      | _String_ |                |        |
| 4   | cognome                       |     |  ✓  |      | _String_ |                |        |
| 5   | codiceFiscale                 |     |  ✓  |  ⚠   | _String_ |                |  __[`RA 6`](#RA6)__ __[`RA 61`](#RA61)__ |
| 6   | ragioneSociale                |     |  ✓  |      | _String_ |                |        |
| 7   | partitaIVA                    |     |  ✓  |  ⚠   | _String_ |                |  __[`RA 7`](#RA7)__ __[`RA 62`](#RA62)__ |
| 8   | tipologiaFiscale              |     |  ✓  |      | _String_ | __`libero professionista`<br/>`ditta individuale`<br/>`azienda`__ |  __[`RA 43`](#RA43)__   |
| 9   | fax                           |     |     |      | _String_ |                |        |
| 10  | cellulare                     |     |     |      | _String_ |                |        |
| 11  | telefono                      |     |     |      | _String_ |                |        |
| 12  | via                           |     |     |      | _String_ |                |        |
| 13  | civico                        |     |     |      | _String_ |                |        |
| 14  | codicePostale                 |     |     |      | _String_ |                |        |
| 15  | località                      |     |     |      | _String_ |                |        |
| 16  | comune                        |     |     |      | _String_ |                |        |
| 17  | provincia                     |     |     |      | _String_ |                |        |
| 18  | dataNascita                   |     |  ✓  |      |  _Date_  |                |        |
| 19  | sesso                         |     |  ✓  |      | _String_ |                |        |

-----------------------------------------------------------------------------------------------

<a name="preferiti-bee"></a>
####[6. PreferitiBee](#preferiti-bee) __[☢](#vincoli-preferiti-bee) [✎](#diagramma-relazioni-utente) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | [`idBee`](#bee)              | ♔♕  |     |      | _String_ |                |  __[`RA 9`](#RA9)__  |
| 2   | [`idBeekeeper`](#beekeeper)  | ♔♕  |     |      | _String_ |                |  __[`RA 9`](#RA9)__  |

----------------------------------------------------------------------------------------------

<a name="preferiti-beekeeper"></a>
####[7. PreferitiBeekeeper](#preferiti-beekeeper) __[☢](#vincoli-preferiti-beekeeper) [✎](#diagramma-relazioni-utente) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |         Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | [`idBeekeeper`](#beekeeper)  | ♔♕  |     |      | _String_ |                |  __[`RA 10`](#RA10)__  |
| 2   | [`idBee`](#bee)              | ♔♕  |     |      | _String_ |                |  __[`RA 10`](#RA10)__  |

----------------------------------------------------------------------------------------------

<a name="prelievo-bee"></a>
####[8. PrelievoBee](#prelievo-bee) __[☢](#vincoli-prelievo-bee) [✎](#diagramma-transazioni-utente) [☝](#indice)__

> `♔ referenced by` : [`DocumentoFiscaleBee`](#documento-fiscale-bee)

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idPrelievoBee`__          |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBee`](#bee)              |  ♕  |  ✓  |      | _String_ |                |  __[`RA 11`](#RA11)__  |
| 3   | codiceOperazione             |     |  ✓  |  ⚠   | _String_ |                |  __[`RA 12`](#RA12)__  |
| 4   | dataPrelievo                 |     |  ✓  |      | _String_ |                |        |
| 5   | importoValutaPrelevata       |     |  ✓  |      | _Number_ |                |        |
| 6   | importoCreditiConvertiti     |     |  ✓  |      | _Number_ |                |  __[`RA 63`](#RA63)__  |
| 7   | statoPrelievo                |     |  ✓  |      | _String_ |      `??`      |  __[`RA 44`](#RA44)__  |

----------------------------------------------------------------------------------------------

<a name="versamento-beekeeper"></a>
####[9. VersamentoBeekeeper](#versamento-beekeeper) __[☢](#vincoli-versamento-beekeeper) [✎](#diagramma-transazioni-utente) [☝](#indice)__

> `♔ referenced by` : [`DocumentoFiscaleBeekeeper`](#documento-fiscale-beekeeper)

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idVersamentoBeekeeper`__  |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBeekeeper`](#beekeeper)  |  ♕  |  ✓  |      | _String_ |                |  __[`RA 13`](#RA13)__  |
| 3   | codiceOperazione             |     |  ✓  |  ⚠   | _String_ |                |  __[`RA 14`](#RA14)__  |
| 4   | dataVersamento               |     |  ✓  |      | _String_ |                |        |
| 5   | importoValutaVersata         |     |  ✓  |      | _Number_ |                |        |
| 6   | importoCreditiAcquisiti      |     |  ✓  |      | _Number_ |                |        |
| 7   | statoVersamento              |     |  ✓  |      | _String_ |      `??`      |  __[`RA 45`](#RA45)__  |

----------------------------------------------------------------------------------------------

<a name="documento-fiscale-bee"></a>
####[10. DocumentoFiscaleBee](#documento-fiscale-bee) __[☢](#vincoli-documento-fiscale-bee) [✎](#diagramma-transazioni-utente) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |          Attribute Name           | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idDocumentoFiscaleBee`__       |  ♔  |     |      | _String_ |                |        |
| 2   | [`idPrelievoBee`](#prelievo-bee)  |  ♕  |  ✓  |  ⚠   | _String_ |                |  __[`RA 15`](#RA15)__  |
| 3   | nomeFile                          |     |  ✓  |      | _String_ |                |        |
| 4   | dimensione                        |     |  ✓  |      | _Number_ |                |        |
| 5   | URL                               |     |  ✓  |      | _String_ |                |        |
| 6   | dataEmissione                     |     |  ✓  |      |  _Date_  |                |        |
| 7   | intestatario                      |     |  ✓  |      | _String_ |                |        |
| 8   | destinatario                      |     |  ✓  |      | _String_ |                |        |
| 9   | tipoDocumento                     |     |  ✓  |      | _String_ | __`fattura`<br/>`ritenuta`__ |  __[`RA 46`](#RA46)__  |

---------------------------------------------------------------------------------------------------

<a name="documento-fiscale-beekeeper"></a>
####[11. DocumentoFiscaleBeekeeper](#documento-fiscale-beekeeper) __[☢](#vincoli-documento-fiscale-beekeeper) [✎](#diagramma-transazioni-utente) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |                  Attribute Name                   | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idDocumentoFiscaleBeekeeper`__                 |  ♔  |     |      | _String_ |                |        |
| 2   | [`idVersamentoBeekeeper`](#versamento-beekeeper)  |  ♕  |  ✓  |  ⚠   | _String_ |                |  __[`RA 16`](#RA16)__  |
| 3   | nomeFile                                          |     |  ✓  |      | _String_ |                |        |
| 4   | dimensione                                        |     |  ✓  |      | _Number_ |                |        |
| 5   | URL                                               |     |  ✓  |      | _String_ |                |        |
| 6   | dataEmissione                                     |     |  ✓  |      |  _Date_  |                |        |
| 7   | intestatario                                      |     |  ✓  |      | _String_ |                |        |
| 8   | destinatario                                      |     |  ✓  |      | _String_ |                |        |
| 9   | tipoDocumento                                     |     |  ✓  |      | _String_ | __`fattura`<br/>`ritenuta`__ |  __[`RA 46`](#RA46)__  |

-------------------------------------------------------------------------------------------------------------------

<a name="feedback-bee-to-beekeeper"></a>
####[12. FeedbackBeeToBeekeeper](#feedback-bee-to-beekeeper) __[☢](#vincoli-feedback-bee-to-beekeeper) [✎](#diagramma-feedbacks) [☝](#indice)__

> `♔ referenced by` : _[`NotificaBee(idEvento)`](#notifica-bee)_ _[`NotificaBeekeeper(idEvento)`](#notifica-beekeeper)_

|  #  |               Attribute Name                | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idFeedbackBeeToBeekeeper`__              |  ♔  |     |      | _String_ |                |        |
| 2   | [`idAssegnazioneTask`](#assegnazione-task)  |  ♕  |  ✓  |  ⚠   | _String_ |                |  __[`RA 17`](#RA17)__  |
| 3   | _[`idBee`](#bee)_                           |  ♖  |  ✓  |      | _String_ |                |        |
| 4   | _[`idBeekeeper`](#beekeeper)_               |  ♖  |  ✓  |      | _String_ |                |        |
| 5   | votoBee                                     |     |  ✓  |      | _Number_ |                |        |
| 6   | commentoBee                                 |     |  ✓  |      | _String_ |                |        |
| 7   | dataUltimaModifica                          |     |  ✓  |      |  _Date_  |                |        |

-------------------------------------------------------------------------------------------------------------

<a name="feedback-beekeeper-to-bee"></a>
####[13. FeedbackBeekeeperToBee](#feedback-beekeeper-to-bee) __[☢](#vincoli-feedback-beekeeper-to-bee) [✎](#diagramma-feedbacks) [☝](#indice)__

> `♔ referenced by` : _[`NotificaBeekeeper(idEvento)`](#notifica-beekeeper)_ _[`NotificaBee(idEvento)`](#notifica-bee)_

|  #  |               Attribute Name                | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idFeedbackBeekeeperToBee`__              |  ♔  |     |      | _String_ |                |        |
| 2   | [`idAssegnazioneTask`](#assegnazione-task)  |  ♕  |  ✓  |  ⚠   | _String_ |                |  __[`RA 18`](#RA18)__  |
| 3   | _[`idBee`](#bee)_                           |  ♖  |  ✓  |      | _String_ |                |        |
| 4   | _[`idBeekeeper`](#beekeeper)_               |  ♖  |  ✓  |      | _String_ |                |        |
| 5   | votoBeekeeper                               |     |  ✓  |      | _Number_ |                |        |
| 6   | commentoBeekeeper                           |     |  ✓  |      | _String_ |                |        |
| 7   | dataUltimaModifica                          |     |  ✓  |      |  _Date_  |                |        |

-------------------------------------------------------------------------------------------------------------

<a name="chat-room"></a>
####[14. ChatRoom](#chat-room) __[☢](#vincoli-chat-room) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__

> `♔ referenced by` : [`MessaggioChat`](#messaggio-chat)

|  #  |               Attribute Name                | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idChatRoom`__                            |  ♔  |     |      | _String_ |                |        |
| 2   | [`idAssegnazioneTask`](#assegnazione-task)  |  ♕  |  ✓  |  ⚠   | _String_ |                | __[`RA 19`](#RA19)__ |
| 3   | statoChatRoom                               |     |  ✓  |      | _String_ | __`attiva`<br/>`archiviata`__ | __[`RA 47`](#RA47)__ |

-------------------------------------------------------------------------------------------------------------

<a name="messaggio-chat"></a>
####[15. MessaggioChat](#messaggio-chat) __[☢](#vincoli-messaggio-chat) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idMessaggioChat`__           |  ♔  |     |      | _String_ |                |        |
| 2   | [`idChatRoom`](#chat-room)      |  ♕  |  ✓  |      | _String_ |                | __[`RA 20`](#RA20)__ |
| 3   | _[`idBee`](#bee)_               |  ♖  |  ✓  |      | _String_ |                |        |
| 4   | _[`idBeekeeper`](#beekeeper)_   |  ♖  |  ✓  |      | _String_ |                |        |
| 5   | tipoMittente                    |     |  ✓  |      | _String_ | __[`Bee`](#bee)<br/>[`Beekeeper`](#beekeeper)__ | __[`RA 48`](#RA48)__ |
| 6   | timestamp                       |     |  ✓  |      |  _Date_  |                |        |
| 7   | testo                           |     |  ✓  |      | _String_ |                |        |

-------------------------------------------------------------------------------------------------

<a name="notifica-bee"></a>
####[16. NotificaBee](#notifica-bee) __[☢](#vincoli-notifica-bee) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idNotificaBee`__             |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBeeDestinatario`](#bee)     |  ♕  |  ✓  |      | _String_ |                | __[`RA 21`](#RA21)__ |
| 3   |  idEvento                       |     |  ✓  |      | _String_ |                |        |
| 4   | tipoEvento                      |     |  ✓  |      | _String_ | __[`FeedbackBeeToBeekeeper`](#feedback-bee-to-beekeeper)<br/>[`FeedbackBeekeeperToBee`](#feedback-beekeeper-to-bee)<br/>[`Accredito`](#accredito)<br/>[`CandidaturaTask`](#candidatura-task)<br/>[`AssegnazioneTask`](#assegnazione-task)__ |  __[`RA 49`](#RA49)__  |
| 5   | mittente                        |     |  ✓  |      | _String_ |                |        |
| 6   | subject                         |     |  ✓  |      | _String_ |                |        |
| 7   | timestamp                       |     |  ✓  |      |  _Date_  |                |        |
| 8   | testo                           |     |  ✓  |      | _String_ |                |        |

-------------------------------------------------------------------------------------------------

<a name="notifica-beekeeper"></a>
####[17. NotificaBeekeeper](#notifica) __[☢](#vincoli-notifica-beekeeper) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |              Attribute Name              | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idNotificaBeekeeper`__                |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBeekeeperDestinatario`](#beekeeper)  |  ♕  |  ✓  |      | _String_ |                |  __[`RA 21`](#RA21)__  |
| 3   |  idEvento                                |     |  ✓  |      | _String_ |                |        |
| 4   | tipoEvento                      |     |  ✓  |      | _String_ | __[`FeedbackBeeToBeekeeper`](#feedback-bee-to-beekeeper)<br/>[`FeedbackBeekeeperToBee`](#feedback-beekeeper-to-bee)<br/>[`Accredito`](#accredito)<br/>[`CandidaturaTask`](#candidatura-task)<br/>[`AssegnazioneTask`](#assegnazione-task)__ | __[`RA 49`](#RA49)__ |
| 5   | mittente                                 |     |  ✓  |      | _String_ |                |        |
| 6   | subject                                  |     |  ✓  |      | _String_ |                |        |
| 7   | timestamp                                |     |  ✓  |      |  _Date_  |                |        |
| 8   | testo                                    |     |  ✓  |      | _String_ |                |        |

----------------------------------------------------------------------------------------------------------

<a name="candidatura-task"></a>
####[18. CandidaturaTask](#candidatura-task) __[☢](#vincoli-candidatura-task) [✎](#diagramma-assegnazioni-e-candidature-task) [☝](#indice)__

> `♔ referenced by` : [`AssegnazioneTask`](#assegnazione-task)

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idCandidaturaTask`__         |  ♔  |     |      | _String_ |                |        |
| 2   | [`idTask`](#task)               |  ♕  |  ✓  |  ⚛   | _String_ |                |  __[`RA 22`](#RA22)__  |
| 3   | [`idBee`](#bee)                 |  ♕  |  ✓  |  ⚛   | _String_ |                |  __[`RA 22`](#RA22)__  |
| 4   | dataCandidatura                 |     |  ✓  |      |  _Date_  |                |        |
| 5   | tipoCandidatura                 |     |  ✓  |      | _String_ | __`invito`<br/>`spontanea`__ |  __[`RA 50`](#RA50)__  |
| 6   | statoCandidatura                |     |  ✓  |      | _String_ |  __`pendente`<br/>`accettata`<br/>`rifiutata`<br/>`declinata`<br/>`annullata`__ | __[`RA 51`](#RA51)__<br/>__[`RA 69`](#RA69)__<br/>__[`RA 70`](#RA70)__<br/>__[`RA 75`](#RA75)__ |
| 7   | offertaCreditiBee               |     |  ✓  |      | _Number_ |                | __[`RA 71`](#RA71)__<br/>__[`RA 72`](#RA72)__ |
| 8   | codiceInvito                    |     |  ✓  |      | _String_ |                |        |
| 9   | dataInvito                      |     |  ✓  |      |  _Date_  |                |        |

-------------------------------------------------------------------------------------------------

<a name="assegnazione-task"></a>
####[19. AssegnazioneTask](#assegnazione-task) __[☢](#vincoli-assegnazione-task) [✎](#diagramma-assegnazioni-e-candidature-task) [☝](#indice)__

> `♔ referenced by` : [`FeedbackBeeToBeekeeper`](#feedback-bee-to-beekeeper) [`FeedbackBeekeeperToBee`](#feedback-beekeeper-to-bee) [`ChatRoom`](#chat-room) [`Accredito`](#accredito) [`SvolgimentoSequenzaAzioniTask`](#svolgimento-sequenza-azioni-task)

|  #  |              Attribute Name              | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idAssegnazioneTask`__                 |  ♔  |     |      | _String_ |                |        |
| 2   | [`idCandidaturaTask`](#candidatura-task) |  ♕  |  ✓  |  ⚠   | _String_ |                |  __[`RA 23`](#RA23)__  |
| 3   | _[`idTask`](#task)_                      |  ♖  |  ✓  |      | _String_ |                |        |
| 4   | _[`idBee`](#bee)_                        |  ♖  |  ✓  |      | _String_ |                |        |
| 5   | _[`idBeekeeper`](#beekeeper)_            |  ♖  |  ✓  |      | _String_ |                |        |
| 6   | dataAssegnazione                         |     |  ✓  |      |  _Date_  |                |        |
| 7   | statoAssegnazione                        |     |  ✓  |      | _String_ | __`attiva`<br/>`completata`<br/>`rifiutata`<br/>`annullata`<br/>`scaduta`__ | __[`RA 52`](#RA52)__<br/>__[`RA 73`](#RA73)__ |
| 8   | creditiPattuiti                          |     |  ✓  |      | _Number_ |                | __[`RA 72`](#RA72)__ |
| 9   | dataScadenzaAssegnazione                 |     |     |      |  _Date_  |                |        |
| 10  | dataCompletamento                        |     |     |      |  _Date_  |                |        |

----------------------------------------------------------------------------------------------------------

<a name="accredito"></a>
####[20. Accredito](#accredito) __[☢](#vincoli-accredito) [✎](#diagramma-assegnazioni-e-candidature-task) [☝](#indice)__

> `♔ referenced by` : _[`NotificaBeekeeper(idEvento)`](#notifica-beekeeper)_ _[`NotificaBee(idEvento)`](#notifica-bee)_

|  #  |               Attribute Name                | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idAccredito`__                           |  ♔  |     |      | _String_ |                |        |
| 2   | [`idAssegnazioneTask`](#assegnazione-task)  |  ♕  |  ✓  |  ⚠   | _String_ |                | __[`RA 24`](#RA24)__ |
| 3   | _[`idBee`](#bee)_                           |  ♖  |  ✓  |      | _String_ |                |        |
| 4   | _[`idBeekeeper`](#beekeeper)_               |  ♖  |  ✓  |      | _String_ |                |        |
| 5   | _[`idTask`](#task)_                         |  ♖  |  ✓  |  ⚠   | _String_ |                |        |
| 6   | dataAccredito                               |     |  ✓  |      |  _Date_  |                |        |
| 7   | importoAccredito                            |     |  ✓  |      | _Number_ |                |        |

-------------------------------------------------------------------------------------------------------------

<a name="job"></a>
####[21. Job](#job) __[☢](#vincoli-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`Task`](#task) [`SequenzaPredefinitaAzioniJob`](#sequenza-predefinita-azioni-job)

|  #  |     Attribute Name              | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idJob`__                     |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBeekeeper`](#beekeeper)     |  ♕  |  ✓  |      | _String_ |                | __[`RA 25`](#RA25)__ |
| 3   | titoloJob                       |     |  ✓  |      | _String_ |                |        |
| 4   | descrizioneJob                  |     |     |      | _String_ |                |        |
| 5   | statoPubblicazione              |     |  ✓  |      | _String_ | __`attiva`<br/>`disabilitata`<br/>`archiviata`__ | __[`RA 54`](#RA54)__<br/>__[`RA 64`](#RA64)__<br/>__[`RA 74`](#RA74)__ |
| 6   | dataCreazione                   |     |  ✓  |      |  _Date_  |                |        |
| 7   | dataPubblicazione               |     |     |      |  _Date_  |                |        |
| 8   | dataScadenzaPubblicazione       |     |     |      |  _Date_  |                |        |
| 9   | percentualeCompletamento        |     |     |      | _Number_ | __[`⚡ attributo calcolato`](#21.9)__ |

<a name="attributi-calcolati-job"></a>
#####[Attributi Calcolati Job ⚡](#attributi-calcolati-job)

<a name="21.9"></a>
* `percentualeCompletamento` : Rappresenta il rapporto tra tutti i [`Task`](#task)
   di un [`Job`](#job) con stato di assegnazione 'conclusa' e tutti i [`Task`](#task)
   di quel [`Job`](#job), che sono nello stato di pubblicazione 'attiva'.

-------------------------------------------------------------------------------------------------

<a name="task"></a>
####[22. Task](#task) __[☢](#vincoli-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`CandidaturaTask`](#candidatura-task) [`SequenzaRichiestaAzioniTask`](#sequenza-richiesta-azioni-task) [`LuogoTask`](#luogo-task) _[`AssegnazioneTask`](#assegnazione-task)_

|  #  |     Attribute Name    | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|-----------------------|:---:|:---:|:----:|:----------:|:--------------:|:------:|
| 1   | [`idTask`](#task)     |  ♔  |     |      |  _String_  |                |        |
| 2   | [`idJob`](#job)       |  ♕  |  ✓  |      |  _String_  |                | __[`RA 26`](#RA26)__ |
| 3   | statoPubblicazione    |     |  ✓  |      |  _String_  | __`attiva`<br/>`disabilitata`<br/>`archiviata`<br/>__ | __[`RA 55`](#RA55)__<br/>__[`RA 73`](#RA73)__<br/>__[`RA 74`](#RA74)__<br/>__[`RA 75`](#RA75)__ |
| 4   | taskAssegnato         |     |  ✓  |      |  _Boolean_ | __`true` `false`__ |        |
| 5   | taskCompletato        |     |  ✓  |      |  _Boolean_ | __`true` `false`__ |        |
| 6   | dataCreazione         |     |  ✓  |      |   _Date_   |                |        |
| 7   | dataPubblicazione     |     |     |      |   _Date_   |                |        |
| 8   | totaleCreditiOfferti  |     |  ✓  |      |  _Number_  | __[`⚡ attributo calcolato`](#22.8)__ | __[`RA 64`](#RA64)__<br/>__[`RA 71`](#RA71)__ |

<a name="22.8"></a>
* `totaleCreditiOfferti` : Rappresenta la somma di tutti i crediti offerti per
   ogni [`SequenzaRichiestaAzioniTask`](#sequenza-richiesta-azioni-task) definita per quel [`Task`](#task).

-----------------------------------------------------------------------------------------

<a name="sequenza-predefinita-azioni-job"></a>
####[23. SequenzaPredefinitaAzioniJob](#sequenza-predefinita-azioni-job) __[☢](#vincoli-sequenza-predefinita-azioni-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`AzionePredefinitaJob`](#azione-predefinita-job)

|  #  |             Attribute Name            | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|---------------------------------------|:---:|:---:|:----:|:----------:|:--------------:|:------:|
| 1   | __`idSequenzaPredefinitaAzioniJob`__  |  ♔  |     |      |  _String_  |                |        |
| 2   | [`idJob`](#job)                       |  ♕  |  ✓  |      |  _String_  |                | __[`RA 27`](#RA27)__ |
| 3   | indiceSequenza                        |     |  ✓  |      |  _Number_  |                |        |
| 4   | totaleCreditiSequenza                 |     |  ✓  |      |  _Number_  |  __[`⚡ attributo calcolato`](#23.4)__  |        |
| 5   | bonus                                 |     |     |      |  _Boolean_ | __`true` `false`__ |        |

<a name="23.4"></a>
* `totaleCreditiSequenza` : Rappresenta la somma di tutti i crediti, offerti da
   un Beekeeper, per ogni [`AzionePredefinitaJob`](#azione-predefinita-job) definita per la sequenza.

---------------------------------------------------------------------------------------------------------

<a name="sequenza-richiesta-azioni-task"></a>
####[24. SequenzaRichiestaAzioniTask](#sequenza-richiesta-azioni-task) __[☢](#vincoli-sequenza-richiesta-azioni-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`AzioneRichiestaTask`](#azione-richiesta-task) [`SvolgimentoSequenzaAzioniTask`](#svolgimento-sequenza-azioni-task)

|  #  |             Attribute Name           | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|--------------------------------------|:---:|:---:|:----:|:----------:|:--------------:|:------:|
| 1   | __`idSequenzaRichiestaAzioniTask`__  |  ♔  |     |      |  _String_  |                |        |
| 2   | [`idTask`](#task)                    |  ♕  |  ✓  |      |  _String_  |                | __[`RA 28`](#RA28)__ |
| 3   | indiceSequenza                       |     |  ✓  |      |  _Number_  |                |        |
| 4   | totaleCreditiSequenza                |     |  ✓  |      |  _Number_  | __[`⚡ attributo calcolato`](#24.4)__ |        |
| 5   | bonus                                |     |     |      |  _Boolean_ |  __`true` `false`__ |        |

<a name="24.4"></a>
* `totaleCreditiSequenza` : Rappresenta la somma di tutti i crediti, offerti da
   un Beekeeper, per ogni [`AzioneRichiestaTask`](#azione-richiesta-task) definita per la sequenza.

---------------------------------------------------------------------------------------------------------

<a name="azione-predefinita-job"></a>
####[25. AzionePredefinitaJob](#azione-predefinita-job) __[☢](#vincoli-azione-predefinita-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`ImmagineEsempioAzionePredefinitaJob`](#immagine-esempio-azione-predefinita-job) [`DomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job)

|  #  |                            Attribute Name                             | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idAzionePredefinitaJob`__                                          |  ♔  |     |  ⚛   | _String_ |                |        |
| 2   | [`idSequenzaPredefinitaAzioniJob`](#sequenza-predefinita-azioni-job)  |  ♕  |  ✓  |  ⚛   | _String_ |                | __[`RA 29`](#RA29)__ |
| 3   | titolo                                                                |     |  ✓  |      | _String_ |                |        |
| 4   | descrizione                                                           |     |  ✓  |      | _String_ |                |        |
| 5   | tipoAzione                                                            |     |  ✓  |      | _String_ | __`foto`<br/>`video`<br/>`questionario`__ | __[`RA 56`](#RA56)__ |
| 6   | limiteDimensione                                                      |     |  ✓  |      | _Number_ |                |        |
| 7   | limiteRichieste                                                       |     |  ✓  |      | _Number_ |                |        |
| 8   | offertaCrediti                                                        |     |  ✓  |      | _Number_ |                |        |

---------------------------------------------------------------------------------------------------------------------------------------

<a name="azione-richiesta-task"></a>
####[26. AzioneRichiestaTask](#azione-richiesta-task) __[☢](#vincoli-azione-richiesta-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`ImmagineRicevutaTask`](#immagine-ricevuta-task) [`FilmatoRicevutoTask`](#filmato-ricevuto-task) [`DomandaRichiestaQuestionarioTask`](#domanda-richiesta-questionario-task) 

|  #  |                            Attribute Name                           | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idAzioneRichiestaTask`__                                         |  ♔  |     |  ⚛   | _String_ |                |        |
| 2   | [`idSequenzaRichiestaAzioniTask`](#sequenza-richiesta-azioni-task)  |  ♕  |  ✓  |  ⚛   | _String_ |                | __[`RA 30`](#RA30)__ |
| 3   | titolo                                                              |     |  ✓  |      | _String_ |                |        |
| 4   | descrizione                                                         |     |  ✓  |      | _String_ |                |        |
| 5   | tipoAzione                                                          |     |  ✓  |      | _String_ | __`foto`<br/>`video`<br/>`questionario`__ | __[`RA 57`](#RA57)__ |
| 6   | limiteDimensione                                                    |     |  ✓  |      | _Number_ |                |        |
| 7   | limiteRichieste                                                     |     |  ✓  |      | _Number_ |                |        |
| 8   | offertaCrediti                                                      |     |  ✓  |      | _Number_ |                |        |

-------------------------------------------------------------------------------------------------------------------------------------

<a name="immagine-ricevuta-task"></a>
####[27. ImmagineRicevutaTask](#immagine-ricevuta-task) __[☢](#vincoli-immagine-ricevuta-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |                    Attribute Name                  | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|----------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idImmagineRicevutaTask`__                       |  ♔  |     |      | _String_ |                |        |
| 2   | [`idAzioneRichiestaTask`](#azione-richiesta-task)  |  ♕  |  ✓  |      | _String_ |                | __[`RA 31`](#RA31)__ |
| 3   | nomeFile                                           |     |  ✓  |      | _String_ |                |        |
| 4   | dimensione                                         |     |  ✓  |      | _Number_ |                |        |
| 5   | URL                                                |     |  ✓  |      | _String_ |                |        |
| 6   | dataInvio                                          |     |  ✓  |      |  _Date_  |                |        |
| 7   | latitudine                                         |     |     |      | _String_ |                |        |
| 8   | longitudine                                        |     |     |      | _String_ |                |        |

--------------------------------------------------------------------------------------------------------------------

<a name="filmato-ricevuto-task"></a>
####[28. FilmatoRicevutoTask](#filmato-ricevuto-task) __[☢](#vincoli-filmato-ricevuto-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |                   Attribute Name                   | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|----------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idFilmatoRicevutoTask`__                        |  ♔  |     |      | _String_ |                |        |
| 2   | [`idAzioneRichiestaTask`](#azione-richiesta-task)  |  ♕  |  ✓  |      | _String_ |                | __[`RA 32`](#RA32)__ |
| 3   | nomeFile                                           |     |  ✓  |      | _String_ |                |        |
| 4   | dimensione                                         |     |  ✓  |      | _Number_ |                |        |
| 5   | URL                                                |     |  ✓  |      | _String_ |                |        |
| 6   | dataInvio                                          |     |  ✓  |      |  _Date_  |                |        |
| 7   | latitudine                                         |     |     |      | _String_ |                |        |
| 8   | longitudine                                        |     |     |      | _String_ |                |        |

--------------------------------------------------------------------------------------------------------------------

<a name="immagine-esempio-azione-predefinita-job"></a>
####[29. ImmagineEsempioAzionePredefinitaJob](#immagine-esempio-azione-predefinita-job) __[☢](#vincoli-immagine-esempio-azione-predefinita-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |                   Attribute Name                     | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idImmagineEsempioAzionePredefinitaJob`__          |  ♔  |     |      | _String_ |                |        |
| 2   | [`idAzionePredefinitaJob`](#azione-predefinita-job)  |  ♕  |  ✓  |      | _String_ |                | __[`RA 33`](#RA33)__ |
| 3   | nomeFile                                             |     |  ✓  |      | _String_ |                |        |
| 4   | dimensione                                           |     |  ✓  |      | _Number_ |                |        |
| 5   | URL                                                  |     |  ✓  |      | _String_ |                |        |

----------------------------------------------------------------------------------------------------------------------

<a name="domanda-questionario-predefinito-job"></a>
####[30. DomandaQuestionarioPredefinitoJob](#domanda-questionario-predefinito-job) __[☢](#vincoli-domanda-questionario-predefinito-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`OpzioneRispostaQuestionarioPredefinitoJob`](#opzione-risposta-questionario-predefinito-job)

|  #  |                     Attribute Name                     | Key | Req | Uniq |   Type   |      Domain     |   BR   |
|:---:|--------------------------------------------------------|:---:|:---:|:----:|:--------:|:---------------:|:------:|
| 1   | __`idDomandaQuestionarioPredefinitoJob`__              |  ♔  |     |      | _String_ |                 |        |
| 2   | [`idAzionePredefinitaJob`](#azione-predefinita-job)    |  ♕  |  ✓  |      | _String_ |                 | __[`RA 34`](#RA34)__ |
| 3   | tipoSelezioneRisposta                                  |     |  ✓  |      | _String_ | __`multipla`<br/> `singola`__ | __[`RA 58`](#RA58)__ |
| 4   | testo                                                  |     |  ✓  |      | _Number_ |                 |        |

-------------------------------------------------------------------------------------------------------------------------

<a name="opzione-risposta-questionario-predefinito-job"></a>
####[31. OpzioneRispostaQuestionarioPredefinitoJob](#opzione-risposta-questionario-predefinito-job) __[☢](#vincoli-opzione-risposta-questionario-predefinito-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |                                Attribute Name                                   | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idOpzioneRispostaQuestionarioPredefinitoJob`__                               |  ♔  |     |      | _String_ |                |        |
| 2   | [`idDomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job)  |  ♕  |  ✓  |      | _String_ |                | __[`RA 35`](#RA35)__ |
| 3   | indiceRisposta                                                                  |     |  ✓  |      | _Number_ |                |        |
| 4   | tipoRisposta                                                                    |     |  ✓  |      | _String_ | __`libera`<br/>`precompilata`__ | __[`RA 59`](#RA59)__ |
| 5   | testoRisposta                                                                   |     |  ✓  |      | _String_ |                |        |

-------------------------------------------------------------------------------------------------------------------------------------------------

<a name="domanda-richiesta-questionario-task"></a>
####[32. DomandaRichiestaQuestionarioTask](#domanda-richiesta-questionario-task) __[☢](#vincoli-domanda-richiesta-questionario-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`OpzioneRispostaQuestionarioTask`](#opzione-risposta-questionario-task) [`RispostaRicevutaQuestionarioTask`](#risposta-ricevuta-questionario-task)

|  #  |                    Attribute Name                  | Key | Req | Uniq |   Type   |      Domain     |   BR   |
|:---:|----------------------------------------------------|:---:|:---:|:----:|:--------:|:---------------:|:------:|
| 1   | __`idDomandaRichiestaQuestionarioTask`__           |  ♔  |     |      | _String_ |                 |        |
| 2   | [`idAzioneRichiestaTask`](#azione-richiesta-task)  |  ♕  |  ✓  |      | _String_ |                 | __[`RA 36`](#RA36)__ |
| 3   | tipoSelezioneRisposta                              |     |  ✓  |      | _String_ | __`multipla`<br/> `singola`__ | __[`RA 58`](#RA58)__ |
| 4   | testo                                              |     |  ✓  |      | _Number_ |                 |        |

---------------------------------------------------------------------------------------------------------------------

<a name="opzione-risposta-questionario-task"></a>
####[33. OpzioneRispostaQuestionarioTask](#opzione-risposta-questionario-task) __[☢](#vincoli-opzione-risposta-questionario-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__

> `♔ referenced by` : [`RispostaRicevutaQuestionarioTask`](#risposta-ricevuta-questionario-task)

|  #  |                                Attribute Name                                 | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-------------------------------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idOpzioneRispostaQuestionarioTask`__                                       |  ♔  |     |      | _String_ |                |        |
| 2   | [`idDomandaRichiestaQuestionarioTask`](#domanda-richiesta-questionario-task)  |  ♕  |  ✓  |      | _String_ |                | __[`RA 37`](#RA37)__ |
| 3   | indiceRisposta                                                                |     |  ✓  |      | _Number_ |                |        |
| 4   | tipoRisposta                                                                  |     |  ✓  |      | _String_ | __`libera`<br/>`precompilata`__ | __[`RA 59`](#RA59)__ |
| 5   | testoRisposta                                                                 |     |  ✓  |      | _String_ |                |        |
| 6   | dataInvio                                                                     |     |  ✓  |      |  _Date_  |                |        |
| 7   | latitudine                                                                    |     |     |      | _String_ |                |        |
| 8   | longitudine                                                                   |     |     |      | _String_ |                |        |

-----------------------------------------------------------------------------------------------------------------------------------------------

<a name="area-presidio-bee"></a>
####[34. AreaPresidioBee](#area-presidio-bee) __[☢](#vincoli-area-presidio-bee) [✎](#diagramma-presidio-bee) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |      Attribute Name      | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|--------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idAreaPresidioBee`__  |  ♔  |     |      | _String_ |                |        |
| 2   | [`idBee`](#bee)          |  ♕  |  ✓  |      | _String_ |                | __[`RA 38`](#RA38)__ |
| 3   | tipoPresidio             |     |  ✓  |      | _String_ | __`predefinito`<br/>`corrente`__ | __[`RA 60`](#RA60)__ |
| 4   | descrizione              |     |     |      | _String_ |                |        |
| 5   | timestamp                |     |  ✓  |      |  _Date_  |                |        |
| 6   | latitudine               |     |  ✓  |      | _String_ |                |        |
| 7   | longitudine              |     |  ✓  |      | _String_ |                |        |
| 8   | raggio                   |     |     |      | _Number_ |                |        |
| 9   | comune                   |     |  ✓  |      | _String_ |                |        |
| 10  | provincia                |     |  ✓  |      | _String_ |                |        |
| 11  | via                      |     |     |      | _String_ |                |        |
| 12  | codicePostale            |     |     |      | _String_ |                |        |
| 13  | località                 |     |     |      | _String_ |                |        |

------------------------------------------------------------------------------------------

<a name="luogo-task"></a>
####[35. LuogoTask](#luogo-task) __[☢](#vincoli-luogo-task) [✎](#diagramma-presidio-bee) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |   Attribute Name   | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|--------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __`idLuogoTask`__  |  ♔  |     |      | _String_ |                |        |
| 2   | [`idTask`](#task)  |  ♕  |  ✓  |  ⚠   | _String_ |                | __[`RA 39`](#RA39)__ |
| 3   | descrizione        |     |     |      | _String_ |                |        |
| 4   | timestamp          |     |  ✓  |      |  _Date_  |                |        |
| 5   | latitudine         |     |  ✓  |      | _String_ |                |        |
| 6   | longitudine        |     |  ✓  |      | _String_ |                |        |
| 7   | raggio             |     |     |      | _Number_ |                |        |
| 8   | comune             |     |  ✓  |      | _String_ |                |        |
| 9   | provincia          |     |  ✓  |      | _String_ |                |        |
| 10  | via                |     |     |      | _String_ |                |        |
| 11  | codicePostale      |     |     |      | _String_ |                |        |
| 12  | località           |     |     |      | _String_ |                |        |

------------------------------------------------------------------------------------

<a name="svolgimento-sequenza-azioni-task"></a>
###[36. SvolgimentoSequenzaAzioniTask](#svolgimento-sequenza-azioni-task) __[☢](#vincoli-svolgimento-sequenza-azioni-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__

> `♔ referenced by` : [`AzioneSvoltaTask`](#azione-svolta-task)

|  #  |                            Attribute Name                           | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|---------------------------------------------------------------------|:---:|:---:|:----:|:----------:|:---------------|:------:|
| 1   | __`idSvolgimentoSequenzaAzioniTask`__                               |  ♔  |     |      |  _String_  |                |        |
| 2   | [`idAssegnazioneTask`](#assegnazione-task)                           |  ♕  |  ✓  |  ⚛   |  _String_  |                | __[`TODO`](#)__ |
| 3   | [`idSequenzaRichiestaAzioniTask`](#sequenza-richiesta-azioni-task)  |  ♕  |  ✓  |  ⚛   |  _String_  |                | __[`TODO`](#)__ |
| 4   | bonus                                                               |     |  ✓  |      |  _Boolean_ |  __`true` `false`__ |        |

---------------------------------------------------------------------------------------------------------------------------------------

<a name="tabella-azione-svolta-task"></a>
###[37. AzioneSvoltaTask](#azione-svolta-task) __[☢](#vincoli-azione-svolta-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__

> `♔ referenced by` : _[`QuestionarioSvoltoTask`](#questionario-svolto-task)_ _[`ImmagineRicevutaTask`](#immagine-ricevuta-task)_ _[`FilmatoRicevutoTask`](#filmato-ricevuto-task)_

|  #  |                              Attribute Name                             | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|-------------------------------------------------------------------------|:---:|:---:|:----:|:----------:|:---------------|:------:|
| 1   | __`idAzioneSvoltaTask`__                                                |  ♔  |     |      |  _String_  |                |        |
| 2   | [`idSvolgimentoSequenzaAzioniTask`](#svolgimento-sequenza-azioni-task)  |  ♕  |  ✓  |      |  _String_  |                | __[`TODO`](#)__ |
| 3   | [`idAzioneRichiestaTask`](#azione-richiesta-task)                       |  ♕  |  ✓  |      |  _String_  |                | __[`TODO`](#)__ |
| 4   | tipoAzioneSvolta                                                        |     |  ✓  |      |  _String_  | __`foto`<br/>`video`<br/>`questionario`__ | __[`TODO`](#)__ |

-------------------------------------------------------------------------------------------------------------------------------------------

<a name="questionario-svolto-task"></a>
###[38. QuestionarioSvoltoTask](#questionario-svolto-task) __[☢](#vincoli-questionario-svolto-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__

> `♔ referenced by` : [`RispostaRicevutaQuestionarioTask`](#risposta-ricevuta-questionario-task)

|  #  |                 Attribute Name               | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|----------------------------------------------|:---:|:---:|:----:|:----------:|:---------------|:------:|
| 1   | __`idQuestionarioSvoltoTask`__               |  ♔  |     |      |  _String_  |                |        |
| 2   | [`idAzioneSvoltaTask`](#azione-svolta-task)  |  ♕  |  ✓  |      |  _String_  |                | __[`TODO`](#)__ |
| 3   | dataUltimoAggiornamento                      |     |     |      |   _Date_   |                |        |

----------------------------------------------------------------------------------------------------------

<a name="risposta-ricevuta-questionario-task"></a>
###[39. RispostaRicevutaQuestionarioTask](#risposta-ricevuta-questionario-task) __[☢](#vincoli-risposta-ricevuta-questionario-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__

> `♔ referenced by` : ✗

|  #  |                                Attribute Name                                 | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|-------------------------------------------------------------------------------|:---:|:---:|:----:|:----------:|:---------------|:------:|
| 1   | __`idRispostaRicevutaQuestionarioTask`__                                      |  ♔  |     |      |  _String_  |                |        |
| 2   | [`idQuestionarioSvoltoTask`](#questionario-svolto-task)                       |  ♕  |  ✓  |      |  _String_  |                | __[`TODO`](#)__ |
| 3   | [`idDomandaRichiestaQuestionarioTask`](#domanda-richiesta-questionario-task)  |  ♕  |  ✓  |      |  _String_  |                | __[`TODO`](#)__ |
| 4   | [`idOpzioneRispostaQuestionarioTask`](#opzione-risposta-questionario-task)    |  ♕  |  ✓  |      |  _String_  |                | __[`TODO`](#)__ |
| 5   | dataInvio                                                                     |     |  ✓  |      |   _Date_   |                |        |
| 6   | latitudine                                                                    |     |     |      |   _Date_   |                |        |
| 7   | longitudine                                                                   |     |     |      |   _Date_   |                |        |

-------------------------------------------------------------------------------------------------------------------------------------------------

<a name="regole-aziendali"></a>
###Regole Aziendali - Business Rules ☆

<a name="RA1"></a>
* __[`☆ RA 1`](#RA1) [☝](#indice)__
    * `Descrizione ✍`: Ogni Utente ( Bee o Beekeeper ) deve possedere un'unica 
       Credenziale di Accesso alla piattaforma web. Ogni Credenziale deve
       corrispondere ad un solo Utente.
    * `Strutture ⚒`: [`1.Bee`](#bee) [`2.Beekeeper`](#beekeeper)
    * `Vincoli ☢` : [`V1.1`](#V1) [`V1.2`](#V1) [`V2.1`](#V2) [`V2.2`](#V2).
<a name="RA2"></a>
* __[`☆ RA 2`](#RA2) [☝](#indice)__
    * `Descrizione ✍`: Ogni Utente ( Bee o Beekeeper ) deve possedere una username unica e univoca per
       autenticarsi sulla piattaforma web.
    * `Strutture ⚒`: [`3.CredenzialeAccessoUtente`](#credenziali-accesso-utente)
    * `Vincoli ☢`: [`V3.1`](#V3).
<a name="RA3"></a>
* __[`☆ RA 3`](#RA3) [☝](#indice)__
    * `Descrizione ✍`: Ogni Credenziale Utente deve possedere una email unica e univoca per
       autenticarsi sulla piattaforma web.
    * `Strutture ⚒`: [`3.CredenzialeAccessoUtente`](#credenziali-accesso-utente)
    * `Vincoli ☢`: [`V3.2`](#V3).
<a name="RA4"></a>
* __[`☆ RA 4`](#RA4) [☝](#indice)__
    * `Descrizione ✍`: Associata ad ogni Credenziale di Accesso deve esistere al massimo
       un'occorrenza di una stessa Social Platform ID ( Twitter, Facebook, LinkedIn, .. ).
    * `Strutture ⚒`: [`3.CredenzialeAccessoUtente`](#credenziali-accesso-utente).
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA5"></a>
* __[`☆ RA 5`](#RA5) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Utente ( Bee o Beekeeper ) deve essere associata una
       unica Anagrafica sulla piattaforma web. Ogni Anagrafica deve corrispondere
       ad un solo Utente.
    * `Strutture ⚒`: [`4.AnagraficaBee`](#anagrafica-bee) [`5.AnagraficaBeekeeper`](#anagrafica-beekeeper)
    * `Vincoli ☢`: [`V4.1`](#V4) [`V4.2`](#V4.2) [`V5.1`](#V5) [`V5.2`](#V5).
<a name="RA6"></a>
* __[`☆ RA 6`](#RA6) [`parziale della ☆ RA61`](#RA61) [☝](#indice)__.
    * `Descrizione ✍`: Ogni utente Bee deve possedere un codice fiscale unico.
       Ogni utente Beekeeper deve possedere un codice fiscale unico.
    * `Strutture ⚒`: [`4.AnagraficaBee`](#anagrafica-bee) [`5.AnagraficaBeekeeper`](#anagrafica-beekeeper)
    * `Vincoli ☢`: [`V4.3`](#V4) [`V5.3`](#V5).
<a name="RA7"></a>
* __[`☆ RA 7`](#RA7) [`parziale della ☆ RA62`](#RA62) [☝](#indice)__
    * `Descrizione ✍`: Ogni partita IVA in possesso da un utente Beekeeper deve
       essere unica e univoca tra tutte le AnagraficheBeekeeper.
    * `Strutture ⚒`: [`5.AnagraficaBeekeeper`](#anagrafica-beekeeper)
    * `Vincoli ☢`: [`V5.4`](#V5).
<a name="RA8"></a>
* __[`☆ RA 8`](#RA8) [`parziale della ☆ RA62`](#RA62) [☝](#indice)__
    * `Descrizione ✍`: Ogni utente Bee, di cui la tipologia fiscale sia diversa da 
       `privato`, deve possedere una partita IVA unica e univoca tra tutte le
       AnagraficheBee.
    * `Strutture ⚒`: [`4.AnagraficaBee`](#anagrafica-bee).
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA9"></a>
* __[`☆ RA 9`](#RA9) [☝](#indice)__
    * `Descrizione ✍`: Tra i Preferiti di un certo Bee possono essere aggiunti solo
       utenti Beekeeper già esistenti, ogni Beekeeper deve apparire una sola volta.
    * `Strutture ⚒`: [`6.PreferitiBee`](#preferiti-bee)
    * `Vincoli ☢`: [`V6.1`](#V6) [`V6.2`](#V6) [`V6.3`](#V6). 
<a name="RA10"></a>
* __[`☆ RA 10`](#RA10) [☝](#indice)__
    * `Descrizione ✍`: Tra i Preferiti di un Beekeeper possono essere aggiunti solo
       utenti Bee già esistenti, ogni Bee deve apparire una sola volta.
    * `Strutture ⚒`: [`7.PreferitiBeekeeper`](#preferiti-beekeeper)
    * `Vincoli ☢`: [`V7.1`](#V7) [`V7.2`](#V7) [`V7.3`](#V7).
<a name="RA11"></a>
* __[`☆ RA 11`](#RA11) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Prelievo deve corrispondere un utente Bee.
    * `Strutture ⚒`: [`8.PrelievoBee`](#prelievo-bee)
    * `Vincoli ☢`: [`V8.1`](#V8)
<a name="RA12"></a>
* __[`☆ RA 12`](#RA12) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Prelievo deve essere associato un unico codice di
      operazione.
    * `Strutture ⚒`: [`8.PrelievoBee`](#prelievo-bee)
    * `Vincoli ☢`: [`V8.2`](#V8)
<a name="RA13"></a>
* __[`☆ RA 13`](#RA13) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Versamento deve corrispondere un utente Beekeeper.
    * `Strutture ⚒`: [`9.VersamentoBeekeeper`](#versamento-beekeeper)
    * `Vincoli ☢`: [`V9.1`](#V9)
<a name="RA14"></a>
* __[`☆ RA 14`](#RA14) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Versamento deve essere associato un unico codice di
      operazione.
    * `Strutture ⚒`: [`9.VersamentoBeekeeper`](#versamento-beekeeper)
    * `Vincoli ☢`: [`V9.2`](#V9)
<a name="RA15"></a>
* __[`☆ RA 15`](#RA15) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Documento Fiscale di un utente Bee deve essere associata
       un'unica operazione di Prelievo. Ad ogni Prelievo eseguito con successo da un Bee,
       deve corrispondere un'unico Documento Fiscale (Bee).
    * `Strutture ⚒`: [`10.DocumentoFiscaleBee`](#documento-fiscale-bee)
    * `Vincoli ☢`: [`V10.1`](#V10) [`V10.2`](#V10)
<a name="RA16"></a>
* __[`☆ RA 16`](#RA16) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Documento Fiscale di un utente Beekeeper deve essere
       associata un'unica operazione di Versamento. Ad ogni Versamento eseguito
       con successo da un Beekeeper, deve corrispondere un'unico Documento Fiscale
        (Beekeeper).
    * `Strutture ⚒`: [`11.DocumentoFiscaleBeekeeper`](#documento-fiscale-beekeeper)
    * `Vincoli ☢`: [`V11.1`](#V11) [`V11.2`](#V11)
<a name="RA17"></a>
* __[`☆ RA 17`](#RA17) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Feedback di un Bee verso un Beekeeper deve corrispondere
       un' Assegnazione Task 'completata'. Per ogni Assegnazione Task 'completata'
       il Beekeeper deve ricevere al massimo un solo Feedback da parte di un Bee.
    * `Strutture ⚒`: [`12.FeedbackBeeToBeekeeper`](#feedback-bee-to-beekeeper)
    * `Vincoli ☢`: [`V12.1`](#V12) [`V12.2`](#V12)
<a name="RA18"></a>
* __[`☆ RA 18`](#RA18) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Feedback di un Beekeeper verso un Bee deve corrispondere
       un' Assegnazione Task 'completata'. Per ogni Assegnazione Task 'completata'
       il Bee deve ricevere un solo Feedback da parte di un Beekeeper.
    * `Strutture ⚒`: [`13.FeedbackBeekeeperToBee`](#feedback-beekeeper-to-bee)
    * `Vincoli ☢`: [`V13.1`](#V13) [`V13.2`](#V13)
<a name="RA19"></a>
* __[`☆ RA 19`](#RA19) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Chat Room deve corrispondere una Assegnazione Task.
       Ad ogni Assegnazione Task deve corrispondere un'unica Chat Room.
    * `Strutture ⚒`: [`14.ChatRoom`](#chat-room)
    * `Vincoli ☢`: [`V14.1`](#V14) [`V14.2`](#V14)
<a name="RA20"></a>
* __[`☆ RA 20`](#RA20) [☝](#indice)__
    * `Descrizione ✍`: Ogni Messaggio Chat deve essere associato ad una Chat Room,
       relativa ad una determinata Assegnazione Task.
    * `Strutture ⚒`: [`15.MessaggioChat`](#messaggio-chat)
    * `Vincoli ☢`: [`V15.1`](#V15)
<a name="RA21"></a>
* __[`☆ RA 21`](#RA21) [☝](#indice)__
    * `Descrizione ✍`: Per ogni messaggio di Notifica deve esistere un Utente
      (Bee o Beekeeper) destinatario.
    * `Strutture ⚒`: [`16.NotificaBee`](#notifica-bee) [`17.NotificaBeekeeper`](#notifica-beekeeper)
    * `Vincoli ☢`: [`V16.1`](#V16) [`V17.1`](#V17)
<a name="RA22"></a>
* __[`☆ RA 22`](#RA22) [☝](#indice)__
    * `Descrizione ✍`: Per ogni Candidatura devono esistere un Bee candidato ed un
       Task 'attivo'. E' possibile un'unica Candidatura di un Bee per un determinato Task.
    * `Strutture ⚒`: [`18.CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: [`V18.1`](#V18) [`V18.2`](#V18) [`V18.3`](#V18)
<a name="RA23"></a>
* __[`☆ RA 23`](#RA23) [☝](#indice)__
    * `Descrizione ✍`: Per ogni Assegnazione Task aggiunta da un Beekeeper, deve
       esistere una Candidatura al Task ( spontanea o su invito ) da parte di un
       Bee. Ad ogni Candidatura Task, può corrispondere al massimo una sola
       Assegnazione Task.
    * `Strutture ⚒`: [`19.AssegnazioneTask`](#assegnazione-task)
    * `Vincoli ☢`: [`V19.1`](#V19) [`V19.2`](#V19)
<a name="RA24"></a>
* __[`☆ RA 24`](#RA24) [☝](#indice)__
    * `Descrizione ✍`: Per ogni Accredito ad un Bee da parte di un Beekeeper, deve
       esistere una Assegnazione Task (di quel Bee). Ad ogni Assegnazione può
       corrispondere al massimo un solo Accredito.
    * `Strutture ⚒`: [`20.Accredito`](#accredito)
    * `Vincoli ☢`: [`V20.1`](#V20) [`V20.2`](#V20)
<a name="RA25"></a>
* __[`☆ RA 25`](#RA25) [☝](#indice)__
    * `Descrizione ✍`: Ogni Job deve cessere creato da un utente Beekeeper. Un Job
       appartiene ad un unico Beekeeper.
    * `Strutture ⚒`: [`21.Job`](#job)
    * `Vincoli ☢`: [`V21.1`](#V21) [`Job V21.2`](#V21)
<a name="RA26"></a>
* __[`☆ RA 26`](#RA26) [☝](#indice)__
    * `Descrizione ✍`: Ogni Task deve corrispondere ad un determinato Job.
       Un Task appartiene ad un unico Job.
    * `Strutture ⚒`: [`Task`](#task)
    * `Vincoli ☢`: [`V22.1`](#V22)
<a name="RA27"></a>
* __[`☆ RA 27`](#RA27) [☝](#indice)__
    * `Descrizione ✍`: Ogni SequenzaPredefinitaAzioniJob deve corrispondere ad un determinato Job.
       Una SequenzaPredefinitaAzioniJob appartiene ad un unico Job.
    * `Strutture ⚒`: [`SequenzaPredefinitaAzioniJob`](#sequenza-predefinita-azioni-job)
    * `Vincoli ☢`: [`V23.1`](#V23)
<a name="RA28"></a>
* __[`☆ RA 28`](#RA28) [☝](#indice)__
    * `Descrizione ✍`: Ogni SequenzaRichiestaAzioniTask deve corrispondere ad un determinato Task.
       Una SequenzaRichiestaAzioniTask appartiene ad un unico Task.
    * `Strutture ⚒`: [`SequenzaRichiestaAzioniTask`](#sequenza-richiesta-azioni-task)
    * `Vincoli ☢`: [`V24.1`](#V24)
<a name="RA29"></a>
* __[`☆ RA 29`](#RA29) [☝](#indice)__
    * `Descrizione ✍`: Ogni AzionePredefinitaJob deve corrispondere ad una determinata
       SequenzaPredefinitaAzioniJob. Un'AzionePredefinitaJob appartiene ad un'unica SequenzaPredefinitaAzioniJob.
    * `Strutture ⚒`: [`AzionePredefinitaJob`](#azione-predefinita-job)
    * `Vincoli ☢`: [`V25.1`](#V25)
<a name="RA30"></a>
* __[`☆ RA 30`](#RA30) [☝](#indice)__
    * `Descrizione ✍`: Ogni AzioneRichiestaTask deve corrispondere ad una determinata
       SequenzaRichiestaAzioniTask. Un'AzioneRichiestaTask appartiene ad un'unica SequenzaRichiestaAzioniTask.
    * `Strutture ⚒`: [`AzioneRichiestaTask`](#azione-richiesta-task)
    * `Vincoli ☢`: [`V26.1`](#V26)
<a name="RA31"></a>
* __[`☆ RA 31`](#RA31) [☝](#indice)__
    * `Descrizione ✍`: Ogni ImmagineRicevutaTask deve corrispondere ad una determinata
       AzioneRichiestaTask. Un'ImmagineRicevutaTask appartiene ad un'unica AzioneRichiestaTask.
    * `Strutture ⚒`: [`ImmagineRicevutaTask`](#immagine-ricevuta-task)
    * `Vincoli ☢`: [`V27.1`](#V27)
<a name="RA32"></a>
* __[`☆ RA 32`](#RA32) [☝](#indice)__
    * `Descrizione ✍`: Ogni FilmatoRicevutoTask deve corrispondere ad una determinata
       AzioneRichiestaTask. Un FilmatoRicevutoTask appartiene ad un'unica AzioneRichiestaTask.
    * `Strutture ⚒`: [`FilmatoRicevutoTask`](#filmato-ricevuto-task)
    * `Vincoli ☢`: [`V28.1`](#V28)
<a name="RA33"></a>
* __[`☆ RA 33`](#RA33) [☝](#indice)__
    * `Descrizione ✍`: Ogni ImmagineEsempioAzionePredefinitaJob deve corrispondere ad una determinata
       AzionePredefinitaJob. Un'ImmagineEsempioAzionePredefinitaJob appartiene ad un'unica AzionePredefinitaJob.
    * `Strutture ⚒`: [`ImmagineEsempioAzionePredefinitaJob`](#immagine-esempio-azione-predefinita-job)
    * `Vincoli ☢`: [`V29.1`](#V29)
<a name="RA34"></a>
* __[`☆ RA 34`](#RA34) [☝](#indice)__
    * `Descrizione ✍`: Ogni DomandaQuestionarioPredefinitoJob deve corrispondere ad una determinata
       AzionePredefinitaJob. Una DomandaQuestionarioPredefinitoJob appartiene ad un'unica AzionePredefinitaJob.
    * `Strutture ⚒`: [`DomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job)
    * `Vincoli ☢`: [`V30.1`](#V30)
<a name="RA35"></a>
* __[`☆ RA 35`](#RA35) [☝](#indice)__
    * `Descrizione ✍`: Ogni OpzioneRispostaQuestionarioPredefinitoJob deve corrispondere ad una determinata
       DomandaQuestionarioPredefinitoJob. Una OpzioneRispostaQuestionarioPredefinitoJob appartiene ad un'unica
       DomandaQuestionarioPredefinitoJob.
    * `Strutture ⚒`: [`OpzioneRispostaQuestionarioPredefinitoJob`](#opzione-risposta-questionario-predefinito-job)
    * `Vincoli ☢`: [`V31.1`](#V31)
<a name="RA36"></a>
* __[`☆ RA 36`](#RA36) [☝](#indice)__
    * `Descrizione ✍`: Ogni DomandaRichiestaQuestionarioTask deve corrispondere ad una determinata
       AzioneRichiestaTask. Una DomandaRichiestaQuestionarioTask appartiene ad un'unica AzioneRichiestaTask.
    * `Strutture ⚒`: [`DomandaRichiestaQuestionarioTask`](#domanda-richiesta-questionario-task)
    * `Vincoli ☢`: [`V32.1`](#V32)
<a name="RA37"></a>
* __[`☆ RA 37`](#RA37) [☝](#indice)__
    * `Descrizione ✍`: Ogni OpzioneRispostaQuestionarioTask deve corrispondere ad una determinata
       DomandaRichiestaQuestionarioTask. Una OpzioneRispostaQuestionarioTask appartiene ad un'unica
       DomandaRichiestaQuestionarioTask.
    * `Strutture ⚒`: [`OpzioneRispostaQuestionarioTask`](#opzione-risposta-questionario-task)
    * `Vincoli ☢`: [`V33.1`](#V33)
<a name="RA37"></a>
* __[`☆ RA 38`](#RA38) [☝](#indice)__
    * `Descrizione ✍`: Ad ogni Area di Presidio deve corrispondere un Bee. Un'Area
       di Presidio appartiene ad un unico Bee.
    * `Strutture ⚒`: [`AreaPresidioBee`](#area-presidio-bee)
    * `Vincoli ☢`: [`V34.1`](#V34)
<a name="RA39"></a>
* __[`☆ RA 39`](#RA39) [☝](#indice)__
    * `Descrizione ✍`: Per ogni LuogoTask deve corrispondere un determinato Task.
       Esiste un'unico LuogoTask per un determinato Task.
    * `Strutture ⚒`: [`LuogoTask`](#luogo-task)
    * `Vincoli ☢`: [`V35.1`](#V35) [`V35.2`](#V35)
<a name="RA40"></a>
* __[`☆ RA 40`](#RA40) [☝](#indice)__
    * `Descrizione ✍`: Lo stato di un Account Utente ( Bee o Beekeeper ) deve essere
      uno tra `attivo` o `disabilitato`.
    * `Strutture ⚒`: [`Bee`](#bee) [`Beekeeper`](#beekeeper)
    * `Vincoli ☢`: [`D1.3`](#V1) [`D2.3`](#V2)
<a name="RA41"></a>
* __[`☆ RA 41`](#RA41) [☝](#indice)__
    * `Descrizione ✍`: Lo stato di verifica delle Credenziali di Accesso di un Utente
       ( Bee o Beekeeper ) deve essere una tra `pendente` o `completata`.
    * `Strutture ⚒`: [`CredenzialiAccessoUtente`](#credenziali-accesso-utente)
    * `Vincoli ☢`: [`D3.3`](#V3)
<a name="RA42"></a>
* __[`☆ RA 42`](#RA42) [☝](#indice)__
    * `Descrizione ✍`: Lo tipologia fiscale di un utente Bee deve essere una tra
      `privato`, `libero professionista`, `ditta individuale` o `azienda`.
    * `Strutture ⚒`: [`AnagraficaBee`](#anagrafica-bee)
    * `Vincoli ☢`: [`D4.4`](#V4)
<a name="RA43"></a>
* __[`☆ RA 43`](#RA43) [☝](#indice)__
    * `Descrizione ✍`: Lo tipologia fiscale di un utente Beekeeper deve essere
       una tra `libero professionista`, `ditta individuale` o `azienda`.
    * `Strutture ⚒`: [`AnagraficaBeekeeper`](#anagrafica-beekeeper)
    * `Vincoli ☢`: [`D5.5`](#V5)
<a name="RA44"></a>
* __[`☆ RA 44`](#RA44) [☝](#indice)__
    * `Descrizione ✍`: lo stato di una operazione di Prelievo da parte di un utente
       Bee deve essere una tra __`????`__.
    * `Strutture ⚒`: [`PrelievoBee`](#prelievo-bee)
    * `Vincoli ☢`: [`D8.3`](#V8)
<a name="RA45"></a>
* __[`☆ RA 45`](#RA45) [☝](#indice)__
    * `Descrizione ✍`: lo stato di una operazione di Versamento da parte di un utente
       Beekeeper deve essere una tra __`????`__.
    * `Strutture ⚒`: [`VersamentoBeekeeper`](#versamento-beekeeper)
    * `Vincoli ☢`: [`D9.3`](#V9)
<a name="RA46"></a>
* __[`☆ RA 46`](#RA46) [☝](#indice)__
    * `Descrizione ✍`: la tipologia di un Documento Fiscale di un Utente ( Bee o 
       Beekeeper ) deve essere una tra `fattura`, `ritenuta`.
    * `Strutture ⚒`: [`DocumentoFiscaleBee`](#documento-fiscale-bee) [`DocumentoFiscaleBeekeeper`](#documento-fiscale-beekeeper)
    * `Vincoli ☢`: [`D10.3`](#V10) [`D11.3`](#V11)
<a name="RA47"></a>
* __[`☆ RA 47`](#RA47) [☝](#indice)__
    * `Descrizione ✍`: lo stato di una Chat Room deve essere uno tra `attiva` o `archiviata`.
    * `Strutture ⚒`: [`ChatRoom`](#chat-room)
    * `Vincoli ☢`: [`D14.3`](#V14)
<a name="RA48"></a>
* __[`☆ RA 48`](#RA48) [☝](#indice)__
    * `Descrizione ✍`: lo stato di una Chat Room deve essere uno tra `attiva` o `archiviata`.
    * `Strutture ⚒`: [`MessaggioChat`](#messaggio-chat)
    * `Vincoli ☢`: [`D15.4`](#V15)
<a name="RA49"></a>
* __[`☆ RA 49`](#RA49) [☝](#indice)__
    * `Descrizione ✍`: il tipo di Evento che produce una Notifica per un Utente
      ( Bee o BeeKeeeper ) deve essere uno tra `FeedbackBeeToBeekeeper`,
      `FeedbackBeekeeperToBee`, `Accredito`, `CandidaturaTask`, `AssegnazioneTask`.
    * `Strutture ⚒`: [`NotificaBee`](#notifica-bee) [`NotificaBeekeeper`](#notifica-beekeeper)
    * `Vincoli ☢`: [`D16.2`](#V16) [`D17.2`](#V17)
<a name="RA50"></a>
* __[`☆ RA 50`](#RA50) [☝](#indice)__
    * `Descrizione ✍`: il tipo di Candidatura di un Bee ad un Task deve essere su
       `invito` o `spontanea`.
    * `Strutture ⚒`: [`CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: [`D18.4`](#V18)
<a name="RA51"></a>
* __[`☆ RA 51`](#RA51) [☝](#indice)__
    * `Descrizione ✍`: lo stato di una Candidatura di un Bee ad un Task deve essere
       una tra `pendente`, `accettata`, `annullata`, `rifiutata`, `declinata`.
    * `Strutture ⚒`: [`CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: [`D18.5`](#V18)
<a name="RA52"></a>
* __[`☆ RA 52`](#RA52) [☝](#indice)__
    * `Descrizione ✍`: lo stato di una Assegnazione Task ad un Bee deve essere uno
       tra `attiva`, `completata`, `rifiutata`, `annullata`, `scaduta`.
    * `Strutture ⚒`: [`AssegnazioneTask`](#assegnazione-task)
    * `Vincoli ☢`: [`D19.6`](#V19)
<a name="RA53"></a>
* __[`☆ RA 53`](#RA53) [☝](#indice)__
    * `Descrizione ✍`: il tipo di Credenziale Accesso per un Utente, deve essere
       uno tra `Bee`, `Beekeeper`.
    * `Strutture ⚒`: [`CredenzialiAccessoUtente`](#credenziali-accesso-utente)
    * `Vincoli ☢`: [`D3.4`](#V3)
<a name="RA54"></a>
* __[`☆ RA 54`](#RA54) [☝](#indice)__
    * `Descrizione ✍`: Lo stato di pubblicazione di un Job deve essere uno tra
      `attiva`, `disabilitata`, `archiviata`.
    * `Strutture ⚒`: [`Job`](#job)
    * `Vincoli ☢`: [`D21.2`](#V21)
<a name="RA55"></a>
* __[`☆ RA 55`](#RA54) [☝](#indice)__
    * `Descrizione ✍`: Lo stato di pubblicazione di un Task deve essere uno tra
      `attiva`, `disabilitata`, `archiviata`.
    * `Strutture ⚒`: [`Task`](#task)
    * `Vincoli ☢`: [`D22.2`](#V22)
<a name="RA56"></a>
* __[`☆ RA 56`](#RA56) [☝](#indice)__
    * `Descrizione ✍`: il tipo di un'Azione definita per un Job deve essere una tra
        `foto`, `video`, `questionario`.
    * `Strutture ⚒`: [`AzionePredefinitaJob`](#azione-predefinita-job)
    * `Vincoli ☢`: [`D25.2`](#V25)
<a name="RA57"></a>
* __[`☆ RA 57`](#RA57) [☝](#indice)__
    * `Descrizione ✍`: il tipo di un'Azione definita per un Task deve essere una tra
        `foto`, `video`, `questionario`.
    * `Strutture ⚒`: [`AzioneRichiestaTask`](#azione-richiesta-task)
    * `Vincoli ☢`: [`D26.2`](#V26)
<a name="RA58"></a>
* __[`☆ RA 58`](#RA58) [☝](#indice)__
    * `Descrizione ✍`: il tipo di selezione per la serie di risposte relative ad una
       Domanda di un Questionario definito per un Azione ( Job o Task ), deve essere
       una tra `multipla`, `singola`.
    * `Strutture ⚒`: [`DomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job) [`DomandaRichiestaQuestionarioTask`](#domanda-richiesta-questionario-task)
    * `Vincoli ☢`: [`D30.2`](#V30) [`D32.2`](#V32)
<a name="RA59"></a>
* __[`☆ RA 59`](#RA59) [☝](#indice)__
    * `Descrizione ✍`: il tipo di una Risposta relativa ad un Questionario definito
       da un Azione ( Job o Task ) deve essere una tra `libera`, `precompilata`.
    * `Strutture ⚒`: [`OpzioneRispostaQuestionarioPredefinitoJob`](#opzione-risposta-questionario-predefinito-job) [`OpzioneRispostaQuestionarioTask`](#opzione-risposta-questionario-task)
    * `Vincoli ☢`: [`D31.2`](#V31) [`D33.2`](#V33)
<a name="RA60"></a>
* __[`☆ RA 60`](#RA60) [☝](#indice)__
    * `Descrizione ✍`: il tipo di Presidio di un Area geografica da parte di un Bee,
       deve essere uno tra `predefinito`, `corrente`.
    * `Strutture ⚒`: [`AreaPresidioBee`](#area-presidio-bee)
    * `Vincoli ☢`: [`D34.2`](#V34)
<a name="RA61"></a>
* __[`☆ RA 61`](#RA61) [`include la ☆ RA6`](#RA6) [☝](#indice)__
    * `Descrizione ✍`: Ogni Utente deve possedere un codice fiscale unico e univoco
       tra tutte le Anagrafiche degli Utenti.
    * `Strutture ⚒`: [`AnagraficaBee`](#anagrafica-bee) [`AnagraficaBeekeeper`](#anagrafica-beekeeper)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA62"></a>
* __[`☆ RA 62`](#RA62) [`include la ☆ RA7`](#RA7) [`include la ☆ RA8`](#RA8) [☝](#indice)__
    * `Descrizione ✍`: Ogni partita IVA in possesso dagli Utenti deve essere
       unica e univoca tra tutte le Anagrafiche degli Utenti.
    * `Strutture ⚒`: [`AnagraficaBee`](#anagrafica-bee) [`AnagraficaBeekeeper`](#anagrafica-beekeeper)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA63"></a>
* __[`☆ RA 63`](#RA63) [☝](#indice)__
    * `Descrizione ✍`: un Bee non può effettuare un Prelievo convertendo un importo
       di crediti superiore al suo attuale bankroll crediti.
    * `Strutture ⚒`: [`PrelievoBee`](#prelievo-bee) [`Bee`](#bee)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA64"></a>
* __[`☆ RA 64`](#RA64) [☝](#indice)__
    * `Descrizione ✍`:  un Beekeeper non può pubblicare un Job se i suoi crediti
       disponibili sono inferiori al totale crediti attualmente offerti per tutti
       i Task di quel Job.
    * `Strutture ⚒`: [`Task`](#task) [`Beekeeper`](#beekeeper)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA65"></a>
* __[`☆ RA 65`](#RA65) [☝](#indice)__
    * `Descrizione ✍`: Quando lo stato di verifica delle credenziali di un Utente
      è 'completato' lo stato del suo Account passa da 'disabilitato' ad 'attivo'.
    * `Strutture ⚒`: [`CredenzialiAccessoUtente`](#credenziali-accesso-utente) [`Bee`](#bee) [`Beekeeper`](#beekeeper)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA66"></a>
* __[`☆ RA 66`](#RA66) [☝](#indice)__
    * `Descrizione ✍`: Un Utente ( Bee o Beekeeper ), può effettuare operazioni
        sulla piattaforma ( quali Versamenti, Prelievi, Candidature, Accrediti ),
        solo se lo stato del suo Account è 'attivo'.
    * `Strutture ⚒`: [`Bee`](#) [`Beekeeper`](#beekeeper).
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA67"></a>
* __[`☆ RA 67`](#RA67) [☝](#indice)__
    * `Descrizione ✍`: Un Bee può presentare una propria Candidatura ad un Task
       solo se lo stato della pubblicazione del Task è 'attiva'.
    * `Strutture ⚒`: [`Task`](#task) [`CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA68"></a>
* __[`☆ RA 68`](#RA68) [☝](#indice)__
    * `Descrizione ✍`: Un Beekeeper può invitare a candidarsi un Bee per un Task,
       solo se lo stato della pubblicazione del Task è 'attiva'.
    * `Strutture ⚒`: [`Task`](#task) [`CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA69"></a>
* __[`☆ RA 69`](#RA69) [☝](#indice)__
    * `Descrizione ✍`: Quando un Beekeeper rifiuta una Candidatura spontanea
       ad un Task, lo stato della Candidatura deve essere 'declinata'.
    * `Strutture ⚒`: [`CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA70"></a>
* __[`☆ RA 70`](#RA70) [☝](#indice)__
    * `Descrizione ✍`: Quando un Bee rifiuta una Candidatura su invito ad un Task,
       lo stato della Candidatura deve essere 'rifutata'.
    * `Strutture ⚒`: [`CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA71"></a>
* __[`☆ RA 71`](#RA71) [☝](#indice)__
    * `Descrizione ✍`: L'importo dell'offerta crediti di un Bee, espresso per
       una Candidatura ad un Task, se non specificato direttamente, deve essere
       uguale al totale dei crediti originalmente offerti dal Beekeeper per quel
       Task.
    * `Strutture ⚒`: [`CandidaturaTask`](#candidatura-task) [`Task`](#task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA72"></a>
* __[`☆ RA 72`](#RA72) [☝](#indice)__
    * `Descrizione ✍`: Quando è aggiunta un'Assegnazione di un Bee ad un Task, a
       partire da una Candidatura, i crediti pattuiti nell'Assegnazione devono
       essere uguali ai crediti offerti dal Bee, nella Candidatura associata.
    * `Strutture ⚒`: [`CandidaturaTask`](#candidatura-task) [`AssegnazioneTask`](#assegnazione-task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA73"></a>
* __[`☆ RA 73`](#RA73) [☝](#indice)__
    * `Descrizione ✍`: Si può disabilitare la pubblicazione di un Task solo
       se non esiste una Assegnazione 'attiva' per quel Task.
    * `Strutture ⚒`: [`Task`](#task) [`AssegnazioneTask`](#assegnazione-task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA74"></a>
* __[`☆ RA 74`](#RA74) [☝](#indice)__
    * `Descrizione ✍`: E' possibile 'disabilitare' la pubblicazione di un Job solo
       se è possibile disabilitare la pubblicazione di tutti i suoi Task.
    * `Strutture ⚒`: [`Job`](#job) [`Task`](#task)
    * `Vincoli ☢`: __[`None`](#)__.
<a name="RA75"></a>
* __[`☆ RA 75`](#RA75) [☝](#indice)__
    * `Descrizione ✍`: Quando la pubblicazione di un Task viene 'disabilitata',
       ogni Candidatura al Task deve essere 'annullata'.
    * `Strutture ⚒`: [`Task`](#task) [`CandidaturaTask`](#candidatura-task)
    * `Vincoli ☢`: __[`None`](#)__.

> __TODO..__

--------------------------------------------------------------------------------

<a name="vincoli"></a>
###Vincoli ☢

<a name="vincoli-bee"></a>
<a name="V1"></a>
* [1. Bee](#vincoli-bee) __[⚒](#bee) [✎](#diagramma-relazioni-utente) [☝](#indice)__
    * [`V1.1 ♕`](#V1.1) : Bee( idCredenzialiAccessoUtente ) -> CredenzialiAccessoUtente( idCredenzialiAccessoUtente ). [`☆ RA 1`](#RA1)
    * [`V1.2 ⚠`](#V1.2) : unique( CredenzialiAccessoUtente( idCredenzialiAccessoUtente ) ). [`☆ RA 1`](#RA1).
    * [`D1.3`](#D1.3) : Bee( statoAccount ) -> [ 'attivo', 'disabilitato' ]. [`☆ RA 40`](#RA40)

<a name="vincoli-beekeeper"></a>
<a name="V2"></a>
* [2. Beekeeper](#vincoli-beekeeper) __[⚒](#beekeeper) [✎](#diagramma-relazioni-utente) [☝](#indice)__
    * [`V2.1 ♕`](#V2.1) : Beekeeper( idCredenzialiAccessoUtente ) -> CredenzialiAccessoUtente( idCredenzialiAccessoUtente ). [`☆ RA 1`](#RA1)
    * [`V2.2 ⚠`](#V2.2) : unique( CredenzialiAccessoUtente( idCredenzialiAccessoUtente ) ). [`☆ RA 1`](#RA1)
    * [`D2.3 ⚡`](#D2.3) : Beekeeper( statoAccount ) -> [ 'attivo', 'disabilitato' ]. [`☆ RA 40`](#RA40)

<a name="vincoli-credenziali-accesso-utente"></a>
<a name="V3"></a>
* [3. CredenzialiAccessoUtente](#vincoli-credenziali-accesso-utente) __[⚒](#credenziali-accesso-utente) [✎](#diagramma-credenziali-utente) [☝](#indice)__
    * [`V3.1 ⚠`](#V3.1) : unique( CredenzialiAccessoUtente( email ) ). [`☆ RA 2`](#RA2)
    * [`V3.2 ⚠`](#V3.2) : unique( CredenzialiAccessoUtente( username ) ). [`☆ RA 3`](#RA3)
    * [`D3.3 ⚡`](#D3.3) : CredenzialiAccessoUtente( statoVerifica ) -> [ 'pendente', 'completata' ]. [`☆ RA 41`](#RA41)
    * [`D3.4 ⚡`](#D3.4) : CredenzialiAccessoUtente( tipoUtente ) -> [ 'Bee', 'Beekeeper' ]. [`☆ RA 53`](#RA53)

<a name="vincoli-anagrafica-bee"></a>
<a name="V4"></a>
* [4. AnagraficaBee](#vincoli-anagrafica-bee) __[⚒](#anagrafica-bee) [✎](#diagramma-credenziali-utente) [☝](#indice)__
    * [`V4.1 ♕`](#V4.1) : AnagraficaBee( idBee ) -> Bee( idBee ). [`☆ RA 5`](#RA5)
    * [`V4.2 ⚠`](#V4.2) : unique( AnagraficaBee( idBee ) ). [`☆ RA 5`](#RA5)
    * [`V4.3 ⚠`](#V4.3) : unique( AnagraficaBee( codiceFiscale ) ). [`☆ RA 6`](#RA6)
    * [`D4.4 ⚡`](#D4.4) : AnagraficaBee( tipologiaFiscale ) -> [ 'privato', 'libero professionista', 'ditta individuale', 'azienda' ]. [`☆ RA 42`](#RA42)

<a name="vincoli-anagrafica-beekeeper"></a>
<a name="V5"></a>
* [5. AnagraficaBeekeeper](#vincoli-anagrafica-beekeeper) __[⚒](#anagrafica-beekeeper) [✎](#diagramma-credenziali-utente) [☝](#indice)__
    * [`V5.1 ♕`](#V5.1) : AnagraficaBeekeeper( idBeekeeper ) -> Beekeeper( idBeekeeper ). [`☆ RA 5`](#RA5)
    * [`V5.2 ⚠`](#V5.2) : unique( AnagraficaBeekeeper( idBeekeeper ) ). [`☆ RA 5`](#RA5)
    * [`V5.3 ⚠`](#V5.3) : unique( AnagraficaBeekeeper( codiceFiscale ) ). [`☆ RA 6`](#RA6)
    * [`V5.4 ⚠`](#V5.4) : unique( AnagraficaBeekeeper( partitaIVA ) ). [`☆ RA 7`](#RA7)
    * [`D5.5 ⚡`](#D5.5) : AnagraficaBeekeeper( tipologiaFiscale ) -> [ 'libero professionista', 'ditta individuale', 'azienda' ]. [`☆ RA 43`](#RA43)

<a name="vincoli-preferiti-bee"></a>
<a name="V6"></a>
* [6. PreferitiBee](#vincoli-preferiti-bee) __[⚒](#preferiti-bee) [✎](#diagramma-relazioni-utente) [☝](#indice)__
    * [`V6.1 ♕`](#V6.1) : PreferitiBee( idBee ) -> Bee( idBee ). [`☆ RA 9`](#RA9)
    * [`V6.2 ♕`](#V6.2) : PreferitiBee( idBeekeeper ) -> Beekeeper( idBeekeeper ). [`☆ RA 9`](#RA9)
    * [`V6.3 ♔`](#V6.3) : unique( PreferitiBee( idBee ), PreferitiBee( idBeekeeper ). ) [`☆ RA 9`](#RA9)

<a name="vincoli-preferiti-beekeeper"></a>
<a name="V7"></a>
* [7. PreferitiBeekeeper](#vincoli-preferiti-beekeeper) __[⚒](#preferiti-beekeeper) [✎](#diagramma-relazioni-utente) [☝](#indice)__
    * [`V7.1 ♕`](#V7.1) : PreferitiBeekeeper( idBeekeeper ) -> Beekeeper( idBeekeeper ). [`☆ RA 10`](#RA10)
    * [`V7.2 ♕`](#V7.2) : PreferitiBeekeeper( idBee ) -> Bee( idBee ). [`☆ RA 10`](#RA10)
    * [`V7.3 ♔`](#V7.3) : unique( PreferitiBeeKeeeper( idBeekeeper ), PreferitiBeekeeper( idBee ) ). [`☆ RA 10`](#RA10)

<a name="vincoli-prelievo-bee"></a>
<a name="V8"></a>
* [8. PrelievoBee](#vincoli-prelievo-bee) __[⚒](#prelievo-bee) [✎](#diagramma-transazioni-utente) [☝](#indice)__
    * [`V8.1 ♕`](#V8.1) : PrelievoBee( idBee ) -> Bee( idBee ). [`☆ RA 11`](#RA11)
    * [`V8.2 ⚠`](#V8.2) : unique( PrelievoBee( codiceOperazione ) ). [`☆ RA 12`](#RA12)
    * [`D8.3 ⚡`](#D8.3) : PrelievoBee( statoOperazione ) -> [ __'????'__ ]. [`☆ RA 44`](#RA44)

<a name="vincoli-versamento-beekeeper"></a>
<a name="V9"></a>
* [9. VersamentoBeekeeper](#vincoli-versamento-beekeeper) __[⚒](#versamento-beekeeper) [✎](#diagramma-transazioni-utente) [☝](#indice)__
    * [`V9.1 ♕`](#V9.1) : VersamentoBeekeeper( idBeekeeper ) -> Beekeeper( idBeekeeper ). [`☆ RA 13`](#RA13)
    * [`V9.2 ⚠`](#V9.2) : unique( VersamentoBeekeeper( codiceOperazione ) ). [`☆ RA 14`](#RA14)
    * [`D9.3 ⚡`](#D9.3) : VersamentoBeekeeper( statoOperazione ) -> [ __'????'__ ]. [`☆ RA 45`](#RA45)

<a name="vincoli-documento-fiscale-bee"></a>
<a name="V10"></a>
* [10. DocumentoFiscaleBee](#vincoli-documento-fiscale-bee) __[⚒](#documento-fiscale-bee) [✎](#diagramma-transazioni-utente) [☝](#indice)__
    * [`V10.1 ♕`](#V10.1) : DocumentoFiscaleBee( idPrelievoBee ) -> PrelievoBee( idPrelievoBee ). [`☆ RA 15`](#RA15)
    * [`V10.2 ⚠`](#V10.2) : unique( DocumentoFiscaleBee( idPrelievoBee ) ). [`☆ RA 15`](#RA15)
    * [`D10.3 ⚡`](#D10.3) : DocumentoFiscaleBee( tipoDocumento ) -> [ 'fattura', 'ritenuta' ]. [`☆ RA 46`](#RA46)

<a name="vincoli-documento-fiscale-beekeeper"></a>
<a name="V11"></a>
* [11. DocumentoFiscaleBeekeeper](#vincoli-documento-fiscale-beekeeper) __[⚒](#documento-fiscale-beekeeper) [✎](#diagramma-transazioni-utente) [☝](#indice)__
    * [`V11.1 ♕`](#V11.1) : DocumentoFiscaleBeekeeper( idVersamentoBeekeeper ) -> VersamentoBeekeeper( idVersamentoBeekeeper ). [`☆ RA 16`](#RA16 )
    * [`V11.2 ⚠`](#V11.2) : unique( DocumentoFiscaleBeekeeper( idVersamentoBeekeeper ) ). [`☆ RA 16`](#RA16)
    * [`D11.3 ⚡`](#D11.3) : DocumentoFiscaleBeekeeper( tipoDocumento ) -> [ 'fattura', 'ritenuta' ]. [`☆ RA 46`](#RA46)

<a name="vincoli-feedback-bee-to-beekeeper"></a>
<a name="V12"></a>
* [12. FeedbackBeeToBeekeeper](#vincoli-feedback-bee-to-beekeeper) __[⚒](#feedback-bee-to-beekeeper) [✎](#diagramma-feedbacks) [☝](#indice)__
    * [`V12.1 ♕`](#V12.1) : FeedbackBeeToBeekeeper( idAssegnazioneTask ) -> AssegnazioneTask( idAssegnazioneTask ). [`☆ RA 17`](#RA17)
    * [`V12.2 ⚠`](#V12.2) : unique( FeedbackBeeToBeekeeper( idAssegnazioneTask ) ). [`☆ RA 17`](#RA17)
    * [`VR12.3 ♖`](#V12.3) : FeedbackBeeToBeekeeper( idBee ) -> Bee( idBee )
    * [`VR12.4 ♖`](#V12.4) : FeedbackBeeToBeekeeper( idBeekeeper ) -> Beekeeper( idBeekeeper )

<a name="vincoli-feedback-beekeeper-to-bee"></a>
<a name="V13"></a>
* [13. FeedbackBeekeeperToBee](#vincoli-feedback-beekeeper-to-bee) __[⚒](#feedback-beekeeper-to-bee) [✎](#diagramma-feedbacks) [☝](#indice)__
    * [`V13.1 ♕`](#V13.1) : FeedbackBeekeeperToBee( idAssegnazioneTask ) -> AssegnazioneTask( idAssegnazioneTask ) . [`☆ RA 18`](#RA18)
    * [`V13.2 ⚠`](#V13.2) : unique( FeedbackBeekeeperToBee( idAssegnazioneTask ) ). [`☆ RA 18`](#RA18)
    * [`VR13.3 ♖`](#V13.3) : FeedbackBeekeeperToBee( idBeekeeper ) -> Beekeeper( idBeekeeper )
    * [`VR13.4 ♖`](#V13.4) : FeedbackBeekeeperToBee( idBee ) -> Bee( idBee )

<a name="vincoli-chat-room"></a>
<a name="V14"></a>
* [14. ChatRoom](#vincoli-chat-room) __[⚒](#chat-room) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__
    * [`V14.1 ♕`](#V14.1) : ChatRoom( idAssegnazioneTask ) -> AssegnazioneTask( idAssegnazioneTask ). [`☆ RA 19`](#RA19)
    * [`V14.2 ⚠`](#V14.2) : unique( ChatRoom( idAssegnazioneTask ) ). [`☆ RA 19`](#RA19)
    * [`D14.3 ⚡`](#D14.3) : ChatRoom( statoChatRoom ) -> [ 'attiva'. 'archiviata' ]. [`☆ RA 47`](#RA47)

<a name="vincoli-messaggio-chat"></a>
<a name="V15"></a>
* [15. MessaggioChat](#vincoli-messaggio-chat) __[⚒](#messaggio-chat) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__
    * [`V15.1 ♕`](#V15.1) : MessaggioChat( idChatRoom ) -> ChatRoom( idChatRoom ). [`☆ RA 20`](#RA20)
    * [`VR15.2 ♖`](#V15.2) : MessaggioChat( idBee ) -> Bee( idBee )
    * [`VR15.3 ♖`](#V15.3) : MessaggioChat( idBeekeeper ) -> Bee( idBeekeeper )
    * [`D15.4 ⚡`](#D15.4) : MessaggioChat( tipoMittente ) -> [ 'Bee', 'Beekeeper' ] . [`☆ RA 48`](#RA48)

<a name="vincoli-notifica-bee"></a>
<a name="V16"></a>
* [16. NotificaBee](#vincoli-notifica-bee) __[⚒](#notifica-bee) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__
    * [`V16.1 ♕`](#V16.1) : NotificaBee( idBeeDestinatario ) -> Bee( idBee ). [`☆ RA 21`](#RA21)
    * [`D16.2 ⚡`](#D16.2) : NotificaBee( tipoEvento ) -> [ 'FeedbackBeeToBeekeeper', 'FeedbackBeekeeperToBee', 'Accredito', 'CandidaturaTask', 'AssegnazioneTask' ]. [`☆ RA 49`](#RA49)

<a name="vincoli-notifica-beekeeper"></a>
<a name="V17"></a>
* [17. NotificaBeekeeper](#vincoli-notifica-beekeeper) __[⚒](#notifica-beekeeper) [✎](#diagramma-messaggi-e-notifiche) [☝](#indice)__
    * [`V17.1 ♕`](#V17.1) : NotificaBeekeeper( idBeekeeperDestinatario ) -> Beekeeper( idBeekeeper ). [`☆ RA 21`](#RA21)
    * [`D17.2 ⚡`](#D17.2) : NotificaBee( tipoEvento ) -> [ 'FeedbackBeeToBeekeeper', 'FeedbackBeekeeperToBee', 'Accredito', 'CandidaturaTask', 'AssegnazioneTask' ]. [`☆ RA 49`](#RA49)

<a name="vincoli-candidatura-task"></a>
<a name="V18"></a>
* [18. CandidaturaTask](#vincoli-candidatura-task) __[⚒](#candidatura-task) [✎](#diagramma-assegnazioni-e-candidature-task) [☝](#indice)__
    * [`V18.1 ♕`](#V18.1) : CandidaturaTask( idTask ) -> Task( idTask ). [`☆ RA 22`](#RA22)
    * [`V18.2 ♕`](#V18.2) : CandidaturaTask( idBee ) -> Bee( idBee ). [`☆ RA 22`](#RA22)
    * [`V18.3 ⚛`](#V18.3) : unique( CandidaturaTask( idTask ), CandidaturaTask( idBee ) ). [`☆ RA 22`](#RA22)
    * [`D18.4 ⚡`](#D18.4) : CandidaturaTask( tipoCandidatura ) -> [ 'invito', 'spontanea' ]. [`☆ RA 50`](#RA50)
    * [`D18.5 ⚡`](#D18.5) : CandidaturaTask( statoCandidatura ) -> [ 'pendente', 'accettata', 'annullata', 'rifiutata', 'declinata' ]. [`☆ RA 51`](#RA51)

<a name="vincoli-assegnazione-task"></a>
<a name="V19"></a>
* [19. AssegnazioneTask](#vincoli-assegnazione-task) __[⚒](#assegnazione-task) [✎](#diagramma-assegnazioni-e-candidature-task) [☝](#indice)__
    * [`V19.1 ♕`](#V19.1) : AssegnazioneTask( idCandidaturaTask ) -> CandidaturaTask( idCandidaturaTask ). [`☆ RA 23`](#RA23)
    * [`V19.2 ⚠`](#V19.2) : unique( AssegnazioneTask( idCandidaturaTask ) ). [`☆ RA 23`](#RA23)
    * [`VR19.3 ♖`](#V19.3) : AssegnazioneTask( idTask ) -> Task( idTask )
    * [`VR19.4 ♖`](#V19.4) : AssegnazioneTask( idBee ) -> Bee( idBee )
    * [`VR19.5 ♖`](#V19.5) : AssegnazioneTask( idBeekeeper ) -> Bee( idBeekeeper )
    * [`D19.6 ⚡`](#D19.6) : AssegnazioneTask( statoCandidatura ) -> [ 'attiva', 'completata', 'rifiutata', 'annullata', 'scaduta' ]. [`☆ RA 52`](#RA52)

<a name="vincoli-accredito"></a>
<a name="V20"></a>
* [20. Accredito](#vincoli-accredito) __[⚒](#accredito) [✎](#diagramma-assegnazioni-e-candidature-task) [☝](#indice)__
    * [`V20.1 ♕`](#V20.1) : Accredito( idAssegnazioneTask ) -> AssegnazioneTask( idAssegnazioneTask ). [`☆ RA 24`](#RA23)
    * [`V20.2 ⚠`](#V20.2) : unique( Accredito( idAssegnazioneTask ) ). [`☆ RA 24`](#RA24)
    * [`VR20.3 ♖`](#V20.3) : Accredito( idBeekeeper ) -> Beekeeper( idBeekeeper )
    * [`VR20.4 ♖`](#V20.4) : Accredito( idBee ) -> Bee( idBee )

<a name="vincoli-job"></a>
<a name="V21"></a>
* [21. Job](#vincoli-job) __[⚒](#job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V21.1 ♕`](#V21.1) : Job( idBeekeeper ) -> Beekeeper( idBeekeeper ). [`☆ RA 25`](#RA25)
    * [`D21.2 ⚡`](#D21.2) : Job( statoJob ) -> [ 'attiva', 'disabilitata', 'archiviata' ]. [`☆ RA 54`](#RA54)

<a name="vincoli-task"></a>
<a name="V22"></a>
* [22. Task](#vincoli-task) __[⚒](#task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V22.1 ♕`](#V22.1) : Task( idJob ) -> Job( idJob ). [`☆ RA 26`](#RA26)
    * [`D22.2 ⚡`](#D22.2) : Task( statoPubblicazione ) -> [ 'attiva', 'disabilitata', 'archiviata' ]. [`☆ RA 55`](#RA55)

<a name="vincoli-sequenza-predefinita-azioni-job"></a>
<a name="V23"></a>
* [23. SequenzaPredefinitaAzioniJob](#vincoli-sequenza-predefinita-azioni-job) __[⚒](#sequenza-predefinita-azioni-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V23.1 ♕`](#V23.1) : SequenzaPredefinitaAzioniJob( idJob ) -> Job( idJob ). [`☆ RA 27`](#RA27)

<a name="vincoli-sequenza-richiesta-azioni-job"></a>
<a name="V24"></a>
* [24. SequenzaRichiestaAzioniTask](#vincoli-sequenza-richiesta-azioni-task) __[⚒](#sequenza-richiesta-azioni-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V24.1 ♕`](#V24.1) : SequenzaRichiestaAzioniTask( idTask ) -> Task( idTask ). [`☆ RA 28`](#RA28)

<a name="vincoli-azione-predefinita-job"></a>
<a name="V25"></a>
* [25. AzionePredefinitaJob](#vincoli-azione-predefinita-job) __[⚒](#azione-predefinita-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V25.1 ♕`](#V25.1) : AzionePredefinitaJob( idSequenzaPredefinitaAzioniJob ) -> SequenzaPredefinitaAzioniJob( idSequenzaPredefinitaAzioniJob ). [`☆ RA 29`](#RA29)
    * [`D25.2 ⚡`](#D25.2) : AzionePredefinitaJob( tipoAzione ) -> [ 'foto', 'video', 'questionario' ]. [`☆ RA 56`](#RA56)

<a name="vincoli-azione-richiesta-task"></a>
<a name="V26"></a>
* [26. AzioneRichiestaTask](#vincoli-azione-richiesta-task) __[⚒](#azione-richiesta-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V26.1 ♕`](#V26.1) : AzioneRichiestaTask( idSequenzaRichiestaAzioniTask ) -> SequenzaRichiestaAzioniTask( idSequenzaRichiestaAzioniTask ). [`☆ RA 30`](#RA30)
    * [`D26.2 ⚡`](#D26.2) : AzioneRichiestaTask( tipoAzione ) -> [ 'foto', 'video', 'questionario' ]. [`☆ RA 57`](#RA57)

<a name="vincoli-immagine-ricevuta-task"></a>
<a name="V27"></a>
* [27. ImmagineRicevutaTask](#vincoli-immagine-ricevuta-task) __[⚒](#immagine-ricevuta-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V27.1 ♕`](#V27.1) : ImmagineRicevutaTask( idAzioneRichiestaTask ) -> AzioneRichiestaTask( idAzioneRichiestaTask ). [`☆ RA 31`](#RA31)

<a name="vincoli-filmato-ricevuto-task"></a>
<a name="V28"></a>
* [28. FilmatoRicevutoTask](#vincoli-filmato-ricevuto-task) __[⚒](#filmato-ricevuto-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V28.1 ♕`](#V28.1) : FilmatoRicevutoTask( idAzioneRichiestaTask ) -> AzioneRichiestaTask( idAzioneRichiestaTask ). [`☆ RA 32`](#RA32)

<a name="vincoli-immagine-esempio-azione-predefinita-job"></a>
<a name="V29"></a>
* [29. ImmagineEsempioAzionePredefinitaJob](#vincoli-immagine-esempio-azione-predefinita-job) __[⚒](#immagine-esempio-azione-predefinita-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V29.1 ♕`](#V29.1) : ImmagineEsempio( idAzionePredefinitaJob ) -> AzionePredefinitaJob( idAzionePredefinitaJob ). [`☆ RA 33`](#RA33)

<a name="vincoli-domanda-questionario-predefinito-job"></a>
<a name="V30"></a>
* [30. DomandaQuestionarioPredefinitoJob](#vincoli-domanda-questionario-predefinito-job) __[⚒](#domanda-questionario-predefinito-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V30.1 ♕`](#V30.1) : DomandaQuestionarioPredefinitoJob( idAzionePredefinitaJob ) -> AzionePredefinitaJob( idAzionePredefinitaJob ). [`☆ RA 34`](#RA34)
    * [`D30.2 ⚡`](#D30.2) : DomandaQuestionarioPredefinitoJob( tipoSelezioneRisposta ) -> [ 'multipla', 'singola' ]. [`☆ RA 58`](#RA58)

<a name="vincoli-opzione-risposta-questionario-predefinito-job"></a>
<a name="V31"></a>
* [31. OpzioneRispostaQuestionarioPredefinitoJob](#vincoli-opzione-risposta-questionario-predefinito-job) __[⚒](#opzione-risposta-questionario-predefinito-job) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V31.1 ♕`](#V31.1) : OpzioneRispostaQuestionarioPredefinitoJob( idDomandaQuestionarioPredefinitoJob ) -> DomandaQuestionarioPredefinitoJob( idDomandaQuestionarioPredefinitoJob ). [`☆ RA 35`](#RA35)
    * [`D31.2 ⚡`](#D31.2) : OpzioneRispostaQuestionarioPredefinitoJob( tipoRisposta ) -> [ 'libera', 'precompilata' ]. [`☆ RA 59`](#RA59)

<a name="vincoli-domanda-richiesta-questionario-task"></a>
<a name="V32"></a>
* [32. DomandaRichiestaQuestionarioTask](#vincoli-domanda-richiesta-questionario-task) __[⚒](#domanda-richiesta-questionario-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V32.1 ♕`](#V32.1) : DomandaRichiestaQuestionarioTask( idAzioneRichiestaTask ) -> AzioneRichiestaTask( idAzioneRichiestaTask ). [`☆ RA 36`](#RA36)
    * [`D32.2 ⚡`](#D32.2) : DomandaRichiestaQuestionarioTask( tipoSelezioneRisposta ) -> [ 'multipla', 'singola' ]. [`☆ RA 58`](#RA58)

<a name="vincoli-opzione-risposta-questionario-task"></a>
<a name="V33"></a>
* [33. OpzioneRispostaQuestionarioTask](#vincoli-opzione-risposta-questionario-task) __[⚒](#opzione-risposta-questionario-task) [✎](#diagramma-azioni-job-e-task) [☝](#indice)__
    * [`V33.1 ♕`](#V33.1) : OpzioneRispostaQuestionarioTask( idDomandaRichiestaQuestionarioTask ) -> DomandaRichiestaQuestionarioTask( idDomandaRichiestaQuestionarioTask ). [`☆ RA 37`](#RA37)
    * [`D33.2 ⚡`](#D33.2) : OpzioneRispostaQuestionarioTask( tipoRisposta ) -> [ 'libera', 'precompilata' ]. [`☆ RA 59`](#RA59)

<a name="vincoli-area-presidio-bee"></a>
<a name="V34"></a>
* [34. AreaPresidioBee](#vincoli-area-presidio-bee) __[⚒](#area-presidio-bee) [✎](#diagramma-area-presidio-bee) [☝](#indice)__
    * [`V34.1 ♕`](#V34.1) : AreaPresidioBee( idBee ) -> Bee( idBee ). [`☆ RA 38`](#RA38)
    * [`D34.2 ⚡`](#D34.2) : AreaPresidioBee( tipoPresidio ) -> [ 'predefinito', 'corrente' ]. [`☆ RA 60`](#RA60)

<a name="vincoli-luogo-task"></a>
<a name="V35"></a>
* [35. LuogoTask](#vincoli-luogo-task) __[⚒](#luogo-task) [✎](#diagramma-area-presidio-bee) [☝](#indice)__
    * [`V35.1 ♕`](#V35.1) : LuogoTask( idTask ) -> Task( idTask ). [`☆ RA 39`](#RA39)
    * [`V35.2 ⚠`](#V35.2) : unique( LuogoTask( idTask ) ). [`☆ RA 39`](#RA39)

<a name="vincoli-svolgimento-sequenza-azioni-task"></a>
<a name="V36"></a>
* [36. SvolgimentoSequenzaAzioniTask](#vincoli-svolgimento-sequenza-azioni-task) __[⚒](#svolgimento-sequenza-azioni-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__
    * [`V36.1 ♕`](#V36.1) : SvolgimentoSequenzaAzioniTask( idAssegnazioneTask ) -> AssegnazioneTask( idAssegnazioneTask ). [`☆`](#)
    * [`V36.2 ♕`](#V36.2) : SvolgimentoSequenzaAzioniTask( idSequenzaRichiestaAzioniTask ) -> SequenzaRichiestaAzioniTask( ididSequenzaRichiestaAzioniTask ). [`☆ TODO`](#)
    * [`V36.3 ⚛`](#V36.3) : unique( SvolgimentoSequenzaAzioniTask( idAssegnazioneTask ), SvolgimentoSequenzaAzioniTask( idSequenzaRichiestaAzioniTask ) ). [`☆ TODO`](#)

<a name="vincoli-azione-svolta-task"></a>
<a name="V37"></a>
* [37. AzioneSvoltaTask](#vincoli-azione-svolta-task) __[⚒](#azione-svolta-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__
    * [`V37.1 ♕`](#V37.1) : AzioneSvoltaTask( idSvolgimentoSequenzaAzioniTask ) -> SvolgimentoSequenzaAzioniTask( idSvolgimentoSequenzaAzioniTask ). [`☆ TODO`](#)
    * [`V37.2 ♕`](#V37.2) : AzioneSvoltaTask( idAzioneRichiestaTask ) -> AzioneRichiestaTask( idAzioneRichiestaTask ). [`☆ TODO`](#)

<a name="vincoli-questionario-svolto-task"></a>
<a name="V38"></a>
* [38. QuestionarioSvoltoTask](#vincoli-questionario-svolto-task) __[⚒](#questionario-svolto-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__
    * [`V38.1 ♕`](#V38.1) : QuestionarioSvoltoTask( idAzioneSvoltaTask ) -> AzioneSvoltaTask( idAzioneSvoltaTask ). [`☆ TODO`](#)

<a name="vincoli-risposta-ricevuta-questionario-task"></a>
<a name="V39"></a>
* [39. RispostaRicevutaQuestionarioTask](#vincoli-risposta-ricevuta-questionario-task) __[⚒](#risposta-ricevuta-questionario-task) [✎](#diagramma-svolgimento-task) [☝](#indice)__
    * [`V39.1 ♕`](#V39.1) : RispostaRicevutaQuestionarioTask( idQuestionarioSvoltoTask ) -> QuestionarioSvoltoTask( idQuestionarioSvoltoTask ). [`☆ TODO`](#)
    * [`V39.2 ♕`](#V39.2) : RispostaRicevutaQuestionarioTask( idDomandaRichiestaQuestionarioTask ) -> DomandaRichiestaQuestionarioTask( idDomandaRichiestaQuestionarioTask ). [`☆ TODO`](#)
    * [`V39.3 ♕`](#V39.3) : RispostaRicevutaQuestionarioTask( idOpzioneRispostaQuestionarioTask ) -> OpzioneRispostaQuestionarioTask( idOpzioneRispostaQuestionarioTask ). [`☆ TODO`](#)

--------------------------------------------------------------------------------

<a name="diagrammi-er"></a>
###Diagrammi E-R ✎

<a name="diagramma-legenda-rappresentazioni"></a>
####[Legenda Rappresentazioni](#diagramma-legenda-rappresentazioni) [☝](#indice)

![legenda rappresentazioni](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/legenda_rappresentazioni.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-credenziali-utente"></a>
####[Credenziali Utente](#iagramma-credenziali-utente") [☝](#indice)

> __Tags__ : [__`AnagraficaBee ⚒`__](#anagrafica-bee) [__`AnagraficaBeekeeper ⚒`__](#anagrafica-beekeeper) __[`CredenzialiAccessoUtente`](#credenziali-accesso-utente)__

![credenziali utente](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/credenziali_utente.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-relazioni-utente"></a>
####[Relazioni Utente](#diagramma-relazioni-utente) [☝](#indice)

> __Tags__ : [__`Bee ⚒`__](#bee) [__`Beekeeper ⚒`__](#beekeeper) [__`PreferitiBee ⚒`__](#preferiti-bee) [__`PreferitiBeekeeper ⚒`__](#preferiti-beekeeper)

![relazioni utente](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/relazioni_utente.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-documenti"></a>
####[Documenti](#diagramma-documenti) [☝](#indice)

> __Tags__ : [__`DocumentoFiscaleBee ⚒`__](#documento-fiscale-bee) [__`DocumentoFiscaleBeekeeper ⚒`__](#documento-fiscale-beekeeper) [__`ImmagineRicevutaTask ⚒`__](#immagine-ricevuta-task) [__`FilmatoRicevutoTask ⚒`__](#filmato-ricevuto-task)

![documenti](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/documenti.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-transazioni-utente"></a>
####[Transazioni Utente](#diagramma-transazioni-utente) [☝](#indice)

> __Tags__ : [__`PrelievoBee ⚒`__](#prelievo-bee) [__`VersamentoBeekeeper ⚒`__](#versamento-beekeeper) [__`DocumentoFiscaleBee ⚒`__](#documento-fiscale-bee) [__`DocumentoFiscaleBeekeeper ⚒`__](#documento-fiscale-beekeeper) [__`Bee ⚒`__](#bee) [__`Beekeeper ⚒`__](#beekeeper)

![transazioni utente](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/transazioni_utente.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-feedbacks"></a>
####[Feedbacks](#diagramma-feedbacks) [☝](#indice)

> __Tags__ : [__`FeedbackBeeToBeekeeper ⚒`__](#feedback-bee-to-beekeper) [__`FeedbackBeekeeperToBee ⚒`__](#feedback-beekeeper-to-bee) [__`NotificaBee ⚒`__](#notifica-bee) [__`NotificaBeekeeper ⚒`__](#notifica-beekeeper)

![feedbacks](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/feedbacks.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-messaggi-e-notifiche"></a>
####[Messaggi e Notifiche](#diagramma-messaggi-e-notifiche) [☝](#indice)

> __Tags__ : [__`ChatMessage ⚒`__](#chat-message) [__`ChatRoom ⚒`__](#chat-room) [__`NotificaBee ⚒`__](#notifica-bee) [__`NotificaBeekeeper ⚒`__](#notifica-beekeeper)

![messaggi](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/messaggi_e_notifiche.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-eventi"></a>
####[Eventi](#diagramma-eventi) [☝](#indice)

> __Tags__ : [__`FeedbackBeeToBeekeeper ⚒`__](#feedback-bee-to-beekeper) [__`FeedbackBeekeeperToBee ⚒`__](#feedback-beekeeper-to-bee) [__`Assegnazione ⚒`__](#assegnazione) [__`Accredito ⚒`__](#accredito) [__`NotificaBee ⚒`__](#notifica-bee) [__`NotificaBeekeeper ⚒`__](#notifica-beekeeper) [__`Bee ⚒`__](#bee) [__`Beekeeper ⚒`__](#beekeeper)

![eventi](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/eventi.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-assegnazioni-e-candidature-task"></a>
####[Assegnazioni e Candidature Task](#diagramma-assegnazioni-e-candidature-task) [☝](#indice)

> __Tags__ : [__`AssegnazioneTask ⚒`__](#assegnazione-task) [__`Job ⚒`__](#job) [__`Task ⚒`__](#task) [__`FeedbackBeeToBeekeeper ⚒`__](#feedback-bee-to-beekeeper) [__`FeedbackBeekeeperToBee ⚒`__](#feedback-beekeeper-to-bee) [__`CandidaturaTask ⚒`__](#candidature-task) [__`Accredito ⚒`__](#accredito) [__`ChatMessage ⚒`__](#chat-message) [__`ChatRoom ⚒`__](#chat-room) [__`Bee ⚒`__](#bee) [__`Beekeeper ⚒`__](#beekeeper)

![Assegnazione e Candidature Task](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/assegnazioni_e_candidature_task.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-svolgimento-task"></a>
####[Svolgimento Task](#diagramma-svolgimento-task)  [☝](#indice)

> __Tags__ : [__`Job ⚒`__](#job) [__`Task ⚒`__](#task) [__`Beekeeper ⚒`__](#beekeeper) [__`LuogoTask ⚒`__](#luogo-task) [__`SequenzaPredefinitaAzioniJob ⚒`__](#sequenza-predefinita-azioni-job) [__`SequenzaRichiestaAzioniTask ⚒`__](#sequenza-richiesta-azioni-task) [__`AzionePredefinitaJob ⚒`__](#azione-predefinita-job) [__`AzioneRichiestaTask ⚒`__](#azione-richiesta-task) [__`AzioneSvoltaTask ⚒`__](#azione-svolta-task) [__`ImmagineRicevutaTask ⚒`__](#immagine-ricevuta-task) [__`FilmatoRicevutoTask ⚒`__](#filmato-ricevuto-ask) [__`DomandaQuestionarioPredefinitoJob ⚒`__](#domanda-questionario-predefinito-job) [__`OpzioneRispostaQuestionarioPredefinitoJob ⚒`__](#opzione-risposta-questionario-predefinito-job) [__`DomandaRichiestaQuestionarioTask ⚒`__](#somanda-richiesta-questionario-task) [__`OpzioneRispostaQuestionarioTask ⚒`__](#opzione-risposta-questionario-task) [__`SvolgimentoSequenzaAzioniTask ⚒`__](#svolgimento-sequenza-azioni-task) [__`QuestionarioSvoltoTask ⚒`__](#questionario-svolto-task) [__`RispostaRicevutaQuestionarioTask ⚒`__](#risposta-ricevuta-questionario-task)

![svolgimento task](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/svolgimento_task.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-attività-job-e-task"></a>
####[Attività Job e Task](#diagramma-attività-job-e-task) [☝](#indice)

> __Tags__ : [__`Job ⚒`__](#job) [__`Task ⚒`__](#task) [__`Beekeeper ⚒`__](#beekeeper) [__`LuogoTask ⚒`__](#luogo-task) [__`SequenzaPredefinitaAzioniJob ⚒`__](#sequenza-predefinita-azioni-job) [__`SequenzaRichiestaAzioniTask ⚒`__](#sequenza-richiesta-azioni-task) [__`AzionePredefinitaJob ⚒`__](#azione-predefinita-job) [__`AzioneRichiestaTask ⚒`__](#azione-richiesta-task)

![attività job e task](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/attivit_job_e_task.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-azioni-job-e-task"></a>
####[Azioni Job e Task](#diagramma-azioni-job-e-task) [☝](#indice)

> __Tags__ : [__`DomandaQuestionarioPredefinitoJob ⚒`__](#domanda-questionario-predefinito-job) [__`OpzioneRispostaQuestionarioPredefinitoJob ⚒`__](#opzione-risposta-questionario-predefinito-job) [__`DomandaRichiestaQuestionarioTask ⚒`__](#domanda-richiesta-questionario-task) [__`OpzioneRispostaQuestionarioTask ⚒`__](#opzione-risposta-questionario-task) [__`AzionePredefinitaJob ⚒`__](#azione-predefinita-job) [__`AzioneRichiestaTask ⚒`__](#azione-richiesta-task)

![azioni job e task](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/azioni_job_e_task.png?raw=true)

--------------------------------------------------------------------------------

<a name="diagramma-presidio-bee"></a>
####[Presidio Bee](#diagramma-presidio-bee) [☝](#indice)

> __Tags__ : [__`Bee ⚒`__](#bee) [__`AreaPresidioBee ⚒`__](#area-presidio-bee) [__`LuogoTask ⚒`__](#luogo-task)

![presidio bee](https://github.com/topcs/bateleur/blob/master/docs/DB/sketches/png/presidio_bee.png?raw=true)

--------------------------------------------------------------------------------