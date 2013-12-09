####Schema Concettuale DB
<a name="indice-tabelle"></a>
_[Torna all'indice generale](../Readme.md)_

* __[Indice Tabelle](#indice-tabelle)__
    * __[⚒](#utente) [☢](#V1)__ `T1. Utente`
    * __[⚒](#bee) [☢](#V2)__ `T2. Bee`
    * __[⚒](#beekeeper) [☢](#V3)__ `T3. Beekeeper`
    * __[⚒](#preferiti-bee) [☢](#V4)__ `T4. PreferitiBee`
    * __[⚒](#preferiti-beekeeper) [☢](#V5)__ `T5. PreferitiBeekeeper`
    * __[⚒](#prelievo-bee) [☢](#V6)__ `T6. PrelievoBee`
    * __[⚒](#documento-fiscale-bee) [☢](#V7)__ `T7. DocumentoFiscaleBee`
    * __[⚒](#prodotto) [☢](#V8)__ `T8. Prodotto`
    * __[⚒](#ordine-beekeeper) [☢](#V9)__ `T9. OrdineBeekeeper`
    * __[⚒](#storico-ordine-beekeeper) [☢](#V10)__ `T10. StoricoOrdineBeekeeper`
    * __[⚒](#stato-ordine-beekeeper) [☢](#V11)__ `T11. StatoOrdineBeekeeper`
    * __[⚒](#ScontoProdotto) [☢](#V12)__ `T12. ScontoProdotto`
    * __[⚒](#versamento-beekeeper) [☢](#V13)__ `T13. VersamentoBeekeeper`
    * __[⚒](#fattura-emessa) [☢](#V14)__ `T14. FatturaEmessa`
    * __[⚒](#job) [☢](#V15)__ `T15. Job`
    * __[⚒](#task) [☢](#V16)__ `T16. Task`
    * __[⚒](#luogo-task) [☢](#V17)__ `T17. LuogoTask`
    * __[⚒](#area-presidio-bee) [☢](#V18)__ `T18. AreaPresidioBee`
    * __[⚒](#chat-room-task) [☢](#V19)__ `T19. ChatRoomTask`
    * __[⚒](#messaggio-chat) [☢](#V20)__ `T20. MessaggioChat`
    * __[⚒](#notifica-utente) [☢](#V21)__ `T21. NotificaUtente`
    * __[⚒](#candidatura-task) [☢](#V22)__ `T22. CandidaturaTask`
    * __[⚒](#azione-predefinita-job) [☢](#V23)__ `T23. AzionePredefinitaJob`
    * __[⚒](#immagine-esempio-azione-predefinita-job) [☢](#V24)__ `T24. ImmagineEsempioAzionePredefinitaJob`
    * __[⚒](#domanda-questionario-predefinito-job) [☢](#V25)__ `T25. DomandaQuestionarioPredefinitoJob`
    * __[⚒](#opzione-risposta-questionario-predefinito-job) [☢](#V26)__ `T26. OpzioneRispostaQuestionarioPredefinitoJob`
    * __[⚒](#azione-richiesta-task) [☢](#V27)__ `T27. AzioneRichiestaTask`
    * __[⚒](#immagine-ricevuta-task) [☢](#V28)__ `T28. ImmagineRicevutaTask`
    * __[⚒](#filmato-ricevuto-task) [☢](#V29)__ `T29. FilmatoRicevutoTask`
    * __[⚒](#domanda-questionario-task) [☢](#V30)__ `T30. DomandaQuestionarioTask`
    * __[⚒](#opzione-risposta-questionario-task) [☢](#V31)__ `T31. OpzioneRispostaQuestionarioTask`
    * __[⚒](#storico-stato-task) [☢](#V32)__ `T32. StoricoStatoTask`
    * __[⚒](#stato-task) [☢](#V33)__ `T33 StatoTask`

<a name="indice-diagrammi"></a>
* __[Indice Diagrammi](#indice-diagrammi)__:
    * __[✎](#D1)__ `D1. Legenda Rappresentazioni`
    * __[✎](#D2)__ `D2. Credenziali Utente`
    * __[✎](#D3)__ `D3. Relazioni Utente`
    * __[✎](#D4)__ `D4. Assegnazioni e Candidature Task`
    * __[✎](#D5)__ `D5. Svolgimento Task`
    * __[✎](#D6)__ `D6. Azioni Job e Task`
    * __[✎](#D7)__ `D7. Presidio Bee`
    * __[✎](#D8)__ `D8. Transazioni Utente`
    * __[✎](#D9)__ `D9. Ordini e Sconti`
    * __[✎](#D10)__ `D10. Documenti`
    * __[✎](#D11)__ `D11. Messaggi e Notifiche`
    * __[✎](#D12)__ `D12. Feedbacks`
    * __[✎](#D13)__ `D13. Eventi`

<a name="legenda-simboli"></a>
* __[Legenda Simboli ♣](#legenda-simboli)__:
    * __[Links ⚓](#legenda-simboli)__:
        * __[⚒](#legenda-simboli)__ : _link alla tabella_
        * __[☢](#legenda-simboli)__ : _link ai vincoli di integrità_
        * __[✎](#legenda-simboli)__ : _link ai diagrammi_
        * __[☝](#legenda-simboli)__ : _link all'indice_
    * __[Vincoli Attributo ☢](#legenda-simboli)__:
        * __[♔](#legenda-simboli)__ : _vincolo di chiave primaria_
        * __[♕](#legenda-simboli)__ : _vincolo di chiave esterna_
        * __[♖](#legenda-simboli)__ : _vincolo di chiave esterna ridondante_
        * __[⚠](#legenda-simboli)__ : _vincolo unique su attributo singolo_
        * __[⚛](#legenda-simboli)__ : _vincolo unique su attributo multiplo_
        * __[✓](#legenda-simboli)__ : _vincolo di attributo obbligatorio_
        * __[⚡](#legenda-simboli)__ : _vincolo di dominio_
    * __[Regole Aziendali - Business Rules ☆](#legenda-simboli)__
        * __[vi](#)__ : `♔` `♕` `⚠` `⚛` _vincolo d'integrità referenziale_
        * __[vd](#)__ : `⚡` _vincolo di dominio_
        * __[vr](#)__ : ` ♖` _vincolo d'integrità referenziale ridondante / opzionale_
        * __[✍](#)__ : _descrizione_

--------------------------------------------------------------------------------

<a name="tabelle"></a>
####Tabelle ⚒

<a name="utente"></a>
####[T1. Utente](#utente) [☢](#V1) [☝](#indice-tabelle)

> `♔ referenced by` : [`T2. Bee`](#bee) [`T3. Beekeeper`](#beekeeper) [`T21. NotificaUtente`](#notifica-utente)
<br/>
> `✎ diagrams` : [`D2. CredenzialiUtente`](#D2) [`D3. RelazioniUtente`](#D3) [`D8. Transazioni Utente`](#D8)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idUtente__                      |  ♔  |     |      | _Number_ |                |  |
| 2   | username                          |     |  ✓  |  ⚠   | _String_ |                |  |
| 3   | email                             |     |  ✓  |  ⚠   | _Number_ |                |  |
| 4   | auth                              |     |  ✓  |      | _String_ |                |  |
| 5   | dataCreazione                     |     |  ✓  |      | _Date_   |                |  |
| 6   | statoUtenza                       |     |  ✓  |      | _String_ | __`attiva`<br/>`disabilitata`__ |  |
| 7   | statoVerificaCredenziali          |     |  ✓  |      | _String_ | __`pendente`<br/>`completata`__ |  |
| 8   | tipoUtente                        |     |  ✓  |      | _String_ | __`Bee`<br/>`Beekeeper`__ |  |
| 9   | dataUltimoAccesso                 |     |     |      | _Date_   |                |  |
| 10  | dataUltimaModifica                |     |     |      | _Date_   |                |  |
| 11  | twitterId                         |     |     |      | _String_ |                |  |
| 12  | facebookId                        |     |     |      | _String_ |                |  |
| 13  | linkedinId                        |     |     |      | _String_ |                |  |
| 14  | avatarURL                         |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="bee"></a>
####[T2. Bee](#bee) [☢](#V2) [☝](#indice-tabelle)

> `♔ referenced by` : [`T4. PreferitiBee`](#preferiti-bee) [`T5. PreferitiBeekeeper`](#preferiti-beekeeper) [`T6. PrelievoBee`](#prelievo-bee) [`T16.Task`](#task) [`T18.AreaPresidioBee`](#area-presidio-bee) [`T22. CandidaturaTask`](#candidatura-task)  [`T20. MessaggioChat`](#messaggio-chat)
<br/>
> `✎ diagrams` : [`D2. CredenzialiUtente`](#D2) [`D3. RelazioniUtente`](#D3) [`D4. Assegnazioni e Candidature Task`](#D4) [`D7. PresidioBee`](#D7) [`D8. Transazioni Utente`](#D8) [`D11. Messaggi e Notifiche`](#D11) [`D12. Feedbacks`](#D12)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idBee__                         |  ♔  |     |      | _Number_ |                |  |
| 2   | bankrollCrediti                   |     |  ✓  |      | _Number_ | __[`⚡ attributo calcolato`](#T2.2)__ |  |
| 3   | nome                              |     |  ✓  |      | _String_ |                |  |
| 4   | cognome                           |     |  ✓  |      | _String_ |                |  |
| 5   | codiceFiscale                     |     |  ✓  |  ⚠   | _String_ |                |  |
| 6   | ragioneSociale                    |     |  ✓  |      | _String_ |                |  |
| 7   | partitaIVA                        |     |  ✓  |  ⚠   | _String_ |                |  |
| 8   | tipologiaFiscale                  |     |     |      | _String_ | __`privato`<br/>`libero professionista`<br/>`ditta individuale`<br/>`azienda`__ |  |
| 9   | fax                               |     |     |      | _String_ |                |  |
| 10  | cellulare                         |     |     |      | _String_ |                |  |
| 11  | telefono                          |     |     |      | _String_ |                |  |
| 12  | via                               |     |     |      | _String_ |                |  |
| 13  | civico                            |     |     |      | _String_ |                |  |
| 14  | codicePostale                     |     |     |      | _String_ |                |  |
| 15  | località                          |     |     |      | _String_ |                |  |
| 16  | comune                            |     |     |      | _String_ |                |  |
| 17  | provincia                         |     |     |      | _String_ |                |  |
| 18  | dataNascita                       |     |  ✓  |      |  _Date_  |                |  |
| 19  | sesso                             |     |  ✓  |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="beekeeper"></a>
####[T3. Beekeeper](#beekeeper) [☢](#V3) [☝](#indice-tabelle)

> `♔ referenced by` : [`T4. PreferitiBee`](#preferiti-bee) [`T5. PreferitiBeekeeper`](#preferiti-beekeeper) [`T9. OrdineBeekeeper`](#ordine-beekeeper) [`T15. Job`](#job) [`T20. MessaggioChat`](#messaggio-chat)
<br/>
> `✎ diagrams` : [`D2. CredenzialiUtente`](#D2) [`D3. RelazioniUtente`](#D3) [`D4. Assegnazioni e Candidature Task`](#D4) [`D8. Transazioni Utente`](#D8) [`D9. Ordini e Sconti`](#D9) [`D12. Feedbacks`](#D12)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idBeekeeper__                   |  ♔  |     |      | _Number_ |                |  |
| 2   | bankrollCrediti                   |     |  ✓  |      | _Number_ | __[`⚡ attributo calcolato`](#T3.2)__ |  |
| 3   | creditiDisponibili                |     |  ✓  |      | _Number_ | __[`⚡ attributo calcolato`](#T3.3)__ |  |
| 4   | nome                              |     |  ✓  |      | _String_ |                |  |
| 5   | cognome                           |     |  ✓  |      | _String_ |                |  |
| 6   | codiceFiscale                     |     |  ✓  |  ⚠   | _String_ |                |  |
| 7   | ragioneSociale                    |     |  ✓  |      | _String_ |                |  |
| 8   | partitaIVA                        |     |  ✓  |  ⚠   | _String_ |                |  |
| 9   | fax                               |     |     |      | _String_ |                |  |
| 10  | cellulare                         |     |     |      | _String_ |                |  |
| 11  | telefono                          |     |     |      | _String_ |                |  |
| 12  | via                               |     |     |      | _String_ |                |  |
| 13  | civico                            |     |     |      | _String_ |                |  |
| 14  | codicePostale                     |     |     |      | _String_ |                |  |
| 15  | località                          |     |     |      | _String_ |                |  |
| 16  | comune                            |     |     |      | _String_ |                |  |
| 17  | provincia                         |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="preferiti-bee"></a>
####[T4. PreferitiBee](#preferiti-bee) [☢](#V4) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D3. RelazioniUtente`](#D3) 

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __[`idBee`](#bee)__             |  ♔♕ |     |      | _Number_ |                |  |
| 2   | __[`idBeekeeper`](#beekeeper)__ |  ♔♕ |     |      | _Number_ |                |  |

--------------------------------------------------------------------------------

<a name="preferiti-beekeeper"></a>
####[T5. PreferitiBeekeeper](#preferiti-beekeeper) [☢](#V5) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D3. RelazioniUtente`](#D3) 

|  #  |          Attribute Name           | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __[`idBeekeeper`](##beekeeper)__  |  ♔♕ |     |      | _Number_ |                |  |
| 2   | __[`idBee`](#bee)__               |  ♔♕ |     |      | _Number_ |                |  |

--------------------------------------------------------------------------------

<a name="prelievo-bee"></a>
####[T6. PrelievoBee](#prelievo-bee) [☢](#V6) [☝](#indice-tabelle)

> `♔ referenced by` : [`T7. DocumentoFiscaleBee`](#documento-fiscale-bee)
<br/>
> `✎ diagrams` : [`D8. Transazioni Utente`](#D8)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idPrelievoBee__         |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idBee`](#bee)__       |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | codiceOperazione          |     |  ✓  |  ⚠   | _String_ |                |  |
| 4   | dataRichiesta             |     |  ✓  |      |  _Date_  |                |  |
| 5   | dataPrelievo              |     |     |      |  _Date_  |                |  |
| 6   | statoPrelievo             |     |  ✓  |      | _String_ | __`in elaborazione`<br/>`annullato`<br/>`completato`__ |  |
| 7   | importoValutaPrelevata    |     |  ✓  |      | _Number_ |                |  |
| 8   | importoCreditiCeduti      |     |  ✓  |      | _Number_ |                |  |

--------------------------------------------------------------------------------

<a name="documento-fiscale-bee"></a>
####[T7. DocumentoFiscaleBee](#documento-fiscale-bee) [☢](#V7) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D8. Transazioni Utente`](#D8) [`D10. Documenti`](#D10)

|  #  |            Attribute Name            | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|--------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idDocumentoFiscaleBee__            |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idPrelievoBee`](#prelievo-bee)__ |  ♕  |  ✓  |  ⚠   | _Number_ |                |  |
| 3   | numeroDocumento                      |     |  ✓  |      | _Number_ |                |  |
| 4   | tipoDocumento                        |     |  ✓  |      | _String_ | __`fattura`<br/>`ritenuta`__ |  |
| 5   | nomeFile                             |     |  ✓  |      | _String_ |                |  |
| 6   | URL                                  |     |  ✓  |      | _String_ |                |  |
| 7   | dataEmissione                        |     |  ✓  |      |  _Date_  |                |  |

--------------------------------------------------------------------------------

<a name="prodotto"></a>
####[T8. Prodotto](#prodotto) [☢](#V8) [☝](#indice-tabelle)

> `♔ referenced by` : [`T9. OrdineBeekeeper`](#ordine-beekeeper)
<br/>
> `✎ diagrams` : [`D8. Transazioni Utente`](#D8) [`D9. Ordini e Sconti`](#D9)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idProdotto__            |  ♔  |     |      | _Number_ |                |  |
| 2   | descrizione               |     |  ✓  |      | _String_ |                |  |
| 3   | dataCreazione             |     |  ✓  |      |  _Date_  |                |  |
| 4   | prezzo                    |     |  ✓  |      | _Number_ |                |  |
| 5   | crediti                   |     |  ✓  |      | _Number_ |                |  |
| 6   | tipoVersamentoRichiesto   |     |  ✓  |      | _String_ | __`pagamento online`<br/>`bonifico bancario`__ |  |

--------------------------------------------------------------------------------

<a name="ordine-beekeeper"></a>
####[T9. OrdineBeekeeper](#ordine-beekeeper) [☢](#V9) [☝](#indice-tabelle)

> `♔ referenced by` : [`T10. StoricoOrdineBeekeeper`](#storico-ordine-beekeeper) [`T13. VersamentoBeekeeper`](#versamento-beekeeper)
<br/>
> `✎ diagrams` : [`D8. Transazioni Utente`](#D8) [`D9. Ordini e Sconti`](#D9)

|  #  |              Attribute Name               | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idOrdineBeekeeper__                     |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idBeekeeper`](#beekeeper)__           |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | __[`idProdotto`](#prodotto)__             |  ♕  |  ✓  |      | _Number_ |                |  |
| 4   | __[`idScontoProdotto`](#ScontoProdotto)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 5   | codiceOrdine                              |     |  ✓  |      | _String_ |                |  |
| 6   | dataOrdine                                |     |  ✓  |      |  _Date_  |                |  |
| 7   | importoValutaOrdine                       |     |  ✓  |      | _Number_ | __[`⚡ attributo calcolato`](#T9.7)__ |  |
| 8   | statoCorrente                             |     |  ✓  |      | _String_ |                |  |
| 9   | dataStatoCorrente                         |     |  ✓  |      |  _Date_  |                |  |

--------------------------------------------------------------------------------

<a name="storico-ordine-beekeper"></a>
####[T10. StoricoOrdineBeekeeper](#storico-stato-ordine) [☢](#V10) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D9. Ordini e Sconti`](#D9)

|  #  |                     Attribute Name                      | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idStoricoOrdineBeekeeper__                            |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idOrdineBeekeeper`](#beekeeper)__                   |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | __[`idStatoOrdineBeekeeper`](#stato-ordine-beekeeper)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 4   | data                                                    |     |  ✓  |      |  _Date_  |                |  |

--------------------------------------------------------------------------------

<a name="stato-ordine-beekeeper"></a>
####[T11. StatoOrdineBeekeeper](#stato-ordine-beekeeper) [☢](#V11) [☝](#indice-tabelle)

> `♔ referenced by` : [`T10. StoricoOrdineBeekeeper`](#storico-ordine-beekeeper)
<br/>
> `✎ diagrams` : [`D9. Ordini e Sconti`](#D9)

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idStatoOrdineBeekeeper__   |  ♔  |     |      | _Number_ |                |  |
| 2   | statoOrdine                  |     |  ✓  |  ⚠   | _String_ | __`accettato`<br/>`pagato`<br/>`rifiutato`<br/>`annullato`__ |  |
| 3   | descrizioneStato             |     |  ✓  |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="ScontoProdotto"></a>
####[T12. ScontoProdotto](#ScontoProdotto) [☢](#V12) [☝](#indice-tabelle)

> `♔ referenced by` : [`T9. OrdineBeekeeper`](#ordine-beekeeper)
<br/>
> `✎ diagrams` : [`D8. Transazioni Utente`](#D8) [`D9. Ordini e Sconti`](#D9)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idScontoProdotto__      |  ♔  |     |      | _Number_ |                |  |
| 2   | codiceSconto              |     |  ✓  |  ⚠   | _String_ |                |  |
| 3   | percentualeSconto         |     |  ✓  |      | _Number_ |                |  |
| 4   | dataInserimento           |     |     |      |  _Date_  |                |  |
| 5   | dataScadenza              |     |     |      |  _Date_  |                |  |

--------------------------------------------------------------------------------

<a name="versamento-beekeeper"></a>
####[T13. VersamentoBeekeeper](#versamento-beekeeper) [☢](#V13) [☝](#indice-tabelle)

> `♔ referenced by` : [`T14. FatturaEmessa`](#fattura-emessa)
<br/>
> `✎ diagrams` : [`D8. Transazioni Utente`](#D8) [`D9. Ordini e Sconti`](#D9)

|  #  |                Attribute Name                | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|----------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idVersamentoBeekeeper__                    |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idOrdineBeekeeper`](#ordine-beekeeper)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | codiceOperazione                             |     |  ✓  |  ⚠   | _String_ |                |  |
| 4   | dataVersamento                               |     |  ✓  |      |  _Date_  |                |  |
| 5   | tipoVersamento                               |     |  ✓  |      | _String_ | __`pagamento online`<br/>`bonifico bancario`__ |  |
| 6   | importoValutaVersata                         |     |  ✓  |      | _Number_ |                |  |

--------------------------------------------------------------------------------

<a name="fattura-emessa"></a>
####[T14. FatturaEmessa](#fattura-emessa) [☢](#V14) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D8. Transazioni Utente`](#D8) [`D9. Ordini e Sconti`](#D9) [`D10. Documenti`](#D10)

|  #  |                   Attribute Name                     | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idFatturaEmessa__                                  |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idVersamentoBeekeeper`](#versamento-beekeeper)__ |  ♕  |     |      | _Number_ |                |  |
| 2   | nomeFile                                             |  ♕  |  ✓  |      | _String_ |                |  |
| 3   | URL                                                  |     |  ✓  |      | _String_ |                |  |
| 4   | numeroFattura                                        |     |  ✓  |      | _Number_ |                |  |
| 5   | dataEmissione                                        |     |  ✓  |      |  _Date_  |                |  |

--------------------------------------------------------------------------------

<a name="job"></a>
####[T15. Job](#job) [☢](#V15) [☝](#indice-tabelle)

> `♔ referenced by` : [`T16. Task`](#task) [`T23. AzionePredefinitaJob`](#azione-predefinita-job)
<br/>
> `✎ diagrams` : [`D4. Assegnazioni e Candidature Task`](#D4) [`D5. Svolgimento Task`](#D5)

|  #  |          Attribute Name         | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idJob__                       |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idBeekeeper`](#beekeeper)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | titoloJob                       |     |  ✓  |      | _String_ |                |  |
| 4   | descrizioneJob                  |     |  ✓  |      | _String_ |                |  |
| 5   | statoPubblicazione              |     |  ✓  |      | _String_ | __`attiva`<br/>`disabilitata`<br/>`archiviata`__ |  |
| 6   | dataCreazione                   |     |  ✓  |      |  _Date_  |                |  |
| 7   | dataPubblicazione               |     |     |      |  _Date_  |                |  |
| 8   | dataScadenzaPubblicazione       |     |     |      |  _Date_  |                |  |
| 9   | percentualeCompletamento        |     |     |      | _Number_ | __[`⚡ attributo calcolato`](#T15.9)__ |  |
| 10  | totaleCreditiInvestiti          |     |     |      | _Number_ | __[`⚡ attributo calcolato`](#T15.10)__ |  |

--------------------------------------------------------------------------------

<a name="task"></a>
####[T16. Task](#task) [☢](#V16) [☝](#indice-tabelle)

> `♔ referenced by` : [`T17. LuogoTask`](#luogo-task) [`T19. ChatRoomTask`](#chat-room-task) [`T22. CandidaturaTask`](#candidatura-task)
<br/>
> `✎ diagrams` : [`D4. Assegnazioni e Candidature Task`](#D4) [`D5. Svolgimento Task`](#D5) [`D12. Feedbacks`](#feedbacks)

|  #  |     Attribute Name    | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|-----------------------|:---:|:---:|:----:|:----------:|:--------------:|:------:|
| 1   | __idTask__            |  ♔  |     |      |  _Number_  |                |  |
| 2   | __[`idJob`](#job)__   |  ♕  |  ✓  |      |  _Number_  |                |  |
| 3   | __[`idBee`](#bee)__   |  ♕  |  ✓  |      |  _Number_  |                |  |
| 4   | statoPubblicazione    |     |  ✓  |      |  _String_  | __`attiva`<br/>`disabilitata`<br/>`archiviata`__ |  |
| 5   | statoCorrenteTask     |     |  ✓  |      |  _String_  | __`disponibile`<br/>`assegnato`<br/>`scaduto`<br/>`approvato`<br/>`in revisione`__ |  |
| 6   | dataStatoCorrente     |     |  ✓  |      |   _Date_   |                |
| 7   | dataCreazione         |     |  ✓  |      |   _Date_   |                |  |
| 8   | dataPubblicazione     |     |     |      |   _Date_   |                |  |
| 9   | totaleCreditiOfferti  |     |     |      |  _Number_  | __[`⚡ attributo calcolato`](#T16.10)__ |  |
| 10  | totaleCreditiPattuiti |     |     |      |  _Number_  | __[`⚡ attributo calcolato`](#T16.11)__ |  |
| 11  | votoBee               |     |     |      |  _Number_  |                |  |
| 12  | votoBeekeeper         |     |     |      |  _Number_  |                |  |
| 13  | commentoBee           |     |     |      |  _String_  |                |  |
| 14  | commentoBeekeeper     |     |     |      |  _String_  |                |  |

--------------------------------------------------------------------------------

<a name="luogo-task"></a>
####[T17. LuogoTask](#luogo-task) [☢](#V17) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D7. PresidioBee`](#D7)

|  #  |     Attribute Name    | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idLuogoTask__       |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idTask`](#task)__ |  ♕  |  ✓  |  ⚠   | _Number_ |                |  |
| 3   | descrizione           |     |     |      | _String_ |                |  |
| 4   | timestamp             |     |  ✓  |      |  _Date_  |                |  |
| 5   | latitudine            |     |  ✓  |      | _String_ |                |  |
| 6   | longitudine           |     |  ✓  |      | _String_ |                |  |
| 7   | raggio                |     |     |      | _Number_ |                |  |
| 8   | comune                |     |  ✓  |      | _String_ |                |  |
| 9   | provincia             |     |  ✓  |      | _String_ |                |  |
| 10  | via                   |     |     |      | _String_ |                |  |
| 11  | codicePostale         |     |     |      | _String_ |                |  |
| 12  | località              |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="area-presidio-bee"></a>
####[T18. AreaPresidioBee](#area-presidio-bee) [☢](#V18) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D7. PresidioBee`](#D7)

|  #  |    Attribute Name     | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idAreaPresidioBee__ |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idBee`](#bee)__   |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | tipoPresidio          |     |  ✓  |      | _String_ | __`predefinito`<br/>`corrente`__ |  |
| 4   | descrizione           |     |     |      | _String_ |                |  |
| 5   | timestamp             |     |  ✓  |      |  _Date_  |                |  |
| 6   | latitudine            |     |  ✓  |      | _String_ |                |  |
| 7   | longitudine           |     |  ✓  |      | _String_ |                |  |
| 8   | raggio                |     |     |      | _Number_ |                |  |
| 9   | comune                |     |  ✓  |      | _String_ |                |  |
| 10  | provincia             |     |  ✓  |      | _String_ |                |  |
| 11  | via                   |     |     |      | _String_ |                |  |
| 12  | codicePostale         |     |     |      | _String_ |                |  |
| 13  | località              |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="chat-room-task"></a>
####[T19. ChatRoomTask](#chat-room-task) [☢](#V19) [☝](#indice-tabelle)

> `♔ referenced by` : [`T20. MessaggioChat`](#messaggio-chat)
<br/>
> `✎ diagrams` : [`D4. Assegnazioni e Candidature Task`](#D4) [`D11. Messaggi e Notifiche`](#D11)

|  #  |     Attribute Name     | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idChatRoomTask__     |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idTask`](#task)__  |  ♕  |  ✓  |  ⚠   | _Number_ |                |  |
| 3   | statoChatRoom          |     |  ✓  |      | _String_ | __`attiva`<br/>`archiviata`__ |  |
| 4   | titolo                 |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="messaggio-chat"></a>
####[T20. MessaggioChat](#messaggio-chat) [☢](#V20) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D4. Assegnazioni e Candidature Task`](#D4) [`D11. Messaggi e Notifiche`](#D11)

|  #  |             Attribute Name              | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-----------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idMessaggioChat__                     |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idChatRoomTask`](#chat-room-task)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | _[`idBee`](#bee)_                       |  ♖  |  ✓  |      | _Number_ |                |  |
| 4   | _[`idBeekeeper`](#beekeeper)_           |  ♖  |  ✓  |      | _Number_ |                |  |
| 5   | tipoMittente                            |     |  ✓  |      | _String_ | __`Bee`<br/>`Beekeeper`__ |  |
| 6   | timestamp                               |     |  ✓  |      |  _Date_  |                |  |
| 7   | body                                    |     |  ✓  |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="notifica-utente"></a>
####[T21. NotificaUtente](#notifica-utente) [☢](#V21) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D11. Messaggi e Notifiche`](#D11) [`D12. Feedbacks`](#feedbacks)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idNotificaUtente__      |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idUtente`](#utente)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | timestamp                 |     |  ✓  |      |  _Date_  |                |  |
| 4   | oggetto                   |     |  ✓  |      | _String_ | __`Feedback Bee a Beekeeper`<br/>`Feedback Beekeeper a Bee`<br/>`Accredito Task`<br/>`Invito Task`<br/>`Assegnazione Task`<br/>`Candidatura Task`<br/>`Messaggio Chat`__ |  |
| 5   | URL                       |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="candidatura-task"></a>
####[T22. CandidaturaTask](#candidatura-task) [☢](#V22) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D4. Assegnazioni e Candidature Task`](#D4)

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idCandidaturaTask__           |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idTask`](#task)__           |  ♕  |  ✓  |  ⚛   | _Number_ |                |  |
| 3   | __[`idBee`](#bee)__             |  ♕  |  ✓  |  ⚛   | _Number_ |                |  |
| 4   | statoCandidatura                |     |  ✓  |      | _String_ |  __`pendente`<br/>`accettata`<br/>`rifiutata`<br/>`declinataBee`__ |  |
| 5   | tipoCandidatura                 |     |  ✓  |      | _String_ | __`invito`<br/>`spontanea`__ |  |
| 6   | dataCandidatura                 |     |  ✓  |      |  _Date_  |                |  |
| 7   | offertaCreditiBee               |     |  ✓  |      | _Number_ |                |  |
| 8   | codiceInvito                    |     |     |      | _String_ |                |  |
| 9   | dataInvito                      |     |     |      |  _Date_  |                |  |

--------------------------------------------------------------------------------

<a name="azione-predefinita-job"></a>
####[T23. AzionePredefinitaJob](#azione-predefinita-job) [☢](#V24) [☝](#indice-tabelle)

> `♔ referenced by` : [`T24. ImmagineEsempioAzionePredefinitaJob`](#immagine-esempio-azione-predefinita-job) [`T25. DomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job)
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6)

|  #  |            Attribute Name             | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idAzionePredefinitaJob__            |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idJob`](#job)__                   |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | titolo                                |     |  ✓  |      | _Number_ |                |  |
| 4   | descrizione                           |     |  ✓  |      | _String_ |                |  |
| 5   | tipoAzione                            |     |  ✓  |      | _String_ | __`foto`<br/>`video`<br/>`questionario`__ |  |
| 6   | creditiOfferti                        |     |  ✓  |      | _Number_ |                |  |

--------------------------------------------------------------------------------

<a name="immagine-esempio-azione-predefinita-job"></a>
####[T24. ImmagineEsempioAzionePredefinitaJob](#immagine-esempio-azione-predefinita-job) [☢](#V25) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D6. Azioni Job e Task`](#D6) [`D10. Documenti`](#D10)

|  #  |                       Attribute Name                    | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idImmagineEsempioAzionePredefinitaJob__               |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idAzionePredefinitaJob`](#azione-predefinita-job)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 4   | dataInserimento                                         |     |  ✓  |      |  _Date_  |                |  |
| 3   | nomeFile                                                |     |  ✓  |      | _String_ |                |  |
| 5   | URL                                                     |     |  ✓  |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="domanda-questionario-predefinito-job"></a>
####[T25. DomandaQuestionarioPredefinitoJob](#domanda-questionario-predefinito-job) [☢](#V26) [☝](#indice-tabelle)

> `♔ referenced by` : [`T26. OpzioneRispostaQuestionarioPredefinitoJob`](#opzione-risposta-questionario-predefinito-job)
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6)

|  #  |                       Attribute Name                    | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idDomandaQuestionarioPredefinitoJob__                 |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idAzionePredefinitaJob`](#azione-predefinita-job)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | indiceDomanda                                           |     |  ✓  |      | _Number_ |                |  |
| 4   | testoDomanda                                            |     |  ✓  |      | _String_ |                |  |
| 5   | tipoSelezioneRisposta                                   |     |  ✓  |      | _String_ | __`multipla`<br/> `singola`__ |  |

--------------------------------------------------------------------------------

<a name="opzione-risposta-questionario-predefinito-job"></a>
####[T26. OpzioneRispostaQuestionarioPredefinitoJob](#opzione-risposta-questionario-predefinito-job) [☢](#V27) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6)

|  #  |                                   Attribute Name                                   | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|------------------------------------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idOpzioneRispostaQuestionarioPredefinitoJob__                                    |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idDomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | indiceRisposta                                                                     |     |  ✓  |      | _Number_ |                |  |
| 4   | tipoRisposta                                                                       |     |  ✓  |      | _String_ | __`libera`<br/>`precompilata`__ |  |
| 5   | testoRisposta                                                                      |     |     |      | _String_ |                 |  |

--------------------------------------------------------------------------------

<a name="azione-richiesta-task"></a>
####[T27. AzioneRichiestaTask](#azione-richiesta-task) [☢](#V28) [☝](#indice-tabelle)

> `♔ referenced by` : [`T28. ImmagineRicevutaTask`](#immagine-ricevuta-task) [`T30. FilmatoRicevutoTask`](#filmato-ricevuto-task)
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6)

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idAzioneRichiestaTask__       |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idTask`](#task)__           |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | titolo                          |     |  ✓  |      | _String_ |                |  |
| 4   | descrizione                     |     |  ✓  |      | _String_ |                |  |
| 5   | tipoAzione                      |     |  ✓  |      | _String_ | __`foto`<br/>`video`<br/>`questionario`__ |  |
| 6   | creditiOfferti                  |     |  ✓  |      | _Number_ |                |  |

--------------------------------------------------------------------------------

<a name="immagine-ricevuta-task"></a>
####[T28. ImmagineRicevutaTask](#immagine-ricevuta-task) [☢](#V29) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6) [`D10. Documenti`](#D10)

|  #  |                     Attribute Name                     | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|--------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idImmagineRicevutaTask__                             |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idAzioneRichiestaTask`](#azione-richiesta-task)__  |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | nomeFile                                               |     |  ✓  |      | _String_ |                |  |
| 4   | URL                                                    |     |  ✓  |      | _String_ |                |  |
| 5   | dataInvio                                              |     |  ✓  |      |  _Date_  |                |  |
| 6   | latitudine                                             |     |     |      | _String_ |                |  |
| 7   | longitudine                                            |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="filmato-ricevuto-task"></a>
####[T30. FilmatoRicevutoTask](#filmato-ricevuto-task) [☢](#V30) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6) [`D10. Documenti`](#D10)

|  #  |                      Attribute Name                    | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|--------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idFilmatoRicevutoTask__                              |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idAzioneRichiestaTask`](#azione-richiesta-task)__  |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | nomeFile                                               |     |  ✓  |      | _String_ |                |  |
| 4   | URL                                                    |     |  ✓  |      | _String_ |                |  |
| 5   | dataInvio                                              |     |  ✓  |      |  _Date_  |                |  |
| 6   | latitudine                                             |     |     |      | _String_ |                |  |
| 7   | longitudine                                            |     |     |      | _String_ |                |  |

--------------------------------------------------------------------------------

<a name="domanda-questionario-task"></a>
####[T30. DomandaQuestionarioTask](#domanda-questionario-task) [☢](#V31) [☝](#indice-tabelle)

> `♔ referenced by` : [`T31. OpzioneRispostaQuestionarioTask`](#opzione-risposta-questionario-task)
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6)

|  #  |                      Attribute Name                   | Key | Req | Uniq |   Type   |     Domain     |   BR   |
|:---:|-------------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|:------:|
| 1   | __idDomandaQuestionarioTask__                         |  ♔  |     |      | _Number_ |                |  |
| 2   | __[`idAzioneRichiestaTask`](#azione-richiesta-task)__ |  ♕  |  ✓  |      | _Number_ |                |  |
| 3   | indiceDomanda                                         |     |  ✓  |      | _Number_ |                |  |
| 4   | testoDomanda                                          |     |  ✓  |      | _String_ |                |  |
| 5   | tipoSelezioneRisposta                                 |     |  ✓  |      | _String_ |  __`multipla`<br/> `singola`__ |  |

--------------------------------------------------------------------------------

<a name="opzione-risposta-questionario-task"></a>
####[T31. OpzioneRispostaQuestionarioTask](#opzione-risposta-questionario-task) [☢](#V32) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D5. Svolgimento Task`](#D5) [`D6. Azioni Job e Task`](#D6)

|  #  |                       Attribute Name                          | Key | Req | Uniq |    Type    |     Domain     |   BR   |
|:---:|---------------------------------------------------------------|:---:|:---:|:----:|:----------:|:--------------:|:------:|
| 1   | __idOpzioneRispostaQuestionarioTask__                         |  ♔  |     |      |  _Number_  |                |  |
| 2   | __[`idDomandaQuestionarioTask`](#domanda-questionario-task)__ |  ♕  |  ✓  |      |  _Number_  |                |  |
| 3   | indiceRisposta                                                |     |  ✓  |      |  _Number_  |                |  |
| 4   | tipoRisposta                                                  |     |  ✓  |      |  _String_  | __`libera`<br/>`precompilata`__ |  |
| 5   | selezionata                                                   |     |  ✓  |      |  _Boolean_ | __`true`<br/>`false`__ |  |
| 6   | dataInvio                                                     |     |  ✓  |      |  _Date_    |                |  |
| 7   | testoRisposta                                                 |     |     |      |  _String_  |                |  |
| 8   | latitudine                                                    |     |     |      |  _String_  |                |  |
| 9   | longitudine                                                   |     |     |      |  _String_  |                |  |

--------------------------------------------------------------------------------

<a name="storico-stato-task"></a>
####[T32. StoricoStatoTask](#storico-stato-task) [☝](#indice-tabelle)

> `♔ referenced by` : ✗
<br/>
> `✎ diagrams` : [`D4. Assegnazioni e Candidature Task`](#D4)

|  #  |          Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __[`idTask`](#task)__            |  ♔♕ |     |      | _Number_ |                |
| 2   | __[`idStatoTask`](#stato-task)__ |  ♔♕ |     |      | _Number_ |                |
| 3   | data                             |     |     |      |  _Date_  |                |

-----------------------------------------------------------------------------------------

<a name="stato-task"></a>
####[T33. StatoTask](#stato-task) [☝](#indice-tabelle)

> `♔ referenced by` : [`T32. StoricoStatoTask`](#storico-stato-task)
<br/>
> `✎ diagrams` : [`D4. Assegnazioni e Candidature Task`](#D4)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idStatoTask__                   |  ♔  |     |      | _Number_ |                |
| 2   | stato                             |     |     |      | _String_ | __`disponibile`<br/>`assegnato`<br/>`scaduto`<br/>`approvato`<br/>`in revisione`__ |
| 3   | descrizione                       |     |     |      | _String_ |                |

------------------------------------------------------------------------------------------

<a name="diagrammi-er"></a>
####Diagrammi E-R ✎

<a name="D1"></a>
####[D1. Legenda Rappresentazioni](#legenda-rappresentazioni) __[☝](#indice-diagrammi)__

> `⚒ tables` : ✗

![legenda rappresentazioni](../sketches/png/legenda_rappresentazioni.png?raw=true)

--------------------------------------------------------------------------------

<a name="D2"></a>
####[D2. Credenziali Utente](#credenziali-utente) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T1. Utente`](#utente) [`T2. Bee`](#bee) [`T3. Beekeeper`](#beekeeper)

![credenziali utente](../sketches/png/credenziali_utente.png?raw=true)

--------------------------------------------------------------------------------

<a name="D3"></a>
####[D3. Relazioni Utente](#relazioni-utente) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T1. Utente`](#utente) [`T2. Bee`](#bee) [`T3. Beekeeper`](#beekeeper) [`T4. PreferitiBee`](#preferiti-bee) [`T5. PreferitiBeekeeper`](#preferiti-beekeeper)

![relazioni utente](../sketches/png/relazioni_utente.png?raw=true)

--------------------------------------------------------------------------------

<a name="D4"></a>
####[D4. Assegnazioni e Candidature Task](#assegnazioni-e-candidature-task) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T2. Bee`](#bee) [`T3. Beekeeper`](#beekeeper) [`T15. Job`](#job) [`T16. Task`](#task) [`T19. ChatRoomTask`](#chat-room-task) [`T19. CandidaturaTask`](#candidatura-task) [`T20. MessaggioChat`](#messaggio-chat) [`T32. StoricoStatoTask`](#storico-stato-task) [`T33. StatoTask`](#stato-task)

![assegnazioni e candidature task](../sketches/png/assegnazioni_e_candidature_task.png?raw=true)

--------------------------------------------------------------------------------

<a name="D5"></a>
####[D5. Svolgimento Task](#svolgimento-task) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T15. Job`](#job) [`T16. Task`](#task) [`T17. LuogoTask`](#luogo-task) [`T23. AzionePredefinitaJob`](#azione-predefinita-job) [`T25. DomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job) [`T26. OpzioneRispostaQuestionarioPredefinitoJob`](#opzione-risposta-questionario-predefinito-job)[`T27. AzioneRichiestaTask`](#azione-richiesta-task) [`T28. ImmagineRicevutaTask`](#immagine-ricevuta-task) [`T30. FilmatoRicevutoTask`](#filmato--ricevuta-task) [`T30. DomandaQuestionarioTask`](#domanda-questionario-task) [`T31. OpzioneRispostaQuestionarioTask`](#opzione-risposta-questionario-task)

![svolgimento task](../sketches/png/svolgimento_task.png?raw=true)

--------------------------------------------------------------------------------

<a name="D6"></a>
####[D6. Azioni Job e Task](#azioni-job-e-task) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T23. AzionePredefinitaJob`](#azione-predefinita-job) [`T24. ImmagineEsempioAzionePredefinitaJob`](#immagine-esempio-azione-predefinita-job) [`T25. DomandaQuestionarioPredefinitoJob`](#domanda-questionario-predefinito-job) [`T26. OpzioneRispostaQuestionarioPredefinitoJob`](#opzione-risposta-questionario-predefinito-job) [`T27. AzioneRichiestaTask`](#azione-richiesta-task) [`T28. ImmagineRicevutaTask`](#immagine-ricevuta-task) [`T30. FilmatoRicevutoTask`](#filmato-ricevuto-task) [`T30. DomandaQuestionarioTask`](#domanda-questionario-task) [`T31. OpzioneRispostaQuestionarioTask`](#opzione-risposta-questionario-task)

![azioni job e task](../sketches/png/azioni_job_e_task.png?raw=true)

--------------------------------------------------------------------------------

<a name="D7"></a>
####[D7. Presidio Bee](#presidio-bee) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T2. Bee`](#bee) [`T17. LuogoTask`](#luogo-task) [`T18. AreaPresidioBee`](#area-presidio-bee)

![presidio bee](../sketches/png/presidio_bee.png?raw=true)

--------------------------------------------------------------------------------

<a name="D8"></a>
####[D8. Transazioni Utente](#transazioni-utente) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T1. Utente`](#utente) [`T2. Bee`](#bee) [`T6. PrelievoBee`](#prelievo-bee) [`T3. Beekeeper`](#beekeeper) [`T7. DocumentoFiscaleBee`](#documento-fiscale-bee) [`T8. Prodotto`](#prodotto) [`T9. OrdineBeekeeper`](#ordine-beekeeper) [`T12. ScontoProdotto`](#ScontoProdotto) [`T13. VersamentoBeekeeper`](#versamento-beekeeper) [`T14. FatturaEmessa`](#fattura-emessa)

![transazioni utente](../sketches/png/transazioni_utente.png?raw=true)

--------------------------------------------------------------------------------

<a name="D9"></a>
####[D9. Ordini e Sconti](#ordini-e-sconti) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T3. Beekeeper`](#beekeeper) [`T8. Prodotto`](#prodotto) [`T9. OrdineBeekeeper`](#ordine-beekeeper) [`T10. StoricoOrdineBeekeeper`](#storico-ordine-beekeeper) [`T11. StatoOrdineBeekeeper`](#stato-ordine-beekeeper) [`T12. ScontoProdotto`](#ScontoProdotto) [`T13. VersamentoBeekeeper`](#versamento-beekeeper) [`T14. FatturaEmessa`](#fattura-emessa)

![ordini e sconti](../sketches/png/ordini_e_sconti.png?raw=true)

--------------------------------------------------------------------------------

<a name="D10"></a>
####[D10. Documenti](#documenti) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T7. DocumentoFiscaleBee`](#documento-fiscale-bee) [`T14. FatturaEmessa`](#fattura-emessa) [`T24. ImmagineEsempioAzionePredefinitaJob`](#immagine-esempio-azione-predefinita-job) [`T28. ImmagineRicevutaTask`](#immagine-ricevuta-task) [`T30. FilmatoRicevutoTask`](#filmato-ricevuto-task)

![documenti](../sketches/png/documenti.png?raw=true)

--------------------------------------------------------------------------------

<a name="D11"></a>
####[D11. Messaggi e Notifiche](#messaggi-e-notifiche) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T1. Utente`](#utente) [`T19. ChatRoomTask`](#chat-room-task) [`T20. MessaggioChat`](#messaggio-chat) [`T21. NotificaUtente`](#notifica-utente)

![messaggi](../sketches/png/messaggi_e_notifiche.png?raw=true)

--------------------------------------------------------------------------------

<a name="D12"></a>
####[D12. Feedbacks](#feedbacks) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T2. Bee`](#bee) [`T3. Beekeeper`](#beekeeper) [`T16. Task`](#task) [`T21. NotificaUtente`](#notifica-utente)

![feedbacks](../sketches/png/feedbacks.png?raw=true)

--------------------------------------------------------------------------------

<a name="D13"></a>
####[D13. Eventi](#eventi) __[☝](#indice-diagrammi)__

> `⚒ tables` : [`T1. Utente`](#utente) [`T2. Bee`](#bee) [`T3. Beekeeper`](#beekeeper) [`T16. Task`](#task) [`T19. CandidaturaTask`](#candidatura-task) [`T21. NotificaUtente`](#notifica-utente)

![eventi](../sketches/png/eventi.png?raw=true)

--------------------------------------------------------------------------------

<a name="vincoli"></a>
#### WIP - Vincoli ☢

<a name="V1"></a>
* __[1. Utente](#V1) [⚒](#Uuente) [☝](#indice-tabelle)__

<a name="V2"></a>
* __[2. Bee](#V2) [⚒](#bee) [☝](#indice-tabelle)__

<a name="V3"></a>
* __[3. Beekeeper](#V3) [⚒](#beekeeper) [☝](#indice-tabelle)__

<a name="V4"></a>
* __[4. PreferitiBee](#V4) [⚒](#preferiti-bee) [☝](#indice-tabelle)__

<a name="V5"></a>
* __[5. PreferitiBeekeeper](#V5) [⚒](#preferiti-beekeeper) [☝](#indice-tabelle)__

<a name="V6"></a>
* __[6. PrelievoBee](#V6) [⚒](#prelievo-bee) [☝](#indice-tabelle)__

<a name="V7"></a>
* __[7. DocumentoFiscaleBee](#V7) [⚒](#documento-fiscale-bee) [☝](#indice-tabelle)__

<a name="V8"></a>
* __[8. Prodotto](#V8) [⚒](#prodotto) [☝](#indice-tabelle)__

<a name="V9"></a>
* __[9. OrdineBeekeeper](#V9) [⚒](#ordine-beekeeper) [☝](#indice-tabelle)__

<a name="V10"></a>
* __[10. StoricoOrdineBeekeeper](#V10) [⚒](#storico-ordine-beekeeper) [☝](#indice-tabelle)__

<a name="V11"></a>
* __[11. StatoOrdineBeekeeper](#V11) [⚒](#stato-ordine-beekeeper) [☝](#indice-tabelle)__

<a name="V12"></a>
* __[12. ScontoProdotto](#V12) [⚒](#ScontoProdotto) [☝](#indice-tabelle)__

<a name="V13"></a>
* __[13. VersamentoBeekeeper](#V13) [⚒](#versamento-beekeeper) [☝](#indice-tabelle)__

<a name="V14"></a>
* __[14. FatturaEmessa](#V14) [⚒](#fattura-emessa) [☝](#indice-tabelle)__

<a name="V15"></a>
* __[15. Job](#V15) [⚒](#job) [☝](#indice-tabelle)__

<a name="V16"></a>
* __[16. Task](#V16) [⚒](#task) [☝](#indice-tabelle)__

<a name="V17"></a>
* __[17. LuogoTask](#V17) [⚒](#luogo-task) [☝](#indice-tabelle)__

<a name="V18"></a>
* __[18. AreaPresidioBee](#V18) [⚒](#area-presidio-bee) [☝](#indice-tabelle)__

<a name="V19"></a>
* __[19. ChatRoomTask](#V19) [⚒](#chat-room-task) [☝](#indice-tabelle)__

<a name="V20"></a>
* __[20. MessaggioChat](#V20) [⚒](#messaggio-chat) [☝](#indice-tabelle)__

<a name="V21"></a>
* __[21. NotificaUtente](#V21) [⚒](#notifica-utente) [☝](#indice-tabelle)__

<a name="V22"></a>
* __[22. CandidaturaTask](#V22) [⚒](#candidatura-task) [☝](#indice-tabelle)__

<a name="V23"></a>
* __[23. AzionePredefinitaJob](#V24) [⚒](#azione-predefinita-job) [☝](#indice-tabelle)__

<a name="V24"></a>
* __[24. ImmagineEsempioAzionePredefinitaJob](#V25) [⚒](#immagine-esempio-azione-predefinita-job) [☝](#indice-tabelle)__

<a name="V25"></a>
* __[25. DomandaQuestionarioPredefinitoJob](#V26) [⚒](#domanda-questionario-predefinito-job) [☝](#indice-tabelle)__

<a name="V26"></a>
* __[26. OpzioneRispostaQuestionarioPredefinitoJob](#V27) [⚒](#opzione-risposta-questionario-predefinito-job) [☝](#indice-tabelle)__

<a name="V27"></a>
* __[27. AzioneRichiestaTask](#V28) [⚒](#azione-richiesta-task) [☝](#indice-tabelle)__

<a name="V28"></a>
* __[28. ImmagineRicevutaTask](#V29) [⚒](#immagine-ricevuta-task) [☝](#indice-tabelle)__

<a name="V29"></a>
* __[29. FilmatoRicevutoTask](#V30) [⚒](#filmato-ricevuto-task) [☝](#indice-tabelle)__

<a name="V30"></a>
* __[30. DomandaQuestionarioTask](#V31) [⚒](#domanda-questionario-task) [☝](#indice-tabelle)__

<a name="V31"></a>
* __[31. OpzioneRispostaQuestionarioTask](#V32 [⚒](#opzione-risposta-questionario-task) [☝](#indice-tabelle)__

<a name="V32"></a>
* __[32. StoricoStatoTask](#V32) [⚒](#storico-stato-task) [☝](#indice-tabelle)__

<a name="V33"></a>
* __[33. StatoTask](#V33) [⚒](#stato-task) [☝](#indice-tabelle)__

--------------------------------------------------------------------------------