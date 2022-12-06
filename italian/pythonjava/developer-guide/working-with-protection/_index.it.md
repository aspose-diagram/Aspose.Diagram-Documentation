---
title: Lavorare con la protezione
type: docs
weight: 90
url: /it/python-java/working-with-protection/
---
## **Set Protezione del Visio Diagram**
Protecting diagrams allow users to lock backgrounds, masters (stencils), shapes and styles so that they cannot be edited. This is useful for protecting corporate styles, for example, and ensure a consistent look across a set of diagrams. Developers can achieve this using Aspose.Diagram for Python via Java.

### **Modifica protezione del Visio Diagram**
I metodi getProtectBkgnds, getProtectMasters, getProtectShapes e getProtectStyles, esposti dalla classe DocumentSettings, supportano l'oggetto BoolValue. Queste proprietà possono essere utilizzate per proteggere e sproteggere i diagrammi Microsoft Visio.

In Microsoft Visio proteggi i documenti in questo modo:

1. Apri uno diagram in Microsoft Visio.
1. Apre la finestra Esplora Disegno.
1.  Fare clic con il tasto destro su diagram e selezionare**Proteggi documento** dal menù.
1. Nella finestra Proteggi documento, seleziona o deseleziona le opzioni per bloccare o sbloccare diversi elementi diagram.
1.  Clic**OK**.

**Si prega di vedere come possiamo controllare o cancellare le opzioni manualmente.** 

Use the code below in your application to perform the same tasks – lock and unlock different elements of your diagram – using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioDiagramProtection.py" >}}

### **Modifica la protezione della forma Visio**
Protecting Visio shapes allow users to lock specific aspects of shapes. Aspects of shapes that can be locked through shape protection include width, height, x-position, y-position, rotation and more. Developers can achieve this using Aspose.Diagram for Python via Java.

 Il**getBloccoAspetto()**, **getLockBegin()**, **getBloccoCalcWH()**, **getBloccoRitaglia()**, **getLockCustProp()**, **getLockDelete()**, **getBloccoFine()**, **getBloccoFormato()**, **getBloccoDaFormatoGruppo()**, **getBloccoGruppo()**, **getBloccoAltezza()**, **getBloccaSpostaX()**, **getBloccoSpostaY()**, **getBloccaRuota()**, **getBloccoSeleziona()**, **getLockTextEdit()**, **getBloccoTemaColori()**, **getLockThemeEffects()**, **getLockVtxEdit()** e**getLockWidth()** metodi esposti dal**Protezione** class supportano l'oggetto BoolValue. Questi metodi possono essere utilizzati per proteggere/sproteggere le forme.

In Visio, è necessario eseguire le seguenti azioni per proteggere qualsiasi forma:

1. Apri uno diagram in Microsoft Visio.
1. Seleziona una forma.
1.  Selezionare**Protezione** dal**Formato** menu (Visio 2007), o selezionare**Protezione** dal**Sviluppatore** menù (Visio 2010).
1.  Nel**Protezione** finestra, selezionare o deselezionare le opzioni per bloccare o sbloccare l'attributo della forma.
1.  Clic**OK**.

**Le opzioni di protezione di una forma, come si vede in Microsoft Visio** 

Use the following code in your Java application to do the same thing (lock/unlock any shape attribute) using Aspose.Diagram for Python via Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Protection-VisioShapeProtection.py" >}}
