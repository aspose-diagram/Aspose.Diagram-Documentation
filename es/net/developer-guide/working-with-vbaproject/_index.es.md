---
title: Administre los códigos VBA de Visio habilitados para macros diagram.
linktitle: Diagram Proyecto VBA
type: docs
weight: 200
url: /es/net/working-with-vbaproject/
description: Agregue el módulo VBA y modifique VBA o macro con la biblioteca Aspose.Diagram.
---
## **Agregar un módulo VBA**
{{% alert color="primary" %}}

 Aspose.Diagram le permite agregar un nuevo módulo VBA y código de macro usando Aspose.Diagram. Utilice el[**Diagram.VbaProject.Modules.Add()**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbamodulecollection/methods/add/index) método para agregar el nuevo Módulo VBA dentro del diagram

{{% /alert %}}

 El siguiente código de muestra agrega un nuevo módulo VBA y código de macro y guarda el resultado en el formato VSDM. Una vez, abrirá el archivo de salida VSDM en Microsoft Visio y haga clic en el**Desarrollador > Visual Basic** comandos de menú, verá un módulo llamado "TestModule" y dentro de él, verá el siguiente código de macro.

{{< highlight "java" >}}

 Sub ShowMessage()

    MsgBox "Welcome to Aspose!"

End Sub

{{< /highlight >}}

Aquí está el código de muestra para generar el archivo de salida VSDM con el módulo VBA y el código de macro.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-AddModule.cs" >}}

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

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-Working-Diagrams-Vba-ModifyModule.cs" >}}

## **Temas avanzados**
- [Compruebe si el código VBA está firmado](/diagram/es/net/check-if-vba-code-is-signed/)
