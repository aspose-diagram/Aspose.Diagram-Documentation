---
title: العمل مع عناصر SolutionXML
type: docs
weight: 110
url: /ar/net/working-with-solutionxml-elements/
description: يشرح هذا القسم كيفية إضافة solutionXml أو الحصول على قيم xml من عنصر solutionXml مع Aspose.Diagram.
---
## **أضف عنصر SolutionXML إلى رسم Visio**
 إن SolutionXML عبارة عن XML منسق بشكل جيد ومضمَّن في عنصر SolutionXML الذي يوفر وسيلة معيارية لبيانات الحل المستمرة. يمكن للمستخدمين تخزين SolutionXML على مستوى المستند ، حيث يتم تخزينه على الفور في عنصر VisioDocument. عادةً ما تكون هذه هي أسهل طريقة لتخزين واسترداد SolutionXML باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 ال[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) تمثل class عنصر SolutionXML في رسومات Visio. طريقة الإضافة ، المكشوفة بواسطة[SolutionXML](http://www.aspose.com/api/net/diagram/aspose.diagram/solutionXML) class ، تسمح بإضافة عنصر SolutionXML.
### **أضف نموذجًا لبرمجة عنصر SolutionXML**
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
## **قراءة قيم XML من SolutionXML Element**
إن SolutionXML عبارة عن XML منسق بشكل جيد ومضمَّن في عنصر SolutionXML الذي يوفر وسيلة معيارية لبيانات الحل المستمرة. يمكن للمستخدمين قراءة قيم XML من عنصر SolutionXML باستخدام[Aspose.Diagram for .NET](https://products.aspose.com/diagram/net/).

 الخاصية SolutionXMLs ، المكشوفة بواسطة ملف[Diagram](http://www.aspose.com/api/net/diagram/aspose.diagram/diagram) فئة ، تدعم مجموعة Aspose.Diagram.SolutionXML كائنات. يمكن استخدام هذه الخاصية لقراءة قيم XML من عنصر SolutionXML.
### **نموذج البرمجة لعنصر SolutionXML**
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
