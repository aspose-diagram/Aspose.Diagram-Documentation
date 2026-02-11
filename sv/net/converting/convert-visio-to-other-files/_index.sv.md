---
title:  Konvertera Visio till andra format
linktitle:  Konvertera Visio till andra format
type: docs
weight: 40
url: /sv/net/convert-visio-to-other-files/
description: Det här ämnet visar hur du Aspose.Diagram tillåter att konvertera Visio till SVG,XPS,XML,XAML format. Konvertera VSD, VSS, VDW, VST, VSDX, VSSX, VSTX, VSDM, VSTM,0761123411 till 3061123411 kod,3011123411 till 3011123411 till 301123411 kod
---
## **Exportera till XML**
### **Exportera Microsoft Visio Ritning till PDF**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till PDF med C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToPDF.vsd");

MemoryStream pdfStream = new MemoryStream();
// Save diagram
diagram.Save(pdfStream, SaveFileFormat.PDF);

// Create a PDF file
FileStream pdfFileStream = new FileStream(dataDir + "ExportToPDF_out.pdf", FileMode.Create, FileAccess.Write);
pdfStream.WriteTo(pdfFileStream);
pdfFileStream.Close();

pdfStream.Close();

// Display Status.
System.Console.WriteLine("Conversion from vsd to pdf performed successfully.");

{{< /highlight >}}
```

 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XML med[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

- VDX definierar en XML diagram.
- VTX definierar en XML-mall.
- VSX definierar en XML-stencil.

 De[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' konstruktörer läser en diagram och Save-metoden används för att spara, eller exportera, en diagram i ett annat filformat. Kodavsnitten i den här artikeln visar hur du använder metoden Spara för att spara en Visio-fil till[VDX](https://docs.aspose.com/diagram/net/save-visio-document/), [VTX](https://docs.aspose.com/diagram/net/save-visio-document/) och[VSX](https://docs.aspose.com/diagram/net/save-visio-document/).

Bilden nedan visar diagram som exporteras i kodavsnitten nedan. Den exporterade filen visas före varje kodavsnitt.

|**A Microsoft Visio diagram på väg att exporteras.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_3.png)|

### **Exportera VSD till VDX**
VDX är ett schemabaserat XML-filformat som låter dig spara diagram i ett format som andra produkter än Microsoft Visio kan läsa. Det är ett användbart format för att överföra diagram mellan program och behålla redigerbara data.

Så här exporterar du ett VSD diagram till VDX:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VDX.

|**Den exporterade VDX-filen.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_4.png)|

### **Exportera från VSD till VSX**
VSX är ett XML-format för att definiera stenciler, de grundläggande objekten från vilka en diagram är uppbyggd. När en Visio-fil konverteras till VSX, exporteras endast schablonerna.

Så här exporterar du ett VSD diagram till VSX:

- Skapa en instans av klassen Diagram.
- Ring Diagram-klassens Spara-metod för att skriva Visio-ritningsfilen till VSX.
### **Exportera VSD till VTX**
TVX är en XML-representation av en mallfil och lagrar inställningarna för dokumentet.

Så här exporterar du ett VSD diagram till VTX:

1. Skapa en instans av klassen Diagram.
1. Ring diagram-klassens Spara-metod för att skriva Visio-ritningsfilen i formatet VTX.
### **Exportera Microsoft Visio Ritning till XML**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till XML med C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
            
/* 1. Exporting VSDX to VDX */
// Call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "ExportToXML.vsd");

// Save input VSD as VDX
diagram.Save(dataDir + "ExportToXML_out.vdx", SaveFileFormat.VDX);

/* 2. Exporting from VSD to VSX */
// Call the diagram constructor to load diagram from a VSD file
            
// Save input VSD as VSX
diagram.Save(dataDir + "ExportToXML_out.vsx", SaveFileFormat.VSX);
            
/* 3. Export VSD to VTX */
// Save input VSD as VTX
diagram.Save(dataDir + "ExportToXML_out.vtx", SaveFileFormat.VTX);

{{< /highlight >}}
```

## **Exportera till XPS**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XPS med[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.
 Använd[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

Kodavsnitten i den här artikeln tar diagram nedan som indata. Du kan också använda andra diagram-format (VSS, VSSX, VSSM, VDX, VST, VSTX, VDX, 0761803713) eller 4.

|**Källdokumentet.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_5.png)|


Så här exporterar du VSD diagram till XPS:

1. Skapa en instans av klassen Diagram.
1. Ring Diagram-klassens Spara-metod och ställ in XPS som utdataformat.
### **Exportera Microsoft Visio Ritning till XPS**
Kodexemplen visar hur man exporterar Microsoft Visio Ritning till XPS med C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Open a VSD file
Diagram diagram = new Diagram(dataDir + "LayOutShapesInCompactTreeStyle.vdx");

// Save diagram to an XPS format
diagram.Save(dataDir + "ExportToXPS_out.xps", SaveFileFormat.XPS);

