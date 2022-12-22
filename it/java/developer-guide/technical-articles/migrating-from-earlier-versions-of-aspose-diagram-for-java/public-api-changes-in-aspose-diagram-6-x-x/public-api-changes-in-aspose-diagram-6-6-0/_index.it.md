---
title: Pubblico API Modifiche Aspose.Diagram 6.6.0
type: docs
weight: 30
url: /it/java/public-api-changes-in-aspose-diagram-6-6-0/
---
{{% alert color="primary" %}} 

Questo documento descrive le modifiche allo Aspose.Diagram API dalla versione 6.3.0 alla 6.6.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.Diagram.

{{% /alert %}} 
### **Aggiunge i formati VSDM, VSSM e VSTM nella classe LoadFileFormat**
Questa versione aggiunge il supporto per la lettura dei formati Visio abilitati per le macro.
### **Aggiunge i formati VSDM, VSSM e VSTM nella classe SaveFileFormat**
Questa versione aggiunge il supporto per la scrittura di formati Visio abilitati per le macro.
### **Modifica il codice del modulo VBA in Visio Diagram**
Abbiamo aggiunto le classi Vba, VbaProject e VbaModule. Queste classi aiutano a ottenere il controllo sul progetto VBA. Utilizzando questa nuova versione 6.6.0 o successiva, gli sviluppatori possono estrarre e modificare il codice del modulo VBA. Si prega di controllare questo esempio di codice:

**Java**

{{< highlight "java" >}}

 // carica un Visio diagram esistente

InputStream input = new FileInputStream("c:\\temp\\macro.vsdm");

Diagram diagram = nuovo Diagram(input);

// estrae il progetto VBA

VbaProject v = diagram.getVbaProject();

// Itera attraverso i moduli e modifica il codice macro VBA

per (int i=0;i< diagram.getVbaProject().getModules().getCount();i++)

{

    VbaModule module =  diagram.getVbaProject().getModules().get(i);

    String code = module.getCodes();

    if (code.contains("This is test message."))

        code = code.replace("This is test message.", "This is Aspose.Diagram message.");

    module.setCodes (code);

}

// save the Visio diagram

diagram.Save("c:\\temp\\out.vssm", SaveFileFormat.VSSM);

{{< /highlight >}}
### **Aggiunge un metodo getImageData nella classe ForeignData**
Rappresenta un'immagine di un oggetto ole come un array di byte. Oltre a questo, abbiamo anche migliorato la manipolazione degli oggetti OLE. Gli sviluppatori ora possono anche sostituire un oggetto OLE nel Visio diagram. Controlla questo esempio di codice:

**Java**

{{< highlight "java" >}}

 String DirPath = "c:\\temp\\";

// load a Visio diagram

Diagram diagram = new Diagram(DirPath + "Drawing1.vsdx");

// get page of the Visio diagram by name

Page page = diagram.getPages().getPage("Page-1");

// get shape of the Visio diagram by ID

Shape OLE_Shape = page.getShapes().getShape(2);

// filter shapes by type Foreign

if (OLE_Shape.getType() == TypeValue.FOREIGN)

{

    if (OLE_Shape.getForeignData().getForeignType() == ForeignType.OBJECT)

    {

    	ByteArrayInputStream Ole_stream = new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData());

        // get format of the OLE file object

        com.aspose.words.FileFormatInfo info = com.aspose.words.FileFormatUtil.detectFileFormat(Ole_stream);

        if (info.getLoadFormat() == com.aspose.words.LoadFormat.DOC || info.getLoadFormat() == com.aspose.words.LoadFormat.DOCX)

        {

            // modify an OLE object

            com.aspose.words.Document doc = new com.aspose.words.Document(new ByteArrayInputStream(OLE_Shape.getForeignData().getObjectData()));

    	    doc.getRange().replace("testing", "Aspose", false, true);

            ByteArrayOutputStream outStream = new ByteArrayOutputStream();

            doc.save(outStream, com.aspose.words.SaveFormat.DOCX);

            // seve an OLE object

            OLE_Shape.getForeignData().setObjectData(outStream.toByteArray());

        }

    }

}

// save Visio diagram

diagram.save(DirPath + "modified.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
