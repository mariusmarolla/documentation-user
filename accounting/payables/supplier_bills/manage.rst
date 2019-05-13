=============================
Gestire le fatture d'acquisto
=============================

Gli **Acquisti** ti consentono di gestire gli ordini d'acquisto,
i prodotti in ingresso e le fatture, tutto del medesimo posto.

Per impostare un processo di controllo delle fatture fornitore, la prima
cose da fare è verificare che vi siano alcuni dati di acquisto in Zelo.
Sapere cosa è stato acquistato e ricevuto è il primo passo per comprendere
la gestione del processo d'acquisto.

il processo predefinito in Zelo è il seguente:

1. Iniziamo con una **Richiesta di Quotazione** da inviare al/ai fornitore/i.

2. Una volta che il fornitore ha risposto alla Richiesta di Quotazione,
   confermiamo l'**Ordine di Acquisto**.

3. La conferma dell'ordine di acquisto genere una **Spedizione in Entrata**
   (se il prodotto acquistato è di tipo **stoccabile**).

4. Dopo aver ricevuto la **Fattura d'Acquisto** del tuo fornitore,
   validala confrontandola con i prodotti ricevuti nel passaggio precedente.

Questo processo può essere svolto da tre diverse persone all'interno dell'azienda,
oppure solo da una.

Configurazione
==============

Creare prodotti
---------------

La creazione di prodotti in Zelo è essenziale per un processo di acquisto
rapido ed efficiente. Spostati nel sottomenu Prodotti degli Acquisti e
fai clic sul pulsante **Crea**.

.. image:: ./media/manage01.png
  :align: center

Durante la creazione di un prodotto, presta attenzione al **Tipo di Prodotto**,
poiché è estremamente importante:

- I prodotti impostati come **Stoccabili o Consumabili** ti consentiranno
  di tenere traccia dei livelli di magazzino. Queste opzioni implicano
  la gestione dello stock e ti consentiranno di ricevere questo tipo di prodotti.
  
- Per contro, i prodotti impostati come **Servizi o Prodotti Digitali**
  non implicano la gestione dello stock, poiché semplicemente non vi è
  alcuni inventario gestire. Ovviamente non sarà possibile ricevere
  questo tipo di prodotti.
  
.. tip::

        Ti consigliamo vivamente di creare un prodotto **Varie** per tutti quegli acquisti
	che non ricorrono frequentemente e che non richiedono una gestione o una valutazione
	di inventario.
	Creando un prodotto di questo tipo, conviene impostarlo come **Servizio**.

Gestire le fatture d'acquisto
=============================

Acquistare prodotti o servizi
-----------------------------

Dagli Acquisti è possibile creare un ordine d'acquisto contenente numerosi
prodotti diversi. Se il tuo fornitore ti invia una conferma o una quotazione,
puoi registrare il numero di riferimento ordine nel campo **Rif. Fornitore**.
Questo ti consentirà di far corrispondere più avanti l'ordine d'acquisto
con la fattura (poiché la fattura indicherà molto probabilmente il Riferimento
Fornitore).

.. image:: ./media/manage02.png
  :align: center

Valida ora l'ordine d'acquisto e ricevi i prodotti nell'area Magazzino.

Ricevere i prodotti
-------------------

Se hai acquistato prodotti stoccabili per i quali richiesta una gestione
del magazzino, avrei la necessità di effettuare il **Ricevimento Merci**
dopo aver confermato l'ordine d'acquisto. Nel **Dashboard del Magazzino**
dovresti vedere un pulsante che ti condurrà direttamente al trasferimento
dei prodotti.

.. image:: ./media/manage03.png
  :align: center

Seguendo questo percorso, verrà condotto a una lista di tutti gli ordini
in attesa di essere ricevuti.

.. image:: ./media/manage04.png
  :align: center

