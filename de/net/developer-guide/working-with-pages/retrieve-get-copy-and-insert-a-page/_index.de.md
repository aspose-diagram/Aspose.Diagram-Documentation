---
title: Abrufen, Abrufen, Kopieren und Einfügen einer Seite
type: docs
weight: 10
url: /de/net/retrieve-get-copy-and-insert-a-page/
description: In diesem Abschnitt wird erläutert, wie Sie mit Aspose.Diagram eine Seite einfügen, eine Seite kopieren oder Seiteninformationen abrufen.
---
## **Abrufen von Seiteninformationen**
In Microsoft Visio sind Seiten entweder Vorder- oder Hintergrundseiten. Um Seiteninformationen zu erhalten, z. B. Seiten-ID und Seitenname, stellen Sie zunächst fest, ob es sich bei einer Seite um eine Hintergrund- oder eine Vordergrundseite handelt.

 Das[Buchseite](http://www.aspose.com/api/net/diagram/aspose.diagram/page)Objekt stellt den Zeichenbereich einer Vordergrundseite oder einer Hintergrundseite dar. Die Pages-Eigenschaft, die von der[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) -Klasse unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten. Diese Eigenschaft kann verwendet werden, um Seiteninformationen abzurufen.

Verwenden Sie die Page.Background-Eigenschaft, um zu bestimmen, ob eine Seite eine Vorder- oder Hintergrundseite ist.
### **Programmierbeispiel zum Abrufen von Seiteninformationen**
Der folgende Codeabschnitt ruft die Seiteninformationen von diagram ab.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram vdxDiagram = new Diagram(dataDir + "RetrievePageInfo.vdx");

foreach (Aspose.Diagram.Page page in vdxDiagram.Pages)
{
    // Checks if current page is a background page
    if (page.Background == Aspose.Diagram.BOOL.True)
    {
        // Display information about the background page
        Console.WriteLine("Background Page ID : " + page.ID);
        Console.WriteLine("Background Page Name : " + page.Name);
    }
    else
    {
        // Display information about the foreground page
        Console.WriteLine("\nPage ID : " + page.ID);
        Console.WriteLine("Universal Name : " + page.NameU);
        Console.WriteLine("ID of the Background Page : " + page.BackPage);
    }
}

{{< /highlight >}}

## **Rufen Sie die Visio-Seite von einer Diagram ab**
Manchmal müssen Entwickler die Seitendetails einer Visio-Zeichnung abrufen. Aspose.Diagram hat Funktionen, die ihnen dabei helfen.

 Aspose.Diagram for .NET bietet die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Die Pages-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten. Die PageCollection-Klasse macht die GetPage-Methode verfügbar, die zum Abrufen des Page-Objekts aufgerufen werden kann.
### **Abrufen eines Visio-Seitenobjekts nach ID**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetPage-Methode der Diagram.Pages-Klasse auf.

Das folgende Beispiel zeigt, wie ein Seitenobjekt anhand der ID aus der Zeichnung Visio abgerufen wird.
#### **Programmierbeispiel zum Abrufen des Seitenobjekts nach ID**

{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.Pages.GetPage(pageid);

{{< /highlight >}}

### **Abrufen eines Visio-Seitenobjekts nach Name**
Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein Objekt der Klasse Diagram.
1. Rufen Sie die GetPage-Methode der Diagram.Pages-Klasse auf.
#### **Programmierbeispiel zum Abrufen des Seitenobjekts nach Namen**
Das folgende Beispiel zeigt, wie ein Seitenobjekt anhand des Namens aus der Zeichnung Visio abgerufen wird.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
string pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.Pages.GetPage(pageName);

{{< /highlight >}}

## **Kopieren Sie eine Visio-Seite in eine andere Diagram-Seite**
Aspose.Diagram for .NET API ermöglicht es Entwicklern, den Inhalt von einer Visio diagram zu einer anderen zu kopieren und hinzuzufügen. In diesem Hilfethema wird erläutert, wie Sie diese Aufgabe ausführen.

 Aspose.Diagram for .NET API hat die[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) Klasse, die eine Visio-Zeichnung darstellt. Die Pages-Eigenschaft, die von der Diagram-Klasse verfügbar gemacht wird, unterstützt eine Sammlung von Aspose.Diagram.Page-Objekten. Die PageCollection-Klasse macht die Add-Methode verfügbar, die aufgerufen werden kann, um ein weiteres Page-Objekt hinzuzufügen.

Dieses Beispiel funktioniert wie folgt:

1. Erstellen Sie ein neues Objekt der Klasse Diagram.
1. Laden Sie ein vorhandenes Visio diagram in das Klassenobjekt Diagram.
1. Fügen Sie alle Master aus dem geladenen Visio diagram hinzu
1. Holen Sie sich das Seitenobjekt aus dem geladenen diagram (das kopiert werden muss).
1. Legen Sie den Namen und die ID des Seitenobjekts fest.
1. Leerseite der neuen diagram entfernen (optional).
1. Rufen Sie die Add-Methode der PageCollection-Klasse auf.
1. Speichern Sie die neue diagram im Computerspeicher.
### **Kopieren Sie ein Programmierbeispiel für die Seite Visio**
Das folgende Codebeispiel zeigt, wie Sie ein Visio-Seitenobjekt in eine andere Visio-Zeichnung kopieren.


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Initialize the new visio diagram
Diagram NewDigram = new Diagram();

// Load source diagram
Diagram dgm = new Diagram(dataDir + "Drawing1.vsdx");
// Add all masters from the source Visio diagram
foreach (Master master in dgm.Masters)
    NewDigram.Masters.Add(master);

// Get page object
Aspose.Diagram.Page SrcPage = dgm.Pages.GetPage("Page-1");
// Set name
SrcPage.Name = "new page";

// It calculates max page id
int max = 0;
if (NewDigram.Pages.Count != 0)
    max = NewDigram.Pages[0].ID;

for (int i = 1; i < NewDigram.Pages.Count; i++)
{
    if (max < NewDigram.Pages[i].ID)
        max = NewDigram.Pages[i].ID;
}
            
// Set max page ID 
int MaxPageId = max;
// Set page ID
SrcPage.ID = MaxPageId + 1;

// Add page from the source diagram
NewDigram.Pages.Add(SrcPage);
// Remove first empty page
NewDigram.Pages.Remove(NewDigram.Pages[0]);
// Save diagram
NewDigram.Save(dataDir + "CopyVisioPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Kopieren Sie die Seite Visio in eine andere Seiteninstanz**
Die Copy-Methode der Page-Klasse nimmt eine Seiteninstanz zum Klonen.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Einfügen einer leeren Seite in eine Visio-Zeichnung**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) kann eine neue leere Seite in die Zeichnung Microsoft Office Visio einfügen. In diesem Beispielthema wird beschrieben, wie Sie dies tun.

Die Add-Methode, die von der Pages-Auflistung bereitgestellt wird, ermöglicht es Entwicklern, eine neue leere Seite in Visio diagram hinzuzufügen. Die Seiten-ID sollte zugewiesen werden.
### **Programmierbeispiel für eine leere Seite einfügen**
Der folgende Codeabschnitt fügt eine leere Seite in die Zeichnung Visio ein:


{{< highlight csharp >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_VisioPages();

// Load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// It calculates max page id
int max = 0;
if (diagram.Pages.Count != 0)
    max = diagram.Pages[0].ID;

for (int i = 1; i < diagram.Pages.Count; i++)
{
    if (max < diagram.Pages[i].ID)
        max = diagram.Pages[i].ID;
}

// Set max page ID
int MaxPageId = max;

// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.Name = "new page";
// Set page ID
newPage.ID = MaxPageId + 1;

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.Pages.Add(newPage);

// Save diagram
diagram.Save(dataDir + "InsertBlankPage_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Seitenposition in der Zeichnung Visio verschieben**
Aspose.Diagram for .NET API kann die Seitenposition in der Visio Zeichnung verschieben. Die MoveTo-Methode, die von der Page-Klasse verfügbar gemacht wird, hilft Entwicklern, die Seitenposition zu verschieben.
### **Verschieben der Seitenposition Programmierbeispiel**
Das MoveTo-Member verwendet den Index der Zielseite als Parameter, um die Position der Seite in der Zeichnung Visio zu verschieben:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
