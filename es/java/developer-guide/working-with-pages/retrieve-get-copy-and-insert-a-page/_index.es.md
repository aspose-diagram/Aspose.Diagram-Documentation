---
title: Recuperar, obtener, copiar e insertar una página
type: docs
weight: 10
url: /es/java/retrieve-get-copy-and-insert-a-page/
---
## **Recuperación de información de la página**
En Microsoft Visio, las páginas son páginas de primer plano o de fondo. Para obtener información de la página, por ejemplo, el ID de la página y el nombre de la página, primero establezca si una página es una página de fondo o de primer plano.

 los[Página](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page)objeto representa el área de dibujo de una página de primer plano o una página de fondo. La propiedad Pages expuesta por el[Diagram](https://reference.aspose.com/diagram/java) La clase admite una colección de objetos Aspose.Diagram.Page. Esta propiedad se puede utilizar para recuperar información de la página.

Utilice la propiedad Page.Background para determinar si una página es una página de primer plano o de fondo.

La siguiente imagen muestra el resultado de los fragmentos de código de este artículo.

**Una consola que muestra la salida.** 

![todo:imagen_alternativa_texto](retrieve-get-copy-and-insert-a-page_1.png)
### **Muestra de programación de información de la página de recuperación**
El siguiente fragmento de código recupera la información de las páginas de un diagram.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(RetrievePageInfo.class);

//Call the diagram constructor to load diagram
Diagram diagram = new Diagram(dataDir+ "RetrievePageInfo.vdx");

for (Page page : (Iterable<Page>) diagram.getPages())
{
    //Checks if current page is a background page
    if (page.getBackground() == com.aspose.diagram.BOOL.TRUE)
    {
        //Display information about the background page
        System.out.println("Background Page ID : " + page.getID());
        System.out.println("Background Page Name : " + page.getName());
    }
    else
    {
        //Display information about the foreground page
        System.out.println("\nPage ID : " + page.getID());
        System.out.println("Universal Name : " + page.getNameU());
        System.out.println("ID of the Background Page : " + page.getBackPage());
    }
}

{{< /highlight >}}
```
## **Obtenga la página Visio de un Diagram**
A veces, los desarrolladores necesitan obtener los detalles de la página del dibujo Visio. Aspose.Diagram tiene características que les ayudan a hacer esto.

 Aspose.Diagram for Java ofrece la[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) clase que representa un dibujo Visio. La propiedad Pages expuesta por la clase Diagram admite una colección de objetos Aspose.Diagram.Page. La clase PageCollection expone el método GetPage que se puede llamar para obtener el objeto Page.
### **Obtener un objeto de página Visio por ID**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetPage de la clase Diagram.Pages.

El siguiente ejemplo muestra cómo obtener un objeto de página por ID del dibujo Visio.
#### **Obtener objeto de página por ejemplo de programación de ID**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyID.class); 
// Call the diagram constructor to load diagram from a VDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page id
int pageid = 2;
// Get page object by id
Page page2 = diagram.getPages().getPage(pageid);

{{< /highlight >}}
```
### **Obtener un objeto de página Visio por nombre**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetPage de la clase Diagram.Pages.
#### **Obtener objeto de página por nombre Ejemplo de programación**
El siguiente ejemplo muestra cómo obtener un objeto de página por nombre del dibujo Visio.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(GetVisioPagebyName.class);     
// Call the diagram constructor to load diagram from a VSDX file
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Set page name
String pageName = "Flow 2";
// Get page object by name
Page page2 = diagram.getPages().getPage(pageName);

{{< /highlight >}}
```
## **Copie una página Visio en otra Diagram**
Aspose.Diagram for Java API permite a los desarrolladores copiar y agregar su contenido de Visio diagram a otro. Este tema de ayuda explica cómo realizar esta tarea.

 Aspose.Diagram for Java API tiene el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) clase que representa un dibujo Visio. La propiedad Pages expuesta por la clase Diagram admite una colección de objetos Aspose.Diagram.Page. La clase PageCollection expone el método Add al que se puede llamar para agregar otro objeto Page.

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

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(CopyVisioPage.class);
        
// Call the diagram constructor to load diagram from a VSD file
Diagram originalDiagram = new Diagram(dataDir + "Drawing1.vsd");

// initialize the new visio diagram
Diagram newDiagram = new Diagram();

// add all masters from the source Visio diagram
MasterCollection originalMasters = originalDiagram.getMasters();
for (Master master : (Iterable<Master>) originalMasters) {
   newDiagram.addMaster(originalDiagram, master.getName());
}

// get the page object from the original diagram
Page SrcPage = originalDiagram.getPages().getPage("Page-1");
// set page name
SrcPage.setName("new page");
        
// it calculates max page id
int max = 0;
if (newDiagram.getPages().getCount() != 0)
    max = newDiagram.getPages().get(0).getID();

for (int i = 1; i < newDiagram.getPages().getCount(); i++)
{
    if (max < newDiagram.getPages().get(i).getID())
        max = newDiagram.getPages().get(i).getID();
}
       
int MaxPageId = max;
// set page id
SrcPage.setID(MaxPageId);
// add reference of the original diagram page
newDiagram.getPages().add(SrcPage);

// remove first empty page
newDiagram.getPages().remove(newDiagram.getPages().get(0));

// save diagram in VDX format
newDiagram.save(dataDir + "CopyVisioPage_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Copie la página Visio a otra instancia de la página**
El método Copy de la clase Page toma una instancia de página para clonar.

**Java**

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page();

// copy page

newPage.copy(diagram.getPages().getPage("Page-1"));

{{< /highlight >}}
## **Insertar una página en blanco en un dibujo Visio**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) puede insertar una nueva página en blanco en el dibujo Microsoft Office Visio. Este tema de ejemplo describe cómo hacerlo.

El método Add, expuesto por la colección Pages, permite a los desarrolladores agregar una nueva página en blanco en el Visio diagram. Se debe asignar el ID de la página.
### **Insertar una muestra de programación de página en blanco**
El siguiente fragmento de código inserta una página en blanco en el dibujo Visio:

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(InsertBlankPageInVisio.class);   
// load diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
        
// it calculates max page id
int max = 0;
if (diagram.getPages().getCount() != 0)
    max = diagram.getPages().get(0).getID();

for (int i = 1; i < diagram.getPages().getCount(); i++)
{
    if (max < diagram.getPages().get(i).getID())
        max = diagram.getPages().get(i).getID();
}
        
// Initialize a new page object
Page newPage = new Page();
// Set name
newPage.setName("new page");
// Set page ID
newPage.setID(max + 1);

// Or try the Page constructor
// Page newPage = new Page(MaxPageId + 1);

// Add a new blank page
diagram.getPages().add(newPage);

// Save diagram
diagram.save(dataDir + "InsertBlankPageInVisio_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Mover la posición de la página en el dibujo Visio**
Aspose.Diagram for Java API puede mover la posición de la página en el dibujo Visio. El método moveTo, expuesto por la clase Page, ayuda a los desarrolladores a mover la posición de la página.
### **Mover posición de página Ejemplo de programación**
El miembro MoveTo toma el índice de la página de destino como parámetro para mover la posición de la página en el dibujo Visio:

{{< highlight "java" >}}

 // import diagram

Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

Page newPage = new Page(1);

// move page in the diagram

newPage.moveTo(2);

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
