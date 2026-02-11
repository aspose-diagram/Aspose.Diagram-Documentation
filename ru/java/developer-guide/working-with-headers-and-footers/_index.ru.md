---
title: Работа с верхними и нижними колонтитулами
type: docs
weight: 150
url: /ru/java/working-with-headers-and-footers/
---
{{% alert color="primary" %}} 

Aspose.Diagram for Java предоставляет механизм для установки верхних и нижних колонтитулов диаграмм Microsoft Office Visio. Разработчики могут получить или задать текстовую строку, которая отображается слева, в центре и справа от верхнего/нижнего колонтитула документа. Они также могут устанавливать поля верхнего и нижнего колонтитула вместе со свойствами шрифта текста.

{{% /alert %}} 
### **Настройка свойств верхних и нижних колонтитулов**
[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/diagram)Объект класса предлагает свойство HeaderFooter, которое позволяет получать и устанавливать текст верхнего и нижнего колонтитула, значения шрифта и полей. Во время предварительного просмотра чертежа Visio пользователи могут нажать кнопку ссылки «Редактировать верхний и нижний колонтитулы» в Microsoft Visio 2013 (в Microsoft Visio 2010 >> кнопка «Верхний и нижний колонтитулы»). Есть несколько вариантов добавления текста, как показано на скриншоте ниже. Пользователи могут программно управлять этими свойствами с помощью Aspose.Diagram API следующим образом:

**Управляйте текстом верхних и нижних колонтитулов, полями и свойствами шрифта.** 

![дело:изображение_альтернативный_текст](working-with-headers-and-footers_1.png)

Следующий фрагмент кода помогает управлять свойствами верхних и нижних колонтитулов.
#### **Примеры программирования**
```
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ManageHeadersandFooters.class);
// call the diagram constructor to a load Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// add page number at the right corner of header
diagram.getHeaderFooter().setHeaderRight("&p");

// set text at the center
diagram.getHeaderFooter().setHeaderCenter("Center of the header");

// set text at the left side
diagram.getHeaderFooter().setHeaderLeft("Left of the header");

// add text at the right corner of footer
diagram.getHeaderFooter().setFooterRight("Right of the footer");

// set text at the center
diagram.getHeaderFooter().setFooterCenter("Center of the footer");

// set text at the left side
diagram.getHeaderFooter().setFooterLeft("Left of the footer");

// set header & footer color
diagram.getHeaderFooter().setHeaderFooterColor(Color.getRed());

// set text font properties
diagram.getHeaderFooter().getHeaderFooterFont().setItalic(BOOL.TRUE);
diagram.getHeaderFooter().getHeaderFooterFont().setUnderline(BOOL.FALSE);

// save Visio diagram
diagram.save(dataDir + "EditConnectorGeometry_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
