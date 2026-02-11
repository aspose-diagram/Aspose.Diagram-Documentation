---
title: Уменьшить размер файла
type: docs
weight: 50
url: /ru/java/reduce-file-size/
description: В этом разделе объясняется, как уменьшить размер файла с diagram до Aspose.Diagram.
---
## **Уменьшить размер файла**
 Aspose.Diagram for Java API позволяет разработчикам удалять скрытую информацию из diagram для уменьшения размера файла.
[Страница](https://reference.aspose.com/diagram/java/com.aspose.diagram/Page) объект представляет область рисования страницы переднего плана или страницы фона. Чтобы уменьшить размер файла, вы можете использовать[RemoveHiddenInfoItem](https://reference.aspose.com/diagram/java/com.aspose.diagram/RemoveHiddenInfoItem) свойства в**УдалитьСкрытуюИнформацию()** метод[Diagram](https://reference.aspose.com/diagram/java)учебный класс. В приведенном ниже примере кода показано, как удалить скрытую информацию из diagram.


{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReduceFileSize.class);

// Load a Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Remove hidden information from diagram
diagram.removeHiddenInformation((int)(RemoveHiddenInfoItem.SHAPES | RemoveHiddenInfoItem.MASTERS));
{{< /highlight >}}

