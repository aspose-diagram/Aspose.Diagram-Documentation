---
title: Administrar propiedades de documentos
linktitle: Propiedades del documento
type: docs
weight: 80
url: /es/java/document-properties/
aliases: [/java/document-properties/]
description: Administre las propiedades del documento de los archivos visio.
---
## **Introducción**

Microsoft Visio brinda la posibilidad de agregar propiedades a los archivos visio. Estas propiedades del documento brindan información útil y se dividen en 2 categorías, como se detalla a continuación.

- Propiedades definidas por el sistema (integradas): las propiedades integradas contienen información general sobre el documento, como el título del documento, el nombre del autor, las estadísticas del documento, etc.
- Propiedades definidas por el usuario (personalizadas): propiedades personalizadas definidas por el usuario final en forma de par nombre-valor.

{{% alert color="primary" %}}

El punto más importante que debe saber acerca de las propiedades integradas y personalizadas es que se puede acceder a las propiedades integradas y modificarlas, pero no crearlas ni eliminarlas. Sin embargo, las propiedades personalizadas se pueden crear y administrar.

{{% /alert %}}

## **Administración de propiedades de documentos mediante Microsoft Visio**

 Microsoft Visio le permite administrar las propiedades del documento de los archivos Visio de manera WYSIWYG. Siga los pasos a continuación para abrir el**Propiedades** diálogo en Visio 2016.

1.  Desde el**Expediente** menú, seleccione**Información**.

|**Selección del menú de información**|
|:- |
|![todo:imagen_alternativa_texto](managing-document-properties_1.png)|
1.  Haga clic en**Propiedades** encabezado y seleccione "Propiedades avanzadas".

|**Hacer clic en Selección de propiedades avanzadas**|
|:- |
|![todo:imagen_alternativa_texto](managing-document-properties_2.png)|
1. Administre las propiedades del documento del archivo.

|**Diálogo de propiedades**|
|:- |
|![todo:imagen_alternativa_texto](managing-document-properties_3.png)|
En el cuadro de diálogo Propiedades, hay diferentes pestañas, como General, Resumen, Estadísticas, Contenido y Aduanas. Cada pestaña ayuda a configurar diferentes tipos de información relacionada con el archivo. La pestaña Personalizado se utiliza para administrar las propiedades personalizadas.

## **Trabajar con propiedades de documentos usando Aspose.Diagram**

Los desarrolladores pueden administrar dinámicamente las propiedades del documento utilizando las API Aspose.Diagram. Esta función ayuda a los desarrolladores a almacenar información útil junto con el archivo, como cuándo se recibió, procesó, marcó la hora, etc.

{{% alert color="primary" %}}

Aspose.Diagram for Java escribe directamente la información sobre API y el número de versión en los documentos de salida.

Tenga en cuenta que no puede indicar al Aspose.Diagram for Java que cambie o elimine esta información de los documentos de salida.

{{% /alert %}}

### **Acceso a las propiedades del documento**

 Aspose.Diagram Las API admiten ambos tipos de propiedades de documentos, integradas y personalizadas. Aspose.Diagram'[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) clase representa un archivo Visio y, como un archivo visio, el[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) La clase puede contener varias páginas, cada una representada por el[**Página**](https://reference.aspose.com/diagram/java/com.aspose.diagram/page) mientras que la colección de páginas está representada por el[**Colección de páginas**](https://reference.aspose.com/diagram/java/com.aspose.diagram/pagecollection)clase.

 Utilizar el[**Diagram**](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram)para acceder a las propiedades del documento del archivo como se describe a continuación.

- Para acceder a las propiedades del documento incorporado, utilice[**diagram.DocumentProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/documentproperties).
-  Para acceder a las propiedades del documento personalizado, use[**diagram.DocumentProps.CustomProps**](https://reference.aspose.com/diagram/java/com.aspose.diagram/CustomPropCollection).


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


### **Adición o eliminación de propiedades de documentos personalizados**

Como describimos anteriormente al comienzo de este tema, los desarrolladores no pueden agregar o quitar propiedades integradas porque estas propiedades están definidas por el sistema, pero es posible agregar o quitar propiedades personalizadas porque están definidas por el usuario.

### **Adición de propiedades personalizadas**

 Aspose.Diagram Las API han expuesto el[**Agregar**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#add(com.aspose.diagram.CustomProp) ) método para el[**CustomPropCollection**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection)class para agregar propiedades personalizadas a la colección.


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


### **Eliminación de propiedades personalizadas**

 Para eliminar propiedades personalizadas usando Aspose.Diagram, llame al[**CustomPropCollection.Remove**](https://reference.aspose.com/diagram/java/com.aspose.diagram/custompropcollection#remove(com.aspose.diagram.CustomProp)) y pase el nombre de la propiedad del documento que se eliminará.


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