{{< /highlight >}}
```

## **Exportera ett Diagram till SVG**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till SVG (Scalable Vector Graphics) med[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Använd[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

För att exportera VSD diagram till SVG, utför följande steg:

1. Skapa en instans av klassen Diagram.
1. Anropa klassens spara-metod och ange SVG som exportformat.
### **Exportera Microsoft Visio Ritning till SVG**
Kodexemplen visar hur man exporterar en diagram till SVG med C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Call the diagram constructor to load a VSD diagram
Diagram diagram = new Diagram(dataDir + "ExportToSVG.vsd");

// Save SVG Output file
diagram.Save(dataDir + "Output.svg", SaveFileFormat.SVG);

{{< /highlight >}}
```
## **Exportera till SWF**
 Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till SWF med[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) API.

 Använd[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)klassens konstruktörer för att läsa diagram-filerna och sedan Diagram-klassens Spara-metoden för att exportera formatet diagram till SWF. The image below shows the input VSD file that the code renders to SWF. You can use other diagram formats (VSS, VSSX, VSSM, VDW, VDX, VST, VSTX, VSTM, VDX, VTX or VSX) as well.

|**Ingång diagram.**|
|:- |
|![todo:image_alt_text](how-to-convert-a-visio-diagram_7.png)|

Efter koden finns en bild av utgången.

För att exportera VSD diagram till SWF::

- Skapa en instans av klassen Diagram.
- Ring Diagram-klassens Spara-metod och ange SWF-format för att exportera din diagram till SWF.
### **Inbyggd Viewer-programmeringsexempel**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ActvDir.vsd");
// Save diagram
diagram.Save(dataDir + "Output_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
### **Utan Viewer-programmeringsexempel**
SWF-filen som skapas av dessa kodavsnitt inkluderar en SWF-visare. Uteslut visningsprogrammet SWF från filen med följande kod.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Diagrams();

// Instantiate Diagram Object and open VSD file
Diagram diagram = new Diagram(dataDir + "ExportToSWFWithoutViewer.vsd");

// Instantiate the Save Options
SWFSaveOptions options = new SWFSaveOptions();

// Set Save format as SWF
options.SaveFormat = SaveFileFormat.SWF;

// Exclude the embedded viewer
options.ViewerIncluded = false;

// Save the resultant SWF file
diagram.Save(dataDir + "ExportToSWFWithoutViewer_out.swf", SaveFileFormat.SWF);

{{< /highlight >}}
```
## **Exportera ett Diagram till XAML**
Den här artikeln förklarar hur du exporterar en Microsoft Visio diagram till XAML (Extensible Application Markup Language) med[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) API.

 Använd[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class' konstruktor för att läsa diagram-filerna och Spara-metoden för att exportera diagram till valfritt bildformat som stöds.

Så här exporterar du ett VSD diagram till XAML:

1. Skapa en instans av klassen Diagram.
1. Anropa klassens spara-metod och ange XAML som exportformat.
### **Exportera Microsoft Visio Ritning till XAML**
Kodexemplet visar hur man exporterar en diagram till XAML med C#.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();
// Load diagram
Diagram diagram = new Diagram(dataDir + "ExportToXAML.vsd");
// Save diagram
diagram.Save(dataDir + "ExportToXAML_out.xaml", SaveFileFormat.XAML);

{{< /highlight >}}
```
## **Konvertera Visio Rita med selektiva former**
Med hjälp av Aspose.Diagram API kan utvecklare välja en grupp former för att konvertera en Visio-ritning till vilket annat format som helst. RenderingSaveOptions-klassen erbjuder en Shapes-medlem för att underhålla gruppen av former. Varje sparalternativklass är den utökade formen av RenderingSaveOptions-klassen.

Så här exporterar du en Visio-ritning med selektiva former:

1. Skapa en instans av klassen Diagram.
1. Skapa en instans av en SaveOption-klass för att ange inställningar som beskrivs här:[Ange Visio Spara alternativ](https://docs.aspose.com/diagram/net/save-visio-document/#specifying-visio-save-options)
1. Anropa metoden Spara för klassobjektet Diagram och skicka spara alternativ klassobjekt som parameter.
### **Konvertera Visio Ritning med selektiva former Programmeringsexempel**
Kodexemplet visar hur man exporterar en ritning med selektiva Visio-former.

```
{{< highlight "csharp" >}}
// the path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// call the diagram constructor to load diagram from a VSD file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// create an instance SVG save options class
SVGSaveOptions options = new SVGSaveOptions();
ShapeCollection shapes = options.Shapes;

// get shapes by page index and shape ID, and then add in the shape collection object
shapes.Add(diagram.Pages[0].Shapes.GetShape(1));
shapes.Add(diagram.Pages[0].Shapes.GetShape(2));

// save Visio drawing
diagram.Save(dataDir + "SelectiveShapes_out.svg", options);
{{< /highlight >}}
```