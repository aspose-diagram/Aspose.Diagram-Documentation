---
title: 在 PHP 中读取 Shape 的用户定义单元格
type: docs
weight: 20
url: /zh/java/read-shape-s-user-defined-cells-in-php/
---
## **Aspose.Diagram - 读取形状的用户定义单元格**
使用读取形状的用户定义单元格**Aspose.Diagram Java 用于 PHP** 只需调用**读取用户定义的单元格**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir . "drawing.vdx");

$shapes = $diagram->getPages()->getPage("Flow 1")->getShapes();

$i = 0;

while($i<(int)(string)$shapes->getCount()) {

$shape=$shapes->get($i);

if($shape->getNameU()=="Process") {

$users = $shape->getUsers();

$j = 0;

while ($j<(int)(string)$users->getCount()) {

$user = $users->get($j);

print $user->getName() . ": " . $user->getValue()->getVal();

$j += 1;

}

break;

}

$i+=1;

}

{{< /highlight >}}
## **下载运行代码**
下载**读取形状的用户定义单元格 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithUserdefinedCells/ReadUserDefinedCells.php)
