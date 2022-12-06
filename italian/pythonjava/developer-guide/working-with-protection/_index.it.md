---
title: Lavorare con la protezione
type: docs
weight: 90
url: /it/python-java/working-with-protection/
---
## **Set Protezione del Visio Diagram**
La protezione dei diagrammi consente agli utenti di bloccare sfondi, master (stencil), forme e stili in modo che non possano essere modificati. Ciò è utile per proteggere gli stili aziendali, ad esempio, e garantire un aspetto coerente in una serie di diagrammi. Gli sviluppatori possono raggiungere questo obiettivo utilizzando Aspose.Diagram per Python tramite Java.

### **Modifica protezione del Visio Diagram**
I metodi getProtectBkgnds, getProtectMasters, getProtectShapes e getProtectStyles, esposti dalla classe DocumentSettings, supportano l'oggetto BoolValue. Queste proprietà possono essere utilizzate per proteggere e sproteggere i diagrammi Microsoft Visio.

In Microsoft Visio proteggi i documenti in questo modo:

1. Apri uno diagram in Microsoft Visio.
1. Apre la finestra Esplora Disegno.
1.  Fare clic con il tasto destro su diagram e selezionare**Proteggi documento** dal menù.
1. Nella finestra Proteggi documento, seleziona o deseleziona le opzioni per bloccare o sbloccare diversi elementi diagram.
1.  Clic**OK**.

**Si prega di vedere come possiamo controllare o cancellare le opzioni manualmente.** 

Usa il codice qui sotto nella tua applicazione per eseguire le stesse attività - blocca e sblocca diversi elementi del tuo diagram - usando Aspose.Diagram per Python tramite Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Modifica la protezione della forma Visio**
La protezione delle forme Visio consente agli utenti di bloccare aspetti specifici delle forme. Gli aspetti delle forme che possono essere bloccati tramite la protezione delle forme includono larghezza, altezza, posizione x, posizione y, rotazione e altro. Gli sviluppatori possono raggiungere questo obiettivo utilizzando Aspose.Diagram per Python tramite Java.

 Il**getBloccoAspetto()**, **getLockBegin()**, **getBloccoCalcWH()**, **getBloccoRitaglia()**, **getLockCustProp()**, **getLockDelete()**, **getBloccoFine()**, **getBloccoFormato()**, **getBloccoDaFormatoGruppo()**, **getBloccoGruppo()**, **getBloccoAltezza()**, **getBloccaSpostaX()**, **getBloccoSpostaY()**, **getBloccaRuota()**, **getBloccoSeleziona()**, **getLockTextEdit()**, **getBloccoTemaColori()**, **getLockThemeEffects()**, **getLockVtxEdit()** e**getLockWidth()** metodi esposti dal**Protezione** class supportano l'oggetto BoolValue. Questi metodi possono essere utilizzati per proteggere/sproteggere le forme.

In Visio, è necessario eseguire le seguenti azioni per proteggere qualsiasi forma:

1. Apri uno diagram in Microsoft Visio.
1. Seleziona una forma.
1.  Selezionare**Protezione** dal**Formato** menu (Visio 2007), o selezionare**Protezione** dal**Sviluppatore** menù (Visio 2010).
1.  Nel**Protezione** finestra, selezionare o deselezionare le opzioni per bloccare o sbloccare l'attributo della forma.
1.  Clic**OK**.

**Le opzioni di protezione di una forma, come si vede in Microsoft Visio** 

Usa il seguente codice nella tua applicazione Java per fare la stessa cosa (bloccare/sbloccare qualsiasi attributo di forma) usando Aspose.Diagram per Python tramite Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
