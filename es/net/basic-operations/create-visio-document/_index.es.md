---
title: Crear documento Visio mediante programación
linktitle: Crear documento Visio
type: docs
weight: 10
url: /es/net/create-visio-document/
description: Esta página describe cómo crear el documento Visio desde cero con la biblioteca Aspose.Diagram.
---
## **Creación de un nuevo dibujo Visio**
Aspose.Diagram for .NET le permite leer y crear diagramas Microsoft Visio desde sus propias aplicaciones, sin Microsoft Office automatización. El primer paso al crear nuevos documentos es crear un diagram. Luego agregue formas y conectores para construir el diagram.
## **Create Visio Ejemplo de programación de dibujo**
El siguiente código muestra cómo crear un nuevo dibujo Microsoft Visio. Tenga en cuenta que el dibujo en blanco contiene una sola página vacía.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_LoadSaveConvert();

// Initialize a Diagram class
Diagram diagram = new Diagram();

// Save diagram in the VSDX format
diagram.Save(dataDir + "CreateNewVisio_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

{{% alert color="primary" %}} 

El tamaño del papel de dibujo es Carta por defecto.

{{% /alert %}} 

