=======================================================================
Come scegliere tra le regole produzione su ordine e approvvigionamento?
=======================================================================

Le regole **Produzione su ordine** e **regole di approvvigionamento** hanno conseguenze simili ma logiche differenti. 
Dovrebbero essere opportunamente utilizzate a seconda delle tue logiche di produzione e consegna.

Terminologia
============

Regole di approvvigionamento
----------------------------

Le regole di approvvigionamento sono utilizzate per garantire la costante presenza di una minima quantità di prodotto 
che ti permetta di fabbricare ciò che vendi e rispondere alle esigenze dei clienti.
Nello specifico quando un prodotto raggiunge la quantità minima presente fissata, Zelo genera 
automaticamente un ordine contenente la quantità necessaria a riportare la quantità presente al livello massimo fissato.

Produzione su ordine
--------------------

La funzione **Produzione su ordine** genera un ordine di acquisto dell’importo dell’ordine di vendita relativo al prodotto. 
Non avviene alcun controllo sulla quantità attuale presente del prodotto. 
Ciò significa che verrà generata una bozza d’ordine indipendentemente dalla quantità posseduta.

Configurazione
==============

Regole di approvvigionamento
-----------------------------

Puoi configurare le regole di approvvigionamento in :menuselection:` Inventario --> Anagrafiche  Regole di Approvvigionamento`. 
Qui fai clic su **Crea** per impostare i valori minimi e massimi di riferimento per uno specifico prodotto.

.. image:: media/min_stock_rule_vs_mto01.png
   :align: center

.. demo:fields:: stock.action_orderpoint_form

   ---Lo smart buttom *Attivo* vi da la possibilità di archiviare quella regola, rendendola inattiva, senza cancellarla rendendola al
   contenpo, dunque, recuperabile.
   L'unità di misura è quella utilizzata di default per tutte le operazioni di magazzino.
   Gruppo di approvvigionamento?---

   ---La quantità minima indica la soglia al di sotto della quale parte la generazione automatica dell'ordine d'acquisto per
   aumentare le scorte.
   La quantità massima è il riferimento utilizzato da Zelo per indicare una quantità nell'ordine d'acquisto: il sistema infatti
   tenderà a riportare la quantità disponibile alla quantità massima di riferimento indicata.
   Il campo multiplo quantità rappresenta il riferimento per arrotondare la quantità inserita nell'ordine d'acquisto. Se il valore                          indicato è 0 allora verrà indicata la quantità esatta.
   Infine il campo *tempi di consegna* può indicare il numero di giorni, dopo l'esecuzione della regola, necessari per ricevere i   prodotti o per confermare l'ordine al fornitore.---



Poi, cerca e clicca sul prodotto per accedere alla sua scheda profilo e, nel tab **Magazzino**, ricordati di inserire un fornitore.

.. image:: media/min_stock_rule_vs_mto02.png
   :align: center

.. tip::
    Fai attenzione a selezionare la giusta tipologia di prodotto quando lo crei.
    Zelo non tiene la consistenza di magazzino dei prodotti consumabili poichè vengono considerati sempre presenti
    pertanto una regola di approvigionamento non funzionerebbe.
    

Produzione su ordine
---------------------

Puoi configurare la regola di produzione su ordine all'interno della scheda profilo del 
prodotto: :menuselection:`Magazzino --> Anagrafiche --> Prodotti` (o al limite accedendo ai prodotti da altre aree
in cui è possibile farlo come ad esempio Vendite o Acquisti).

all'interno della scheda prodotto, nel tab **Magazzino**, seleziona l'opzione **Produzione su ordine** nella sezione *Percorsi approvvigionamento*

.. image:: media/min_stock_rule_vs_mto03.png
   :align: center

Scegliere tra le due opzioni
----------------------------
Quale opzione scegliere tra le due presentate dipende dalla vostra strategia di gestione del
magazzino. Le regole di approvvigionamento sono utili qualora tu preferisca avere una scorta minima
sempre presente mentre, al contrario, la produzione su ordine è utile qualora tu preferisca
procurarti i prodotti necessari a soddisfare la richiesta del cliente solo quando la vendita è confermata.

The choice between the two options is thus dependent of your inventory
strategy. If you prefer to have a buffer and always have at least a
minimum amount, the minimum stock rule should be used. If you want to
reorder your stocks only if your sale is confirmed it is better to use
the Make to Order.
