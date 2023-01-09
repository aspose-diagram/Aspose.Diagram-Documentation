---
title: Trabajar con orígenes de datos externos
type: docs
weight: 190
url: /es/java/working-with-external-data-sources/
---
## **Actualizar conexión de datos del dibujo Visio**
Aspose.Diagram API permite a los usuarios editar la conexión de datos de SQL Server del dibujo Visio vinculado. Para traer datos al dibujo Visio, necesitamos acceso a los datos de SQL Server. Asegúrese de que la base de datos no esté abierta en modo exclusivo.

 Ahora es un fenómeno común vincular los datos de los diagramas Microsoft Visio de las fuentes de datos externas. los[DataConnectionCollectionDataConnectionCollection](https://reference.aspose.com/diagram/java/com.aspose.diagram/dataconnectioncollection) La clase contiene todas las conexiones de datos.
### **Ejemplo de programación**
El siguiente fragmento de código edita una conexión de datos en particular y también actualiza todos los conjuntos de registros disponibles en Visio diagram.

{{< gist "aspose-diagram-gists" "a970e3b0531843f718d7f46abf12d56a" "Examples-src-main-java-com-aspose-diagram-examples-ExternalDataSources-EditDataConAndRefreshRecords-EditDataConAndRefreshRecords.java" >}}
