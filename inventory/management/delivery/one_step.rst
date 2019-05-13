=====================================================================
Come elaborare gli ordini di consegna in un'unico step (spedizione)?
=====================================================================

Panoramica
==========

Quando un ordine di vendita arriva nel reparto spedizioni per la consegna finale, Zelo
è impostato di default per utilizzare un'operazione che consiste un un'unica fase: quando tutte le
merci sono pronte e disponibili queste possono essere spedite in un'unico ordine di consegna.

Configurazione
==============
Non è necessaria alcuna configurazione. Le spedizioni in uscita sono configurate di default per essere
consegnate direttamente in magazzino.

Tuttavia, se l'opzione **Percorsi multipassaggio** è stata abilitata ed è stata impostata un'altra configurazione per il tuo magazzino,
puoi facilmente tornare al sistema ad uno step.
Per farlo ti basterà andare in :menuselection:`Configurazione --> Magazzini` e modificare la configurazione del
magazzino in questione.

Imposta **Spedizioni in uscita** sull'opzione **Spedisci direttamente i Prodotti dal Punto di Stoccaggio (Solo Spedizione)**.

.. image:: media/one_step01.png
   :align: center

Creare un ordine di vendita
===========================

Crea un preventivo con inseriti diversi prodotti da spedire.
Conferma il preventivo trasformandolo in un ordine di vendita.

Vedrai apparire a questo punto uno smart buttom **Consegna** in alto a destra che ti
indica la presenza di una consegna associata all'ordine.

.. image:: media/one_step03.png
   :align: center

Cliccandoci sopra verrai direttamente portato nel movimento di magazzino corrispondente all'ordine.

Processare una consegna
=======================

Recupera il movimento di magazzino associato all'ordine di vendita.
Per farlo puoi utilizzare lo smart buttom **Consegna** nell'ordine (come visto sopra)
o andare in **Magazzino** e cliccare sul pulsante **# DA FARE** sotto **Ordini di Consegna** kanban card
e cercare il movimento nella lista.

.. image:: media/one_step02.png
   :align: center

in entrambi i casi entra nel movimento di magazzino.

Clicca sul pulsante **Valida** per completare il movimento di evasione dell'ordine dal
magazzino (WH/Output) al cliente.

In questo modo si è conclusa la spedizione in un step e lo stato del
movimento, che puoi vedere in alto a destra, dovrebbe essere **Fatto** per cui
il prodotto risulta spedito al cliente.


.. todo::
    Ajouter un lien vers ces pages quand elles existeront
    -  Process Overview: From sales orders to delivery orders

    -  Process Overview: From purchase orders to receptions
