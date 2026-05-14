**Package:** *GestioneUtenti*

*abstract: Utente*
	+ String: Nome
	+ String: Cognome
	+ String: e-mail
	+ String: password
	+ boolean: liberatoriaPrivacy
	+ boolean: documentoIdetita

*Atleta*
	+ date: dataNascita
	+ String: Campionato
	+ certificatoMedico: certificatoMedico
	+ Enum (Attivo, bloccato, sospeso): statoAccount

*Allenatore*
	+ String: Qualifica

**Package:** *GestioneAmministrazione* 

*certificatoMedico*
	+ Date: dataEmissione
	+ Date: dataScadenza
	+ Path: file
	+ Enum (In attesa, Validato, Rifiutato): statoCertficato
	+ String: motivazioneRifiuto

*rata*
	+ date: dataEmissione
	+ date: dataScadenza
	+ double: importo

*generazioneRata*
	+ double: tariffarioBase
	+ double: maggiorazioneCampionato

*pagamento*
	+ rata: riferimentoRata
	+ date: dataPagamento
	+ String: metodoPagamento
	+ boolean: esito

*abstract: notifiche* (da cui ereditano notificheDocumenti, notifichePagamenti e notificaSportiva)
	+ utente: destinatario
	+ Enum: canaleUtilizzato
	+ String: tipoMessaggio
	+ date: ultimoInvio

**Package:** *GestioneSportiva* 

*sessioneSportiva*
	+ date: Data
	+ time: oraInizio
	+ time: oraFine
	+ String: luogo
	+ convocazione: convocati

*presenza*
	+ Enum (Presente, Assente, Giustificato, Ritardo): statoPresenza
	+ String: note

*eventoSportivo*
	+ String: avversario
	+ date: data
	+ time: ora
	+ String: luogo
	+ file/pdf: convocazioni

*convocazione*
	+ collection di atleti: convocati
	+ eventoSportivo: evento
	+ Enum (inviata/non inviata): statoConvocazione
