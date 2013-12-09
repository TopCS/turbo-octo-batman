### Elenco Attributi Entità

*[Torna all'indice generale](../Readme.md)*

<a name="indice"></a>
* __[Indice](#indice)__:
    * __[1. Utente](#utente)__
    * __[2. Bee](#bee)__
    * __[3. Beekeeper](#beekeeper)__
    * __[4. PreferitiBee](#preferiti-bee)__
    * __[5. PreferitiBeekeeper](#preferiti-beekeeeper)__
    * __[6. PrelievoBee](#prelievo-bee)__
    * __[7. DocumentoFiscaleBee](#documento-fiscale-bee)__
    * __[8. Prodotto](#prodotto)__
    * __[9. OrdineBeekeeper](#ordine-beekeeper)__
    * __[10. StoricoOrdineBeekeeper](#storico-ordine-beekeeper)__
    * __[11. StatoOrdineBeekeeper](#stato-ordine-beekeeper)__
    * __[12. ScontoProdotto](#ScontoProdotto)__
    * __[13. VersamentoBeekeeper](#versamento-beekeeper)__
    * __[14. FatturaEmessa](#fattura-emessa-beekeeper)__
    * __[15. Job](#job)__
    * __[16. Task](#task)__
    * __[17. LuogoTask](#luogo-task)__
    * __[18. AreaPresidioBee](#area-presidio-bee)__
    * __[19. ChatRoomTask](#chat-room-task)__
    * __[20. MessaggioChat](#messaggio-chat)__
    * __[21. NotificaUtente](#notifica-utente)__
    * __[22. CandidaturaTask](#candidatura-task)__
    * __[23. AzionePredefinitaJob](#azione-predefinita-job)__
    * __[24. ImmagineEsempioAzionePredefinitaJob](#immagine-esempio-azione-predefinita-job)__
    * __[25. DomandaQuestionarioPredefinitoJob](#domanda-questionario-predefinito-job)__
    * __[26. OpzioneRispostaQuestionarioPredefinitoJob](#opzione-risposta-questionario-predefinito-job)__
    * __[27. AzioneRichiestaTask](#azione-richiesta-task)__
    * __[28. ImmagineRicevutaTask](#immagine-ricevuta-task)__
    * __[29. FilmatoRicevutoTask](#filmato-ricevuto-task)__
    * __[30. DomandaQuestionarioTask](#domanda-questionario-task)__
    * __[31. OpzioneRispostaQuestionarioTask](#opzione-risposta-questionario-task)__
    * __[32. StoricoStatoTask](#storico-stato-task)__
    * __[33. StatoTask](#stato-task)__

--------------------------------------------------------------------------------

<a name="utente"></a>
* [1. Utente](#utente) __[☝](#indice)__
    * __idUtente__
    * username
    * email
    * auth
    * dataCreazione
    * statoUtenza
    * statoVerificaCredenziali
    * tipoUtente
    * dataUltimoAccesso
    * dataUltimaModifica
    * twitterId
    * facebookId
    * linkedinId
    * avatarURL

<a name="bee"></a>
* [2. Bee](#bee) __[☝](#indice)__
    * __idBee__
    * bankrollCrediti
    * nome
    * cognome
    * codiceFiscale
    * ragioneSociale
    * partitaIVA
    * tipologiaFiscale
    * fax
    * cellulare
    * telefono
    * via
    * civico
    * codicePostale
    * località
    * comune
    * provincia
    * dataNascita
    * sesso

<a name="beekeeper"></a>
* [3. Beekeeper](#beekeeper) __[☝](#indice)__
    * __idBeekeper__
    * bankrollCrediti
    * creditiDisponibili
    * nome
    * cognome
    * codiceFiscale
    * ragioneSociale
    * partitaIVA
    * fax
    * cellulare
    * telefono
    * via
    * civico
    * codicePostale
    * località
    * comune
    * provincia

<a name="preferiti-bee"></a>
* [4. PreferitiBee](#preferiti-bee) __[☝](#indice)__
    * __`idBee`__
    * __`idBeekeeper`__

<a name="preferiti-beekeeper"></a>
* [5. PreferitiBeekeeper](#preferiti-beekeeper) __[☝](#indice)__
    * __`idBeekeeper`__
    * __`idBee`__

<a name="prelievo-bee"></a>
* [6. PrelievoBee](#prelievo-bee) __[☝](#indice)__
    * __idPrelievoBee__
    * __`idBee`__
    * codiceOperazione
    * dataRichiesta
    * dataPrelievo
    * statoPrelievo
    * importoValutaPrelevata
    * importoCreditiCeduti

<a name="documento-fiscale-bee"></a>
* [7. DocumentoFiscaleBee](#documento-fiscale-bee) __[☝](#indice)__
    * __idDocumentoFiscaleBee__
    * __`idPrelievoBee`__
    * numeroDocumento
    * tipoDocumento
    * nomeFile
    * URL
    * dataEmissione

<a name="prodotto"></a>
* [8. Prodotto](#prodotto) __[☝](#indice)__
    * __idProdotto__
    * descrizione
    * dataCreazione
    * prezzo
    * crediti
    * tipoVersamentoRichiesto

<a name="ordine-beekeeper"></a>
* [9. OrdineBeekeeper](#ordine-beekeeper) __[☝](#indice)__
    * __idOrdineBeekeeper__
    * __`idBeekeeper`__
    * __`idProdotto`__
    * __`idScontoProdotto`__
    * codiceOrdine
    * dataOrdine
    * importoValutaOrdine
    * statoCorrente
    * dataStatoCorrente

<a name="storico-ordine-beekeeper"></a>
* [10. StoricoOrdineBeekeeper](#storico-ordine-beekeeper) __[☝](#indice)__
    * __idStoricoOrdineBeekeeper__
    * __`idOrdineBeekeeper`__
    * __`idStatoOrdineBeekeeper`__
    * data

<a name="stato-ordine-beekeeper"></a>
* [11. StatoOrdineBeekeeper](#stato-ordine-beekeeper) __[☝](#indice)__
    * __idStatoOrdineBeekeeper__
    * statoOrdine
    * descrizioneStato

<a name="ScontoProdotto"></a>
* [12. ScontoProdotto](#ScontoProdotto) __[☝](#indice)__
    * __idScontoProdotto__
    * codiceSconto
    * percentualeSconto
    * dataInserimento
    * dataScadenza

<a name="versamento-beekeeper"></a>
* [13. VersamentoBeekeeper](#versamento-beekeeper) __[☝](#indice)__
    * __idVersamentoBeekeeper__
    * __`idOrdineBeekeeper`__
    * codiceOperazione
    * dataVersamento
    * tipoVersamento
    * importoValutaVersata

<a name="fattura-emessa"></a>
* [14. FatturaEmessa](#fattura-emessa) __[☝](#indice)__
    * __idFatturaEmessa__
    * __`idVersamentoBeekeeper`__
    * nomeFile
    * URL
    * numeroFattura
    * dataEmissione

<a name="job"></a>
* [15. Job](#job) __[☝](#indice)__
    * __idJob__
    * __`idBeekeeper`__
    * titoloJob
    * descrizioneJob
    * statoPubblicazione
    * dataCreazione
    * dataPubblicazione
    * dataScadenzaPubblicazione
    * percentualeCompletamento
    * totaleCreditiInvestiti

<a name="task"></a>
* [16. Task](#task) __[☝](#indice)__
    * __idTask__
    * __`idJob`__
    * __`idBee`__
    * statoPubblicazione
    * statoCorrenteTask
    * dataStatoCorrente
    * dataCreazione
    * dataPubblicazione
    * totaleCreditiOfferti
    * totaleCreditiPattuiti
    * votoBee
    * votoBeekeeper
    * commentoBee
    * commentoBeekeeper

<a name="luogo-task"></a>
* [17. LuogoTask](#luogo-task) __[☝](#indice)__
    * __idLuogoTask__
    * __`idTask`__
    * descrizione
    * timestamp
    * latitudine
    * longitudine
    * raggio
    * comune
    * provincia
    * via
    * codicePostale
    * località

<a name="area-presidio-bee"></a>
* [18. AreaPresidioBee](#area-presidio-bee) __[☝](#indice)__
    * __idAreaPresidioBee__
    * __`idBee`__
    * tipoPresidio
    * descrizione
    * timestamp
    * latitudine
    * longitudine
    * raggio
    * comune
    * provincia
    * via
    * codicePostale
    * località

<a name="chat-room-task"></a>
* [19. ChatRoomTask](#chat-room-task) __[☝](#indice)__
    * __idChatRoomTask__
    * __`idTask`__
    * statoChatRoom
    * titolo

<a name="messaggio-chat"></a>
* [20. MessaggioChat](#messaggio-chat) __[☝](#indice)__
    * __idMessaggioChat__
    * __`idChatRoomTask`__
    * _`idBee`_
    * _`idBeekeeper`_
    * tipoMittente
    * timestamp
    * testo

<a name="notifica-utente"></a>
* [21. NotificaUtente](#notifica-utente) __[☝](#indice)__
    * __idNotificaUtente__
    * __`idUtente`__
    * timestamp
    * oggetto
    * URL

<a name="candidatura-task"></a>
* [22. CandidaturaTask](#candidatura-task) __[☝](#indice)__
    * __idCandidaturaTask__
    * __`idTask`__
    * __`idBee`__
    * statoCandidatura
    * tipoCandidatura
    * dataCandidatura
    * offertaCreditiBee
    * codiceInvito
    * dataInvito

<a name="azione-predefinita-job"></a>
* [23. AzionePredefinitaJob](#azione-predefinita-job) __[☝](#indice)__
    * __idAzionePredefinitaJob__
    * __`idJob`__
    * titolo
    * descrizione
    * tipoAzione
    * creditiOfferti

<a name="immagine-esempio-azione-predefinita-job"></a>
* [24. ImmagineEsempioAzionePredefinitaJob](#immagine-esempio-azione-predefinita-job) __[☝](#indice)__
    * __idImmagineEsempioAzionePredefinitaJob__
    * __`idAzionePredefinitaJob`__
    * dataInserimento
    * nomeFile
    * URL

<a name="domanda-questionario-predefinito-job"></a>
* [25. DomandaQuestionarioPredefinitoJob](#domanda-questionario-predefinito-job) __[☝](#indice)__
    * __idDomandaQuestionarioPredefinitoJob__
    * __`idAzionePredefinitaJob`__
    * indiceDomanda
    * testoDomanda
    * tipoSelezioneRisposta

<a name="opzione-risposta-questionario-predefinito-job"></a>
* [26. OpzioneRispostaQuestionarioPredefinitoJob](#opzione-risposta-questionario-predefinito-job) __[☝](#indice)__
    * __idOpzioneRispostaQuestionarioPredefinitoJob__
    * __`idDomandaQuestionarioPredefinitoJob`__
    * indiceRisposta
    * tipoRisposta
    * testoRisposta

<a name="azione-richiesta-task"></a>
* [27. AzioneRichiestaTask](#azione-richiesta-task) __[☝](#indice)__
    * __idAzioneRichiestaTask__
    * __`idSequenzaRichiestaAzioniTask`__
    * titolo
    * descrizione
    * tipoAzione
    * creditiOfferti

<a name="immagine-ricevuta-task"></a>
* [28. ImmagineRicevutaTask](#immagine-ricevuta-task) __[☝](#indice)__
    * __idImmagineRicevutaTask__
    * __`idAzioneRichiestaTask`__
    * nomeFile
    * URL
    * dataInvio
    * latitudine
    * longitudine

<a name="filmato-ricevuto-task"></a>
* [29. FilmatoRicevutoTask](#filmato-ricevuto-task) __[☝](#indice)__
    * __idFilmatoRicevutoTask__
    * __`idAzioneRichiestaTask`__
    * nomeFile
    * URL
    * dataInvio
    * latitudine
    * longitudine

<a name="domanda-questionario-task"></a>
* [30. DomandaQuestionarioTask](#domanda-questionario-task) __[☝](#indice)__
    * __idDomandaQuestionarioTask__
    * __`idQuestionarioTask`__
    * indiceDomanda
    * testoDomanda
    * tipoSelezioneRisposta

<a name="opzione-risposta-questionario-task"></a>
* [31. OpzioneRispostaQuestionarioTask](#opzione-risposta-questionario-task) __[☝](#indice)__
    * __idOpzioneRispostaQuestionarioTask__
    * __`idDomandaQuestionarioTask`__
    * indiceRisposta
    * tipoRisposta
    * selezionata
    * dataInvio
    * testoRisposta
    * latitudine
    * longitudine

<a name="storico-stato-task"></a>
* [32. StoricoStatoTask](#storico-stato-task) __[☝](#indice)__
    * __`idTask`__
    * __`idStatoTask`__
    * data

<a name="stato-task"></a>
* [33. StatoTask](#stato-task) __[☝](#indice)__
    * __idStatoTask__
    * stato
    * descrizione
