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
Crea un preventivo con inseriti diversi prodotti da spedire. Conferma il preventivo trasformandolo in un ordine di vendita.

Vedrai apparire a questo punto uno smart buttom Consegna in alto a destra che ti indica la presenza di due trasferimenti associata all'ordine.

.. image:: media/two_steps01.png
   :align: center

Cliccandoci sopra verrai direttamente portato nel magazzino e vedrai due differenti trasferimenti 
corrispondenti all'ordine: uno con riferimento **PICK** che fa riferimento al prelievo e raggruppamento merce e 
**OUT** che fa riferimento alla spedizione.

.. image:: media/two_steps04.png
   :align: center

Processare una consegna
=======================

Come processare lo step di picking o prelievo merce?
-----------------------------------------------------

Recupera il movimento di magazzino **PICK** associato all'ordine di vendita. 
Per farlo puoi utilizzare lo smart buttom Consegna nell'ordine (come visto sopra) o andare in **Magazzino** e cliccare sul pulsante **# Trasferimenti** sotto **Pick** kanban card e cercare il movimento nella lista.

.. image:: media/two_steps06.png
   :align: center

In entrambi i casi entra nel movimento di magazzino.

(Click on **Reserve** to reserve the products if they are available.?)

Clicca su **Valida** per completare il movimento dei prodotti da **WH/Stock** a **WH/Output**.

In questo modo si è concluso lo step del prelievo (picking) e lo stato del movimento, che puoi vedere in alto a destra, dovrebbe essere **Fatto** per cui il prodotto risulta trasferito da **WH/Stock** a **WH/Output** ed è **pronto e disponibile per lo step successivo** ossia la spedizione.

Come processare lo step di spedizione o consegna?
-------------------------------------------------

Recupera il movimento di magazzino **OUT** associato all'ordine di vendita. 
Per farlo puoi utilizzare lo smart buttom Consegna nell'ordine (come visto sopra) o andare in **Magazzino** e cliccare sul pulsante **# DA FARE** sotto **Ordini di Consegna** kanban card e cercare il movimento nella lista.

.. image:: media/two_steps02.png
   :align: center

In entrambi i casi entra nel movimento di magazzino.

Clicca sul pulsante **Valida** per completare il movimento di evasione dell'ordine dal magazzino **WH/Output** al cliente.

In questo modo si è concluso lo step di consegna e lo stato del movimento **WH/OUT**, che puoi vedere in alto a destra, dovrebbe essere **Fatto** per cui il prodotto risulta spedito al cliente.

.. todo::
    link to these sections when they will be available
    -  Process Overview: From sales orders to delivery orders

    -  Process Overview: From purchase orders to receptions
