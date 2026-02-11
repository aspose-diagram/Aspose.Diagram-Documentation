---
title: Hantera dokumentegenskaper
linktitle: Dokument egenskaper
type: docs
weight: 80
url: /sv/java/document-properties/
aliases: [/java/document-properties/]
description: Hantera dokumentegenskaper för visio-filer.
---
## **Introduktion**

Microsoft Visio ger möjlighet att lägga till egenskaper till visio-filer. Dessa dokumentegenskaper ger användbar information och är indelade i två kategorier enligt beskrivningen nedan.

- Systemdefinierade (inbyggda) egenskaper: Inbyggda egenskaper innehåller allmän information om dokumentet som dokumenttitel, författarens namn, dokumentstatistik och så vidare.
- Användardefinierade (anpassade) egenskaper: Anpassade egenskaper definierade av slutanvändaren i form av namn-värdepar.

{{% alert color="primary" %}}

Den viktigaste punkten att veta om inbyggda och anpassade egenskaper är att inbyggda egenskaper kan nås och ändras, men inte skapas eller tas bort. Däremot kan anpassade egenskaper skapas och hanteras.

{{% /alert %}}

## **Hantera dokumentegenskaper med Microsoft Visio**

 Microsoft Visio låter dig hantera dokumentegenskaperna för Visio-filerna på ett WYSIWYG-sätt. Följ stegen nedan för att öppna**Egenskaper** dialogrutan på Visio 2016.

1.  Från**Fil** menyn, välj**Info**.

|**Välj infomeny**|
|:- |
|![todo:image_alt_text](managing-document-properties_1.png)|
1.  Klicka på**Egenskaper** rubrik och välj "Avancerade egenskaper".

|**Klicka på Avancerat val av egenskaper**|
|:- |
|![todo:image_alt_text](managing-document-properties_2.png)|
1. Hantera filens dokumentegenskaper.

|**Egenskapsdialog**|
|:- |
|![todo:image_alt_text](managing-document-properties_3.png)|
I dialogrutan Egenskaper finns det olika flikar, som Allmänt, Sammanfattning, Statistik, Innehåll och Tull. Varje flik hjälper till att konfigurera olika typer av information relaterad till filen. Fliken Anpassad används för att hantera anpassade egenskaper.

## **Arbeta med dokumentegenskaper med Aspose.Diagram**

Utvecklare kan hantera dokumentegenskaperna dynamiskt med hjälp av Aspose.Diagram API:er. Den här funktionen hjälper utvecklarna att lagra användbar information tillsammans med filen, som när filen togs emot, bearbetades, tidsstämplad och så vidare.

{{% alert color="primary" %}}

Aspose.Diagram for Java skriver direkt informationen om API och versionsnummer i utdatadokument.

Observera att du inte kan instruera Aspose.Diagram for Java att ändra eller ta bort denna information från utdatadokument.

{{% /alert %}}

### **Åtkomst till dokumentegenskaper**

 Aspose.Diagram API:er stöder båda typerna av dokumentegenskaper, inbyggda och anpassade. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) klass representerar en Visio-fil och, liksom en visio-fil,[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) klass kan innehålla flera sidor, var och en representerad av[**Sida**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) klass medan samlingen av sidor representeras av[**Sidsamling**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection)klass.

 Använd[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)för att komma åt filens dokumentegenskaper enligt beskrivningen nedan.

- För att komma åt inbyggda dokumentegenskaper, använd[**diagram.DocumentProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/documentproperties).
-  För att komma åt anpassade dokumentegenskaper, använd[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/CustomPropCollection).


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


### **Lägga till eller ta bort anpassade dokumentegenskaper**

Som vi har beskrivit tidigare i början av detta ämne kan utvecklare inte lägga till eller ta bort inbyggda egenskaper eftersom dessa egenskaper är systemdefinierade men det är möjligt att lägga till eller ta bort anpassade egenskaper eftersom dessa är användardefinierade.

### **Lägga till anpassade egenskaper**

 Aspose.Diagram API:er har avslöjat[**Lägg till**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#add(com.aspose.diagram.CustomProp) ) metod för[**CustomPropCollection**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection)klass för att lägga till anpassade egenskaper till samlingen.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}


### **Ta bort anpassade egenskaper**

 För att ta bort anpassade egenskaper med Aspose.Diagram, ring[**CustomPropCollection.Remove**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#remove(com.aspose.diagram.CustomProp)) och skicka namnet på dokumentegenskapen som ska tas bort.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(DetectFormatfromInputStream.class);

// Open the stream. Read only access to load a Visio diagram.
String stream = new String(dataDir + "Drawing1.vsdx");
// detect file format using an input stream
FileFormatInfo info = FileFormatUtil.detectFileFormat(stream);

// get the detected file format
System.out.println("The spreadsheet format is: " + info.getFileFormatType());

{{< /highlight >}}

