============================================================================
Come processare gli ordini di consegna in due steps (prelievo + spedizione)?
============================================================================

Panoramica
==========

Quando un ordine viene mandato al reparto spedizioni, la configurazione di default di
Zelo consiste nell'utilizzo di uno step: quando tutti i prodotti sono pronti e
disponibili possono essere spediti in un'unico ordine di consegna.
Tuttavia, il processo di gestione del magazzino e delle consegne della tua azienda potrebbe 
necessitare di più step prima della spedizione. 
Nel processo con **due step** i prodotti di un ordine vengono prima **raggruppati in una location per l'uscita** e 
successivamente vengono **spediti**.

Per utilizzare il sistema a due fasi ci sono poche passaggi di configurazione necessari.
Tali passaggi creeranno una location aggiuntiva chiamata **Output** per cui se il tuo
magazzino è identificato con **WH** verrà creata la location **WH/Output**.
Le merci si sposteranno da *WH/Stock* a *WH/Output* nel primo step e poi da quest'ultimo a 
*WH/Customers*, nel caso degli ordini di vendita, nel secondo step.

.. note::
    Consulta :doc:`inventory_flow` per determinare se questo sistema è il metodo giusto per soddisfare
    le esigenze della tua attività.

Configurazione
==============

Consentire la gestione dei percorsi
------------------------------------
Zelo configura e gestisce gli ordini di consegna tramite i **Percorsi**. 
Questi consistono in meccanismi per concatenare le varie azioni.
In questo caso, vogliamo legare la fase di prelievo dei prodotti alla fase 
di spedizione degli stessi.

Per poter gestire i percorsi vai in :menuselection:`Magazzino --> Configurazione --> impostazioni`.

Abilita l'opzione **Percorsi Multi-Passaggio**.

.. image:: media/two_steps05.png
   :align: center

Premi il pulsante **Salva** in alto a sinistra per tenere le modifiche alla nuova
configurazione.

.. note::
    Nel caso l'opzione **Location Magazzino** non fosse stata precedentemente abilitata
    noterai che verrà automaticamente spuntata insieme a quella relativa ai percorsi.

Configurare il magazzino con due step
-------------------------------------
Per configurare il magazzino all'uso di due step vai in :menuselection:`Magazzino --> Configurazione --> Magazzini` 
e modifica le impostazioni del magazzino che utilizzerai.

In particolare seleziona l'opzione **Porta i Prodotti nell'area d'uscita prima della spedizione (Pick + Ship)** per
quanto riguarda le *Spedizioni in Uscita*.

.. image:: media/two_steps03.png
   :align: center

Creare un Ordine di Vendita
===========================

Install the **Sale** if it is not the case, and 
create a sales order with some products to deliver.

Notice that we now see ``2`` transfers associated with this sales order
in the **Delivery** stat button above the sales order.

.. image:: media/two_steps01.png
   :align: center

If you click on the **2 Transfers** stat button, you should now see two
different pickings, one with a reference **PICK** to designate the
picking process and another with a reference **OUT** to designate the
shipping process.

.. image:: media/two_steps04.png
   :align: center

Process a Delivery
==================

How to Process the Picking Step?
--------------------------------

Ensure that you have enough product in stock, and go to 
**Inventory** and click on the **Waiting** link under the **Pick** kanban card.

.. image:: media/two_steps06.png
   :align: center

Click on the picking that you want to process.

Click on **Reserve** to reserve the products if they are available.

Click on **Validate** to complete the move from **WH/Stock** to **WH/Output**.

This has completed the picking step and the **WH/PICK** move should now show
**Done** in the status column at the top of the page. The product has
been moved from **WH/Stock** to **WH/Output** location, which makes the product
**available for the next step** (Shipping).

How to Process the Shipping Step?
---------------------------------

Go to **Inventory** and click on the **# TO DO** link under the
**Delivery Orders** kanban card.

.. image:: media/two_steps02.png
   :align: center

Click on the picking that you want to process.

Click on **Validate** to complete the move from **WH/Output** to the
customer (Click **Apply** to assign the quantities based on the
quantities listed in the **To Do** column)

This has completed the shipping step and the **WH/OUT** move should now show
**Done** in the status column at the top of the page. The product has
been shipped to the customer.

.. todo::
    link to these sections when they will be available
    -  Process Overview: From sales orders to delivery orders

    -  Process Overview: From purchase orders to receptions
