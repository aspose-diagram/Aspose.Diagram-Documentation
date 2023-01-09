---
title: Crear, actualizar, diseñar y autoajustar formas
type: docs
weight: 10
url: /es/net/create-update-layout-and-auto-fit-shapes/
description: Use C# Diagram API para crear, actualizar y diseñar formas automáticamente en archivos Visio usando C# dentro de sus aplicaciones. Guía completa con ejemplos de código C#.
---
## **Creando un Diagram**
 Aspose.Diagram for .NET le permite leer y crear diagramas Microsoft Visio desde sus propias aplicaciones, sin Microsoft Office automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego[añadir formas y conectores](https://docs.aspose.com/diagram/net/add-retrieve-copy-and-read-visio-shape-data/)para construir el diagram. Use el constructor predeterminado de[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase para crear un nuevo diagram.
### **Ejemplo de programación**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-CreateDiagram-CreateDiagram.cs" >}}
## **Formas de diseño en estilo de diagrama de flujo**
 Con ciertos tipos de dibujos conectados, como diagramas de flujo y diagramas de red, puede utilizar el**Formas de diseño** característica para posicionar formas automáticamente. El posicionamiento automático es más rápido que arrastrar manualmente cada forma a una nueva ubicación.

Por ejemplo, si está actualizando un diagrama de flujo grande para incluir un nuevo proceso, puede agregar y conectar las formas que componen el proceso y luego usar la función de diseño para diseñar automáticamente el dibujo actualizado.

 El método Layout, expuesto por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) la clase diseña las formas y/o redirige los conectores en todas las páginas de diagram. Este método acepta un[Opciones de diseño](https://reference.aspose.com/diagram/net/aspose.diagram.autolayout/layoutoptions)objeto como argumento. Use las diferentes propiedades expuestas por la clase LayoutOptions para diseñar formas automáticamente.

La siguiente imagen muestra el diagram cargado por los fragmentos de código en este artículo, antes de que se aplique el diseño automático. Los fragmentos de código muestran cómo aplicar[diseños de diagrama de flujo](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) y[diseños de árboles compactos](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/).

**La fuente diagram.**

![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_1.png)

Los fragmentos de código de este artículo toman la fuente diagram y le aplican varios tipos de diseño automático, guardando cada uno en un archivo separado.

|<p>**Formas de diseño de abajo hacia arriba** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_2.png)</p>|<p>**Formas de diseño de arriba a abajo** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Diseño de formas de izquierda a derecha** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_4.png)</p>|<p>**Diseño de formas de derecha a izquierda** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_5.png)</p>|
Para diseñar formas en estilo de diagrama de flujo:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de la clase LayoutOptions y configure las propiedades relacionadas con el estilo del diagrama de flujo.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el dibujo Visio.
### **Ejemplo de programación de estilo de diagrama de flujo**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInFlowchartStyle-LayOutShapesInFlowchartStyle.cs" >}}
### **Disposición de formas en el estilo de árbol compacto**
 El estilo de diseño de árbol compacto intenta construir una estructura de árbol. Utiliza el mismo archivo de entrada que el[ejemplo anterior](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) guarda en varios estilos diferentes de árboles compactos.

