---
title: Проверьте, подписан ли код VBA
type: docs
weight: 100
url: /ru/java/check-if-vba-code-is-signed/
description: Проверьте, подписан ли код vba библиотекой Aspose.Diagram.
---
{{% alert color="primary" %}}

Aspose.Diagram позволяет пользователю проверить, подписан ли проект кода VBA или нет. Используйте свойство [**Diagram.VbaProject.IsSigned**], чтобы проверить, подписан ли проект кода VBA.

{{% /alert %}}

 В следующем коде объясняется, как проверить, подписан ли код VBA или нет, используя свойство [**Diagram.VbaProject.IsSigned**]. Вы можете использовать любой из ваших файлов visio для проверки этого кода. В целях тестирования вы можете использовать[этот файл visio, используемый в коде](1.vsdm).

## Образец кода

```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(Test.class);

// Load a diagram
Diagram diagram = new Diagram(dataDir + "1.vsdm");
  
//Check signed     
boolean isSigned = diagram.getVbaProject().isSigned();

diagram.save(dataDir + "1out.vsdm", SaveFileFormat.VSDM);

{{< /highlight >}}
```

## Консольный вывод

 Ниже приведен консольный вывод приведенного выше кода с использованием[образец файла visio](1out.vsdm) предоставлено по ссылке.

{{< highlight "java" >}}

Is VBA Code Project Signed: False

{{< /highlight >}}
