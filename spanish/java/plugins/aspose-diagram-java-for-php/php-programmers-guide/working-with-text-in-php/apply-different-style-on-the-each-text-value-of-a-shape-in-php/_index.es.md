---
title: Aplique un estilo diferente en cada valor de texto de una forma en PHP
type: docs
weight: 20
url: /es/java/apply-different-style-on-the-each-text-value-of-a-shape-in-php/
---
## **Aspose.Diagram - Aplicar un estilo diferente en cada valor de texto de una forma**
 Para aplicar un estilo diferente en cada valor de texto de una forma usando**Aspose.Diagram Java para PHP** , simplemente invocar**AñadirShapeTextAndStyles** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

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
## **Descargar código de ejecución**
 Descargar**Aplicar un estilo diferente en cada valor de texto de una forma (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithText/AddShapeTextAndStyles.php)
