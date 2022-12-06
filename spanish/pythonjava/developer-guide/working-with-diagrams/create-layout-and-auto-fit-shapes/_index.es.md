---
title: Crear, diseñar y autoajustar formas
type: docs
weight: 10
url: /es/python-java/create-layout-and-auto-fit-shapes/
---
## **Creando un Diagram**
 Aspose.Diagram para Python a través de Java le permite leer y crear Microsoft Visio diagramas desde sus propias aplicaciones, sin Microsoft Office Automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego[añadir formas y conectores](/diagram/es/python-java/add-and-connect-visio-shapes/) para construir el diagram. Use el constructor predeterminado de la clase Diagram para crear un nuevo diagram.
### **Ejemplo de programación**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-CreateDiagram.py" >}}
## **Formas de diseño en estilo de diagrama de flujo**
 Con ciertos tipos de dibujos conectados, como diagramas de flujo y diagramas de red, puede utilizar el**Formas de diseño** característica para posicionar formas automáticamente. El posicionamiento automático es más rápido que arrastrar manualmente cada forma a una nueva ubicación.

Por ejemplo, si está actualizando un diagrama de flujo grande para incluir un nuevo proceso, puede agregar y conectar las formas que componen el proceso y luego usar la función de diseño para diseñar automáticamente el dibujo actualizado.

El método Layout, expuesto por la clase Diagram, diseña las formas y/o redirige los conectores en todas las páginas de diagram. Este método acepta un objeto LayoutOptions como argumento. Use las diferentes propiedades expuestas por la clase LayoutOptions para diseñar formas automáticamente.

La siguiente imagen muestra el diagram cargado por los fragmentos de código en este artículo, antes de que se aplique el diseño automático. Los fragmentos de código muestran cómo aplicar diseños de diagrama de flujo y diseños de árbol compacto.

**La fuente diagram.** 

![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_1.png)

Los fragmentos de código de este artículo toman la fuente diagram y le aplican varios tipos de diseño automático, guardando cada uno en un archivo separado.

|<p>**Formas de diseño de abajo hacia arriba** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_2.png)</p>|<p>**Formas de diseño de arriba a abajo** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_3.png)</p>|
|:- |:- |
|<p>**Diseño de formas de izquierda a derecha** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_4.png)</p>|<p>**Diseño de formas de derecha a izquierda** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_5.png)</p>|
Para diseñar formas en estilo de diagrama de flujo:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de la clase LayoutOptions y configure las propiedades relacionadas con el estilo del diagrama de flujo.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el dibujo Visio.
### **Ejemplo de programación de estilo de diagrama de flujo**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInFlowchartStyle.py" >}}
### **Disposición de formas en el estilo de árbol compacto**
El estilo de diseño de árbol compacto intenta construir una estructura de árbol. Utiliza el mismo archivo de entrada que el ejemplo anterior y se guarda en varios estilos de árbol compacto diferentes.

|<p>**Diseño de árbol compacto: abajo y a la derecha** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_6.png)</p>|
|:- |
|<p>**Diseño de árbol compacto: abajo e izquierda** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_7.png)</p>|


|<p>**Diseño de árbol compacto: derecha y abajo** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_8.png)</p>|<p>**Diseño de árbol compacto: izquierda y abajo** </p><p>![todo:imagen_alternativa_texto](create-layout-and-auto-fit-shapes_9.png)</p>|
|:- |:- |
Para diseñar formas en el estilo de árbol compacto:

1. Cree una instancia de la clase Diagram.
1. Cree una instancia de la clase LayoutOptions y establezca propiedades de estilo de árbol compacto.
1. Llame al método Layout de la clase Diagram pasando LayoutOptions.
1. Llame al método Guardar de la clase Diagram para escribir el archivo Visio.
#### **Ejemplo de programación de estilo de árbol compacto**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-LayOutShapesInCompactTreeStyle.py" >}}
## **Ajuste automático el Visio Diagram**
Aspose.Diagram API admite el ajuste automático del dibujo Visio. Esta función de operación ayuda a traer formas externas dentro del límite de la página Visio.

Aspose.Diagram para Python a través de Java API tiene la clase Diagram que representa un dibujo Visio. La clase DiagramSaveOptions expone la propiedad AutoFitPageToDrawingContent para ajustar automáticamente el dibujo Visio.

Este ejemplo funciona de la siguiente manera:

1. Cree un objeto de la clase Diagram.
1. Cree un objeto de la clase DiagramSaveOptions y pase el formato de archivo resultante.
1. Establezca la propiedad AutoFitPageToDrawingContent del objeto DiagramSaveOptions.
1. Llame al método Save del objeto de clase Diagram y también pase la ruta completa del archivo y el objeto DiagramSaveOptions.
### **Ejemplo de programación de ajuste automático**
El siguiente código de ejemplo muestra cómo ajustar formas automáticamente en Visio diagram.

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-AutoFitShapesInVisio.py" >}}
## **Trabajando con Proyecto VBA**
### **Modifique el código del módulo VBA en Visio Diagram**
Este artículo muestra cómo modificar un código de módulo de VBA automáticamente usando Aspose.Diagram para Python a través de Java.

Hemos agregado las clases VbaModule, VbaModuleCollection, VbaProject, VbaProjectReference y VbaProjectReferenceCollection. Estas clases ayudan a controlar el proyecto VBA. Los desarrolladores pueden extraer y modificar el código del módulo VBA.
### **Modificar ejemplo de programación de código de módulo VBA**
Por favor, compruebe este ejemplo de código:

{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-ModifyVBAModuleCode.py" >}}
### **Eliminar todas las macros del Visio Diagram**
Aspose.Diagram para Python a través de Java permite a los desarrolladores eliminar todas las macros del Visio diagram.

La propiedad JavaProjectData, expuesta por la clase Diagram, le permite eliminar todas las macros del dibujo Visio.
### **Eliminar todas las macros Ejemplo de programación**
{{< gist "aspose-diagram-gists" "af605f5a3113e8afc05e4bae8990fb41" "Examples-PythonJava-Diagrams-RemoveMacrosFromVisio.py" >}}
