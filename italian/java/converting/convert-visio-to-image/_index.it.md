---
title:  Converti Visio in formati Immagini
linktitle: Converti Visio in immagini
type: docs
weight: 20
url: /it/java/convert-visio-to-image/
description: Questo argomento mostra come Aspose.Diagram consente di convertire Visio in vari formati di immagini. Converti Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM in immagini PNG, JPEG, BMP con poche righe di codice.
---
## **Esportazione di diagrammi in formati di file immagine**
 Questo articolo spiega come esportare un Microsoft Visio diagram in un'immagine utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizzare il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)class' per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato. L'immagine seguente mostra un file VSD che sta per essere salvato in formato PNG. È possibile utilizzare anche altri formati diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).
**Il file sorgente. Si noti che le etichette Freccia e Triangolo sono in grassetto.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/WOV36ek.png)

Per esportare un diagram in un'immagine:

- Creare un'istanza della classe Diagram.
- Chiama il metodo Save della classe Diagram e imposta il formato dell'immagine in cui desideri esportare. Il file dell'immagine di output ha l'aspetto del file originale.

**Il file PNG di output.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/WOV36ek.png)
### **Esempio di programmazione dell'esportazione in un file immagine**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

È anche possibile salvare una pagina particolare come immagine, invece dell'intero documento:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}