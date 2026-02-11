---
title: Работа с элементами SolutionXML
type: docs
weight: 110
url: /ru/net/working-with-solutionxml-elements/
description: В этом разделе объясняется, как добавить solutionXml или получить значения xml из элемента solutionXml с номером Aspose.Diagram.
---
## **Добавьте элемент SolutionXML в чертеж Visio**
 SolutionXML — это правильно сформированный XML, содержащийся в элементе SolutionXML, который предоставляет стандартизированные средства сохранения данных решения. Пользователи могут хранить SolutionXML на уровне документа, где он сохраняется непосредственно в элементе VisioDocument. Как правило, это самый простой способ сохранить и получить SolutionXML с помощью[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) класс представляет элемент SolutionXML в чертежах Visio. Метод Add, предоставляемый[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) класс позволяет добавить элемент SolutionXML.
### **Добавить пример программирования элемента SolutionXML**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// Set name
solXML.Name = "Solution XML";
// Set xml value
solXML.XmlValue = "XML Value";
// Add SolutionXML element
diagram.SolutionXMLs.Add(solXML);

// Save Visio diagram
diagram.Save(dataDir + "AddSolutionXMLElement_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
## **Чтение значений XML из элемента SolutionXML**
SolutionXML — это правильно сформированный XML, содержащийся в элементе SolutionXML, который предоставляет стандартизированные средства сохранения данных решения. Пользователи могут читать значения XML из элемента SolutionXML, используя[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 Свойство SolutionXMLs, предоставляемое[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) class поддерживает набор объектов Aspose.Diagram.SolutionXML. Это свойство можно использовать для чтения значений XML из элемента SolutionXML.
### **Чтение примера программирования элемента SolutionXML**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_SolutionXML();

// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// Iterate through SolutionXML elements
foreach (SolutionXML solutionXML in diagram.SolutionXMLs)
{
    // Get name property
    Console.WriteLine(solutionXML.Name);
    // Get xml value
    Console.WriteLine(solutionXML.XmlValue);
}

{{< /highlight >}}
```
