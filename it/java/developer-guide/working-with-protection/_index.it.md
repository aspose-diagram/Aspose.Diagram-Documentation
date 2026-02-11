---
title: Lavorare con la protezione
type: docs
weight: 90
url: /it/java/working-with-protection/
---
## **Set Protezione del Visio Diagram**
 La protezione dei diagrammi consente agli utenti di bloccare sfondi, master (stencil), forme e stili in modo che non possano essere modificati. Ciò è utile per proteggere gli stili aziendali, ad esempio, e garantire un aspetto coerente in una serie di diagrammi. Gli sviluppatori possono raggiungere questo obiettivo utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Modifica protezione del Visio Diagram**
 I metodi getProtectBkgnds, getProtectMasters, getProtectShapes e getProtectStyles, esposti dal[Impostazioni documento](https://reference.aspose.com/diagram/java/com.aspose.diagram/DocumentSettings) class supporta l'oggetto com.aspose.diagram.BoolValue. Queste proprietà possono essere utilizzate per proteggere e sproteggere i diagrammi Microsoft Visio.

In Microsoft Visio proteggi i documenti in questo modo:

1. Apri uno diagram in Microsoft Visio.
1. Apre la finestra Esplora Disegno.
1.  Fare clic con il tasto destro su diagram e selezionare**Proteggi documento** dal menù.
1. Nella finestra Proteggi documento, seleziona o deseleziona le opzioni per bloccare o sbloccare diversi elementi diagram.
1.  Clic**OK**.

**Si prega di vedere come possiamo controllare o cancellare le opzioni manualmente.** 

![cose da fare:immagine_alt_testo](working-with-protection_1.png)

Usa il codice qui sotto in un'applicazione Java per eseguire le stesse attività – blocca e sblocca diversi elementi del tuo diagram – usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioDiagramProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");

diagram.getDocumentSettings().setProtectBkgnds(BOOL.TRUE);
diagram.getDocumentSettings().setProtectMasters(BOOL.TRUE);
diagram.getDocumentSettings().setProtectShapes(BOOL.TRUE);
diagram.getDocumentSettings().setProtectStyles(BOOL.TRUE);
// save diagram
diagram.save(dataDir + "VisioDiagramProtection_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
### **Modifica la protezione della forma Visio**
 La protezione delle forme Visio consente agli utenti di bloccare aspetti specifici delle forme. Gli aspetti delle forme che possono essere bloccati tramite la protezione delle forme includono larghezza, altezza, posizione x, posizione y, rotazione e altro. Gli sviluppatori possono raggiungere questo obiettivo utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 Il**getBloccoAspetto()**, **getLockBegin()**, **getBloccoCalcWH()**, **getBloccoRitaglia()**, **getLockCustProp()**, **getLockDelete()**, **getBloccoFine()**, **getBloccoFormato()**, **getBloccoDaFormatoGruppo()**, **getBloccoGruppo()**, **getBloccoAltezza()**, **getBloccaSpostaX()**, **getBloccoSpostaY()**, **getBloccaRuota()**, **getBloccoSeleziona()**, **getLockTextEdit()**, **getBloccoTemaColori()**, **getLockThemeEffects()**, **getLockVtxEdit()** e**getLockWidth()** metodi esposti dal[Protezione](https://reference.aspose.com/diagram/java/com.aspose.diagram/Protection) class supporta l'oggetto com.aspose.diagram.BoolValue. Questi metodi possono essere utilizzati per proteggere/sproteggere le forme.

In Visio, è necessario eseguire le seguenti azioni per proteggere qualsiasi forma:

1. Apri uno diagram in Microsoft Visio.
1. Seleziona una forma.
1.  Selezionare**Protezione** dal**Formato** menu (Visio 2007), o selezionare**Protezione** dal**Sviluppatore** menù (Visio 2010).
1.  Nel**Protezione** finestra, selezionare o deselezionare le opzioni per bloccare o sbloccare l'attributo della forma.
1.  Clic**OK**.

**Le opzioni di protezione di una forma, come si vede in Microsoft Visio** 

![cose da fare:immagine_alt_testo](working-with-protection_2.png)

Usa il seguente codice nella tua applicazione Java per fare la stessa cosa (bloccare/sbloccare qualsiasi attributo di forma) usando Aspose.Diagram for Java.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(VisioShapeProtection.class);
//Load diagram
Diagram diagram = new Diagram(dataDir + "ProtectAndUnprotect.vsd");
// get page by name
Page page = diagram.getPages().getPage("Flow 1");
// get shape by ID
Shape shape = page.getShapes().getShape(1);

// set protections
shape.getProtection().getLockAspect().setValue(BOOL.TRUE);
shape.getProtection().getLockBegin().setValue(BOOL.TRUE);
shape.getProtection().getLockCalcWH().setValue(BOOL.TRUE);
shape.getProtection().getLockCrop().setValue(BOOL.TRUE);
shape.getProtection().getLockCustProp().setValue(BOOL.TRUE);
shape.getProtection().getLockDelete().setValue(BOOL.TRUE);
shape.getProtection().getLockEnd().setValue(BOOL.TRUE);
shape.getProtection().getLockFormat().setValue(BOOL.TRUE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.TRUE);
shape.getProtection().getLockGroup().setValue(BOOL.TRUE);
shape.getProtection().getLockHeight().setValue(BOOL.TRUE);
shape.getProtection().getLockMoveX().setValue(BOOL.TRUE);
shape.getProtection().getLockMoveY().setValue(BOOL.TRUE);
shape.getProtection().getLockRotate().setValue(BOOL.TRUE);
shape.getProtection().getLockSelect().setValue(BOOL.TRUE);
shape.getProtection().getLockTextEdit().setValue(BOOL.TRUE);
shape.getProtection().getLockThemeColors().setValue(BOOL.TRUE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.TRUE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.TRUE);
shape.getProtection().getLockWidth().setValue(BOOL.TRUE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vdx", SaveFileFormat.VDX);

{{< /highlight >}}
```
