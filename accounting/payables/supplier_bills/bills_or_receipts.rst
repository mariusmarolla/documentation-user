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

Configuration
=============

To handle purchase receipts in Odoo one module and one app has to be
installed. Go into the app module and install the accounting app.

.. image:: ./media/bill01.png
  :align: center

Then, go in the search bar, delete the default module search, and search
for "purchase". Install the **Sale & Purchase Vouchers** module.

.. image:: ./media/bill02.png
  :align: center

Register a receipt 
===================

By installing the **Sale & Purchase Vouchers** I've made the new
**Purchase Receipts** drop down menu visible in the accounting app.

To import our 50 euros worth of tea purchase receipt, enter the
accounting app, select :menuselection:`Purchases --> Purchase Receipts`.

Create a new Purchase Receipt and fill in all the necessary information.
Note that you have the choice in the Payment field between **Pay Later**
or **Pay Now**. It's a significant difference as Pay Later will generate
a debt accounting entry whereas Pay Now will immediately credit the Bank
account.

In most cases you immediately pay, we will thus select the Pay Directly
option. Add the products, the related account and the appropriate taxe.
For the example we suppose the tea is a 12% taxe and the Tea Pott 21%.

.. image:: ./media/bill03.png
  :align: center

Validate the Purchase Receipt to post it. Don't forget you need to
:doc:`reconcile payments <../../bank/reconciliation/use_cases>` in order to
completely close the transaction in your accounting.
