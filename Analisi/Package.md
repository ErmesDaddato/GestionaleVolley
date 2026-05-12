**Package:** *GestioneUtenti*
	+ *Abstract* Utente: contiene email, password e ruolo per gestire login, recupero credenziali, carta d'identità/liberatoria privacy (boolean), certificato medico (associazione tra entità);

Utente -> Atleta, Allenatore, Amministratore.

Document sarà un attributo dello user che tiene traccia dello stato del caricamento e della scadenza dei documenti

**Package:** *GestioneAmministrazione* 
	+ certificatoMedico: memorizza file, la data di emissione e la scadenza;
	+ Rata: rappresenta la singola quota emessa con relativo stato di scadenza;
	+ NotifichePagamenti: si occupa dei solleciti, dei blocchi per morosità e della generazione.
	+ NotificheDocumenti: gestisce le notifiche automatiche di scadenza e i blocchi funzionali in caso di documenti non validi.
	+ GenrazioneRata: contiene le regole per il calcolo dinamico delle tariffe;
	+ Pagamento: contiene i metodi per il pagamento;

**Package:** *GestioneSportiva*
	+ SessioneSportiva: gestisce data, ora, luogo e l'eventuale annullamento delle sessioni;
	+ Presenza: registra le presenze degli atleti per ogni allenamento;
	+ EventoSportivo: rappresenta la gara o l'evento sportivo;
	+ Convocazione: associa gli atleti a una gara specifica;
	+ NotificaSportiva: gestisce l'invio delle notifiche per convocazioni o variazioni di programma. 

*Da mettere nella sezione di analisi*
Interagiscono con la view
**Package:** *Controller*
	+ AccountController: gestisce la logica di ricerca, modifica ed eliminazione dei profili.
	+ PaymentController: registra i dettagli della transazione avvenuta tramite gateway di pagamento oppure utilizza GenerazioneRata;
	+ DocumentController: si occupa di liberatoria privacy, carta d'identità e certificato medico;
	+ SportController: si occupa della gestione della view per tutte le informazioni riguardanti il package sportOperations.
