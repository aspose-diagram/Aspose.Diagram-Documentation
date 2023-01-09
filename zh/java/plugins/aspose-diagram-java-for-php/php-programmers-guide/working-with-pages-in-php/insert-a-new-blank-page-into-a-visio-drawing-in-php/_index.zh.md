---
title: 在 Visio PHP 绘图中插入一个新的空白页
type: docs
weight: 20
url: /zh/java/insert-a-new-blank-page-into-a-visio-drawing-in-php/
---
## **Aspose.Diagram - 将新的空白页插入到 Visio 绘图中**
要将新的空白页插入到 Visio 绘图中，请使用**Aspose.Diagram Java 用于 PHP** 只需调用**添加页面**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Call the diagram constructor to load diagram from a VSD file

$diagram = new Diagram($dataDir."drawing.vsd");

\# Get max page ID

$max_page_id = $diagram->getPages()->getPage(0)->getID();

$i = 1;

while ($i<(int)(string)$diagram->getPages()->getCount()) {

if ($max_page_id<$diagram->getPages()->getPage($i)->getID()){

$max_page_id=$diagram->getPages()->getPage($i)->getID();

}

$i+=1;

}

\# Initialize a new page object

$new_page = new Page();

\# Set name

$new_page->setName("new page");

\# Set page ID

$new_page->setID((int)(string)$max_page_id+1);

\# Or try the Page constructor

\# Page newPage = new Page(MaxPageId + 1);

\# Add a new blank page

$diagram->getPages()->add($new_page);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."NewPage_Output.vdx", $saveFileFormat->VDX);

print "Added new page.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**将新空白页插入 Visio 绘图 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithPages/AddPage.php)
