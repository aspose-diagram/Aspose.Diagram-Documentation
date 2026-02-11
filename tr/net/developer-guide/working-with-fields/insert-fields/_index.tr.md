---
title: Oluştur, Alan ekle
type: docs
weight: 10
url: /tr/net/create-insert-fields/
description: C# Diagram API kullanarak alanlar nasıl oluşturulur, eklenir.
---
## **Alan ekle**
 Aspose.Diagram for .NET oluşturmanıza ve eklemenize izin verir[alan](https://reference.aspose.com/diagram/net/aspose.diagram/field) Microsoft Office Otomasyon olmadan kendi uygulamalarınız içinden Microsoft Visio şemaları.
### **Programlama Örneği**
```
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-diagram/Aspose.Diagram-for-.NET
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_InsertField();

// Create a new diagram
// Load source Visio diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get Visio page
Aspose.Diagram.Page page = diagram.Pages.GetPage("Page-1");

//Get Visio Shape
Shape shape = page.Shapes[0];
//Insert field
Field fld = new Field();
fld.Value.Val = "1";
shape.Fields.Add(fld);

// Save diagram 
diagram.Save(dataDir + "InsertField_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
```
