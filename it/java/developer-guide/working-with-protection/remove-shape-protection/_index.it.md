---
title: Rimuovi la protezione della forma
type: docs
weight: 20
url: /it/java/remove-shape-protection/
description: Questa sezione spiega come rimuovere la protezione della forma utilizzando Aspose.Diagram.
---
## **Rimuovere la protezione della forma Visio**
 La protezione delle forme Visio consente agli utenti di bloccare aspetti specifici delle forme. Gli aspetti delle forme che possono essere bloccati tramite la protezione delle forme includono larghezza, altezza, posizione x, posizione y, rotazione e altro. Gli sviluppatori possono raggiungere questo obiettivo utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).
### **Modifica la protezione della forma Visio**
**LockAspect**, **LockBegin**, **LockCalc WH**, **LockCrop**, **LockCustProp**, **BloccaElimina**, **LockEnd**, **BloccaFormat**, **LockFromGroupFormat**, **Gruppo di blocco**, **LockHeight**, **LockMoveX**, **LockMoveY**, **Blocca Ruota**, **BloccaSeleziona**, **LockTextModifica**, **LockThemeColors**, **LockThemeEffects**, **LockVtxModifica** e**LockWidth** proprietà esposte da[**Protezione**](https://reference.aspose.com/diagram/java/com.aspose.diagram/protection) classe sostenere il**Aspose.Diagram.BoolValue** oggetto. Queste proprietà possono essere utilizzate per proteggere e rimuovere la protezione delle forme.

In Microsoft Office Visio, l'utente può eseguire le seguenti azioni per proteggere qualsiasi forma:

- Aperto diagram in Microsoft Office Visio
- Seleziona qualsiasi forma
- Selezionare 'Protezione' dal menu 'Formato' se si utilizza Visio 2007 o selezionare 'Protezione' dal menu 'Sviluppatore' se si utilizza Visio 2010
- Nella finestra "Protezione", deseleziona qualsiasi casella di testo per sbloccare qualsiasi attributo della forma
- Premere OK'
### **Rimuovi l'esempio di programmazione di Shape Protection**
Usa il seguente codice nella tua applicazione Java per fare la stessa cosa (sbloccare qualsiasi attributo di forma) usando Aspose.Diagram for Java.


{{< highlight java >}}
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
shape.getProtection().getLockAspect().setValue(BOOL.FALSE);
shape.getProtection().getLockBegin().setValue(BOOL.FALSE);
shape.getProtection().getLockCalcWH().setValue(BOOL.FALSE);
shape.getProtection().getLockCrop().setValue(BOOL.FALSE);
shape.getProtection().getLockCustProp().setValue(BOOL.FALSE);
shape.getProtection().getLockDelete().setValue(BOOL.FALSE);
shape.getProtection().getLockEnd().setValue(BOOL.FALSE);
shape.getProtection().getLockFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockFromGroupFormat().setValue(BOOL.FALSE);
shape.getProtection().getLockGroup().setValue(BOOL.FALSE);
shape.getProtection().getLockHeight().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveX().setValue(BOOL.FALSE);
shape.getProtection().getLockMoveY().setValue(BOOL.FALSE);
shape.getProtection().getLockRotate().setValue(BOOL.FALSE);
shape.getProtection().getLockSelect().setValue(BOOL.FALSE);
shape.getProtection().getLockTextEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeColors().setValue(BOOL.FALSE);
shape.getProtection().getLockThemeEffects().setValue(BOOL.FALSE);
shape.getProtection().getLockVtxEdit().setValue(BOOL.FALSE);
shape.getProtection().getLockWidth().setValue(BOOL.FALSE);
        
// save diagram
diagram.save(dataDir + "VisioShapeProtection_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}


