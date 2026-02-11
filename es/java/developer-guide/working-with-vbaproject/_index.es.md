---
title: Administre los códigos VBA de Visio habilitados para macros diagram.
linktitle: Diagram Proyecto VBA
type: docs
weight: 200
url: /es/java/working-with-vbaproject/
description: Agregue el módulo VBA y modifique VBA o macro con la biblioteca Aspose.Diagram.
---
## **Agregar un módulo VBA**
{{% alert color="primary" %}}

Aspose.Diagram le permite agregar un nuevo módulo VBA y código de macro usando Aspose.Diagram. Utilice el método [**Diagram.VbaProject.Modules.Add()**] para agregar el nuevo módulo VBA dentro del diagram

{{% /alert %}}

 El siguiente código de muestra agrega un nuevo módulo VBA y código de macro y guarda el resultado en el formato VSDM. Una vez, abrirá el archivo de salida VSDM en Microsoft Visio y haga clic en el**Desarrollador > Visual Basic** comandos de menú, verá un módulo llamado "TestModule" y dentro de él, verá el siguiente código de macro.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Aquí está el código de muestra para generar el archivo de salida VSDM con el módulo VBA y el código de macro.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Add module
int index = diagram.getVbaProject().getModules().add(VbaModuleType.PROCEDURAL, "TestModule");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(index);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"Welcome to Aspose!\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Modificar VBA o Macro**

{{% alert color="primary" %}} 

Puede modificar VBA o código de macro usando Aspose.Diagram. Aspose.Diagram agregó el siguiente espacio de nombres y clases para leer y modificar el proyecto de VBA en el archivo Visio.

- Aspose.Diagram.Vba
- Proyecto Vba
- VbaModuleCollection
- Módulo Vba

Este artículo le mostrará cómo cambiar el código VBA o macro dentro del archivo fuente Visio usando Aspose.Diagram.

{{% /alert %}} 

El siguiente código de ejemplo carga el archivo fuente Visio que tiene un código VBA o macro siguiente dentro de él

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is test message."

End Sub

{{< /highlight >}}

Después de la ejecución del código de muestra Aspose.Diagram, el código VBA o Macro se modificará de esta manera

{{< highlight "java" >}}

 Sub Button1_Click()

    MsgBox "This is Aspose.Diagram message."

End Sub

{{< /highlight >}}

 Puedes descargar el[fuente Visio archivo]() y el[archivo de salida Visio]() de los enlaces dados.

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
//Get module 
com.aspose.diagram.VbaModule module = diagram.getVbaProject().getModules().get(2);
//Set module
module.setCodes("Attribute VB_Name = \"module2\"\r\n Sub Button1_Click()\r\n\r\n    MsgBox \"This is Aspose.Diagram message.\"\r\n\r\nEnd Sub\r\n");

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## **Temas avanzados**
- [Compruebe si el código VBA está firmado](/diagram/es/java/check-if-vba-code-is-signed/)