|<p>**Diseño de árbol compacto: abajo y a la derecha** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Diseño de árbol compacto: abajo e izquierda** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Diseño de árbol compacto: derecha y abajo** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_8.png)</p>|<p>**Diseño de árbol compacto: izquierda y abajo** </p><p>![todo:imagen_alternativa_texto](create-update-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Para diseñar formas en el estilo de árbol compacto:

1.  Crear una instancia de la[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase.
1. Cree una instancia de la clase LayoutOptions y establezca propiedades de estilo de árbol compacto.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el archivo Visio.
#### **Ejemplo de programación de estilo de árbol compacto**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-LayOutShapesInCompactTreeStyle-LayOutShapesInCompactTreeStyle.cs" >}}
## **Ajuste automático el Visio Diagram**
 Aspose.Diagram API admite el ajuste automático del dibujo Visio. Esta función de operación ayuda a traer formas externas dentro del límite de la página Visio. Aspose.Diagram for .NET API tiene el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) clase que representa un dibujo Visio. los[DiagramaGuardarOpciones](https://reference.aspose.com/diagram/net/aspose.diagram.saving/diagramsaveoptions) La clase expone la propiedad AutoFitPageToDrawingContent para ajustar automáticamente el dibujo Visio.

Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Cree un objeto de la clase DiagramSaveOptions y pase el formato de archivo resultante.
1. Establezca la propiedad AutoFitPageToDrawingContent del objeto DiagramSaveOptions.
1. Llame al método Save del objeto de clase Diagram y también pase la ruta completa del archivo y el objeto DiagramSaveOptions.
### **Ejemplo de programación de ajuste automático**
El siguiente código de ejemplo muestra cómo ajustar formas automáticamente en Visio diagram.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-AutoFitShapesInVisio-AutoFitShapesInVisio.cs" >}}
## **Trabajando con Proyecto VBA**
### **Modifique el código del módulo VBA en Visio Diagram**
 Este artículo muestra cómo modificar un código de módulo de VBA automáticamente usando Aspose.Diagram for .NET. Hemos agregado[Módulo Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModule), [VbaModuleCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaModuleCollection), [Proyecto Vba](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProject), [VbaProjectReferenceVbaProjectReference](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReference) y[VbaProjectReferenceCollectionVbaProjectReferenceCollection](http://www.aspose.com/api/net/diagram/aspose.diagram.vba/VbaProjectReferenceCollection) clases Estas clases ayudan a controlar el proyecto VBA. Los desarrolladores pueden extraer y modificar el código del módulo VBA.
### **Modificar ejemplo de programación de código de módulo VBA**
Por favor, compruebe este ejemplo de código:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-ModifyVBAModule-ModifyVBAModule.cs" >}}
### **Eliminar todas las macros del Visio Diagram**
 Aspose.Diagram for .NET permite a los desarrolladores eliminar todas las macros del Visio diagram. La propiedad VbProjectData, expuesta por el[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class, le permite eliminar todas las macros del dibujo Visio.
### **Eliminar todas las macros Ejemplo de programación**
{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-RemoveMacrosFromVisio-RemoveMacrosFromVisio.cs" >}}
## **Creación de un nuevo Diagram con VSTO**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/)permite a los desarrolladores crear y trabajar con Microsoft Office Visio diagramas e incorporar características en sus aplicaciones de software. Hay otras formas de trabajar con archivos Visio, más comúnmente, Microsoft Automatización. Desafortunadamente, eso tiene algunas limitaciones. Aspose.Diagram es potente y rápido y funciona de forma independiente sin Microsoft Office instalación.

 Este artículo de migración muestra cómo usar first[VSTO](https://docs.aspose.com/diagram/net/create-update-layout-and-auto-fit-shapes/) y entonces[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) para crear un nuevo diagram y agregarle algunas formas. Notará que el código Aspose.Diagram es más corto que el código VSTO. Siéntase libre de usar el código como base para su propio desarrollo y mejorarlo para satisfacer sus necesidades. VSTO le permite programar con archivos Microsoft Visio. Para crear un nuevo diagram:

1. Cree un objeto de aplicación Visio.
1. Haga que el objeto de la aplicación sea invisible.
1. Cree un diagram vacío.
1. Agregue formas de Visio maestros (plantillas).
1. Guarde el archivo como VDX.
### **Crear nuevo Diagram con muestra de programación VSTO**
{{% alert color="primary" %}}

usando Visio = Microsoft.Office.Interop.Visio;
Importaciones Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}


**Ejemplo:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithVSTO-CreatingDiagramWithVSTO.cs" >}}
## **Creando un Nuevo Diagram con Aspose.Diagram for .NET**
Usando Aspose.Diagram API, los desarrolladores no necesitan Microsoft Office Visio instalación en la máquina, y pueden trabajar independientemente de Microsoft Office Automatización.

Para crear un nuevo diagram:

1. Cree un diagram vacío.
1. Agregue formas de Visio maestros (plantillas).
1. Guarde el archivo como VDX.
### **Nuevo Diagram con Aspose.Diagram for .NET Ejemplo de programación**
{{% alert color="primary" %}}

usando Aspose.Diagram;
Importaciones Aspose.Diagram

{{% /alert %}}

Ejemplo:

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-CreatingDiagramWithAspose-CreatingDiagramWithAspose.cs" >}}
## **Actualizar propiedades de forma**
 Al trabajar con diagramas Microsoft Visio, los usuarios pueden actualizar los atributos de forma, incluidos el texto, el estilo, la posición, la altura y el ancho. Como desarrollador de software que trabaja con archivos Visio, se le pedirá que haga esto mediante programación. La buena noticia es que es posible, ya sea usando los mecanismos de programación con archivos Visio que proporciona Microsoft, VSTO, o usando[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 El siguiente tema muestra cómo usar[VSTO](https://products.aspose.com/diagram/net/) y[Aspose.Diagram](https://products.aspose.com/diagram/net/) para actualizar las propiedades de la forma. Los fragmentos de código a continuación muestran cómo actualizar las propiedades de forma para VSTO y Aspose.Diagram for .NET. Siéntase libre de usar el código y aplicarlo a su situación particular.
### **Actualización de propiedades de forma con VSTO**
VSTO le permite programar con archivos Microsoft Visio. Para actualizar las propiedades de la forma:

1. Cree un objeto de aplicación Visio.
1. Haga que el objeto de la aplicación sea invisible.
1. Abra un archivo Visio VSD existente.
1. Encuentre la forma requerida.
1. Actualice las propiedades de la forma (texto, estilo de texto, posición y tamaño).
1. Guarde el archivo como VDX.
#### **Actualización de las propiedades de la forma con el ejemplo de programación de VSTO**
{{% alert color="primary" %}}

usando Visio = Microsoft.Office.Interop.Visio;
Importaciones Visio = Microsoft.Office.Interop.Visio

{{% /alert %}}

**Ejemplo:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithVSTO-UpdateShapePropsWithVSTO.cs" >}}
### **Actualización de propiedades de forma con Aspose.Diagram for .NET**
Usando Aspose.Diagram API, los desarrolladores no necesitan Microsoft Office Visio en la máquina, y pueden trabajar independientemente de Microsoft Office Automatización.

Para actualizar las propiedades de la forma con Aspose.Diagram for .NET:

1. Abra un archivo Visio VSD existente.
1. Encuentre la forma requerida.
1. Actualice las propiedades de la forma (texto, estilo de texto, posición y tamaño).
1. Guarde el archivo como VDX.
#### **Actualización de propiedades de forma con Aspose.Diagram for .NET Ejemplo de programación**
{{% alert color="primary" %}}

usando Aspose.Diagram;
Importaciones Aspose.Diagram

{{% /alert %}}

**Ejemplo:**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Knowledge-Base-UpdateShapePropsWithAspose-UpdateShapePropsWithAspose.cs" >}}
