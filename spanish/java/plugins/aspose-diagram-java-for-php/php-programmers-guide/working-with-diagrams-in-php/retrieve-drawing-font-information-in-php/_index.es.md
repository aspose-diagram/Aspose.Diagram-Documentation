---
title: Recuperar información de fuentes de dibujo en PHP
type: docs
weight: 40
url: /es/java/retrieve-drawing-font-information-in-php/
---
## **Aspose.Diagram - Recuperar información de fuente de dibujo**
 Para recuperar información de fuentes de dibujo usando**Aspose.Diagram Java para PHP** , simplemente invocar**ObtenerDiagramFontInfo** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."drawing.vsd");

$fonts = $diagram->getFonts();

$i = 0;

while ($i<sizeof($fonts->getCount())) {

$font = $fonts->get($i);

\# Display information about the fonts

print $font->getName();

$i+=1;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar información de fuente de dibujo (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithDiagrams/GetDiagramFontInfo.php)
