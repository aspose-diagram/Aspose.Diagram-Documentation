---
title: Печать Diagram в VSTO и Aspose.Diagram
type: docs
weight: 100
url: /ru/net/printing-a-diagram-in-vsto-and-aspose-diagram/
---
## **ВСТО**
Ниже приведен код, показывающий, как напечатать diagram:

{{< highlight "cs" >}}

   Application.ActiveDocument.Print();

{{< /highlight >}}
## **Aspose.Diagram**
 Печать diagram на**принтер по умолчанию** довольно просто в Aspose.Diagram for .NET. Выполните следующие шаги, чтобы распечатать diagram на принтере по умолчанию:

- Создайте экземпляр класса Diagram для загрузки diagram, который должен быть напечатан.
- Вызовите метод Print без параметров, предоставляемых объектом Diagram.

 Печать diagram на**конкретный принтер** требуется имя принтера в качестве параметра метода печати Diagram. Выполните следующие шаги, чтобы распечатать diagram на нужном принтере:

- Создайте экземпляр класса Diagram для загрузки diagram, который должен быть напечатан.
- Вызовите метод Print класса Diagram с именем принтера в качестве строкового параметра для метода Print.

Ниже приведен код использования по умолчанию и конкретного принтера:

{{< highlight "cs" >}}

  string FilePath = "demo.vsd";

 //Load the diagram

 Diagram diagram = new Diagram(FilePath);

 //Call the print method to print whole Diagram to the default printer

 diagram.Print();

 //Call the print method to print whole Diagram to the desired printer

 diagram.Print("LaserJet1100");

 PrinterSettings settings = new PrinterSettings();

 settings.PrinterName = "LaserJet1100";

 //Call the print method to print whole Diagram to the desired printer and set document name in print job

 diagram.Print(settings, "Job name while printing with Aspose.Diagram");


{{< /highlight >}}
## **Скачать пример кода**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/releases/tag/AsposeDiagramVsVSTOv1.1)
## **Скачать рабочий код**
- [Гитхаб](https://github.com/aspose-diagram/Aspose.Diagram-for-.NET/tree/master/Plugins/Aspose.Diagram%20Vs%20VSTO%20Visio/Code%20Comparison%20of%20Common%20Features/Printing%20a%20Diagram)
