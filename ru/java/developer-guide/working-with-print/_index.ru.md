---
title: Работа с печатью
type: docs
weight: 80
url: /ru/java/working-with-print/
---
## **Печать Diagram**
[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/) предоставляет четыре метода перегрузки для печати диаграмм. Эти методы достаточно гибкие, чтобы распечатать diagram на принтере по умолчанию или на любом доступном принтере с индивидуальными настройками. Вам нужно только выбрать подходящий метод печати в соответствии с требованиями.
### **Печать на указанный принтер**
Для печати diagram на конкретном принтере требуется имя принтера в качестве параметра метода печати Diagram. Выполните следующие шаги, чтобы напечатать diagram на нужном принтере:

- Создайте экземпляр класса Diagram для загрузки diagram, который должен быть напечатан.
- Вызовите метод Print класса Diagram с именем принтера в качестве строкового параметра для метода Print.
#### **Пример программирования печати на конкретном принтере**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(BySpecificPrinter.class); 
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name
diagram.print("LaserJet1100");

{{< /highlight >}}

### **Установка имени принтера и документа**
Aspose.Diagram API позволяет задать конкретный принтер и имя документа для задания на печать. Выполните следующие шаги, чтобы распечатать diagram на нужном принтере:

- Создайте экземпляр класса Diagram для загрузки diagram, который должен быть напечатан.
- Вызовите метод Print класса Diagram с принтером и именем документа в качестве строкового параметра для метода Print.
#### **Пример программирования установки имени принтера и документа**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(SetPrintJobAndPrinterName.class);   
// load a source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// call the print method to print whole Diagram using the printer name and set document name in the print job
diagram.print("LaserJet1100", "Job name while printing with Aspose.Diagram");

{{< /highlight >}}

