---
title:  Converti Visio in formati Immagini
linktitle: Converti Visio in immagini
type: docs
weight: 20
url: /it/python-java/convert-visio-to-image/
description: This topic show you how to convert Visio to various images formats using Aspose.Diagram for Python via Java. Convert Visio,VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to PNG, JPEG, BMP images with a poche righe di codice.
---
## **Esportazione di diagrammi in formati di file immagine**
Questo articolo spiega come esportare un Microsoft Visio diagram in un'immagine utilizzando Aspose.Diagram per Python tramite Java.

Utilizzare il costruttore della classe Diagram per leggere i file diagram e il metodo Save per esportare diagram in qualsiasi formato di immagine supportato. L'immagine seguente mostra un file VSD che sta per essere salvato in formato PNG. È possibile utilizzare anche altri formati diagram (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, VTX o VSX).

**[Il file VSD di esempio.](ExportToImage.vsd)**

Per esportare un diagram in un'immagine:

- Creare un'istanza della classe Diagram.
- Chiama il metodo Save della classe Diagram e imposta il formato dell'immagine in cui desideri esportare. Il file dell'immagine di output ha l'aspetto del file originale.

**Il file PNG di output.**

![cose da fare:immagine_alt_testo](ExportToImage.png)
### **Esempio di programmazione dell'esportazione in un file immagine**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToImage.py" >}}

È anche possibile salvare una pagina particolare come immagine, invece dell'intero documento:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportPageToImage.py" >}}