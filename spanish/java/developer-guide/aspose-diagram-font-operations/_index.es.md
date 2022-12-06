﻿---
title: Aspose.Diagram Operaciones de fuentes
type: docs
weight: 170
url: /es/java/aspose-diagram-font-operations/
---
{{% alert color="primary" %}} 

Aspose.Diagram permite a los desarrolladores configurar los directorios de fuentes para renderizar en diagramas Visio. Este artículo muestra cómo utilizar fuentes de directorios personalizados.

{{% /alert %}} 
### **Trabajar con fuentes**
#### **Donde Aspose.Diagram busca fuentes TrueType en Windows**
 Aspose.Diagram busca fuentes en el**Windows\Fuentes** carpeta. Esta configuración predeterminada funciona la mayor parte del tiempo, así que solo especifique sus propias carpetas de fuentes si realmente lo necesita.
#### **Cómo especificar explícitamente una carpeta de fuentes**
 Aspose.Diagram API ha expuesto el método setFontDirs para el[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram) class para especificar las carpetas de fuentes como se describe a continuación.

1. El método Diagram.setFontDirs toma una matriz de cadenas como parámetro, por lo que el desarrollador puede especificar muchos directorios de fuentes usando este enfoque.

{{% alert color="primary" %}} 

Al especificar la carpeta de fuentes utilizando el enfoque mencionado anteriormente, recomendamos configurar la ubicación de la fuente al inicio de la aplicación; de lo contrario, puede obtener resultados con un formato deficiente.

{{% /alert %}} {{% alert color="primary" %}} 

Configurar la carpeta de fuentes con cualquiera de los métodos anteriores no garantiza que Aspose.Diagram API no busque las fuentes en ubicaciones predeterminadas, como la carpeta de fuentes del sistema.

{{% /alert %}} 

Muestra cómo configurar Aspose.Diagram para buscar fuentes TrueType en varias carpetas al renderizar o incrustar fuentes.
#### **Ejemplo de programación**
El siguiente código de ejemplo muestra cómo configurar Aspose.Diagram para buscar fuentes TrueType en varias carpetas al renderizar o incrustar fuentes.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Fonts-SpecifyFontLocation-SpecifyFontLocation.java" >}}
### **Reciba notificaciones de fuentes faltantes y sustitución de fuentes durante el renderizado**
Aspose.Diagram API requiere acceso a la fuente precisa para representar correctamente el dibujo en formato PDF. Si la fuente requerida no está disponible en la máquina, entonces Aspose.Diagram API representa cualquier instancia de esa fuente utilizando la fuente predeterminada o la fuente más cercana disponible en la máquina, dado que esta sustitución puede cambiar el aspecto del dibujo representado, es posible que los desarrolladores deban ser notificado cuando falta una fuente y con qué fuente será reemplazada.
#### **Ejemplo de programación de notificación de fuentes faltantes y sustitución de fuentes**
Para ser notificado de la sustitución de fuentes durante el renderizado:

1. Cree una clase que implemente el[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)
1. Páselo a la propiedad PdfSaveOptions.setWarningCallback(com.aspose.diagram.IWarningCallback).

Durante el guardado del dibujo, la instancia de[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)se llama si hay posibles problemas de fidelidad con el dibujo. En este caso, elegimos procesar solo las advertencias que son de sustitución de fuente e imprimir la advertencia en la pantalla. El siguiente ejemplo muestra cómo recibir notificaciones de sustituciones de fuentes usando[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback).

**Java**

{{< highlight "java" >}}

 // load the document to render.

Diagram diagram = new Diagram("C:\\temp\\Output.vsdx");


// initialize PdfSaveOptions object

com.aspose.diagram.PdfSaveOptions saveOp = new com.aspose.diagram.PdfSaveOptions();

// create a new class implementing IWarningCallback which collect any warnings produced during drawing save.

HandleDocumentWarnings callback = new HandleDocumentWarnings();

saveOp.setWarningCallback(callback);



// pass the save options along with the save path to the save method.

diagram.save("C:\\temp\\Rendering.MissingFontNotification Out.pdf", saveOp);

{{< /highlight >}}
#### **Implementando IWarningCallback**
El último paso es crear la clase que implementa el[IAdvertenciaDevolución de llamada](https://reference.aspose.com/diagram/java/com.aspose.diagram/IWarningCallback)interfaz. Esta clase imprimirá cualquier advertencia de sustitución de fuentes en la consola. El siguiente ejemplo muestra cómo implementar IWarningCallback para recibir una notificación de cualquier sustitución de fuente durante el guardado del documento.



**Java**

{{< highlight "java" >}}

 public class HandleDocumentWarnings implements IWarningCallback {

     /**

     * Our callback only needs to implement the "Warning" method. This method is

     * called whenever there is a potential issue during document processing.

     * The callback can be set to listen for warnings generated during document

     * load and/or document save.

     */

     public void warning(WarningInfo info) {

         // We are only interested in fonts being substituted.

         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION) {

         System.out.println("Font substitution: " + info.getDescription());

     }

 }

}

{{< /highlight >}}
