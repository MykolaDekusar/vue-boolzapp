- Milestone 1
  Replica della grafica con la possibilità di avere messaggi scritti dall’utente (verdi) e dall’interlocutore (bianco) assegnando due classi CSS diverse
  Visualizzazione dinamica della lista contatti: tramite la direttiva v-for, visualizzare nome e immagine di ogni contatto.

- Milestone 2
  Visualizzazione dinamica dei messaggi: tramite la direttiva v-for, visualizzare tutti i messaggi relativi al contatto attivo all’interno del pannello della conversazione
  Click sul contatto mostra la conversazione del contatto cliccato.

- Milestone 3
  Aggiunta di un messaggio: l’utente scrive un testo nella parte bassa e digitando “enter” il testo viene aggiunto al thread sopra, come messaggio verde
  Risposta dall’interlocutore: ad ogni inserimento di un messaggio, l’utente riceverà un “ok” come risposta, che apparirà dopo 1 secondo.

- Milestone 4
  Ricerca utenti: scrivendo qualcosa nell’input a sinistra, vengono visualizzati solo i contatti il cui nome contiene le lettere inserite (es, Marco, Matteo Martina -> Scrivo “mar” rimangono solo Marco e Martina)

- Milestone 5 - opzionale
  Cancella messaggio: cliccando sul messaggio appare un menu a tendina che permette di cancellare il messaggio selezionato.
  Visualizzazione ora e ultimo messaggio inviato/ricevuto nella lista dei contatti.

-------- Pensiero ---------

- Milestone 1:
  Prendo il vecchio progetto di Boolzapp e lo copio.
  Importo Vue.js nel progetto tramite CDN e nel data() return: gli assegno la stringa di persone con immagini, valore booleano e messaggi.
  Utilizzo il v-for per ciclare la stringa contacts e importare il name e avatar dentro l'html

- Milestone 2:
  A class="contact-card" ci aggiungo un @click con la funzione changeUser che mi va a prendere l'index di ogni utente e me lo imposta nel Vue.js ( ES primo contatto sarà 0, il secondo sarà 1 ecc...) in modo tale da mostrare sia l'immagine del contatto che il nome nella chat.

- Milestone 3:
  All'input del testo assegno un v-model che mi salva il messaggio inserito dall'utente e tramite @keyup.enter vado ad inserirlo dentro l'array in posizione di userIndex, una volta che inserisco il messaggio svuoto la cache del messaggio utente per poter inserire un nuovo messaggio.
  Dentro la stessa funzione creo una funzione anonima setTimeout che dopo 1 secondo mi richiama una funzione che pusha un oggetto dentro l'array corrente con il valore del messaggio Ok e status received.

- Milestone 4:
