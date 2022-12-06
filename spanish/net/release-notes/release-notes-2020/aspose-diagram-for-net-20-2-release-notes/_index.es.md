---
title: Aspose.Diagram for .NET 20.2 Notas de la versión
type: docs
weight: 60
url: /es/net/aspose-diagram-for-net-20-2-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene información sobre las notas de la versión para Aspose.Diagram for .NET 20.2.

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51747|Cambios en el archivo después de la conversión Visio vsd->vsdx|Mejora|
|DIAGRAMNET-51750|Agregando la bandera "HasHiddenInfo"|Mejora|
|DIAGRAMNET-51748|Agregar PNG a Diagram - se pierde la transparencia|Insecto|
|DIAGRAMNET-51749|Se produce un error al guardar el documento Visio|Insecto|
|DIAGRAMNET-51751|VSDX a PNG: se muestra una imagen adicional|Insecto|
|DIAGRAMNET-51752|VSDX a PNG: se muestra espacio adicional|Insecto|
|DIAGRAMNET-51753|VSDX a PNG: la posición de los iconos está cambiando|Insecto|
|DIAGRAMNET-51754|VSDX a PNG: se cambia la posición del icono del signo de interrogación|Insecto|
|DIAGRAMNET-51762|El PDF generado es diferente en comparación con la entrada Visio diagram|Insecto|
|DIAGRAMNET-51763|VSDX a PNG: falta información en la salida|Insecto|
## ` `**Public API y cambios incompatibles con versiones anteriores**
` ` La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.
### **Se agregó EnlargePage en ImageSaveOptions**
- Especifica si ampliar la página

{{< highlight "java" >}}

 Aspose.Diagram.Saving.ImageSaveOptions opt = new Aspose.Diagram.Saving.ImageSaveOptions(Aspose.Diagram.SaveFileFormat.PNG);

opt.EnlargePage = false;

{{< /highlight >}}
### **Se agregó HasHiddenInfo en Diagram**
- Indica si este diagram tiene información oculta.



{{< highlight "java" >}}

 diagram.HasHiddenInfo();

{{< /highlight >}}




