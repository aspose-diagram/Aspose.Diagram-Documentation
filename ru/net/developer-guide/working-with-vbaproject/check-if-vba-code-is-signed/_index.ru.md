---
title: Проверьте, подписан ли код VBA
type: docs
weight: 100
url: /ru/net/check-if-vba-code-is-signed/
description: Проверьте, подписан ли код vba библиотекой Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram позволяет пользователю проверить, подписан ли проект кода VBA или нет. Пожалуйста, используйте[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) свойство, чтобы проверить, подписан ли проект кода VBA или нет.

{{% /alert %}}

 В следующем коде объясняется, как проверить, подписан ли код VBA или нет, используя[**Diagram.VbaProject.IsSigned**](https://reference.aspose.com/diagram/net/aspose.diagram.vba/vbaproject/properties/issigned) имущество. Вы можете использовать любой из ваших файлов visio для проверки этого кода. В целях тестирования вы можете использовать[этот файл visio, используемый в коде](1.vsdm).

## Образец кода


{{< highlight csharp >}}

// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");

// Signature is valid
Console.WriteLine("Is VBA Code Project Signed: " + diagram.VbaProject.IsSigned);

diagram.Save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}


## Консольный вывод

 Ниже приведен консольный вывод приведенного выше кода с использованием[образец файла visio](1out.vsdm) предоставлено по ссылке.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
