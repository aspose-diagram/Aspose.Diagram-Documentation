---
title: Recuperar, obtener, copiar e insertar una página
type: docs
weight: 10
url: /es/net/retrieve-get-copy-and-insert-a-page/
description: Esta sección explica cómo insertar una página, copiar una página u obtener información de la página con Aspose.Diagram.
---
## **Recuperación de información de la página**
En Microsoft Visio, las páginas son páginas de primer plano o de fondo. Para obtener información de la página, por ejemplo, el ID de la página y el nombre de la página, primero establezca si una página es una página de fondo o de primer plano.

 los[Página](http://www.aspose.com/api/net/diagram/aspose.diagram/page)objeto representa el área de dibujo de una página de primer plano o una página de fondo. La propiedad Pages expuesta por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) La clase admite una colección de objetos Aspose.Diagram.Page. Esta propiedad se puede utilizar para recuperar información de la página.

Utilice la propiedad Page.Background para determinar si una página es una página de primer plano o de fondo.
### **Muestra de programación de información de la página de recuperación**
El siguiente fragmento de código recupera la información de las páginas de un diagram.


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

## **Obtenga la página Visio de un Diagram**
A veces, los desarrolladores necesitan obtener los detalles de la página del dibujo Visio. Aspose.Diagram tiene características que les ayudan a hacer esto.

 Aspose.Diagram for .NET ofrece la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase que representa un dibujo Visio. La propiedad Pages expuesta por la clase Diagram admite una colección de objetos Aspose.Diagram.Page. La clase PageCollection expone el método GetPage que se puede llamar para obtener el objeto Page.
### **Obtener un objeto de página Visio por ID**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetPage de la clase Diagram.Pages.

El siguiente ejemplo muestra cómo obtener un objeto de página por ID del dibujo Visio.
#### **Obtener objeto de página por ejemplo de programación de ID**

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

### **Obtener un objeto de página Visio por nombre**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetPage de la clase Diagram.Pages.
#### **Obtener objeto de página por nombre Ejemplo de programación**
El siguiente ejemplo muestra cómo obtener un objeto de página por nombre del dibujo Visio.


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

## **Copie una página Visio en otra Diagram**
Aspose.Diagram for .NET API permite a los desarrolladores copiar y agregar su contenido de Visio diagram a otro. Este tema de ayuda explica cómo realizar esta tarea.

 Aspose.Diagram for .NET API tiene el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase que representa un dibujo Visio. La propiedad Pages expuesta por la clase Diagram admite una colección de objetos Aspose.Diagram.Page. La clase PageCollection expone el método Add al que se puede llamar para agregar otro objeto Page.

Este ejemplo funciona de la siguiente manera:

1. Cree un nuevo objeto de la clase Diagram.
1. Cargue un Visio diagram existente en el objeto de clase Diagram.
1. Agregue todos los maestros del cargado Visio diagram
1. Obtenga el objeto de página del diagram cargado (que debe copiarse).
1. Establezca el nombre y la identificación del objeto de la página.
1. Eliminar página vacía del nuevo diagram (opcional).
1. Llame al método Add de la clase PageCollection.
1. Guarde el nuevo diagram en el almacenamiento de la computadora.
### **Copie una muestra de programación de página Visio**
El siguiente ejemplo de código muestra cómo copiar un objeto de página Visio en otro dibujo Visio.


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

## **Copie la página Visio a otra instancia de la página**
El método Copy de la clase Page toma una instancia de página para clonar.

**C#**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.Copy(diagram.Pages.GetPage("Page-1"));

{{< /highlight >}}
## **Insertar una página en blanco en un dibujo Visio**
[Aspose.Diagram for .NET](http://www.aspose.com/.net/diagram-component.aspx) puede insertar una nueva página en blanco en el dibujo Microsoft Office Visio. Este tema de ejemplo describe cómo hacerlo.

El método Add, expuesto por la colección Pages, permite a los desarrolladores agregar una nueva página en blanco en el Visio diagram. Se debe asignar el ID de la página.
### **Insertar una muestra de programación de página en blanco**
El siguiente fragmento de código inserta una página en blanco en el dibujo Visio:


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

## **Mover la posición de la página en el dibujo Visio**
Aspose.Diagram for .NET API puede mover la posición de la página en el dibujo Visio. El método MoveTo, expuesto por la clase Page, ayuda a los desarrolladores a mover la posición de la página.
### **Mover posición de página Ejemplo de programación**
El miembro MoveTo toma el índice de la página de destino como parámetro para mover la posición de la página en el dibujo Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.MoveTo(2);

diagram.Save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
