---
title: Alanları Güncelle, Kaldır
type: docs
weight: 20
url: /tr/net/update-remove-fields/
description: Bu bölümde alanların nasıl güncelleneceği veya kaldırılacağı açıklanmaktadır.
---
## **Alanı Güncelle**
 Aspose.Diagram for .NET güncellemenizi ve kaldırmanızı sağlar[alan](https://reference.aspose.com/diagram/net/aspose.diagram/field) Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio şemaları.

 bu[Alan](https://reference.aspose.com/diagram/net/aspose.diagram/field) nesne bir metin alanını temsil eder[Metin](https://reference.aspose.com/diagram/net/aspose.diagram/text) koşmak. tarafından gösterilen alan özelliği[Şekil](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) class, Aspose.Diagram.Field nesnelerinin bir koleksiyonunu destekler.
### **Programlama Örneği**
Aşağıdaki kod parçası güncelleme alanı şeklindedir.
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_UpdateField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Get field
Field fld = shape.Fields[0];
//Update format of field
fld.Format.Val = "";
fld.Format.Ufev.Unit = MeasureConst.Undefined;
fld.Format.Ufev.F = "";

//Update value of field
fld.Value.Val = "1";
fld.Value.Ufev.F = "";
fld.Value.Ufev.Unit = MeasureConst.Undefined;

// Save diagram 
diagram.Save(dataDir + "UpdateField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```

### **Alanı Kaldır**
Aşağıdaki kod parçası, şekildeki alanı kaldırır.
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_RemoveField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Get field
Field fld = shape.Fields[0];
//Remove field
shape.Fields.Remove(fld);

// Save diagram 
diagram.Save(dataDir + "RemoveField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
