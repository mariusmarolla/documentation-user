=========================================
Fatture d'acquisto o ricevute d'acquisto?
=========================================

Le ricevute d'acquisto sono diverse dalle fatture d'acquisto. Le fatture
d'acquisto sono richieste di pagamento. Se confermo un ordine d'acquisto, nella
maggior parte dei casi il mio fornitore emetterà un fattura. Dipendentemente
poi dagli accordi con il fornitore, avrò a disposizione un certo periodo di
tempo per pagare la fattura. Le ricevute d'acquisto, invece, sono conferme
di avvenuti pagamenti.

Dal punto di vista contabile c'è una differenza significativa, poichè una
fattura d'acquisto andrà ad accreditare un conto di debito prima di riconciliare
il pagamento con il conto bancario. Dall'altro lato, generalmente il pagamento
di una ricevuta avviene nel momento esatto della sua emissione (il che significa
che non è necessario valorizzare alcun conto di debito).

Inoltre, le ricevute d'acquisto possono avere un importo di imposta diverso
per ogni riga, mentre le fatture d'acquisto possono avere un solo importo di imposta
per l'intero conto.

Se utilizzo il conto bancario della mia azienda per pagare l'acquisto di prodotti
per i quali è stata emessa solo una ricevuta, dovrò utilizzare proprio la ricevuta
per gestire l'acquisto in contabilità.

Facciamo il seguente esempio: dobbiamo acquistare del tè per i nostri clienti da
un negozio locale che però non emette fatture. Ogni settimana acquistiamo 50€ di tè
e una teiera da 20€. Paghiamo utilizzando il conto bancario della nostra azienda.

Configurazione
==============

Non vi sono particolari configurazioni o impostazioni da applicare. Tutti gli
strumenti necessari dovrebbero essere già stati installati.

Registrare una ricevuta
=======================

Per importare la nostra ricevuta di 50€ per il te acquistato, dalla Contabilità
seleziona :menuselection:`Acquisti --> Ricevute d'Acquisto`.

Crea una nuova ricevuta e inserisci tutte le informazioni richieste.
Nota che, per il campo **Pagamento** hai la possibilità di scegliere tra
**Paga Adesso** e **Paga più tardi**. La differenza è significativa, poichè
con *Paga più tardi* il sistema generarerà una voce in un conto di debito,
mentre il *Paga Adesso* utilizzerà solo il conto bancario.

Nella maggior parte dei casi, il pagamento sarà immediato, e quindi selezioniamo
la voce *Paga Adesso*. Aggiungi il prodotto, il relativo conto e l'imposta.
Per questo esempio supponiamo che il te abbia un'imposta del 10% e la teiera del 22%.

.. image:: ./media/bill03.png
  :align: center

Valida la Ricevuta d'Acquisto per registrarla. Ricorda che devi
Validate the Purchase Receipt to post it. Don't forget you need to
:doc:`riconciliare i pagamenti <../../bank/reconciliation/use_cases>` 
per chiudere completamente la transazione nella tua contabilità.
