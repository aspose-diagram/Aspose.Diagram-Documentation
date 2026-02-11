---
title: Работа с верхними и нижними колонтитулами
type: docs
weight: 140
url: /ru/net/working-with-headers-and-footers/
description: В этом разделе объясняется, как установить верхний и нижний колонтитулы Microsoft Office Visio с Aspose.Diagram.
---
## **Управление верхними и нижними колонтитулами диаграмм Visio**
[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/) предоставляет механизм для установки верхних и нижних колонтитулов диаграмм Microsoft Office Visio. Разработчики могут получить или задать текстовую строку, которая отображается слева, в центре и справа от верхнего/нижнего колонтитула документа. Они также могут устанавливать поля верхнего и нижнего колонтитула вместе со свойствами шрифта текста.
### **Настройка свойств верхних и нижних колонтитулов**
[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram)Объект класса предлагает свойство HeaderFooter, которое позволяет получать и устанавливать текст верхнего и нижнего колонтитула, значения шрифта и полей. Во время предварительного просмотра чертежа Visio пользователи могут нажать кнопку ссылки «Редактировать верхний и нижний колонтитулы» в Microsoft Visio 2013 (в Microsoft Visio 2010 >> кнопка «Верхний и нижний колонтитулы»). Есть несколько вариантов добавления текста, как показано на скриншоте ниже. Пользователи могут программно управлять этими свойствами с помощью Aspose.Diagram API следующим образом:
#### **Образец программирования**
Следующий фрагмент кода помогает управлять свойствами верхних и нижних колонтитулов.

```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_HeadersAndFooters();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Add page number at the right corner of header
diagram.HeaderFooter.HeaderRight = "&p";

// Set text at the center
diagram.HeaderFooter.HeaderCenter = "Center of the header";

// Set text at the left side
diagram.HeaderFooter.HeaderLeft = "Left of the header";

// Add text at the right corner of footer
diagram.HeaderFooter.FooterRight = "Right of the footer";

// Set text at the center
diagram.HeaderFooter.FooterCenter = "Center of the footer";

// Set text at the left side
diagram.HeaderFooter.FooterLeft = "Left of the footer";

// Set header & footer color
diagram.HeaderFooter.HeaderFooterColor = Color.AliceBlue;

// Set text font properties
diagram.HeaderFooter.HeaderFooterFont.Italic = BOOL.True;
diagram.HeaderFooter.HeaderFooterFont.Underline = BOOL.False;

// Save Visio diagram
diagram.Save(dataDir + "ManageHeadersandFooters_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
