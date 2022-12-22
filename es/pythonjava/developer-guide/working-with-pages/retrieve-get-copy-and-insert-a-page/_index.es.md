---
title: Recuperar, obtener, copiar e insertar una página
type: docs
weight: 10
url: /es/python-java/retrieve-get-copy-and-insert-a-page/
---
## **Recuperación de información de la página**
En Microsoft Visio, las páginas son páginas de primer plano o de fondo. Para obtener información de la página, por ejemplo, el ID de la página y el nombre de la página, primero establezca si una página es una página de fondo o de primer plano.

The `Page` object represents the drawing area of a foreground page or a background page. The Pages property exposed by the `Diagram` class supports a collection of Page objects. This property can be used to retrieve page information.

Use the `Page.Background` property to determine whether a page is a foreground or background page .

### **Muestra de programación de información de la página de recuperación**
El siguiente fragmento de código recupera la información de las páginas de un diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-RetrievePageInfo.py" >}}

## **Obtenga la página Visio de un Diagram**
Sometimes, developers need to get a Visio drawing's page details. Aspose.Diagram for Python via Java has features that helps them do this.

Aspose.Diagram for Python via Java offers the `Diagram` class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of `Page` objects. The PageCollection class exposes `getPage` method that can be called to get Page object.

### **Obtener un objeto de página Visio por ID**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Call the Diagram.Pages class' getPage method.

El siguiente ejemplo muestra cómo obtener un objeto de página por ID del dibujo Visio.

#### **Obtener objeto de página por ejemplo de programación de ID**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyID.py" >}}

### **Obtener un objeto de página Visio por nombre**
Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Llame al método GetPage de la clase Diagram.Pages.

#### **Obtener objeto de página por nombre Ejemplo de programación**
El siguiente ejemplo muestra cómo obtener un objeto de página por nombre del dibujo Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-GetVisioPagebyName.py" >}}

## **Copie una página Visio en otra Diagram**
Aspose.Diagram for Python via Java API allows developers to copy and add its content from the one Visio diagram to another. This help topic explains how to accomplish this task.

Aspose.Diagram for Python via Java API has the `Diagram` class that represents a Visio drawing. The Pages property exposed by the Diagram class supports a collection of `Page` objects. The PageCollection class exposes `add` method that can be called to add another Page object.

Este ejemplo funciona de la siguiente manera:

1. Cree un nuevo objeto de la clase Diagram.
1. Cargue un Visio diagram existente en el objeto de clase Diagram.
1. Agregue todos los maestros del cargado Visio diagram
1. Obtenga el objeto de página del diagram cargado (que debe copiarse).
1. Establezca el nombre y la identificación del objeto de la página.
1. Eliminar página vacía del nuevo diagram (opcional).
1. Call add method of the PageCollection class.
1. Guarde el nuevo diagram en el almacenamiento de la computadora.

### **Copie una muestra de programación de página Visio**
El siguiente ejemplo de código muestra cómo copiar un objeto de página Visio en otro dibujo Visio.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-CopyVisioPage.py" >}}

## **Copie la página Visio a otra instancia de la página**
The `copy` method of the `Page` class takes a page instance to clone.

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page()

# copy page

newPage.copy(diagram.getPages().getPage("Page-1"))

```

## **Insertar una página en blanco en un dibujo Visio**
Aspose.Diagram for Python via Java can insert a new blank page into the Microsoft Office Visio drawing. This example topic describes how to do so.

The `add` method, exposed by the Pages collection, allows developers to add a new blank page in the Visio diagram. The page ID should be assigned.

### **Insertar una muestra de programación de página en blanco**
El siguiente fragmento de código inserta una página en blanco en el dibujo Visio:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Pages-InsertBlankPageInVisio.py" >}}

## **Mover la posición de la página en el dibujo Visio**
Aspose.Diagram for Python via Java API can move page position in the Visio drawing. The `moveTo` method, exposed by the `Page` class, helps developers to move the page position.

### **Mover posición de página Ejemplo de programación**
El miembro MoveTo toma el índice de la página de destino como parámetro para mover la posición de la página en el dibujo Visio:

``` python
# import diagram

diagram = Diagram(dataDir + "Drawing1.vsdx")

newPage = Page(1)

# move page in the diagram

newPage.moveTo(2)

diagram.save(dataDir + "Drawing1.vsdx", SaveFileFormat.VSDX)
```
