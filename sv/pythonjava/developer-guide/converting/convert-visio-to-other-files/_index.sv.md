---
title:  Konvertera Visio till andra format
linktitle:  Konvertera Visio till andra format
type: docs
weight: 40
url: /sv/python-java/convert-visio-to-other-files/
description: This topic show you how to convert Visio to SVG,XPS,XML,XAML formats using Aspose.Diagram for Python via Java. Convert VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM, VSSM to SVG,XPS,XML ,XAML med några rader kod.
---
**[A Microsoft Visio diagram som ska exporteras.](ExportToXML.vsd)**

## **Exporterar till XML**
Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XML med Aspose.Diagram för Python via Java.

- VDX definierar en XML diagram.
- VTX definierar en XML-mall.
- VSX definierar en XML-stencil.

Diagram-klassens konstruktörer läser ett diagram och Save-metoden används för att spara, eller exportera, en diagram i ett annat filformat. Kodavsnitten i den här artikeln visar hur du använder metoden Spara för att spara en Visio-fil i formaten VDX, VTX och VSX.

### **Exporterar VSD till VDX**
VDX är ett schemabaserat XML-filformat som låter dig spara diagram i ett format som andra produkter än Microsoft Visio kan läsa. Det är ett användbart format för att överföra diagram mellan program och behålla redigerbara data.

Så här exporterar du ett VSD diagram till VDX:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VDX.

### **Exporterar från VSD till VSX**
VSX är ett XML-format för att definiera stenciler, de grundläggande objekten från vilka en diagram är uppbyggd. När en Visio-fil konverteras till VSX, exporteras endast schablonerna.

Så här exporterar du ett VSD diagram till VSX:

- Skapa en instans av klassen Diagram.
- Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VSX.

Bilden nedan visar utdatafilen VSX. Observera att schablonerna som används i diagram, inte själva diagram, exporteras.

### **Exportera VSD till VTX**
TVX är en XML-representation av en mallfil och lagrar inställningarna för dokumentet.

Så här exporterar du ett VSD diagram till VTX:

1. Skapa en instans av klassen Diagram.
1. Ring diagram-klassens Spara-metod för att skriva Visio-ritningsfilen i formatet VTX.

Bilden nedan visar utdatafilen VTX.

### **Exportera till XML-programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXML.py" >}}

## **Exporterar till XPS**
Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XPS med Aspose.Diagram för Python via Java.
Använd Diagram-klassens konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

Kodavsnitten i den här artikeln tar diagram nedan som indata. Du kan också använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VSTM, VDX, 0716188181 eller 38161).

Så här exporterar du VSD diagram till XPS:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram-klassens Spara-metod och ställ in XPS som utdataformat.

Bilden nedan visar utdata-XPS-filen.

### **Exportera till XPS-programmeringsexempel**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXPS.py" >}}

## **Exporterar en Diagram till SVG**
Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till SVG (Scalable Vector Graphics) med Aspose.Diagram för Python via Java.

Använd Diagram-klassens konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

För att exportera VSD diagram till SVG, utför följande steg:

1. Skapa en instans av klassen Diagram.
1. Anropa klassens spara-metod och ange SVG som exportformat.

### **Exporterar Diagram till SVG-programmeringsexempel**
Kodexemplen visar hur man exporterar en diagram till SVG med Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToSVG.py" >}}

## **Exporterar en Diagram till XAML**
Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XAML (Extensible Application Markup Language) med Aspose.Diagram för Python via Java.

Använd Diagram-klassens konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

Så här exporterar du ett VSD diagram till XAML:

1. Skapa en instans av klassen Diagram.
1. Anropa klassens spara-metod och ange XAML som exportformat.

### **Exportera till XAML-programmeringsexempel**
Kodexemplet visar hur man exporterar en diagram till XAML med Java.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ExportToXAML.py" >}}

## **Konvertera Visio Rita med selektiva former**
Med hjälp av Aspose.Diagram API kan utvecklare välja en grupp former för att konvertera en Visio-ritning till vilket annat format som helst. RenderingSaveOptions-klassen erbjuder en Shapes-medlem för att underhålla gruppen av former. Varje sparalternativklass är den utökade formen av RenderingSaveOptions-klassen.

Så här exporterar du en Visio-ritning med selektiva former:

1. Skapa en instans av klassen Diagram.
1. Skapa en instans av valfri SaveOption-klass för att ange inställningar som berättade
1. Anrop sparmetoden för klassobjektet Diagram och skicka spara alternativ klassobjekt som parameter.

### **Konvertera Visio Ritning med selektiva former Programmeringsexempel**
Kodexemplet visar hur man exporterar en ritning med selektiva Visio-former.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-LoadSaveConvert-ConvertVisioWithSelectiveShapes.py" >}}