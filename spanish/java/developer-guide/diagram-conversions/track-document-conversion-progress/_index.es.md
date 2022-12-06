﻿---
title: Seguimiento del progreso de la conversión de documentos
type: docs
weight: 970
url: /es/java/track-document-conversion-progress/
description: Esta sección explica cómo rastrear el progreso de conversión de archivos visio con Aspose.Diagram.
---
## **Posibles escenarios de uso**

A veces, la conversión de archivos grandes visio puede llevar algún tiempo. Durante este tiempo, es posible que desee mostrar el progreso de la conversión del documento en lugar de solo una pantalla de carga para mejorar la usabilidad de su aplicación. Aspose.Diagram admite el proceso de conversión de documentos de seguimiento al proporcionar la interfaz IPageSavingCallback. La interfaz IPageSavingCallback proporciona métodos PageStartSaving y PageEndSaving que puede implementar en su clase personalizada. También puede controlar qué páginas se procesan como se muestra en la T*estDiagramPageSavingCallback*clase personalizada.

## **Seguimiento del progreso de la conversión de documentos**

 El siguiente ejemplo de código carga el[fuente visio archivo](Drawing1.vsdx) e imprime su progreso de conversión en la consola usando el*TestPageSavingCallback*clase personalizada que implementa la interfaz IPageSavingCallback.

## **Código de muestra**

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

El siguiente es el código para el*TestDiagramPageSavingCallback*clase personalizada.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-Introduction-DetectFormatfromInputStream-DetectFormatfromInputStream.java" >}}

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
