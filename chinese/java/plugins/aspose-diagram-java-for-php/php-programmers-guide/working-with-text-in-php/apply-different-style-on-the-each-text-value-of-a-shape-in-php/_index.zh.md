---
title: 在 PHP 中对形状的每个文本值应用不同的样式
type: docs
weight: 20
url: /zh/java/apply-different-style-on-the-each-text-value-of-a-shape-in-php/
---
## **Aspose.Diagram - 对形状的每个文本值应用不同的样式**
要在形状的每个文本值上应用不同的样式，请使用**Aspose.Diagram Java 用于 PHP** 只需调用**添加形状文本和样式**模块。在这里您可以看到示例代码。

**PHP代码**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

\# Get a particular shape

$shape=$diagram->getPages()->getPage("Flow 1")->getShapes()->getShape(1);

\# Clear shape text values and chars

$shape->getText()->getValue()->clear();

$shape->getChars()->clear();

\# Mark character run and add text

$shape->getText()->getValue()->add(new Cp(0));

$shape->getText()->getValue()->add(new Txt("TextStyle_Regular"));

$shape->getText()->getValue()->add(new Cp(1));

$shape->getText()->getValue()->add(new Txt("TextStyle_Bold_Italic"));

$shape->getText()->getValue()->add(new Cp(2));

$shape->getText()->getValue()->add(new Txt("TextStyle_Underline_Italic"));

$shape->getText()->getValue()->add(new Cp(3));

$shape->getText()->getValue()->add(new Txt("TextStyle_Bold_Italic_Underline"));

\# Add formatting characters

$shape->getChars()->add(new Char());

$shape->getChars()->add(new Char());

$shape->getChars()->add(new Char());

$shape->getChars()->add(new Char());

$style_value = new StyleValue();

\# Set properties e.g. color, font, size and style etc.

$shape->getChars()->getChar(0)->setIX(0);

$shape->getChars()->getChar(0)->getColor()->setValue("#FF0000");

$shape->getChars()->getChar(0)->getFont()->setValue(4);

$shape->getChars()->getChar(0)->getSize()->setValue(0.22);

$shape->getChars()->getChar(0)->getStyle()->setValue($style_value->UNDEFINED);

\# Set properties e.g. color, font, size and style etc.

$shape->getChars()->getChar(1)->setIX(1);

$shape->getChars()->getChar(1)->getColor()->setValue("#FF00FF");

$shape->getChars()->getChar(1)->getFont()->setValue(4);

$shape->getChars()->getChar(1)->getSize()->setValue(0.22);

(int)(string)$shape->getChars()->getChar(1)->getStyle()->setValue((string)$style_value->BOLD | (string)$style_value->ITALIC);

\# Set properties e.g. color, font, size and style etc.

$shape->getChars()->getChar(2)->setIX(2);

$shape->getChars()->getChar(2)->getColor()->setValue("#00FF00");

$shape->getChars()->getChar(2)->getFont()->setValue(4);

$shape->getChars()->getChar(2)->getSize()->setValue(0.22);

(int)(string)$shape->getChars()->getChar(2)->getStyle()->setValue((string)$style_value->UNDERLINE | (string)$style_value->ITALIC);

\# Save diagram

$saveFileFormat=new SaveFileFormat();

$diagram->save($dataDir."AddShapeTextAndStyles.vdx", $saveFileFormat->VDX);

print "Added shape text and styles.".PHP_EOL;

{{< /highlight >}}
## **下载运行代码**
下载**对形状的每个文本值应用不同的样式 (Aspose.Diagram)**来自以下任何社交编码网站：

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/AddShapeTextAndStyles.php)
