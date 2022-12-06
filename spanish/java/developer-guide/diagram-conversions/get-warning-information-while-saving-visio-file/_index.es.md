---
title: Obtenga información de advertencia al guardar el archivo Visio
type: docs
weight: 110
url: /es/java/get-warning-information-while-saving-visio-file/
---
## **Posibles escenarios de uso**

 A veces, el usuario intenta guardar el diagram que contiene texto que no tiene una fuente local. En tal caso, Aspose.Diagram arroja advertencias mientras guarda el diagram. Puede detectar estas advertencias implementando el**[IWarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback)** interfaz y configuración**[SaveOptions.WarningCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/saveoptions/properties/warningcallback)**propiedad.

## **Recibe advertencias al guardar el archivo Visio**

 El siguiente código de ejemplo explica cómo obtener advertencias al guardar el archivo visio. El código convierte el[muestra visio archivo](sampleFontSubstitution.vsdx) que lanza**[Sustitución de fuentes](https://reference.aspose.com/diagram/net/aspose.diagram/warningtype)** advertencia sobre el ahorro. Esta advertencia es captada por**[IWarningCallback.Warning()](https://reference.aspose.com/diagram/net/aspose.diagram/iwarningcallback/methods/warning)**método que imprime los mensajes de advertencia en la consola. Consulte también la salida de la consola del código que se proporciona a continuación para obtener más información.

## **Código de muestra**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-GetWarningInformation.cs" >}}

## **Salida de consola**

Aquí está la salida de la consola del código anterior cuando se ejecuta con el proporcionado[muestra visio archivo](sampleFontSubstitution.vsdx).

{{< highlight "java" >}}
Font substitution: Font [ Athene Logos ]has been substituted by Font[Times New Roman]{{< /highlight >}}
