---
title: Работа с элементами SolutionXML
type: docs
weight: 140
url: /ru/java/working-with-solutionxml-elements/
---
## **Добавьте элемент SolutionXML в чертеж Visio**
 SolutionXML — это правильно сформированный XML, содержащийся в элементе SolutionXML, который предоставляет стандартизированные средства сохранения данных решения. Пользователи могут хранить SolutionXML на уровне документа, где он сохраняется непосредственно в элементе VisioDocument. Как правило, это самый простой способ сохранить и получить SolutionXML с помощью[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

[SolutionXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) класс представляет элемент SolutionXML в чертежах Visio. Метод Add, предоставляемый[SolutionXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) класс позволяет добавить элемент SolutionXML.
### **Добавить пример программирования элемента SolutionXML**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(AddSolutionXMLElement.class);  
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// initialize SolutionXML object
SolutionXML solXML = new SolutionXML();
// set name
solXML.setName("Solution XML");
// set xml value
solXML.setXmlValue("XML Value");
// add SolutionXML element
diagram.getSolutionXMLs().add(solXML);

// save Visio diagram
diagram.save(dataDir + "AddSolutionXMLElement_Out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}

## **Чтение значений XML из элемента SolutionXML**
SolutionXML — это правильно сформированный XML, содержащийся в элементе SolutionXML, который предоставляет стандартизированные средства сохранения данных решения. Пользователи могут читать значения XML из элемента SolutionXML, используя[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 Свойство SolutionXMLs, предоставляемое[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) class поддерживает набор объектов Aspose.Diagram.SolutionXML. Это свойство можно использовать для чтения значений XML из элемента SolutionXML.
### **Чтение примера программирования элемента SolutionXML**

{{< highlight java >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-Java
// The path to the documents directory.
String dataDir = Utils.getDataDir(ReadSolutionXMLElement.class);   
// load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");

// iterate through SolutionXML elements
for (SolutionXML solutionXML :(Iterable<SolutionXML>) diagram.getSolutionXMLs())
{
    // get name property
    System.out.println(solutionXML.getName());
    // get xml value
    System.out.println(solutionXML.getXmlValue());
}

{{< /highlight >}}

