---
title:  Converti Visio in formati Immagini
linktitle: Converti Visio in immagini
type: docs
weight: 20
url: /it/java/convert-visio-to-image/
description: This topic show you how to Aspose.Diagram allows to convert Visio to various images formats. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,VSSM to PNG, JPEG, BMP images with a few lines of code.
---
## **Esportazione di diagrammi in formati di file immagine**
 Questo articolo spiega come esportare un Microsoft Visio diagram in un'immagine utilizzando[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) API.

 Utilizzare il[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class' constructor to read the diagram files and the Save method to export the diagram to any supported image format.The image below shows a VSD file about to be saved to PNG format. You can use other diagram formats (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.
**Il file sorgente. Si noti che le etichette Freccia e Triangolo sono in grassetto.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/WOV36ek.png)

Per esportare un diagram in un'immagine:

- Creare un'istanza della classe Diagram.
- Chiama il metodo Save della classe Diagram e imposta il formato dell'immagine in cui desideri esportare. Il file dell'immagine di output ha l'aspetto del file originale.

**Il file di output PNG.**

![cose da fare:immagine_alt_testo](http://i.imgur.com/WOV36ek.png)
### **Esempio di programmazione dell'esportazione in un file immagine**
{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportToImage-ExportToImage.java" >}}

È anche possibile salvare una pagina particolare come immagine, invece dell'intero documento:

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-LoadSaveConvert-ExportPageToImage-ExportPageToImage.java" >}}