---
title: العمل مع عناصر SolutionXML
type: docs
weight: 140
url: /ar/java/working-with-solutionxml-elements/
---
## **أضف عنصر SolutionXML إلى رسم Visio**
 إن SolutionXML عبارة عن XML منسق بشكل جيد ومضمَّن في عنصر SolutionXML الذي يوفر وسيلة معيارية لبيانات الحل المستمرة. يمكن للمستخدمين تخزين SolutionXML على مستوى المستند ، حيث يتم تخزينه على الفور في عنصر VisioDocument. عادةً ما تكون هذه هي أسهل طريقة لتخزين واسترداد SolutionXML باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 ال[SolutionXML](https://reference.aspose.com/diagram/java/com.aspose.diagram/SolutionXML) تمثل class عنصر SolutionXML في رسومات Visio. طريقة الإضافة ، المكشوفة بواسطة[SolutionXML](http://www.aspose.com/api/java/diagram/com.aspose.diagram/classes/SolutionXML) class ، تسمح بإضافة عنصر SolutionXML.
### **أضف نموذجًا لبرمجة عنصر SolutionXML**

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

## **قراءة قيم XML من SolutionXML Element**
إن SolutionXML عبارة عن XML منسق بشكل جيد ومضمَّن في عنصر SolutionXML الذي يوفر وسيلة معيارية لبيانات الحل المستمرة. يمكن للمستخدمين قراءة قيم XML من عنصر SolutionXML باستخدام[Aspose.Diagram for Java](https://products.aspose.com/diagram/java/).

 الخاصية SolutionXMLs ، المكشوفة بواسطة ملف[Diagram](https://reference.aspose.com/diagram/java/com.aspose.diagram/Diagram) فئة ، تدعم مجموعة Aspose.Diagram.SolutionXML كائنات. يمكن استخدام هذه الخاصية لقراءة قيم XML من عنصر SolutionXML.
### **نموذج البرمجة لعنصر SolutionXML**

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

