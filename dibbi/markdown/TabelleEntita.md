### Tabelle Entità

*[Torna all'indice generale](../Readme.md)*

<a name="legenda-simboli"></a>
* __[Legenda Simboli](#legenda-simboli-tabelle)__:
    * __[♔](#)__ : _vincolo di chiave primaria_
    * __[♕](#)__ : _vincolo di chiave esterna_
    * __[♖](#)__ : _vincolo di chiave esterna ridondante_
    * __[⚠](#)__ : _vincolo unique su singolo attributo_
    * __[⚛](#)__ : _vincolo unique su multipli attributi_
    * __[✓](#)__ : _attributo obbligatorio_
    * __[☝](#indice-tabelle)__ : _torna all'indice_

<a name="indice-tabelle"></a>
* __[Indice Tabelle](#indice-tabelle)__:
    * __[T1. Utente](#utente)__
    * __[T2. Bee](#bee)__
    * __[T3. Beekeeper](#beekeeper)__
    * __[T4. PreferitiBee](#preferiti-bee)__
    * __[T5. PreferitiBeekeeper](#preferiti-beekeeper)__
    * __[T6. PrelievoBee](#prelievo-bee)__
    * __[T7. DocumentoFiscaleBee](#documento-fiscale-bee)__
    * __[T8. Prodotto](#prodotto)__
    * __[T9. OrdineBeekeeper](#ordine-beekeeper)__
    * __[T10. StoricoOrdineBeekeeper](#storico-ordine-beekeeper)__
    * __[T11. StatoOrdineBeekeeper](#stato-ordine-beekeeper)__
    * __[T12. ScontoProdotto](#sconto-prodotto)__
    * __[T13. VersamentoBeekeeper](#versamento-beekeeper)__
    * __[T14. FatturaEmessa](#fattura-emessa)__
    * __[T15. Job](#job)__
    * __[T16. Task](#task)__
    * __[T17. LuogoTask](#luogo-task)__
    * __[T18. AreaPresidioBee](#area-presidio-bee)__
    * __[T19. ChatRoomTask](#chat-room-task)__
    * __[T20. MessaggioChat](#messaggio-chat)__
    * __[T21. NotificaUtente](#notifica-utente)__
    * __[T22. CandidaturaTask](#candidatura-task)__
    * __[T23. AzionePredefinitaJob](#azione-predefinita-job)__
    * __[T24. ImmagineEsempioAzionePredefinitaJob](#immagine-esempio-azione-predefinita-job)__
    * __[T25. DomandaQuestionarioPredefinitoJob](#domanda-questionario-predefinito-job)__
    * __[T26. OpzioneRispostaQuestionarioPredefinitoJob](#opzione-risposta-questionario-predefinito-job)__
    * __[T27. AzioneRichiestaTask](#azione-richiesta-task)__
    * __[T28. ImmagineRicevutaTask](#immagine-ricevuta-task)__
    * __[T29. FilmatoRicevutoTask](#filmato-ricevuto-task)__
    * __[T30. DomandaQuestionarioTask](#domanda-questionario-task)__
    * __[T31. OpzioneRispostaQuestionarioTask](#opzione-risposta-questionario-task)__
    * __[T32. StoricoStatoTask](#storico-stato-task)__
    * __[T33. StatoTask](#stato-task)__

--------------------------------------------------------------------------------

<a name="utente"></a>
###[T1. Utente](#utente) [☝](#indice-tabelle)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idUtente__                      |  ♔  |     |      | _Number_ |                |
| 2   | username                          |     |  ✓  |  ⚠   | _String_ |                |
| 3   | email                             |     |  ✓  |  ⚠   | _Number_ |                |
| 4   | auth                              |     |  ✓  |      | _String_ |                |
| 5   | dataCreazione                     |     |  ✓  |      | _Date_   |                |
| 6   | statoUtenza                       |     |  ✓  |      | _String_ |  __`attiva`<br/>`disabilitata`__  |
| 7   | statoVerificaCredenziali          |     |  ✓  |      | _String_ |  __`pendente`<br/>`completata`__  |
| 8   | tipoUtente                        |     |  ✓  |      | _String_ |  __`Bee`<br/>`Beekeeper`__  |
| 9   | dataUltimoAccesso                 |     |     |      | _Date_   |                |
| 10  | dataUltimaModifica                |     |     |      | _Date_   |                |
| 11  | twitterId                         |     |     |      | _String_ |                |
| 12  | facebookId                        |     |     |      | _String_ |                |
| 13  | linkedinId                        |     |     |      | _String_ |                |
| 14  | avatarURL                         |     |     |      | _String_ |                |

------------------------------------------------------------------------------------------

<a name="bee"></a>
###[T2. Bee](#bee) [☝](#indice-tabelle)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idBee__                         |  ♔  |     |      | _Number_ |                |
| 2   | bankrollCrediti                   |     |  ✓  |      | _Number_ | __`⚡ attributo calcolato`__ |
| 3   | nome                              |     |  ✓  |      | _String_ |                |
| 4   | cognome                           |     |  ✓  |      | _String_ |                |
| 5   | codiceFiscale                     |     |  ✓  |  ⚠   | _String_ |                |
| 6   | ragioneSociale                    |     |     |      | _String_ |                |  |
| 7   | partitaIVA                        |     |  ✓  |  ⚠   | _String_ |                |
| 8   | tipologiaFiscale                  |     |     |      | _String_ | __`privato`<br/>`libero professionista`<br/>`ditta individuale`__ |
| 9   | fax                               |     |     |      | _String_ |                |
| 10  | cellulare                         |     |     |      | _String_ |                |
| 11  | telefono                          |     |     |      | _String_ |                |
| 12  | via                               |     |     |      | _String_ |                |
| 13  | civico                            |     |     |      | _String_ |                |
| 14  | codicePostale                     |     |     |      | _String_ |                |
| 15  | località                          |     |     |      | _String_ |                |
| 16  | comune                            |     |     |      | _String_ |                |
| 17  | provincia                         |     |     |      | _String_ |                |
| 18  | dataNascita                       |     |  ✓  |      |  _Date_  |                |
| 19  | sesso                             |     |  ✓  |      | _String_ |                |

------------------------------------------------------------------------------------------

<a name="beekeeper"></a>
###[T3. Beekeeper](#beekeeper) [☝](#indice-tabelle)

|  #  |           Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idBeekeeper__                   |  ♔  |     |      | _Number_ |                |
| 2   | bankrollCrediti                   |     |  ✓  |      | _Number_ | __`⚡ attributo calcolato`__ |
| 3   | creditiDisponibili                |     |  ✓  |      | _Number_ | __`⚡ attributo calcolato`__ |
| 4   | nome                              |     |  ✓  |      | _String_ |                |
| 5   | cognome                           |     |  ✓  |      | _String_ |                |
| 6   | codiceFiscale                     |     |  ✓  |  ⚠   | _String_ |                |
| 7   | ragioneSociale                    |     |  ✓  |      | _String_ |                |
| 8   | partitaIVA                        |     |  ✓  |  ⚠   | _String_ |                |
| 9   | fax                               |     |     |      | _String_ |                |
| 10  | cellulare                         |     |     |      | _String_ |                |
| 11  | telefono                          |     |     |      | _String_ |                |
| 12  | via                               |     |     |      | _String_ |                |
| 13  | civico                            |     |     |      | _String_ |                |
| 14  | codicePostale                     |     |     |      | _String_ |                |
| 15  | località                          |     |     |      | _String_ |                |
| 16  | comune                            |     |     |      | _String_ |                |
| 17  | provincia                         |     |     |      | _String_ |                |

------------------------------------------------------------------------------------------

<a name="preferiti-bee"></a>
###[T4. PreferitiBee](#preferiti-bee) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __`idBee`__               |  ♔♕ |     |      | _Number_ |                |
| 2   | __`idBeekeeper`__         |  ♔♕ |     |      | _Number_ |                |

----------------------------------------------------------------------------------

<a name="preferiti-beekeeper"></a>
###[T5. PreferitiBeekeeper](#preferiti-beekeeper) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __`idBeekeeper`__         |  ♔♕ |     |      | _Number_ |                |
| 2   | __`idBee`__               |  ♔♕ |     |      | _Number_ |                |

----------------------------------------------------------------------------------

<a name="prelievo-bee"></a>
###[T6. PrelievoBee](#prelievo-bee) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idPrelievoBee__         |  ♔  |     |      | _Number_ |                |
| 2   | __`idBee`__               |  ♕  |  ✓  |      | _Number_ |                |
| 3   | codiceOperazione          |     |  ✓  |  ⚠   | _String_ |                |
| 4   | dataRichiesta             |     |  ✓  |      |  _Date_  |                |
| 5   | dataPrelievo              |     |     |      |  _Date_  |                |
| 6   | statoPrelievo             |     |  ✓  |      | _String_ | __`in elaborazione`<br/>`annullato`<br/>`completato`__ |
| 7   | importoValutaPrelevata    |     |  ✓  |      | _Number_ |                |
| 8   | importoCreditiCeduti      |     |  ✓  |      | _Number_ |                |

----------------------------------------------------------------------------------

<a name="documento-fiscale-bee"></a>
###[T7. DocumentoFiscaleBee](#documento-fiscale-bee) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idDocumentoFiscaleBee__ |  ♔  |     |      | _Number_ |                |
| 2   | __`idPrelievoBee`__       |  ♕  |  ✓  |  ⚠   | _Number_ |                |
| 3   | numeroDocumento           |     |  ✓  |      | _Number_ |                |
| 4   | tipoDocumento             |     |  ✓  |      | _String_ | __`fattura`<br/>`ritenuta`__ |
| 5   | nomeFile                  |     |  ✓  |      | _String_ |                |
| 6   | URL                       |     |  ✓  |      | _String_ |                |
| 7   | dataEmissione             |     |  ✓  |      |  _Date_  |                |

----------------------------------------------------------------------------------

<a name="prodotto"></a>
###[T8.Prodotto](#prodotto) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idProdotto__            |  ♔  |     |      | _Number_ |                |
| 2   | descrizione               |     |  ✓  |      | _String_ |                |
| 3   | dataCreazione             |     |  ✓  |      |  _Date_  |                |
| 4   | prezzo                    |     |  ✓  |      | _Number_ |                |
| 5   | crediti                   |     |  ✓  |      | _Number_ |                |
| 6   | tipoVersamentoRichiesto   |     |  ✓  |      | _String_ | __`pagamento online`<br/>`bonifico bancario`__ |

----------------------------------------------------------------------------------

<a name="ordine-beekeeper"></a>
###[T9. OrdineBeekeeper](#ordine-beekeeper) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idOrdineBeekeeper__     |  ♔  |     |      | _Number_ |                |
| 2   | __`idBeekeeper`__         |  ♕  |  ✓  |      | _Number_ |                |
| 3   | __`idProdotto`__          |  ♕  |  ✓  |      | _Number_ |                |
| 4   | __`idScontoProdotto`__    |  ♕  |  ✓  |      | _Number_ |                |
| 5   | codiceOrdine              |     |  ✓  |      | _String_ |                |
| 6   | dataOrdine                |     |  ✓  |      |  _Date_  |                |
| 7   | importoValutaOrdine       |     |  ✓  |      | _Number_ | __`⚡ attributo calcolato`__ |
| 8   | statoCorrente             |     |  ✓  |      | _String_ |                |
| 9   | dataStatoCorrente         |     |  ✓  |      |  _Date_  |                |

----------------------------------------------------------------------------------

<a name="storico-ordine-beekeeper"></a>
###[T10. StoricoOrdineBeekeeper](#storico-ordine-beekeeper) [☝](#indice-tabelle)

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idStoricoOrdineBeekeeper__ |  ♔  |     |      | _Number_ |                |
| 2   | __`idOrdineBeekeeper`__      |  ♕  |  ✓  |      | _Number_ |                |
| 3   | __`idStatoOrdineBeekeeper`__ |  ♕  |  ✓  |      | _Number_ |                |
| 4   | data                         |     |  ✓  |      |  _Date_  |                |

-------------------------------------------------------------------------------------

<a name="stato-ordine-beekeeper"></a>
###[T11. StatoOrdineBeekeeper](#stato-ordine-beekeeper) [☝](#indice-tabelle)

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idStatoOrdineBeekeeper__   |  ♔  |     |      | _Number_ |                |
| 2   | statoOrdine                  |     |  ✓  |  ⚠   | _String_ | __`accettato`<br/>`pagato`<br/>`rifiutato`<br/>`annullato`__ |
| 3   | descrizioneStato             |     |  ✓  |      | _String_ |                |

-------------------------------------------------------------------------------------

<a name="sconto-prodotto"></a>
###[T12. ScontoProdotto](#sconto-prodotto) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idScontoProdotto__       |  ♔  |     |      | _Number_ |                |
| 2   | codiceSconto              |     |  ✓  |  ⚠   | _String_ |                |
| 3   | percentualeSconto         |     |  ✓  |      | _Number_ |                |
| 4   | dataInserimento           |     |     |      |  _Date_  |                |
| 5   | dataScadenza              |     |     |      |  _Date_  |                |

----------------------------------------------------------------------------------

<a name="versamento-beekeeper"></a>
###[T13. VersamentoBeekeeper](#versamento-beekeeper) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idVersamentoBeekeeper__ |  ♔  |     |      | _Number_ |                |
| 2   | __`idOrdineBeekeeper`__   |  ♕  |  ✓  |      | _Number_ |                |
| 3   | codiceOperazione          |     |  ✓  |  ⚠   | _String_ |                |
| 4   | dataVersamento            |     |  ✓  |      |  _Date_  |                |
| 5   | tipoVersamento            |     |  ✓  |      | _String_ | __`pagamento online`<br/>`bonifico bancario`__ |
| 6   | importoValutaVersata      |     |  ✓  |      | _Number_ |                |

----------------------------------------------------------------------------------

<a name="fattura-emessa"></a>
###[T14. FatturaEmessa](#fattura-emessa) [☝](#indice-tabelle)

|  #  |       Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |
|:---:|-----------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idFatturaEmessa__         |  ♔  |     |      | _Number_ |                |
| 2   | __`idVersamentoBeekeeper`__ |  ♕  |     |      | _Number_ |                |
| 2   | nomeFile                    |  ♕  |  ✓  |      | _String_ |                |
| 3   | URL                         |     |  ✓  |      | _String_ |                |
| 4   | numeroFattura               |     |  ✓  |      | _Number_ |                |
| 5   | dataEmissione               |     |  ✓  |      |  _Date_  |                |

----------------------------------------------------------------------------------

<a name="job"></a>
###[T15. Job](#job) [☝](#indice-tabelle)

|  #  |       Attribute Name      | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idJob__                 |  ♔  |     |      | _Number_ |                |
| 2   | __`idBeekeeper`__         |  ♕  |  ✓  |      | _Number_ |                |
| 3   | titoloJob                 |     |  ✓  |      | _String_ |                |
| 4   | descrizioneJob            |     |  ✓  |      | _String_ |                |
| 5   | statoPubblicazione        |     |  ✓  |      | _String_ | __`attiva`<br/>`disabilitata`<br/>`archiviata`__ |
| 6   | dataCreazione             |     |  ✓  |      |  _Date_  |                |
| 7   | dataPubblicazione         |     |     |      |  _Date_  |                |
| 8   | dataScadenzaPubblicazione |     |     |      |  _Date_  |                |
| 9   | percentualeCompletamento  |     |     |      | _Number_ | __`⚡ attributo calcolato`__ |
| 10  | totaleCreditiInvestiti    |     |     |      | _Number_ | __`⚡ attributo calcolato`__ |

----------------------------------------------------------------------------------

<a name="task"></a>
###[T16. Task](#task) [☝](#indice-tabelle)

|  #  |     Attribute Name    | Key | Req | Uniq |    Type    |     Domain     |
|:---:|-----------------------|:---:|:---:|:----:|:----------:|:--------------:|
| 1   | __idTask__            |  ♔  |     |      |  _Number_  |                |
| 2   | __`idJob`__           |  ♕  |  ✓  |      |  _Number_  |                |
| 3   | __`idBee`__           |  ♕  |  ✓  |      |  _Number_  |                |
| 4   | statoPubblicazione    |     |  ✓  |      |  _String_  | __`attiva`<br/>`disabilitata`<br/>`archiviata`__ |
| 5   | statoCorrenteTask     |     |  ✓  |      |  _String_  | __`disponibile`<br/>`assegnato`<br/>`scaduto`<br/>`approvato`<br/>`in revisione`__ |  |
| 6   | dataStatoCorrente     |     |  ✓  |      |   _Date_   |                |
| 7   | dataCreazione         |     |  ✓  |      |   _Date_   |                |
| 8   | dataPubblicazione     |     |     |      |   _Date_   |                |
| 9   | totaleCreditiOfferti  |     |     |      |  _Number_  | __`⚡ attributo calcolato`__ |
| 10  | totaleCreditiPattuiti |     |     |      |  _Number_  | __`⚡ attributo calcolato`__ |
| 11  | votoBee               |     |     |      |  _Number_  |                |
| 12  | votoBeekeeper         |     |     |      |  _Number_  |                |
| 13  | commentoBee           |     |     |      |  _String_  |                |
| 14  | commentoBeekeeper     |     |     |      |  _String_  |                |

--------------------------------------------------------------------------------

<a name="luogo-task"></a>
###[T17. LuogoTask](#luogo-task) [☝](#indice-tabelle)

|  #  |  Attribute Name  | Key | Req | Uniq |   Type   |     Domain     |
|:---:|------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idLuogoTask__  |  ♔  |     |      | _Number_ |                |
| 2   | __`idTask`__     |  ♕  |  ✓  |  ⚠   | _Number_ |                |
| 3   | descrizione      |     |     |      | _String_ |                |
| 4   | timestamp        |     |  ✓  |      |  _Date_  |                |
| 5   | latitudine       |     |  ✓  |      | _String_ |                |
| 6   | longitudine      |     |  ✓  |      | _String_ |                |
| 7   | raggio           |     |     |      | _Number_ |                |
| 8   | comune           |     |  ✓  |      | _String_ |                |
| 9   | provincia        |     |  ✓  |      | _String_ |                |
| 10  | via              |     |     |      | _String_ |                |
| 11  | codicePostale    |     |     |      | _String_ |                |
| 12  | località         |     |     |      | _String_ |                |

-------------------------------------------------------------------------

<a name="area-presidio-bee"></a>
###[T18. AreaPresidioBee](#area-presidio-bee) [☝](#indice-tabelle)

|  #  |    Attribute Name     | Key | Req | Uniq |   Type   |     Domain     |
|:---:|-----------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idAreaPresidioBee__ |  ♔  |     |      | _Number_ |                |
| 2   | __`idBee`__           |  ♕  |  ✓  |      | _Number_ |                |
| 3   | tipoPresidio          |     |  ✓  |      | _String_ | __`predefinito`<br/>`corrente`__ |
| 4   | descrizione           |     |     |      | _String_ |                |
| 5   | timestamp             |     |  ✓  |      |  _Date_  |                |
| 6   | latitudine            |     |  ✓  |      | _String_ |                |
| 7   | longitudine           |     |  ✓  |      | _String_ |                |
| 8   | raggio                |     |     |      | _Number_ |                |
| 9   | comune                |     |  ✓  |      | _String_ |                |
| 10  | provincia             |     |  ✓  |      | _String_ |                |
| 11  | via                   |     |     |      | _String_ |                |
| 12  | codicePostale         |     |     |      | _String_ |                |
| 13  | località              |     |     |      | _String_ |                |

------------------------------------------------------------------------------

<a name="chat-room-task"></a>
###[T19. ChatRoomTask](#chat-room-task) [☝](#indice-tabelle)

|  #  |    Attribute Name    | Key | Req | Uniq |   Type   |     Domain     |
|:---:|----------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idChatRoomTask__   |  ♔  |     |      | _Number_ |                |
| 2   | __`idTask`__         |  ♕  |  ✓  |  ⚠   | _Number_ |                |
| 3   | statoChatRoom        |     |  ✓  |      | _String_ | __`attiva`<br/>`archiviata`__ |
| 4   | titolo               |     |     |      | _String_ |                |

----------------------------------------------------------------------------------------

<a name="messaggio-chat"></a>
###[T20. MessaggioChat](#messaggio-chat) [☝](#indice-tabelle)

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idMessaggioChat__             |  ♔  |     |      | _Number_ |                |
| 2   | __`idChatRoomTask`__            |  ♕  |  ✓  |      | _Number_ |                |
| 3   | _`idBee`_                       |  ♖  |  ✓  |      | _Number_ |                |
| 4   | _`idBeekeeper`_                 |  ♖  |  ✓  |      | _Number_ |                |
| 5   | tipoMittente                    |     |  ✓  |      | _String_ | __`Bee`<br/>`Beekeeper`__ |
| 6   | timestamp                       |     |  ✓  |      |  _Date_  |                |
| 7   | body                            |     |  ✓  |      | _String_ |                |

----------------------------------------------------------------------------------------

<a name="notifica-utente"></a>
###[T21. NotificaUtente](#notifica-utente) [☝](#indice-tabelle)

|  #  |      Attribute Name      | Key | Req | Uniq |   Type   |     Domain     |
|:---:|--------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idNotificaUtente__     |  ♔  |     |      | _Number_ |                |
| 2   | __`idUtente`__           |  ♕  |  ✓  |      | _Number_ |                |
| 3   | timestamp                |     |  ✓  |      |  _Date_  |                |
| 4   | oggetto                  |     |  ✓  |      | _String_ | __`Feedback Bee a Beekeeper`<br/>`Feedback Beekeeper a Bee`<br/>`Accredito Task`<br/>`Invito Task`<br/>`Assegnazione Task`<br/>`Candidatura Task`<br/>`Messaggio Chat`__ |
| 5   | URL                      |     |     |      | _String_ |                |

---------------------------------------------------------------------------------

<a name="candidatura-task"></a>
###[T22. CandidaturaTask](#candidatura-task) [☝](#indice-tabelle)

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idCandidaturaTask__           |  ♔  |     |      | _Number_ |                |
| 2   | __`idTask`__                    |  ♕  |  ✓  |  ⚛   | _Number_ |                |
| 3   | __`idBee`__                     |  ♕  |  ✓  |  ⚛   | _Number_ |                |
| 4   | statoCandidatura                |     |  ✓  |      | _String_ |  __`pendente`<br/>`accettata`<br/>`rifiutata`<br/>`declinatoBee`__ |
| 5   | tipoCandidatura                 |     |  ✓  |      | _String_ | __`invito`<br/>`spontanea`__ |
| 6   | dataCandidatura                 |     |  ✓  |      |  _Date_  |                |
| 7   | offertaCreditiBee               |     |  ✓  |      | _Number_ |                |
| 8   | codiceInvito                    |     |     |      | _String_ |                |
| 9   | dataInvito                      |     |     |      |  _Date_  |                |

----------------------------------------------------------------------------------------

<a name="azione-predefinita-job"></a>
###[T23. AzionePredefinitaJob](#azione-predefinita-job) [☝](#indice-tabelle)

|  #  |            Attribute Name             | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idAzionePredefinitaJob__            |  ♔  |     |      | _Number_ |                |
| 2   | __`idJob`__                           |  ♕  |  ✓  |      | _Number_ |                |
| 3   | titolo                                |     |  ✓  |      | _String_ |                |
| 4   | descrizione                           |     |  ✓  |      | _String_ |                |
| 5   | tipoAzione                            |     |  ✓  |      | _String_ | __`foto`<br/>`video`<br/>`questionario`__ |
| 6   | creditiOfferti                        |     |  ✓  |      | _Number_ |                |

----------------------------------------------------------------------------------------------

<a name="immagine-esempio-azione-predefinita-job"></a>
###[T24. ImmagineEsempioAzionePredefinitaJob](#immagine-esempio-azione-predefinita-job) [☝](#indice-tabelle)

|  #  |                  Attribute Name                | Key | Req | Uniq |   Type   |     Domain     |
|:---:|------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idImmagineEsempioAzionePredefinitaJob__      |  ♔  |     |      | _Number_ |                |
| 2   | __`idAzionePredefinitaJob`__                   |  ♕  |  ✓  |      | _Number_ |                |
| 4   | dataInserimento                                |     |  ✓  |      |  _Date_  |                |
| 3   | nomeFile                                       |     |  ✓  |      | _String_ |                |
| 5   | URL                                            |     |  ✓  |      | _String_ |                |

-------------------------------------------------------------------------------------------------------

<a name="domanda-questionario-predefinito-job"></a>
###[T25. DomandaQuestionarioPredefinitoJob](#domanda-questionario-predefinito-job) [☝](#indice-tabelle)

|  #  |              Attribute Name              | Key | Req | Uniq |   Type   |     Domain     |
|:---:|------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idDomandaQuestionarioPredefinitoJob__  |  ♔  |     |      | _Number_ |                |
| 2   | __`idAzionePredefinitaJob`__             |  ♕  |  ✓  |      | _Number_ |                |
| 3   | indiceDomanda                            |     |  ✓  |      | _Number_ |                |
| 4   | testoDomanda                             |     |  ✓  |      | _String_ |                |
| 5   | tipoSelezioneRisposta                    |     |  ✓  |      | _String_ |  __`multipla`<br/> `singola`__ |

-------------------------------------------------------------------------------------------------

<a name="opzione-risposta-questionario-predefinito-job"></a>
###[T26. OpzioneRispostaQuestionarioPredefinitoJob](#opzione-risposta-questionario-predefinito-job) [☝](#indice-tabelle)

|  #  |                   Attribute Name                 | Key | Req | Uniq |   Type   |     Domain     |
|:---:|--------------------------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idOpzioneRispostaQuestionarioPredefinitoJob__  |  ♔  |     |      | _Number_ |                |
| 2   | __`idDomandaQuestionarioPredefinitoJob`__        |  ♕  |  ✓  |      | _Number_ |                |
| 3   | indiceRisposta                                   |     |  ✓  |      | _Number_ |                |
| 4   | tipoRisposta                                     |     |  ✓  |      | _String_ | __`libera`<br/>`precompilata`__ |
| 5   | testoRisposta                                    |     |     |      | _String_ |                |

---------------------------------------------------------------------------------------------------------

<a name="azione-richiesta-task"></a>
###[T27. AzioneRichiestaTask](#azione-richiesta-task) [☝](#indice-tabelle)

|  #  |         Attribute Name          | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idAzioneRichiestaTask__       |  ♔  |     |      | _Number_ |                |
| 2   | __`idTask`__                    |  ♕  |  ✓  |      | _Number_ |                |
| 3   | titolo                          |     |  ✓  |      | _String_ |                |
| 4   | descrizione                     |     |  ✓  |      | _String_ |                |
| 5   | tipoAzione                      |     |  ✓  |      | _String_ | __`foto`<br/>`video`<br/>`questionario`__ |
| 6   | creditiOfferti                  |     |  ✓  |      | _Number_ |                |

----------------------------------------------------------------------------------------

<a name="immagine-ricevuta-task"></a>
###[T28. ImmagineRicevutaTask](#immagine-ricevuta-task) [☝](#indice-tabelle)

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idImmagineRicevutaTask__   |  ♔  |     |      | _Number_ |                |
| 2   | __`idAzioneRichiestaTask`__  |  ♕  |  ✓  |      | _Number_ |                |
| 3   | nomeFile                     |     |  ✓  |      | _String_ |                |
| 4   | URL                          |     |  ✓  |      | _String_ |                |
| 5   | dataInvio                    |     |  ✓  |      |  _Date_  |                |
| 6   | latitudine                   |     |     |      | _String_ |                |
| 7   | longitudine                  |     |     |      | _String_ |                |

-------------------------------------------------------------------------------------

<a name="filmato-ricevuto-task"></a>
###[T29. FilmatoRicevutoTask](#filmato-ricevuto-task) [☝](#indice-tabelle)

|  #  |        Attribute Name        | Key | Req | Uniq |   Type   |     Domain     |
|:---:|------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idFilmatoRicevutoTask__    |  ♔  |     |      | _Number_ |                |
| 2   | __`idAzioneRichiestaTask`__  |  ♕  |  ✓  |      | _Number_ |                |
| 3   | nomeFile                     |     |  ✓  |      | _String_ |                |
| 4   | URL                          |     |  ✓  |      | _String_ |                |
| 5   | dataInvio                    |     |  ✓  |      |  _Date_  |                |
| 6   | latitudine                   |     |     |      | _String_ |                |
| 7   | longitudine                  |     |     |      | _String_ |                |

-------------------------------------------------------------------------------------

<a name="domanda-questionario-task"></a>
###[T30. DomandaQuestionarioTask](#domanda-questionario-task) [☝](#indice-tabelle)

|  #  |              Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|-----------------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __idDomandaQuestionarioTask__     |  ♔  |     |      | _Number_ |                |
| 2   | __`idAzioneRichiestaTask`__       |  ♕  |  ✓  |      | _Number_ |                |
| 3   | indiceDomanda                     |     |  ✓  |      | _Number_ |                |
| 4   | testoDomanda                      |     |  ✓  |      | _String_ |                |
| 5   | tipoSelezioneRisposta             |     |  ✓  |      | _String_ |  __`multipla`<br/> `singola`__ |

------------------------------------------------------------------------------------------

<a name="opzione-risposta-questionario-task"></a>
###[T31. OpzioneRispostaQuestionarioTask](#opzione-risposta-questionario-task) [☝](#indice-tabelle)

|  #  |              Attribute Name               | Key | Req | Uniq |    Type    |     Domain     |
|:---:|-------------------------------------------|:---:|:---:|:----:|:----------:|:--------------:|
| 1   | __idOpzioneRispostaQuestionarioTask__     |  ♔  |     |      |  _Number_  |                |
| 2   | __`idDomandaQuestionarioTask`__           |  ♕  |  ✓  |      |  _Number_  |                |
| 3   | indiceRisposta                            |     |  ✓  |      |  _Number_  |                |
| 4   | tipoRisposta                              |     |  ✓  |      |  _String_  | __`libera`<br/>`precompilata`__ |
| 5   | selezionata                               |     |  ✓  |      |  _Boolean_ | __`true`<br/>`false`__ |
| 6   | dataInvio                                 |     |  ✓  |      |  _Date_    |                |
| 7   | testoRisposta                             |     |     |      |  _String_  |                |
| 8   | latitudine                                |     |     |      |  _String_  |                |
| 9   | longitudine                               |     |     |      |  _String_  |                |

----------------------------------------------------------------------------------------------------

<a name="storico-stato-task"></a>
###[T32. StoricoStatoTask](#storico-stato-task) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __`idTask`__              |  ♔♕ |     |      | _Number_ |                |
| 2   | __`idStatoTask`__         |  ♔♕ |     |      | _Number_ |                |
| 3   | data                      |     |     |      |  _Date_  |                |

----------------------------------------------------------------------------------

<a name="stato-task"></a>
###[T33. StatoTask](#stato-task) [☝](#indice-tabelle)

|  #  |      Attribute Name       | Key | Req | Uniq |   Type   |     Domain     |
|:---:|---------------------------|:---:|:---:|:----:|:--------:|:--------------:|
| 1   | __`idStatoTask`__         |  ♔  |     |      | _Number_ |                |
| 2   | stato                     |     |     |      | _String_ | __`disponibile`<br/>`assegnato`<br/>`scaduto`<br/>`approvato`<br/>`in revisione`__ |
| 3   | descrizione               |     |     |      | _String_ |                |

----------------------------------------------------------------------------------