---
title: 使用形状段落
type: docs
weight: 40
url: /zh/net/working-with-shapes-paragraph/
---
下面的代码显示了如何：

1. 加载示例文件。
1. 访问特定形状。
1. 设置形状的段落。
## **设置形状的段落编程示例**
在您的 .NET 应用程序中使用以下代码，使用 Aspose.Diagram for .NET 设置形状的段落。


{{< highlight csharp >}}
// ExStart:ApplyThemeToNewShape
// The path to the documents directory.
string dataDir = RunExamples.GetDataDir_Shapes();

// Load a diagram
Diagram diagram = new Diagram(dataDir + "Drawing1.vsdx");
// Get page by name
Page page = diagram.Pages.GetPage("Page-2");

// Add master with stencil file path and master name
string masterName = "Rectangle";
diagram.AddMaster(dataDir + "Basic Shapes.vss", masterName);

// Page indexing starts from 0
int PageIndex = 1;
double width = 2, height = 2, pinX = 4.25, pinY = 4.5;
// Add a new rectangle shape
long rectangleId = diagram.AddShape(pinX, pinY, width, height, masterName, PageIndex);

// Set shape properties 
Shape rectangle = page.Shapes.GetShape(rectangleId);

//Get shape's paragraph
Para para = rectangle.Paras[0];

//Set horizontal of paragraph
para.HorzAlign.Value = HorzAlignValue.LeftAlign;

//Set left indent of paragraph
para.IndLeft.Value = 0.1;

//Set Right indent of paragraph
para.IndRight.Value = 0.1;

//Set First indent of paragraph
para.IndFirst.Value = 0.1;

//Set the amount of space inserted before each paragraph in the shape's text block
para.SpBefore.Value = 0.1;

//Set the amount of space inserted after each paragraph in the shape's text block
para.SpAfter.Value = 0.1;

//Set the distance between one line of text and the next, where 100% is the height of a text line.
para.SpLine.Value = 0.1;

//Set Bullet string of paragraph
para.BulletStr.Value = "";

//Set Bullet string of paragraph
para.Bullet.Value = BulletValue.Style1;

diagram.Save(dataDir + "SettingParagraphOfShape_out.vsdx", SaveFileFormat.VSDX);

{{< /highlight >}}
