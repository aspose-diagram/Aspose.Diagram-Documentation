﻿---
title: Seguimiento del progreso de la conversión de documentos
type: docs
weight: 970
url: /es/net/track-document-conversion-progress/
description: Esta sección explica cómo rastrear el progreso de conversión de archivos visio con Aspose.Diagram.
---
## **Posibles escenarios de uso**

 A veces, la conversión de archivos grandes visio puede llevar algún tiempo. Durante este tiempo, es posible que desee mostrar el progreso de la conversión del documento en lugar de solo una pantalla de carga para mejorar la usabilidad de su aplicación. Aspose.Diagram admite el proceso de conversión de documentos de seguimiento al proporcionar el**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)** interfaz. los**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**interfaz proporciona**[PageStartSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pagestartsaving)**y**[PageEndSaving](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback/methods/pageendsaving)**métodos que puede implementar en su clase personalizada. También puede controlar qué páginas se procesan como se muestra en la T*estDiagramPageSavingCallback*clase personalizada.

## **Seguimiento del progreso de la conversión de documentos**

 El siguiente ejemplo de código carga el[fuente visio archivo](Drawing1.vsdx) e imprime su progreso de conversión en la consola usando el*TestPageSavingCallback* clase personalizada que implementa el**[IPageSavingCallback](https://reference.aspose.com/diagram/net/aspose.diagram.saving/ipagesavingcallback)**interfaz.

## **Código de muestra**

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-1.cs" >}}

El siguiente es el código para el*TestDiagramPageSavingCallback*clase personalizada.

{{< gist "aspose-diagram-gists" "efd56218048f8b0ab925efd494227fdd" "Examples-CSharp-DiagramConversions-DocumentConversionProgress-2.cs" >}}

## **Salida de consola**

Empezar a guardar el índice de la página 0 de las páginas 11</br>
Terminar de guardar el índice de página 0 de las páginas 11</br>
Empezar a guardar el índice de la página 1 de las páginas 11</br>
Terminar de guardar el índice de página 1 de las páginas 11</br>
Empezar a guardar el índice de la página 2 de las páginas 11</br>
Terminar de guardar el índice de la página 2 de las páginas 11</br>
Empezar a guardar el índice de la página 3 de las páginas 11</br>
Terminar de guardar el índice de la página 3 de las páginas 11</br>
Comience a guardar el índice de la página 4 de las páginas 11</br>
Terminar de guardar el índice de página 4 de las páginas 11</br>
Empezar a guardar el índice de la página 5 de las páginas 11</br>
Terminar de guardar el índice de la página 5 de las páginas 11</br>
Comience a guardar el índice de la página 6 de las páginas 11</br>
Terminar de guardar el índice de página 6 de las páginas 11</br>
Empezar a guardar el índice de la página 7 de las páginas 11</br>
Terminar de guardar el índice de página 7 de las páginas 11</br>
Empezar a guardar el índice de la página 8 de las páginas 11</br>
Terminar de guardar el índice de la página 8 de las páginas 11
