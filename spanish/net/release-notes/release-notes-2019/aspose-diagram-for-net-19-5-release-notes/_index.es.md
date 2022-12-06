---
title: Aspose.Diagram for .NET 19.5 Notas de la versión
type: docs
weight: 80
url: /es/net/aspose-diagram-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Esta página contiene notas de la versión para[Aspose.Diagram for .NET 19.5](https://www.nuget.org/packages/Aspose.Diagram/19.5.0)

{{% /alert %}} 
## **Mejoras y Cambios**

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMNET-51606|Detecte y elimine temas, gráficos de datos y estilos no utilizados de los diagramas Visio|Mejora|
|DIAGRAMNET-51637|La forma anidada dentro de un contenedor agrupado no se conserva correctamente|Mejora|
|DIAGRAMNET-51638|No se puede obtener Prop.Value.Val cuando el valor es un número entero|Mejora|
|DIAGRAMNET-51640|Determinar estilos no utilizados en un archivo Visio|Mejora|
|DIAGRAMNET-50051|VSDX a conversión de PDF, falta la flecha de conexión junto con el texto fuera de lugar|Insecto|
|DIAGRAMNET-50052|VSDX a conversión de PDF, formas con color de texto de fuente incorrecto|Insecto|
|DIAGRAMNET-51179|Sombreado incorrecto sobre un botón de correo electrónico al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51190|Visualización incorrecta de la forma hipervinculada al guardar un VDX en SVG|Insecto|
|DIAGRAMNET-51194|Representación incorrecta de un icono al guardar un VDX en SVG|Insecto|
|DIAGRAMNET-51254|Sombreado incorrecto en la barra superior al convertir un VSDM a SVG|Insecto|
|DIAGRAMNET-51618|Visio a PDF - Formato de fecha incorrecto y datos faltantes|Insecto|
|DIAGRAMNET-51628|Valor de texto incorrecto para el texto predeterminado eliminado en diagramas .vsdx|Insecto|
|DIAGRAMNET-51634|Visio a SVG: índice z incorrecto de algunas formas en la salida|Insecto|
|DIAGRAMNET-51636|Visio a SVG: no todos los elementos de ruta se exportan correctamente como elementos rect|Insecto|
|DIAGRAMNET-51641|Se muestra una imagen adicional al volver a guardar Visio con API|Insecto|
## **Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for .NET. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en la[Aspose.Diagram foro de soporte](https://forum.aspose.com/c/diagram/17).
### **Agrega GetUnusedStyles en Diagram**
Consigue estilos sin usar.

{{< highlight "java" >}}

  StyleSheetCollection unused = diagram.GetUnusedStyles();

{{< /highlight >}}