Se hai molti ordini in attesa, applica un filtro utilizzando la barra di
ricerca in alto a destra. La barra di ricerca puoi filtrare gli ordini
per fornitore (partner), per prodotto o per documento di origine
(il riferimento del tuo ordine d'acquisto). Potrai inoltre raggruppare
gli ordini secondo diversi criteri utilizzando il menu **Raggruppa**.
Selezionando infine un elemento della lista, si aprirà la seguente schermata
dalla quale potrai ricevere i prodotti.

.. image:: ./media/manage05.png
  :align: center

L'acquisto di prodotti di tipo **Servizio** non comporterà la creazione
di un movimento di **Ingresso Merci**.

Gestire le fatture d'acquisto
-----------------------------

Quando ricevi una fattura d'acquisto per un ordine d'acquisto, assicurati
di registrarla nel menu **Controllo** degli Acquisti. Dovrai creare
una nuova fatture d'acquisto anche se hai già registrato un ordine d'acquisto.

.. image:: ./media/manage06.png
  :align: center

La prima cosa da fare per creare una fattura d'acquisto è la selezione
del fornitore, poiché questa operazione consentirà al sistema di caricare
tutte le informazioni contabili ed il listino associati a questo partner.
Solo a questo punto potrai specificare uno o più ordini d'acquisto da collegare
alla fattura. Quando selezioni un ordine d'acquisto dalla lista, Zelo
recupererà tutti i prodotti non fatturati associati a quell'ordine d'acquisto
e li inserirà nella fattura. Se dovessi avere difficoltà a trovare l'ordine
che stai cercando, potrai spostarti nella lista inserendo il Numero di Riferimento
Fornitore o il codice interno dell'ordine d'acquisto.

.. image:: ./media/manage07.png
  :align: center

Fintanto che la fattura si trova nello stato Bozza, puoi effettuare tutte le modifiche
che ritieni opportune (aggiungere o rimuovere righe, modificare quantità
e modificare prezzi).

.. note::

	Il fornitore potrebbe inviarti più fatture per il medesimo ordine d'acquisto se:
	
	1. Il fornitore effettua una consegna parziale ed emette fatture sulla base dei
	   prodotti consegnati.
	2. Il fornitore sta inviando una fattura parziale o richiede un acconto.

Ogni volta che registri una fatture d'acquisto, Zelo completerà automaticamente
le quantità di prodotto sulla base delle quantità ricevuto del fornitore.
Se viene visualizzata una quantità a 0, significa che non hai ancora ricevuto
questo prodotto e ti ricorda che non lo hai ancora disponibile. In ogni momento,
prima di validare la fattura d'acquisto, puoi forzare questa quantità.

Corrispondenza delle fatture d'acquisto
=======================================

Cosa fare se la fattura d'acquisto non corrisponde alle merci ricevute
----------------------------------------------------------------------


If the bill you receive from the vendor has different quantities than
what Odoo automatically populates as quantities, this could be due to
several reasons:

- the vendor is incorrectly charging you for products and/or services
  that you have not ordered,

- the vendor is billing you for products that you might not have
  received yet, as the invoicing control may be based on ordered or
  received quantities,

- or the vendor did not bill you for previously purchased products.

In these instances it is recommended that you verify that the bill, and
any associated purchase order to the vendor, are accurate and that you
understand what you have ordered and what you have already received.

If you are unable to find a purchase order related to a vendor bill,
this could be due to one of a few reasons:

- the vendor has already invoiced you for this purchase order,
  therefore it is not going to appear anywhere in the selection,

- someone in the company forgot to record a purchase order for this
  vendor,

- or the vendor is charging you for something you did not order.



How product quantities are managed
----------------------------------

By default, services are managed based on ordered quantities, while
stockables and consumables are managed based on received quantities.

If you need to manage products based on ordered quantities over received
quantities, you will need to belong to the group **Purchase Manager**.
Ask your system administrator to enable these access on :menuselection:`Settings
--> Users --> Users --> Access Rights`. Once you belong to the correct group,
select the product(s) you wish to modify, and you should see a new field appear,
labeled **Control Purchase Bills**.

.. image:: ./media/manage08.png
  :align: center

You can then change the default management method for the selected
product to be based on either:

- Ordered quantities

- or Received quantities

Batch Billing
-------------

When creating a vendor bill and selecting the appropriate purchase
order, you may continue to select additional purchase orders and Odoo
will add the additional line items from that purchase order.. If you
have not deleted the previous line items from the first purchase order
the bill will be linked to all the appropriate purchase orders.
