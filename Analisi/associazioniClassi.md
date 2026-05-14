**Package:** *GestioneUtenti*

C'è un'unica classe, quindi non ci sono relazioni.

**Package:** *GestioneAmministrazione* 

Un'atleta può avere da 0 (se non ancora caricato) e 1 certificato medico, mentre un certificato medico può essere associato ad un unico atleta.

Un'atleta può avere associate da 0 a n (n dipende dal numero di rate che decide di emettere la società) rate, mentre una rata può essere associata ad un unico atleta.

generazioneRata viene utilizzata da rata.

Un'atleta può effettuare da 0 a n pagamenti, mentre un pagamento può essere effettuato da un unico atleta.

Le notifiche sono utilizzate da certificato medico e rata per inviare notifiche di sollecito e/o scadenza.

**Package:** *GestioneSportiva* 

Un'atleta può essere associato a un'unica convocazione, mentre a una convocazione possono essere associati più atleti.

Un evento sportivo può essere associato a un'unica sessione sportiva e a una sessione sportiva può essere associato un unico evento.

Sessione sportiva utilizzata presenza.

Una convocazione è associata a un'unica sessione sportiva, mentre a una sessione sportiva è associata un'unica convocazione.
