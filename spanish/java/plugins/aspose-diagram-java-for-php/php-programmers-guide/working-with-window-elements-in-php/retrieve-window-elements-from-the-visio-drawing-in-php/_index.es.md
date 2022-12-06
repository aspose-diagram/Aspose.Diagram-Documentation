---
title: Recuperar elementos de ventana del dibujo Visio en PHP
type: docs
weight: 30
url: /es/java/retrieve-window-elements-from-the-visio-drawing-in-php/
---
## **Aspose.Diagram - Recuperar elementos de ventana del dibujo Visio**
 Para recuperar elementos de ventana del dibujo Visio usando**Aspose.Diagram Java para PHP** , simplemente invocar**Obtener elementos de ventana** módulo. Aquí puedes ver el código de ejemplo.

**Código PHP**

{{< highlight "php" >}}

 # Create instance of Diagram

$diagram = new Diagram($dataDir."Drawing.vsd");

$windows=$diagram->getWindows();

$i = 0;

while ($i<(int)(string)$windows->getCount()) {

$window=$windows->get($i);

print "ID: ".(string)$window->getID();

print "Type: ".(string)$window->getWindowType();

print "Window height: ".(string)$window->getWindowHeight();

print "Window width: ".(string)$window->getWindowWidth();

print"Window state: ".(string)$window->getWindowState();

$i+= 1;

}

{{< /highlight >}}
## **Descargar código de ejecución**
 Descargar**Recuperar elementos de ventana del dibujo Visio (Aspose.Diagram)**de cualquiera de los sitios de codificación social mencionados a continuación:

- [GitHub](https://github.com/asposediagram/Aspose.Diagram-for-Java/blob/master/Plugins/Aspose_Diagram_Java_for_PHP/src/aspose/diagram/WorkingwithWindowElements/GetWindowElements.php)
