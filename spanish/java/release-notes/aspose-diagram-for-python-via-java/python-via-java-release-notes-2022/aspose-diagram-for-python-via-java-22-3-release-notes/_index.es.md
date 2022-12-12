﻿---
title: Aspose.Diagram for Python via Java 22.3 Release Notes
type: docs
weight: 25
url: /es/java/aspose-diagram-for-python-via-java-22-3-release-notes/
---
{{% alert color="primary" %}}

This page contains release notes information for Aspose.Diagram for Python via Java 22.3.

{{% /alert %}}
## **Mejoras y Cambios**  ##

|**Llave**|**Resumen**|**Categoría**|
|:- |:- |:- |
|DIAGRAMJAVA-50883|Determine las fuentes que faltan y la información de sustitución de fuentes del API|Insecto|

## `?`**Public API y cambios incompatibles con versiones anteriores**
La siguiente es una lista de los cambios realizados al público API, como miembros agregados, renombrados, eliminados o obsoletos, así como cualquier cambio no compatible con versiones anteriores realizado en Aspose.Diagram for Java. Si tiene inquietudes sobre cualquier cambio enumerado, plantéelo en el foro de soporte Aspose.Diagram.

### **Agrega AddText en la página**
- Agrega texto con PinX y PinY definidos.

{{< highlight "java" >}}
Shape shape = page.addText(1, 1, 2, 2, "Test text", "Calibri", "#a5a5a5", 0.25);
{{< /highlight >}}
